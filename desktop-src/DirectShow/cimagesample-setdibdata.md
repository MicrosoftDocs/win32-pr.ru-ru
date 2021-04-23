---
description: Метод Сетдибдата указывает сведения о независимом от устройства GDI (DIB), который управляет этим объектом. Вызовите этот метод, чтобы инициализировать объект Цимажесампле.
ms.assetid: 850fa16b-d4b9-4fe6-b202-7b54c49a4589
title: Цимажесампле. Сетдибдата, метод (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageSample.SetDIBData
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 418263da0416b325b1b080713dd6289f3bcc688e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665227"
---
# <a name="cimagesamplesetdibdata-method"></a><span data-ttu-id="61f66-104">Цимажесампле. Сетдибдата, метод</span><span class="sxs-lookup"><span data-stu-id="61f66-104">CImageSample.SetDIBData method</span></span>

<span data-ttu-id="61f66-105">`SetDIBData`Метод указывает сведения о независимом от устройства GDI (DIB), который управляет этим объектом.</span><span class="sxs-lookup"><span data-stu-id="61f66-105">The `SetDIBData` method specifies information about the GDI device-independent bitmap (DIB) that this object is managing.</span></span> <span data-ttu-id="61f66-106">Вызовите этот метод, чтобы инициализировать объект **Цимажесампле** .</span><span class="sxs-lookup"><span data-stu-id="61f66-106">Call this method to initialize the **CImageSample** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="61f66-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="61f66-107">Syntax</span></span>


```C++
void SetDIBData(
   DIBDATA *pDibData
);
```



## <a name="parameters"></a><span data-ttu-id="61f66-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="61f66-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61f66-109">*пдибдата*</span><span class="sxs-lookup"><span data-stu-id="61f66-109">*pDibData*</span></span> 
</dt> <dd>

<span data-ttu-id="61f66-110">Указатель на структуру [**дибдата**](dibdata.md) .</span><span class="sxs-lookup"><span data-stu-id="61f66-110">Pointer to a [**DIBDATA**](dibdata.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61f66-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="61f66-111">Return value</span></span>

<span data-ttu-id="61f66-112">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="61f66-112">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="61f66-113">Требования</span><span class="sxs-lookup"><span data-stu-id="61f66-113">Requirements</span></span>



| <span data-ttu-id="61f66-114">Требование</span><span class="sxs-lookup"><span data-stu-id="61f66-114">Requirement</span></span> | <span data-ttu-id="61f66-115">Значение</span><span class="sxs-lookup"><span data-stu-id="61f66-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="61f66-116">Header</span><span class="sxs-lookup"><span data-stu-id="61f66-116">Header</span></span><br/>  | <dl> <span data-ttu-id="61f66-117"><dt>Винутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="61f66-117"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="61f66-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="61f66-118">Library</span></span><br/> | <dl> <span data-ttu-id="61f66-119"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="61f66-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61f66-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="61f66-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61f66-121">**Класс Цимажесампле**</span><span class="sxs-lookup"><span data-stu-id="61f66-121">**CImageSample Class**</span></span>](cimagesample.md)
</dt> </dl>

 

 




