---
description: Метод Алтеркуалити уведомляет фильтр о том, что запрошено изменение качества.
ms.assetid: 46743d6b-65cf-4d63-8913-114277d76da4
title: Ктрансформфилтер. Алтеркуалити, метод (Трансфрм. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.AlterQuality
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 592fc67dd5cee5e4f76b8171b6e842532d71371b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657027"
---
# <a name="ctransformfilteralterquality-method"></a><span data-ttu-id="f5155-103">Ктрансформфилтер. Алтеркуалити, метод</span><span class="sxs-lookup"><span data-stu-id="f5155-103">CTransformFilter.AlterQuality method</span></span>

<span data-ttu-id="f5155-104">`AlterQuality`Метод уведомляет фильтр о запросе изменения качества.</span><span class="sxs-lookup"><span data-stu-id="f5155-104">The `AlterQuality` method notifies the filter that a quality change is requested.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5155-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f5155-105">Syntax</span></span>


```C++
virtual HRESULT AlterQuality(
   Quality q
);
```



## <a name="parameters"></a><span data-ttu-id="f5155-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f5155-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5155-107">*формате*</span><span class="sxs-lookup"><span data-stu-id="f5155-107">*q*</span></span> 
</dt> <dd>

<span data-ttu-id="f5155-108">Структура [**качества**](/windows/win32/api/strmif/ns-strmif-quality) , содержащая сообщение контроля качества.</span><span class="sxs-lookup"><span data-stu-id="f5155-108">[**Quality**](/windows/win32/api/strmif/ns-strmif-quality) structure that contains the quality control message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5155-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f5155-109">Return value</span></span>

<span data-ttu-id="f5155-110">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f5155-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="f5155-111">Возможные значения включают в себя, показанные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="f5155-111">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="f5155-112">Код возврата</span><span class="sxs-lookup"><span data-stu-id="f5155-112">Return code</span></span>                                                                             | <span data-ttu-id="f5155-113">Описание</span><span class="sxs-lookup"><span data-stu-id="f5155-113">Description</span></span>                                                                           |
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f5155-114"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="f5155-114"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="f5155-115">Не обрабатывает сообщение качества.</span><span class="sxs-lookup"><span data-stu-id="f5155-115">Did not handle the quality message.</span></span> <span data-ttu-id="f5155-116">Сообщение должно быть передано в поток.</span><span class="sxs-lookup"><span data-stu-id="f5155-116">The message should be passed upstream.</span></span><br/> |
| <dl> <span data-ttu-id="f5155-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="f5155-117"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="f5155-118">Обработано сообщение качества.</span><span class="sxs-lookup"><span data-stu-id="f5155-118">Handled the quality message.</span></span> <span data-ttu-id="f5155-119">Никаких дополнительных действий не требуется.</span><span class="sxs-lookup"><span data-stu-id="f5155-119">No further action is necessary.</span></span><br/>               |



 

## <a name="remarks"></a><span data-ttu-id="f5155-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f5155-120">Remarks</span></span>

<span data-ttu-id="f5155-121">Переопределите этот метод, если фильтр может выполнять контроль качества.</span><span class="sxs-lookup"><span data-stu-id="f5155-121">Override this method if the filter can perform quality control.</span></span> <span data-ttu-id="f5155-122">Дополнительные сведения см. в разделе [Управление качеством](quality-control-management.md).</span><span class="sxs-lookup"><span data-stu-id="f5155-122">For more information, see [Quality-Control Management](quality-control-management.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f5155-123">Требования</span><span class="sxs-lookup"><span data-stu-id="f5155-123">Requirements</span></span>



| <span data-ttu-id="f5155-124">Требование</span><span class="sxs-lookup"><span data-stu-id="f5155-124">Requirement</span></span> | <span data-ttu-id="f5155-125">Значение</span><span class="sxs-lookup"><span data-stu-id="f5155-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5155-126">Header</span><span class="sxs-lookup"><span data-stu-id="f5155-126">Header</span></span><br/>  | <dl> <span data-ttu-id="f5155-127"><dt>Трансфрм. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f5155-127"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="f5155-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f5155-128">Library</span></span><br/> | <dl> <span data-ttu-id="f5155-129"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="f5155-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5155-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f5155-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5155-131">**Класс Ктрансформфилтер**</span><span class="sxs-lookup"><span data-stu-id="f5155-131">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




