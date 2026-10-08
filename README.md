# CATCH_HOUSE_APP

Monorepo cho ứng dụng Catch House.

## Cấu trúc

| Thư mục    | Mô tả                                              |
|------------|----------------------------------------------------|
| `backend/` | REST API viết bằng Spring Boot (Maven, Java 21, MySQL) |
| `android/` | Ứng dụng Android native (Java, Gradle, `com.catchhouse.app`) |

## Nhánh

- `main`    : nhánh ổn định, chỉ nhận merge đã kiểm thử.
- `develop` : nhánh phát triển/tích hợp để test ứng dụng.

Quy trình: làm việc trên `develop` -> test -> merge vào `main`.

## Yêu cầu môi trường

- JDK 21 (backend) và JDK 17 (Android build).
- Maven 3.9+ để build backend.
- Android Studio (kèm Android SDK) để build/mở `android/`.

## Backend

```bash
cd backend
mvn spring-boot:run
```

Cấu hình kết nối MySQL trong `backend/src/main/resources/application.properties`.

## Android

Mở thư mục `android/` bằng Android Studio. Gradle wrapper sẽ được tự sinh khi sync lần đầu.
