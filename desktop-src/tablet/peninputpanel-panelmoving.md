---
description: Не рекомендуется. Пенинпутпанел был заменен панелью ввода текста (TIP). Происходит при перемещении объекта Пенинпутпанел.
ms.assetid: 0c51d875-cef9-4087-b17d-5c5af04f81a5
title: Событие Пенинпутпанел. Панелмовинг (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7be69e227188739cb656e6a1eb471716e1aa4feb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693723"
---
# <a name="peninputpanelpanelmoving-event"></a><span data-ttu-id="ee3d9-104">Пенинпутпанел. Панелмовинг, событие</span><span class="sxs-lookup"><span data-stu-id="ee3d9-104">PenInputPanel.PanelMoving event</span></span>

<span data-ttu-id="ee3d9-105">Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="ee3d9-105">Deprecated.</span></span> <span data-ttu-id="ee3d9-106">[**Пенинпутпанел**](peninputpanel-class.md) был заменен [панелью ввода текста (TIP)](text-input-panel-reference.md).</span><span class="sxs-lookup"><span data-stu-id="ee3d9-106">The [**PenInputPanel**](peninputpanel-class.md) has been replaced by the [Text Input Panel (TIP)](text-input-panel-reference.md).</span></span>

<span data-ttu-id="ee3d9-107">Происходит при перемещении объекта [**пенинпутпанел**](peninputpanel-class.md) .</span><span class="sxs-lookup"><span data-stu-id="ee3d9-107">Occurs when the [**PenInputPanel**](peninputpanel-class.md) object is moving.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee3d9-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ee3d9-108">Syntax</span></span>


```C++
HRESULT PanelMoving(
  [in, out] long *Left,
  [in, out] long *Top
);
```



## <a name="parameters"></a><span data-ttu-id="ee3d9-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="ee3d9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee3d9-110">По *левому краю* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="ee3d9-110">*Left* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ee3d9-111">Новая горизонтальная ось, или оси x, Расположение левого края объекта [**пенинпутпанел**](peninputpanel-class.md) в экранных координатах.</span><span class="sxs-lookup"><span data-stu-id="ee3d9-111">The new horizontal, or x-axis, position of the left edge of the [**PenInputPanel**](peninputpanel-class.md) object, in screen coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="ee3d9-112">В *Начало* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="ee3d9-112">*Top* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ee3d9-113">Новая вертикальная ось, или оси y, Расположение левого края объекта [**пенинпутпанел**](peninputpanel-class.md) в экранных координатах.</span><span class="sxs-lookup"><span data-stu-id="ee3d9-113">The new vertical, or y-axis, position of the left edge of the [**PenInputPanel**](peninputpanel-class.md) object, in screen coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee3d9-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ee3d9-114">Return value</span></span>

<span data-ttu-id="ee3d9-115">Если это событие завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="ee3d9-115">If this event succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ee3d9-116">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ee3d9-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="ee3d9-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ee3d9-117">Remarks</span></span>

<span data-ttu-id="ee3d9-118">Событие **панелмовинг** предназначено для изменения расположения панели ввода с помощью пера путем изменения параметров *Left* и *Top* .</span><span class="sxs-lookup"><span data-stu-id="ee3d9-118">The **PanelMoving** event is designed to be used to change the position of the pen input panel by changing the *Left* and *Top* parameters.</span></span>

<span data-ttu-id="ee3d9-119">Методы [**MoveTo**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-moveto) и [**Refresh**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-refresh) приводят к тому, что объект [**пенинпутпанел**](peninputpanel-class.md) вызывает его код автоматического позиционирования, который активирует событие **панелмовинг** .</span><span class="sxs-lookup"><span data-stu-id="ee3d9-119">The [**MoveTo**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-moveto) and [**Refresh**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-refresh) methods cause the [**PenInputPanel**](peninputpanel-class.md) object to call its auto-positioning code which triggers a **PanelMoving** event.</span></span> <span data-ttu-id="ee3d9-120">Следовательно, вызов этих методов внутри обработчика **панелмовинг** может привести к созданию рекурсивного бесконечного цикла.</span><span class="sxs-lookup"><span data-stu-id="ee3d9-120">Consequently, calling these methods inside a **PanelMoving** handler can result in a recursive endless loop.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee3d9-121">Требования</span><span class="sxs-lookup"><span data-stu-id="ee3d9-121">Requirements</span></span>



| <span data-ttu-id="ee3d9-122">Требование</span><span class="sxs-lookup"><span data-stu-id="ee3d9-122">Requirement</span></span> | <span data-ttu-id="ee3d9-123">Значение</span><span class="sxs-lookup"><span data-stu-id="ee3d9-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee3d9-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ee3d9-124">Minimum supported client</span></span><br/> | <span data-ttu-id="ee3d9-125">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="ee3d9-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="ee3d9-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ee3d9-126">Minimum supported server</span></span><br/> | <span data-ttu-id="ee3d9-127">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="ee3d9-127">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="ee3d9-128">Header</span><span class="sxs-lookup"><span data-stu-id="ee3d9-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="ee3d9-129"><dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="ee3d9-129"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="ee3d9-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ee3d9-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="ee3d9-131"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ee3d9-131"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="ee3d9-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ee3d9-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee3d9-133">**пенинпутпанел**</span><span class="sxs-lookup"><span data-stu-id="ee3d9-133">**PenInputPanel**</span></span>](peninputpanel-class.md)
</dt> </dl>

 

 




