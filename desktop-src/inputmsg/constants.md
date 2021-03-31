---
title: Константы
description: В подразделах этого раздела приведены справочные спецификации для входных сообщений указателя и констант уведомлений.
ms.assetid: 2224DCD0-DAE1-4AC2-AB36-23D114803138
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 26fbcc479a339cee67e578803c6feed228736a90
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104069912"
---
# <a name="constants"></a><span data-ttu-id="00ae9-103">Константы</span><span class="sxs-lookup"><span data-stu-id="00ae9-103">Constants</span></span>

<span data-ttu-id="00ae9-104">В подразделах этого раздела приведены справочные спецификации для [входных сообщений указателя и констант уведомлений](messages-and-notifications-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="00ae9-104">The topics in this section provide the reference specifications for [Pointer Input Messages and Notifications](messages-and-notifications-portal.md) constants.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="00ae9-105">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="00ae9-105">In this section</span></span>



| <span data-ttu-id="00ae9-106">Раздел</span><span class="sxs-lookup"><span data-stu-id="00ae9-106">Topic</span></span>                                                                             | <span data-ttu-id="00ae9-107">Описание</span><span class="sxs-lookup"><span data-stu-id="00ae9-107">Description</span></span>                                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="00ae9-108">**Состояние клавиши модификатора**</span><span class="sxs-lookup"><span data-stu-id="00ae9-108">**Modifier Key State**</span></span>](modifier-key-states-constants.md)<br/>            | <span data-ttu-id="00ae9-109">Указывает, какие клавиши модификатора клавиатуры были нажаты во время создания входных данных.</span><span class="sxs-lookup"><span data-stu-id="00ae9-109">Indicates which keyboard modifier keys were pressed at the time input was being generated.</span></span><br/>                                                                                                       |
| [<span data-ttu-id="00ae9-110">**Флаги пера**</span><span class="sxs-lookup"><span data-stu-id="00ae9-110">**Pen Flags**</span></span>](pen-flags-constants.md)<br/>                               | <span data-ttu-id="00ae9-111">Значения, которые могут отображаться в поле **пенфлагс** структуры [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="00ae9-111">Values that can appear in the **penFlags** field of the [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) structure.</span></span><br/>                                                                         |
| [<span data-ttu-id="00ae9-112">**Маска пера**</span><span class="sxs-lookup"><span data-stu-id="00ae9-112">**Pen Mask**</span></span>](pen-mask-constants.md)<br/>                                 | <span data-ttu-id="00ae9-113">Значения, которые могут отображаться в поле **пенмаск** структуры [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="00ae9-113">Values that can appear in the **penMask** field of the [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) structure.</span></span><br/>                                                                          |
| [<span data-ttu-id="00ae9-114">**Изменение указателя в устройстве**</span><span class="sxs-lookup"><span data-stu-id="00ae9-114">**Pointer Device Change**</span></span>](pointer-device-change-constants.md)<br/>       | <span data-ttu-id="00ae9-115">Значения, которые могут быть переданы в параметре *wParam* сообщения [**WM_POINTERDEVICECHANGE**](wm-pointerdevicechange.md) .</span><span class="sxs-lookup"><span data-stu-id="00ae9-115">Values that can be passed in the *wParam* parameter of the [**WM_POINTERDEVICECHANGE**](wm-pointerdevicechange.md) message.</span></span><br/>                                                                    |
| [<span data-ttu-id="00ae9-116">**Флаги указателя**</span><span class="sxs-lookup"><span data-stu-id="00ae9-116">**Pointer Flags**</span></span>](pointer-flags-contants.md)<br/>                        | <span data-ttu-id="00ae9-117">Значения, которые могут отображаться в поле **поинтерфлагс** структуры [**POINTER_INFO**](/previous-versions/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="00ae9-117">Values that can appear in the **pointerFlags** field of the [**POINTER_INFO**](/previous-versions/windows/desktop/api) structure.</span></span><br/>                                                                              |
| [<span data-ttu-id="00ae9-118">**Флаги сообщения указателя**</span><span class="sxs-lookup"><span data-stu-id="00ae9-118">**Pointer Message Flags**</span></span>](pointer-message-flags.md)<br/>                 | <span data-ttu-id="00ae9-119">Значения, используемые в различных макросах указателя (см. [макросы](macros.md)).</span><span class="sxs-lookup"><span data-stu-id="00ae9-119">Values that are used in various pointer macros (see [Macros](macros.md)).</span></span><br/>                                                                                                                       |
| [<span data-ttu-id="00ae9-120">**Сенсорные флаги**</span><span class="sxs-lookup"><span data-stu-id="00ae9-120">**Touch Flags**</span></span>](touch-flags-constants.md)<br/>                           | <span data-ttu-id="00ae9-121">Значения, которые могут отображаться в поле **таучфлагс** структуры [**POINTER_TOUCH_INFO**](/previous-versions/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="00ae9-121">Values that can appear in the **touchFlags** field of the [**POINTER_TOUCH_INFO**](/previous-versions/windows/desktop/api) structure.</span></span><br/>                                                                   |
| [<span data-ttu-id="00ae9-122">**Окно проверки нажатия касания**</span><span class="sxs-lookup"><span data-stu-id="00ae9-122">**Touch Hit Testing Window**</span></span>](touch-hit-testing-window-constants.md)<br/> | <span data-ttu-id="00ae9-123">Указывает, как сообщения для проверки попадания касания обрабатываются окнами, зарегистрированными с помощью функции [**регистертаучхиттестингвиндов**](/windows/win32/api/winuser/nf-winuser-registertouchhittestingwindow) .</span><span class="sxs-lookup"><span data-stu-id="00ae9-123">Indicates how messages for touch hit testing are processed by windows that are registered through the [**RegisterTouchHitTestingWindow**](/windows/win32/api/winuser/nf-winuser-registertouchhittestingwindow) function.</span></span><br/> |
| [<span data-ttu-id="00ae9-124">**Маска касания**</span><span class="sxs-lookup"><span data-stu-id="00ae9-124">**Touch Mask**</span></span>](touch-mask-constants.md)<br/>                             | <span data-ttu-id="00ae9-125">Значения, которые могут отображаться в поле **таучмаск** структуры [**POINTER_TOUCH_INFO**](/previous-versions/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="00ae9-125">Values that can appear in the **touchMask** field of the [**POINTER_TOUCH_INFO**](/previous-versions/windows/desktop/api) structure.</span></span><br/>                                                                    |



 

## <a name="related-topics"></a><span data-ttu-id="00ae9-126">См. также</span><span class="sxs-lookup"><span data-stu-id="00ae9-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="00ae9-127">Ссылка на входящее сообщение указателя</span><span class="sxs-lookup"><span data-stu-id="00ae9-127">Pointer Input Message Reference</span></span>](wmpointer-reference.md)
</dt> </dl>

 

