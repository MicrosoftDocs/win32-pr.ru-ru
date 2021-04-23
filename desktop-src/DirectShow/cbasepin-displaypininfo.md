---
description: Метод Дисплайпининфо отслеживает подключение ПИН-кода во время отладки.
ms.assetid: 3c1aa5ab-7f6b-4518-abf3-b5138f6267ee
title: Кбасепин. Дисплайпининфо, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.DisplayPinInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ea563ca07eaea6b6974a831726918866414a33b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668772"
---
# <a name="cbasepindisplaypininfo-method"></a><span data-ttu-id="f6628-103">Кбасепин. Дисплайпининфо, метод</span><span class="sxs-lookup"><span data-stu-id="f6628-103">CBasePin.DisplayPinInfo method</span></span>

<span data-ttu-id="f6628-104">`DisplayPinInfo`Метод отслеживает подключение ПИН-кода во время отладки.</span><span class="sxs-lookup"><span data-stu-id="f6628-104">The `DisplayPinInfo` method traces a pin connection during debugging.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6628-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f6628-105">Syntax</span></span>


```C++
void DisplayPinInfo(
   IPin *pReceivePin
);
```



## <a name="parameters"></a><span data-ttu-id="f6628-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f6628-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6628-107">*прецеивепин*</span><span class="sxs-lookup"><span data-stu-id="f6628-107">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="f6628-108">Указатель на принимающий ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="f6628-108">Pointer to the receiving pin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f6628-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f6628-109">Return value</span></span>

<span data-ttu-id="f6628-110">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="f6628-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f6628-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f6628-111">Remarks</span></span>

<span data-ttu-id="f6628-112">В отладочных сборках этот метод вызывает функцию [**дбглог**](dbglog.md) для трассировки попытки соединения.</span><span class="sxs-lookup"><span data-stu-id="f6628-112">In debug builds, this method calls the [**DbgLog**](dbglog.md) function to trace a connection attempt.</span></span> <span data-ttu-id="f6628-113">В розничных сборках этот метод не выполняет никаких действий.</span><span class="sxs-lookup"><span data-stu-id="f6628-113">In retail builds, this method does nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6628-114">Требования</span><span class="sxs-lookup"><span data-stu-id="f6628-114">Requirements</span></span>



| <span data-ttu-id="f6628-115">Требование</span><span class="sxs-lookup"><span data-stu-id="f6628-115">Requirement</span></span> | <span data-ttu-id="f6628-116">Значение</span><span class="sxs-lookup"><span data-stu-id="f6628-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6628-117">Header</span><span class="sxs-lookup"><span data-stu-id="f6628-117">Header</span></span><br/>  | <dl> <span data-ttu-id="f6628-118"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f6628-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="f6628-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f6628-119">Library</span></span><br/> | <dl> <span data-ttu-id="f6628-120"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="f6628-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f6628-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f6628-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6628-122">**Класс Кбасепин**</span><span class="sxs-lookup"><span data-stu-id="f6628-122">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




