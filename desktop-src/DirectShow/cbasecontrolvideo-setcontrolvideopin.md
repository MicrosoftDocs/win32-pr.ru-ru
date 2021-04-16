---
description: Метод Сетконтролвидеопин задает ПИН-код, используемый фильтром.
ms.assetid: 4346f828-4380-4150-9ecb-74eb690bdcdf
title: Кбасеконтролвидео. Сетконтролвидеопин, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.SetControlVideoPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a4cf47469800a4d1ecd8abe373d6f3c1fd53ece5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105656983"
---
# <a name="cbasecontrolvideosetcontrolvideopin-method"></a><span data-ttu-id="3fbfb-103">Кбасеконтролвидео. Сетконтролвидеопин, метод</span><span class="sxs-lookup"><span data-stu-id="3fbfb-103">CBaseControlVideo.SetControlVideoPin method</span></span>

<span data-ttu-id="3fbfb-104">`SetControlVideoPin`Метод задает ПИН-код, используемый фильтром.</span><span class="sxs-lookup"><span data-stu-id="3fbfb-104">The `SetControlVideoPin` method sets the pin used by the filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="3fbfb-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3fbfb-105">Syntax</span></span>


```C++
void SetControlVideoPin(
   CBasePin *pPin
);
```



## <a name="parameters"></a><span data-ttu-id="3fbfb-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3fbfb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3fbfb-107">*ппин*</span><span class="sxs-lookup"><span data-stu-id="3fbfb-107">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="3fbfb-108">Указатель на ПИН-код, с которым синхронизируется интерфейс.</span><span class="sxs-lookup"><span data-stu-id="3fbfb-108">Pointer to the pin with which the interface is synchronized.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3fbfb-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3fbfb-109">Return value</span></span>

<span data-ttu-id="3fbfb-110">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="3fbfb-110">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3fbfb-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3fbfb-111">Remarks</span></span>

<span data-ttu-id="3fbfb-112">Интерфейс можно вызывать только после успешного подключения фильтра.</span><span class="sxs-lookup"><span data-stu-id="3fbfb-112">The interface can be called only when the filter has been connected successfully.</span></span> <span data-ttu-id="3fbfb-113">Объект передается через этот метод в ПИН-код, с которым он синхронизирован; в большинстве случаев он определяет, подключен ли ПИН-код при вызове метода интерфейса, и при сбое возвращает VFW \_ E \_ Not \_ Connected.</span><span class="sxs-lookup"><span data-stu-id="3fbfb-113">The object is passed through this method to the pin with which it is synchronized; in most cases it will determine if the pin is connected when it has an interface method called and will return VFW\_E\_NOT\_CONNECTED if it fails.</span></span>

## <a name="requirements"></a><span data-ttu-id="3fbfb-114">Требования</span><span class="sxs-lookup"><span data-stu-id="3fbfb-114">Requirements</span></span>



| <span data-ttu-id="3fbfb-115">Требование</span><span class="sxs-lookup"><span data-stu-id="3fbfb-115">Requirement</span></span> | <span data-ttu-id="3fbfb-116">Значение</span><span class="sxs-lookup"><span data-stu-id="3fbfb-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3fbfb-117">Header</span><span class="sxs-lookup"><span data-stu-id="3fbfb-117">Header</span></span><br/>  | <dl> <span data-ttu-id="3fbfb-118"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3fbfb-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="3fbfb-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="3fbfb-119">Library</span></span><br/> | <dl> <span data-ttu-id="3fbfb-120"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="3fbfb-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3fbfb-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3fbfb-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3fbfb-122">**Класс Кбасеконтролвидео**</span><span class="sxs-lookup"><span data-stu-id="3fbfb-122">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




