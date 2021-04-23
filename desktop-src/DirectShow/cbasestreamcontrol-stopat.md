---
description: 'Метод StopAt информирует ПИН-код, когда следует отказаться от доставки данных. Этот метод реализует метод Иамстреамконтрол:: StopAt.'
ms.assetid: cc9f0fdc-253b-4feb-95ce-56ebc575a49b
title: Метод Кбасестреамконтрол. StopAt (Стрмктл. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl.StopAt
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8e6b794f5f05721f403d943252c2aabd48614519
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105674796"
---
# <a name="cbasestreamcontrolstopat-method"></a><span data-ttu-id="e1c90-104">Кбасестреамконтрол. StopAt, метод</span><span class="sxs-lookup"><span data-stu-id="e1c90-104">CBaseStreamControl.StopAt method</span></span>

<span data-ttu-id="e1c90-105">`StopAt`Метод информирует ПИН-код, когда следует отказаться от доставки данных.</span><span class="sxs-lookup"><span data-stu-id="e1c90-105">The `StopAt` method informs the pin when to stop delivering data.</span></span> <span data-ttu-id="e1c90-106">Этот метод реализует метод [**иамстреамконтрол:: StopAt**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-stopat) .</span><span class="sxs-lookup"><span data-stu-id="e1c90-106">This method implements the [**IAMStreamControl::StopAt**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-stopat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1c90-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e1c90-107">Syntax</span></span>


```C++
HRESULT StopAt(
   const REFERENCE_TIME *ptStop = NULL,
         BOOL           bSendExtra = FALSE,
         DWORD          dwCookie = 0
);
```



## <a name="parameters"></a><span data-ttu-id="e1c90-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="e1c90-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1c90-109">*птстоп*</span><span class="sxs-lookup"><span data-stu-id="e1c90-109">*ptStop*</span></span> 
</dt> <dd>

<span data-ttu-id="e1c90-110">Указатель на значение [**\_ времени ссылки**](reference-time.md) , указывающее, когда ПИН-код должен прекращать доставку данных.</span><span class="sxs-lookup"><span data-stu-id="e1c90-110">Pointer to a [**REFERENCE\_TIME**](reference-time.md) value that specifies when the pin should stop delivering data.</span></span>

</dd> <dt>

<span data-ttu-id="e1c90-111">*бсендекстра*</span><span class="sxs-lookup"><span data-stu-id="e1c90-111">*bSendExtra*</span></span> 
</dt> <dd>

<span data-ttu-id="e1c90-112">Задает логическое значение, указывающее, следует ли отправить дополнительный пример после запланированного времени окончания.</span><span class="sxs-lookup"><span data-stu-id="e1c90-112">Specifies a Boolean value that indicates whether to send an extra sample after the scheduled stop time.</span></span> <span data-ttu-id="e1c90-113">Если **значение — true**, ПИН-код отправляет один дополнительный пример.</span><span class="sxs-lookup"><span data-stu-id="e1c90-113">If **TRUE**, the pin sends one extra sample.</span></span>

</dd> <dt>

<span data-ttu-id="e1c90-114">*двкукие*</span><span class="sxs-lookup"><span data-stu-id="e1c90-114">*dwCookie*</span></span> 
</dt> <dd>

<span data-ttu-id="e1c90-115">Указывает значение для отправки вместе с уведомлением о запуске.</span><span class="sxs-lookup"><span data-stu-id="e1c90-115">Specifies a value to send along with the start notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e1c90-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e1c90-116">Return value</span></span>

<span data-ttu-id="e1c90-117">Возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="e1c90-117">Returns S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1c90-118">Требования</span><span class="sxs-lookup"><span data-stu-id="e1c90-118">Requirements</span></span>



| <span data-ttu-id="e1c90-119">Требование</span><span class="sxs-lookup"><span data-stu-id="e1c90-119">Requirement</span></span> | <span data-ttu-id="e1c90-120">Значение</span><span class="sxs-lookup"><span data-stu-id="e1c90-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1c90-121">Header</span><span class="sxs-lookup"><span data-stu-id="e1c90-121">Header</span></span><br/>  | <dl> <span data-ttu-id="e1c90-122"><dt>Стрмктл. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e1c90-122"><dt>Strmctl.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e1c90-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e1c90-123">Library</span></span><br/> | <dl> <span data-ttu-id="e1c90-124"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="e1c90-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1c90-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e1c90-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1c90-126">**Класс Кбасестреамконтрол**</span><span class="sxs-lookup"><span data-stu-id="e1c90-126">**CBaseStreamControl Class**</span></span>](cbasestreamcontrol.md)
</dt> </dl>

 

 




