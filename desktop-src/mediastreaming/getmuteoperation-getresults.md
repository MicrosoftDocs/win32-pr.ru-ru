---
title: Жетмутеоператион. results, метод
description: Возвращает результаты асинхронной операции, запущенной Жетмутеасинк.
ms.assetid: 5B6DB1B3-54D4-486D-AA03-5FEEC92304B0
keywords:
- API потоковой передачи мультимедиа метода
- API потоковой передачи мультимедиа, интерфейс Жетмутеоператион
- API потоковой передачи мультимедиа интерфейса Жетмутеоператион, метод Results
topic_type:
- apiref
api_name:
- GetMuteOperation.GetResults
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 33c43dc7fee228b1808ff4f607ee6a72faf1e770
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104133747"
---
# <a name="getmuteoperationgetresults-method"></a><span data-ttu-id="1c70d-106">Жетмутеоператион. results, метод</span><span class="sxs-lookup"><span data-stu-id="1c70d-106">GetMuteOperation.GetResults method</span></span>

<span data-ttu-id="1c70d-107">Возвращает результаты асинхронной операции, запущенной [**жетмутеасинк**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getmuteasync).</span><span class="sxs-lookup"><span data-stu-id="1c70d-107">Returns the results of the asynchronous operation started by [**GetMuteAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getmuteasync).</span></span>

## <a name="syntax"></a><span data-ttu-id="1c70d-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1c70d-108">Syntax</span></span>


```C++
HRESULT GetResults(
  [out, retval] boolean *value
);
```



## <a name="parameters"></a><span data-ttu-id="1c70d-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="1c70d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c70d-110">*значение* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="1c70d-110">*value* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="1c70d-111">Значение выключения.</span><span class="sxs-lookup"><span data-stu-id="1c70d-111">The mute value.</span></span> <span data-ttu-id="1c70d-112">Значение true указывает, что звук в данный момент выключен.</span><span class="sxs-lookup"><span data-stu-id="1c70d-112">A value of true indicates that audio is currently muted.</span></span> <span data-ttu-id="1c70d-113">Значение false указывает, что звук не отключен.</span><span class="sxs-lookup"><span data-stu-id="1c70d-113">A value of false indicates that audio is not muted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c70d-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1c70d-114">Return value</span></span>

<span data-ttu-id="1c70d-115">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="1c70d-115">The method returns an **HRESULT**.</span></span> <span data-ttu-id="1c70d-116">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="1c70d-116">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="1c70d-117">Код возврата</span><span class="sxs-lookup"><span data-stu-id="1c70d-117">Return code</span></span>                                                                          | <span data-ttu-id="1c70d-118">Описание</span><span class="sxs-lookup"><span data-stu-id="1c70d-118">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="1c70d-119"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="1c70d-119"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="1c70d-120">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="1c70d-120">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="1c70d-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1c70d-121">Remarks</span></span>

<span data-ttu-id="1c70d-122">Метод " **Results** " обычно вызывается из обработчика событий, зарегистрированного путем установки свойства [**Completed**](getmuteoperation-completed.md) .</span><span class="sxs-lookup"><span data-stu-id="1c70d-122">The **GetResults** method is typically called from the event handler that was registered by setting the [**Completed**](getmuteoperation-completed.md) property.</span></span>

## <a name="see-also"></a><span data-ttu-id="1c70d-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1c70d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c70d-124">**жетмутеоператион**</span><span class="sxs-lookup"><span data-stu-id="1c70d-124">**GetMuteOperation**</span></span>](getmuteoperation.md)
</dt> </dl>

 

