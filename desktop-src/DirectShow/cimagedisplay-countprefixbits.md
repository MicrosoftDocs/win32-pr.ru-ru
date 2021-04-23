---
description: Метод Каунтпрефиксбитс вычисляет количество нулевых битов в начале указанного битового поля.
ms.assetid: 36fc5c5f-dc64-4588-9130-1b0740d03be1
title: Цимажедисплай. Каунтпрефиксбитс, метод (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.CountPrefixBits
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4333e1b0826b4fac7bfff463531b5d2e10704418
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657657"
---
# <a name="cimagedisplaycountprefixbits-method"></a><span data-ttu-id="6dfeb-103">Цимажедисплай. Каунтпрефиксбитс, метод</span><span class="sxs-lookup"><span data-stu-id="6dfeb-103">CImageDisplay.CountPrefixBits method</span></span>

<span data-ttu-id="6dfeb-104">`CountPrefixBits`Метод вычисляет количество нулевых битов в начале указанного битового поля.</span><span class="sxs-lookup"><span data-stu-id="6dfeb-104">The `CountPrefixBits` method calculates the number of zero bits at the start of a specified bit field.</span></span>

## <a name="syntax"></a><span data-ttu-id="6dfeb-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6dfeb-105">Syntax</span></span>


```C++
DWORD CountPrefixBits(
   const DWORD Field
);
```



## <a name="parameters"></a><span data-ttu-id="6dfeb-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6dfeb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6dfeb-107">*Поле*</span><span class="sxs-lookup"><span data-stu-id="6dfeb-107">*Field*</span></span> 
</dt> <dd>

<span data-ttu-id="6dfeb-108">Задает битовое поле в виде значения **типа DWORD** .</span><span class="sxs-lookup"><span data-stu-id="6dfeb-108">Specifies a bit field as a **DWORD** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6dfeb-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6dfeb-109">Return value</span></span>

<span data-ttu-id="6dfeb-110">Возвращает число нулей, предшествующих первому 1 биту, или 0x80000000, если все биты равны нулю.</span><span class="sxs-lookup"><span data-stu-id="6dfeb-110">Returns the number of zero bits that occur before the first 1 bit, or 0x80000000 if all bits are zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="6dfeb-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6dfeb-111">Remarks</span></span>

<span data-ttu-id="6dfeb-112">Этот метод полезен для работы с цветовыми масками в структурах [**видеоинфо**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) .</span><span class="sxs-lookup"><span data-stu-id="6dfeb-112">This method is useful for working with color masks in [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) structures.</span></span>

## <a name="requirements"></a><span data-ttu-id="6dfeb-113">Требования</span><span class="sxs-lookup"><span data-stu-id="6dfeb-113">Requirements</span></span>



| <span data-ttu-id="6dfeb-114">Требование</span><span class="sxs-lookup"><span data-stu-id="6dfeb-114">Requirement</span></span> | <span data-ttu-id="6dfeb-115">Значение</span><span class="sxs-lookup"><span data-stu-id="6dfeb-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6dfeb-116">Header</span><span class="sxs-lookup"><span data-stu-id="6dfeb-116">Header</span></span><br/>  | <dl> <span data-ttu-id="6dfeb-117"><dt>Винутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6dfeb-117"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="6dfeb-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="6dfeb-118">Library</span></span><br/> | <dl> <span data-ttu-id="6dfeb-119"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="6dfeb-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6dfeb-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6dfeb-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6dfeb-121">**Класс Цимажедисплай**</span><span class="sxs-lookup"><span data-stu-id="6dfeb-121">**CImageDisplay Class**</span></span>](cimagedisplay.md)
</dt> </dl>

 

 




