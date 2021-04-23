---
description: Извлекает количество интерфейсов типа данных, предоставленных объектом.
ms.assetid: 29575325-8f97-4f39-8272-86a917d9144f
title: Кмедиаконтрол. Жеттипеинфокаунт, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaControl.GetTypeInfoCount
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f2454e503a045a02db20c0dc457b6367f6d3b427
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669192"
---
# <a name="cmediacontrolgettypeinfocount-method"></a><span data-ttu-id="545a0-103">Кмедиаконтрол. Жеттипеинфокаунт, метод</span><span class="sxs-lookup"><span data-stu-id="545a0-103">CMediaControl.GetTypeInfoCount method</span></span>

<span data-ttu-id="545a0-104">Извлекает количество интерфейсов типа данных, предоставленных объектом.</span><span class="sxs-lookup"><span data-stu-id="545a0-104">Retrieves the number of type-information interfaces provided by an object.</span></span>

## <a name="syntax"></a><span data-ttu-id="545a0-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="545a0-105">Syntax</span></span>


```C++
HRESULT GetTypeInfoCount(
   UINT *pctinfo
);
```



## <a name="parameters"></a><span data-ttu-id="545a0-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="545a0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="545a0-107">*пктинфо*</span><span class="sxs-lookup"><span data-stu-id="545a0-107">*pctinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="545a0-108">Указатель на число интерфейсов типа-данных, предоставляемых объектом.</span><span class="sxs-lookup"><span data-stu-id="545a0-108">Pointer to the number of type-information interfaces that the object provides.</span></span> <span data-ttu-id="545a0-109">Если объект предоставляет сведения о типе, это число равно 1; в противном случае число равно 0.</span><span class="sxs-lookup"><span data-stu-id="545a0-109">If the object provides type information, this number is 1; otherwise, the number is 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="545a0-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="545a0-110">Return value</span></span>

<span data-ttu-id="545a0-111">Возвращает \_ указатель E, если *пктинфо* является недопустимым; в противном случае возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="545a0-111">Returns E\_POINTER if *pctinfo* is invalid; otherwise, returns S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="545a0-112">Требования</span><span class="sxs-lookup"><span data-stu-id="545a0-112">Requirements</span></span>



| <span data-ttu-id="545a0-113">Требование</span><span class="sxs-lookup"><span data-stu-id="545a0-113">Requirement</span></span> | <span data-ttu-id="545a0-114">Значение</span><span class="sxs-lookup"><span data-stu-id="545a0-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="545a0-115">Header</span><span class="sxs-lookup"><span data-stu-id="545a0-115">Header</span></span><br/>  | <dl> <span data-ttu-id="545a0-116"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="545a0-116"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="545a0-117">Библиотека</span><span class="sxs-lookup"><span data-stu-id="545a0-117">Library</span></span><br/> | <dl> <span data-ttu-id="545a0-118"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="545a0-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="545a0-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="545a0-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="545a0-120">**Класс Кмедиаконтрол**</span><span class="sxs-lookup"><span data-stu-id="545a0-120">**CMediaControl Class**</span></span>](cmediacontrol.md)
</dt> </dl>

 

 




