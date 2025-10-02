# Embedded Linux Development Repository

## 개요 (Overview)
임베디드 리눅스 개발을 위한 학습 및 프로젝트 저장소입니다.

## 목적 (Purpose)
- 임베디드 리눅스 시스템 개발 학습
- 디바이스 드라이버 개발
- 커널 모듈 개발
- 크로스 컴파일링 환경 구축
- 실제 하드웨어 프로젝트 관리

## 구성 (Structure)
```
embedded_linux_wy/
├── kernel_modules/     # 커널 모듈 소스코드
├── device_drivers/     # 디바이스 드라이버
├── cross_compile/      # 크로스 컴파일링 설정
├── hardware_projects/  # 하드웨어 연동 프로젝트
├── docs/              # 학습 문서 및 가이드
└── tools/             # 개발 도구 및 스크립트
```

## 개발 환경 (Development Environment)
- **Target**: ARM/x86 임베디드 시스템
- **Host OS**: Linux (Ubuntu/Debian 권장)
- **Cross Compiler**: GCC ARM Toolchain
- **Build System**: Make, CMake
- **Version Control**: Git

## 주요 학습 영역 (Learning Areas)
1. **Linux Kernel**: 커널 구조 이해 및 모듈 개발
2. **Device Drivers**: 문자/블록/네트워크 드라이버
3. **System Programming**: 시스템 콜, IPC, 메모리 관리
4. **Hardware Interface**: GPIO, I2C, SPI, UART 제어
5. **Real-time Systems**: RT 패치, 스케줄링 최적화

## 설치 및 사용법 (Installation & Usage)
```bash
# 저장소 클론
git clone https://github.com/dev365code/embedded_linux_wy.git

# 개발 환경 설정
cd embedded_linux_wy
./setup.sh

# 프로젝트 빌드
make all
```

## 기여 (Contributing)
이 저장소는 개인 학습용이지만, 개선사항이나 제안사항은 언제든 환영합니다.

## 라이선스 (License)
MIT License - 자세한 내용은 LICENSE 파일을 참조하세요.