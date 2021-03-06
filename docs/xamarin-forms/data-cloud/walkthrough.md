---
title: 이 샘플 이해
description: 이 항목에서는 다른 웹 서비스와 통신 하는 방법을 보여 주는 Xamarin.Forms 샘플 응용 프로그램의 연습을 제공 합니다. 각 웹 서비스 응용 프로그램을 별도 예제를 사용 하는 동안은 기능적으로 비슷하지만 하 고 일반 클래스를 공유 합니다.
ms.prod: xamarin
ms.assetid: A3FEB262-0D79-42E6-8F8B-A565618C490B
ms.technology: xamarin-forms
author: davidbritch
ms.author: dabritch
ms.date: 02/28/2017
ms.openlocfilehash: d10bdc605fca199a4d0286ce662a27094b5b98f4
ms.sourcegitcommit: d80d93957040a14b4638a91b0eac797cfaade840
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/07/2018
ms.locfileid: "34847568"
---
# <a name="understanding-the-sample"></a>이 샘플 이해

_이 항목에서는 다른 웹 서비스와 통신 하는 방법을 보여 주는 Xamarin.Forms 샘플 응용 프로그램의 연습을 제공 합니다. 각 웹 서비스 응용 프로그램을 별도 예제를 사용 하는 동안은 기능적으로 비슷하지만 하 고 일반 클래스를 공유 합니다._

샘플 할 일 목록 응용 프로그램 아래에 설명 된 다양 한 유형의 Xamarin.Forms 사용한 웹 서비스 백 엔드를 액세스 하는 방법을 보여 주기 위해 사용 됩니다. 기능을을 제공합니다.

- 작업 목록을 봅니다.
- 추가, 편집 및 작업을 삭제 합니다.
- '완료'에 작업의 상태를 설정 합니다.
- 작업의 이름 및 정보 필드를 말하십시오.

모든 경우에는 작업은 웹 서비스를 통해 액세스 되는 백 엔드에 저장 됩니다.

응용 프로그램을 시작할 때 웹 서비스에서 검색 된 모든 작업을 나열 하 고 새 작업을 만들 수 있도록 하는 페이지가 표시 됩니다. 작업을 클릭 하면 응용 프로그램에 있는 작업 편집, 저장, 삭제 및 수 발음 두 번째 페이지를 이동 합니다. 최종 응용 프로그램은 다음과 같습니다.

![](walkthrough-images/app-example-1.png "Todo 응용 프로그램-첫 페이지")
![](walkthrough-images/app-example-2.png "Todo 응용 프로그램-두 번째 페이지")

이 가이드의 각 항목에 대 한 다운로드 링크를 제공는 *다른* 는 특정 유형의 웹 서비스 백 엔드를 보여 주는 응용 프로그램의 버전입니다. 각 웹 서비스 스타일에 관련 된 페이지에서 관련 샘플 코드를 다운로드 합니다.

## <a name="understanding-the-application-anatomy"></a>응용 프로그램 분석 이해

각 샘플 응용 프로그램에 대 한 PCL 프로젝트 세 개의 주 폴더가 이루어져 있습니다.

|폴더|용도|
|--- |--- |
|데이터|클래스 및 데이터 항목을 관리 하 고 웹 서비스와 통신 하는 데 사용 되는 인터페이스를 포함 합니다. 여기에 최소한은 `TodoItemManager` 클래스의 속성을 통해 노출 되는 `App` 웹 서비스 작업을 호출 하는 클래스입니다.|
|모델|응용 프로그램에 대 한 데이터 모델 클래스를 포함합니다. 여기에 최소한의 `TodoItem` 응용 프로그램에서 사용 되는 데이터의 단일 항목을 모델링 하는 클래스입니다. 폴더는 사용자 데이터를 모델에 사용 되는 모든 추가 클래스를 포함할 수도 있습니다.|
|보기|응용 프로그램 페이지가 포함 됩니다. 일반적으로 이루어져이 `TodoListPage` 및 `TodoItemPage` 클래스 및 인증을 위해 사용 되는 모든 추가 클래스입니다.|

또한 각 응용 프로그램에 대 한 PCL 프로젝트 다양 한 중요 한 파일 구성 됩니다.

|파일|용도|
|--- |--- |
|Constants.cs|`Constants` 웹 서비스와 통신 하는 응용 프로그램에서 사용 하는 모든 상수를 지정 하는 클래스입니다. 이러한 상수는 공급자에 대해 만든 개인 백 엔드 서비스에 액세스 하려면 업데이트 해야 합니다.|
|ITextToSpeech.cs|`ITextToSpeech` 인터페이스를 지정 하는 `Speak` 모든 구현 클래스에서 메서드를 제공 해야 합니다.|
|Todo.cs|`App` 모두 첫 번째 페이지에서 각 플랫폼에 응용 프로그램에 의해 표시 되는 인스턴스화를 담당 하는 클래스 및 `TodoItemManager` 웹 서비스 작업을 호출 하는 데 사용 되는 클래스입니다.|

### <a name="viewing-pages"></a>페이지 보기

대부분의 샘플 응용 프로그램에 최소한 두 페이지가 포함 되어 있습니다.

- **TodoListPage** –이 페이지의 목록이 표시 됩니다. `TodoItem` 인스턴스 및 확인 아이콘 경우는 `TodoItem.Done` 속성은 `true`합니다. 항목을 클릭 하면로 이동는 `TodoItemPage`합니다. 또한,를 클릭 하 여 새 항목을 만들 수 수는 *+* 기호입니다.
- **TodoItemPage** – 선택한 항목에 대 한 세부 정보를 표시 하는이 페이지 `TodoItem`, 편집, 저장, 삭제 및 읽을 수 있게 합니다.

또한 일부 샘플 응용 프로그램 사용자 인증 프로세스를 관리 하는 데 사용 되는 추가 페이지를 포함 합니다.

### <a name="modeling-the-data"></a>데이터 모델링

각 예제 응용 프로그램 사용은 `TodoItem` 표시 되며 저장소에 대 한 웹 서비스로 전송 된 데이터를 모델링 하는 클래스입니다. 다음 코드 예제는 `TodoItem` 클래스를 보여줍니다.

```csharp
public class TodoItem
{
    public string ID { get; set; }
    public string Name { get; set; }
    public string Notes { get; set; }
    public bool Done { get; set; }
}
```

`ID` 속성은 각 고유 하 게 식별 하는 데 사용 `TodoItem` 인스턴스를 선택한 각 웹 서비스에 의해 업데이트 되거나 삭제 될 데이터를 식별 하는 데 사용 됩니다.

### <a name="invoking-web-service-operations"></a>웹 서비스 작업 호출

웹 서비스 작업을 통해 액세스 되는 `TodoItemManager` 클래스 및 클래스의 인스턴스를 통해 액세스할 수는 `App.TodoManager` 속성입니다. `TodoItemManager` 클래스 웹 서비스 작업을 호출 하려면 다음 메서드를 제공 합니다.

- **GetTasksAsync** –이 메서드는 채우는 데는 `ListView` 에서 제어는 `TodoListPage` 와 `TodoItem` 웹 서비스에서 검색 된 인스턴스.
- **SaveTaskAsync** –이 메서드는 만들기 또는 업데이트 하는 데 사용 되는 `TodoItem` 웹 서비스에서 인스턴스.
- **DeleteTaskAsync** –이 메서드는 삭제 하는 데 사용 되는 `TodoItem` 웹 서비스에서 인스턴스.

일부 샘플 응용 프로그램에 추가 메서드를 포함 하는 또한는 `TodoItemManager` 클래스는 사용자 인증 프로세스를 관리 하는 데 사용 됩니다.

웹 서비스 작업을 직접 호출 하지 않고는 `TodoItemManager` 에 삽입 하는 종속 클래스에서 메서드를 호출 하는 메서드는 `TodoItemManager` 생성자입니다. 샘플 응용 프로그램 하나를 삽입 합니다. 예를 들어는 `RestService` 클래스에 `TodoItemManager` REST Api를 사용 하 여 데이터에 액세스 하는 구현을 제공 하는 생성자입니다.

### <a name="translating-text-to-speech"></a>Text to Speech 변환

대부분의 샘플 응용 프로그램으로 언급 해야 할 값의 텍스트 음성 변환 (TTS) 기능이 포함 된 `TodoItem.Name` 및 `TodoItem.Notes` 속성입니다. 이렇게는 `OnSpeakActivated` 의 이벤트 처리기는 `TodoItemPage` 다음 코드 예제와 같이 클래스:

```csharp
void OnSpeakActivated (object sender, EventArgs e)
{
    var todoItem = (TodoItem)BindingContext;
    App.Speech.Speak(todoItem.Name + " " + todoItem.Notes);
}
```

이 메서드를 호출 하기만 `Speak` 플랫폼 관련에서 구현 되는 메서드 `Speech` 클래스입니다. 각 `Speech` 클래스 구현은 `ITextToSpeech` 인터페이스 및 플랫폼별 시작 코드의 인스턴스를 만듭니다는 `Speech` 를 통해 액세스할 수 있는 클래스는 `App.Speech` 속성입니다.

## <a name="summary"></a>요약

이 항목 다른 웹 서비스와 통신 하는 방법을 보여 주기 위해 사용 되는 Xamarin.Forms 샘플 응용 프로그램의 연습을 제공 합니다. 각 웹 서비스 응용 프로그램을 별도 예제를 사용 하는 동안 모든 과정에 기반 하는 동일한 사용자 인터페이스 및 비즈니스 논리 위에 설명 된 대로-만 웹 서비스가 데이터 저장소 메커니즘은 다른입니다.


## <a name="related-links"></a>관련 링크

- [ASMX 버전 (샘플)](https://developer.xamarin.com/samples/xamarin-forms/WebServices/TodoASMX)
- [WCF 버전 (샘플)](https://developer.xamarin.com/samples/xamarin-forms/WebServices/TodoWCF)
- [REST 버전 (샘플)](https://developer.xamarin.com/samples/xamarin-forms/WebServices/TodoREST)
- [Azure 버전 (샘플)](https://developer.xamarin.com/samples/xamarin-forms/WebServices/TodoAzure)
