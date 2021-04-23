---
description: Метод Комплетеконнект завершает подключение входного контакта к другому ПИН-коду.
ms.assetid: 8dfc1a50-bc73-436a-a471-d8d3218410d3
title: Кбасерендерер. Комплетеконнект, метод (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a9d2d35f99a3b3b8dc5b668b8ee9a9f94f0a53dd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657479"
---
# <a name="cbaserenderercompleteconnect-method"></a><span data-ttu-id="0f36d-103">Кбасерендерер. Комплетеконнект, метод</span><span class="sxs-lookup"><span data-stu-id="0f36d-103">CBaseRenderer.CompleteConnect method</span></span>

<span data-ttu-id="0f36d-104">`CompleteConnect`Метод завершает подключение входного контакта к другому ПИН-коду.</span><span class="sxs-lookup"><span data-stu-id="0f36d-104">The `CompleteConnect` method completes the input pin's connection to another pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f36d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0f36d-105">Syntax</span></span>


```C++
virtual HRESULT CompleteConnect(
   IPin *pReceivePin
);
```



## <a name="parameters"></a><span data-ttu-id="0f36d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0f36d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f36d-107">*прецеивепин*</span><span class="sxs-lookup"><span data-stu-id="0f36d-107">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="0f36d-108">Указатель на интерфейс [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin) выходного контакта.</span><span class="sxs-lookup"><span data-stu-id="0f36d-108">Pointer to the output pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f36d-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0f36d-109">Return value</span></span>

<span data-ttu-id="0f36d-110">Возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="0f36d-110">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="0f36d-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0f36d-111">Remarks</span></span>

<span data-ttu-id="0f36d-112">Входной ПИН-код фильтра вызывает этот метод из собственного `CompleteConnect` метода, который вызывается для завершения соединения с ПИН-кодом.</span><span class="sxs-lookup"><span data-stu-id="0f36d-112">The filter's input pin calls this method from inside its own `CompleteConnect` method, which is called in order to complete a pin connection.</span></span> <span data-ttu-id="0f36d-113">(Дополнительные сведения см. в разделе [**кбасепин:: комплетеконнект**](cbasepin-completeconnect.md).) Фильтр вызывает метод [**кбасерендерер:: сетрепаинтстатус**](cbaserenderer-setrepaintstatus.md) , чтобы включить события [**\_ перерисовки EC**](ec-repaint.md) .</span><span class="sxs-lookup"><span data-stu-id="0f36d-113">(For more information, see [**CBasePin::CompleteConnect**](cbasepin-completeconnect.md).) The filter calls the [**CBaseRenderer::SetRepaintStatus**](cbaserenderer-setrepaintstatus.md) method to enable [**EC\_REPAINT**](ec-repaint.md) events.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f36d-114">Требования</span><span class="sxs-lookup"><span data-stu-id="0f36d-114">Requirements</span></span>



| <span data-ttu-id="0f36d-115">Требование</span><span class="sxs-lookup"><span data-stu-id="0f36d-115">Requirement</span></span> | <span data-ttu-id="0f36d-116">Значение</span><span class="sxs-lookup"><span data-stu-id="0f36d-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f36d-117">Header</span><span class="sxs-lookup"><span data-stu-id="0f36d-117">Header</span></span><br/>  | <dl> <span data-ttu-id="0f36d-118"><dt>Ренбасе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0f36d-118"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="0f36d-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="0f36d-119">Library</span></span><br/> | <dl> <span data-ttu-id="0f36d-120"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="0f36d-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f36d-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0f36d-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f36d-122">**Класс Кбасерендерер**</span><span class="sxs-lookup"><span data-stu-id="0f36d-122">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




