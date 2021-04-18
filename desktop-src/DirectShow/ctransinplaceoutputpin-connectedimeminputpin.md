---
description: 'Метод Коннектедимеминпутпин извлекает указатель на нисходящий входной ПИН-код. Этот метод возвращает переменную члена Кбасеаутпутпин:: m \_ пинпутпин.'
ms.assetid: 39a12603-7768-43c3-9558-7caaa8f55108
title: Ктрансинплацеаутпутпин. Коннектедимеминпутпин, метод (Трансип. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceOutputPin.ConnectedIMemInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 83f92472e67e1d37a51cd2526b8be65ea9bdbc6d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657081"
---
# <a name="ctransinplaceoutputpinconnectedimeminputpin-method"></a><span data-ttu-id="e5e92-104">Ктрансинплацеаутпутпин. Коннектедимеминпутпин, метод</span><span class="sxs-lookup"><span data-stu-id="e5e92-104">CTransInPlaceOutputPin.ConnectedIMemInputPin method</span></span>

<span data-ttu-id="e5e92-105">`ConnectedIMemInputPin`Метод получает указатель на нисходящий входной ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="e5e92-105">The `ConnectedIMemInputPin` method retrieves a pointer to the downstream input pin.</span></span> <span data-ttu-id="e5e92-106">Этот метод возвращает переменную члена [**кбасеаутпутпин:: m \_ пинпутпин**](cbaseoutputpin-m-pinputpin.md) .</span><span class="sxs-lookup"><span data-stu-id="e5e92-106">This method returns the [**CBaseOutputPin::m\_pInputPin**](cbaseoutputpin-m-pinputpin.md) member variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5e92-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e5e92-107">Syntax</span></span>


```C++
IMemInputPin* ConnectedIMemInputPin();
```



## <a name="parameters"></a><span data-ttu-id="e5e92-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="e5e92-108">Parameters</span></span>

<span data-ttu-id="e5e92-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="e5e92-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e5e92-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e5e92-110">Return value</span></span>

<span data-ttu-id="e5e92-111">Возвращает указатель на интерфейс [**имеминпутпин**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) для входного контакта нисходящего входа.</span><span class="sxs-lookup"><span data-stu-id="e5e92-111">Returns a pointer to the [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) interface on the downstream input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5e92-112">Требования</span><span class="sxs-lookup"><span data-stu-id="e5e92-112">Requirements</span></span>



| <span data-ttu-id="e5e92-113">Требование</span><span class="sxs-lookup"><span data-stu-id="e5e92-113">Requirement</span></span> | <span data-ttu-id="e5e92-114">Значение</span><span class="sxs-lookup"><span data-stu-id="e5e92-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5e92-115">Header</span><span class="sxs-lookup"><span data-stu-id="e5e92-115">Header</span></span><br/>  | <dl> <span data-ttu-id="e5e92-116"><dt>Трансип. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e5e92-116"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e5e92-117">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e5e92-117">Library</span></span><br/> | <dl> <span data-ttu-id="e5e92-118"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="e5e92-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5e92-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e5e92-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5e92-120">**Класс Ктрансинплацеаутпутпин**</span><span class="sxs-lookup"><span data-stu-id="e5e92-120">**CTransInPlaceOutputPin Class**</span></span>](ctransinplaceoutputpin.md)
</dt> </dl>

 

 




