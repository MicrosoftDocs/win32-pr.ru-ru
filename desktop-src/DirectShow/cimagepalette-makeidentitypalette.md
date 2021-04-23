---
description: Метод Макеидентитипалетте пытается сделать &\# 0034; палитра удостоверений, &\# 0034; определяется как один, сопоставляемый непосредственно с палитрой, выбранной в устройстве вывода.
ms.assetid: 08a0cf67-f43f-44c0-bfb3-6527fd434ea4
title: Цимажепалетте. Макеидентитипалетте, метод (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImagePalette.MakeIdentityPalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8e105652108e74907375408f0bd8946c69194202
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665235"
---
# <a name="cimagepalettemakeidentitypalette-method"></a><span data-ttu-id="c9056-103">Цимажепалетте. Макеидентитипалетте, метод</span><span class="sxs-lookup"><span data-stu-id="c9056-103">CImagePalette.MakeIdentityPalette method</span></span>

<span data-ttu-id="c9056-104">`MakeIdentityPalette`Метод пытается создать "палитру удостоверений", определенную как, которая непосредственно сопоставляется с палитрой, выбранной в устройстве вывода.</span><span class="sxs-lookup"><span data-stu-id="c9056-104">The `MakeIdentityPalette` method attempts to make an "identity palette," defined as one that maps directly to the palette selected in the display device.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9056-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c9056-105">Syntax</span></span>


```C++
HRESULT MakeIdentityPalette(
   PALETTEENTRY *pEntry,
   INT          iColours,
   LPSTR        szDevice
);
```



## <a name="parameters"></a><span data-ttu-id="c9056-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c9056-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9056-107">*пентри*</span><span class="sxs-lookup"><span data-stu-id="c9056-107">*pEntry*</span></span> 
</dt> <dd>

<span data-ttu-id="c9056-108">Указатель на массив записей палитры.</span><span class="sxs-lookup"><span data-stu-id="c9056-108">Pointer to an array of palette entries.</span></span>

</dd> <dt>

<span data-ttu-id="c9056-109">*иколаурс*</span><span class="sxs-lookup"><span data-stu-id="c9056-109">*iColours*</span></span> 
</dt> <dd>

<span data-ttu-id="c9056-110">Число записей палитры в *пентри*.</span><span class="sxs-lookup"><span data-stu-id="c9056-110">Number of palette entries in *pEntry*.</span></span>

</dd> <dt>

<span data-ttu-id="c9056-111">*сздевице*</span><span class="sxs-lookup"><span data-stu-id="c9056-111">*szDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="c9056-112">Указатель на строку, содержащую имя устройства вывода, которое возвращается функцией GDI **енумдисплайдевицес** .</span><span class="sxs-lookup"><span data-stu-id="c9056-112">Pointer to a string that contains the name of the display device, as returned by the GDI **EnumDisplayDevices** function.</span></span> <span data-ttu-id="c9056-113">Чтобы использовать основное устройство вывода, присвойте этому параметру **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="c9056-113">To use the main display device, set this parameter to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9056-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c9056-114">Return value</span></span>

<span data-ttu-id="c9056-115">При \_ успешном выполнении или при сбое возвращает \_ значение ОК.</span><span class="sxs-lookup"><span data-stu-id="c9056-115">Returns S\_OK if successful or S\_FALSE if unsuccessful.</span></span>

## <a name="remarks"></a><span data-ttu-id="c9056-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c9056-116">Remarks</span></span>

<span data-ttu-id="c9056-117">Этот метод сравнивает зарезервированные записи в системной палитре с соответствующими записями в массиве *пентри* .</span><span class="sxs-lookup"><span data-stu-id="c9056-117">This method compares the reserved entries in the system palette against the corresponding entries in the *pEntry* array.</span></span> <span data-ttu-id="c9056-118">Если они точно соответствуют друг другу, метод устанавливает \_ флаг СВОРАЧИВАНИЯ ПК в оставшихся (не зарезервированных) записях палитры в *пентри*.</span><span class="sxs-lookup"><span data-stu-id="c9056-118">If they match exactly, the method sets the PC\_NOCOLLAPSE flag in the remaining (non-reserved) palette entries in *pEntry*.</span></span> <span data-ttu-id="c9056-119">Этот флаг предотвращает попытку GDI сопоставлять записи логической палитры с записями системной палитры.</span><span class="sxs-lookup"><span data-stu-id="c9056-119">This flag prevents GDI from trying map logical palette entries to system palette entries.</span></span>

<span data-ttu-id="c9056-120">Метод [**Цимажепалетте:: макепалетте**](cimagepalette-makepalette.md) вызывает этот метод.</span><span class="sxs-lookup"><span data-stu-id="c9056-120">The [**CImagePalette::MakePalette**](cimagepalette-makepalette.md) method calls this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9056-121">Требования</span><span class="sxs-lookup"><span data-stu-id="c9056-121">Requirements</span></span>



| <span data-ttu-id="c9056-122">Требование</span><span class="sxs-lookup"><span data-stu-id="c9056-122">Requirement</span></span> | <span data-ttu-id="c9056-123">Значение</span><span class="sxs-lookup"><span data-stu-id="c9056-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9056-124">Header</span><span class="sxs-lookup"><span data-stu-id="c9056-124">Header</span></span><br/>  | <dl> <span data-ttu-id="c9056-125"><dt>Винутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c9056-125"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c9056-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c9056-126">Library</span></span><br/> | <dl> <span data-ttu-id="c9056-127"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="c9056-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9056-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c9056-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9056-129">**Класс Цимажепалетте**</span><span class="sxs-lookup"><span data-stu-id="c9056-129">**CImagePalette Class**</span></span>](cimagepalette.md)
</dt> </dl>

 

 




