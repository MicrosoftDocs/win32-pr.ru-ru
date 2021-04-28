---
description: Метод конструктора Кбасевиндов. Кбасевиндов.
ms.assetid: 9f0b91c4-0364-4c73-b97f-86703ca3ef74
title: Конструктор Кбасевиндов. Кбасевиндов (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.CBaseWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 05205750810294076bf005d0e5b73fda6b2143d5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095822"
---
# <a name="cbasewindowcbasewindow-constructor"></a><span data-ttu-id="bf893-103">Кбасевиндов. Кбасевиндов, конструктор</span><span class="sxs-lookup"><span data-stu-id="bf893-103">CBaseWindow.CBaseWindow constructor</span></span>

<span data-ttu-id="bf893-104">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="bf893-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf893-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bf893-105">Syntax</span></span>


```C++
CBaseWindow(
   BOOL bDoGetDC = TRUE,
   BOOL bPostToDestroy = FALSE
);
```



## <a name="parameters"></a><span data-ttu-id="bf893-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="bf893-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf893-107">*бдожетдк*</span><span class="sxs-lookup"><span data-stu-id="bf893-107">*bDoGetDC*</span></span> 
</dt> <dd>

<span data-ttu-id="bf893-108">Логическое значение, указывающее, следует ли извлекать контекст устройства.</span><span class="sxs-lookup"><span data-stu-id="bf893-108">Boolean value that specifies whether to retrieve the device context.</span></span>

</dd> <dt>

<span data-ttu-id="bf893-109">*бпосттодестрой*</span><span class="sxs-lookup"><span data-stu-id="bf893-109">*bPostToDestroy*</span></span> 
</dt> <dd>

<span data-ttu-id="bf893-110">Логическое значение, указывающее переменную члена [**кбасевиндов:: m \_ бдопосттодестрой**](cbasewindow-m-bdoposttodestroy.md) .</span><span class="sxs-lookup"><span data-stu-id="bf893-110">Boolean value that specifies the [**CBaseWindow::m\_bDoPostToDestroy**](cbasewindow-m-bdoposttodestroy.md) member variable.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bf893-111">Remarks</span><span class="sxs-lookup"><span data-stu-id="bf893-111">Remarks</span></span>

<span data-ttu-id="bf893-112">После создания объекта вызовите метод [**кбасевиндов::P репаревиндов**](cbasewindow-preparewindow.md) , чтобы создать окно.</span><span class="sxs-lookup"><span data-stu-id="bf893-112">After you create the object, call the [**CBaseWindow::PrepareWindow**](cbasewindow-preparewindow.md) method to create the window.</span></span> <span data-ttu-id="bf893-113">**Препаревиндов** является виртуальным методом.</span><span class="sxs-lookup"><span data-stu-id="bf893-113">**PrepareWindow** is a virtual method.</span></span> <span data-ttu-id="bf893-114">Он вызывает [**кбасевиндов:: инитиалисевиндов**](cbasewindow-initialisewindow.md), а также виртуальный метод.</span><span class="sxs-lookup"><span data-stu-id="bf893-114">It calls [**CBaseWindow::InitialiseWindow**](cbasewindow-initialisewindow.md), also a virtual method.</span></span> <span data-ttu-id="bf893-115">Эти методы отделены от конструктора, чтобы производные классы могли переопределять их при необходимости.</span><span class="sxs-lookup"><span data-stu-id="bf893-115">These methods are separated from the constructor so that derived classes can override them, if necessary.</span></span>

<span data-ttu-id="bf893-116">Если значение параметра *бдожетдк* равно **true**, `CBaseWindow` объект получает маркер для контекста устройства (DC) окна и сохраняет его в переменной члена [**кбасевиндов:: m \_ HDC**](cbasewindow-m-hdc.md) .</span><span class="sxs-lookup"><span data-stu-id="bf893-116">If the value of the *bDoGetDC* parameter is **TRUE**, the `CBaseWindow` object retrieves a handle to the window's device context (DC) and stores it in the [**CBaseWindow::m\_hdc**](cbasewindow-m-hdc.md) member variable.</span></span> <span data-ttu-id="bf893-117">Объект также создает совместимый с памятью контроллер домена, который хранится в переменной-члене [**кбасевиндов:: m \_ меморидк**](cbasewindow-m-memorydc.md) .</span><span class="sxs-lookup"><span data-stu-id="bf893-117">The object also creates a compatible memory DC, which it stores in the [**CBaseWindow::m\_MemoryDC**](cbasewindow-m-memorydc.md) member variable.</span></span> <span data-ttu-id="bf893-118">Эти действия выполняются в методе **инитиалисевиндов** .</span><span class="sxs-lookup"><span data-stu-id="bf893-118">These actions occur in the **InitialiseWindow** method.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf893-119">Требования</span><span class="sxs-lookup"><span data-stu-id="bf893-119">Requirements</span></span>



| <span data-ttu-id="bf893-120">Требование</span><span class="sxs-lookup"><span data-stu-id="bf893-120">Requirement</span></span> | <span data-ttu-id="bf893-121">Значение</span><span class="sxs-lookup"><span data-stu-id="bf893-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf893-122">Header</span><span class="sxs-lookup"><span data-stu-id="bf893-122">Header</span></span><br/>  | <dl> <span data-ttu-id="bf893-123"><dt>Винутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bf893-123"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="bf893-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="bf893-124">Library</span></span><br/> | <dl> <span data-ttu-id="bf893-125"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="bf893-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf893-126">См. также</span><span class="sxs-lookup"><span data-stu-id="bf893-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf893-127">**Класс Кбасевиндов**</span><span class="sxs-lookup"><span data-stu-id="bf893-127">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




