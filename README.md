# Embedded Linux Development Repository

## 개요 (Overview)
임베디드 리눅스 개발을 위한 단계별 학습 및 프로젝트 저장소입니다.
취미로 진행하는 장기 학습 계획으로, 체계적이고 지속가능한 성장을 목표로 합니다.

## 학습 목표 (Learning Goals)
- 임베디드 리눅스 시스템 개발 마스터
- 디바이스 드라이버 개발 역량 구축
- 커널 모듈 개발 및 시스템 프로그래밍
- 실제 프로젝트를 통한 실무 경험 축적

## 장기 학습 로드맵 (Long-term Learning Roadmap)

### Stage 1: 기초 탄탄히 (3-4개월)
**목표**: 하드웨어 제어와 통신 프로토콜 이해

#### Phase 1-1: 환경 구축 & GPIO 제어 (4-6주)
```
Week 1-2: 개발 환경 세팅
├── Raspberry Pi 4 설치 및 설정
├── SSH, VNC 원격 개발 환경 구축
├── Linux 기본 명령어 및 시스템 이해
└── GPIO 핀맵 및 전기적 특성 학습

Week 3-4: Python으로 기초 하드웨어 제어
├── LED, 버튼, PWM 제어
├── 센서 기초 (DHT11, 초음파, PIR)
├── 릴레이, 부저 제어
└── 실습 프로젝트: 스마트 홈 제어 시스템
```

#### Phase 1-2: I2C 통신 마스터 (3-4주)
```
Week 5-6: I2C 프로토콜 심화
├── I2C 이론 및 타이밍 분석
├── OLED 디스플레이 제어
├── RTC (DS3231) 시간 관리
├── ADC/DAC (PCF8591) 아날로그 처리
└── 다중 I2C 장치 관리

Week 7-8: C언어 전환 시작
├── Python → C언어 변환 실습
├── smbus → ioctl 시스템콜 이해
├── 메모리 매핑 기초 (/dev/mem)
└── 실습 프로젝트: 실시간 환경 모니터링
```

#### Phase 1-3: SPI & UART 통신 (3-4주)
```
Week 9-10: SPI 통신
├── SPI 프로토콜 및 timing 이해
├── RFID (RC522) 카드 리더
├── 74HC595 시프트 레지스터
├── MicroSD 카드 제어
└── /dev/spidev 활용법

Week 11-12: UART & 무선 통신
├── UART/RS232 프로토콜
├── 블루투스 (HC-06) 통신
├── LoRa/Wi-Fi 모듈 제어
├── termios 시리얼 프로그래밍
└── 실습 프로젝트: IoT 센서 네트워크
```

### Stage 2: 시스템 프로그래밍 (4-5개월)
**목표**: C언어 시스템 프로그래밍 및 커널 이해

#### Phase 2-1: 고급 C 시스템 프로그래밍 (6-8주)
```
Week 13-16: 메모리 관리 & 파일 시스템
├── 포인터, 동적 메모리 할당 심화
├── mmap()을 통한 레지스터 직접 제어
├── 파일 I/O 최적화 (read, write, select, poll)
├── 프로세스 간 통신 (pipe, fifo, shm)
├── 멀티쓰레딩 (pthread) 및 동기화
└── Signal 처리 및 비동기 프로그래밍

Week 17-20: 실시간 시스템 기초
├── 인터럽트 처리 및 우선순위
├── RT 패치 적용 및 스케줄링
├── 타이머 및 정밀한 시간 제어
├── DMA 개념 및 활용
└── 실습 프로젝트: 실시간 데이터 수집 시스템
```

#### Phase 2-2: 리눅스 커널 기초 (4-6주)
```
Week 21-24: 커널 컴파일 & 모듈 개발
├── 커널 소스 분석 및 컴파일
├── Device Tree 이해 및 수정
├── 첫 번째 커널 모듈 (Hello World)
├── 모듈 파라미터 및 sysfs 인터페이스
└── proc 파일시스템 활용

Week 25-26: 디버깅 & 분석 도구
├── printk, dmesg를 통한 커널 디버깅
├── ftrace, perf 성능 분석
├── GDB 커널 디버깅
└── 메모리 분석 (valgrind, kmemleak)
```

### Stage 3: 디바이스 드라이버 개발 (5-6개월)
**목표**: 실제 하드웨어 디바이스 드라이버 작성

#### Phase 3-1: Character Device Driver (8-10주)
```
Week 27-30: 기본 캐릭터 드라이버
├── file_operations 구조체 완전 이해
├── register_chrdev vs cdev 방식
├── ioctl 명령 설계 및 구현
├── 사용자-커널 간 데이터 전송
└── 실습: /dev/mysensor 드라이버

Week 31-34: 고급 드라이버 기능
├── GPIO 서브시스템 활용
├── 인터럽트 핸들러 구현
├── tasklet, workqueue 비교 활용
├── 커널 타이머 및 지연 처리
├── 동기화 (mutex, spinlock, semaphore)
└── 실습: 인터럽트 기반 입력 드라이버

Week 35-36: 플랫폼 드라이버
├── Platform device/driver 모델
├── Device Tree 바인딩
├── 리소스 관리 (ioremap, request_irq)
└── 실습: I2C 센서 플랫폼 드라이버
```

#### Phase 3-2: 고급 서브시스템 (6-8주)
```
Week 37-40: V4L2 카메라 드라이버
├── V4L2 프레임워크 이해
├── 비디오 캡처 드라이버 구조
├── 버퍼 관리 (MMAP, USERPTR)
├── DMA 버퍼 최적화
└── 실습: USB 카메라 커스텀 드라이버

Week 41-44: 네트워크 드라이버
├── CAN 버스 드라이버 개발
├── SocketCAN 프레임워크
├── 네트워크 디바이스 구조
├── SKB (Socket Buffer) 관리
└── 실습: CAN 통신 드라이버
```

### Stage 4: 통합 프로젝트 & 최적화 (3-4개월)
**목표**: 실무 수준의 완성된 시스템 구현

#### Phase 4-1: 아키텍처 설계 (4-6주)
```
Week 45-48: 시스템 아키텍처
├── 요구사항 분석 및 설계
├── 하드웨어-소프트웨어 인터페이스 정의
├── 모듈화 및 계층 구조 설계
├── 전력 관리 전략
└── 안전성 및 신뢰성 고려사항

Week 49-50: 개발 환경 고도화
├── 크로스 컴파일 환경 구축
├── 자동화된 빌드 시스템 (Yocto/Buildroot)
├── 버전 관리 및 배포 전략
└── 테스트 자동화 프레임워크
```

#### Phase 4-2: 최종 프로젝트 구현 (6-8주)
```
Week 51-54: 핵심 시스템 구현
├── 다중 센서 통합 시스템
├── 실시간 영상 처리 및 저장
├── 무선 통신 및 원격 제어
├── 데이터 로깅 및 분석
└── 사용자 인터페이스 (웹/모바일)

Week 55-58: 최적화 및 완성
├── 성능 최적화 (메모리, CPU, 전력)
├── 예외 상황 처리 및 복구
├── 보안 강화 (암호화, 인증)
├── 문서화 및 포트폴리오 정리
└── 배포 및 유지보수 가이드
```

## 구성 (Directory Structure)
```
embedded_linux_wy/
├── phase1_basics/          # Stage 1 기초 학습
│   ├── gpio_control/       # GPIO 제어 예제
│   ├── i2c_projects/       # I2C 통신 프로젝트
│   └── spi_uart/           # SPI, UART 통신
├── phase2_system/          # Stage 2 시스템 프로그래밍
│   ├── c_programming/      # 고급 C 프로그래밍
│   ├── kernel_basics/      # 커널 기초
│   └── debugging/          # 디버깅 도구
├── phase3_drivers/         # Stage 3 드라이버 개발
│   ├── char_drivers/       # 캐릭터 드라이버
│   ├── platform_drivers/   # 플랫폼 드라이버
│   └── subsystems/         # V4L2, 네트워크 등
├── phase4_integration/     # Stage 4 통합 프로젝트
│   ├── architecture/       # 시스템 설계
│   ├── final_project/      # 최종 프로젝트
│   └── optimization/       # 최적화 기법
├── docs/                   # 학습 노트 및 문서
│   ├── learning_notes/     # 단계별 학습 기록
│   ├── troubleshooting/    # 문제 해결 사례
│   └── references/         # 참고 자료
└── tools/                  # 개발 도구 및 스크립트
    ├── build_scripts/      # 빌드 자동화
    ├── test_tools/         # 테스트 도구
    └── utilities/          # 유틸리티 스크립트
```

## 학습 방법론 (Learning Methodology)

### 일일 학습 패턴
```
평일 (1-1.5시간):
├── 30분: 이론 학습 (문서, 책)
├── 45분: 실습 및 코딩
└── 15분: 학습 기록 정리

주말 (2-3시간):
├── 1시간: 심화 학습 및 복습
├── 1-2시간: 프로젝트 진행
└── 30분: 다음 주 계획 수립
```

### 마일스톤 체크포인트
- **3개월**: 모든 통신 프로토콜 활용 가능
- **6개월**: 기본적인 커널 모듈 작성 능력
- **12개월**: Character Device Driver 구현 완료
- **18개월**: 고급 서브시스템 드라이버 개발
- **24개월**: 완성된 임베디드 시스템 포트폴리오

### 평가 기준
각 Phase 완료 시 다음 기준으로 자가 평가:
1. **이론 이해도**: 핵심 개념 설명 가능
2. **실습 완료도**: 모든 예제 코드 동작 확인
3. **응용 능력**: 유사한 문제 독립적 해결
4. **문제 해결**: 에러 상황 분석 및 해결

## 개발 환경 (Development Environment)
- **Target Hardware**: Raspberry Pi 4B (4GB RAM)
- **Host OS**: Ubuntu 22.04 LTS
- **Cross Compiler**: GCC ARM Toolchain
- **Build System**: Make, CMake, Yocto Project
- **Debug Tools**: GDB, Valgrind, Ftrace
- **Version Control**: Git (GitHub)

## 주요 참고 자료 (References)
1. **서적**
   - Linux Device Drivers (3rd Edition)
   - Linux Kernel Development (Robert Love)
   - Embedded Linux Primer (Christopher Hallinan)

2. **온라인 자료**
   - Linux Kernel 공식 문서
   - Raspberry Pi Foundation 가이드
   - Embedded Linux Wiki

3. **커뮤니티**
   - Stack Overflow (embedded-linux 태그)
   - Raspberry Pi Forums
   - Linux Kernel Mailing List

## 성공 지표 (Success Metrics)
최종 목표 달성 시 보유하게 될 역량:

### 기술적 역량
- 임베디드 리눅스 커널 수정 및 컴파일
- Character/Block/Network Device Driver 개발
- I2C, SPI, UART, CAN 통신 프로토콜 활용
- V4L2 카메라 제어 및 영상 처리
- 실시간 시스템 설계 및 최적화
- DMA, 인터럽트 처리, 메모리 관리
- 크로스 컴파일 및 배포 자동화

### 프로젝트 포트폴리오
- **기초 프로젝트**: IoT 센서 네트워크 (5개 이상)
- **중급 프로젝트**: 커스텀 디바이스 드라이버 (3개 이상)
- **고급 프로젝트**: 통합 임베디드 시스템 (1개)
- **GitHub**: 체계적으로 정리된 학습 기록

이 로드맵은 무리하지 않고 꾸준히 진행할 수 있도록 설계되었으며,
각자의 속도에 맞춰 조정 가능합니다.

## 라이선스 (License)
MIT License - 자세한 내용은 LICENSE 파일을 참조하세요.