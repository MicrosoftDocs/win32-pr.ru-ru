---
description: Указывает, изменился ли объект со времени последнего сохранения в текущем потоке.
ms.assetid: 69840be6-062e-4505-8381-ea04e822c660
title: Метод Кперсистстреам. IsDirty (Пстреам. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.IsDirty
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4f3bc57998b63ece5ca32543fc00d1d3b5b4389b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668669"
---
# <a name="cpersiststreamisdirty-method"></a><span data-ttu-id="8cf64-103">Кперсистстреам. IsDirty, метод</span><span class="sxs-lookup"><span data-stu-id="8cf64-103">CPersistStream.IsDirty method</span></span>

<span data-ttu-id="8cf64-104">Указывает, изменился ли объект со времени последнего сохранения в текущем потоке.</span><span class="sxs-lookup"><span data-stu-id="8cf64-104">Indicates whether the object has changed since it was last saved to its current stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="8cf64-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8cf64-105">Syntax</span></span>


```C++
HRESULT IsDirty();
```



## <a name="parameters"></a><span data-ttu-id="8cf64-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8cf64-106">Parameters</span></span>

<span data-ttu-id="8cf64-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="8cf64-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8cf64-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8cf64-108">Return value</span></span>

<span data-ttu-id="8cf64-109">Возвращает значение \_ ОК, если для фильтра требуется сохранение, и \_ false, если нет необходимости сохранять.</span><span class="sxs-lookup"><span data-stu-id="8cf64-109">Returns S\_OK if the filter needs saving and S\_FALSE if it does not need saving.</span></span>

## <a name="remarks"></a><span data-ttu-id="8cf64-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8cf64-110">Remarks</span></span>

<span data-ttu-id="8cf64-111">Эта функция члена реализует метод **IPersistStream:: IsDirty** .</span><span class="sxs-lookup"><span data-stu-id="8cf64-111">This member function implements the **IPersistStream::IsDirty** method.</span></span>

## <a name="requirements"></a><span data-ttu-id="8cf64-112">Требования</span><span class="sxs-lookup"><span data-stu-id="8cf64-112">Requirements</span></span>



| <span data-ttu-id="8cf64-113">Требование</span><span class="sxs-lookup"><span data-stu-id="8cf64-113">Requirement</span></span> | <span data-ttu-id="8cf64-114">Значение</span><span class="sxs-lookup"><span data-stu-id="8cf64-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8cf64-115">Header</span><span class="sxs-lookup"><span data-stu-id="8cf64-115">Header</span></span><br/>  | <dl> <span data-ttu-id="8cf64-116"><dt>Пстреам. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8cf64-116"><dt>Pstream.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="8cf64-117">Библиотека</span><span class="sxs-lookup"><span data-stu-id="8cf64-117">Library</span></span><br/> | <dl> <span data-ttu-id="8cf64-118"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="8cf64-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8cf64-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8cf64-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8cf64-120">**Класс Кперсистстреам**</span><span class="sxs-lookup"><span data-stu-id="8cf64-120">**CPersistStream Class**</span></span>](cpersiststream.md)
</dt> </dl>

 

 




