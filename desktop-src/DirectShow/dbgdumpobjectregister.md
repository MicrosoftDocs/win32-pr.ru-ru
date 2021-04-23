---
description: Функция Дбгдумпобжектрегистер отображает сведения об активных объектах. Игнорируется в розничных сборках.
ms.assetid: 362d9912-662c-4a72-95b4-01f3d808e299
title: Функция Дбгдумпобжектрегистер (Вксдебуг. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgDumpObjectRegister
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 727d9c00ebbe3d48bb46797a1e27b9dd27c7b2c0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657224"
---
# <a name="dbgdumpobjectregister-function"></a><span data-ttu-id="245fd-104">Функция Дбгдумпобжектрегистер</span><span class="sxs-lookup"><span data-stu-id="245fd-104">DbgDumpObjectRegister function</span></span>

<span data-ttu-id="245fd-105">`DbgDumpObjectRegister`Функция отображает сведения об активных объектах.</span><span class="sxs-lookup"><span data-stu-id="245fd-105">The `DbgDumpObjectRegister` function displays information about active objects.</span></span> <span data-ttu-id="245fd-106">Игнорируется в розничных сборках.</span><span class="sxs-lookup"><span data-stu-id="245fd-106">Ignored in retail builds.</span></span>

## <a name="syntax"></a><span data-ttu-id="245fd-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="245fd-107">Syntax</span></span>


```C++
void DbgDumpObjectRegister(void);
```



## <a name="parameters"></a><span data-ttu-id="245fd-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="245fd-108">Parameters</span></span>

<span data-ttu-id="245fd-109">У этой функции нет параметров.</span><span class="sxs-lookup"><span data-stu-id="245fd-109">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="245fd-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="245fd-110">Return value</span></span>

<span data-ttu-id="245fd-111">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="245fd-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="245fd-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="245fd-112">Remarks</span></span>

<span data-ttu-id="245fd-113">В отладочных сборках библиотека отладки поддерживает список активных объектов.</span><span class="sxs-lookup"><span data-stu-id="245fd-113">In debug builds, the debug library maintains a list of active objects.</span></span> <span data-ttu-id="245fd-114">Список включает все объекты, производные от [**кбасеобжект**](cbaseobject.md), которые были созданы текущим модулем и не были уничтожены.</span><span class="sxs-lookup"><span data-stu-id="245fd-114">The list includes any objects that derive from [**CBaseObject**](cbaseobject.md), were created by the current module, and have not been destroyed.</span></span> <span data-ttu-id="245fd-115">Конструктор **кбасеобжект** и методы деструктора обновляют список.</span><span class="sxs-lookup"><span data-stu-id="245fd-115">The **CBaseObject** constructor and destructor methods update the list.</span></span>

<span data-ttu-id="245fd-116">Эта функция создает несколько \_ сообщений в памяти журнала.</span><span class="sxs-lookup"><span data-stu-id="245fd-116">This function generates several LOG\_MEMORY messages.</span></span> <span data-ttu-id="245fd-117">При уровне ведения журнала 1 функция отображает только общее число объектов.</span><span class="sxs-lookup"><span data-stu-id="245fd-117">At logging level 1, the function displays only the total number of objects.</span></span> <span data-ttu-id="245fd-118">При уровне ведения журнала 2 или более поздней версии отображается список объектов.</span><span class="sxs-lookup"><span data-stu-id="245fd-118">At logging level 2 or higher, it displays a list of the objects.</span></span>

## <a name="requirements"></a><span data-ttu-id="245fd-119">Требования</span><span class="sxs-lookup"><span data-stu-id="245fd-119">Requirements</span></span>



| <span data-ttu-id="245fd-120">Требование</span><span class="sxs-lookup"><span data-stu-id="245fd-120">Requirement</span></span> | <span data-ttu-id="245fd-121">Значение</span><span class="sxs-lookup"><span data-stu-id="245fd-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="245fd-122">Header</span><span class="sxs-lookup"><span data-stu-id="245fd-122">Header</span></span><br/>  | <dl> <span data-ttu-id="245fd-123"><dt>Вксдебуг. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="245fd-123"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="245fd-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="245fd-124">Library</span></span><br/> | <dl> <span data-ttu-id="245fd-125"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="245fd-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="245fd-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="245fd-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="245fd-127">Выходные функции отладки</span><span class="sxs-lookup"><span data-stu-id="245fd-127">Debug Output Functions</span></span>](debug-output-functions.md)
</dt> </dl>

 

 




