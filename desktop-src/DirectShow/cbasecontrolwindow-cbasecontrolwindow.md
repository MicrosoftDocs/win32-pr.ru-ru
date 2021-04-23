---
description: Метод конструктора.
ms.assetid: 575f7f94-5f55-4834-bdb6-0db877187388
title: Конструктор Кбасеконтролвиндов. Кбасеконтролвиндов (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.CBaseControlWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9eb3e50daef8ec4ad11bf96a8f0b605f4c8fe679
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657059"
---
# <a name="cbasecontrolwindowcbasecontrolwindow-constructor"></a><span data-ttu-id="09e10-103">Кбасеконтролвиндов. Кбасеконтролвиндов, конструктор</span><span class="sxs-lookup"><span data-stu-id="09e10-103">CBaseControlWindow.CBaseControlWindow constructor</span></span>

<span data-ttu-id="09e10-104">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="09e10-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="09e10-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="09e10-105">Syntax</span></span>


```C++
CBaseControlWindow(
   CBaseMediaFilter *pFilter,
   CCritSec         *pInterfaceLock,
   TCHAR            *pName,
   LPUNKNOWN        pUnk,
   HRESULT          *phr
);
```



## <a name="parameters"></a><span data-ttu-id="09e10-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="09e10-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09e10-107">*пфилтер*</span><span class="sxs-lookup"><span data-stu-id="09e10-107">*pFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="09e10-108">Указатель на объект фильтра мультимедиа-владельца.</span><span class="sxs-lookup"><span data-stu-id="09e10-108">Pointer to the owning media filter object.</span></span>

</dd> <dt>

<span data-ttu-id="09e10-109">*пинтерфацелокк*</span><span class="sxs-lookup"><span data-stu-id="09e10-109">*pInterfaceLock*</span></span> 
</dt> <dd>

<span data-ttu-id="09e10-110">Указатель на критическую секцию, используемую для блокировки.</span><span class="sxs-lookup"><span data-stu-id="09e10-110">Pointer to the critical section to use for locking.</span></span>

</dd> <dt>

<span data-ttu-id="09e10-111">*pName*</span><span class="sxs-lookup"><span data-stu-id="09e10-111">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="09e10-112">Указатель на описание объекта.</span><span class="sxs-lookup"><span data-stu-id="09e10-112">Pointer to the object description.</span></span>

</dd> <dt>

<span data-ttu-id="09e10-113">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="09e10-113">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="09e10-114">Указатель на управляющий интерфейс **IUnknown** , если объект является частью статистической функции; в противном случае **значение должно быть равно NULL**.</span><span class="sxs-lookup"><span data-stu-id="09e10-114">Pointer to the controlling **IUnknown** interface, if the object is part of an aggregate; otherwise, must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="09e10-115">*фр*</span><span class="sxs-lookup"><span data-stu-id="09e10-115">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="09e10-116">Указатель на переменную, которая получает значение HRESULT, указывающее на успешность или ошибку метода конструктора.</span><span class="sxs-lookup"><span data-stu-id="09e10-116">Pointer to a variable that receives an HRESULT value indicating the success or failure of the constructor method.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="09e10-117">Требования</span><span class="sxs-lookup"><span data-stu-id="09e10-117">Requirements</span></span>



| <span data-ttu-id="09e10-118">Требование</span><span class="sxs-lookup"><span data-stu-id="09e10-118">Requirement</span></span> | <span data-ttu-id="09e10-119">Значение</span><span class="sxs-lookup"><span data-stu-id="09e10-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="09e10-120">Header</span><span class="sxs-lookup"><span data-stu-id="09e10-120">Header</span></span><br/>  | <dl> <span data-ttu-id="09e10-121"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="09e10-121"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="09e10-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="09e10-122">Library</span></span><br/> | <dl> <span data-ttu-id="09e10-123"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="09e10-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09e10-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="09e10-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09e10-125">**Класс Кбасеконтролвиндов**</span><span class="sxs-lookup"><span data-stu-id="09e10-125">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




