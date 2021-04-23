---
description: 'Метод Куерипининфо извлекает сведения о ПИН-коде. Этот метод реализует метод Ипин:: Куерипининфо.'
ms.assetid: 9de41f61-9f03-4594-a320-2f7f0ed734fd
title: Кбасепин. Куерипининфо, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.QueryPinInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f69977a15deb7d84b3370bb6e08c02a4e5129212
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668543"
---
# <a name="cbasepinquerypininfo-method"></a><span data-ttu-id="6af8c-104">Кбасепин. Куерипининфо, метод</span><span class="sxs-lookup"><span data-stu-id="6af8c-104">CBasePin.QueryPinInfo method</span></span>

<span data-ttu-id="6af8c-105">`QueryPinInfo`Метод получает сведения о ПИН-коде.</span><span class="sxs-lookup"><span data-stu-id="6af8c-105">The `QueryPinInfo` method retrieves information about the pin.</span></span> <span data-ttu-id="6af8c-106">Этот метод реализует метод [**Ипин:: куерипининфо**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) .</span><span class="sxs-lookup"><span data-stu-id="6af8c-106">This method implements the [**IPin::QueryPinInfo**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="6af8c-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6af8c-107">Syntax</span></span>


```C++
HRESULT QueryPinInfo(
   PIN_INFO *pInfo
);
```



## <a name="parameters"></a><span data-ttu-id="6af8c-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="6af8c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6af8c-109">*пинфо*</span><span class="sxs-lookup"><span data-stu-id="6af8c-109">*pInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="6af8c-110">Указатель на [**\_ информационную структуру ПИН-**](/windows/win32/api/strmif/ns-strmif-pin_info) кода, который получает сведения о ПИН-коде.</span><span class="sxs-lookup"><span data-stu-id="6af8c-110">Pointer to a [**PIN\_INFO**](/windows/win32/api/strmif/ns-strmif-pin_info) structure that receives the pin information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6af8c-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6af8c-111">Return value</span></span>

<span data-ttu-id="6af8c-112">Возвращает значение S \_ (ОК) или \_ указатель E.</span><span class="sxs-lookup"><span data-stu-id="6af8c-112">Returns S\_OK or E\_POINTER.</span></span>

## <a name="remarks"></a><span data-ttu-id="6af8c-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6af8c-113">Remarks</span></span>

<span data-ttu-id="6af8c-114">Этот метод использует переменную-член [**кбасепин:: m \_ pName**](cbasepin-m-pname.md) для элемента **ачнаме** в \_ информационной структуре.</span><span class="sxs-lookup"><span data-stu-id="6af8c-114">This method uses the [**CBasePin::m\_pName**](cbasepin-m-pname.md) member variable for the **achName** member of the PIN\_INFO structure.</span></span>

<span data-ttu-id="6af8c-115">Если метод возвращает значение, если элемент **пфилтер** структуры PIN-кода \_ не **равен null**, то он содержит необработанные ссылки.</span><span class="sxs-lookup"><span data-stu-id="6af8c-115">When the method returns, if the **pFilter** member of the PIN\_INFO structure is non-**NULL**, it has an outstanding reference count.</span></span> <span data-ttu-id="6af8c-116">Не забудьте освободить интерфейс по завершении.</span><span class="sxs-lookup"><span data-stu-id="6af8c-116">Be sure to release the interface when you are done.</span></span>

## <a name="requirements"></a><span data-ttu-id="6af8c-117">Требования</span><span class="sxs-lookup"><span data-stu-id="6af8c-117">Requirements</span></span>



| <span data-ttu-id="6af8c-118">Требование</span><span class="sxs-lookup"><span data-stu-id="6af8c-118">Requirement</span></span> | <span data-ttu-id="6af8c-119">Значение</span><span class="sxs-lookup"><span data-stu-id="6af8c-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6af8c-120">Header</span><span class="sxs-lookup"><span data-stu-id="6af8c-120">Header</span></span><br/>  | <dl> <span data-ttu-id="6af8c-121"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6af8c-121"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="6af8c-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="6af8c-122">Library</span></span><br/> | <dl> <span data-ttu-id="6af8c-123"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="6af8c-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6af8c-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6af8c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6af8c-125">**Класс Кбасепин**</span><span class="sxs-lookup"><span data-stu-id="6af8c-125">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




