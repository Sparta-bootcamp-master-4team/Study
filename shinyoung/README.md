# 📝 면접 질문 정리

---

## 📅 2025-05-14

### 질문 1
**Q.** iOS 앱에서 데이터를 저장하는 방법에는 어떤 것들이 있나요?

**A.**  
    `UserDefaults`로 간단한 설정 값을 저장하고 이미지, PDF, JSON 등을 `FileManager`를 통해 파일 단위로 저장할 수 있습니다.  
    토큰, 비밀번호 등 민감 정보는 `Keychain`에 저장할 수 있습니다.  
    엔터티 간 관계나 쿼리가 필요한 경우 관계형 모델의 영구 저장소인 `Core Data`를 사용할 수 있습니다.  
    SQL 쿼리를 직접 제어하고 싶을 때는 `SQLite`로 경량 데이터베이스를 직접 사용할 수 있습니다.  
    서드파티 NoSQL 데이터베이스인 `Realm`을 사용하면 Core Data 보다 더 직관적이고 빠르게 모델을 저장할 수 있습니다.

    데이터의 복잡도에 따라 UserDefaults와 Keychain은 Key-Value 등 비교적 단순한 단일값을 다루며 
    CoreData, Realm, FileManager, SQLite는 여러 속성, 관계, 리스트, 복합 타입 등 구조화된 데이터를 다룹니다.
    UserDefaults와 Keychain은 앱 설정이나 사용자 기본 정보를 Key로 직접 접근할 수 있으며 데이터간 관계가 거의 없거나 약합니다.
    CoreData, Realm, FileManager, SQLite는 앱의 주요 컨텐츠나 기능을 위한 데이터를 저장하며 조건 검색, 정렬, 필터링, 기능을 제공합니다.

---
