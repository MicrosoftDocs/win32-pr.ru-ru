---
description: Метод Бреакконнект освобождает входной ПИН-код из соединения.
ms.assetid: e295cec1-8c8f-471c-8832-075ac7708cb1
title: Кбасерендерер. Бреакконнект, метод (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.BreakConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 98c1e01c15740616541706ca4d9da3ab5e66538c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668750"
---
# <a name="cbaserendererbreakconnect-method"></a><span data-ttu-id="4e7d7-103">Кбасерендерер. Бреакконнект, метод</span><span class="sxs-lookup"><span data-stu-id="4e7d7-103">CBaseRenderer.BreakConnect method</span></span>

<span data-ttu-id="4e7d7-104">`BreakConnect`Метод освобождает входной ПИН-код из соединения.</span><span class="sxs-lookup"><span data-stu-id="4e7d7-104">The `BreakConnect` method releases the input pin from a connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e7d7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4e7d7-105">Syntax</span></span>


```C++
virtual HRESULT BreakConnect();
```



## <a name="parameters"></a><span data-ttu-id="4e7d7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4e7d7-106">Parameters</span></span>

<span data-ttu-id="4e7d7-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="4e7d7-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4e7d7-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4e7d7-108">Return value</span></span>

<span data-ttu-id="4e7d7-109">Возвращает одно из значений **HRESULT** , приведенных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="4e7d7-109">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="4e7d7-110">Код возврата</span><span class="sxs-lookup"><span data-stu-id="4e7d7-110">Return code</span></span>                                                                                         | <span data-ttu-id="4e7d7-111">Описание</span><span class="sxs-lookup"><span data-stu-id="4e7d7-111">Description</span></span>                            |
|-----------------------------------------------------------------------------------------------------|----------------------------------------|
| <dl> <span data-ttu-id="4e7d7-112"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="4e7d7-112"><dt>**S\_FALSE**</dt></span></span> </dl>             | <span data-ttu-id="4e7d7-113">ПИН-код не подключен.</span><span class="sxs-lookup"><span data-stu-id="4e7d7-113">The pin was not connected.</span></span><br/>  |
| <dl> <span data-ttu-id="4e7d7-114"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="4e7d7-114"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="4e7d7-115">Успешно.</span><span class="sxs-lookup"><span data-stu-id="4e7d7-115">Success.</span></span><br/>                    |
| <dl> <span data-ttu-id="4e7d7-116"><dt>**VFW \_ E \_ не \_ остановлен**</dt></span><span class="sxs-lookup"><span data-stu-id="4e7d7-116"><dt>**VFW\_E\_NOT\_STOPPED**</dt></span></span> </dl> | <span data-ttu-id="4e7d7-117">Фильтр все еще активен.</span><span class="sxs-lookup"><span data-stu-id="4e7d7-117">The filter is still active.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4e7d7-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4e7d7-118">Remarks</span></span>

<span data-ttu-id="4e7d7-119">Входной ПИН-код фильтра вызывает этот метод из собственного `BreakConnect` метода.</span><span class="sxs-lookup"><span data-stu-id="4e7d7-119">The filter's input pin calls this method from inside its own `BreakConnect` method.</span></span> <span data-ttu-id="4e7d7-120">(Дополнительные сведения см. в разделе [**кбасепин:: бреакконнект**](cbasepin-breakconnect.md).) Фильтр выполняет некоторый внутренний бухгалтерский перевод, например сброс флага конца потока.</span><span class="sxs-lookup"><span data-stu-id="4e7d7-120">(For more information, see [**CBasePin::BreakConnect**](cbasepin-breakconnect.md).) The filter performs some internal bookkeeping, such as resetting the end-of-stream flag.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e7d7-121">Требования</span><span class="sxs-lookup"><span data-stu-id="4e7d7-121">Requirements</span></span>



| <span data-ttu-id="4e7d7-122">Требование</span><span class="sxs-lookup"><span data-stu-id="4e7d7-122">Requirement</span></span> | <span data-ttu-id="4e7d7-123">Значение</span><span class="sxs-lookup"><span data-stu-id="4e7d7-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e7d7-124">Header</span><span class="sxs-lookup"><span data-stu-id="4e7d7-124">Header</span></span><br/>  | <dl> <span data-ttu-id="4e7d7-125"><dt>Ренбасе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4e7d7-125"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="4e7d7-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="4e7d7-126">Library</span></span><br/> | <dl> <span data-ttu-id="4e7d7-127"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="4e7d7-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e7d7-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4e7d7-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e7d7-129">**Класс Кбасерендерер**</span><span class="sxs-lookup"><span data-stu-id="4e7d7-129">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




