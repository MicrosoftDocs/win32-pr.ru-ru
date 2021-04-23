---
title: Жетпоситионинформатионоператион. results, метод
description: Возвращает результаты асинхронной операции, запущенной Жетпоситионинформатионасинк.
ms.assetid: 1DC7CD65-1F0F-44A5-9836-C77A5C23F91E
keywords:
- API потоковой передачи мультимедиа метода
- API потоковой передачи мультимедиа, интерфейс Жетпоситионинформатионоператион
- API потоковой передачи мультимедиа интерфейса Жетпоситионинформатионоператион, метод Results
topic_type:
- apiref
api_name:
- GetPositionInformationOperation.GetResults
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7a0b4311c3be814a73ddb1e2a9b18d8e19aea9ee
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103791220"
---
# <a name="getpositioninformationoperationgetresults-method"></a><span data-ttu-id="32d0d-106">Жетпоситионинформатионоператион. results, метод</span><span class="sxs-lookup"><span data-stu-id="32d0d-106">GetPositionInformationOperation.GetResults method</span></span>

<span data-ttu-id="32d0d-107">Возвращает результаты асинхронной операции, запущенной [**жетпоситионинформатионасинк**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getpositioninformationasync).</span><span class="sxs-lookup"><span data-stu-id="32d0d-107">Returns the results of the asynchronous operation started by [**GetPositionInformationAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getpositioninformationasync).</span></span>

## <a name="syntax"></a><span data-ttu-id="32d0d-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="32d0d-108">Syntax</span></span>


```C++
HRESULT GetResults(
  [out, retval] PositionInformation *value
);
```



## <a name="parameters"></a><span data-ttu-id="32d0d-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="32d0d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32d0d-110">*значение* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="32d0d-110">*value* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="32d0d-111">Ссылка на структуру [**поситионинформатион**](/previous-versions/windows/desktop/api/windows.media.streaming/ns-windows-media-streaming-positioninformation) , которая содержит результаты операции.</span><span class="sxs-lookup"><span data-stu-id="32d0d-111">A reference to a [**PositionInformation**](/previous-versions/windows/desktop/api/windows.media.streaming/ns-windows-media-streaming-positioninformation) structure that contains the results of the operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32d0d-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="32d0d-112">Return value</span></span>

<span data-ttu-id="32d0d-113">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="32d0d-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="32d0d-114">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="32d0d-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="32d0d-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="32d0d-115">Return code</span></span>                                                                          | <span data-ttu-id="32d0d-116">Описание</span><span class="sxs-lookup"><span data-stu-id="32d0d-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="32d0d-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="32d0d-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="32d0d-118">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="32d0d-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="32d0d-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="32d0d-119">Remarks</span></span>

<span data-ttu-id="32d0d-120">Метод " **Results** " обычно вызывается из обработчика событий, зарегистрированного путем установки свойства [**Completed**](getpositioninformationoperation-completed.md) .</span><span class="sxs-lookup"><span data-stu-id="32d0d-120">The **GetResults** method is typically called from the event handler that was registered by setting the [**Completed**](getpositioninformationoperation-completed.md) property.</span></span>

## <a name="see-also"></a><span data-ttu-id="32d0d-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="32d0d-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32d0d-122">**жетпоситионинформатионоператион**</span><span class="sxs-lookup"><span data-stu-id="32d0d-122">**GetPositionInformationOperation**</span></span>](getpositioninformationoperation.md)
</dt> </dl>

 

