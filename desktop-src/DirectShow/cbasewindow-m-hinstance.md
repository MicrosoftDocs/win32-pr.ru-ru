---
description: Обработчик для экземпляра модуля.
ms.assetid: ad889ebe-2bd8-4456-9517-9e2909697a02
title: 'Элемент Кбасевиндов:: m_hInstance (Винутил. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_hInstance
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6482aac80c1298ea403019f43ddc4effdc30b00a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657045"
---
# <a name="cbasewindowm_hinstance-member"></a><span data-ttu-id="b9102-103">Элемент Кбасевиндов:: m \_ HINSTANCE</span><span class="sxs-lookup"><span data-stu-id="b9102-103">CBaseWindow::m\_hInstance member</span></span>

<span data-ttu-id="b9102-104">Обработчик для экземпляра модуля.</span><span class="sxs-lookup"><span data-stu-id="b9102-104">Handle to the module instance.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9102-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b9102-105">Syntax</span></span>


```C++
HINSTANCE m_hInstance;
```



## <a name="remarks"></a><span data-ttu-id="b9102-106">Примечания</span><span class="sxs-lookup"><span data-stu-id="b9102-106">Remarks</span></span>

<span data-ttu-id="b9102-107">Функция точки входа библиотеки DLL задает глобальную переменную с помощью маркера экземпляра модуля.</span><span class="sxs-lookup"><span data-stu-id="b9102-107">The DLL entry point function sets a global variable with a handle to the module instance.</span></span> <span data-ttu-id="b9102-108">Класс **кбасевиндов** сохраняет этот обработчик в своем методе конструктора.</span><span class="sxs-lookup"><span data-stu-id="b9102-108">The **CBaseWindow** class stores this handle in its constructor method.</span></span>

## <a name="requirements"></a><span data-ttu-id="b9102-109">Требования</span><span class="sxs-lookup"><span data-stu-id="b9102-109">Requirements</span></span>



| <span data-ttu-id="b9102-110">Требование</span><span class="sxs-lookup"><span data-stu-id="b9102-110">Requirement</span></span> | <span data-ttu-id="b9102-111">Значение</span><span class="sxs-lookup"><span data-stu-id="b9102-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9102-112">Header</span><span class="sxs-lookup"><span data-stu-id="b9102-112">Header</span></span><br/>  | <dl> <span data-ttu-id="b9102-113"><dt>Винутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b9102-113"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b9102-114">Библиотека</span><span class="sxs-lookup"><span data-stu-id="b9102-114">Library</span></span><br/> | <dl> <span data-ttu-id="b9102-115"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="b9102-115"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b9102-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b9102-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9102-117">**Класс Кбасевиндов**</span><span class="sxs-lookup"><span data-stu-id="b9102-117">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




