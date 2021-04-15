---
description: Метод Disconnect прерывает соединение с выходным закреплением.
ms.assetid: 6e362e32-7b74-4392-b46f-1ab47a30a07b
title: Метод Кпуллпин. Disconnect (Пуллпин. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.Disconnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ec13a7f29a06bab4f79ddb58932796f8363adadc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669061"
---
# <a name="cpullpindisconnect-method"></a><span data-ttu-id="26136-103">Кпуллпин. Disconnect, метод</span><span class="sxs-lookup"><span data-stu-id="26136-103">CPullPin.Disconnect method</span></span>

<span data-ttu-id="26136-104">`Disconnect`Метод прерывает соединение с выходным закреплением.</span><span class="sxs-lookup"><span data-stu-id="26136-104">The `Disconnect` method breaks the connection with the output pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="26136-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="26136-105">Syntax</span></span>


```C++
HRESULT Disconnect();
```



## <a name="parameters"></a><span data-ttu-id="26136-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="26136-106">Parameters</span></span>

<span data-ttu-id="26136-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="26136-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="26136-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="26136-108">Return value</span></span>

<span data-ttu-id="26136-109">Возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="26136-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="26136-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="26136-110">Remarks</span></span>

<span data-ttu-id="26136-111">Этот метод прерывает все соединения, сделанные в методе [**кпуллпин:: Connect**](cpullpin-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="26136-111">This method breaks any connection made in the [**CPullPin::Connect**](cpullpin-connect.md) method.</span></span> <span data-ttu-id="26136-112">Вызовите этот метод внутри метода [**Ипин::D соединения**](/windows/desktop/api/Strmif/nf-strmif-ipin-disconnect) .</span><span class="sxs-lookup"><span data-stu-id="26136-112">Call this method inside your [**IPin::Disconnect**](/windows/desktop/api/Strmif/nf-strmif-ipin-disconnect) method.</span></span> <span data-ttu-id="26136-113">(Если ПИН-код является производным от [**кбасепин**](cbasepin.md), переопределите [**Кбасепин:: бреакконнект**](cbasepin-breakconnect.md) , чтобы вызвать этот метод.)</span><span class="sxs-lookup"><span data-stu-id="26136-113">(If your pin derives from [**CBasePin**](cbasepin.md), override [**CBasePin::BreakConnect**](cbasepin-breakconnect.md) to call this method.)</span></span>

## <a name="requirements"></a><span data-ttu-id="26136-114">Требования</span><span class="sxs-lookup"><span data-stu-id="26136-114">Requirements</span></span>



| <span data-ttu-id="26136-115">Требование</span><span class="sxs-lookup"><span data-stu-id="26136-115">Requirement</span></span> | <span data-ttu-id="26136-116">Значение</span><span class="sxs-lookup"><span data-stu-id="26136-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="26136-117">Header</span><span class="sxs-lookup"><span data-stu-id="26136-117">Header</span></span><br/>  | <dl> <span data-ttu-id="26136-118"><dt>Пуллпин. h</dt></span><span class="sxs-lookup"><span data-stu-id="26136-118"><dt>Pullpin.h</dt></span></span> </dl>                                                                                                       |
| <span data-ttu-id="26136-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="26136-119">Library</span></span><br/> | <dl> <span data-ttu-id="26136-120"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="26136-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26136-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="26136-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26136-122">**Класс Кпуллпин**</span><span class="sxs-lookup"><span data-stu-id="26136-122">**CPullPin Class**</span></span>](cpullpin.md)
</dt> </dl>

 

 




