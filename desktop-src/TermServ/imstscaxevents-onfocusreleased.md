---
title: Имстскаксевентс Онфокусрелеасед, метод
description: Вызывается при нажатии сочетания клавиш для фокуса в выпуске. Например, это событие вызывается, когда пользователь нажимает клавишу CTRL + ALT + стрелка влево или сочетание клавиш CTRL + ALT + стрелка вправо.
ms.assetid: f5d755b0-4b8f-4d62-8dc4-f6b63e3819e5
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Онфокусрелеасед
- Службы удаленных рабочих столов метода Онфокусрелеасед, интерфейс Имстскаксевентс
- Службы удаленных рабочих столов интерфейса Имстскаксевентс, метод Онфокусрелеасед
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnFocusReleased
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6eff03f95d4ebbb068bccbfd9f68a930c00f0b00
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681928"
---
# <a name="imstscaxeventsonfocusreleased-method"></a><span data-ttu-id="1a37e-107">Метод Имстскаксевентс:: Онфокусрелеасед</span><span class="sxs-lookup"><span data-stu-id="1a37e-107">IMsTscAxEvents::OnFocusReleased method</span></span>

<span data-ttu-id="1a37e-108">Вызывается при нажатии сочетания клавиш для фокуса в выпуске.</span><span class="sxs-lookup"><span data-stu-id="1a37e-108">Called when the release focus key combination is pressed.</span></span> <span data-ttu-id="1a37e-109">Например, это событие вызывается, когда пользователь нажимает клавишу CTRL + ALT + стрелка влево или сочетание клавиш CTRL + ALT + стрелка вправо.</span><span class="sxs-lookup"><span data-stu-id="1a37e-109">For example, this event is called when the user presses the CTRL+ALT+LEFT ARROW or the CTRL+ALT+RIGHT ARROW key combination.</span></span>

<span data-ttu-id="1a37e-110">Это событие позволяет контейнеру элемента управления ActiveX убрать элемент управления с элемента управления ActiveX.</span><span class="sxs-lookup"><span data-stu-id="1a37e-110">This event enables the ActiveX control container to take away control from the ActiveX control.</span></span> <span data-ttu-id="1a37e-111">Например, это полезно в ситуации, когда у вас нет мыши, а специальные сочетания клавиш, такие как ALT + TAB, перенаправляются на сервер.</span><span class="sxs-lookup"><span data-stu-id="1a37e-111">For example, this is useful in a scenario where you do not have a mouse, and special key combinations such as ALT+TAB are being redirected to the server.</span></span> <span data-ttu-id="1a37e-112">В этом случае нет способа вернуть фокус клавиатуры обратно на локальный рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="1a37e-112">In this case, you do not have a way to return the keyboard focus back to the local desktop.</span></span> <span data-ttu-id="1a37e-113">Однако с помощью сочетания клавиш CTRL + ALT + стрелка влево или CTRL + ALT + стрелка вправо контейнер ActiveX может прослушивать это событие и реагировать на него, отключив фокус от элемента управления ActiveX.</span><span class="sxs-lookup"><span data-stu-id="1a37e-113">However, with the CTRL+ALT+LEFT ARROW or the CTRL+ALT+RIGHT ARROW key combination, the ActiveX container can listen for this event and respond by taking focus away from the ActiveX control.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a37e-114">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1a37e-114">Syntax</span></span>


```C++
void OnFocusReleased(
  [in] INT iDirection
);
```



## <a name="parameters"></a><span data-ttu-id="1a37e-115">Параметры</span><span class="sxs-lookup"><span data-stu-id="1a37e-115">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a37e-116">*идиректион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1a37e-116">*iDirection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a37e-117">Параметр направления 1 (CTRL + ALT + стрелка вправо) или 1 (CTRL + ALT + стрелка влево).</span><span class="sxs-lookup"><span data-stu-id="1a37e-117">The direction parameter of 1 (CTRL+ALT+RIGHT ARROW) or  1 (CTRL+ALT+LEFT ARROW).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a37e-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1a37e-118">Return value</span></span>

<span data-ttu-id="1a37e-119">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="1a37e-119">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1a37e-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1a37e-120">Remarks</span></span>

<span data-ttu-id="1a37e-121">Это событие доступно, если на клиенте используется подключение к удаленному рабочему столу 6,0.</span><span class="sxs-lookup"><span data-stu-id="1a37e-121">This event is available when Remote Desktop Connection 6.0 is used on the client.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a37e-122">Требования</span><span class="sxs-lookup"><span data-stu-id="1a37e-122">Requirements</span></span>



| <span data-ttu-id="1a37e-123">Требование</span><span class="sxs-lookup"><span data-stu-id="1a37e-123">Requirement</span></span> | <span data-ttu-id="1a37e-124">Значение</span><span class="sxs-lookup"><span data-stu-id="1a37e-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1a37e-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1a37e-125">Minimum supported client</span></span><br/> | <span data-ttu-id="1a37e-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1a37e-126">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="1a37e-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1a37e-127">Minimum supported server</span></span><br/> | <span data-ttu-id="1a37e-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1a37e-128">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="1a37e-129">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="1a37e-129">Type library</span></span><br/>             | <dl> <span data-ttu-id="1a37e-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1a37e-130"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="1a37e-131">DLL</span><span class="sxs-lookup"><span data-stu-id="1a37e-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1a37e-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1a37e-132"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="1a37e-133">IID</span><span class="sxs-lookup"><span data-stu-id="1a37e-133">IID</span></span><br/>                      | <span data-ttu-id="1a37e-134">Имстскаксевентс определяется как 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="1a37e-134">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="1a37e-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1a37e-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a37e-136">**имстскаксевентс**</span><span class="sxs-lookup"><span data-stu-id="1a37e-136">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





