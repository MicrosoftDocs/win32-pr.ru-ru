---
description: Метод конструктора.
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
ms.openlocfilehash: 4b13fe906af1900dbf067e8aa9273d811b3c1ef3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665152"
---
# <a name="cbaseobjectcbaseobject-constructor"></a><span data-ttu-id="5f07e-103">Кбасеобжект. Кбасеобжект, конструктор</span><span class="sxs-lookup"><span data-stu-id="5f07e-103">CBaseObject.CBaseObject constructor</span></span>

<span data-ttu-id="5f07e-104">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="5f07e-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f07e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5f07e-105">Syntax</span></span>


```C++
CBaseObject(
   const TCHAR *pName
);
```



## <a name="parameters"></a><span data-ttu-id="5f07e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5f07e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f07e-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="5f07e-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="5f07e-108">Строка, содержащая имя объекта для целей отладки.</span><span class="sxs-lookup"><span data-stu-id="5f07e-108">String that contains the name of the object, for debugging purposes.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5f07e-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5f07e-109">Remarks</span></span>

<span data-ttu-id="5f07e-110">Этот метод увеличивает число активных объектов.</span><span class="sxs-lookup"><span data-stu-id="5f07e-110">This method increments the active-object count.</span></span> <span data-ttu-id="5f07e-111">(См. [**кбасеобжект:: обжектсактиве**](cbaseobject-objectsactive.md).)</span><span class="sxs-lookup"><span data-stu-id="5f07e-111">(See [**CBaseObject::ObjectsActive**](cbaseobject-objectsactive.md).)</span></span>

<span data-ttu-id="5f07e-112">Выделить параметр *pName* в статической памяти:</span><span class="sxs-lookup"><span data-stu-id="5f07e-112">Allocate the *pName* parameter in static memory:</span></span>


```C++
// Correct.
CBaseObject *pObject = new CBaseObject(NAME("My Object"));

// Incorrect.
TCHAR ObjectName[] = TEXT("My Object");
CBaseObject *pObject = new CObject(ObjectName);
```



<span data-ttu-id="5f07e-113">Макрос [**Name**](name.md) компилируется в **значение NULL** в розничных сборках, чтобы статические строки отображались только в отладочных сборках.</span><span class="sxs-lookup"><span data-stu-id="5f07e-113">The [**NAME**](name.md) macro compiles to **NULL** in retail builds, so that static strings appear only in debug builds.</span></span> <span data-ttu-id="5f07e-114">Дополнительные сведения см. в разделе [**дбгдумпобжектрегистер**](dbgdumpobjectregister.md).</span><span class="sxs-lookup"><span data-stu-id="5f07e-114">For more information, see [**DbgDumpObjectRegister**](dbgdumpobjectregister.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5f07e-115">Требования</span><span class="sxs-lookup"><span data-stu-id="5f07e-115">Requirements</span></span>



| <span data-ttu-id="5f07e-116">Требование</span><span class="sxs-lookup"><span data-stu-id="5f07e-116">Requirement</span></span> | <span data-ttu-id="5f07e-117">Значение</span><span class="sxs-lookup"><span data-stu-id="5f07e-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f07e-118">Header</span><span class="sxs-lookup"><span data-stu-id="5f07e-118">Header</span></span><br/>  | <dl> <span data-ttu-id="5f07e-119"><dt>Комбасе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5f07e-119"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="5f07e-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="5f07e-120">Library</span></span><br/> | <dl> <span data-ttu-id="5f07e-121"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="5f07e-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f07e-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5f07e-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f07e-123">**Класс Кбасеобжект**</span><span class="sxs-lookup"><span data-stu-id="5f07e-123">**CBaseObject Class**</span></span>](cbaseobject.md)
</dt> </dl>

 

 




