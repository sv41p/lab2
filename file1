#include <iostream>
#include <string>
using namespace std;

class ATC {
private:
    string address;      // Адрес АТС
    int subscriberCount;      // Число абонентов
    double subscriptionFee;    // Абонентская плата

public:
    ATC(const string& addr, int count, double fee)
        : address(addr), subscriberCount(count), subscriptionFee(fee) {}

    void setAddress(const string& addr) {
        address = addr;
    }

    void setSubscriberCount(int count) {
        subscriberCount = count;
    }

    void setSubscriptionFee(double fee) {
        subscriptionFee = fee;
    }

    double calculateTotalSubscriptionFee() const {
        return subscriberCount * subscriptionFee;
    }

    void displayInfo() const {
        cout << "Адрес: " << address << endl;
        cout << "Количество абонентов: " << subscriberCount << endl;
        cout << "Абонентская плата: " << subscriptionFee << endl;
        cout << "Абонентская плата для всех клиентов: " << calculateTotalSubscriptionFee() << endl;
    }
};

int main() {
    setlocale(LC_ALL, "RU");

    string address;
    int subscriberCount;
    double subscriptionFee;

    cout << "Введите адрес ATC: ";
    getline(cin, address);

    
    do {
        cout << "Введите количество абонентов: ";
        cin >> subscriberCount;
        if (subscriberCount >= 100) {
            cout << "Ошибка: количество абонентов должно быть менее 100." << endl;
        }
    } while (subscriberCount >= 100);

    
    do {
        cout << "Введите стоимость абонентской платы: ";
        cin >> subscriptionFee;
        if (subscriptionFee >= 10000) {
            cout << "Ошибка: стоимость абонентской платы должна быть менее 10000." << endl;
        }
    } while (subscriptionFee >= 10000);

    // Создание объекта ATC
    ATC atc(address, subscriberCount, subscriptionFee);
    atc.displayInfo();

    return 0;
}
