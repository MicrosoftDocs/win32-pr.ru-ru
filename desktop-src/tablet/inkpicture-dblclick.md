---
description: Происходит при двойном щелчке элемента управления InkPicture.
ms.assetid: 5b2a6413-d415-4bf1-a291-35f4c3c5a0dc
title: Событие InkPicture. DblClick (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48c3d9bb9125c8142186da969acf6ce03f5f76b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347885"
---
# <a name="inkpicturedblclick-event"></a><span data-ttu-id="e239c-103">Событие InkPicture. DblClick</span><span class="sxs-lookup"><span data-stu-id="e239c-103">InkPicture.DblClick event</span></span>

<span data-ttu-id="e239c-104">Происходит при двойном щелчке элемента управления [InkPicture](inkpicture-control-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="e239c-104">Occurs when the [InkPicture](inkpicture-control-reference.md) control is double-clicked.</span></span>

## <a name="syntax"></a><span data-ttu-id="e239c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e239c-105">Syntax</span></span>


```C++
void DblClick(
  [in, out] VARIANT_BOOL *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="e239c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e239c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e239c-107">*Отмена* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="e239c-107">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e239c-108">Следует ли отменять событие для родительского элемента управления.</span><span class="sxs-lookup"><span data-stu-id="e239c-108">Whether the event should be canceled for the parent control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e239c-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e239c-109">Return value</span></span>

<span data-ttu-id="e239c-110">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="e239c-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e239c-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e239c-111">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e239c-112">Чтобы различать левую, правую и среднюю кнопки мыши, используйте события [**MouseDown**](inkpicture-mousedown.md) и [**MouseUp**](inkpicture-mouseup.md) .</span><span class="sxs-lookup"><span data-stu-id="e239c-112">To distinguish between the left, right, and middle mouse buttons, use the [**MouseDown**](inkpicture-mousedown.md) and [**MouseUp**](inkpicture-mouseup.md) events.</span></span> <span data-ttu-id="e239c-113">Если в событии [**Click**](inkpicture-click.md) есть код, событие **DblClick** не запустится.</span><span class="sxs-lookup"><span data-stu-id="e239c-113">If there is code in the [**Click**](inkpicture-click.md) event, the **DblClick** event will never trigger.</span></span>

 

<span data-ttu-id="e239c-114">Этот метод события определен в интерфейсе **\_ иинкпиктуривентс** .</span><span class="sxs-lookup"><span data-stu-id="e239c-114">This event method is defined in the **\_IInkPictureEvents** interface.</span></span> <span data-ttu-id="e239c-115">Интерфейс **\_ иинкпиктуривентс** реализует интерфейс IDispatch с идентификатором **DISPID \_ ипедблкликк**.</span><span class="sxs-lookup"><span data-stu-id="e239c-115">The **\_IInkPictureEvents** interface implements the IDispatch interface with an identifier of **DISPID\_IPEDblClick**.</span></span>

## <a name="requirements"></a><span data-ttu-id="e239c-116">Требования</span><span class="sxs-lookup"><span data-stu-id="e239c-116">Requirements</span></span>



| <span data-ttu-id="e239c-117">Требование</span><span class="sxs-lookup"><span data-stu-id="e239c-117">Requirement</span></span> | <span data-ttu-id="e239c-118">Значение</span><span class="sxs-lookup"><span data-stu-id="e239c-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e239c-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e239c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e239c-120">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="e239c-120">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="e239c-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e239c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e239c-122">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="e239c-122">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="e239c-123">Header</span><span class="sxs-lookup"><span data-stu-id="e239c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="e239c-124"><dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="e239c-124"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="e239c-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e239c-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="e239c-126"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e239c-126"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="e239c-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e239c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e239c-128">InkPicture</span><span class="sxs-lookup"><span data-stu-id="e239c-128">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> </dl>

 

 




