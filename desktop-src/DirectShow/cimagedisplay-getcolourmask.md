---
description: Метод Жетколаурмаск извлекает цветовую маску для текущего формата экрана.
ms.assetid: 386d0439-8502-411d-935c-3c2153a8b5b4
title: Цимажедисплай. Жетколаурмаск, метод (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.GetColourMask
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 499b3677cd68444b58514d692d87cd4f631350b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679949"
---
# <a name="cimagedisplaygetcolourmask-method"></a><span data-ttu-id="51e5c-103">Цимажедисплай. Жетколаурмаск, метод</span><span class="sxs-lookup"><span data-stu-id="51e5c-103">CImageDisplay.GetColourMask method</span></span>

<span data-ttu-id="51e5c-104">`GetColourMask`Метод извлекает цветовую маску для текущего формата экрана.</span><span class="sxs-lookup"><span data-stu-id="51e5c-104">The `GetColourMask` method retrieves the color masks for the current display format.</span></span>

## <a name="syntax"></a><span data-ttu-id="51e5c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="51e5c-105">Syntax</span></span>


```C++
BOOL GetColourMask(
   DWORD *pMaskRed,
   DWORD *pMaskGreen,
   DWORD *pMaskBlue
);
```



## <a name="parameters"></a><span data-ttu-id="51e5c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="51e5c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51e5c-107">*пмаскред*</span><span class="sxs-lookup"><span data-stu-id="51e5c-107">*pMaskRed*</span></span> 
</dt> <dd>

<span data-ttu-id="51e5c-108">Указатель на переменную, получающую маску красного компонента.</span><span class="sxs-lookup"><span data-stu-id="51e5c-108">Pointer to a variable that receives the red-component mask.</span></span>

</dd> <dt>

<span data-ttu-id="51e5c-109">*пмаскгрин*</span><span class="sxs-lookup"><span data-stu-id="51e5c-109">*pMaskGreen*</span></span> 
</dt> <dd>

<span data-ttu-id="51e5c-110">Указатель на переменную, которая получает маску зеленого компонента.</span><span class="sxs-lookup"><span data-stu-id="51e5c-110">Pointer to a variable that receives the green-component mask.</span></span>

</dd> <dt>

<span data-ttu-id="51e5c-111">*пмаскблуе*</span><span class="sxs-lookup"><span data-stu-id="51e5c-111">*pMaskBlue*</span></span> 
</dt> <dd>

<span data-ttu-id="51e5c-112">Указатель на переменную, получающую маску синего компонента.</span><span class="sxs-lookup"><span data-stu-id="51e5c-112">Pointer to a variable that receives the blue-component mask.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="51e5c-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="51e5c-113">Return value</span></span>

<span data-ttu-id="51e5c-114">Возвращает **значение true** , если успешно, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="51e5c-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="51e5c-115">Требования</span><span class="sxs-lookup"><span data-stu-id="51e5c-115">Requirements</span></span>



| <span data-ttu-id="51e5c-116">Требование</span><span class="sxs-lookup"><span data-stu-id="51e5c-116">Requirement</span></span> | <span data-ttu-id="51e5c-117">Значение</span><span class="sxs-lookup"><span data-stu-id="51e5c-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51e5c-118">Header</span><span class="sxs-lookup"><span data-stu-id="51e5c-118">Header</span></span><br/>  | <dl> <span data-ttu-id="51e5c-119"><dt>Винутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="51e5c-119"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="51e5c-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="51e5c-120">Library</span></span><br/> | <dl> <span data-ttu-id="51e5c-121"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="51e5c-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51e5c-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="51e5c-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51e5c-123">**Класс Цимажедисплай**</span><span class="sxs-lookup"><span data-stu-id="51e5c-123">**CImageDisplay Class**</span></span>](cimagedisplay.md)
</dt> </dl>

 

 




