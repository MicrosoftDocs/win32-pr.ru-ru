---
description: Происходит, когда пользователь щелкает элемент управления InkEdit.
ms.assetid: 99fd7ef0-02cf-4390-9026-00ef2bbc1e37
title: InkEdit. Click, событие (с. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55df62807ee78e0f083a301c83a756b4cffb729d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684206"
---
# <a name="inkeditclick-event"></a><span data-ttu-id="8198b-103">Событие InkEdit. Click</span><span class="sxs-lookup"><span data-stu-id="8198b-103">InkEdit.Click event</span></span>

<span data-ttu-id="8198b-104">Происходит, когда пользователь щелкает элемент управления [InkEdit](inkedit-control-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="8198b-104">Occurs when a user clicks the [InkEdit](inkedit-control-reference.md) control.</span></span>

## <a name="syntax"></a><span data-ttu-id="8198b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8198b-105">Syntax</span></span>


```C++
void Click();
```



## <a name="parameters"></a><span data-ttu-id="8198b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8198b-106">Parameters</span></span>

<span data-ttu-id="8198b-107">У этого события нет параметров.</span><span class="sxs-lookup"><span data-stu-id="8198b-107">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8198b-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8198b-108">Return value</span></span>

<span data-ttu-id="8198b-109">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="8198b-109">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8198b-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8198b-110">Remarks</span></span>

<span data-ttu-id="8198b-111">При щелчке элемента управления создаются события [**MouseDown**](inkedit-mousedown.md) и [**MouseUp**](inkedit-mouseup.md) в дополнение к событию Click.</span><span class="sxs-lookup"><span data-stu-id="8198b-111">Clicking a control generates [**MouseDown**](inkedit-mousedown.md) and [**MouseUp**](inkedit-mouseup.md) events in addition to the Click event.</span></span>

> [!Note]  
> <span data-ttu-id="8198b-112">Чтобы различать левую, правую и среднюю кнопки мыши, используйте события [**MouseDown**](inkedit-mousedown.md) и [**MouseUp**](inkedit-mouseup.md) .</span><span class="sxs-lookup"><span data-stu-id="8198b-112">To distinguish between the left, right, and middle mouse buttons, use the [**MouseDown**](inkedit-mousedown.md) and [**MouseUp**](inkedit-mouseup.md) events.</span></span>

 

<span data-ttu-id="8198b-113">Если в событии **Click** есть код, событие [**DblClick**](inkedit-dblclick.md) никогда не запустится, так как событие **Click** является первым событием для активации между двумя.</span><span class="sxs-lookup"><span data-stu-id="8198b-113">If there is code in the **Click** event, the [**DblClick**](inkedit-dblclick.md) event will never trigger, because the **Click** event is the first event to trigger between the two.</span></span> <span data-ttu-id="8198b-114">В результате нажатие кнопки мыши перехватывается событием **нажатия** , поэтому событие **DblClick** не возникает.</span><span class="sxs-lookup"><span data-stu-id="8198b-114">As a result, the mouse click is intercepted by the **Click** event, so the **DblClick** event doesn't occur.</span></span>

<span data-ttu-id="8198b-115">Этот метод события определен в интерфейсе **\_ иинкедитевентс** .</span><span class="sxs-lookup"><span data-stu-id="8198b-115">This event method is defined in the **\_IInkEditEvents** interface.</span></span> <span data-ttu-id="8198b-116">Интерфейс **\_ иинкедитевентс** реализует интерфейс IDispatch с идентификатором **DISPID \_ иикликк**.</span><span class="sxs-lookup"><span data-stu-id="8198b-116">The **\_IInkEditEvents** interface implements the IDispatch interface with an identifier of **DISPID\_IeeClick**.</span></span>

## <a name="requirements"></a><span data-ttu-id="8198b-117">Требования</span><span class="sxs-lookup"><span data-stu-id="8198b-117">Requirements</span></span>



| <span data-ttu-id="8198b-118">Требование</span><span class="sxs-lookup"><span data-stu-id="8198b-118">Requirement</span></span> | <span data-ttu-id="8198b-119">Значение</span><span class="sxs-lookup"><span data-stu-id="8198b-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8198b-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8198b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="8198b-121">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="8198b-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="8198b-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8198b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="8198b-123">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="8198b-123">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="8198b-124">Header</span><span class="sxs-lookup"><span data-stu-id="8198b-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="8198b-125"><dt>«С». h (также требует \_ ввода i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="8198b-125"><dt>Inked.h (also requires inked\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="8198b-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="8198b-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="8198b-127"><dt>InkEd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8198b-127"><dt>InkEd.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="8198b-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8198b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8198b-129">InkEdit</span><span class="sxs-lookup"><span data-stu-id="8198b-129">InkEdit</span></span>](inkedit-control-reference.md)
</dt> </dl>

 

 




