---
description: Происходит, когда пользователь щелкает элемент управления InkPicture.
ms.assetid: 326bac37-2d5d-434b-916c-8a675bab5052
title: Событие InkPicture. Click (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1dd90cd69555f65531f5ab2684f886dab23e191
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912347"
---
# <a name="inkpictureclick-event"></a><span data-ttu-id="1c54c-103">Событие InkPicture. Click</span><span class="sxs-lookup"><span data-stu-id="1c54c-103">InkPicture.Click event</span></span>

<span data-ttu-id="1c54c-104">Происходит, когда пользователь щелкает элемент управления [InkPicture](inkpicture-control-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="1c54c-104">Occurs when a user clicks the [InkPicture](inkpicture-control-reference.md) control.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c54c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1c54c-105">Syntax</span></span>


```C++
void Click();
```



## <a name="parameters"></a><span data-ttu-id="1c54c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1c54c-106">Parameters</span></span>

<span data-ttu-id="1c54c-107">У этого события нет параметров.</span><span class="sxs-lookup"><span data-stu-id="1c54c-107">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1c54c-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1c54c-108">Return value</span></span>

<span data-ttu-id="1c54c-109">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="1c54c-109">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1c54c-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1c54c-110">Remarks</span></span>

<span data-ttu-id="1c54c-111">При щелчке элемента управления создаются события [**MouseDown**](inkpicture-mousedown.md) и [**MouseUp**](inkpicture-mouseup.md) в дополнение к событию Click.</span><span class="sxs-lookup"><span data-stu-id="1c54c-111">Clicking a control generates [**MouseDown**](inkpicture-mousedown.md) and [**MouseUp**](inkpicture-mouseup.md) events in addition to the Click event.</span></span>

> [!Note]  
> <span data-ttu-id="1c54c-112">Чтобы различать левую, правую и среднюю кнопки мыши, используйте события [**MouseDown**](inkpicture-mousedown.md) и [**MouseUp**](inkpicture-mouseup.md) .</span><span class="sxs-lookup"><span data-stu-id="1c54c-112">To distinguish between the left, right, and middle mouse buttons, use the [**MouseDown**](inkpicture-mousedown.md) and [**MouseUp**](inkpicture-mouseup.md) events.</span></span>

 

<span data-ttu-id="1c54c-113">Если в событии **Click** есть код, событие [**DblClick**](inkpicture-dblclick.md) никогда не запустится, так как событие **Click** является первым событием для активации между двумя.</span><span class="sxs-lookup"><span data-stu-id="1c54c-113">If there is code in the **Click** event, the [**DblClick**](inkpicture-dblclick.md) event will never trigger, because the **Click** event is the first event to trigger between the two.</span></span> <span data-ttu-id="1c54c-114">В результате нажатие кнопки мыши перехватывается событием **нажатия** , поэтому событие **DblClick** не возникает.</span><span class="sxs-lookup"><span data-stu-id="1c54c-114">As a result, the mouse click is intercepted by the **Click** event, so the **DblClick** event doesn't occur.</span></span>

<span data-ttu-id="1c54c-115">Этот метод события определен в интерфейсе **\_ иинкпиктуривентс** .</span><span class="sxs-lookup"><span data-stu-id="1c54c-115">This event method is defined in the **\_IInkPictureEvents** interface.</span></span> <span data-ttu-id="1c54c-116">Интерфейс **\_ иинкпиктуривентс** реализует интерфейс IDispatch с идентификатором **DISPID \_ ипекликк**.</span><span class="sxs-lookup"><span data-stu-id="1c54c-116">The **\_IInkPictureEvents** interface implements the IDispatch interface with an identifier of **DISPID\_IPEClick**.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c54c-117">Требования</span><span class="sxs-lookup"><span data-stu-id="1c54c-117">Requirements</span></span>



| <span data-ttu-id="1c54c-118">Требование</span><span class="sxs-lookup"><span data-stu-id="1c54c-118">Requirement</span></span> | <span data-ttu-id="1c54c-119">Значение</span><span class="sxs-lookup"><span data-stu-id="1c54c-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c54c-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1c54c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="1c54c-121">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="1c54c-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="1c54c-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1c54c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="1c54c-123">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="1c54c-123">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="1c54c-124">Header</span><span class="sxs-lookup"><span data-stu-id="1c54c-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="1c54c-125"><dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="1c54c-125"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="1c54c-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="1c54c-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="1c54c-127"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1c54c-127"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="1c54c-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1c54c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c54c-129">InkPicture</span><span class="sxs-lookup"><span data-stu-id="1c54c-129">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> </dl>

 

 




