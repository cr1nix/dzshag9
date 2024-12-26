class CurrencyConverter:
    def __init__(self, exchange_rate):
        self.exchange_rate = exchange_rate

    def uah_to_usd(self, amount_uah):
        amount_usd = amount_uah / self.exchange_rate
        return amount_usd

if __name__ == "__main__":
    # Офіційний курс гривні до долара США на 23.12.2024
    exchange_rate = 41.8761

    converter = CurrencyConverter(exchange_rate)

    try:
        amount_uah = float(input("Введіть кількість гривень: "))
        amount_usd = converter.uah_to_usd(amount_uah)
        print(f"{amount_uah:.2f} грн = {amount_usd:.2f} доларів США")
    except ValueError:
        print("Будь ласка, введіть числове значення.")
