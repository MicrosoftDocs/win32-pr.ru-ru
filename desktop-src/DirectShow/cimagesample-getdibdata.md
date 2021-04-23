---
description: Метод Жетдибдата извлекает сведения о независимом от устройства GDI (DIB), который управляет этим объектом.
ms.assetid: ec337336-69ec-47ff-a522-42c0388f9bc0
title: Цимажесампле. Жетдибдата, метод (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageSample.GetDIBData
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0fd198152e7c0042a6d48cf942a48745540960d3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105674939"
---
# <a name="cimagesamplegetdibdata-method"></a><span data-ttu-id="df215-103">Цимажесампле. Жетдибдата, метод</span><span class="sxs-lookup"><span data-stu-id="df215-103">CImageSample.GetDIBData method</span></span>

<span data-ttu-id="df215-104">`GetDIBData`Метод извлекает сведения о независимом от устройства GDI (DIB), который управляет этим объектом.</span><span class="sxs-lookup"><span data-stu-id="df215-104">The `GetDIBData` method retrieves information about the GDI device-independent bitmap (DIB) that this object is managing.</span></span>

## <a name="syntax"></a><span data-ttu-id="df215-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="df215-105">Syntax</span></span>


```C++
DIBDATA* GetDIBData();
```



## <a name="parameters"></a><span data-ttu-id="df215-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="df215-106">Parameters</span></span>

<span data-ttu-id="df215-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="df215-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="df215-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="df215-108">Return value</span></span>

<span data-ttu-id="df215-109">Возвращает указатель на структуру [**дибдата**](dibdata.md) .</span><span class="sxs-lookup"><span data-stu-id="df215-109">Returns a pointer to a [**DIBDATA**](dibdata.md) structure.</span></span>

## <a name="remarks"></a><span data-ttu-id="df215-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="df215-110">Remarks</span></span>

<span data-ttu-id="df215-111">Перед вызовом этого метода вызывающий объект должен инициализировать структуру **дибдата** ; Проверьте значение **Цимажесампле:: m \_ Бинит**.</span><span class="sxs-lookup"><span data-stu-id="df215-111">The caller must initialize the **DIBDATA** structure before calling this method; check the value of **CImageSample::m\_bInit**.</span></span> <span data-ttu-id="df215-112">Чтобы инициализировать структуру, вызовите метод [**Цимажесампле:: сетдибдата**](cimagesample-setdibdata.md) .</span><span class="sxs-lookup"><span data-stu-id="df215-112">To initialize the structure, call the [**CImageSample::SetDIBData**](cimagesample-setdibdata.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="df215-113">Требования</span><span class="sxs-lookup"><span data-stu-id="df215-113">Requirements</span></span>



| <span data-ttu-id="df215-114">Требование</span><span class="sxs-lookup"><span data-stu-id="df215-114">Requirement</span></span> | <span data-ttu-id="df215-115">Значение</span><span class="sxs-lookup"><span data-stu-id="df215-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df215-116">Header</span><span class="sxs-lookup"><span data-stu-id="df215-116">Header</span></span><br/>  | <dl> <span data-ttu-id="df215-117"><dt>Винутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="df215-117"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="df215-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="df215-118">Library</span></span><br/> | <dl> <span data-ttu-id="df215-119"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="df215-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df215-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="df215-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df215-121">**Класс Цимажесампле**</span><span class="sxs-lookup"><span data-stu-id="df215-121">**CImageSample Class**</span></span>](cimagesample.md)
</dt> </dl>

 

 




