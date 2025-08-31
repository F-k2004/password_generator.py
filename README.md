# password_generator.py
import random
import string

def generate_password(length=12):
    chars = string.ascii_letters + string.digits + string.punctuation
    password = ''.join(random.choice(chars) for _ in range(length))
    return password

def main():
    print("🔑 تولیدکننده پسورد تصادفی")
    length = input("طول پسورد (پیش‌فرض 12): ")
    length = int(length) if length.isdigit() else 12

    pwd = generate_password(length)
    print(f"\n✅ پسورد شما: {pwd}")

if __name__ == "__main__":
    main()
