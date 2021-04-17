---
description: Функция LoadOLEAut32 загружает библиотеку динамической компоновки (OleAut32.dll).
ms.assetid: af907341-1e2c-4c63-bf4e-d6c49b4f6a6e
title: Функция LoadOLEAut32 (Комбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LoadOLEAut32
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b23bad7e445eebc78ecf8a849ddde8fc23746131
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685132"
---
# <a name="loadoleaut32-function"></a><span data-ttu-id="c88c0-103">Функция LoadOLEAut32</span><span class="sxs-lookup"><span data-stu-id="c88c0-103">LoadOLEAut32 function</span></span>

<span data-ttu-id="c88c0-104">Функция **LoadOLEAut32** загружает библиотеку динамической компоновки (OleAut32.dll).</span><span class="sxs-lookup"><span data-stu-id="c88c0-104">The **LoadOLEAut32** function loads the Automation dynamic-link library (OleAut32.dll).</span></span>

## <a name="syntax"></a><span data-ttu-id="c88c0-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c88c0-105">Syntax</span></span>


```C++
HINSTANCE LoadOLEAut32(void);
```



## <a name="parameters"></a><span data-ttu-id="c88c0-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c88c0-106">Parameters</span></span>

<span data-ttu-id="c88c0-107">У этой функции нет параметров.</span><span class="sxs-lookup"><span data-stu-id="c88c0-107">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c88c0-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c88c0-108">Return value</span></span>

<span data-ttu-id="c88c0-109">Возвращает маркер для экземпляра библиотеки DLL службы автоматизации.</span><span class="sxs-lookup"><span data-stu-id="c88c0-109">Returns a handle to an Automation DLL instance.</span></span>

## <a name="remarks"></a><span data-ttu-id="c88c0-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c88c0-110">Remarks</span></span>

<span data-ttu-id="c88c0-111">Когда деструктор [**кбасеобжект**](cbaseobject.md) уничтожает объект, который загрузил OleAut32.dll, он выгружает библиотеку, если она все еще загружена.</span><span class="sxs-lookup"><span data-stu-id="c88c0-111">When the [**CBaseObject**](cbaseobject.md) destructor destroys the object that loaded OleAut32.dll, it will unload the library if it is still loaded.</span></span>

## <a name="requirements"></a><span data-ttu-id="c88c0-112">Требования</span><span class="sxs-lookup"><span data-stu-id="c88c0-112">Requirements</span></span>



| <span data-ttu-id="c88c0-113">Требование</span><span class="sxs-lookup"><span data-stu-id="c88c0-113">Requirement</span></span> | <span data-ttu-id="c88c0-114">Значение</span><span class="sxs-lookup"><span data-stu-id="c88c0-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c88c0-115">Header</span><span class="sxs-lookup"><span data-stu-id="c88c0-115">Header</span></span><br/>  | <dl> <span data-ttu-id="c88c0-116"><dt>Комбасе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c88c0-116"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c88c0-117">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c88c0-117">Library</span></span><br/> | <dl> <span data-ttu-id="c88c0-118"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="c88c0-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c88c0-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c88c0-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c88c0-120">**Вспомогательные функции COM**</span><span class="sxs-lookup"><span data-stu-id="c88c0-120">**COM Helper Functions**</span></span>](com-helper-functions.md)
</dt> </dl>

 

 




