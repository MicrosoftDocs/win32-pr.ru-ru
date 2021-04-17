---
title: VIEW. Тимеринтервал
description: Атрибут Тимеринтервал указывает или получает интервал (в миллисекундах), в течение которого таймер запускает события в обработчик событий OnTime.
ms.assetid: 1a69890f-5ea4-493a-8a9e-04fe60a41804
keywords:
- Просмотреть. Тимеринтервал проигрыватель Windows Media
topic_type:
- apiref
api_name:
- VIEW.timerInterval
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 790c95fbb2cded134222271d04c4c37dae412b8d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105717792"
---
# <a name="viewtimerinterval"></a><span data-ttu-id="da0e4-104">VIEW. Тимеринтервал</span><span class="sxs-lookup"><span data-stu-id="da0e4-104">VIEW.timerInterval</span></span>

<span data-ttu-id="da0e4-105">Атрибут **тимеринтервал** указывает или получает интервал (в миллисекундах), в течение которого таймер запускает события в обработчик событий **OnTime** .</span><span class="sxs-lookup"><span data-stu-id="da0e4-105">The **timerInterval** attribute specifies or retrieves the interval, in milliseconds, at which the timer fires events to the **ontimer** event handler.</span></span>

``` syntax
        elementID.timerInterval
```

## <a name="possible-values"></a><span data-ttu-id="da0e4-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="da0e4-106">Possible Values</span></span>

<span data-ttu-id="da0e4-107">Этот атрибут имеет **номер** для чтения и записи (**длинный**) со значением по умолчанию 1000.</span><span class="sxs-lookup"><span data-stu-id="da0e4-107">This attribute is a read/write **Number** (**long**) with a default value of 1000.</span></span>



| <span data-ttu-id="da0e4-108">Значение</span><span class="sxs-lookup"><span data-stu-id="da0e4-108">Value</span></span>        | <span data-ttu-id="da0e4-109">Описание</span><span class="sxs-lookup"><span data-stu-id="da0e4-109">Description</span></span>                    |
|--------------|--------------------------------|
| <span data-ttu-id="da0e4-110">0</span><span class="sxs-lookup"><span data-stu-id="da0e4-110">0</span></span>            | <span data-ttu-id="da0e4-111">Событие Timer не срабатывает.</span><span class="sxs-lookup"><span data-stu-id="da0e4-111">The timer event does not fire.</span></span> |
| <span data-ttu-id="da0e4-112">50 и старше</span><span class="sxs-lookup"><span data-stu-id="da0e4-112">50 and above</span></span> | <span data-ttu-id="da0e4-113">Интервал в миллисекундах.</span><span class="sxs-lookup"><span data-stu-id="da0e4-113">The interval in milliseconds.</span></span>  |



 

<span data-ttu-id="da0e4-114">Любое значение ниже 50 (включая отрицательные числа, но не включая ноль) приводит к ошибке, а предыдущее значение сохраняется.</span><span class="sxs-lookup"><span data-stu-id="da0e4-114">Any value below 50 (including negative numbers, but not including zero) generates an error and the previous value is maintained.</span></span>

## <a name="remarks"></a><span data-ttu-id="da0e4-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="da0e4-115">Remarks</span></span>

<span data-ttu-id="da0e4-116">Это не будет срабатывать автоматически, если не реализован обработчик событий OnTime **time** .</span><span class="sxs-lookup"><span data-stu-id="da0e4-116">This will not fire automatically if no **ontimer** event handler is implemented.</span></span> <span data-ttu-id="da0e4-117">Поэтому производительность не снижается, несмотря на то, что значение по умолчанию не равно нулю.</span><span class="sxs-lookup"><span data-stu-id="da0e4-117">Thus there is no performance degradation even though the default value is nonzero.</span></span>

## <a name="requirements"></a><span data-ttu-id="da0e4-118">Требования</span><span class="sxs-lookup"><span data-stu-id="da0e4-118">Requirements</span></span>



| <span data-ttu-id="da0e4-119">Требование</span><span class="sxs-lookup"><span data-stu-id="da0e4-119">Requirement</span></span> | <span data-ttu-id="da0e4-120">Значение</span><span class="sxs-lookup"><span data-stu-id="da0e4-120">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="da0e4-121">Версия</span><span class="sxs-lookup"><span data-stu-id="da0e4-121">Version</span></span><br/> | <span data-ttu-id="da0e4-122">Проигрыватель Windows Media версии 7,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="da0e4-122">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="da0e4-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="da0e4-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da0e4-124">**VIEW, элемент**</span><span class="sxs-lookup"><span data-stu-id="da0e4-124">**VIEW Element**</span></span>](view-element.md)
</dt> <dt>

[<span data-ttu-id="da0e4-125">**Просмотр. OnTime**</span><span class="sxs-lookup"><span data-stu-id="da0e4-125">**VIEW.ontimer**</span></span>](view-ontimer.md)
</dt> </dl>

 

 





