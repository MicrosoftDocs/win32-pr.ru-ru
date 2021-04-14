---
description: Метод конструктора.
ms.assetid: 00549dfe-5dd4-445e-bad3-eb6bcfea8f5f
title: Конструктор Кмедиаконтрол. Кмедиаконтрол (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaControl.CMediaControl
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 63b965ff2484d4db7f7de41d8d524bc74c31ac73
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675556"
---
# <a name="cmediacontrolcmediacontrol-constructor"></a><span data-ttu-id="310f2-103">Кмедиаконтрол. Кмедиаконтрол, конструктор</span><span class="sxs-lookup"><span data-stu-id="310f2-103">CMediaControl.CMediaControl constructor</span></span>

<span data-ttu-id="310f2-104">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="310f2-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="310f2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="310f2-105">Syntax</span></span>


```C++
CMediaControl(
   const TCHAR     *pName,
         LPUNKNOWN pUnk
);
```



## <a name="parameters"></a><span data-ttu-id="310f2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="310f2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="310f2-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="310f2-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="310f2-108">Указатель на имя объекта для целей отладки.</span><span class="sxs-lookup"><span data-stu-id="310f2-108">Pointer to the name of the object for debugging purposes.</span></span>

</dd> <dt>

<span data-ttu-id="310f2-109">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="310f2-109">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="310f2-110">Указатель на владельца этого объекта.</span><span class="sxs-lookup"><span data-stu-id="310f2-110">Pointer to the owner of this object.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="310f2-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="310f2-111">Remarks</span></span>

<span data-ttu-id="310f2-112">Выделите параметр *pName* в статической памяти.</span><span class="sxs-lookup"><span data-stu-id="310f2-112">Allocate the *pName* parameter in static memory.</span></span> <span data-ttu-id="310f2-113">Это имя отображается в терминале отладки при создании и удалении объекта.</span><span class="sxs-lookup"><span data-stu-id="310f2-113">This name appears on the debugging terminal upon creation and deletion of the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="310f2-114">Требования</span><span class="sxs-lookup"><span data-stu-id="310f2-114">Requirements</span></span>



| <span data-ttu-id="310f2-115">Требование</span><span class="sxs-lookup"><span data-stu-id="310f2-115">Requirement</span></span> | <span data-ttu-id="310f2-116">Значение</span><span class="sxs-lookup"><span data-stu-id="310f2-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="310f2-117">Header</span><span class="sxs-lookup"><span data-stu-id="310f2-117">Header</span></span><br/>  | <dl> <span data-ttu-id="310f2-118"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="310f2-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="310f2-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="310f2-119">Library</span></span><br/> | <dl> <span data-ttu-id="310f2-120"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="310f2-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="310f2-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="310f2-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="310f2-122">**Класс Кмедиаконтрол**</span><span class="sxs-lookup"><span data-stu-id="310f2-122">**CMediaControl Class**</span></span>](cmediacontrol.md)
</dt> </dl>

 

 




