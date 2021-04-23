---
title: Жетволумеоператион. results, метод
description: Возвращает результаты асинхронной операции, запущенной Жетволумеасинк.
ms.assetid: 71DC4D76-4CC2-4D40-960F-AF56E1F33557
keywords:
- API потоковой передачи мультимедиа метода
- API потоковой передачи мультимедиа, интерфейс Жетволумеоператион
- API потоковой передачи мультимедиа интерфейса Жетволумеоператион, метод Results
topic_type:
- apiref
api_name:
- GetVolumeOperation.GetResults
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 444eaf590e5afc5d4f5185bcd3793698d6fe4535
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "105700861"
---
# <a name="getvolumeoperationgetresults-method"></a><span data-ttu-id="451d8-106">Жетволумеоператион. results, метод</span><span class="sxs-lookup"><span data-stu-id="451d8-106">GetVolumeOperation.GetResults method</span></span>

<span data-ttu-id="451d8-107">Возвращает результаты асинхронной операции, запущенной [**жетволумеасинк**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getvolumeasync).</span><span class="sxs-lookup"><span data-stu-id="451d8-107">Returns the results of the asynchronous operation started by [**GetVolumeAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getvolumeasync).</span></span>

## <a name="syntax"></a><span data-ttu-id="451d8-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="451d8-108">Syntax</span></span>


```C++
HRESULT GetResults(
  [out, retval] UINT32 *value
);
```



## <a name="parameters"></a><span data-ttu-id="451d8-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="451d8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="451d8-110">*значение* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="451d8-110">*value* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="451d8-111">Том.</span><span class="sxs-lookup"><span data-stu-id="451d8-111">The volume.</span></span> <span data-ttu-id="451d8-112">Значение от 0 до 100.</span><span class="sxs-lookup"><span data-stu-id="451d8-112">A value between 0 and 100.</span></span> <span data-ttu-id="451d8-113">0 указывает на минимальный том, а 100 — на максимальный.</span><span class="sxs-lookup"><span data-stu-id="451d8-113">0 indicates minimum volume, and 100 indicates maximum volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="451d8-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="451d8-114">Return value</span></span>

<span data-ttu-id="451d8-115">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="451d8-115">The method returns an **HRESULT**.</span></span> <span data-ttu-id="451d8-116">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="451d8-116">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="451d8-117">Код возврата</span><span class="sxs-lookup"><span data-stu-id="451d8-117">Return code</span></span>                                                                          | <span data-ttu-id="451d8-118">Описание</span><span class="sxs-lookup"><span data-stu-id="451d8-118">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="451d8-119"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="451d8-119"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="451d8-120">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="451d8-120">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="451d8-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="451d8-121">Remarks</span></span>

<span data-ttu-id="451d8-122">Метод " **Results** " обычно вызывается из обработчика событий, зарегистрированного путем установки свойства [**Completed**](getvolumeoperation-completed.md) .</span><span class="sxs-lookup"><span data-stu-id="451d8-122">The **GetResults** method is typically called from the event handler that was registered by setting the [**Completed**](getvolumeoperation-completed.md) property.</span></span>

## <a name="see-also"></a><span data-ttu-id="451d8-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="451d8-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="451d8-124">**жетволумеоператион**</span><span class="sxs-lookup"><span data-stu-id="451d8-124">**GetVolumeOperation**</span></span>](getvolumeoperation.md)
</dt> </dl>

 

