---
description: Метод отсрочки задает новое время презентации для ранее поставленной в очередь команды.
ms.assetid: 6201eb18-8180-445c-8d29-980511748fe4
title: Метод Кдеферредкомманд. отсрочки (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDeferredCommand.Postpone
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c9ce19c5391541336f52dd872b44bb9f3a447c27
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680081"
---
# <a name="cdeferredcommandpostpone-method"></a><span data-ttu-id="3a1f8-103">Кдеферредкомманд. Отсрочка метода</span><span class="sxs-lookup"><span data-stu-id="3a1f8-103">CDeferredCommand.Postpone method</span></span>

<span data-ttu-id="3a1f8-104">`Postpone`Метод задает новое время презентации для ранее поставленной в очередь команды.</span><span class="sxs-lookup"><span data-stu-id="3a1f8-104">The `Postpone` method specifies a new presentation time for a previously queued command.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a1f8-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3a1f8-105">Syntax</span></span>


```C++
HRESULT Postpone(
   REFTIME newtime
);
```



## <a name="parameters"></a><span data-ttu-id="3a1f8-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3a1f8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a1f8-107">*невтиме*</span><span class="sxs-lookup"><span data-stu-id="3a1f8-107">*newtime*</span></span> 
</dt> <dd>

<span data-ttu-id="3a1f8-108">Новое время презентации.</span><span class="sxs-lookup"><span data-stu-id="3a1f8-108">New presentation time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a1f8-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3a1f8-109">Return value</span></span>

<span data-ttu-id="3a1f8-110">Возвращает \_ электронное \_ время \_ VFW \_ , которое уже прошло, если *невтиме* уже передан.</span><span class="sxs-lookup"><span data-stu-id="3a1f8-110">Returns VFW\_E\_TIME\_ALREADY\_PASSED if *newtime* is already passed.</span></span> <span data-ttu-id="3a1f8-111">В противном случае возвращает **значение HRESULT** , полученное в результате вызова метода [**ккмдкуеуе:: reinsert**](ccmdqueue-remove.md) (при извлечении из списка) или [**ккмдкуеуе:: INSERT**](ccmdqueue-insert.md) (при повторной вставке с измененным временем).</span><span class="sxs-lookup"><span data-stu-id="3a1f8-111">Otherwise, returns an **HRESULT** resulting from a call to [**CCmdQueue::Remove**](ccmdqueue-remove.md) (when extracting from the list) or [**CCmdQueue::Insert**](ccmdqueue-insert.md) (when reinserting with the changed time).</span></span>

## <a name="remarks"></a><span data-ttu-id="3a1f8-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3a1f8-112">Remarks</span></span>

<span data-ttu-id="3a1f8-113">Эта функция члена реализует метод [**идеферредкомманд::P остпоне**](/windows/desktop/api/Control/nf-control-ideferredcommand-postpone) .</span><span class="sxs-lookup"><span data-stu-id="3a1f8-113">This member function implements the [**IDeferredCommand::Postpone**](/windows/desktop/api/Control/nf-control-ideferredcommand-postpone) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a1f8-114">Требования</span><span class="sxs-lookup"><span data-stu-id="3a1f8-114">Requirements</span></span>



| <span data-ttu-id="3a1f8-115">Требование</span><span class="sxs-lookup"><span data-stu-id="3a1f8-115">Requirement</span></span> | <span data-ttu-id="3a1f8-116">Значение</span><span class="sxs-lookup"><span data-stu-id="3a1f8-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a1f8-117">Header</span><span class="sxs-lookup"><span data-stu-id="3a1f8-117">Header</span></span><br/>  | <dl> <span data-ttu-id="3a1f8-118"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3a1f8-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="3a1f8-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="3a1f8-119">Library</span></span><br/> | <dl> <span data-ttu-id="3a1f8-120"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="3a1f8-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a1f8-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3a1f8-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a1f8-122">**Класс Кдеферредкомманд**</span><span class="sxs-lookup"><span data-stu-id="3a1f8-122">**CDeferredCommand Class**</span></span>](cdeferredcommand.md)
</dt> </dl>

 

 




