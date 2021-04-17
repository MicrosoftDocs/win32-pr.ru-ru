---
description: Происходит при двойном щелчке элемента управления InkEdit.
ms.assetid: 380499e4-8697-4823-8153-29f24b2f234c
title: Событие InkEdit. DblClick (с. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fee0ec42171c9abbe0c99691f881b99db512869
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684410"
---
# <a name="inkeditdblclick-event"></a><span data-ttu-id="6a877-103">Событие InkEdit. DblClick</span><span class="sxs-lookup"><span data-stu-id="6a877-103">InkEdit.DblClick event</span></span>

<span data-ttu-id="6a877-104">Происходит при двойном щелчке элемента управления [InkEdit](inkedit-control-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="6a877-104">Occurs when the [InkEdit](inkedit-control-reference.md) control is double-clicked.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a877-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6a877-105">Syntax</span></span>


```C++
void DblClick(
  [in, out] VARIANT_BOOL *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="6a877-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6a877-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a877-107">*Отмена* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="6a877-107">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6a877-108">**Вариант \_ Значение TRUE** , чтобы отменить событие для родительского элемента управления; в противном случае — **\_ значение false**.</span><span class="sxs-lookup"><span data-stu-id="6a877-108">**VARIANT\_TRUE** to cancel the event for the parent control; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a877-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6a877-109">Return value</span></span>

<span data-ttu-id="6a877-110">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="6a877-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6a877-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6a877-111">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="6a877-112">Чтобы различать левую, правую и среднюю кнопки мыши, используйте события [**MouseDown**](inkedit-mousedown.md) и [**MouseUp**](inkedit-mouseup.md) .</span><span class="sxs-lookup"><span data-stu-id="6a877-112">To distinguish between the left, right, and middle mouse buttons, use the [**MouseDown**](inkedit-mousedown.md) and [**MouseUp**](inkedit-mouseup.md) events.</span></span> <span data-ttu-id="6a877-113">Если в событии [**Click**](inkedit-click.md) есть код, событие **DblClick** не запустится.</span><span class="sxs-lookup"><span data-stu-id="6a877-113">If there is code in the [**Click**](inkedit-click.md) event, the **DblClick** event will never trigger.</span></span>

 

<span data-ttu-id="6a877-114">Этот метод события определен в интерфейсе **\_ иинкедитевентс** .</span><span class="sxs-lookup"><span data-stu-id="6a877-114">This event method is defined in the **\_IInkEditEvents** interface.</span></span> <span data-ttu-id="6a877-115">Интерфейс **\_ иинкедитевентс** реализует интерфейс IDispatch с идентификатором **DISPID \_ иидблкликк**.</span><span class="sxs-lookup"><span data-stu-id="6a877-115">The **\_IInkEditEvents** interface implements the IDispatch interface with an identifier of **DISPID\_IeeDblClick**.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a877-116">Требования</span><span class="sxs-lookup"><span data-stu-id="6a877-116">Requirements</span></span>



| <span data-ttu-id="6a877-117">Требование</span><span class="sxs-lookup"><span data-stu-id="6a877-117">Requirement</span></span> | <span data-ttu-id="6a877-118">Значение</span><span class="sxs-lookup"><span data-stu-id="6a877-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a877-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6a877-119">Minimum supported client</span></span><br/> | <span data-ttu-id="6a877-120">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="6a877-120">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="6a877-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6a877-121">Minimum supported server</span></span><br/> | <span data-ttu-id="6a877-122">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="6a877-122">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="6a877-123">Header</span><span class="sxs-lookup"><span data-stu-id="6a877-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="6a877-124"><dt>«С». h (также требует \_ ввода i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="6a877-124"><dt>Inked.h (also requires inked\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="6a877-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="6a877-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="6a877-126"><dt>InkEd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6a877-126"><dt>InkEd.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="6a877-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6a877-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a877-128">InkEdit</span><span class="sxs-lookup"><span data-stu-id="6a877-128">InkEdit</span></span>](inkedit-control-reference.md)
</dt> </dl>

 

 




