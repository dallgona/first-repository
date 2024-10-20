AIFFEL Data Scientist Campus Code Peer Review

코더 : 손지현

리뷰어 : 김진형

🔑 **PRT(Peer Review Template)**

[V]  **1. 주어진 문제를 해결하는 완성된 코드가 제출되었나요?**

문제해결이 완성된 코드가 제출되었음.
    
[V]  **2. 전체 코드에서 핵심적이거나 복잡하고 이해하기 어려운 부분에 작성된 주석 또는 doc string을 보고 해당 코드가 잘 이해되었나요?**

    # 입금 메서드
    def deposit(self, money):
        if money >= 1:  # 입금은 최소 1원 이상 가능
            self.balance += money
            self.deposit_count += 1  # 입금 횟수 증가
            self.deposit_log.append(money)  # 입금 내역 기록
            print(f"{money:,}원이 입금되었습니다. 현재 잔액은 {self.balance:,}원 입니다.")

            # 입금 횟수가 5회일 때 잔고의 1% 이자 지급
            if self.deposit_count % 5 == 0:
                interest = self.balance * 0.01
                self.balance += interest
                self.deposit_log.append(interest)  # 이자 지급 내역 기록
                print(f'{interest:,}원이 지급되었습니다. 현재 잔액은 {self.balance:,}원 입니다.')
        else:
            print('입금은 최소 1원이상 가능합니다.')

    # 출금 메서드
    def withdraw(self, money):
        if money > self.balance:
            print("잔액 부족으로 출금할 수 없습니다.")
        else:
            self.balance -= money
            self.withdraw_log.append(money)  # 출금 내역 기록
            print(f"{money:,}원이 출금되었습니다. 현재 잔액은 {self.balance:,}원 입니다.")

입출금, 이자 지급 내역 출력 메서드가 핵심이라 생각함. 
설명이 필요한 부분에 주석이 간결하게 정리되어 있음. 주석을 보고 코드 이해가 잘 되었다고 판단함.

[V]  **3. 에러가 난 부분을 디버깅하여 문제를 “해결한 기록"을 남겼거나 "새로운 시도 
또는 추가 실험"을 수행해봤나요?**

에러 관련해 디버깅 문제 해결 기록은 찾을 수 없어서 문제를 잘 해결해서 결과물 산출했다고 판단함.
        
[V]  **4. 회고를 잘 작성했나요?**
회고는 작성되지 않았음.

[V]  **5. 코드가 간결하고 효율적인가요?**
간결하고 효율적으로 작성되었다고 판단됨. 스타일 가이드 (PEP8)를 준수하였는지는 잘 판단이 안되지만 코드 중복을 피해 잘 작성되었다고 생각됨.

---
### 참고 문헌




