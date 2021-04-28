---
description: Метод конструктора Кбасеобжект. Кбасеобжект.
ms.assetid: 20c3c4af-b22f-4b74-a6b6-5ee309de4eef
title: Конструктор Кбасеобжект. Кбасеобжект (Комбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseObject.CBaseObject
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 14fa2d3d38d42fa0feb387b477205cc51e0b6b87
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099622"
---
# <a name="cbaseobjectcbaseobject-constructor"></a><span data-ttu-id="163bd-103">Кбасеобжект. Кбасеобжект, конструктор</span><span class="sxs-lookup"><span data-stu-id="163bd-103">CBaseObject.CBaseObject constructor</span></span>

<span data-ttu-id="163bd-104">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="163bd-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="163bd-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="163bd-105">Syntax</span></span>


```C++
CBaseObject(
   const TCHAR *pName
);
```



## <a name="parameters"></a><span data-ttu-id="163bd-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="163bd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="163bd-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="163bd-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="163bd-108">Строка, содержащая имя объекта для целей отладки.</span><span class="sxs-lookup"><span data-stu-id="163bd-108">String that contains the name of the object, for debugging purposes.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="163bd-109">Remarks</span><span class="sxs-lookup"><span data-stu-id="163bd-109">Remarks</span></span>

<span data-ttu-id="163bd-110">Этот метод увеличивает число активных объектов.</span><span class="sxs-lookup"><span data-stu-id="163bd-110">This method increments the active-object count.</span></span> <span data-ttu-id="163bd-111">(См. [**кбасеобжект:: обжектсактиве**](cbaseobject-objectsactive.md).)</span><span class="sxs-lookup"><span data-stu-id="163bd-111">(See [**CBaseObject::ObjectsActive**](cbaseobject-objectsactive.md).)</span></span>

<span data-ttu-id="163bd-112">Выделить параметр *pName* в статической памяти:</span><span class="sxs-lookup"><span data-stu-id="163bd-112">Allocate the *pName* parameter in static memory:</span></span>


```C++
// Correct.
CBaseObject *pObject = new CBaseObject(NAME("My Object"));

// Incorrect.
TCHAR ObjectName[] = TEXT("My Object");
CBaseObject *pObject = new CObject(ObjectName);
```



<span data-ttu-id="163bd-113">Макрос [**Name**](name.md) компилируется в **значение NULL** в розничных сборках, чтобы статические строки отображались только в отладочных сборках.</span><span class="sxs-lookup"><span data-stu-id="163bd-113">The [**NAME**](name.md) macro compiles to **NULL** in retail builds, so that static strings appear only in debug builds.</span></span> <span data-ttu-id="163bd-114">Дополнительные сведения см. в разделе [**дбгдумпобжектрегистер**](dbgdumpobjectregister.md).</span><span class="sxs-lookup"><span data-stu-id="163bd-114">For more information, see [**DbgDumpObjectRegister**](dbgdumpobjectregister.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="163bd-115">Требования</span><span class="sxs-lookup"><span data-stu-id="163bd-115">Requirements</span></span>



| <span data-ttu-id="163bd-116">Требование</span><span class="sxs-lookup"><span data-stu-id="163bd-116">Requirement</span></span> | <span data-ttu-id="163bd-117">Значение</span><span class="sxs-lookup"><span data-stu-id="163bd-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="163bd-118">Header</span><span class="sxs-lookup"><span data-stu-id="163bd-118">Header</span></span><br/>  | <dl> <span data-ttu-id="163bd-119"><dt>Комбасе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="163bd-119"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="163bd-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="163bd-120">Library</span></span><br/> | <dl> <span data-ttu-id="163bd-121"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="163bd-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="163bd-122">См. также</span><span class="sxs-lookup"><span data-stu-id="163bd-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="163bd-123">**Класс Кбасеобжект**</span><span class="sxs-lookup"><span data-stu-id="163bd-123">**CBaseObject Class**</span></span>](cbaseobject.md)
</dt> </dl>

 

 




