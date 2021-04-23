---
title: Жеттранспортинформатионоператион, метод
description: Возвращает результаты асинхронной операции, запущенной Жеттранспортинформатионасинк.
ms.assetid: 8CC6641E-C1E6-4C64-90EC-4120ECB54135
keywords:
- API потоковой передачи мультимедиа метода
- API потоковой передачи мультимедиа, интерфейс Жеттранспортинформатионоператион
- API потоковой передачи мультимедиа интерфейса Жеттранспортинформатионоператион, метод Results
topic_type:
- apiref
api_name:
- GetTransportInformationOperation.GetResults
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 17f846a5824ed07bcaf849a540429eaabe46f3d2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104412905"
---
# <a name="gettransportinformationoperationgetresults-method"></a><span data-ttu-id="66490-106">Жеттранспортинформатионоператион:: Results, метод</span><span class="sxs-lookup"><span data-stu-id="66490-106">GetTransportInformationOperation::GetResults method</span></span>

<span data-ttu-id="66490-107">Возвращает результаты асинхронной операции, запущенной [**жеттранспортинформатионасинк**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-gettransportinformationasync).</span><span class="sxs-lookup"><span data-stu-id="66490-107">Returns the results of the asynchronous operation started by [**GetTransportInformationAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-gettransportinformationasync).</span></span>

## <a name="syntax"></a><span data-ttu-id="66490-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="66490-108">Syntax</span></span>


```C++
HRESULT GetResults(
  [out, retval] TransportInformation *value
);
```



## <a name="parameters"></a><span data-ttu-id="66490-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="66490-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66490-110">*значение* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="66490-110">*value* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="66490-111">Ссылка на структуру [**транспортинформатион**](/previous-versions/windows/desktop/api/windows.media.streaming/ns-windows-media-streaming-transportinformation) , которая содержит результаты операции.</span><span class="sxs-lookup"><span data-stu-id="66490-111">A reference to a [**TransportInformation**](/previous-versions/windows/desktop/api/windows.media.streaming/ns-windows-media-streaming-transportinformation) structure that contains the results of the operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66490-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="66490-112">Return value</span></span>

<span data-ttu-id="66490-113">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="66490-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="66490-114">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="66490-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="66490-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="66490-115">Return code</span></span>                                                                          | <span data-ttu-id="66490-116">Описание</span><span class="sxs-lookup"><span data-stu-id="66490-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="66490-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="66490-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="66490-118">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="66490-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="66490-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="66490-119">Remarks</span></span>

<span data-ttu-id="66490-120">Метод " **Results** " обычно вызывается из обработчика событий, зарегистрированного путем установки свойства [**Completed**](gettransportinformationoperation-completed.md) .</span><span class="sxs-lookup"><span data-stu-id="66490-120">The **GetResults** method is typically called from the event handler that was registered by setting the [**Completed**](gettransportinformationoperation-completed.md) property.</span></span>

## <a name="see-also"></a><span data-ttu-id="66490-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="66490-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66490-122">**жеттранспортинформатионоператион**</span><span class="sxs-lookup"><span data-stu-id="66490-122">**GetTransportInformationOperation**</span></span>](gettransportinformationoperation.md)
</dt> </dl>

 

