---
title: Xamarin.iOS errors
ms.topic: article
ms.prod: xamarin
ms.assetid: 9F76162B-D622-45DA-996B-2FBF8017E208
ms.technology: xamarin-ios
author: bradumbaugh
ms.author: brumbaug
ms.date: 06/26/2017
ms.openlocfilehash: 5a11ca19de7ce06088478f1a39dae5a246d701a8
ms.sourcegitcommit: 6cd40d190abe38edd50fc74331be15324a845a28
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/27/2018
---
# <a name="xamarinios-errors"></a>Xamarin.iOS errors


## <a name="mt0xxx-mtouch-error-messages"></a>MT0xxx: mtouch 오류 메시지

예: 매개 변수, 환경, 도구 누락입니다.

<!--
 MT0xxx mtouch itself, e.g. parameters, environment (e.g. missing tools)
 https://github.com/xamarin/xamarin-macios/blob/master/tools/mtouch/error.cs
    -->

### <a name="a-namemt0000mt0000-unexpected-error---please-fill-a-bug-report-at-httpbugzillaxamarincom"></a><a name="MT0000"/>MT0000: 예기치 않은 오류-http://bugzilla.xamarin.com에 버그 보고서를 채우십시오.

예기치 않은 오류가 발생 했습니다. 하십시오 [버그 보고](https://bugzilla.xamarin.com/enter_bug.cgi?product=iOS) 최대한 많은 정보를 포함 합니다.

* 최대 세부 정보 표시와 전체 빌드 로그, (예: `-v -v -v -v` 에 **추가 mtouch 인수**);
* 오류를 재현 하는 최소한의 테스트 사례 및
* 모든 버전 정보

사용 하는 정확한 버전 정보를 가져올 수는 가장 쉬운 방법은 **Mac 용 Visual Studio** 메뉴 **Mac 용 Visual Studio에 대 한** 항목 **자세한 정보 표시** 단추와 복사/붙여넣기는 버전 정보 (사용할 수 있습니다는 **복사본 정보** 단추).

### <a name="a-namemt0001mt0001--devname-was-provided-without-any-device-specific-action"></a><a name="MT0001"/>MT0001: '-devname' 장치별 개입 없이 제공 된

이것은 경고를 실행-devname mtouch 때 아무 장치 관련 작업에 전달 되 면 내보내집니다 (-logdev/installdev/killdev/launchdev /-listapps) 요청 되었습니다.

### <a name="a-namemt0002mt0002-could-not-parse-the-environment-variable-"></a><a name="MT0002"/>MT0002: 환경 변수를 분석할 수 없습니다 * 합니다.

잘못 된 환경 키를 설정 하려고 하면이 오류가 발생 하면 = 변수 값 쌍입니다. 올바른 형식은 다음과 같습니다. `mtouch --setenv=VARIABLE=VALUE`

### <a name="a-namemt0003mt0003-application-name-exe-conflicts-with-an-sdk-or-product-assembly-dll-name"></a><a name="MT0003"/>MT0003: 응용 프로그램 이름 ' *.exe ' SDK 또는 제품 어셈블리 (.dll) 이름과 충돌 합니다.

실행 가능한 어셈블리의 이름 및 응용 프로그램의 이름을 응용 프로그램에서 dll의 이름을 일치할 수 없습니다. 실행 파일의 이름을 수정 하십시오.

### <a name="a-namemt0004mt0004-new-refcounting-logic-requires-sgen-to-be-enabled-too"></a><a name="MT0004"/>MT0004: 새로운 refcounting 논리 SGen도 사용으로 설정 하려면 필요 합니다.

Refcounting 확장을 사용 하도록 설정 하면 iOS 프로젝트의 빌드 옵션 (고급 탭) SGen 가비지 수집기에도 설정 해야 합니다.

이 요구 사항을 Xamarin.iOS 7.2.1 부터는 없어졌으며, Boehm와 SGen 가비지 수집기가 새 refcounting 논리를 사용할 수 있습니다.

### <a name="a-namemt0005mt0005-the-output-directory--does-not-exist"></a><a name="MT0005"/>MT0005: 출력 디렉터리 * 존재 하지 않습니다.

디렉터리를 만드십시오.

이 오류는 더 이상 발생 하지 않습니다, 존재 하지 않는 경우 mtouch에서 디렉터리를 자동으로 만듭니다.

### <a name="a-namemt0006mt0006-there-is-no-devel-platform-at--use---platformplat-to-specify-the-sdk"></a><a name="MT0006"/>MT0006: 없는 개발자 플랫폼에는 *를 사용-플랫폼 SDK를 지정 하는 구획 = 합니다.

Xamarin.iOS 오류 메시지에 언급 된 위치에서 SDK 디렉터리를 찾을 수 없습니다. 경로가 정확한 지 확인 하십시오.

### <a name="a-namemt0007mt0007-the-root-assembly--does-not-exist"></a><a name="MT0007"/>MT0007: 루트 어셈블리 * 존재 하지 않습니다.

Xamarin.iOS 오류 메시지에 언급 된 위치에서 어셈블리를 찾을 수 없습니다. 경로가 정확한 지 확인 하십시오.

### <a name="a-namemt0008mt0008-you-should-provide-one-root-assembly-only-found--assemblies-"></a><a name="MT0008"/>MT0008: 제공 해야 하나 루트 어셈블리, 찾은 # 어셈블리: * 합니다.

하나의 루트 어셈블리 있을 수 있지만 둘 이상의 루트 어셈블리 mtouch에 전달 되었습니다.

### <a name="a-namemt0009mt0009-error-while-loading-assemblies-"></a><a name="MT0009"/>MT0009: 어셈블리를 로드 하는 동안 오류: * 합니다.

루트 어셈블리 참조 어셈블리를 로드 하는 동안 오류가 발생 했습니다. 자세한 내용은 빌드 출력에 제공 될 수 있습니다.

### <a name="a-namemt0010mt0010-could-not-parse-the-command-line-arguments-"></a><a name="MT0010"/>MT0010: 명령줄 인수 구문 분석할 수 없습니다: * 합니다.

명령줄 인수 구문 분석 하는 동안 오류가 발생 했습니다. 모두 정확한 지 확인 하십시오.

### <a name="a-namemt0011mt0011--was-built-against-a-more-recent-runtime--than-monotouch-supports"></a><a name="MT0011"/>MT0011: * MonoTouch 지 원하는 것 보다 더 최신 런타임 (*)에 대해 작성 합니다.

프로젝트에 Xamarin.iOS BCL을 사용 하 여 만들어지지 않은 하는 클래스 라이브러리에 대 한 참조 하기 때문에이 경고는 일반적으로 보고 됩니다.

.NET 2.0 지원 시스템에.NET 4.0 SDK를 사용 하 여 앱이 작동 하지 않을 수에 관계 없이 동일한 방식으로.NET 4.0을 사용 하 여 빌드된 라이브러리 Xamarin.iOS에서 작동 하지 않을, Xamarin.iOS에 없는 API를 사용할 수 있습니다.

일반적인 해결 Xamarin.iOS 클래스 라이브러리와 라이브러리를 작성 하는 것입니다. 이 새 Xamarin.iOS 클래스 라이브러리 프로젝트를 만들어 수행할 수 있으며 모든 소스 파일을 추가 합니다. 라이브러리의 소스 코드가 없는 경우에 공급 업체에 문의 하 고 이러한가 라이브러리의 Xamarin.iOS 호환 버전을 제공 하도록 요청 해야 합니다.

### <a name="a-namemt0012mt0012-incomplete-data-is-provided-to-complete-"></a><a name="MT0012"/>MT0012: 불완전 한 데이터가을 완료할 제공 * 합니다.

이 오류 Xamarin.iOS의 현재 버전에서 더 이상 보고 되지 않습니다.

### <a name="a-namemt0013mt0013-profiling-support-requires-sgen-to-be-enabled-too"></a><a name="MT0013"/>MT0013: sgen 너무 사용 하도록 설정할 필요 프로 파일링 지원 합니다.

SGen (-sgen) 프로 파일링 하는 경우에 사용할 수 있어야 합니다 (-프로 파일링)를 사용할 수 있습니다.

### <a name="a-namemt0014mt0014-the-ios--sdk-does-not-support-building-applications-targeting-"></a><a name="MT0014"/>MT0014: iOS * SDK 대상으로 하는 응용 프로그램 빌드를 지원 하지 않습니다 *.

이 작업은 다음과 같은 경우에 발생할 수 있습니다.

*  ARMv6 사용 하도록 설정 하 고 Xcode 4.5 이상을 설치 됩니다.
*  ARMv7s 사용 하도록 설정 하 고 Xcode 4.4 또는 이전 버전을 설치 됩니다.


설치 된 버전의 Xcode에 선택한 아키텍처를 지원 하는지 확인 하십시오.

### <a name="a-namemt0015mt0015-invalid-abi--supported-abis-are-i386-x8664--armv7-armv7llvm-armv7llvmthumb2-armv7s-armv7sllvm-armv7sllvmthumb2-arm64-and-arm64llvm"></a><a name="MT0015"/>MT0015: Invalid ABI: *. 지원 되는 ABIs 됩니다: i386, x86_64, armv7, armv7 + 원하는 llvm, armv7 + 원하는 llvm + thumb2, armv7s, armv7s + 원하는 llvm, armv7s + 원하는 llvm + thumb2, arm64 및 arm64 + 원하는 llvm 합니다.

잘못 된 ABI mtouch에 전달 되었습니다. 유효한 ABI를 지정 하십시오.

### <a name="a-namemt0016mt0016-the-option--has-been-deprecated"></a><a name="MT0016"/>MT0016: 옵션 * 사용 되지 않습니다.

언급 한 mtouch 옵션이 사용 되지 않으며 무시 됩니다.

### <a name="a-namemt0017mt0017-you-should-provide-a-root-assembly"></a><a name="MT0017"/>MT0017: 루트 어셈블리를 제공 해야 합니다.

루트 어셈블리 (일반적으로 주 실행 파일)를 지정 하는 응용 프로그램을 빌드하는 경우.

### <a name="a-namemt0018mt0018-unknown-command-line-argument-"></a><a name="MT0018"/>MT0018: 알 수 없는 명령줄 인수: * 합니다.

Mtouch 오류 메시지에 명령줄 인수를 인식 하지 못합니다.

### <a name="a-namemt0019mt0019-only-one---loginstallkilllaunchdev-or---launchdebugsim-option-can-be-used"></a><a name="MT0019"/>MT0019: 하나만-[로그 | 설치 | kill | 시작] 개발자 또는--[시작 | 디버그] sim 옵션을 사용할 수 있습니다.

동시에 사용할 수 없는 mtouch에 대 한 여러 가지가 있습니다.

-  --logdev
-  --installdev
-  -killdev
-  -launchdev
-  --launchdebug
-  --launchsim




### <a name="a-namemt0020mt0020-the-valid-options-for--are-"></a><a name="MT0020"/>MT0020에 대해 유효한 옵션이 '\*'는'\*'.



### <a name="a-namemt0021mt0021-cannot-compile-using-gccg---use-gcc-when-using-the-static-registrar-this-is-the-default-when-compiling-for-device-either-remove-the---use-gcc-flag-or-use-the-dynamic-registrar---registrardynamic"></a><a name="MT0021"/>Gcc를 사용 하 여 MT0021 없습니다 컴파일 / g + + (-gcc 사용) (이 기본 장치에 대해 컴파일할 때) 정적 등록자를 사용 하는 경우. 제거 하거나--사용 gcc 플래그를 지정 하거나 동적 등록을 사용 하 여 (-등록자: 동적).



### <a name="a-namemt0022mt0022-the-options---unsupported--enable-generics-in-registrar-and---registrar-are-not-compatible"></a><a name="MT0022"/>MT0022 옵션 '-지원 되지 않는-enable-제네릭-에-등록자 ' 및 '-등록자 ' 호환 되지 않습니다.

제거 옵션 모두 `--unsupported--enable-generics-in-registrar` 및 `--registrar`합니다. 부터는 Xamarin.iOS 7.2.1 기본 등록 기관에서 제네릭을 지원 합니다.

이 오류가 더 이상 표시 됩니다 (명령줄 인수 `--unsupported--enable-generics-in-registrar` mtouch에서 제거 되었습니다).

### <a name="a-namemt0023mt0023-application-name-exe-conflicts-with-another-user-assembly"></a><a name="MT0023"/>MT0023 응용 프로그램 이름 ' *.exe ' 다른 사용자 어셈블리와 충돌 합니다.

실행 가능한 어셈블리의 이름 및 응용 프로그램의 이름을 응용 프로그램에서 dll의 이름을 일치할 수 없습니다. 실행 파일의 이름을 수정 하십시오.

### <a name="a-namemt0024mt0024-could-not-find-required-file-"></a><a name="MT0024"/>필요한 파일을 찾을 MT0024 수 없습니다. ' *'입니다.



### <a name="a-namemt0025mt0025-no-sdk-version-was-provided-please-add---sdkxy-to-specify-which-ios-sdk-should-be-used-to-build-your-application"></a><a name="MT0025"/>MT0025 아니요 SDK 버전이 제공 되었습니다. 추가 하십시오 `--sdk=X.Y` 어떤 iOS를 지정 하려면 응용 프로그램을 빌드하려면 SDK를 사용 합니다.



### <a name="a-namemt0026mt0026-could-not-parse-the-command-line-argument--"></a><a name="MT0026"/>명령줄 인수 구문 분석할 MT0026 수 없습니다 ' *': *



### <a name="a-namemt0027mt0027-the-options--and--are-not-compatible"></a><a name="MT0027"/>MT0027 옵션\*'및'\*' 호환 되지 않습니다.



### <a name="a-namemt0028mt0028-cannot-enable-pie--pie-when-targeting-ios-41-or-earlier-please-disable-pie--piefalse-or-set-the-deployment-target-to-at-least-ios-42"></a><a name="MT0028"/>원형 사용 MT0028 수 없습니다 (-원형) iOS 4.1 또는 그 이전 버전을 대상으로 지정 합니다. 원형을 중지 하십시오 (-원형: false) 이상으로 배포 대상을 설정 하거나 iOS 4.2



### <a name="a-namemt0029mt0029-repl---enable-repl-is-only-supported-in-the-simulator---sim"></a><a name="MT0029"/>MT0029: REPL (-enable repl)만 시뮬레이터에서 지원 됩니다 (-sim).

REPL은 시뮬레이터에 대 한 작성 하는 경우에 지원 됩니다. 즉, 전달 하는 경우 `--enable-repl` mtouch에 전달 해야 `--sim`합니다.

### <a name="a-namemt0030mt0030-the-executable-name--and-the-app-name--are-different-this-may-prevent-crash-logs-from-getting-symbolicated-properly"></a><a name="MT0030"/>MT0030: 실행 파일 이름 (\*) 및 응용 프로그램 이름 (\*) 다른이 제대로 symbolicated 가져오기에서 크래시 로그를 하지 않을 수 있습니다.

Xcode symbolicates 때 (함수 이름 및 파일/줄 번호를 메모리 주소 변환) 하는 프로세스는 실행 파일 및 응용 프로그램 (확장명 없음) 다른 이름이 있는 경우에 실패할 수 있습니다.

문제를 해결 하려면 프로젝트의 빌드/iOS 응용 프로그램 옵션 또는 프로젝트의 빌드/출력 옵션에서 ' 어셈블리 이름 ' 변경 ' 응용 프로그램 이름 ' 변경이 중 하나입니다.

### <a name="a-namemt0031mt0031-the-command-line-arguments---enable-background-fetch-and---launch-for-background-fetch-require---launchsim-too"></a><a name="MT0031"/>MT0031: 명령줄 인수 '-enable 배경 페치 ' 및 '-시작에 대 한 백그라운드 가져오기를 ' 필요 '-launchsim' 너무 합니다.

### <a name="a-namemt0032mt0032-the-option---debugtrack-is-ignored-unless---debug-is-also-specified"></a><a name="MT0032"/>MT0032: 옵션 '-debugtrack'은 무시 됩니다 '-디버그 '도 지정 합니다.

### <a name="a-namemt0033mt0033--a-xamarinios-project-must-reference-either-monotouchdll-or-xamariniosdll"></a><a name="MT0033"/>Monotouch.dll 또는 Xamarin.iOS.dll MT0033 A Xamarin.iOS 프로젝트 참조 해야 합니다.

### <a name="a-namemt0034mt0034--cannot-include-both-monotouchdll-and-xamariniosdll-in-the-same-xamarinios-project----is-referenced-explicitly-while--is-referenced-by-"></a><a name="MT0034"/>동일한 Xamarin.iOS 프로젝트-에 'monotouch.dll' 및 'Xamarin.iOS.dll' 포함 MT0034 수 없습니다. '\*'은 명시적으로 참조 하는 동안 '\*'에서 참조 ' *'입니다.

<!-- MT0035 unused -->

### <a name="a-namemt0036mt0036--cannot-launch-a--simulator-for-a--app-please-enable-the-correct-architectures-in-your-projects-ios-build-options-advanced-page"></a><a name="MT0036"/>시작 MT0036 없습니다는 *에 대 한 시뮬레이터는 * 응용 프로그램입니다. 프로젝트의 iOS 빌드 옵션 (고급 페이지)에서 올바른 architecture(s) 사용 하도록 설정 하십시오.

### <a name="a-namemt0037mt0037--monotouchdll-is-not-64-bit-compatible-either-reference-xamariniosdll-or-do-not-build-for-a-64-bit-architecture-arm64-andor-x8664"></a><a name="MT0037"/>MT0037 monotouch.dll 하지 64 비트와 호환 됩니다. Xamarin.iOS.dll, 참조 또는 (ARM64 및/또는 x86_64) 64 비트 아키텍처에 대 한 작성 하지 마십시오.

### <a name="a-namemt0038mt0038--the-old-registrars---registraroldstaticolddynamic-are-not-supported-when-referencing-xamariniosdll"></a><a name="MT0038"/>MT0038 이전 기관 (-등록자: oldstatic | olddynamic) Xamarin.iOS.dll 참조 하는 경우 지원 되지 않습니다.

### <a name="a-namemt0039mt0039--applications-targeting-armv6-cannot-reference-xamariniosdll"></a><a name="MT0039"/>ARMv6를 대상으로 하는 MT0039 응용 프로그램 Xamarin.iOS.dll 참조할 수 없습니다.

### <a name="a-namemt0040mt0040--could-not-find-the-assembly--referenced-by-"></a><a name="MT0040"/>어셈블리를 찾지 MT0040 못했습니다 '\*', 참조'\*'.

### <a name="a-namemt0041mt0041--cannot-reference-both-monotouchdll-and-xamariniosdll"></a><a name="MT0041"/>'Monotouch.dll'와 'Xamarin.iOS.dll' MT0041 참조할 수 없습니다.

### <a name="a-namemt0042mt0042--no-reference-to-either-monotouchdll-or-xamariniosdll-was-found-a-reference-to-monotouchdll-will-be-added"></a><a name="MT0042"/>Monotouch.dll 또는 Xamarin.iOS.dll MT0042 아니요 참조가 발견 되었습니다. Monotouch.dll에 대 한 참조가 추가 됩니다.

### <a name="a-namemt0043mt0043-the-boehm-garbage-collector-is-currently-not-supported-when-referencing-xamariniosdll-the-sgen-garbage-collector-has-been-selected-instead"></a><a name="MT0043"/>MT0043: Boehm 가비지 수집기는 현재 지원 되지 않습니다 'Xamarin.iOS.dll'를 참조 하는 경우. SGen 가비지 수집기를 대신 선택 했습니다.

통합 프로젝트와 함께 SGen 가비지 수집기에만 사용할 수 있습니다. 확인 Boehm 가비지 수집기로 지정 하는 추가 mtouch 플래그가 없습니다.

### <a name="a-namemt0044mt0044---listsim-is-only-supported-with-xcode-60-or-later"></a><a name="MT0044"/>MT0044: Xcode 6.0 이상-listsim 지원만 됩니다.

새 Xcode 버전을 설치 합니다.

### <a name="a-namemt0045mt0045---extension-is-only-supported-when-using-the-ios-80-or-later-sdk"></a><a name="MT0045"/>MT0045:-확장은 iOS를 사용 하는 경우에 지원 SDK 8.0 (또는 이후 버전).

<!-- MT0046 is not reported anymore -->

### <a name="a-namemt0047mt0047-the-minimum-deployment-target-for-unified-applications-is-511-the-current-deployment-target-is--please-select-a-newer-deployment-target-in-your-projects-ios-application-options"></a><a name="MT0047"/>MT0047: 통합 응용 프로그램에 대 한 최소 배포 대상은 5.1.1, 현재 배포 목표는 ' *'입니다. 프로젝트의 iOS 응용 프로그램 옵션에서에서 새로운 배포 대상을 선택 하십시오.

<!-- MT0048 is not reported anymore -->

### <a name="a-namemt0049mt0049-framework-is-supported-only-if-deployment-target-is-80-or-later--features-might-not-work-correctly"></a><a name="MT0049"/>MT0049: *.framework 배포 대상이 8.0 이상 하는 경우에 지원 됩니다. * 기능이 올바르게 작동 하지 수도 있습니다.

지정 된 프레임 워크는 배포 대상에서 참조 하는 iOS 버전에서 지원 되지 않습니다. 배포 대상 새 iOS 버전으로 업데이트 하거나 응용 프로그램에서 지정 된 프레임 워크의 사용을 제거 합니다.

<!-- MT0050 is not reported anymore -->

### <a name="a-namemt0051mt0051-xamarinios--requires-xcode-50-or-later-the-current-xcode-version-found-in--is-"></a><a name="MT0051"/>MT0051: Xamarin.iOS * Xcode 5.0 이상이 필요 합니다. 현재는 Xcode 버전 (에 *)는 *입니다.

최신 Xcode를 설치 합니다.

### <a name="a-namemt0052mt0052-no-command-specified"></a><a name="MT0052"/>MT0052: 명령을 지정 합니다.

아무 작업도 mtouch에 지정 되었습니다.

<!-- 0053 is used by mmp -->

### <a name="a-namemt0054mt0054-unable-to-canonicalize-the-path--"></a><a name="MT0054"/>MT0054: 경로 정식화 수 없습니다. ' *': *

내부 오류입니다. 이 오류를 표시 하는 경우 버그를 제출 하세요 [http://bugzilla.xamarin.com](https://bugzilla.xamarin.com/enter_bug.cgi?product=iOS)합니다.

### <a name="a-namemt0055mt0055-the-xcode-path--does-not-exist"></a><a name="MT0055"/>MT0055: Xcode path ' *'가 없습니다.

Xcode 경로 사용 하 여 전달 `--sdkroot` 존재 하지 않습니다. 올바른 경로 지정 하십시오.

### <a name="a-namemt0056mt0056-cannot-find-xcode-in-the-default-location-applicationsxcodeapp-please-install-xcode-or-pass-a-custom-path-using---sdkroot-path"></a><a name="MT0056"/>MT0056: 기본 위치에서 Xcode를 찾을 수 없습니다 (/ Applications/Xcode.app). -Sdkroot를 사용 하 여 사용자 지정 경로 전달 하거나, Xcode를 설치 하십시오 <path>합니다.
### <a name="a-namemt0057mt0057-cannot-determine-the-path-to-xcodeapp-from-the-sdk-root--please-specify-the-full-path-to-the-xcodeapp-bundle"></a><a name="MT0057"/>MT0057: sdk 루트에서 Xcode.app에 경로 확인할 수 없습니다 ' *'입니다. Xcode.app 번들의 전체 경로 지정 하십시오.

전달 되는 경로 사용 하 여 `--sdkroot` 올바른 Xcode 앱을 지정 하지 않습니다. Xcode 응용 프로그램에 대 한 경로 지정 하십시오.

### <a name="a-namemt0058mt0058-the-xcodeapp--is-invalid-the-file--does-not-exist"></a><a name="MT0058"/>MT0058: Xcode.app '\*' 올바르지 않습니다 (파일 '\*' 존재 하지 않는).

전달 되는 경로 사용 하 여 `--sdkroot` 올바른 Xcode 앱을 지정 하지 않습니다. Xcode 응용 프로그램에 대 한 경로 지정 하십시오.

### <a name="a-namemt0059mt0059-could-not-find-the-currently-selected-xcode-on-the-system-"></a><a name="MT0059"/>MT0059: 시스템에서 현재 선택 된 Xcode를 찾을 수 없습니다: *

### <a name="a-namemt0060mt0060-could-not-find-the-currently-selected-xcode-on-the-system-xcode-select---print-path-returned--but-that-directory-does-not-exist"></a><a name="MT0060"/>MT0060: 시스템에서 현재 선택 된 Xcode를 찾을 수 없습니다. ' xcode 선택-인쇄 경로 ' 반환 ' *'는 없지만 디렉터리가 존재 하지 않습니다.

### <a name="a-namemt0061mt0061-no-xcodeapp-specified-using---sdkroot-using-the-system-xcode-as-reported-by-xcode-select---print-path-"></a><a name="MT0061"/>MT0061: Xcode.app (-sdkroot 사용), 지정 된 ' xcode 선택-인쇄 경로 '가 보고 시스템 Xcode를 사용 하 여: *

이 Xcode 될를 설명 하는 정보 제공 경고를 사용할 지정 되지 않았습니다.

### <a name="a-namemt0062mt0062-no-xcodeapp-specified-using---sdkroot-or-xcode-select---print-path-using-the-default-xcode-instead-"></a><a name="MT0062"/>MT0062: Xcode.app 대신 기본 Xcode를 사용 하 여 (-sdkroot 또는 ' xcode 선택-인쇄 경로 ' 사용), 지정 된: *

이 Xcode 될를 설명 하는 정보 제공 경고를 사용할 지정 되지 않았습니다.

### <a name="a-namemt0063mt0063-cannot-find-the-executable-in-the-extension--no-cfbundleexecutable-entry-in-its-infoplist"></a><a name="MT0063"/>MT0063: 확장에서 실행 파일을 찾을 수 없으면 * (해당 Info.plist에서 CFBundleExecutable 항목 없음)

하지만 빌드하는 동안 항목이 자동으로 생성 해야 모든 Info.plist는 실행 파일 (CFBundleExecutable 항목 사용)이 있어야 합니다.

이것은 보통 Xamarin.iOS;의 버그를 나타냅니다. 에 버그 보고서를 제출 하세요 [http://bugzilla.xamarin.com](https://bugzilla.xamarin.com/enter_bug.cgi?product=iOS) 테스트 사례와 합니다.

### <a name="a-namemt0064mt0064-xamarinios-only-supports-embedded-frameworks-with-unified-projects"></a><a name="MT0064"/>MT0064: Xamarin.iOS 통합 프로젝트와 함께 포함 된 프레임 워크만 지원합니다.

통합 된 API를 사용 하는 경우만 Xamarin.iOS 포함 된 프레임 워크 지원 통합 API를 사용 하도록 프로젝트를 업데이트 하십시오.

### <a name="a-namemt0065mt0065-xamarinios-only-supports-embedded-frameworks-when-deployment-target-is-at-least-80-current-deployment-target--embedded-frameworks-"></a><a name="MT0065"/>MT0065: Xamarin.iOS만 포함 된 프레임 워크 때 지원 배포 대상이 8.0 이상 (현재 배포 대상: * 프레임 워크를 포함: *)

Xamarin.iOS 경우 배포 대상 8.0 이상 (이전 버전 iOS 포함 된 프레임 워크를 지원 하지 않음)만 포함 된 프레임 워크를 지원 합니다.

프로젝트의 Info.plist에서 배포 대상을 8.0 이상으로 업데이트 하십시오.

### <a name="a-namemt0066mt0066-invalid-build-registrar-assembly-"></a><a name="MT0066"/>MT0066: 잘못 등록 기관 어셈블리 빌드: *

이것은 보통 Xamarin.iOS;의 버그를 나타냅니다. 에 버그 보고서를 제출 하세요 [http://bugzilla.xamarin.com](https://bugzilla.xamarin.com/enter_bug.cgi?product=iOS) 테스트 사례와 합니다.

### <a name="a-namemt0067mt0067-invalid-registrar-"></a><a name="MT0067"/>MT0067: Invalid registrar: *

이것은 보통 Xamarin.iOS;의 버그를 나타냅니다. 에 버그 보고서를 제출 하세요 [http://bugzilla.xamarin.com](https://bugzilla.xamarin.com/enter_bug.cgi?product=iOS) 테스트 사례와 합니다.

### <a name="a-namemt0068mt0068-invalid-value-for-target-framework-"></a><a name="MT0068"/>MT0068: 대상 프레임 워크에 대 한 값이 잘못 되었습니다: * 합니다.

잘못 된 대상 프레임 워크를 사용 하 여 전달 된의--대상 프레임 워크 인수입니다. 올바른 대상 프레임 워크를 지정 하십시오.

<!--### <a name="MT0069"/>MT0069: currently unused -->

### <a name="a-namemt0070mt0070-invalid-target-framework--valid-target-frameworks-are-"></a><a name="MT0070"/>MT0070: 잘못 된 대상 프레임 워크: * 합니다. 올바른 대상 프레임 워크는: * 합니다.

잘못 된 대상 프레임 워크를 사용 하 여 전달 된의--대상 프레임 워크 인수입니다. 올바른 대상 프레임 워크를 지정 하십시오.

### <a name="a-namemt0071mt0071-unknown-platform--this-usually-indicates-a-bug-in-xamarinios-please-file-a-bug-report-at-httpbugzillaxamarincom-with-a-test-case"></a><a name="MT0071"/>MT0071: 알 수 없는 플랫폼: * 합니다. 이것은 보통 Xamarin.iOS;의 버그를 나타냅니다. 테스트 사례와 http://bugzilla.xamarin.com에 버그 보고서를 제출 하세요.

이것은 보통 Xamarin.iOS;의 버그를 나타냅니다. 에 버그 보고서를 제출 하세요 [http://bugzilla.xamarin.com](https://bugzilla.xamarin.com/enter_bug.cgi?product=iOS) 테스트 사례와 합니다.

### <a name="a-namemt0072mt0072-extensions-are-not-supported-for-the-platform-"></a><a name="MT0072"/>MT0072: 플랫폼에 대 한 확장을 지원 하지 않으므로 ' *'입니다.

이것은 보통 Xamarin.iOS;의 버그를 나타냅니다. 에 버그 보고서를 제출 하세요 [http://bugzilla.xamarin.com](https://bugzilla.xamarin.com/enter_bug.cgi?product=iOS) 테스트 사례와 합니다.

### <a name="a-namemt0073mt0073-xamarinios--does-not-support-a-deployment-target-of--the-minimum-is--please-select-a-newer-deployment-target-in-your-projects-infoplist"></a><a name="MT0073"/>MT0073: Xamarin.iOS *의 배포 대상을 지원 하지 않습니다 * (최소값은 *). 프로젝트의 Info.plist에서 최신 배포 대상을 선택 하십시오.

최소 배포 대상이; 오류 메시지에 지정 된 프로젝트의 Info.plist에서 최신 배포 대상을 선택 하십시오.

배포 대상을 업데이트할 수 없는 경우 다음을 따르십시오 Xamarin.iOS의 이전 버전을.

### <a name="a-namemt0074mt0074-xamarinios--does-not-support-a-minimum-deployment-target-of--the-maximum-is--please-select-an-older-deployment-target-in-your-projects-infoplist-or-upgrade-to-a-newer-version-of-xamarinios"></a><a name="MT0074"/>MT0074: Xamarin.iOS *의 최소 배포 대상을 지원 하지 않습니다 * (최대값은 *). 프로젝트의 Info.plist에서 이전 배포 대상을 선택 하거나 Xamarin.iOS의 최신 버전으로 업그레이드 하세요.

Xamarin.iOS 용 Xamarin.iOS의이 특정 버전으로 빌드된 버전 보다 높은 버전을 최소 배포 대상을 설정 하는 것을 지원 하지 않습니다.

프로젝트의 Info.plist에서 이전 최소 배포 대상을 선택 하거나 Xamarin.iOS의 최신 버전으로 업그레이드 하세요.

### <a name="a-namemt0075mt0075-invalid-architecture--for--projects-valid-architectures-are-"></a><a name="MT0075"/>MT0075: 잘못 된 아키텍처 ' *'에 대 한 * 프로젝트. 올바른 아키텍처는: *

잘못 된 아키텍처를 지정 했습니다. 아키텍처가 유효한 지 확인 하십시오.

### <a name="a-namemt0076mt0075-no-architecture-specified-using-the---abi-argument-an-architecture-is-required-for--projects"></a><a name="MT0076"/>MT0075: 아키텍처 (-abi 인수 사용)을 지정 합니다. 아키텍처는 데 필요한 * 프로젝트.

이것은 보통 Xamarin.iOS;의 버그를 나타냅니다. 에 버그 보고서를 제출 하세요 [http://bugzilla.xamarin.com](https://bugzilla.xamarin.com/enter_bug.cgi?product=iOS) 테스트 사례와 합니다.

### <a name="a-namemt0077mt0076-watchos-projects-must-be-extensions"></a><a name="MT0077"/>MT0076: WatchOS 프로젝트 확장 이어야 합니다.

이것은 보통 Xamarin.iOS;의 버그를 나타냅니다. 에 버그 보고서를 제출 하세요 [http://bugzilla.xamarin.com](https://bugzilla.xamarin.com/enter_bug.cgi?product=iOS) 테스트 사례와 합니다.

### <a name="a-namemt0078mt0077-incremental-builds-are-enabled-with-a-deployment-target--80-currently--this-is-not-supported-the-resulting-application-will-not-launch-on-ios-9-so-the-deployment-target-will-be-set-to-80"></a><a name="MT0078"/>MT0077: 증분 빌드를 사용할 수 있는 배포 대상 < 8.0 (현재 *). 지원 되지 않습니다 (결과 응용 프로그램에서 iOS 9는 시작 되지 않는), 하므로 배포 대상을 8.0으로 설정 됩니다.

증분 빌드가 작업 제대로 배포 대상을이 빌드에 대 한 8.0으로 설정 되어 있는지를 알리는 경고입니다.

증분 빌드 배포 대상 이므로 8.0 이상 (그렇지 않은 경우 iOS 9에서 완성 된 응용 프로그램 시작 되지 않는) 하는 경우에 지원 됩니다.

### <a name="a-namemt0079mt0078-the-recommended-xcode-version-for-xamarinios--is-xcode--or-later-the-current-xcode-version-found-in--is-"></a><a name="MT0079"/>MT0078: 권장된 Xcode 버전 Xamarin.iOS에 대 한 * Xcode가 * 이상. 현재는 Xcode 버전 (에 *)는 *입니다.

현재 버전의 Xcode이 버전의 Xamarin.iOS Xcode의 권장된 버전 없다는 경고입니다.

Xcode 최적 동작을 보장 하기를 업그레이드 하십시오.

### <a name="a-namemt0080mt0080-disabling-newrefcount---new-refcountfalse-is-deprecated"></a><a name="MT0080"/>MT0080: NewRefCount 사용 하지 않도록 설정,--새로 만들기-refcount:false, 사용 되지 않습니다.

이 알리는 경고는 새를 사용 하지 않도록 요청 refcount (-새로 만들기-refcount:false) 무시 되었습니다.

새로운 refcount 기능은 모든 프로젝트에 대 한 필수 이제 이며 불가능 하므로 더 이상 사용 하지 않도록 설정 하려면.

### <a name="a-namemt0081mt0081-the-command-line-argument---download-crash-report-also-requires---download-crash-report-to"></a><a name="MT0081"/>MT0081: 명령줄 인수-다운로드 충돌 보고도-다운로드-크래시-보고서-하려면 필요합니다.
### <a name="a-namemt0082mt0082-repl---enable-repl-is-only-supported-when-linking-is-not-used---nolink"></a><a name="MT0082"/>MT0082: REPL (-enable repl) 연결 사용 되지 않는 경우만 지원 됩니다 (-nolink).
### <a name="a-namemt0083mt0083-asm-only-bitcode-is-not-supported-on-watchos-use-either---bitcodemarker-or---bitcodefull"></a><a name="MT0083"/>MT0083: Asm 전용 bitcode watchOS에서 지원 되지 않습니다. -Bitcode 중 하나를 사용 하 여: 표식 또는-bitcode: 전체.
### <a name="a-namemt0084mt0084-bitcode-is-not-supported-in-the-simulator-do-not-pass---bitcode-when-building-for-the-simulator"></a><a name="MT0084"/>MT0084: Bitcode 시뮬레이터에서 지원 되지 않습니다. 시뮬레이터를 빌드할 때-bitcode를 전달 하지 마십시오.
### <a name="a-namemt0085mt0085-no-reference-to--was-found-it-will-be-added-automatically"></a><a name="MT0085"/>MT0085:에 대 한 참조 ' *'를 찾을 수 있습니다. 자동으로 추가 됩니다.
### <a name="a-namemt0086mt0086-a-target-framework---target-framework-must-be-specified-when-building-for-tvos-or-watchos"></a><a name="MT0086"/>MT0086: 대상 프레임 워크 (-대상 프레임 워크) TVOS 또는 WatchOS 빌드할 때 지정 해야 합니다.

이것은 보통 Xamarin.iOS;의 버그를 나타냅니다. 에 버그 보고서를 제출 하세요 [http://bugzilla.xamarin.com](https://bugzilla.xamarin.com/enter_bug.cgi?product=iOS) 테스트 사례와 합니다.

### <a name="a-namemt0087mt0087-incremental-builds---fastdev-is-not-supported-with-the-boehm-gc-incremental-builds-will-be-disabled"></a><a name="MT0087"/>MT0087: 증분 빌드 (-fastdev) Boehm GC 지원 되지 않습니다. 증분 빌드를 사용할 수 없습니다.

### <a name="a-namemt0088mt0088-the-gc-must-be-in-cooperative-mode-for-watchos-apps-please-remove-the---coopfalse-argument-to-mtouch"></a><a name="MT0088"/>MT0088: GC watchOS 앱에 대 한 공동 작업 모드에 있어야 합니다. 제거 하십시오--coop: false 인수 mtouch입니다.

### <a name="a-namemt0089mt0089-the-option--cannot-take-the-value--when-cooperative-mode-is-enabled-for-the-gc"></a><a name="MT0089"/>MT0089: 옵션 '\*'값을 가져올 수 없습니다'\*' gc 협력 모드 활성화 된 경우.

### <a name="a-namemt0091mt0091-this-version-of-xamarinios-requires-the--sdk-shipped-with-xcode--either-upgrade-xcode-to-get-the-required-header-files-or-set-the-managed-linker-behaviour-to-link-framework-sdks-only-to-try-to-avoid-the-new-apis"></a><a name="MT0091"/>MT0091:이 버전의 Xamarin.iOS 필요는 * SDK (Xcode와 함께 제공 *). 경우 필요한 헤더 파일을 가져오거나를 링크 프레임 워크 Sdk (로 새 Api를 방지 하기 위해 시도)의 관리 되는 링커 동작을 설정 하는 Xcode를 업그레이드 합니다.

Xamarin.iOS 헤더 파일, 응용 프로그램을 빌드하고 오류 메시지에 지정 된 SDK 버전에서 필요 합니다. 이 오류를 해결 하는 권장된 방법은 필요한 SDK를 가져오려는 Xcode를 업그레이드 하는, 여기에 모든 필수 헤더 파일 포함 됩니다. 여러 버전의 Xcode 설치 했거나는 Xcode 기본이 아닌 위치에서 사용할 경우에 IDE의 기본 설정에서 올바른 Xcode 위치를 설정 해야 합니다.

잠재적을 대체 솔루션은 관리 되는 링커를 사용 하도록 설정입니다. 사용 되지 않는 API 등 대부분의 경우 헤더 파일이 없습니다 (또는 불완전) 있는 새로운 API 제거 합니다. 그러나가 제공이 프로젝트에서 프로그램 Xcode 1 보다 최신 SDK에 도입 된 API를 사용 하는 경우를 작동 하지 않습니다.

몰 랐 어 요 솔루션 Xamarin.iOS의 이전 버전을 사용 하는 것을 지 원하는 SDK 프로젝트가 필요 합니다.

<!-- MT0092 used by mlaunch -->

### <a name="a-namemt0093mt0093-could-not-find-mlaunch"></a><a name="MT0093"/>MT0093: 'mlaunch'를 찾을 수 없습니다.

<!-- MT0094 is not reported anymore -->

### <a name="a-namemt0095mt0095-aot-files-could-not-be-copied-to-the-destination-directory-dest-error"></a><a name="MT0095"/>MT0095: Aot 파일 {dest (를) 대상 디렉터리에 복사할 수 없습니다. {error}

### <a name="a-namemt0096mt0096-no-reference-to-xamariniosdll-was-found"></a><a name="MT0096"/>MT0096: Xamarin.iOS.dll에 대 한 참조를 찾을 수 있습니다.

<!-- MT0097: used by mmp -->
<!-- MT0098: used by mmp -->

### <a name="a-namemt0099mt0099-internal-error--please-file-a-bug-report-with-a-test-case-httpbugzillaxamarincom"></a><a name="MT0099"/>: MT0099 내부 오류 * 합니다. 테스트 사례 (http://bugzilla.xamarin.com)를 사용 하 여 버그 보고서를 제출 하세요.

Xamarin.iOS에 내부 일관성 확인 작업을 실패 한 경우이 오류 메시지가 보고 됩니다.

이 Xamarin.iOS;의 버그를 나타냅니다. 에 버그 보고서를 제출 하세요 [http://bugzilla.xamarin.com](https://bugzilla.xamarin.com/enter_bug.cgi?product=iOS) 테스트 사례와 합니다.

### <a name="a-namemt0100mt0100-invalid-assembly-build-target--please-file-a-bug-report-with-a-test-case-httpbugzillaxamarincom"></a><a name="MT0100"/>MT0100: 잘못 된 어셈블리 빌드 대상: ' *'입니다. 테스트 사례 (http://bugzilla.xamarin.com)를 사용 하 여 버그 보고서를 제출 하세요.

Xamarin.iOS에 내부 일관성 확인 작업을 실패 한 경우이 오류 메시지가 보고 됩니다.

이 값은 항상 Xamarin.iOS;의 버그 에 버그 보고서를 제출 하세요 [http://bugzilla.xamarin.com](https://bugzilla.xamarin.com/enter_bug.cgi?product=iOS) 테스트 사례와 합니다.

### <a name="a-namemt0101mt0101-the-assembly--is-specified-multiple-times-in---assembly-build-target-arguments"></a><a name="MT0101"/>MT0101: 어셈블리 ' *' 인--어셈블리 빌드 대상을 인수가 여러 번 지정 되었습니다.

오류 메시지에 언급 된 어셈블리-어셈블리 빌드 대상을 인수에 여러 번 지정 됩니다. 각 어셈블리는 한 번 언급만 있는지 확인 하십시오.

### <a name="a-namemt0102mt0102-the-assemblies--and--have-the-same-target-name--but-different-targets--and-"></a><a name="MT0102"/>MT0102: 어셈블리\*'및'\*' 대상 이름이 같습니다 ('\*'), 하지만 서로 다른 대상 ('\*' 및 ' *').

오류 메시지에는 어셈블리에는 충돌 하는 빌드 대상을 있습니다.

예:

    --assembly-build-target:Assembly1.dll=framework=MyBinary --assembly-build-target:Assembly2.dll=dynamiclibrary=MyBinary

이 예에서는 동적 라이브러리와 프레임 워크 모두 동일한 제조원을 만들려고 시도 (`MyBinary`).

### <a name="a-namemt0103mt0103-the-static-object--contains-more-than-one-assembly--but-each-static-object-must-correspond-with-exactly-one-assembly"></a><a name="MT0103"/>MT0103: 정적 개체 '\*' 둘 이상의 어셈블리가 포함 되어 있습니다 ('\*'), 각 정적 개체는 정확히 하나의 어셈블리와 일치 해야 하지만 합니다.

오류 메시지에 언급 된 어셈블리는 모두 단일 정적 개체에 컴파일됩니다. 이 허용 되지, 다른 정적 개체에는 모든 어셈블리를 컴파일해야 합니다.

예:

    --assembly-build-target:Assembly1.dll=staticobject=MyBinary --assembly-build-target:Assembly2.dll=staticobject=MyBinary

이 예에서는 정적 개체를 작성 하려고 (`MyBinary`) 두 어셈블리 구성 (`Assembly1.dll` 및 `Assembly2.dll`), 허용 되지 않는 합니다.

### <a name="a-namemt0105mt0105-no-assembly-build-target-was-specified-for-"></a><a name="MT0105"/>MT0105:에 대 한 지정 된 어셈블리 빌드 대상이 없습니다 ' *'입니다.

사용 하 여 대상 빌드 어셈블리를 지정 `--assembly-build-target`, 앱에서 모든 어셈블리에 할당 된 빌드 대상이 있어야 합니다.

이 오류는 오류 메시지에 언급 된 어셈블리에 빌드 할당 대상 어셈블리 없을 때 보고 됩니다.

에 대 한 설명서를 참조 하십시오. `--assembly-build-target` 자세한 정보.

### <a name="a-namemt0106mt0106-the-assembly-build-target-name--is-invalid-the-character--is-not-allowed"></a><a name="MT0106"/>MT0106: 어셈블리 빌드 대상 이름 '\*' 올바르지 않습니다: 문자 '\*' 허용 되지 않습니다.

어셈블리 빌드 대상 이름에는 유효한 파일 이름 이어야 합니다.

예를 들어 이러한 값이이 오류가 발생 합니다.

    --assembly-build-target:Assembly1.dll=staticobject=my/path.o

때문에 `my/path.o` 이 디렉터리 구분 문자로 인해 유효한 파일 이름이 아닙니다.

### <a name="a-namemt0107mt0107-the-assemblies--have-different-custom-llvm-optimizations--which-is-not-allowed-when-they-are-all-compiled-to-a-single-binary"></a><a name="MT0107"/>MT0107: 어셈블리\*' 다른 사용자 지정 원하는 LLVM 최적화 (\*)는 모두 컴파일되는 경우 단일 이진이 허용 되지 않습니다.

### <a name="a-namemt0108mt0108-the-assembly-build-target--did-not-match-any-assemblies"></a><a name="MT0108"/>MT0108: 어셈블리 빌드 대상 ' *'는 모든 어셈블리와 일치 하지 않습니다.

### <a name="a-namemt0109mt0109-the-assembly-0-was-loaded-from-a-different-path-than-the-provided-path-provided-path-1-actual-path-2"></a><a name="MT0109"/>MT0109: 어셈블리 ' {'이 (가) 제공된 된 경로 다른 경로에서 로드 된 (경로 제공: {1 \}, 실제 경로: {2 \}).

이 응용 프로그램에서 참조 하는 어셈블리 요청 된 수보다 다른 위치에서 로드 되었음을 나타내는 경고입니다.

응용 프로그램에 동일한 이름이 같지만 (첫 번째 어셈블리에만 사용) 하는 예기치 않은 결과가 발생할 수 있는 서로 다른 위치에서 여러 어셈블리를 참조 하는 것일 수 있습니다.

### <a name="a-namemt0110mt0110-incremental-builds-have-been-disabled-because-this-version-of-xamarinios-does-not-support-incremental-builds-in-projects-that-include-third-party-binding-libraries-and-that-compiles-to-bitcode"></a><a name="MT0110"/>MT0110: 증분 빌드 사용할 제 3 자 바인딩 라이브러리를 포함 하 고 있고 bitcode로 컴파일되는 프로젝트에서이 버전의 Xamarin.iOS 증분 빌드를 지원 하지 않으므로 합니다.

이 버전의 Xamarin.iOS 제 3 자 바인딩 라이브러리를 포함 하 고 있고 bitcode (tvOS 및 watchOS 프로젝트)로 컴파일되는 프로젝트의 증분 빌드를 지원 하지 않으므로 증분 빌드 비활성화 되었습니다.

아무 작업은 필요 하지 않습니다,이 메시지는 정보로 합니다.

자세한 내용은 참조 하십시오. 버그 번호[51710](https://bugzilla.xamarin.com/show_bug.cgi?id=51710)합니다.

이 경고는 더 이상 보고 되지 않습니다.

### <a name="a-namemt0111mt0111-bitcode-has-been-enabled-because-this-version-of-xamarinios-does-not-support-building-watchos-projects-using-llvm-without-enabling-bitcode"></a><a name="MT0111"/>MT0111: Bitcode 설정한이 버전의 Xamarin.iOS 건물 watchOS를 지원 하지 않으므로 bitcode 사용 하지 않고 원하는 LLVM를 사용 하 여 프로젝트입니다.

이 버전의 Xamarin.iOS 건물 watchOS를 지원 하지 않으므로 Bitcode 자동으로 설정 된가 원하는 LLVM bitcode 사용 하지 않더라도 사용 하 여 프로젝트입니다.

아무 작업은 필요 하지 않습니다,이 메시지는 정보로 합니다.

자세한 내용은 참조 하십시오. 버그 번호[51634](https://bugzilla.xamarin.com/show_bug.cgi?id=51634)합니다.

### <a name="a-namemt0112mt0112-native-code-sharing-has-been-disabled-because-"></a><a name="MT0112"/>MT0112: 네이티브 코드 공유에 있으므로 비활성화 되었습니다. *

여러 가지 방법으로 코드 공유를 해제할 수 있습니다.

* 컨테이너 응용 프로그램의 배포 대상 iOS 8.0 보다 이전 이므로 (있기 *)).

네이티브 코드 공유 필요 iOS 8.0 네이티브 코드 공유 사용자 프레임 워크를 사용 하 여 구현 되기 때문에 있는 iOS 8.0에 도입 되었습니다.

* 컨테이너 응용 프로그램 I18N 어셈블리 (*) 포함 하기 때문에

네이티브 코드 공유는 현재 지원 되지 않습니다 컨테이너 응용 프로그램 I18N 어셈블리를 포함 하는 경우.

* 컨테이너 응용 프로그램에 관리 되는 링커 (*)에 대 한 사용자 지정 xml 정의 합니다.

네이티브 코드 공유 하려면 되어야 관리 되는 링커에 대 한 사용자 지정 xml 정의 사용 하는 프로젝트에 지원 되지 않습니다.


### <a name="a-namemt0113mt0113-native-code-sharing-has-been-disabled-for-the-extension--because-"></a><a name="MT0113"/>MT0113: 네이티브 코드 공유 비활성화 된 확장에 대해 ' *' 이므로 * 합니다.

* 컨테이너 응용 프로그램 간에 다를 bitcode 옵션 때문에 (\*) 및 확장 (\*).

  네이티브 코드 공유 코드를 공유 하는 프로젝트 간의 bitcode 옵션 일치 해야 합니다.

* 때문에--어셈블리 빌드 대상을 옵션은 컨테이너 응용 프로그램 간에 다릅니다 (\*) 및 확장 (\*).

  사용 하려면 네이티브 코드 공유는--어셈블리 빌드 대상을 옵션은 코드를 공유 하는 프로젝트 간의 동일 합니다.

  증분 빌드 겹치지 설정 또는 해제 모든 프로젝트에서이 오류가 발생할 수 있습니다.

* 컨테이너 응용 프로그램 간에 I18N 어셈블리 다르기 때문에 (\*) 및 확장 (\*).

  네이티브 코드 공유는 현재 지원 되지 않습니다 I18N 어셈블리를 포함 하는 확장에 대 한 합니다.

* 컨테이너 응용 프로그램 간에 AOT 컴파일러에 대 한 인수 다르기 때문에 (\*) 및 확장 (\*).

  네이티브 코드 공유 필요 AOT 컴파일러에 대 한 인수는 코드를 공유 하는 프로젝트 간의 차이 하지 않습니다.

* 컨테이너 응용 프로그램 간에 AOT 컴파일러에 대 한 다른 인수 다르기 때문에 (\*) 및 확장 (\*).

  네이티브 코드 공유 필요 AOT 컴파일러에 대 한 인수는 코드를 공유 하는 프로젝트 간의 차이 하지 않습니다.

  이 상태는 ' 모든 32 비트 float로 작업을 수행할 64 비트 float' 프로젝트 마다 다를 경우에 발생 합니다.

* 원하는 LLVM 하지 않을 지 설정 컨테이너 앱에서 때문에 (\*) 및 확장 (\*).

  네이티브 코드 공유를 원하는 LLVM 사용 되거나 코드를 공유 하는 모든 프로젝트에 대해 사용 하지 않도록 설정 해야 합니다.

* 컨테이너 응용 프로그램 간에 관리 되는 링커 설정이 다르기 때문에 (\*) 및 확장 (\*).

  네이티브 코드 공유 동일 해야 하는 관리 되는 링커 설정이 코드를 공유 하는 모든 프로젝트에 대 한 합니다.

* 관리 되는 링커 건너뛴된 어셈블리 컨테이너 응용 프로그램 간에 다르기 때문에 (\*) 및 확장 (\*).

  네이티브 코드 공유 동일 해야 하는 관리 되는 링커 설정이 코드를 공유 하는 모든 프로젝트에 대 한 합니다.

* 확장에 관리 되는 링커 (*)에 대 한 사용자 지정 xml 정의 합니다.

  네이티브 코드 공유 하려면 되어야 관리 되는 링커에 대 한 사용자 지정 xml 정의 사용 하는 프로젝트에 지원 되지 않습니다.

* ABI에 대 한 컨테이너 응용 프로그램을 작성 하지 않습니다 때문에 * (이 ABI에 대 한 확장에서는 구축) 하는 중입니다.

  네이티브 코드 공유 컨테이너 응용 프로그램 빌드 서비스나 응용 프로그램 확장 빌드에 대 한 모든 아키텍처에 대 한 필요 합니다.

  예를 들어:이 상태 ARM64 + ARMv7에 대 한 확장 작성은 하지만 컨테이너 앱만 빌드 ARM64에 대 한 경우에 발생 합니다.

* ABI에 대 한 컨테이너 응용 프로그램 빌드 중 이므로 \*, 확장의 ABI와 호환 되지 않는 (\*).

  네이티브 코드 공유 정확히 동일한 API에 대 한 모든 프로젝트 빌드 필요 합니다.

  예를 들어:이 상태 ARMv7 + 원하는 llvm + thumb2에 대 한 확장 작성은 하지만 컨테이너 앱만 ARMv7 + 원하는 llvm 작성 하는 경우에 발생 합니다.

* 컨테이너 응용 프로그램에서 어셈블리를 참조 하기 때문에 '\*'from'\*' 확장에서 다른 버전을 참조 하는 반면, ' *'입니다.

  네이티브 코드 공유 코드를 공유 하는 모든 프로젝트는 모든 어셈블리에 대해 동일한 버전을 사용 해야 합니다.

<!-- MT0114: used by mmp -->

### <a name="a-namemt0115mt0115-it-is-recommended-to-reference-dynamic-symbols-using-code---dynamic-symbol-modecode-when-bitcode-is-enabled"></a><a name="MT0115"/>MT0115: 것이 좋습니다 참조 코드를 사용 하 여 동적 기호 (-동적 기호 모드 = 코드) bitcode 사용 되는 경우.

Xamarin.iOS 프로젝트는 자주 참조 네이티브 기호가 동적으로 의미 하는 네이티브 링커가 네이티브 연결 프로세스 중 네이티브 그러한 기호를 제거할 수 있으므로 이러한 기호를 사용 하는 네이티브 링커는 표시 되지 않습니다.

일반적으로 Xamarin.iOS 그러한 기호를 유지 하려면 기본 링커 묻습니다 (사용 하는 `-u symbol` 링커 플래그), 하지만 때 네이티브 링커 bitcode에 대 한 컴파일을 허용 하지 않습니다는 `-u` 플래그입니다.

Xamarin.iOS 대체 솔루션을 구현 했습니다: 이러한 기호를 참조 하는 추가 네이티브 코드 생성 하 고 따라서 네이티브 링커 이러한 기호를 사용 하는 표시 됩니다. 이 bitcode로 컴파일할 경우 자동으로 수행 됩니다.

경우 `--dynamic-symbol-mode=linker` mtouch, 대체이 솔루션은 비활성화 되 고 Xamarin.iOS는 전달 하려고에 전달 되 `-u` 네이티브 링커에 합니다. 이 대개 네이티브 링커 오류가 발생 합니다.

솔루션 제거 하는 것은 `--dynamic-symbol-mode=linker` 프로젝트의 빌드 옵션에서 추가 mtouch 인수에서 인수입니다.

<!-- 0116 - 0124: free to use -->

### <a name="a-namemt0125mt0125-the---assembly-build-target-command-line-argument-is-ignored-in-the-simulator"></a><a name="MT0125"/>MT0125:--어셈블리-빌드 대상을 시뮬레이터에서 명령줄 인수는 무시 됩니다.

동작은 필요 하지 않습니다,이 메시지는 정보로 합니다.

### <a name="a-namemt0126mt0126-incremental-builds-have-been-disabled-because-incremental-builds-are-not-supported-in-the-simulator"></a><a name="MT0126"/>MT0126: 증분 빌드 사용할 증분 빌드 시뮬레이터에서 지원 되지 않기 때문입니다.

동작은 필요 하지 않습니다,이 메시지는 정보로 합니다.

### <a name="a-namemt0127mt0127-incremental-builds-have-been-disabled-because-this-version-of-xamarinios-does-not-support-incremental-builds-in-projects-that-include-more-than-one-third-party-binding-libraries"></a><a name="MT0127"/>MT0127: 증분 빌드 사용할 Xamarin.iOS의이 버전 이상 1/3 파티 바인딩 라이브러리를 포함 하는 프로젝트의 증분 빌드를 지원 하지 않으므로 합니다.

이 버전의 Xamarin.iOS 항상 빌드하지 않는 여러 공급 업체 바인딩 라이브러리를 사용 하 여 프로젝트 올바르게 때문에 증분 빌드가 자동으로 비활성화 되었습니다.

동작은 필요 하지 않습니다,이 메시지는 정보로 합니다.

자세한 내용은 참조 하십시오. 버그 번호[52727](https://bugzilla.xamarin.com/show_bug.cgi?id=52727)합니다.

## <a name="mt1xxx-project-related-error-messages"></a>MT1xxx: 프로젝트와 관련 된 오류 메시지

### <a name="mt10xx-installer--mtouch"></a>MT10xx: 설치 관리자 / mtouch

<!--
 MT1xxx file copy / symlinks (project related)
  MT10xx installer.cs / mtouch.cs
  -->

### <a name="a-namemt1001mt1001-could-not-find-an-application-at-the-specified-directory"></a><a name="MT1001"/>지정된 된 디렉터리에 응용 프로그램을 찾을 MT1001 수 없습니다.



### <a name="a-namemt1002mt1002-could-not-create-symlinks-files-were-copied"></a><a name="MT1002"/>MT1002 만들 수 없습니다 symlink, 파일 복사



### <a name="a-namemt1003mt1003-could-not-kill-the-application--you-may-have-to-kill-the-application-manually"></a><a name="MT1003"/>응용 프로그램을 종료 하지 MT1003 수 없습니다. ' *'입니다. 응용 프로그램을 수동으로 중지 해야 할 수 있습니다.



### <a name="a-namemt1004mt1004-could-not-get-the-list-of-installed-applications"></a><a name="MT1004"/>설치 된 응용 프로그램의 목록을 가져올 수 없습니다 MT1004 수 없습니다.



### <a name="a-namemt1005mt1005-could-not-kill-the-application--on-the-device----you-may-have-to-kill-the-application-manually"></a><a name="MT1005"/>응용 프로그램을 종료 하지 MT1005 수 없습니다. '\*'' 장치에서\*': *-응용 프로그램을 수동으로 중지 해야 할 수 있습니다.



### <a name="a-namemt1006mt1006-could-not-install-the-application--on-the-device--"></a><a name="MT1006"/>응용 프로그램을 설치 MT1006 수 없습니다. '\*'' 장치에서\*': * 합니다.



### <a name="a-namemt1007mt1007-failed-to-launch-the-application--on-the-device---you-can-still-launch-the-application-manually-by-tapping-on-it"></a><a name="MT1007"/>응용 프로그램을 시작 하지 못했습니다 MT1007 '\*'' 장치에서\*': * 합니다. 여전히 응용 프로그램을 탭 하 여 수동으로 시작할 수 있습니다.



### <a name="a-namemt1008mt1008-failed-to-launch-the-simulator"></a><a name="MT1008"/>MT1008: 시뮬레이터를 시작 하지 못했습니다.



시뮬레이터를 시작 하지 못했습니다 mtouch 하는 경우이 오류가 보고 됩니다.   이러한 현상이 경우에 따라 실행 되는 유효 하지 않은 또는 데드 시뮬레이터 프로세스 이미 있기 때문에 합니다.

Unix 명령줄에서 실행 된 다음 명령이 걸린된 시뮬레이터 프로세스를 데 사용할 수 있습니다.

```bash
$ launchctl list|grep UIKitApplication|awk '{print $3}'|xargs launchctl remove
```

### <a name="a-namemt1009mt1009-could-not-copy-the-assembly--to--"></a><a name="MT1009"/>MT1009 복사할 수 없습니다. 어셈블리 '\*'to'\*': *

Xamarin.iOS의 특정 버전의 알려진된 문제입니다.

이를 경우 다음 해결 방법을 시도해 보십시오.

```csharp
sudo chmod 0644 /Library/Frameworks/Xamarin.iOS.framework/Versions/Current/lib/mono/*/*.mdb
```

그러나 Xamarin.iOS의 최신 버전에서이 문제가 해결 되었습니다, 이후 하십시오 새에서 버그를 보고할 [http://bugzilla.xamarin.com](https://bugzilla.xamarin.com/enter_bug.cgi?product=iOS) 정식 버전 정보 및 빌드 로그 출력 합니다.

### <a name="a-namemt1010mt1010-could-not-load-the-assembly--"></a><a name="MT1010"/>어셈블리를 로드할 MT1010 수 없습니다. ' *': *



### <a name="a-namemt1011mt1011-could-not-add-missing-resource-file-"></a><a name="MT1011"/>누락 된 리소스 파일을 추가 하지 MT1011 없습니다: ' *'



### <a name="a-namemt1012mt1012-failed-to-list-the-apps-on-the-device--"></a><a name="MT1012"/>장치에서 앱을 나열 하지 못했습니다 MT1012 ' *': *



### <a name="a-namemt1013mt1013-dependency-tracking-error-no-files-to-compare-please-file-a-bug-report-at-httpbugzillaxamarincom-with-a-test-case"></a><a name="MT1013"/>MT1013 종속성 오류 추적: 비교할 파일이 없습니다. 테스트 사례와 http://bugzilla.xamarin.com에 버그 보고서를 제출 하세요.

Xamarin.iOS에서 버그를 나타냅니다. 버그를 제출 하세요 [http://bugzilla.xamarin.com](https://bugzilla.xamarin.com/enter_bug.cgi?product=iOS) 테스트 caes 사용 합니다.

### <a name="a-namemt1014mt1014-failed-to-re-use-cached-version-of--"></a><a name="MT1014"/>MT1014 다시 캐시 된 버전을 사용 하지 못했습니다. ' *': * 합니다.



### <a name="a-namemt1015mt1015--failed-to-create-the-executable--"></a><a name="MT1015"/>MT1015 실행 파일을 만들지 못했습니다. ' *': *

### <a name="a-namemt1015mt1015--failed-to-create-the-executable--"></a><a name="MT1015"/>MT1015 실행 파일을 만들지 못했습니다. ' *': *

### <a name="a-namemt1016mt1016-failed-to-create-the-notice-file-because-a-directory-already-exists-with-the-same-name"></a><a name="MT1016"/>MT1016: 이름이 같은 디렉터리가 이미 있기 때문에 알림 파일을 만들지 못했습니다.

디렉터리를 제거 `NOTICE` 프로젝트에서.

### <a name="a-namemt1017mt1017-failed-to-create-the-notice-file-"></a><a name="MT1017"/>MT1017: 알림 파일을 만들지 못했습니다: * 합니다.

### <a name="a-namemt1018mt1018-your-application-failed-code-signing-checks-and-could-not-be-installed-on-the-device--check-your-certificates-provisioning-profiles-and-bundle-ids-probably-your-device-is-not-part-of-the-selected-provisioning-profile-error-0xe8008015"></a><a name="MT1018"/>MT1018: 응용 프로그램 코드 서명 검사에 실패 한 및 장치에 설치할 수 없습니다 ' *'입니다. 프로필을 프로 비전 인증서를 확인 하 고 번들 id 키를 누릅니다. 아마도 장치에 속하지 않습니다 선택한 프로 비전 프로필 (오류: 0xe8008015).
### <a name="a-namemt1019mt1019-your-application-has-entitlements-not-supported-by-your-current-provisioning-profile-and-could-not-be-installed-on-the-device--please-check-the-ios-device-log-for-more-detailed-information-error-0xe8008016"></a><a name="MT1019"/>MT1019: 응용 프로그램 자격 현재 프로비저닝 프로필에서 지원 하지는 및 장치에 설치할 수 없습니다 ' *'입니다. 자세한 내용은 iOS 장치 로그를 확인 하십시오 (오류: 0xe8008016).

이 경우에 발생할 수 있습니다.

* 응용 프로그램에 현재 프로 비전 프로필은 지원 하지 않는 자격.
  가능한 해결 방법:
  - 다른 프로 비전 프로필을 지 원하는 자격을 지정 응용 프로그램 요구 사항입니다.
  - 현재 프로 비전 프로필에서 지원 되지 않습니다 자격을 제거 합니다.
* 사용 하는 프로 비전 프로필에 포함 되지 않은 배포 하려고 하는 장치입니다.
  가능한 해결 방법:
  - Xcode에서 서식 파일에서 새 앱 만들고 같은 프로비저닝 프로필을 동일한 장치에 배포 합니다. 경우에 따라 Xcode 수 자동으로 새로 고침 프로 비전 프로필 (Xcode은 메시지를 표시 해야 할 다른 경우)에 새 장치입니다.
  -IOS Dev Center로 이동 하 고 새 장치를 프로 비전 프로필 업데이트로 다음 컴퓨터에 업데이트 된 프로비저닝 프로필을 다운로드 합니다.


대부분의 경우 오류에 대 한 자세한 내용은 iOS 장치 로그에 표시 됩니다는 문제 진단 도움이 될 수 있는 합니다.

### <a name="a-namemt1020mt1020-failed-to-launch-the-application--on-the-device--"></a><a name="MT1020"/>MT1020: 응용 프로그램을 시작 하지 못했습니다 '\*'' 장치에서\*': *

### <a name="a-namemt1021mt1021-could-not-copy-the-file--to--2"></a><a name="MT1021"/>MT1021: 파일을 복사할 수 없습니다 '\*'to'\*': {2 \}

파일을 복사할 수 없습니다. 복사 작업에서 오류 메시지에는 오류에 대 한 자세한 내용은 있습니다.

### <a name="a-namemt1022mt1022-could-not-copy-the-directory--to--2"></a><a name="MT1022"/>MT1022: 디렉터리를 복사할 수 없습니다. '\*'to'\*': {2 \}

디렉터리를 복사할 수 없습니다. 복사 작업에서 오류 메시지에는 오류에 대 한 자세한 내용은 있습니다.

### <a name="a-namemt1023mt1023-could-not-communicate-with-the-device-to-find-the-application---"></a><a name="MT1023"/>MT1023: 장치에서 응용 프로그램을 찾을를 통신할 수 없습니다 ' *': *

장치에 응용 프로그램을 조회 하려고 하는 오류가 발생 했습니다.

이 문제를 해결 하는 사항은 다음과 같습니다.

* 장치에서 응용 프로그램을 삭제 하 고 다시 시도 하십시오.
* 장치를 분리 하 고 다시 연결 합니다.
* 장치를 다시 부팅 합니다.
* Mac를 다시 부팅

### <a name="a-namemt1024mt1024-the-application-signature-could-not-be-verified-on-device--please-make-sure-that-the-provisioning-profile-is-installed-and-not-expired-error-0xe8008017"></a><a name="MT1024"/>MT1024: 응용 프로그램 서명 장치에서 확인할 수 없습니다 ' *'입니다. 프로비저닝 프로필이 설치 되어 만료 되지 있는지 확인 하십시오 (오류: 0xe8008017).

장치는 서명을 확인할 수 때문에 응용 프로그램 설치를 거부 합니다.

프로비저닝 프로필이 설치 되어 만료 되지 있는지 확인 하십시오.

### <a name="a-namemt1025mt1025-could-not-list-the-crash-reports-on-the-device-"></a><a name="MT1025"/>MT1025: 장치에서 충돌 보고서를 나열할 수 없습니다 * 합니다.

장치에서 충돌 보고서를 나열 하려면 동안 오류가 발생 했습니다.

이 문제를 해결 하는 사항은 다음과 같습니다.

* 장치에서 응용 프로그램을 삭제 하 고 다시 시도 하십시오.
* 장치를 분리 하 고 다시 연결 합니다.
* 장치를 다시 부팅 합니다.
* Mac를 다시 부팅
* (이렇게 하면 모든 충돌 보고서에서에서 제거 장치) iTunes와 장치를 동기화 합니다.

### <a name="a-namemt1026mt1026-could-not-download-the-crash-report--from-the-device-"></a><a name="MT1026"/>MT1026: 충돌 보고서를 다운로드할 수 없습니다. * 장치에서 *.

장치에서 충돌 보고서를 다운로드 하려고 할 때 오류가 있습니다.

이 문제를 해결 하는 사항은 다음과 같습니다.

* 장치에서 응용 프로그램을 삭제 하 고 다시 시도 하십시오.
* 장치를 분리 하 고 다시 연결 합니다.
* 장치를 다시 부팅 합니다.
* Mac를 다시 부팅
* (이렇게 하면 모든 충돌 보고서에서에서 제거 장치) iTunes와 장치를 동기화 합니다.

### <a name="a-namemt1027mt1027-cant-use-xcode-7-to-launch-applications-on-devices-with-ios--xcode-7-only-supports-ios-6"></a><a name="MT1027"/>MT1027: Xcode 7 +를 사용 하 여 ios 장치에서 응용 프로그램을 시작할 수 없습니다 * (Xcode 7은 iOS 6 이상만 지원함).

6.0 아래의 iOS 버전을 사용 하 여 장치에 응용 프로그램을 시작할 Xcode 7 +를 사용 하는 것이 불가능 합니다.

Xcode의 이전 버전을 사용 하거나 응용 프로그램에서 수동으로 시작 하려고를 탭 하세요.

### <a name="a-namemt1028mt1028-invalid-device-specification--expected-ios-watchos-or-all"></a><a name="MT1028"/>MT1028: 잘못 된 장치 사양: ' *'입니다. 예상된 'ios', 'watchos' 또는 'a l l'입니다.

장치 사양-를 사용 하 여 전달 된 장치가 유효 하지 않습니다. 유효한 값은: 'ios', 'watchos' 또는 'a l l'입니다.

### <a name="a-namemt1029mt1029-could-not-find-an-application-at-the-specified-directory-"></a><a name="MT1029"/>MT1029: 지정된 된 디렉터리에 응용 프로그램을 찾을 수 없습니다: *

-Launchdev에 전달 된 응용 프로그램 경로 존재 하지 않습니다. 올바른 앱 번들을 지정 하십시오.

### <a name="a-namemt1030mt1030-launching-applications-on-device-using-a-bundle-identifier-is-deprecated-please-pass-the-full-path-to-the-bundle-to-launch"></a><a name="MT1030"/>MT1030: 응용 프로그램 번들 식별자를 사용 하 여 장치에는 사용 되지 않습니다. 시작 하는 번들의 전체 경로 전달 하십시오.

앱 번들 id만 대신 장치에서 실행에 경로 전달 하는 것이 좋습니다.

### <a name="a-namemt1031mt1031-could-not-launch-the-app--on-the-device--because-the-device-is-locked-please-unlock-the-device-and-try-again"></a><a name="MT1031"/>MT1031: 응용 프로그램을 시작할 수 없습니다 '\*'' 장치에서\*' 장치가 잠겨 있기 때문에 있습니다. 장치의 잠금을 해제 하 고 다시 시도 하십시오.

장치의 잠금을 해제 하 고 다시 시도 하십시오.

### <a name="a-namemt1032mt1032-this-application-executable-might-be-too-large--mb-to-execute-on-device-if-bitcode-was-enabled-you-might-want-to-disable-it-for-development-it-is-only-required-to-submit-applications-to-apple"></a><a name="MT1032"/>MT1032:이 응용 프로그램 실행 파일이 너무 큽니다 (* MB) 장치에서 실행할 수 있습니다. Bitcode 설정한 개발에 사용 하지 않도록 설정 하려는 경우, 응용 프로그램 Apple 제출 해야만 합니다.

### <a name="a-namemt1033mt1033-could-not-uninstall-the-application--from-the-device--"></a><a name="MT1033"/>MT1033: 응용 프로그램을 제거 하지 못했습니다 '\*'' 장치에서에서\*': *

<!-- 1034 used by mmp -->

### <a name="a-namemt1035mt1035-cannot-include-different-versions-of-the-framework-name"></a><a name="MT1035"/>MT1035: 다른 버전의 framework '{name}'를 포함할 수 없습니다.

다른 버전의 동일한 프레임 워크와 연결 하는 것이 불가능 합니다.

이 문제는 일반적으로 확장 될 수 (제 3 자 바인딩 어셈블리)를 통해 컨테이너 응용 프로그램 보다는 프레임 워크의 서로 다른 버전을 참조 하는 경우 발생 합니다.

이 오류 메시지가 나타나면 있을 여러 [MT1036](#MT1036) 오류 각 다른 프레임 워크에 대 한 경로 나열 합니다.

### <a name="a-namemt1036mt1036-framework-name-included-from-path-related-to-previous-error"></a><a name="MT1036"/>MT1036:에서 포함 된 프레임 워크 '{name}': {path} (이전 오류에 관련)

이 오류만 함께 보고 됩니다 [MT1036](#MT1036)합니다. 참조 하십시오 [MT1036](#MT1036) 자세한 정보에 대 한 합니다.

### <a name="mt11xx-debug-service"></a>MT11xx: 서비스를 디버깅 합니다.

<!--
  MT11xx DebugService.cs
  -->

### <a name="a-namemt1101mt1101-could-not-start-app"></a><a name="MT1101"/>응용 프로그램을 시작 MT1101 수 없습니다.



### <a name="a-namemt1102mt1102-could-not-attach-to-the-app-to-kill-it-"></a><a name="MT1102"/>응용 프로그램에서 (중지)에 연결 하지 MT1102 못했습니다: *



### <a name="a-namemt1103mt1103-could-not-detach"></a><a name="MT1103"/>분리할 MT1103 수 없습니다.



### <a name="a-namemt1104mt1104-failed-to-send-packet-"></a><a name="MT1104"/>MT1104 패킷을 보내지 못했습니다: *



### <a name="a-namemt1105mt1105-unexpected-response-type"></a><a name="MT1105"/>MT1105 예기치 않은 응답 유형



### <a name="a-namemt1106mt1106-could-not-get-list-of-applications-on-the-device-request-timed-out"></a><a name="MT1106"/>장치에서 응용 프로그램의 목록을 가져올 MT1106 수 없습니다: 요청 시간이 초과 되었습니다.



### <a name="a-namemt1107mt1107-application-failed-to-launch-"></a><a name="MT1107"/>MT1107: 응용 프로그램을 시작 하지 못했습니다: *

장치가 잠겨 있는지 확인 하십시오.

엔터프라이즈 응용 프로그램에서 배포 하는 되었거나 무료 프로 비전 프로필을 사용 하는 개발자를 신뢰 (이 <a href="http://stackoverflow.com/a/30726375/183422">여기</a>).

### <a name="a-namemt1108mt1108-could-not-find-developer-tools-for-this-xx-yy-device"></a><a name="MT1108"/>MT1108:이 XX (YY) 장치에 대 한 개발자 도구를 찾을 수 없습니다.

Mtouch에서 몇 가지 작업에 필요는 <tt>DeveloperDiskImage.dmg</tt> 파일에 존재 하도록 합니다.   이 파일 Xcode의 일부 이며에 검사를 작성 하는 데 사용 하는 SDK를 기준으로 일반적으로 위치한는 <tt>Xcode.app/Contents/Developer/iPhoneOS.platform/DeviceSupport/VERSION/DeveloperDiskImage.dmg</tt>합니다.

이 오류와 연결 된 장치를 일치 하는 DeveloperDiskImage.dmg 없기 때문에 발생할 수도 있습니다.


### <a name="a-namemt1109mt1109-application-failed-to-launch-because-the-device-is-locked-please-unlock-the-device-and-try-again"></a><a name="MT1109"/>MT1109: 응용 프로그램 장치가 잠겨 있기 때문에 시작 하지 못했습니다. 장치의 잠금을 해제 하 고 다시 시도 하십시오.

장치가 잠겨 있는지 확인 하십시오.

### <a name="a-namemt1110mt1110-application-failed-to-launch-because-of-ios-security-restrictions-please-ensure-the-developer-is-trusted"></a><a name="MT1110"/>MT1110: 응용 프로그램 iOS 보안 제한으로 인해 실행 하지 못했습니다. 개발자는 신뢰할 수 있는 확인 하십시오.

엔터프라이즈 응용 프로그램에서 배포 하는 되었거나 무료 프로 비전 프로필을 사용 하는 개발자를 신뢰 (이 <a href="http://stackoverflow.com/a/30726375/183422">여기</a>).

### <a name="mt12xx-simulator"></a>MT12xx: 시뮬레이터

<!--
  MT12xx simcontroller.cs
  -->

### <a name="a-namemt1201mt1201-could-not-load-the-simulator-"></a><a name="MT1201"/>MT1201: 시뮬레이터를 로드할 수 없습니다: *
### <a name="a-namemt1202mt1202-invalid-simulator-configuration-"></a><a name="MT1202"/>MT1202: 잘못 된 시뮬레이터 구성: *
### <a name="a-namemt1203mt1203-invalid-simulator-specification-"></a><a name="MT1203"/>MT1203: 잘못 된 시뮬레이터 사양: *
### <a name="a-namemt1204mt1204-invalid-simulator-specification--runtime-not-specified"></a><a name="MT1204"/>MT1204: 잘못 된 시뮬레이터 사양 ' *': 런타임 지정 되지 않았습니다.
### <a name="a-namemt1205mt1205-invalid-simulator-specification--device-type-not-specified"></a><a name="MT1205"/>MT1205: 잘못 된 시뮬레이터 사양 ' *': 장치 유형이 지정 되지 않았습니다.
### <a name="a-namemt1206mt1206-could-not-find-the-simulator-runtime-"></a><a name="MT1206"/>MT1206: 시뮬레이터 런타임을 찾을 수 없습니다 ' *'입니다.
### <a name="a-namemt1207mt1207-could-not-find-the-simulator-device-type-"></a><a name="MT1207"/>MT1207: 시뮬레이터 장치 종류를 찾을 수 없습니다 ' *'입니다.
### <a name="a-namemt1208mt1208-could-not-find-the-simulator-runtime-"></a><a name="MT1208"/>MT1208: 시뮬레이터 런타임을 찾을 수 없습니다 ' *'입니다.
### <a name="a-namemt1209mt1209-could-not-find-the-simulator-device-type-"></a><a name="MT1209"/>MT1209: 시뮬레이터 장치 종류를 찾을 수 없습니다 ' *'입니다.
### <a name="a-namemt1210mt1210-invalid-simulator-specification--unknown-key-"></a><a name="MT1210"/>MT1210: 잘못 된 시뮬레이터 사양: \*, 알 수 없는 키 '\*'
### <a name="a-namemt1211mt1211-the-simulator-version--does-not-support-the-simulator-type-"></a><a name="MT1211"/>MT1211: simulator 버전 '\*'시뮬레이터 유형을 지원 하지 않는'\*'
### <a name="a-namemt1212mt1212-failed-to-create-a-simulator-version-where-type---and-runtime--"></a><a name="MT1212"/>MT1212: 시뮬레이터 버전을 만들지 못했습니다 입력할 수 있는 = * 런타임 및 = * 합니다.
### <a name="a-namemt1213mt1213-invalid-simulator-specification-for-xcode-4-"></a><a name="MT1213"/>MT1213: Xcode 4에 대 한 잘못 된 시뮬레이터 사양을: *
### <a name="a-namemt1214mt1214-invalid-simulator-specification-for-xcode-5-"></a><a name="MT1214"/>MT1214: Xcode 5에 대 한 잘못 된 시뮬레이터 사양을: *
### <a name="a-namemt1215mt1215-invalid-sdk-specified-"></a><a name="MT1215"/>MT1215: 지정 된 잘못 된 SDK: *
### <a name="a-namemt1216mt1216-could-not-find-the-simulator-udid-"></a><a name="MT1216"/>MT1216: UDID 시뮬레이터를 찾을 수 없습니다 ' *'입니다.
### <a name="a-namemt1217mt1217-could-not-load-the-app-bundle-at-"></a><a name="MT1217"/>MT1217:에 앱 번들에 로드할 수 없습니다. ' *'입니다.
### <a name="a-namemt1218mt1218-no-bundle-identifier-found-in-the-app-at-"></a><a name="MT1218"/>MT1218: 응용 프로그램에서 있는 번들 식별자 없이 ' *'입니다.
### <a name="a-namemt1219mt1219-could-not-find-the-simulator-for-"></a><a name="MT1219"/>MT1219:에 대 한 시뮬레이터를 찾을 수 없습니다 ' *'입니다.
### <a name="a-namemt1220mt1220-could-not-find-the-latest-simulator-runtime-for-device-"></a><a name="MT1220"/>MT1220: 장치에 대 한 최신 시뮬레이터 런타임의 찾을 수 없습니다 ' *'입니다.

이 일반적으로 Xcode에 문제가 있음을 나타냅니다.

이 문제를 해결 하는 사항은 다음과 같습니다.

* Xcode에서 시뮬레이터를 두 번 사용 합니다.
* -Sdk를 사용 하 여 특정 SDK 버전을 전달 <version>합니다.
* Xcode를 다시 설치 합니다.

### <a name="a-namemt1221mt1221-could-not-find-the-paired-iphone-simulator-for-the-watchos-simulator-"></a><a name="MT1221"/>MT1221: WatchOS 시뮬레이터에 대 한 쌍을 이루는 iPhone 시뮬레이터를 찾을 수 없습니다 ' *'입니다.

WatchOS 시뮬레이터 WatchOS 응용 프로그램을 시작할 때는 쌍으로 연결 된 iOS 시뮬레이터 뿐 이어야 합니다.

감시 시뮬레이터 iOS Xcode의 장치 UI를 사용 하 여 시뮬레이터와 연결할 수 있습니다 (창 메뉴-> 장치).

### <a name="mt13xx-linkwith"></a>MT13xx: [LinkWith]

<!--
  MT13xx [LinkWith]
  -->


### <a name="a-namemt1301mt1301-native-library---was-ignored-since-it-does-not-match-the-current-build-architectures-"></a><a name="MT1301"/>MT1301 네이티브 라이브러리 `*` (\*) 현재 빌드 architecture(s) 일치 하지 않기 때문에 무시 되었습니다 (\*)



### <a name="a-namemt1302mt1302-could-not-extract-the-native-library--from--please-ensure-the-native-library-was-properly-embedded-in-the-managed-assembly-if-the-assembly-was-built-using-a-binding-project-the-native-library-must-be-included-in-the-project-and-its-build-action-must-be-objcbindingnativelibrary"></a><a name="MT1302"/>네이티브 라이브러리를 추출 하지 MT1302 못했습니다 ' *'에서 '+'. 네이티브 라이브러리 (어셈블리가 바인딩 프로젝트를 사용 하 여 작성 하 고 네이티브 라이브러리 프로젝트에 포함 되어야 합니다 빌드 작업 'ObjcBindingNativeLibrary' 해야 합니다.) 경우 제대로 관리 되는 어셈블리에 포함 된 있는지 확인 하십시오.

### <a name="a-namemt1303mt1303-could-not-decompress-the-native-framework--from--please-review-the-build-log-for-more-information-from-the-native-zip-command"></a><a name="MT1303"/>MT1303: 네이티브 프레임 워크 압축을 해제 하지 못했습니다 '\*'from'\*'. Zip' 네이티브' 명령에서 자세한 정보는 빌드 로그를 검토 하십시오.

바인딩 라이브러리에서 지정 된 네이티브 프레임 워크의 압축을 해제할 수 없습니다.

Zip' 네이티브' 명령에서이 오류에 대 한 자세한 내용은 bulid 로그를 검토 하십시오.

### <a name="a-namemt1304mt1304-the-embedded-framework--in--is-invalid-it-does-not-contain-an-infoplist"></a><a name="MT1304"/>MT1304: 포함 된 프레임 워크 ' *'에서 * 잘못 되었습니다:는 Info.plist 포함 되어 있지 않습니다.

지정 된 포함 된 프레임 워크에는 Info.plist 없으며 올바른 프레임 워크 하지 않습니다.

프레임 워크 올바른지 확인 하십시오.

### <a name="a-namemt1305mt1305-the-binding-library--contains-a-user-framework--but-embedded-user-frameworks-require-ios-80-the-current-deployment-target-is--please-set-the-deployment-target-in-the-infoplist-file-to-at-least-80"></a><a name="MT1305"/>MT1305: 바인딩 라이브러리 '\*' 사용자 프레임 워크를 포함 (\*), iOS 8.0이 필요한 정도 포함 된 사용자 프레임 워크 (현재 배포 대상이 *). 8.0 이상 Info.plist 파일에서 배포 대상을 설정 하십시오.

지정 된 바인딩 라이브러리는 포함 된 프레임 워크에 포함 되어 있지만 Xamarin.iOS iOS 8.0 이상에 포함 된 프레임 워크를 지원 합니다.

하십시오이 오류를 해결 하기 위해 8.0 이상 Info.plist 파일에서 배포 대상을 설정 하거나 포함 된 프레임 워크를 사용 하지 마십시오.

### <a name="mt14xx-crash-reports"></a>MT14xx: 충돌 보고서

<!--
  MT14xx    CrashReports.cs
  -->

### <a name="a-namemt1400mt1400-could-not-open-crash-report-service-afcconnectionopen-returned-"></a><a name="MT1400"/>MT1400: 충돌 보고서 서비스를 열 수 없습니다: 반환 된 AFCConnectionOpen *

장치에서 충돌 보고서에 액세스 하려고 하는 오류가 발생 했습니다.

이 문제를 해결 하는 사항은 다음과 같습니다.

* 장치에서 응용 프로그램을 삭제 하 고 다시 시도 하십시오.
* 장치를 분리 하 고 다시 연결 합니다.
* 장치를 다시 부팅 합니다.
* Mac를 다시 부팅
* (이렇게 하면 모든 충돌 보고서에서에서 제거 장치) iTunes와 장치를 동기화 합니다.

### <a name="a-namemt1401mt1401-could-not-close-crash-report-service-afcconnectionclose-returned-"></a><a name="MT1401"/>MT1401: 충돌 보고서 서비스를 닫을 수 없습니다: 반환 된 AFCConnectionClose *

장치에서 충돌 보고서에 액세스 하려고 하는 오류가 발생 했습니다.

이 문제를 해결 하는 사항은 다음과 같습니다.

* 장치에서 응용 프로그램을 삭제 하 고 다시 시도 하십시오.
* 장치를 분리 하 고 다시 연결 합니다.
* 장치를 다시 부팅 합니다.
* Mac를 다시 부팅
* (이렇게 하면 모든 충돌 보고서에서에서 제거 장치) iTunes와 장치를 동기화 합니다.

### <a name="a-namemt1402mt1402-could-not-read-file-info-for--afcfileinfoopen-returned-"></a><a name="MT1402"/>MT1402:에 대 한 파일 정보를 읽지 못했습니다 *: AFCFileInfoOpen 반환 *

장치에서 충돌 보고서에 액세스 하려고 하는 오류가 발생 했습니다.

이 문제를 해결 하는 사항은 다음과 같습니다.

* 장치에서 응용 프로그램을 삭제 하 고 다시 시도 하십시오.
* 장치를 분리 하 고 다시 연결 합니다.
* 장치를 다시 부팅 합니다.
* Mac를 다시 부팅
* (이렇게 하면 모든 충돌 보고서에서에서 제거 장치) iTunes와 장치를 동기화 합니다.

### <a name="a-namemt1403mt1403-could-not-read-crash-report-afcdirectoryopen--returned-"></a><a name="MT1403"/>MT1403: 충돌 보고를 읽을 수 없습니다: AFCDirectoryOpen (*) 반환 했습니다: *

장치에서 충돌 보고서에 액세스 하려고 하는 오류가 발생 했습니다.

이 문제를 해결 하는 사항은 다음과 같습니다.

* 장치에서 응용 프로그램을 삭제 하 고 다시 시도 하십시오.
* 장치를 분리 하 고 다시 연결 합니다.
* 장치를 다시 부팅 합니다.
* Mac를 다시 부팅
* (이렇게 하면 모든 충돌 보고서에서에서 제거 장치) iTunes와 장치를 동기화 합니다.

### <a name="a-namemt1404mt1404-could-not-read-crash-report-afcfilerefopen--returned-"></a><a name="MT1404"/>MT1404: 충돌 보고를 읽을 수 없습니다: AFCFileRefOpen (*) 반환 했습니다: *

장치에서 충돌 보고서에 액세스 하려고 하는 오류가 발생 했습니다.

이 문제를 해결 하는 사항은 다음과 같습니다.

* 장치에서 응용 프로그램을 삭제 하 고 다시 시도 하십시오.
* 장치를 분리 하 고 다시 연결 합니다.
* 장치를 다시 부팅 합니다.
* Mac를 다시 부팅
* (이렇게 하면 모든 충돌 보고서에서에서 제거 장치) iTunes와 장치를 동기화 합니다.

### <a name="a-namemt1405mt1405-could-not-read-crash-report-afcfilerefread--returned-"></a><a name="MT1405"/>MT1405: 충돌 보고를 읽을 수 없습니다: AFCFileRefRead (*) 반환 했습니다: *

장치에서 충돌 보고서에 액세스 하려고 하는 오류가 발생 했습니다.

이 문제를 해결 하는 사항은 다음과 같습니다.

* 장치에서 응용 프로그램을 삭제 하 고 다시 시도 하십시오.
* 장치를 분리 하 고 다시 연결 합니다.
* 장치를 다시 부팅 합니다.
* Mac를 다시 부팅
* (이렇게 하면 모든 충돌 보고서에서에서 제거 장치) iTunes와 장치를 동기화 합니다.

### <a name="a-namemt1406mt1406-could-not-list-crash-reports-afcdirectoryopen--returned-"></a><a name="MT1406"/>MT1406: 충돌 보고서를 나열할 수 없습니다: AFCDirectoryOpen (*) 반환 했습니다: *

장치에서 충돌 보고서에 액세스 하려고 하는 오류가 발생 했습니다.

이 문제를 해결 하는 사항은 다음과 같습니다.

* 장치에서 응용 프로그램을 삭제 하 고 다시 시도 하십시오.
* 장치를 분리 하 고 다시 연결 합니다.
* 장치를 다시 부팅 합니다.
* Mac를 다시 부팅
* (이렇게 하면 모든 충돌 보고서에서에서 제거 장치) iTunes와 장치를 동기화 합니다.

<!--- 1407 used by mmp -->

### <a name="mt16xx-macho"></a>MT16xx: MachO

<!--
  MT16xx    MachO.cs
  -->

### <a name="a-namemt1600mt1600-not-a-mach-o-dynamic-library-unknown-header-0x-"></a><a name="MT1600"/>MT1600: 하지 일치-O 동적 라이브러리 (알 수 없는 헤더 ' 0 x *'): * 합니다.

문제의 동적 라이브러리를 처리 하는 동안 오류가 발생 했습니다.

동적 라이브러리 유효한 일치-O 동적 라이브러리 인지 확인 하십시오.

사용 하 여 라이브러리의 형식을 확인할 수는 `file` 터미널 명령을:

    file -arch all -l /path/to/library.dylib

### <a name="a-namemt1601mt1601-not-a-static-library-unknown-header--"></a><a name="MT1601"/>MT1601: 하지 정적 라이브러리 (알 수 없는 헤더 ' *'): * 합니다.

문제의 정적 라이브러리를 처리 하는 동안 오류가 발생 했습니다.

정적 라이브러리의 유효한 일치-O 정적 라이브러리 인지 확인 하십시오.

사용 하 여 라이브러리의 형식을 확인할 수는 `file` 터미널 명령을:

    file -arch all -l /path/to/library.a

### <a name="a-namemt1602mt1602-not-a-mach-o-dynamic-library-unknown-header-0x-"></a><a name="MT1602"/>MT1602: 하지 일치-O 동적 라이브러리 (알 수 없는 헤더 ' 0 x *'): * 합니다.

문제의 동적 라이브러리를 처리 하는 동안 오류가 발생 했습니다.

동적 라이브러리 유효한 일치-O 동적 라이브러리 인지 확인 하십시오.

사용 하 여 라이브러리의 형식을 확인할 수는 `file` 터미널 명령을:

    file -arch all -l /path/to/library.dylib

### <a name="a-namemt1603mt1603-unknown-format-for-fat-entry-at-position--in-"></a><a name="MT1603"/>MT1603: 위치에 fat 항목에 대 한 알 수 없는 형식 *에서 *.

문제의 fat 보관을 처리 하는 동안 오류가 발생 했습니다.

Fat 보관 올바른지 확인 하십시오.

Fat 보관 파일의 형식을 사용 하 여 확인할 수 있습니다는 `file` 터미널 명령을:

    file -arch all -l /path/to/file

### <a name="a-namemt1604mt1604-file-of-type--is-not-a-macho-file-"></a><a name="MT1604"/>MT1604: 형식의 파일 * 멋진 (*) 파일이 아닙니다.

멋진 해당 파일에는 처리 하는 동안 오류가 발생 했습니다.

파일이 유효한 일치-O 동적 라이브러리 인지 확인 하십시오.

사용 하 여 파일의 형식을 확인할 수는 `file` 터미널 명령을:

    file -arch all -l /path/to/file

## <a name="mt2xxx-linker-error-messages"></a>MT2xxx: 링커 오류 메시지

<!--
 MT2xxx Linker
  MT20xx Linker (general) errors
  -->

### <a name="a-namemt2001mt2001-could-not-link-assemblies"></a><a name="MT2001"/>어셈블리를 연결할 MT2001 수 없습니다.

이 오류 관리 되는 링커 예외가 예: 예기치 않은 오류가 발생 했음을 의미 하 고 완료 하거나 처리 중인 어셈블리를 저장할 수 없습니다. 정확한 오류에 대 한 자세한 내용은 일부가 될 빌드 로그의 예:

``` 
error MT2001: Could not link assemblies.
    Method: `System.Void Todo.TodoListPageCS/<<-ctor>b__1_0>d::SetStateMachine(System.Runtime.CompilerServices.IAsyncStateMachine)`
    Assembly: `QuickTodo, Version=1.0.6297.28241, Culture=neutral, PublicKeyToken=null`
Reason: Value cannot be null.
Parameter name: instruction
```

이러한 문제에 대 한 버그 보고 하는 것이 유용 합니다. 대부분의 경우에서 적절 한 수정 프로그램이 게시 될 때까지 해결 방법을 제공할 수 있습니다. 위의 정보는 문제를 해결 하려면 테스트 사례 및/또는 어셈블리 binairy) (함께 매우 중요 합니다.


### <a name="a-namemt2002mt2002-can-not-resolve-reference-"></a><a name="MT2002"/>참조를 확인할 MT2002 수: *



### <a name="a-namemt2003mt2003-option--will-be-ignored-since-linking-is-disabled"></a><a name="MT2003"/>MT2003 옵션 ' *' 링크는 사용 되지 무시 됩니다



### <a name="a-namemt2004mt2004-extra-linker-definitions-file--could-not-be-located"></a><a name="MT2004"/>추가 MT2004 링커 정의 파일 ' *'를 찾을 수 없습니다.



### <a name="a-namemt2005mt2005-definitions-from--could-not-be-parsed"></a><a name="MT2005"/>MT2005 정의에서 ' *'을 분석할 수 없습니다.



### <a name="a-namemt2006mt2006-can-not-load-mscorlibdll-from--please-reinstall-xamarinios"></a><a name="MT2006"/>MT2006:에서 mscorlib.dll을 로드할 수 없습니다: * 합니다. Xamarin.iOS 다시 설치 하십시오.

일반적으로 이것은 Xamarin.iOS 설치에 문제가 있다는 것을 나타냅니다. Xamarin.iOS 다시 설치 해 보십시오.

<!--- 2007 used by mmp -->
<!--- 2009 used by mmp -->

### <a name="a-namemt2010mt2010-unknown-httpmessagehandler--valid-values-are-httpclienthandler-default-cfnetworkhandler-or-nsurlsessionhandler"></a><a name="MT2010"/>MT2010: 알 수 없는 HttpMessageHandler `*`합니다. 유효한 값은 HttpClientHandler (기본값), CFNetworkHandler 또는 NSUrlSessionHandler

### <a name="a-namemt2011mt2011-unknown-tlsprovider---valid-values-are-default-or-appletls"></a><a name="MT2011"/>MT2011: 알 수 없는 TlsProvider `*`합니다.  유효한 값은 기본값 appletls입니다.

에 제공 된 값 `tls-provider=` 유효한 TLS (전송 계층 보안) 공급자가 아닙니다.

`default` 및 `appletls` 만 유효한 값와 모두 SSL/TLS 네이티브 Apple TLS API를 사용 하 여 지원을 제공할 수 있는 동일한 옵션을 나타내는 됩니다.

<!--- 2012 used by mmp -->
<!--- 2013 used by mmp -->
<!--- 2014 used by mmp -->

### <a name="a-namemt2015mt2015-invalid-httpmessagehandler--for-watchos-the-only-valid-value-is-nsurlsessionhandler"></a><a name="MT2015"/>MT2015: 잘못 된 HttpMessageHandler `*` watchOS에 대 한 합니다. 유일한 유효 값은 NSUrlSessionHandler 합니다.

프로젝트 파일에 잘못 된 HttpMessageHandler 지정 하기 때문에 발생 하는 경고입니다.

프로젝트 파일에 잘못 된 값을 기본적으로 생성 하는 이전 버전의이 미리 보기 도구.

이 경고를 해결 하려면 텍스트 편집기에서 프로젝트 파일을 열고 모든 HttpMessageHandler 노드는 XML에서 제거 합니다.

### <a name="a-namemt2016mt2016-invalid-tlsprovider-legacy-option-the-only-valid-value-appletls-will-be-used"></a><a name="MT2016"/>MT2016: 잘못 된 TlsProvider `legacy` 옵션입니다. 유일한 유효 값 `appletls` 사용 됩니다.

`legacy` 완전히 관리 되는 SSLv3 하 던 공급자 / TLSv1 유일한 공급자 Xamarin.iOS에 더 이상 제공 되지 않습니다. 이 이전 공급자를 사용 하 던 및 최신 형식으로 제품을 제작 하는 프로젝트 `appletls` 하나입니다.

이 경고를 해결 하려면 프로젝트 파일에서 텍스트 편집기를 열고 모두 제거 ' MtouchTlsProvider ' XML에서 노드.

### <a name="a-namemt2017mt2017-could-not-process-xml-description"></a><a name="MT2017"/>MT2017: XML 설명을 처리 하지 못했습니다.

에 오류가 발생 하는이 의미는 [사용자 지정 XML 링커 구성 파일](https://developer.xamarin.com/guides/cross-platform/advanced/custom_linking/) 제공 된 프로그램 파일을 참조 하십시오.

### <a name="a-namemt2018mt2018-the-assembly--is-referenced-from-two-different-locations--and-"></a><a name="MT2018"/>MT2018: 어셈블리 '\*' 서로 다른 두 위치에서 참조: '\*' 및 ' *'입니다.

오류 메시지에 언급 된 어셈블리는 여러 위치에서 로드 됩니다. 항상 동일한 버전의 어셈블리를 사용 하 고 있는지 확인 합니다.

### <a name="a-namemt2019mt2019-can-not-load-the-root-assembly-"></a><a name="MT2019"/>MT2019: 루트 어셈블리를 로드할 수 없습니다 ' *'

루트 어셈블리를 로드할 수 없습니다. 오류 메시지에 대 한 경로를 기존 파일을 참조 하 고 올바른.NET assembly 인지 확인 하십시오.

### <a name="a-namemt202xmt202x-binding-optimizer-failed-processing-"></a><a name="MT202x"/>MT202x: 바인딩 최적화 프로그램에서 처리 하지 못했습니다. `...`합니다.

바인딩 코드 생성 최적화 하는 동안 예기치 않은 문제가 발생 했습니다. 오류 메시지에는 문제를 발생 시킨 요소 라고 합니다. 명명 된 어셈블리 (또는 형식 또는 메서드 이름이 포함 된)이이 문제를 해결 하려면에 제공 해야 합니다는 [버그 보고서](http://bugzilla.xamarin.com) 사용의 자세한 정도를 최종 빌드 로그와 함께 (즉, `-v -v -v -v` 에 **추가 mtouch 인수**).

마지막 자릿수가 양수인 `x` 됩니다.
* `0` 어셈블리 이름;에 대 한
* `1` 형식 이름;에 대해
* `3` 메서드 이름입니다.

### <a name="a-namemt2030mt2030-remove-user-resources-failed-processing-"></a><a name="MT2030"/>MT2030: 사용자 리소스를 제거 하지 못했습니다 처리 `...`합니다.

사용자 리소스를 제거 하려고 할 때 예기치 않은 문제가 발생 했습니다. 오류 메시지에 문제가 발생 하는 어셈블리의 이름은입니다. 어셈블리가이 문제를 해결 하려면에 제공 해야 합니다는 [버그 보고서](http://bugzilla.xamarin.com) 사용의 자세한 정도를 최종 빌드 로그와 함께 (즉, `-v -v -v -v` 에 **추가 mtouch 인수**).

사용자 리소스는 응용 프로그램 번들 작성 빌드 시 추출 해야 하는 (리소스로) 어셈블리 내에 포함 된 파일입니다. 여기에는 다음이 포함됩니다.

* `__monotouch_content_*` 및 `__monotouch_pages_*` 리소스만 및
* 바인딩 어셈블리; 내에 포함 된 네이티브 라이브러리

### <a name="a-namemt2040mt2040-default-httpmessagehandler-setter-failed-processing-"></a><a name="MT2040"/>MT2040: 기본 HttpMessageHandler setter 실패 처리 `...`합니다.

기본 설정 하려고 할 때 예기치 않은 문제가 발생 한 `HttpMessageHandler` 응용 프로그램에 대 한 합니다. 보관는 [버그 보고서](http://bugzilla.xamarin.com) 사용의 자세한 정도를 최종 빌드 로그와 함께 (즉, `-v -v -v -v` 에 **추가 mtouch 인수**).

### <a name="a-namemt2050mt2050-code-remover-failed-processing-"></a><a name="MT2050"/>MT2050: 코드 remover가 처리 하지 못했습니다. `...`합니다.

응용 프로그램으로 전달 BCL에서 코드를 제거 하려고 할 때 예기치 않은 문제가 발생 했습니다. 보관는 [버그 보고서](http://bugzilla.xamarin.com) 사용의 자세한 정도를 최종 빌드 로그와 함께 (즉, `-v -v -v -v` 에 **추가 mtouch 인수**).

### <a name="a-namemt2060mt2060-sealer-failed-processing-"></a><a name="MT2060"/>MT2060: Sealer 처리 하지 못했습니다. `...`합니다.

형식 또는 메서드의 (최종) 봉인 하는 동안 또는 몇 가지 방법을 devirtualizing 때 예기치 않은 문제가 발생 했습니다. 오류 메시지에 문제가 발생 하는 어셈블리의 이름은입니다. 어셈블리가이 문제를 해결 하려면에 제공 해야 합니다는 [버그 보고서](http://bugzilla.xamarin.com) 사용의 자세한 정도를 최종 빌드 로그와 함께 (즉, `-v -v -v -v` 에 **추가 mtouch 인수**).

### <a name="a-namemt2070mt2070-metadata-reducer-failed-processing-"></a><a name="MT2070"/>MT2070: 리 듀 서 메타 데이터를 처리 하지 `...`합니다.

응용 프로그램에서 메타 데이터를 줄이는 하려고 할 때 예기치 않은 문제가 발생 했습니다. 오류 메시지에 문제가 발생 하는 어셈블리의 이름은입니다. 어셈블리가이 문제를 해결 하려면에 제공 해야 합니다는 [버그 보고서](http://bugzilla.xamarin.com) 사용의 자세한 정도를 최종 빌드 로그와 함께 (즉, `-v -v -v -v` 에 **추가 mtouch 인수**).

### <a name="a-namemt2080mt2080-marknsobjects-failed-processing-"></a><a name="MT2080"/>MT2080: MarkNSObjects 처리 하지 못했습니다. `...`합니다.

표시 하려고 할 때 예기치 않은 문제가 발생 한 `NSObject` 응용 프로그램에서 하위 클래스입니다. 오류 메시지에 문제가 발생 하는 어셈블리의 이름은입니다. 어셈블리가이 문제를 해결 하려면에 제공 해야 합니다는 [버그 보고서](http://bugzilla.xamarin.com) 사용의 자세한 정도를 최종 빌드 로그와 함께 (즉, `-v -v -v -v` 에 **추가 mtouch 인수**).

<!-- MT21xx: more linker errors -->

<!--- 2100 used by mmp -->

### <a name="a-namemt2101mt2101-cant-resolve-the-reference--referenced-from-the-method--in-"></a><a name="MT2101"/>MT2101: 참조를 확인할 수 없습니다 '\*', 메서드에서 참조 된'\*'에서 ' *'입니다.

잘못 된 어셈블리 참조는 오류 메시지에 언급 된 메서드를 처리할 때 발생 했습니다.

오류 메시지에 문제가 발생 하는 어셈블리의 이름은입니다. 어셈블리가이 문제를 해결 하려면에 제공 해야 합니다는 [버그 보고서](https://bugzilla.xamarin.com) 사용의 자세한 정도를 최종 빌드 로그와 함께 (즉, `-v -v -v -v` 에 **추가 mtouch 인수**).

### <a name="a-namemt2102mt2102-error-processing-the-method--in-the-assembly--"></a><a name="MT2102"/>MT2102: 메서드를 처리 하는 동안 오류가 '\*어셈블리' '에\*': *

오류 메시지에 언급 된 메서드를 표시 하려고 할 때 예기치 않은 문제가 발생 했습니다.

오류 메시지에 문제가 발생 하는 어셈블리의 이름은입니다. 어셈블리가이 문제를 해결 하려면에 제공 해야 합니다는 [버그 보고서](https://bugzilla.xamarin.com) 사용의 자세한 정도를 최종 빌드 로그와 함께 (즉, `-v -v -v -v` 에 **추가 mtouch 인수**).

## <a name="mt3xxx-aot-error-messages"></a>MT3xxx: AOT 오류 메시지

<!--
 MT3xxx AOT
  MT30xx AOT (general) errors
  -->

### <a name="a-namemt3001mt3001-could-not-aot-the-assembly-"></a><a name="MT3001"/>MT3001 수 없습니다. 어셈블리 AOT 하지 ' *'

일반적으로 이것 AOT 컴파일러의 버그를 나타냅니다. 버그를 제출 하세요 [http://bugzilla.xamarin.com](https://bugzilla.xamarin.com/enter_bug.cgi?product=iOS) 오류를 재현 하는 데 사용할 수 있는 프로젝트입니다.

경우에 따라 iOS 프로젝트의 빌드 옵션에서에서 증분 빌드를 사용 하지 않도록 설정 하 여이 해결할 수 있습니다 (되었지만 여전히 버그를 따라서 그래도 보고 하십시오).

### <a name="a-namemt3002mt3002-aot-restriction-method--must-be-static-since-it-is-decorated-with-monopinvokecallback-see-httpsdeveloperxamarincomguidesiosadvancedtopicslimitationsreversecallbackshttpsdeveloperxamarincomguidesiosadvancedtopicslimitationsreversecallbacks"></a><a name="MT3002"/>MT3002 AOT 제한: 메서드 ' *' [MonoPInvokeCallback]으로 데코레이팅 되었으므로 하므로 정적 이어야 합니다. See [https://developer.xamarin.com/guides/ios/advanced_topics/limitations/#Reverse_Callbacks](https://developer.xamarin.com/guides/ios/advanced_topics/limitations/#Reverse_Callbacks)

이 오류 메시지가 AOT 컴파일러에서 제공 됩니다.



### <a name="a-namemt3003mt3003-conflicting---debug-and---llvm-options-soft-debugging-is-disabled"></a><a name="MT3003"/>MT3003 충돌-디버그 및-원하는 llvm 옵션입니다. 소프트 디버깅 사용할 수 없습니다.

원하는 LLVM가 설정 된 경우 디버깅이 지원 되지 않습니다. 응용 프로그램을 디버깅 해야 할 경우 먼저 원하는 LLVM를 해제 합니다.

### <a name="a-namemt3004mt3004-could-not-aot-the-assembly--because-it-doesnt-exist"></a><a name="MT3004"/>MT3004 수 AOT 어셈블리 하지 ' *' 존재 하지 않습니다.



### <a name="a-namemt3005mt3005-the-dependency--of-the-assembly--was-not-found-please-review-the-projects-references"></a><a name="MT3005"/>MT3005 종속성 '\*어셈블리' '의\*' 찾을 수 없습니다. 프로젝트의 참조를 검토 하십시오.

이 문제는 일반적으로 어셈블리 플랫폼 어셈블리 (일반적으로.NET 4 버전의 mscorlib.dll)의 다른 버전을 참조할 때 발생 합니다.

이 지원 되지 않습니다 및 빌드 없거나 제대로 실행 (어셈블리 API Xamarin.iOS 버전에 없는 mscorlib.dll의.NET 4 버전에서 사용할 수 있습니다).

### <a name="a-namemt3006mt3006-could-not-compute-a-complete-dependency-map-for-the-project-this-will-result-in-slower-build-times-because-xamarinios-cant-properly-detect-what-needs-to-be-rebuilt-and-what-does-not-need-to-be-rebuilt-please-review-previous-warnings-for-more-details"></a><a name="MT3006"/>프로젝트에 대 한 전체 종속성 맵을 계산 하지 MT3006 수 없습니다. 이렇게 하면 빌드 시간이 느려집니다 이므로 다시 작성 해야 할 작업 (및 다시 작성 하지 않아도 어떤) Xamarin.iOS 제대로 검색할 수 없습니다. 자세한 내용은 이전 경고를 검토 하십시오.

 빌드 또는 제대로 실행 (어셈블리 API Xamarin.iOS 버전에 없는 mscorlib.dll의.NET 4 버전에서 사용할 수 있습니다).

### <a name="a-namemt3007mt3007-debug-info-files-mdb-will-not-be-loaded-when-llvm-is-enabled"></a><a name="MT3007"/>MT3007: 원하는 llvm가 설정 된 경우 디버그 정보 파일 (*.mdb) 로드 되지 않습니다.

### <a name="a-namemt3008mt3008-bitcode-support-requires-the-use-of-the-llvm-aot-backend---llvm"></a><a name="MT3008"/>MT3008: Bitcode 지원을 원하는 LLVM AOT 백 엔드를 사용 해야 합니다 (-원하는 llvm)

Bitcode 지원 하려면 원하는 LLVM AOT 백 엔드의 사용 하 여 (-원하는 llvm).

Bitcode 지원 사용 안 함 또는 원하는 LLVM를 사용 하도록 설정 합니다.

<!--- 3009 used by mmp -->
<!--- 3010 used by mmp -->

## <a name="mt4xxx-code-generation-error-messages"></a>MT4xxx: 코드 생성 오류 메시지

### <a name="mt40xx-main"></a>MT40xx: 주

<!--
 MT4xxx code generation
  MT40xx main.m
  -->

### <a name="a-namemt4001mt4001-the-main-template-could-not-be-expanded-to-"></a><a name="MT4001"/>MT4001 기본 서식 파일을 확장할 수 없습니다 `*`합니다.

Main.m 생성 하는 오류가 발생 했습니다. 버그를 제출 하세요 [http://bugzilla.xamarin.com](https://bugzilla.xamarin.com/enter_bug.cgi?product=iOS)합니다.

### <a name="a-namemt4002mt4002-failed-to-compile-the-generated-code-for-pinvoke-methods-please-file-a-bug-report-at-httpbugzillaxamarincom"></a><a name="MT4002"/>MT4002 P/Invoke 메서드에 대 한 생성된 된 코드를 컴파일하지 못했습니다. Http://bugzilla.xamarin.com에 버그 보고서를 제출 하세요

P/Invoke 메서드에 대 한 생성된 된 코드를 컴파일하지 못했습니다. 에 버그 보고서를 제출 하세요 [http://bugzilla.xamarin.com](https://bugzilla.xamarin.com/enter_bug.cgi?product=iOS)합니다.

### <a name="mt41xx-registrar"></a>MT41xx: 등록자

<!--
  MT41xx registrar.m
  -->

### <a name="a-namemt4101mt4101-the-registrar-cannot-build-a-signature-for-type-"></a><a name="MT4101"/>MT4101 등록자 형식에 대 한 시그니처를 작성할 수 없습니다 `*`합니다.

런타임에 없습니다. 목표를에서 마샬링하는 방법을 모릅니다 내보낸된 API에는 유형은 찾을 수

Xamarin.iOS 문제의 종류를 지원 해야 생각 되는 경우에 향상 된 기능 요청을 제출 하세요 [http://bugzilla.xamarin.com](http://bugzilla.xamarin.com)합니다.

### <a name="a-namemt4102mt4102-the-registrar-found-an-invalid-type--in-signature-for-method--use--instead"></a><a name="MT4102"/>MT4102 등록자 잘못 된 형식이 발견 `*` 메서드 서명에서 `*`합니다. 대신 `*`를 사용하세요.

현재만 이런 상황이 발생 한 형식과: System.DateTime 합니다. Objective C 해당 (NSDate)를 대신 사용 합니다.

### <a name="a-namemt4103mt4103-the-registrar-found-an-invalid-type--in-signature-for-method--the-type-implements-inativeobject-but-does-not-have-a-constructor-that-takes-two-intptr-bool-arguments"></a><a name="MT4103"/>MT4103 등록자 잘못 된 형식이 발견 `*` 메서드 서명에서 `*`: 유형을 INativeObject을를 구현 하지만 두 개를 사용 하는 생성자가 없습니다 (IntPtr, bool) 인수

이 문제가 발생 등록자에서 언급 한 특성을 갖는 시그니처의 형식 발생 하는 경우. 등록자는 형식의 새 인스턴스를 만들 해야 할 수 있고이 경우 (IntPtr, bool) 사용 하는 생성자를 필요 서명-(IntPtr) 첫 번째 인수는 호출자가 네이티브 소유권을 전달 하는 경우 두 번째 관리 되는 핸들을 지정 (이 값은 개체에서 호출 보존 false) 하는 경우를 처리 합니다.

### <a name="a-namemt4104mt4104-the-registrar-cannot-marshal-the-return-value-for-type--in-signature-for-method-"></a><a name="MT4104"/>MT4104 등록자 형식에 대 한 반환 값을 마샬링할 수 `*` 메서드 서명에서 `*`합니다.

런타임에 없습니다. 목표를에서 마샬링하는 방법을 모릅니다 내보낸된 API에는 유형은 찾을 수

Xamarin.iOS 문제의 종류를 지원 해야 생각 되는 경우에 향상 된 기능 요청을 제출 하세요 [http://bugzilla.xamarin.com](http://bugzilla.xamarin.com)합니다.

### <a name="a-namemt4105mt4105-the-registrar-cannot-marshal-the-parameter-of-type--in-signature-for-method-"></a><a name="MT4105"/>MT4105 등록자 형식의 매개 변수를 마샬링할 수 `*` 메서드 서명에서 `*`합니다.

Xamarin.iOS 문제의 종류를 지원 해야 생각 되는 경우에 향상 된 기능 요청을 제출 하세요 [http://bugzilla.xamarin.com](http://bugzilla.xamarin.com)합니다.

### <a name="a-namemt4106mt4106-the-registrar-cannot-marshal-the-return-value-for-structure--in-signature-for-method-"></a><a name="MT4106"/>MT4106 등록자 구조에 대 한 반환 값을 마샬링할 수 `*` 메서드 서명에서 `*`합니다.

런타임에 없습니다. 목표를에서 마샬링하는 방법을 모릅니다 내보낸된 API에는 유형은 찾을 수

Xamarin.iOS 문제의 종류를 지원 해야 생각 되는 경우에 향상 된 기능 요청을 제출 하세요 [http://bugzilla.xamarin.com](http://bugzilla.xamarin.com)합니다.

### <a name="a-namemt4107mt4107-the-registrar-cannot-marshal-the-parameter-of-type--in-signature-for-method-"></a><a name="MT4107"/>MT4107 등록자 형식의 매개 변수를 마샬링할 수 `*` 메서드 서명에서 `+`합니다.

런타임에 없습니다. 목표를에서 마샬링하는 방법을 모릅니다 내보낸된 API에는 유형은 찾을 수

Xamarin.iOS 문제의 종류를 지원 해야 생각 되는 경우에 향상 된 기능 요청을 제출 하세요 [http://bugzilla.xamarin.com](http://bugzilla.xamarin.com)합니다.

### <a name="a-namemt4108mt4108-the-registrar-cannot-get-the-objectivec-type-for-managed-type-"></a><a name="MT4108"/>MT4108 등록자에는 관리 되는 형식에 대 한 ObjectiveC 형식을 가져올 수 없습니다 `*`합니다.

런타임에 없습니다. 목표를에서 마샬링하는 방법을 모릅니다 내보낸된 API에는 유형은 찾을 수

Xamarin.iOS 문제의 종류를 지원 해야 생각 되는 경우에 향상 된 기능 요청을 제출 하세요 [http://bugzilla.xamarin.com](http://bugzilla.xamarin.com)합니다.

### <a name="a-namemt4109mt4109-failed-to-compile-the-generated-registrar-code-please-file-a-bug-report-at-httpbugzillaxamarincom"></a><a name="MT4109"/>MT4109 등록자 생성 된 코드를 컴파일하지 못했습니다. Http://bugzilla.xamarin.com에 버그 보고서를 제출 하세요

등록 기관에 대 한 생성된 된 코드를 컴파일하지 못했습니다. 빌드 로그 코드 컴파일 없는 이유를 설명 하는 기본 컴파일러의 출력에 포함 됩니다.

이 값은 항상 Xamarin.iOS;의 버그 에 버그 보고서를 제출 하세요 [http://bugzilla.xamarin.com](http://bugzilla.xamarin.com) 프로젝트 또는 테스트 사례를 사용 합니다.

### <a name="a-namemt4110mt4110-the-registrar-cannot-marshal-the-out-parameter-of-type--in-signature-for-method-"></a><a name="MT4110"/>MT4110 등록자 형식의 out 매개 변수를 마샬링할 수 `*` 메서드 서명에서 `*`합니다.



### <a name="a-namemt4111mt4111-the-registrar-cannot-build-a-signature-for-type--in-method-"></a><a name="MT4111"/>MT4111 등록자 형식에 대 한 시그니처를 작성할 수 없습니다 `*` 메서드에서 `*`합니다.



### <a name="a-namemt4112mt4112-the-registrar-found-an-invalid-type--registering-generic-types-with-objective-c-is-not-supported-and-may-lead-to-random-behavior-andor-crashes-for-backwards-compatibility-with-older-versions-of-xamarinios-it-is-possible-to-ignore-this-error-by-passing---unsupported--enable-generics-in-registrar-as-an-additional-mtouch-argument-in-the-projects-ios-build-options-page-see-developerxamarincomguidesiosadvancedtopicsregistrarhttpsdeveloperxamarincomguidesiosadvancedtopicsregistrar-for-more-information"></a><a name="MT4112"/>MT4112 등록자 잘못 된 형식이 발견 `*`합니다. Objective C 제네릭 형식을 등록 지원 되지 않습니다 및 임의 동작 및/또는 충돌이 발생할 수 있습니다 (에 대 한 이전 버전과 Xamarin.iOS의 이전 버전과 호환성 수 있기를 전달 하 여이 오류를 무시 하려면 `--unsupported--enable-generics-in-registrar` 추가 mtouch로 프로젝트의 iOS 빌드 옵션 페이지에 대 한 인수입니다. 참조 [developer.xamarin.com/guides/ios/advanced_topics/registrar](https://developer.xamarin.com/guides/ios/advanced_topics/registrar) 자세한 정보에 대 한).



### <a name="a-namemt4113mt4113-the-registrar-found-a-generic-method--exporting-generic-methods-is-not-supported-and-will-lead-to-random-behavior-andor-crashes"></a><a name="MT4113"/>MT4113 등록자 제네릭 메서드를 찾을 수: '\*.\*'. 제네릭 메서드 내보내기은 지원 되지 않으며 임의 동작 및/또는 크래시를 일으킵니다.



### <a name="a-namemt4114mt4114-unexpected-error-in-the-registrar-for-the-method----please-file-a-bug-report-at-httpbugzillaxamarincom"></a><a name="MT4114"/>메서드에 대 한 등록자에 MT4114 예기치 않은 오류가 '\*.\*'-http://bugzilla.xamarin.com에 버그 보고서를 제출 하세요



### <a name="a-namemt4116mt4116-could-not-register-the-assembly--"></a><a name="MT4116"/>어셈블리를 등록 하지 MT4116 못했습니다 ' *': *



### <a name="a-namemt4117mt4117-the-registrar-found-a-signature-mismatch-in-the-method----the-selector-indicates-the-method-takes--parameters-while-the-managed-method-has--parameters"></a><a name="MT4117"/>MT4117 등록자 서명 불일치 메서드에서 발견 '*.*'-선택기 나타냅니다 메서드를 사용 하며 * 매개 변수를 관리 되는 메서드에 동안 * 매개 변수입니다.



### <a name="a-namemt4118mt4118-cannot-register-two-managed-types--and--with-the-same-native-name-"></a><a name="MT4118"/>두 개의 관리 되는 형식 등록 MT4118 수 없습니다 ('\*'및'\*') 같은 네이티브 이름의 ('* ').



### <a name="a-namemt4119mt4119-could-not-register-the-selector--of-the-member--because-the-selector-is-already-registered-on-a-different-member"></a><a name="MT4119"/>MT4119 등록할 수 없습니다. 선택기 '\*'member'의\*. *' 선택기 이미 다른 멤버에 등록 되어 있으므로 합니다.



### <a name="a-namemt4120mt4120-the-registrar-found-an-unknown-field-type--in-field--please-file-a-bug-report-at-httpbugzillaxamarincom"></a><a name="MT4120"/>MT4120 등록자 찾을 수 없는 필드 형식 '\*'field' in에서\*. *'입니다. Http://bugzilla.xamarin.com에 버그 보고서를 제출 하세요

이 오류는 Xamarin.iOS의 버그를 나타냅니다. 에 버그 보고서를 제출 하세요 [http://bugzilla.xamarin.com](https://bugzilla.xamarin.com/enter_bug.cgi?product=iOS)합니다.

### <a name="a-namemt4121mt4121-cannot-use-gccg-to-compile-the-generated-code-from-the-static-registrar-when-using-the-accounts-framework-the-header-files-provided-by-apple-used-during-the-compilation-require-clang-either-use-clang---compilerclang-or-the-dynamic-registrar---registrardynamic"></a><a name="MT4121"/>MT4121 사용할 수 없는 GCC / G + + (컴파일 중에 사용할 Apple에서 제공한 헤더 파일에서는 Clang을 요구 하는 데 사용) 계정 프레임 워크를 사용 하는 경우 정적 등록 기관에서 생성된 된 코드를 컴파일할 수 있습니다. Clang을 사용 하거나 (-컴파일러: clang) 또는 동적 등록 기관 (-등록자: 동적).



### <a name="a-namemt4122mt4122-cannot-use-the-clang-compiler-provided-in-the--sdk-to-compile-the-generated-code-from-the-static-registrar-when-non-ascii-type-names--are-present-in-the-application-either-use-gccg---compilergccg-the-dynamic-registrar---registrardynamic-or-a-newer-sdk"></a><a name="MT4122"/>MT4122 사용할 수 없습니다에 제공 된 Clang 컴파일러는 *합니다.* ASCII가 아닌 경우 정적 등록 기관에서 생성된 된 코드를 컴파일하는 데 SDK 유형 이름 ('* ')이 응용 프로그램에 있습니다. GCC를 사용 하거나 / G + + (-컴파일러: gcc | g + +), 동적 등록 기관 (-등록자: 동적) 또는 최신 SDK입니다.



### <a name="a-namemt4123mt4123-the-type-of-the-variadic-parameter-in-the-variadic-function--must-be-systemintptr"></a><a name="MT4123"/>MT4123 variadic 함수에서 variadic 매개 변수 형식의 ' *' 하나 여야 합니다.



### <a name="a-namemt4124mt4124-invalid--found-on--please-file-a-bug-report-at-httpbugzillaxamarincom"></a><a name="MT4124"/>잘못 된 MT4124 *에 ' *'입니다. Http://bugzilla.xamarin.com에 버그 보고서를 제출 하세요

이 오류는 Xamarin.iOS의 버그를 나타냅니다. 에 버그 보고서를 제출 하세요 [http://bugzilla.xamarin.com](https://bugzilla.xamarin.com/enter_bug.cgi?product=iOS)합니다.

### <a name="a-namemt4125mt4125-the-registrar-found-an-invalid-type--in-signature-for-method--the-interface-must-have-a-protocol-attribute-specifying-its-wrapper-type"></a><a name="MT4125"/>MT4125 등록자 검색 된 잘못 된 형식은 '\*'메서드 시그니처의'\*': 인터페이스는 래퍼 형식을 지정 하는 프로토콜 특성을 포함 해야 합니다.



### <a name="a-namemt4126mt4126-cannot-register-two-managed-protocols--and--with-the-same-native-name-"></a><a name="MT4126"/>MT4126 등록할 수 없습니다 두 개의 관리 되는 프로토콜 ('\*'및'\*') 같은 네이티브 이름의 ('* ').



### <a name="a-namemt4127mt4127-cannot-register-more-than-one-interface-method-for-the-method--which-is-implementing-"></a><a name="MT4127"/>메서드에 대 한 인터페이스 메서드를 여러 개 등록 MT4127 수 없습니다. '\*' (은 구현 하는 '\*').



### <a name="a-namemt4128mt4128--the-registrar-found-an-invalid-generic-parameter-type--in-the-method--the-generic-parameter-must-have-an-nsobject-constraint"></a><a name="MT4128"/>MT4128 등록자 검색 된 잘못 된 제네릭 매개 변수 형식은 '\*'method' in에서\*'. 제네릭 매개 변수는 'NSObject' 제약 조건이 있어야 합니다.

### <a name="a-namemt4129mt4129--the-registrar-found-an-invalid-generic-return-type--in-the-method--the-generic-return-type-must-have-an-nsobject-constraint"></a><a name="MT4129"/>MT4129 등록자 발견 잘못 된 제네릭 반환 형식을 '\*'method' in에서\*'. 제네릭 반환 형식을 'NSObject' 제약 조건이 있어야 합니다.

### <a name="a-namemt4130mt4130--the-registrar-cannot-export-static-methods-in-generic-classes-"></a><a name="MT4130"/>MT4130 등록자 제네릭 클래스의 정적 메서드를 내보낼 수 없습니다 ('* ').

### <a name="a-namemt4131mt4131--the-registrar-cannot-export-static-properties-in-generic-classes-"></a><a name="MT4131"/>MT4131 등록자 제네릭 클래스의 정적 속성을 내보낼 수 없습니다 ('\*.\*').

### <a name="a-namemt4132mt4132--the-registrar-found-an-invalid-generic-return-type--in-the-property--the-return-type-must-have-an-nsobject-constraint"></a><a name="MT4132"/>MT4132 등록자 발견 잘못 된 제네릭 반환 형식을 '\*'property' in에서\*'. 반환 형식은 'NSObject' 제약 조건이 있어야 합니다.

### <a name="a-namemt4133mt4133--cannot-construct-an-instance-of-the-type--from-objective-c-because-the-type-is-generic-runtime-exception"></a><a name="MT4133"/>형식의 인스턴스를 생성할 MT4133 수 없습니다. ' *' Objective C에서 형식이 제네릭이므로 합니다. [런타임 예외가]

### <a name="a-namemt4134mt4134--your-application-is-using-the--framework-which-isnt-included-in-the-ios-sdk-youre-using-to-build-your-app-this-framework-was-introduced-in-ios--while-youre-building-with-the-ios--sdk-please-select-a-newer-sdk-in-your-apps-ios-build-options"></a><a name="MT4134"/>MT4134 응용 프로그램 사용 되는 ' *' 프레임 워크는 iOS 앱을 빌드하는 데 사용 하는 SDK에에서 포함 되지 않습니다 (이 프레임 워크는 iOS에 도입 된 * ios 작성 하는 반면, * SDK.) IOS 앱의 빌드 옵션에서에서 최신 SDK를 선택 하십시오.

### <a name="a-namemt4135mt4135--the-member--has-an-export-attribute-that-doesnt-specify-a-selector-a-selector-is-required"></a><a name="MT4135"/>MT4135 멤버 '\*.\*' 선택기를 지정 하지 않으면 내보내기 특성이 포함 됩니다. 선택 기가 필요 합니다.

### <a name="a-namemt4136mt4136--the-registrar-cannot-marshal-the-parameter-type--of-the-parameter--in-the-method-"></a><a name="MT4136"/>MT4136 등록자 매개 변수 형식을 마샬링할 수 없습니다 '\*'의 매개 변수'\*'method' in에서\*. *'

<!-- MT4137 is unused -->

### <a name="a-namemt4138mt4138--the-registrar-cannot-marshal-the-property-type--of-the-property-"></a><a name="MT4138"/>MT4138 등록자 속성 형식을 마샬링할 수 없습니다 '\*'property'의\*. *'입니다.

### <a name="a-namemt4139mt4139--the-registrar-cannot-marshal-the-property-type--of-the-property--properties-with-the-connect-attribute-must-have-a-property-type-of-nsobject-or-a-subclass-of-nsobject"></a><a name="MT4139"/>MT4139 등록자 속성 형식을 마샬링할 수 없습니다 '\*'property'의\*. *'입니다. [연결] 특성을 사용 하 여 속성 NSObject의 속성 형식이 (또는 NSObject의 서브 클래스)에 있어야 합니다.

### <a name="a-namemt4140mt4140--the-registrar-found-a-signature-mismatch-in-the-method----the-selector-indicates-the-variadic-method-takes--parameters-while-the-managed-method-has--parameters"></a><a name="MT4140"/>MT4140 등록자 서명 불일치 메서드에서 발견 '*.*'-선택기 나타냅니다 variadic 메서드를 사용 하며 * 매개 변수를 관리 되는 메서드에 동안 * 매개 변수입니다.

### <a name="a-namemt4141mt4141--cannot-register-the-selector--on-the-member--because-xamarinios-implicitly-registers-this-selector"></a><a name="MT4141"/>MT4141 등록할 수 없습니다 선택기 '\*'member' on\*' Xamarin.iOS이이 선택기를 암시적으로 등록 하기 때문에 있습니다.

경우에 프레임 워크 형식 서브클래싱는 보유' ', 구현 하는 동안 '릴리스' 또는 'dealloc' 메서드:

```csharp
class MyNSObject : NSObject
{
    [Export ("retain")]
    new void Retain () {}

    [Export ("release")]
    new void Release () {}

    [Export ("dealloc")]
    new void Dealloc () {}
}
```

그러나 클래스는 프레임 워크의 첫 번째 하위 클래스 되지 않는 경우 이러한 메서드를 재정의 하려면 가능한 형식입니다.

```csharp
class MyNSObject : NSObject
{
}

class MyCustomNSObject : MyNSObject
{
    [Export ("retain")]
    new void Retain () {}

    [Export ("release")]
    new void Release () {}

    [Export ("dealloc")]
    new void Dealloc () {}
}
```

이 경우 Xamarin.iOS 무시 됩니다 `retain`, `release` 및 `dealloc` 에 `MyNSObject` 클래스와 충돌 하지 않습니다.

### <a name="a-namemt4142mt4142-failed-to-register-the-type-"></a><a name="MT4142"/>MT4142: 형식을 등록 하지 못했습니다 ' *'입니다.
### <a name="a-namemt4143mt4143-the-objectivec-class--could-not-be-registered-it-does-not-seem-to-derive-from-any-known-objectivec-class-including-nsobject"></a><a name="MT4143"/>MT4143: ObjectiveC 클래스 ' *' 수 없는 등록 것으로 보이지 않아 (NSObject 포함) 모든 알려진된 ObjectiveC 클래스에서 파생 됩니다.
### <a name="a-namemt4144mt4144-cannot-register-the-method--since-it-does-not-have-an-associated-trampoline-please-file-a-bug-report-at-httpbugzillaxamarincom"></a><a name="MT4144"/>MT4144: 메서드를 등록할 수 없습니다. ' *' 관련된 trampoline 없기 때문입니다. Http://bugzilla.xamarin.com에 버그 보고서를 제출 하세요.

Xamarin.iOS에서 버그를 나타냅니다. 버그를 제출 하세요 [http://bugzilla.xamarin.com](https://bugzilla.xamarin.com/enter_bug.cgi?product=iOS)합니다.

### <a name="a-namemt4145mt4145-invalid-enum--enums-with-the-native-attribute-must-have-a-underlying-enum-type-of-either-long-or-ulong"></a><a name="MT4145"/>MT4145: 잘못 된 열거 ' *': 열거형 [네이티브] 특성으로 'long' 또는 'ulong'는 기본 열거형 형식이 있어야 합니다.
### <a name="a-namemt4146mt4146-the-name-parameter-of-the-registrar-attribute-on-the-class---contains-an-invalid-character--"></a><a name="MT4146"/>MT4146: Name 매개 변수 클래스는 등록자 특성의\*' ('\*')에 잘못 된 문자가: '\*' (\*).

Objectice C 클래스의 이름을 됨을 의미 있는 공백을 포함할 수 없습니다는 `Register` 해당 관리 되는 클래스의 특성을 가질 수 없습니다는 `Name` 매개 변수 중 하나는 공백을 포함할 수 없습니다.

있는지 확인 하십시오는 `Register` 오류 메시지에 언급 된 관리 되는 클래스의 특성에는 공백이 없어야 합니다.

### <a name="a-namemt4147mt4147-detected-a-protocol-inheriting-from-the-jsexport-protocol-while-using-the-dynamic-registrar-it-is-not-possible-to-export-protocols-to-javascriptcore-dynamically-the-static-registrar-must-be-used-add---registrarstatic-to-the-additional-mtouch-arguments-in-the-projects-ios-build-options-to-select-the-static-registrar"></a><a name="MT4147"/>MT4147: 동적 등록을 사용 하는 동안 JSExport 프로토콜에서 상속 하는 프로토콜을 발견 했습니다. 프로토콜 JavaScriptCore; 동적으로 내보낼 수 없으면 정적 등록을 사용 해야 합니다 (추가 '-등록자: 정적 프로젝트의 iOS 정적 등록자 선택 하려면 빌드 옵션에서에서 추가 mtouch 인수에).
### <a name="a-namemt4148mt4148-the-registrar-found-a-generic-protocol--exporting-generic-protocols-is-not-supported"></a><a name="MT4148"/>MT4148: 등록자 발견 일반적인 프로토콜: ' *'입니다. 일반 프로토콜 내보내기는 지원 되지 않습니다.
### <a name="a-namemt4149mt4149-cannot-register-the-method--because-the-type-of-the-first-parameter--does-not-match-the-category-type-"></a><a name="MT4149"/>MT4149: 메서드를 등록할 수 없습니다. '\*.\*' 때문에 첫 번째 매개 변수 형식 ('\*') 범주 형식과 일치 하지 않습니다 ('\*').
### <a name="a-namemt4150mt4150-cannot-register-the-type--because-the-type-property--in-its-category-attribute-does-not-inherit-from-nsobject"></a><a name="MT4150"/>MT4150: 유형을 등록할 수 없습니다 '\*' 때문에 Type 속성 ('\*') 해당 범주 특성에 NSObject에서 상속 되지 않습니다.
### <a name="a-namemt4151mt4151-cannot-register-the-type--because-the-type-property-in-its-category-attribute-isnt-set"></a><a name="MT4151"/>MT4151: 유형을 등록할 수 없습니다 ' *' 이므로 해당 범주 특성의 Type 속성이 설정 되어 있지 않습니다.
### <a name="a-namemt4152mt4152-cannot-register-the-type--as-a-category-because-it-implements-inativeobject-or-subclasses-nsobject"></a><a name="MT4152"/>MT4152: 유형을 등록할 수 없습니다 ' *'를 범주로 INativeObject 또는 NSObject 하위 클래스에서 구현 하기 때문에 있습니다.
### <a name="a-namemt4153mt4153-cannot-register-the-type--as-a-category-because-its-generic"></a><a name="MT4153"/>MT4153: 유형을 등록할 수 없습니다 '\*' 범주가 제네릭이므로 합니다.
### <a name="a-namemt4154mt4154-cannot-register-the-method--as-a-category-method-because-its-generic"></a><a name="MT4154"/>MT4154: 메서드를 등록할 수 없습니다. '\*' 범주 메서드로 제네릭이므로 합니다.
### <a name="a-namemt4155mt4155-cannot-register-the-method--with-the-selector--as-a-category-method-on--because-the-objective-c-already-has-an-implementation-for-this-selector"></a><a name="MT4155"/>MT4155: 메서드를 등록할 수 없습니다. '\*'with '선택기\*'의 범주 메서드로 ' *' Objective C이이 선택기에 대 한 구현을 이미 있어서 합니다.
### <a name="a-namemt4156mt4156-cannot-register-two-categories--and--with-the-same-native-name-"></a><a name="MT4156"/>MT4156: 두 개의 범주를 등록할 수 없습니다 ('\*'및'\*') 같은 네이티브 이름의 ('* ').
### <a name="a-namemt4157mt4157-cannot-register-the-category-method--because-at-least-one-parameter-is-required-and-its-type-must-match-the-category-type-"></a><a name="MT4157"/>MT4157: 범주 메서드를 등록할 수 없습니다. '\*' 매개 변수가 하나 이상 필요 하기 때문에 (해당 형식은 범주 형식과 일치 해야 하 고 '\*')
### <a name="a-namemt4158mt4158-cannot-register-the-constructor--in-the-category--because-constructors-in-categories-are-not-supported"></a><a name="MT4158"/>MT4158: 생성자를 등록할 수 없습니다. * 범주에 * 범주에는 생성자가 지원 되지 않기 때문입니다.
### <a name="a-namemt4159mt4159-cannot-register-the-method--as-a-category-method-because-category-methods-must-be-static"></a><a name="MT4159"/>MT4159: 메서드를 등록할 수 없습니다. ' *' 범주 방법으로 범주 메서드는 정적 이어야 하기 때문에 있습니다.

### <a name="a-namemt4160mt4160-invalid-character---found-in-selector--for-"></a><a name="MT4160"/>MT4160: 잘못 된 문자 '\*' (\*) 선택기에 '\*'for'\*'.

### <a name="a-namemt4161mt4161-the-registrar-found-an-unsupported-structure--all-fields-in-a-structure-must-also-be-structures-field--with-type-2-is-not-a-structure"></a><a name="MT4161"/>MT4161: 등록자는 지원 되지 않는 구조를 찾을 수 '\*': 구조체의 모든 필드에는 구조 여야 합니다. (필드 '\*' 유형 '{2 \}'는 구조체).

등록자 지원 되지 않는 필드가 있는 구조체를 찾을 수 있습니다.

Objective C에 노출 되는 구조체의 모든 필드에는 구조 (클래스) 여야 합니다.

### <a name="a-namemt4162mt4162-the-type--used-as--2-is-not-available-in---it-was-introduced-in---please-build-with-a-newer--sdk-usually-done-by-using-the-most-recent-version-of-xcode"></a><a name="MT4162"/>MT4162: 형식을 '\*' (으로 사용 * {2 \})에서 사용할 수 없으면 * * (에 도입 된 * *)\* 새로운 구축 하십시오 * SDK (일반적으로 Xcode의 가장 최신 버전을 사용 하 여 수행 합니다.

등록자의 현재 SDK에 포함 되어 있지 않은 형식이 있습니다.

Xcode를 업그레이드 하십시오.

### <a name="a-namemt4163mt4163-internal-error-in-the-registrar--please-file-a-bug-report-at-httpbugzillaxamarincom"></a><a name="MT4163"/>등록 기관 (*)에서 MT4163: 내부 오류입니다. Http://bugzilla.xamarin.com에 버그 보고서를 제출 하세요

이 오류는 Xamarin.iOS의 버그를 나타냅니다. 에 버그 보고서를 제출 하세요 [http://bugzilla.xamarin.com](https://bugzilla.xamarin.com/enter_bug.cgi?product=iOS)합니다.

### <a name="a-namemt4164mt4164-cannot-export-the-property--because-its-selector--is-an-objective-c-keyword-please-use-a-different-name"></a><a name="MT4164"/>MT4164: 내보낼 수 없습니다. 속성 '\*' 때문에 선택기 '\*' Objective C 키워드입니다. 다른 이름을 사용 하십시오.

속성에 대 한 선택기 유효한 Objective-c 식별자 아닙니다.

선택기로 유효한 Objective-c 식별자를 사용 하십시오.

### <a name="a-namemt4165mt4165-the-registrar-couldnt-find-the-type-systemvoid-in-any-of-the-referenced-assemblies"></a><a name="MT4165"/>MT4165: 등록자는 모든 참조 된 어셈블리에서 'System.Void' 형식의 찾을 수 없습니다.

이 오류 가능성이 가장 높은 Xamarin.iOS의 버그를 나타냅니다. 에 버그 보고서를 제출 하세요 [http://bugzilla.xamarin.com](https://bugzilla.xamarin.com/enter_bug.cgi?product=iOS)합니다.

### <a name="a-namemt4166mt4166-cannot-register-the-method--because-the-signature-contains-a-type--that-isnt-a-reference-type"></a><a name="MT4166"/>MT4166: 메서드를 등록할 수 없습니다. '\*' 서명을 형식이 때문에 (\*)가 참조 형식이 아닌입니다.

이것은 보통 Xamarin.iOS;의 버그를 나타냅니다. 버그를 제출 하세요 [http://bugzilla.xamarin.com](https://bugzilla.xamarin.com/enter_bug.cgi?product=iOS)합니다.

### <a name="a-namemt4167mt4167-cannot-register-the-method--because-the-signature-contains-a-generic-type--with-a-generic-argument-type-that-isnt-an-nsobject-subclass-"></a><a name="MT4167"/>MT4167: 메서드를 등록할 수 없습니다. '\*' 시그니처에 제네릭 형식 때문에 (\*) (*)는 NSObject 서브 클래스에 없는 제네릭 인수 형식입니다.

이것은 보통 Xamarin.iOS;의 버그를 나타냅니다. 버그를 제출 하세요 [http://bugzilla.xamarin.com](https://bugzilla.xamarin.com/enter_bug.cgi?product=iOS)합니다.

### <a name="a-namemt4168mt4168-cannot-register-the-type-managedname-because-its-objective-c-name-exportedname-is-an-objective-c-keyword-please-use-a-different-name"></a><a name="MT4168"/>MT4168: 유형을 등록할 수 없습니다 ' {관리\_이름}' 때문에 Objective-c 이름 ' {내보낸\_이름}'은 Objective C 키워드입니다. 다른 이름을 사용 하십시오.

Objective C 이름을 해당 유형에 유효한 Objective-c 식별자가 아닙니다.

유효한 Objective-c 식별자를 사용 하십시오.

## <a name="mt5xxx-gcc-and-toolchain-error-messages"></a>MT5xxx: GCC 및 도구 체인 오류 메시지

### <a name="mt51xx-compilation"></a>MT51xx: 컴파일

<!--
 MT5xxx GCC and toolchain
  MT51xx compilation
  -->

### <a name="a-namemt5101mt5101-missing--compiler-please-install-xcode-command-line-tools-component"></a><a name="MT5101"/>MT5101 누락 ' *' 컴파일러입니다. Xcode '명령줄 도구' 구성 요소를 설치 하십시오



### <a name="a-namemt5102mt5102-failed-to-assemble-the-file--please-file-a-bug-report-at-httpbugzillaxamarincom"></a><a name="MT5102"/>파일을 어셈블하지 못했습니다 MT5102 ' *'입니다. Http://bugzilla.xamarin.com에 버그 보고서를 제출 하세요



### <a name="a-namemt5103mt5103-failed-to-compile-the-file--please-file-a-bug-report-at-httpbugzillaxamarincom"></a><a name="MT5103"/>MT5103 파일을 컴파일하지 못했습니다. ' *'입니다. Http://bugzilla.xamarin.com에 버그 보고서를 제출 하세요



### <a name="a-namemt5104mt5104-could-not-find-neither-the--nor-the--compiler-please-install-xcode-command-line-tools-component"></a><a name="MT5104"/>모두 찾을 수 없습니다 MT5104는 '\*'또는'\*' 컴파일러입니다. Xcode '명령줄 도구' 구성 요소를 설치 하십시오

<!-- 5105 is used by mmp -->

### <a name="a-namemt5106mt5106-could-not-compile-the-files--please-file-a-bug-report-at-httpbugzillaxamarincom"></a><a name="MT5106"/>MT5106: 파일을 컴파일할 수 없습니다 ' *'입니다. Http://bugzilla.xamarin.com에 버그 보고서를 제출 하세요

이것은 보통 Xamarin.iOS;의 버그를 나타냅니다. 버그를 제출 하세요 [http://bugzilla.xamarin.com](https://bugzilla.xamarin.com/enter_bug.cgi?product=iOS)합니다.

### <a name="mt52xx-linking"></a>MT52xx: 연결

<!--
  MT52xx linking
  -->

### <a name="a-namemt5201mt5201-native-linking-failed-please-review-the-build-log-and-the-user-flags-provided-to-gcc-"></a><a name="MT5201"/>MT5201 네이티브 연결에 실패 했습니다. 빌드 로그 및 gcc에 제공 된 사용자 플래그를 검토 하십시오. *

### <a name="a-namemt5202mt5202-native-linking-failed-please-review-the-build-log"></a><a name="MT5202"/>MT5202 네이티브 연결에 실패 했습니다. 빌드 로그를 검토 하십시오.

### <a name="a-namemt5203mt5203-native-linking-warning-"></a><a name="MT5203"/>MT5203 네이티브 경고 연결: *

<!--- 5204-5208 are not used -->

### <a name="a-namemt5209mt5209-native-linking-error-"></a><a name="MT5209"/>MT5209 네이티브 연결 오류: *

### <a name="a-namemt5210mt5210-native-linking-failed-undefined-symbol--please-verify-that-all-the-necessary-frameworks-have-been-referenced-and-native-libraries-are-properly-linked-in"></a><a name="MT5210"/>MT5210: 네이티브 연결 실패 정의 되지 않은 기호: * 합니다. 필요한 모든 프레임 워크 참조 된 네이티브 라이브러리에서 제대로 연결 되어 있는지 확인 하십시오.

이 네이티브 링커 어딘가에 참조 되는 기호를 찾을 수 없을 때 발생 합니다. 여러 가지 이유로이 발생할 수 있습니다.

* 제 3 자 바인딩에 프레임 워크에 필요 하지만 바인딩이이 지정 하지 않습니다는 `[LinkWith]` 특성입니다. 솔루션:
  - 제 3 자 바인딩 작성자는 해당 원본에 액세스할 경우 수정 바인딩의 `[LinkWith]` 필요한 프레임 워크를 포함 하는 특성:

            [LinkWith ("mylib.a", Frameworks = "SystemConfiguration")]

  - 제 3 자 바인딩을 수정할 수 없는 경우 수동으로와 연결할 수는 필요한 프레임 워크를 전달 하 여 `-gcc_flags '-framework SystemFramework'` 를 `mtouch` (프로젝트의 iOS 빌드 옵션 페이지에서 추가 mtouch 인수를 수정 하 여 수행 됩니다. 기억 모든 프로젝트 구성에 대해 수행 해야이).
* 일부 경우에는 관리 되는 바인딩을 이루어져 여러 개의 네이티브 라이브러리 및 모든 바인딩을에 포함 되어야 합니다. 이 솔루션은 필요한 모든 네이티브 라이브러리 바인딩 프로젝트에 추가을 있도록 각 바인딩 프로젝트에 둘 이상의 기본 라이브러리를 것 같습니다.</li>
* 관리 되는 바인딩 네이티브 라이브러리에 존재 하지 않는 기본 기호를 참조 합니다.
    이 문제는 일반적으로 바인딩을 일정 시간 동안 존재 하 고 네이티브 코드는 특정 기본 클래스 중 하나 제거 되거나 바인딩을 업데이트 되지 않은 동안 이름이 변경 되도록이 시간 동안 수정한 후 때 발생 합니다.
* P/Invoke 존재 하지 않는 기본 기호를 참조 합니다. Xamarin.iOS 7.4부터는 <a href="#MT5214">MT5214</a> 이 있는 경우 오류가 보고 됩니다 (자세한 내용은 MT5214 참조).
* 제 3 자 바인딩 / c + +를 사용 하 여 라이브러리를 빌드 하지만 바인딩이이 지정 하지 않습니다는 `[LinkWith]` 특성입니다. 이 일반적으로 비교적 쉽게 인식할 수 없는 작업에 기호 때문에 변환 된 c + + 기호 (한 가지 일반적인 예는 `__ZNKSt9exception4whatEv`).
  - 제 3 자 바인딩 작성자는 해당 원본에 액세스할 경우 수정 바인딩의 `[LinkWith]` 설정할 특성은 `IsCxx` 플래그:

            [LinkWith ("mylib.a", IsCxx = true)]

  - 전달 하 여 해당 하는 플래그를 설정할 수 제 3 자 바인딩을 수정할 수 없습니다. 제 3 자 라이브러리와 함께 수동으로 연결 하 고, <code>-cxx</code> mtouch (이렇게 프로젝트의 iOS 빌드 옵션 페이지에서 추가 mtouch 인수를 수정 하려면 . 기억 모든 프로젝트 구성에 대해 수행 해야이).



### <a name="a-namemt5211mt5211-native-linking-failed-undefined-objective-c-class--the-symbol--could-not-be-found-in-any-of-the-libraries-or-frameworks-linked-with-your-application"></a><a name="MT5211"/>MT5211: 네이티브 연결 실패 정의 되지 않은 Objective-c 클래스: \*합니다. 기호 '\*' 라이브러리 또는 응용 프로그램과 연결 된 프레임 워크 중 하나에서 찾을 수 없습니다.

이 네이티브 링커 어딘가에 참조 되는 Objective-c 클래스를 찾을 수 없을 때 발생 합니다. 여러 가지 이유로이 발생할 수 있습니다: 동일 [MT5210](#MT5210) 외에 있습니다.

* 제 3 자 바인딩 Objective-c 프로토콜을 바인딩되지만 주석을 지정 하지 않았습니다 고 <code>[Protocol]</code> api 정의에 특성입니다. 솔루션:
  - 누락 된 추가 `[Protocol]` 특성:

              [BaseType (typeof (NSObject))]
              [Protocol] // Add this
              public interface MyProtocol
              {
              }



### <a name="a-namemt5212mt5212-native-linking-failed-duplicate-symbol-"></a><a name="MT5212"/>MT5212: 네이티브 연결 실패 중복 기호가: * 합니다.

이 네이티브 링커는 모든 기본 라이브러리 간에 중복 된 기호를 발견할 때 발생 합니다. 이 오류 메시지가 나타나면 있을 수 있습니다 하나 이상의 [MT5213](#MT5213) 기호의 각 위치를 사용 하 여 오류입니다. 이 오류의 원인은 다음과 같습니다.


* 같은 네이티브 라이브러리를 두 번 포함 됩니다.
* 두 개의 고유 네이티브 라이브러리는 동일한 기호를 정의 하려면 발생 합니다.
* 네이티브 라이브러리는 제대로 작성 되지 않은 하 고 동일한 기호를 두 번 이상 포함 합니다.
  터미널에서 명령 집합을 사용 하 여이 확인할 수 있습니다 (x86_64/armv7/armv7s/arm64에 대 한 작성 하는 아키텍처에 따라 i386 바꿉니다).

        # Native libraries are usually fat libraries, containing binary code for
        # several architectures in the same file. First we extract the binary
        # code for the architecture we're interested in.
        lipo libNative.a -thin i386 -output libNative.i386.a

        # Now query the native library for the duplicated symbol.
        nm libNative.i386.a | fgrep 'SYMBOL'

        # You can also list the object files inside the native library.
        # In most cases this will reveal duplicated object files.
        ar -t libNative.i386.a

  이 문제를 해결 하는 몇 가지 가능한 방법에는

  - 네이티브 라이브러리의 공급자 수정 하 고 업데이트 된 버전 제공 요청입니다.
  - 기타 개체 파일 (이 경우에 작동 문제는 실제로 복제 된 개체 파일)를 제거 하 여 직접 해결


            # Find out if the library is a fat library, and which
            # architectures it contains.
            lipo -info libNative.a

            # Extract each architecture (i386/x86_64/armv7/armv7s/arm64) to a separate file
            lipo libNative.a -thin ARCH -output libNative.ARCH.a

            # Extract the object files for the offending architecture
            # This will remove the duplicates by overwriting them
            # (since they have the same filename)
            mkdir -p ARCH
            cd ARCH
            ar -x ../libNative.ARCH.a

            # Reassemble the object files in an .a
            ar -r ../libNative.ARCH.a *.o
            cd ..

            # Reassemble the fat library
            lipo *.a -create -output libNative.a


  - 링커가 사용 하지 않는 코드를 제거 하도록 요청 합니다. Xamarin.iOS에서는이 자동으로 수행 다음 조건이 모두 충족 될 경우:
    - 모든 타사 바인딩 `[LinkWith]` 특성 SmartLink 사용 하도록 설정 합니다.

            [assembly: LinkWith ("libNative.a", SmartLink = true)]

    - 더 `-gcc_flags` mtouch (프로젝트의 iOS 빌드 옵션의 추가 mtouch 인수 필드)에 전달 됩니다.
    - 직접 사용 하지 않는 코드를 추가 하 여 제거 하도록 링커에 물어볼 수 이기도 `-gcc_flags -dead_strip` iOS 프로젝트의 추가 mtouch 인수에 빌드 옵션입니다.


### <a name="a-namemt5213mt5213-duplicate-symbol-in--location-related-to-previous-error"></a><a name="MT5213"/>MT5213: 중복의 기호: * (이전 오류와 관련 된 위치)

이 오류만 함께 보고 됩니다 [MT5212](#MT5212)합니다. 참조 하십시오 [MT5212](#MT5212) 자세한 정보에 대 한 합니다.

### <a name="a-namemt5214mt5214--native-linking-failed-undefined-symbol--this-symbol-was-referenced-the-managed-member--please-verify-that-all-the-necessary-frameworks-have-been-referenced-and-native-libraries-linked"></a><a name="MT5214"/>기호를 정의 되지 않은 연결 실패, MT5214 네이티브: * 합니다. 이 기호가 참조 된 관리 되는 멤버 * 합니다. 필요한 모든 프레임 워크 참조 및 네이티브 라이브러리 연결 되었는지 확인 하십시오.

관리 코드에 존재 하지 않는 기본 메서드를 P/Invoke 포함 되어 있으면이 오류가 보고 됩니다. 예:

```csharp
using System.Runtime.InteropServices;
class MyImports {
   [DllImport ("__Internal")]
   public static extern void MyInexistentFunc ();
}
```

가능한 해결 방법을 몇 가지가 있습니다.

  -  소스 코드에서 P/Invoke를 제거 합니다.
  -  (이렇게 iOS 프로젝트의 빌드 옵션에서에서 "모든 어셈블리"에 "링커 동작"을 설정 하 여) 하는 모든 어셈블리에 대해 관리 되는 링커를 사용 하도록 설정 합니다. 응용 프로그램에서 모든는 P/Invoke 사용 하지 않는 효과적으로 제거 합니다 (자동으로 대신 수동으로 등의 이전 시점). 단점은 시뮬레이터 빌드 느려지지만, 이렇게 하면 하 고 리플렉션을 사용 하 여는-링커에 대 한 자세한 정보를 찾을 수 있습니다 하는 경우 앱을 줄 수 있기 [여기](~/ios/deploy-test/linker.md) )
  -  누락 된 네이티브 기호가 포함 된 두 번째 네이티브 라이브러리를 만듭니다. 해결 방법 뿐입니다 (해당 함수를 호출 하려고 하는 경우 응용 프로그램 작동이 중단 됩니다).

### <a name="a-namemt5215mt5215-references-to--might-require-additional--frameworkxxx-or--lxxx-instructions-to-the-native-linker"></a><a name="MT5215"/>MT5215:에 대 한 참조 ' *' 추가-필요할 수 있습니다 프레임 워크 = XXX 또는-lXXX 네이티브 링커 지침

이 P/Invoke, 라이브러리를 참조 하려면 감지 되었지만 함께 앱 링크 되지 않습니다 있는지를 나타내는 경고 합니다.

### <a name="a-namemt5216mt5216-native-linking-failed-for--please-file-a-bug-report-at-httpbugzillaxamarincom"></a><a name="MT5216"/>MT5216: 네이티브 연결에 대해 실패 한 * 합니다. Http://bugzilla.xamarin.com에 버그 보고서를 제출 하세요

이 오류는 AOT 컴파일러에서 출력에 연결 하는 경우 보고 됩니다.

이 오류 가능성이 가장 높은 Xamarin.iOS의 버그를 나타냅니다. 에 버그 보고서를 제출 하세요 [http://bugzilla.xamarin.com](https://bugzilla.xamarin.com/enter_bug.cgi?product=iOS)합니다.

### <a name="a-namemt5217mt5217-native-linking-possibly-failed-because-the-linker-command-line-was-too-long--characters"></a><a name="MT5217"/>MT5217: 링커 명령줄 너무 길어 수 있는 네이티브 연결 하지 못했습니다. (* 자).

네이티브 연결 실패, 및 링커 명령 너무 길어이 오류가 발생 한 수입니다.

Xamarin.iOS 프로젝트는 자주 참조 네이티브 기호가 동적으로 의미 하는 네이티브 링커가 네이티브 연결 프로세스 중 네이티브 그러한 기호를 제거할 수 있으므로 이러한 기호를 사용 하는 네이티브 링커는 표시 되지 않습니다.

일반적으로 Xamarin.iOS 네이티브 링커를 사용 하 여 이러한 기호를 그대로 유지를 묻습니다는 `-u symbol` 명령줄 전체 많은 기호, 많은 경우 하지만 링커 플래그를 운영 체제에서 지정 된 대로 명령줄 최대 길이 초과 될 수 있습니다.

이러한 동적 기호에 대 한 몇 가지 가능한 소스 가지가 있습니다.

* P/Invoke를 정적으로 연결 된 라이브러리의 메서드 (여기서은 dll 이름 `__Internal` DllImport 특성에 `[DllImport ("__Internal")]`).
* 정적으로 연결 된 라이브러리의 메모리 위치에 대 한 참조를 프로젝트 바인딩에서 필드 (`[Field]` 특성).
* Objective C 클래스 (증분 빌드를 사용 하는 경우 또는 정적 등록자를 사용 하지 않는 경우) 프로젝트 바인딩에서 정적으로 연결 된 라이브러리에서 참조 합니다.

가능한 해결 방법:

* 가능한 경우 유일한 SDK 어셈블리 대신 모든 어셈블리에 대 한 관리 되는 링커를 사용 하도록 설정 합니다. 동적 기호 링커 명령줄의 있도록 하지는 최대값을 초과 대 한 원본 충분히 제거할 수도 있습니다.
* P/Invoke, 필드 참조 및/또는 Objective-c 클래스 수를 줄입니다.
* 짧은 이름에 동적 기호를 다시 작성 합니다.
* 전달 `-dlsym:false` 인수로 추가 mtouch iOS 프로젝트의 빌드 옵션입니다. 이 옵션을 Xamarin.iOS AOT 컴파일된 코드에서 네이티브 참조를 생성할 및이 기호를 유지 하도록 링커에 게 필요 하지는 않습니다. 그러나 장치에만이 방법이 가능 빌드되고 P/Invoke 정적 라이브러리에 존재 하지 않는 함수에 없는 경우 링커 오류가 발생 합니다.
* 전달 `--dynamic-symbol-mode=code` ios 프로젝트의 추가 mtouch 인수로 빌드 옵션입니다. 이 옵션을 Xamarin.iOS 네이티브 링커 명령줄 인수를 사용 하 여 이러한 기호를 그대로 유지를 요청 하는 대신 이러한 기호를 참조 하는 추가 네이티브 코드가 생성 됩니다. 이 방식의 단점은 것 실행 파일의 크기를 다소 증가 합니다입니다.
* 정적 등록 기관 전달 하 여 사용 하도록 설정 `--registrar:static` 인수로 추가 mtouch iOS 프로젝트의 빌드 (에 대 한 옵션 시뮬레이터 빌드, 장치 빌드에 대해 정적 등록 자가 이미 기본 하기 때문). 이러한 클래스를 유지 하려면 기본 링커 요청할 필요가 없습니다 정적 등록 기관 Objective-c 클래스에 정적으로 참조 하는 코드를 생성 됩니다.
* (장치 빌드)에 대 한 증분 빌드를 사용 하지 않도록 설정 합니다. 증분 빌드 설정 되 면 Xamarin.iOS 유지 하도록 링커에 요청 계속 해야 하는 즉 Objective-c 클래스를 참조 하는 네이티브 링커로 정적 등록 기관에 의해 생성 된 코드 것으로 간주 되지 않습니다. 따라서 증분 빌드를 사용 하지 않도록 설정 하면이 요구가 되지 것입니다.

### <a name="a-namemt5218mt5218-cant-ignore-the-dynamic-symbol-symbol---ignore-dynamic-symbolsymbol-because-it-was-not-detected-as-a-dynamic-symbol"></a><a name="MT5218"/>MT5218: 동적 기호 {기호}를 무시할 수 없습니다 (-동적 무시-기호 = {기호로})는 동적 기호로 검색 되지 않아 합니다.

명령줄 인수 `--ignore-dynamic-symbol=symbol` 전달 된이 기호를 수동으로 유지 해야 하는 동적 기호로 인식 된 기호 않습니다.

이 두 가지 주요 이유는

* 기호 이름이 올바르지 않습니다.
    * 기호 이름에 밑줄이 앞에 추가 하지 마십시오.
    * Objective C 클래스에 대 한 기호가 `OBJC_CLASS_$_<classname>`합니다.
* 기호 올바른지, 하지만 (일부 빌드 옵션 원인을 정확 하 게 변경 하려면 동적 기호 목록) 하는 일반적인 방법으로 이미 유지 되는 기호를 쉽습니다.

### <a name="mt53xx-other-tools"></a>기타 도구에 MT53xx:

<!--
  MT53xx other tools
  -->

### <a name="a-namemt5301mt5301-missing-strip-tool-please-install-xcode-command-line-tools-component"></a><a name="MT5301"/>MT5301: '제거' 도구가 없습니다. Xcode '명령줄 도구' 구성 요소를 설치 하십시오



### <a name="a-namemt5302mt5302-missing-dsymutil-tool-please-install-xcode-command-line-tools-component"></a><a name="MT5302"/>MT5302: 누락 된 'dsymutil' 도구입니다. Xcode '명령줄 도구' 구성 요소를 설치 하십시오



### <a name="a-namemt5303mt5303-failed-to-generate-the-debug-symbols-dsym-directory-please-review-the-build-log"></a><a name="MT5303"/>MT5303: 디버그 기호 (dSYM 디렉터리)를 생성 하지 못했습니다. 빌드 로그를 검토 하십시오.

Dsymutil 디버그 기호를 만들려면 최종.app 디렉터리에서 실행 오류가 발생 했습니다. Dsymutil의 출력을 보고 수정 방법을 참조 하세요. 빌드 로그를 검토 하십시오.

### <a name="a-namemt5304mt5304-failed-to-strip-the-final-binary-please-review-the-build-log"></a><a name="MT5304"/>MT5304:를 최종 이진 파일을 제거 하지 못했습니다. 빌드 로그를 검토 하십시오.

응용 프로그램에서 디버깅 정보를 제거 하려면 '스트립' 도구를 실행 하는 오류가 발생 했습니다.

### <a name="a-namemt5305mt5305-missing-lipo-tool-please-install-xcode-command-line-tools-component"></a><a name="MT5305"/>MT5305: 누락 된 'lipo' 도구입니다. Xcode '명령줄 도구' 구성 요소를 설치 하십시오



### <a name="a-namemt5306mt5306-failed-to-create-the-a-fat-library-please-review-the-build-log"></a><a name="MT5306"/>MT5306:를 만들지 못했습니다는 fat 라이브러리입니다. 빌드 로그를 검토 하십시오.

'Lipo' 도구를 실행 하는 오류가 발생 했습니다. 빌드 로그 'lipo'에서 보고 한 오류를 검토 하십시오.

### <a name="a-namemt5307mt5307-failed-to-sign-the-executable-please-review-the-build-log"></a><a name="MT5307"/>MT5307: 실행 파일을 등록 하지 못했습니다. 빌드 로그를 검토 하십시오.

응용 프로그램에 서명 하는 오류가 발생 했습니다. 빌드 로그 '코드 서명'에서 보고 한 오류를 검토 하십시오.

<!-- 5308 is used by mmp -->
<!-- 5309 is used by mmp -->
<!-- 5310 is used by mmp -->

## <a name="mt6xxx-mtouch-internal-tools-error-messages"></a>MT6xxx: mtouch 내부 도구 오류 메시지

### <a name="mt600x-stripper"></a>MT600x: 제거

<!--
 MT6xxx mtouch internal tools
  MT600x Stripper
  -->

### <a name="a-namemt6001mt6001-running-version-of-cecil-doesnt-support-assembly-stripping"></a><a name="MT6001"/>MT6001: Cecil 실행 버전이 제거 되는 어셈블리를 지원 하지 않습니다.

### <a name="a-namemt6002mt6002-could-not-strip-assembly-"></a><a name="MT6002"/>MT6002: 어셈블리를 제거 하지 못했습니다 `*`합니다.

응용 프로그램에는 어셈블리에서 관리 코드 (IL 코드 제거)를 제거 하는 오류가 발생 했습니다.

### <a name="a-namemt6003mt6003-unauthorizedaccessexception-message"></a><a name="MT6003"/>MT6003: [UnauthorizedAccessException message]

디버깅 응용 프로그램에서 기호를 제거 하는 동안 보안 오류가 발생 했습니다.

## <a name="mt7xxx-msbuild-error-messages"></a>MT7xxx: MSBuild 오류 메시지

<!--
 MT7xxx msbuild errors
  -->

### <a name="a-namemt7001mt7001-could-not-resolve-host-ips-for-wifi-debugger-settings"></a><a name="MT7001"/>MT7001: WiFi 디버거 설정에 대 한 호스트 Ip를 확인할 수 없습니다.

*MSBuild 작업: DetectDebugNetworkConfigurationTaskBase*

문제 해결 단계:

- 실행 하려고 `csharp -e 'System.Net.Dns.GetHostEntry (System.Net.Dns.GetHostName ()).AddressList'` (하를 제공 해야 IP 주소와는 오류가 아니라 분명히).
- 실행 하려고 "ping \`hostname\`"를 제공할 수 있습니다에 자세한 내용은 예: `cannot resolve MyHost.local: Unknown host`

일부 경우에는 "로컬 네트워크" 문제 이며 알 수 없는 호스트를 추가 하 여 해결할 수 있습니다 `127.0.0.1   MyHost.local` 에서 `/etc/hosts`합니다.

### <a name="a-namemt7002mt7002-this-machine-does-not-have-any-network-adapters-this-is-required-when-debugging-or-profiling-on-device-over-wifi"></a><a name="MT7002"/>MT7002:이 컴퓨터 네트워크 어댑터에 필요가 없습니다. 이 디버깅 또는 WiFi를 통해 장치에서 프로 파일링 하는 경우에 필요 합니다.

*MSBuild 작업: DetectDebugNetworkConfigurationTaskBase*

### <a name="a-namemt7003mt7003-the-app-extension--does-not-contain-an-infoplist"></a><a name="MT7003"/>MT7003: 응용 프로그램 확장 ' *'는 Info.plist 포함 되어 있지 않습니다.

*MSBuild 작업: ValidateAppBundleTaskBase*

### <a name="a-namemt7004mt7004-the-app-extension--does-not-specify-a-cfbundleidentifier"></a><a name="MT7004"/>MT7004: 응용 프로그램 확장 ' *'는 CFBundleIdentifier 지정 하지 않습니다.

*MSBuild 작업: ValidateAppBundleTaskBase*

### <a name="a-namemt7005mt7005-the-app-extension--does-not-specify-a-cfbundleexecutable"></a><a name="MT7005"/>MT7005: 응용 프로그램 확장 ' *'는 CFBundleExecutable 지정 하지 않습니다.

*MSBuild 작업: ValidateAppBundleTaskBase*

### <a name="a-namemt7006mt7006-the-app-extension--has-an-invalid-cfbundleidentifier--it-does-not-begin-with-the-main-app-bundles-cfbundleidentifier-"></a><a name="MT7006"/>MT7006: 응용 프로그램 확장 '\*'에 잘못 된 CFBundleIdentifier (\*), 기본 응용 프로그램 번들 CFBundleIdentifier (*)로 시작 하지 않습니다.

*MSBuild 작업: ValidateAppBundleTaskBase*

### <a name="a-namemt7007mt7007-the-app-extension--has-a-cfbundleidentifier--that-ends-with-the-illegal-suffix-key"></a><a name="MT7007"/>MT7007: 응용 프로그램 확장 '\*'에 CFBundleIdentifier (\*) 잘못 되었습니다. 접미사 ".key"로 끝나는 합니다.

*MSBuild 작업: ValidateAppBundleTaskBase*

### <a name="a-namemt7008mt7008-the-app-extension--does-not-specify-a-cfbundleshortversionstring"></a><a name="MT7008"/>MT7008: 응용 프로그램 확장 ' *'는 CFBundleShortVersionString 지정 하지 않습니다.

*MSBuild 작업: ValidateAppBundleTaskBase*

### <a name="a-namemt7009mt7009-the-app-extension--has-an-invalid-infoplist-it-does-not-contain-an-nsextension-dictionary"></a><a name="MT7009"/>MT7009: 응용 프로그램 확장 ' *'에 잘못 된 Info.plist: NSExtension 사전 포함 되어 있지 않습니다.

*MSBuild 작업: ValidateAppBundleTaskBase*

### <a name="a-namemt7010mt7010-the-app-extension--has-an-invalid-infoplist-the-nsextension-dictionary-does-not-contain-an-nsextensionpointidentifier-value"></a><a name="MT7010"/>MT7010: 응용 프로그램 확장 ' *'에 잘못 된 Info.plist: NSExtension 사전은 NSExtensionPointIdentifier 값이 포함 되지 않습니다.

*MSBuild 작업: ValidateAppBundleTaskBase*

### <a name="a-namemt7011mt7011-the-watchkit-extension--has-an-invalid-infoplist-the-nsextension-dictionary-does-not-contain-an-nsextensionattributes-dictionary"></a><a name="MT7011"/>MT7011: WatchKit 확장 ' *'에 잘못 된 Info.plist: NSExtension 사전 NSExtensionAttributes 사전 포함 되어 있지 않습니다.

*MSBuild 작업: ValidateAppBundleTaskBase*

### <a name="a-namemt7012mt7012-the-watchkit-extension--does-not-have-exactly-one-watch-app"></a><a name="MT7012"/>MT7012: WatchKit 확장 ' *' 정확히 하나의 watch 앱이 없습니다.

*MSBuild 작업: ValidateAppBundleTaskBase*

### <a name="a-namemt7013mt7013-the-watchkit-extension--has-an-invalid-infoplist-uirequireddevicecapabilities-must-contain-the-watch-companion-capability"></a><a name="MT7013"/>MT7013: WatchKit 확장 ' *'에 잘못 된 Info.plist: UIRequiredDeviceCapabilities ' 조사식 도우미 ' 기능을 포함 해야 합니다.

*MSBuild 작업: ValidateAppBundleTaskBase*

### <a name="a-namemt7014mt7014-the-watch-app--does-not-contain-an-infoplist"></a><a name="MT7014"/>MT7014: Watch 앱 ' *'는 Info.plist 포함 되어 있지 않습니다.

*MSBuild 작업: ValidateAppBundleTaskBase*

### <a name="a-namemt7015mt7015-the-watch-app--does-not-specify-a-cfbundleidentifier"></a><a name="MT7015"/>MT7015: Watch 앱 ' *'는 CFBundleIdentifier 지정 하지 않습니다.

*MSBuild 작업: ValidateAppBundleTaskBase*

### <a name="a-namemt7016mt7016-the-watch-app--has-an-invalid-cfbundleidentifier--it-does-not-begin-with-the-main-app-bundles-cfbundleidentifier-"></a><a name="MT7016"/>MT7016: Watch 앱 '\*'에 잘못 된 CFBundleIdentifier (\*), 기본 응용 프로그램 번들 CFBundleIdentifier (*)로 시작 하지 않습니다.

*MSBuild 작업: ValidateAppBundleTaskBase*

### <a name="a-namemt7017mt7017-the-watch-app--does-not-have-a-valid-uidevicefamily-value-expected-watch-4-but-found--"></a><a name="MT7017"/>MT7017: Watch 앱 '\*' 유효한 UIDeviceFamily 값이 없습니다. 예상 '감시 (4)' 개가 발견 되었습니다 '\* (*)'입니다.

*MSBuild 작업: ValidateAppBundleTaskBase*

### <a name="a-namemt7018mt7018-the-watch-app--does-not-specify-a-cfbundleexecutable"></a><a name="MT7018"/>MT7018: Watch 앱 ' *'는 CFBundleExecutable 지정 하지 않습니다

*MSBuild 작업: ValidateAppBundleTaskBase*

### <a name="a-namemt7019mt7019-the-watch-app--has-an-invalid-wkcompanionappbundleidentifier-value--it-does-not-match-the-main-app-bundles-cfbundleidentifier-"></a><a name="MT7019"/>MT7019: Watch 앱 '\*'에 잘못 된 WKCompanionAppBundleIdentifier 값 ('\*'), 주 응용 프로그램 번들 CFBundleIdentifier와 일치 하지 않습니다 ('* ').

*MSBuild 작업: ValidateAppBundleTaskBase*

### <a name="a-namemt7020mt7020-the-watch-app--has-an-invalid-infoplist-the-wkwatchkitapp-key-must-be-present-and-have-a-value-of-true"></a><a name="MT7020"/>MT7020: Watch 앱 ' *'에 잘못 된 Info.plist: WKWatchKitApp 키 있어야 하며 'true' 값이 있어야 합니다.

*MSBuild 작업: ValidateAppBundleTaskBase*

### <a name="a-namemt7021mt7021-the-watch-app--has-an-invalid-infoplist-the-lsrequiresiphoneos-key-must-not-be-present"></a><a name="MT7021"/>MT7021: Watch 앱 ' *'에 잘못 된 Info.plist: LSRequiresIPhoneOS 키 없어야 합니다.

*MSBuild 작업: ValidateAppBundleTaskBase*

### <a name="a-namemt7022mt7022-the-watch-app--does-not-contain-a-watch-extension"></a><a name="MT7022"/>MT7022: Watch 앱 ' *' 조사식 확장명이 없습니다.

*MSBuild 작업: ValidateAppBundleTaskBase*

### <a name="a-namemt7023mt7023-the-watch-extension--does-not-contain-an-infoplist"></a><a name="MT7023"/>MT7023: 조사식 확장 ' *'는 Info.plist 포함 되어 있지 않습니다.

*MSBuild 작업: ValidateAppBundleTaskBase*

### <a name="a-namemt7024mt7024-the-watch-extension--does-not-specify-a-cfbundleidentifier"></a><a name="MT7024"/>MT7024: 조사식 확장 ' *'는 CFBundleIdentifier 지정 하지 않습니다.

*MSBuild 작업: ValidateAppBundleTaskBase*

### <a name="a-namemt7025mt7025-the-watch-extension--does-not-specify-a-cfbundleexecutable"></a><a name="MT7025"/>MT7025: 조사식 확장 ' *'는 CFBundleExecutable 지정 하지 않습니다.

*MSBuild 작업: ValidateAppBundleTaskBase*

### <a name="a-namemt7026mt7026-the-watch-extension--has-an-invalid-cfbundleidentifier--it-does-not-begin-with-the-main-app-bundles-cfbundleidentifier-"></a><a name="MT7026"/>MT7026: 조사식 확장 '\*'에 잘못 된 CFBundleIdentifier (\*), 기본 응용 프로그램 번들 CFBundleIdentifier (*)로 시작 하지 않습니다.

*MSBuild 작업: ValidateAppBundleTaskBase*

### <a name="a-namemt7027mt7027-the-watch-extension--has-a-cfbundleidentifier--that-ends-with-the-illegal-suffix-key"></a><a name="MT7027"/>MT7027: 조사식 확장 '\*'에 CFBundleIdentifier (\*) 잘못 되었습니다. 접미사 ".key"로 끝나는 합니다.

*MSBuild 작업: ValidateAppBundleTaskBase*

### <a name="a-namemt7028mt7028-the-watch-extension--has-an-invalid-infoplist-it-does-not-contain-an-nsextension-dictionary"></a><a name="MT7028"/>MT7028: 조사식 확장 ' *'에 잘못 된 Info.plist: NSExtension 사전 포함 되어 있지 않습니다.

*MSBuild 작업: ValidateAppBundleTaskBase*

### <a name="a-namemt7029mt7029-the-watch-extension--has-an-invalid-infoplist-the-nsextensionpointidentifier-must-be-comapplewatchkit"></a><a name="MT7029"/>MT7029: 조사식 확장 ' *'에 잘못 된 Info.plist:는 NSExtensionPointIdentifier "com.apple.watchkit" 이어야 합니다.

*MSBuild 작업: ValidateAppBundleTaskBase*

### <a name="a-namemt7030mt7030-the-watch-extension--has-an-invalid-infoplist-the-nsextension-dictionary-must-contain-nsextensionattributes"></a><a name="MT7030"/>MT7030: 조사식 확장 ' *'에 잘못 된 Info.plist: NSExtension 사전 NSExtensionAttributes 포함 해야 합니다.

*MSBuild 작업: ValidateAppBundleTaskBase*

### <a name="a-namemt7031mt7031-the-watch-extension--has-an-invalid-infoplist-the-nsextensionattributes-dictionary-must-contain-a-wkappbundleidentifier"></a><a name="MT7031"/>MT7031: 조사식 확장 ' *'에 잘못 된 Info.plist: NSExtensionAttributes 사전은 WKAppBundleIdentifier 포함 해야 합니다.

*MSBuild 작업: ValidateAppBundleTaskBase*

### <a name="a-namemt7032mt7032-the-watchkit-extension--has-an-invalid-infoplist-uirequireddevicecapabilities-should-not-contain-the-watch-companion-capability"></a><a name="MT7032"/>MT7032: WatchKit 확장 ' *'에 잘못 된 Info.plist: UIRequiredDeviceCapabilities ' 조사식 도우미 ' 기능을 사용할 수 없습니다.

*MSBuild 작업: ValidateAppBundleTaskBase*

### <a name="a-namemt7033mt7033-the-watch-app--does-not-contain-an-infoplist"></a><a name="MT7033"/>MT7033: Watch 앱 ' *'는 Info.plist 포함 되어 있지 않습니다.

*MSBuild 작업: ValidateAppBundleTaskBase*

### <a name="a-namemt7034mt7034-the-watch-app--does-not-specify-a-cfbundleidentifier"></a><a name="MT7034"/>MT7034: Watch 앱 ' *'는 CFBundleIdentifier 지정 하지 않습니다.

*MSBuild 작업: ValidateAppBundleTaskBase*

### <a name="a-namemt7035mt7035-the-watch-app--does-not-have-a-valid-uidevicefamily-value-expected--but-found--"></a><a name="MT7035"/>MT7035: Watch 앱 '\*' 유효한 UIDeviceFamily 값이 없습니다. 예상 '\*'प ू ण'\* (\*)'입니다.

*MSBuild 작업: ValidateAppBundleTaskBase*

### <a name="a-namemt7036mt7036-the-watch-app--does-not-specify-a-cfbundleexecutable"></a><a name="MT7036"/>MT7036: Watch 앱 ' *'는 CFBundleExecutable 지정 하지 않습니다.

*MSBuild 작업: ValidateAppBundleTaskBase*

### <a name="a-namemt7037mt7037-the-watchkit-extension-extensionname-has-an-invalid-wkappbundleidentifier-value--it-does-not-match-the-watch-apps-cfbundleidentifier-"></a><a name="MT7037"/>MT7037: WatchKit 확장 '{extensionName을 (를)'에 잘못 된 WKAppBundleIdentifier 값 ('\*'), Watch 앱 CFBundleIdentifier와 일치 하지 않습니다 ('\*').

*MSBuild 작업: ValidateAppBundleTaskBase*

### <a name="a-namemt7038mt7038-the-watch-app--has-an-invalid-infoplist-the-wkcompanionappbundleidentifier-must-exist-and-must-match-the-main-app-bundles-cfbundleidentifier"></a><a name="MT7038"/>MT7038: Watch 앱 ' *'에 잘못 된 Info.plist:는 WKCompanionAppBundleIdentifier 존재 해야 하며 주 응용 프로그램 번들 CFBundleIdentifier 일치 해야 합니다.

*MSBuild 작업: ValidateAppBundleTaskBase*

### <a name="a-namemt7039mt7039-the-watch-app--has-an-invalid-infoplist-the-lsrequiresiphoneos-key-must-not-be-present"></a><a name="MT7039"/>MT7039: Watch 앱 ' *'에 잘못 된 Info.plist: LSRequiresIPhoneOS 키 없어야 합니다.

*MSBuild 작업: ValidateAppBundleTaskBase*

### <a name="a-namemt7040mt7040-the-app-bundle-appbundlepath-does-not-contain-an-infoplist"></a><a name="MT7040"/>MT7040: 앱 번들 {AppBundlePath}는 Info.plist 포함 되지 않습니다.

*MSBuild 작업: ValidateAppBundleTaskBase*

### <a name="a-namemt7041mt7041-main-infoplist-path-does-not-specify-a-cfbundleidentifier"></a><a name="MT7041"/>MT7041: Main Info.plist 경로 CFBundleIdentifier를 지정 하지 않습니다.

*MSBuild 작업: ValidateAppBundleTaskBase*

### <a name="a-namemt7042mt7042-main-infoplist-path-does-not-specify-a-cfbundleexecutable"></a><a name="MT7042"/>MT7042: Main Info.plist 경로 CFBundleExecutable를 지정 하지 않습니다.

*MSBuild 작업: ValidateAppBundleTaskBase*

### <a name="a-namemt7043mt7043-main-infoplist-path-does-not-specify-a-cfbundlesupportedplatforms"></a><a name="MT7043"/>MT7043: Main Info.plist 경로 CFBundleSupportedPlatforms를 지정 하지 않습니다.

*MSBuild 작업: ValidateAppBundleTaskBase*

### <a name="a-namemt7044mt7044-main-infoplist-path-does-not-specify-a-uidevicefamily"></a><a name="MT7044"/>MT7044: Main Info.plist 경로 UIDeviceFamily를 지정 하지 않습니다.

*MSBuild 작업: ValidateAppBundleTaskBase*

### <a name="a-namemt7045mt7045-unrecognized-format-"></a><a name="MT7045"/>MT7045: 형식을 인식할 수 없는: * 합니다.

*MSBuild 작업: PropertyListEditorTaskBase*

여기서 * 될 수 있습니다.

- string
- array
- dict
- bool
- 실수
- 정수
- date
- 데이터

### <a name="a-namemt7046mt7046-add-entry--incorrectly-specified"></a><a name="MT7046"/>MT7046: Add: Entry, *, Incorrectly Specified.

*MSBuild 작업: PropertyListEditorTaskBase*

### <a name="a-namemt7047mt7047-add-entry--contains-invalid-array-index"></a><a name="MT7047"/>MT7047: Add: Entry, *, Contains Invalid Array Index.

*MSBuild 작업: PropertyListEditorTaskBase*

### <a name="a-namemt7048mt7048-add--entry-already-exists"></a><a name="MT7048"/>MT7048: 추가: * 항목이 이미 있습니다.

*MSBuild 작업: PropertyListEditorTaskBase*

### <a name="a-namemt7049mt7049-add-cant-add-entry--to-parent"></a><a name="MT7049"/>MT7049: 추가: 항목을 추가할 수 없습니다 *, 부모를 합니다.

*MSBuild 작업: PropertyListEditorTaskBase*

### <a name="a-namemt7050mt7050-delete-cant-delete-entry--from-parent"></a><a name="MT7050"/>MT7050: 삭제: 항목을 삭제할 수 없습니다 *, 부모에서 합니다.

*MSBuild 작업: PropertyListEditorTaskBase*

### <a name="a-namemt7051mt7051-delete-entry--contains-invalid-array-index"></a><a name="MT7051"/>MT7051: 삭제: 항목, *, 잘못 된 배열 인덱스를 포함 합니다.

*MSBuild 작업: PropertyListEditorTaskBase*

### <a name="a-namemt7052mt7052-delete-entry--does-not-exist"></a><a name="MT7052"/>MT7052: 삭제: 항목, *, 존재 하지 않습니다.

*MSBuild 작업: PropertyListEditorTaskBase*

### <a name="a-namemt7053mt7053-import-entry--incorrectly-specified"></a><a name="MT7053"/>MT7053: 가져오기: 항목, *, 잘못 지정 된 합니다.

*MSBuild 작업: PropertyListEditorTaskBase*

### <a name="a-namemt7054mt7054-import-entry--contains-invalid-array-index"></a><a name="MT7054"/>MT7054: 가져오기: 항목, *, 잘못 된 배열 인덱스를 포함 합니다.

*MSBuild 작업: PropertyListEditorTaskBase*

### <a name="a-namemt7055mt7055-import-error-reading-file-"></a><a name="MT7055"/>MT7055: 가져오기: 파일 읽기 오류: * 합니다.

*MSBuild 작업: PropertyListEditorTaskBase*

### <a name="a-namemt7056mt7056-import-cant-add-entry--to-parent"></a><a name="MT7056"/>MT7056: 가져오기: 항목을 추가할 수 없습니다 *, 부모를 합니다.

*MSBuild 작업: PropertyListEditorTaskBase*

### <a name="a-namemt7057mt7057-merge-cant-add-array-entries-to-dict"></a><a name="MT7057"/>MT7057: 병합: dict.에 배열 항목을 추가할 수 없습니다

*MSBuild 작업: PropertyListEditorTaskBase*

### <a name="a-namemt7058mt7058-merge-specified-entry-must-be-a-container"></a><a name="MT7058"/>MT7058: 병합: 지정한 항목은 컨테이너 여야 합니다.

*MSBuild 작업: PropertyListEditorTaskBase*

### <a name="a-namemt7059mt7059-merge-entry--contains-invalid-array-index"></a><a name="MT7059"/>MT7059: 병합: 항목, *, 잘못 된 배열 인덱스를 포함 합니다.

*MSBuild 작업: PropertyListEditorTaskBase*

### <a name="a-namemt7060mt7060-merge-entry--does-not-exist"></a><a name="MT7060"/>MT7060: 병합: 항목, *, 존재 하지 않습니다.

*MSBuild 작업: PropertyListEditorTaskBase*

### <a name="a-namemt7061mt7061-merge-error-reading-file-"></a><a name="MT7061"/>MT7061: 병합: 파일 읽기 오류: * 합니다.

*MSBuild 작업: PropertyListEditorTaskBase*

### <a name="a-namemt7062mt7062-set-entry--incorrectly-specified"></a><a name="MT7062"/>MT7062: 설정: 항목, *, 잘못 지정 된 합니다.

*MSBuild 작업: PropertyListEditorTaskBase*

### <a name="a-namemt7063mt7063-set-entry--contains-invalid-array-index"></a><a name="MT7063"/>MT7063: 설정: 항목, *, 잘못 된 배열 인덱스를 포함 합니다.

*MSBuild 작업: PropertyListEditorTaskBase*

### <a name="a-namemt7064mt7064-set-entry--does-not-exist"></a><a name="MT7064"/>MT7064: 설정: 항목, *, 존재 하지 않습니다.

*MSBuild 작업: PropertyListEditorTaskBase*

### <a name="a-namemt7065mt7065-unknown-propertylist-editor-action-"></a><a name="MT7065"/>MT7065: 알 수 없는 PropertyList 편집기 동작: * 합니다.

*MSBuild 작업: PropertyListEditorTaskBase*

### <a name="a-namemt7066mt7066-error-loading--"></a><a name="MT7066"/>MT7066: 로드 오류 ' *': * 합니다.

*MSBuild 작업: PropertyListEditorTaskBase*

### <a name="a-namemt7067mt7067-error-saving--"></a><a name="MT7067"/>MT7067: 오류 절약 ' *': * 합니다.

*MSBuild 작업: PropertyListEditorTaskBase*


## <a name="mt8xxx-runtime-error-messages"></a>MT8xxx: 런타임 오류 메시지

<!--
 MT8xxx runtime
  MT800x misc
  -->

### <a name="a-namemt8001mt8001--version-mismatch-between-the-native-xamarinios-runtime-and-monotouchdll-please-reinstall-xamarinios"></a><a name="MT8001"/>네이티브 Xamarin.iOS 런타임과 monotouch.dll 사이의 MT8001 버전이 일치 하지 않습니다. Xamarin.iOS 다시 설치 하십시오.

### <a name="a-namemt8002mt8002--could-not-find-the-method--in-the-type-"></a><a name="MT8002"/>메서드를 찾지 MT8002 못했습니다 '\*'in '형식\*'.

### <a name="a-namemt8003mt8003--failed-to-find-the-closed-generic-method--on-the-type-"></a><a name="MT8003"/>MT8003 폐쇄형된 제네릭 메서드를 찾지 못했습니다. '\*'유형에'\*'.

### <a name="a-namemt8004mt8004-cannot-create-an-instance-of--for-the-native-object-0x-of-type--because-another-instance-already-exists-for-this-native-object-of-type-"></a><a name="MT8004"/>MT8004:의 인스턴스를 만들 수 * 네이티브 개체 0 x *에 대 한 (형식의 ' *')이 네이티브 개체에 대 한 다른 인스턴스가 이미 있기 때문에, (형식의 *).

### <a name="a-namemt8005mt8005-wrapper-type--is-missing-its-native-objectivec-class-"></a><a name="MT8005"/>MT8005: 래퍼 형식 '\*'네이티브 ObjectiveC 동급 없습니다'\*'.

### <a name="a-namemt8006mt8006-failed-to-find-the-selector--on-the-type-"></a><a name="MT8006"/>MT8006: 선택기를 찾지 못했습니다. '\*'유형에'\*'

### <a name="a-namemt8007mt8007-cannot-get-the-method-descriptor-for-the-selector--on-the-type--because-the-selector-does-not-correspond-to-a-method"></a><a name="MT8007"/>MT8007: 선택기에 대 한 메서드 설명자를 가져올 수 없습니다 '\*'유형에'\*' 선택기는 방법에 해당 하지 않는 때문에

### <a name="a-namemt8008mt8008-the-loaded-version-of-xamariniosdll-was-compiled-for--bits-while-the-process-is--bits-please-file-a-bug-at-httpbugzillaxamarincom"></a><a name="MT8008"/>MT8008: Xamarin.iOS.dll의 로드 된 버전에 대 한 컴파일된 *는 과정은 비트 * 비트입니다. Http://bugzilla.xamarin.com에서 버그를 제출 하세요.

이 빌드 프로세스에서 잘못 된 것을 나타냅니다. 버그를 제출 하세요 [http://bugzilla.xamarin.com](https://bugzilla.xamarin.com/enter_bug.cgi?product=iOS)합니다.

### <a name="a-namemt8009mt8009-unable-to-locate-the-block-to-delegate-conversion-method-for-the-method-s-parameter--please-file-a-bug-at-httpbugzillaxamarincom"></a><a name="MT8009"/>MT8009: 메서드에 대 한 변환 메서드를 위임 하는 블록을 찾을 수 없습니다 *.*' s 매개 변수 # * 합니다. Http://bugzilla.xamarin.com에서 버그를 제출 하세요.

이 API 제대로 연결 되지 않은 것을 나타냅니다. Xamarin에 의해 노출 되는 API 인 경우 하십시오 버그를 보고할 우리의: bugzilla에 ([http://bugzilla.xamarin.com](https://bugzilla.xamarin.com/enter_bug.cgi?product=iOS)) 제 3 자 바인딩이 공급 업체에 문의 하세요.

### <a name="a-namemt8010mt8010-native-type-size-mismatch-between-xamariniosmacdll-and-the-executing-architecture-xamariniosmacdll-was-built-for--bit-while-the-current-process-is--bit"></a><a name="MT8010"/>Xamarin 간의 MT8010: 네이티브 형식 크기 불일치 합니다. [iOS | Mac].dll 및 실행 중인 아키텍처입니다. Xamarin 합니다. [iOS | 용으로 빌드된.dll Mac] *-현재 과정은 비트 *-비트입니다.

이 빌드 프로세스에서 잘못 된 것을 나타냅니다. 버그를 제출 하세요 [http://bugzilla.xamarin.com](https://bugzilla.xamarin.com/enter_bug.cgi?product=iOS)합니다.

### <a name="a-namemt8011mt8011-unable-to-locate-the-delegate-to-block-conversion-attribute-delegateproxy-for-the-return-value-for-the-method--please-file-a-bug-at-httpbugzillaxamarincom"></a><a name="MT8011"/>MT8011: 메서드에 대 한 반환 값에 대 한 대리자 블록 변환 특성 ([DelegateProxy])를 찾을 수 없습니다 *.*합니다. Http://bugzilla.xamarin.com에서 버그를 제출 하세요.

Xamarin.iOS (변환할 대리자를 블록)는 런타임 시 필요한 메서드를 찾을 수 없습니다.

이것은 보통 Xamarin.iOS;의 버그를 나타냅니다. 버그를 제출 하세요 [http://bugzilla.xamarin.com](https://bugzilla.xamarin.com/enter_bug.cgi?product=iOS)합니다.

### <a name="a-namemt8012mt8012-invalid-delegateproxyattribute-for-the-return-value-for-the-method--delegatetype-is-null-please-file-a-bug-at-httpbugzillaxamarincom"></a><a name="MT8012"/>MT8012: 메서드에 대 한 반환 값에 대 한 잘못 된 DelegateProxyAttribute *.*: DelegateType null입니다. Http://bugzilla.xamarin.com에서 버그를 제출 하세요.

해당 메서드에 대 한 DelegateProxy 특성이 올바르지 않습니다.

이것은 보통 Xamarin.iOS;의 버그를 나타냅니다. 버그를 제출 하세요 [http://bugzilla.xamarin.com](https://bugzilla.xamarin.com/enter_bug.cgi?product=iOS)합니다.

### <a name="a-namemt8013mt8013-invalid-delegateproxyattribute-for-the-return-value-for-the-method--delegatetype-2-specifies-a-type-without-a-handler-field-please-file-a-bug-at-httpbugzillaxamarincom"></a><a name="MT8013"/>MT8013: 메서드에 대 한 반환 값에 대 한 잘못 된 DelegateProxyAttribute *.*: DelegateType ({2 \}) 'Handler' 필드 없는 형식을 지정 합니다. Http://bugzilla.xamarin.com에서 버그를 제출 하세요.

해당 메서드에 대 한 DelegateProxy 특성이 올바르지 않습니다.

이것은 보통 Xamarin.iOS;의 버그를 나타냅니다. 버그를 제출 하세요 [http://bugzilla.xamarin.com](https://bugzilla.xamarin.com/enter_bug.cgi?product=iOS)합니다.

### <a name="a-namemt8014mt8014-invalid-delegateproxyattribute-for-the-return-value-for-the-method--the-delegatetypes-2-handler-field-is-null-please-file-a-bug-at-httpbugzillaxamarincom"></a><a name="MT8014"/>MT8014: 메서드에 대 한 반환 값에 대 한 잘못 된 DelegateProxyAttribute *.*: The DelegateType의 ({2 \}) 'Handler' 필드가 null입니다. Http://bugzilla.xamarin.com에서 버그를 제출 하세요.

해당 메서드에 대 한 DelegateProxy 특성이 올바르지 않습니다.

이것은 보통 Xamarin.iOS;의 버그를 나타냅니다. 버그를 제출 하세요 [http://bugzilla.xamarin.com](https://bugzilla.xamarin.com/enter_bug.cgi?product=iOS)합니다.

### <a name="a-namemt8015mt8015-invalid-delegateproxyattribute-for-the-return-value-for-the-method--the-delegatetypes-2-handler-field-is-not-a-delegate-its-a--please-file-a-bug-at-httpbugzillaxamarincom"></a><a name="MT8015"/>MT8015: 메서드에 대 한 반환 값에 대 한 잘못 된 DelegateProxyAttribute *.*: The DelegateType의 ({2 \}) 'Handler' 필드 대리자가 아닌, 이기는 *입니다. Http://bugzilla.xamarin.com에서 버그를 제출 하세요.

해당 메서드에 대 한 DelegateProxy 특성이 올바르지 않습니다.

이것은 보통 Xamarin.iOS;의 버그를 나타냅니다. 버그를 제출 하세요 [http://bugzilla.xamarin.com](https://bugzilla.xamarin.com/enter_bug.cgi?product=iOS)합니다.

### <a name="a-namemt8016mt8016-unable-to-convert-delegate-to-block-for-the-return-value-for-the-method--because-the-input-isnt-a-delegate-its-a--please-file-a-bug-at-httpbugzillaxamarincom"></a><a name="MT8016"/>MT8016: 대리자는 메서드에 대 한 반환 값에 대 한 차단를 변환할 수 없습니다 *.*입력 대리자, 아니어서, 이기는 * 합니다. Http://bugzilla.xamarin.com에서 버그를 제출 하세요.

해당 메서드에 대 한 DelegateProxy 특성이 올바르지 않습니다.

이것은 보통 Xamarin.iOS;의 버그를 나타냅니다. 버그를 제출 하세요 [http://bugzilla.xamarin.com](https://bugzilla.xamarin.com/enter_bug.cgi?product=iOS)합니다.

<!-- 8017 is used by mmp -->

### <a name="a-namemt8018mt8018-internal-consistency-error-please-file-a-bug-report-at-httpbugzillaxamarincom"></a><a name="MT8018"/>MT8018: 내부 일관성 오류가 발생 했습니다. Http://bugzilla.xamarin.com에 버그 보고서를 제출 하세요.

Xamarin.iOS에서 버그를 나타냅니다. 버그를 제출 하세요 [http://bugzilla.xamarin.com](https://bugzilla.xamarin.com/enter_bug.cgi?product=iOS)합니다.

### <a name="a-namemt8019mt8019-could-not-find-the-assembly--in-the-loaded-assemblies"></a><a name="MT8019"/>MT8019: 어셈블리를 찾을 수 없습니다 * 로드 된 어셈블리에 있습니다.

Xamarin.iOS에서 버그를 나타냅니다. 버그를 제출 하세요 [http://bugzilla.xamarin.com](https://bugzilla.xamarin.com/enter_bug.cgi?product=iOS)합니다.

### <a name="a-namemt8020mt8020-could-not-find-the-module-with-metadatatoken--in-the-assembly-"></a><a name="MT8020"/>MT8020: MetadataToken 사용 하 여 모듈을 찾을 수 없습니다 * 어셈블리에서 *.

Xamarin.iOS에서 버그를 나타냅니다. 버그를 제출 하세요 [http://bugzilla.xamarin.com](https://bugzilla.xamarin.com/enter_bug.cgi?product=iOS)합니다.

### <a name="a-namemt8021mt8021-unknown-implicit-token-type-"></a><a name="MT8021"/>MT8021: 알 수 없는 암시적 토큰 유형이: * 합니다.

Xamarin.iOS에서 버그를 나타냅니다. 버그를 제출 하세요 [http://bugzilla.xamarin.com](https://bugzilla.xamarin.com/enter_bug.cgi?product=iOS)합니다.

### <a name="a-namemt8022mt8022-expected-the-token-reference--to-be-a--but-its-a--please-file-a-bug-report-at-httpbugzillaxamarincom"></a><a name="MT8022"/>MT8022: 예상 토큰 참조 * 되도록는 *, 이지만 *입니다. Http://bugzilla.xamarin.com에 버그 보고서를 제출 하세요.

Xamarin.iOS에서 버그를 나타냅니다. 버그를 제출 하세요 [http://bugzilla.xamarin.com](https://bugzilla.xamarin.com/enter_bug.cgi?product=iOS)합니다.

### <a name="a-namemt8023mt8023-an-instance-object-is-required-to-construct-a-closed-generic-method-for-the-open-generic-method--token-reference--please-file-a-bug-report-at-httpbugzillaxamarincom"></a><a name="MT8023"/>MT8023:는 인스턴스 개체 폐쇄형된 제네릭 메서드가 개방형 제네릭 메서드의 만드는 데 필요한: * (참조 토큰: *). Http://bugzilla.xamarin.com에 버그 보고서를 제출 하세요.

Xamarin.iOS에서 버그를 나타냅니다. 버그를 제출 하세요 [http://bugzilla.xamarin.com](https://bugzilla.xamarin.com/enter_bug.cgi?product=iOS)합니다.