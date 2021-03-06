---
title: UrhoSharp Mac 지원
description: 이 문서에서는 UrhoSharp에 대 한 macOS 지원을 설명합니다. 프로젝트를 만드는 방법에 설명 하 고 몇 가지 샘플 코드에 대 한 링크를 제공 합니다.
ms.prod: xamarin
ms.assetid: 95FFBD36-14E9-4C17-B1E8-9A04E81E824D
author: charlespetzold
ms.author: chape
ms.date: 03/29/2017
ms.openlocfilehash: aae7b09231ae0e8f88bb9435f50fadd2ff822c1a
ms.sourcegitcommit: ea1dc12a3c2d7322f234997daacbfdb6ad542507
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/05/2018
ms.locfileid: "34783345"
---
# <a name="urhosharp-mac-support"></a>UrhoSharp Mac 지원

_Mac 특정 설정 및 기능_

플랫폼 특정 기능을 활용 하려는 Urho 이식 가능한 클래스 라이브러리는 고 게임 논리를 다양 한 플랫폼 전반에 걸쳐 사용할 동일한 API를 사용 하면 여전히 초기화 해야 Urho 플랫폼 특정 드라이버에서 한 경우에 따라, 장치 .

아래의 페이지 가정 `MyGame` 의 서브 클래스는 `Application` 클래스입니다.

## <a name="macos"></a>macOS

**지원 되는 아키텍처:** x86/x86-64 32 비트 및 64 비트에 대 한 합니다.

## <a name="creating-a-project"></a>프로젝트 만들기

콘솔 프로젝트를 만들고 Urho NuGet 참조를 찾을 수 있는지 자산 (데이터 디렉터리를 포함 하는 디렉터리) 되었는지 확인 합니다.

```csharp
DesktopUrhoInitializer.AssetsDirectory = "../Assets";
new MyGame().Run();
```

## <a name="example"></a>예

[전체 예제](https://github.com/xamarin/urho-samples/tree/master/FeatureSamples/Cocoa)


