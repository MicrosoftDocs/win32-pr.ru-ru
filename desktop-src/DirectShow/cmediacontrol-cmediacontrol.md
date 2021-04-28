---
description: Метод конструктора Кмедиаконтрол. Кмедиаконтрол.
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
ms.openlocfilehash: 96775678a8d182a3dc88f25fc19b194367c57d92
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099212"
---
# <a name="cmediacontrolcmediacontrol-constructor"></a><span data-ttu-id="3c8f1-103">Кмедиаконтрол. Кмедиаконтрол, конструктор</span><span class="sxs-lookup"><span data-stu-id="3c8f1-103">CMediaControl.CMediaControl constructor</span></span>

<span data-ttu-id="3c8f1-104">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="3c8f1-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c8f1-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3c8f1-105">Syntax</span></span>


```C++
CMediaControl(
   const TCHAR     *pName,
         LPUNKNOWN pUnk
);
```



## <a name="parameters"></a><span data-ttu-id="3c8f1-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3c8f1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c8f1-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="3c8f1-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="3c8f1-108">Указатель на имя объекта для целей отладки.</span><span class="sxs-lookup"><span data-stu-id="3c8f1-108">Pointer to the name of the object for debugging purposes.</span></span>

</dd> <dt>

<span data-ttu-id="3c8f1-109">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="3c8f1-109">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="3c8f1-110">Указатель на владельца этого объекта.</span><span class="sxs-lookup"><span data-stu-id="3c8f1-110">Pointer to the owner of this object.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3c8f1-111">Remarks</span><span class="sxs-lookup"><span data-stu-id="3c8f1-111">Remarks</span></span>

<span data-ttu-id="3c8f1-112">Выделите параметр *pName* в статической памяти.</span><span class="sxs-lookup"><span data-stu-id="3c8f1-112">Allocate the *pName* parameter in static memory.</span></span> <span data-ttu-id="3c8f1-113">Это имя отображается в терминале отладки при создании и удалении объекта.</span><span class="sxs-lookup"><span data-stu-id="3c8f1-113">This name appears on the debugging terminal upon creation and deletion of the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c8f1-114">Требования</span><span class="sxs-lookup"><span data-stu-id="3c8f1-114">Requirements</span></span>



| <span data-ttu-id="3c8f1-115">Требование</span><span class="sxs-lookup"><span data-stu-id="3c8f1-115">Requirement</span></span> | <span data-ttu-id="3c8f1-116">Значение</span><span class="sxs-lookup"><span data-stu-id="3c8f1-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c8f1-117">Header</span><span class="sxs-lookup"><span data-stu-id="3c8f1-117">Header</span></span><br/>  | <dl> <span data-ttu-id="3c8f1-118"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3c8f1-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="3c8f1-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="3c8f1-119">Library</span></span><br/> | <dl> <span data-ttu-id="3c8f1-120"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="3c8f1-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c8f1-121">См. также</span><span class="sxs-lookup"><span data-stu-id="3c8f1-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c8f1-122">**Класс Кмедиаконтрол**</span><span class="sxs-lookup"><span data-stu-id="3c8f1-122">**CMediaControl Class**</span></span>](cmediacontrol.md)
</dt> </dl>

 

 




