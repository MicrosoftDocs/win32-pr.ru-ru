---
description: Метод методом Соединенного соединения извлекает ПИН-код, подключенный к этому ПИН-коду.
ms.assetid: 7b47aa8e-55a9-45f8-aa32-902fee037c72
title: Метод Кбасепин. соединен (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.GetConnected
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e5c583b06a9c25126a611736002c455a2c93ed90
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657421"
---
# <a name="cbasepingetconnected-method"></a><span data-ttu-id="6eb79-103">Кбасепин. соединенный метод</span><span class="sxs-lookup"><span data-stu-id="6eb79-103">CBasePin.GetConnected method</span></span>

<span data-ttu-id="6eb79-104">`GetConnected`Метод извлекает ПИН-код, подключенный к этому ПИН-коду.</span><span class="sxs-lookup"><span data-stu-id="6eb79-104">The `GetConnected` method retrieves the pin connected to this pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="6eb79-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6eb79-105">Syntax</span></span>


```C++
IPin* GetConnected();
```



## <a name="parameters"></a><span data-ttu-id="6eb79-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6eb79-106">Parameters</span></span>

<span data-ttu-id="6eb79-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="6eb79-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6eb79-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6eb79-108">Return value</span></span>

<span data-ttu-id="6eb79-109">Возвращает указатель на интерфейс [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin) другого ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="6eb79-109">Returns a pointer to the other pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

## <a name="remarks"></a><span data-ttu-id="6eb79-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6eb79-110">Remarks</span></span>

<span data-ttu-id="6eb79-111">Если ПИН-код не подключен, этот метод возвращает **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="6eb79-111">If the pin is not connected, this method returns **NULL**.</span></span> <span data-ttu-id="6eb79-112">Вызовите метод [**кбасепин::**](cbasepin-isconnected.md) , чтобы определить, подключен ли ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="6eb79-112">Call the [**CBasePin::IsConnected**](cbasepin-isconnected.md) method to determine whether the pin is connected.</span></span>

<span data-ttu-id="6eb79-113">Метод не вызывает **AddRef** для интерфейса **Ипин** , поэтому вызывающий объект не должен освобождать интерфейс.</span><span class="sxs-lookup"><span data-stu-id="6eb79-113">The method does not call **AddRef** on the **IPin** interface, so the caller should not release the interface.</span></span>

## <a name="examples"></a><span data-ttu-id="6eb79-114">Примеры</span><span class="sxs-lookup"><span data-stu-id="6eb79-114">Examples</span></span>

<span data-ttu-id="6eb79-115">Так как счетчик ссылок не увеличивается на возвращенном указателе, вызовы метода можно объединить в цепочку.</span><span class="sxs-lookup"><span data-stu-id="6eb79-115">Because the reference count is not incremented on the returned pointer, you can chain method calls together:</span></span>


```C++
if (m_MyPin->IsConnected())
{
    m_MyPin->GetConnected()->EndOfStream();
}
```



<span data-ttu-id="6eb79-116">Этот шаблон программирования очень удобен; но, как показано в примере, необходимо избегать разыменования **пустого** указателя, если ПИН-код не подключен.</span><span class="sxs-lookup"><span data-stu-id="6eb79-116">This coding pattern is very convenient; but as the example shows, you must be careful not to dereference a **NULL** pointer when the pin is unconnected.</span></span>

## <a name="requirements"></a><span data-ttu-id="6eb79-117">Требования</span><span class="sxs-lookup"><span data-stu-id="6eb79-117">Requirements</span></span>



| <span data-ttu-id="6eb79-118">Требование</span><span class="sxs-lookup"><span data-stu-id="6eb79-118">Requirement</span></span> | <span data-ttu-id="6eb79-119">Значение</span><span class="sxs-lookup"><span data-stu-id="6eb79-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6eb79-120">Header</span><span class="sxs-lookup"><span data-stu-id="6eb79-120">Header</span></span><br/>  | <dl> <span data-ttu-id="6eb79-121"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6eb79-121"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="6eb79-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="6eb79-122">Library</span></span><br/> | <dl> <span data-ttu-id="6eb79-123"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="6eb79-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6eb79-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6eb79-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6eb79-125">**Класс Кбасепин**</span><span class="sxs-lookup"><span data-stu-id="6eb79-125">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




