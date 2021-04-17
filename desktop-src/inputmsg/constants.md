---
title: Входные сообщения указателя и константы уведомлений
description: В подразделах этого раздела приведены справочные спецификации для входных сообщений указателя и констант уведомлений.
ms.assetid: 2224DCD0-DAE1-4AC2-AB36-23D114803138
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 6db54614e10c02cea5dfd4df9b7cf637abb3977c
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/02/2021
ms.locfileid: "106188033"
---
# <a name="pointer-input-messages-and-notifications-constants"></a><span data-ttu-id="2053e-103">Входные сообщения указателя и константы уведомлений</span><span class="sxs-lookup"><span data-stu-id="2053e-103">Pointer Input Messages and Notifications constants</span></span>

<span data-ttu-id="2053e-104">В подразделах этого раздела приведены справочные спецификации для [входных сообщений указателя и констант уведомлений](messages-and-notifications-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="2053e-104">The topics in this section provide the reference specifications for [Pointer Input Messages and Notifications](messages-and-notifications-portal.md) constants.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="2053e-105">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="2053e-105">In this section</span></span>



| <span data-ttu-id="2053e-106">Раздел</span><span class="sxs-lookup"><span data-stu-id="2053e-106">Topic</span></span>                                                                             | <span data-ttu-id="2053e-107">Описание</span><span class="sxs-lookup"><span data-stu-id="2053e-107">Description</span></span>                                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2053e-108">**Состояние клавиши модификатора**</span><span class="sxs-lookup"><span data-stu-id="2053e-108">**Modifier Key State**</span></span>](modifier-key-states-constants.md)<br/>            | <span data-ttu-id="2053e-109">Указывает, какие клавиши модификатора клавиатуры были нажаты во время создания входных данных.</span><span class="sxs-lookup"><span data-stu-id="2053e-109">Indicates which keyboard modifier keys were pressed at the time input was being generated.</span></span><br/>                                                                                                       |
| [<span data-ttu-id="2053e-110">**Флаги пера**</span><span class="sxs-lookup"><span data-stu-id="2053e-110">**Pen Flags**</span></span>](pen-flags-constants.md)<br/>                               | <span data-ttu-id="2053e-111">Значения, которые могут отображаться в поле **пенфлагс** структуры [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="2053e-111">Values that can appear in the **penFlags** field of the [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) structure.</span></span><br/>                                                                         |
| [<span data-ttu-id="2053e-112">**Маска пера**</span><span class="sxs-lookup"><span data-stu-id="2053e-112">**Pen Mask**</span></span>](pen-mask-constants.md)<br/>                                 | <span data-ttu-id="2053e-113">Значения, которые могут отображаться в поле **пенмаск** структуры [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="2053e-113">Values that can appear in the **penMask** field of the [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) structure.</span></span><br/>                                                                          |
| [<span data-ttu-id="2053e-114">**Изменение указателя в устройстве**</span><span class="sxs-lookup"><span data-stu-id="2053e-114">**Pointer Device Change**</span></span>](pointer-device-change-constants.md)<br/>       | <span data-ttu-id="2053e-115">Значения, которые могут быть переданы в параметре *wParam* сообщения [**WM_POINTERDEVICECHANGE**](wm-pointerdevicechange.md) .</span><span class="sxs-lookup"><span data-stu-id="2053e-115">Values that can be passed in the *wParam* parameter of the [**WM_POINTERDEVICECHANGE**](wm-pointerdevicechange.md) message.</span></span><br/>                                                                    |
| [<span data-ttu-id="2053e-116">**Флаги указателя**</span><span class="sxs-lookup"><span data-stu-id="2053e-116">**Pointer Flags**</span></span>](pointer-flags-contants.md)<br/>                        | <span data-ttu-id="2053e-117">Значения, которые могут отображаться в поле **поинтерфлагс** структуры [**POINTER_INFO**](/previous-versions/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="2053e-117">Values that can appear in the **pointerFlags** field of the [**POINTER_INFO**](/previous-versions/windows/desktop/api) structure.</span></span><br/>                                                                              |
| [<span data-ttu-id="2053e-118">**Флаги сообщения указателя**</span><span class="sxs-lookup"><span data-stu-id="2053e-118">**Pointer Message Flags**</span></span>](pointer-message-flags.md)<br/>                 | <span data-ttu-id="2053e-119">Значения, используемые в различных макросах указателя (см. [макросы](macros.md)).</span><span class="sxs-lookup"><span data-stu-id="2053e-119">Values that are used in various pointer macros (see [Macros](macros.md)).</span></span><br/>                                                                                                                       |
| [<span data-ttu-id="2053e-120">**Сенсорные флаги**</span><span class="sxs-lookup"><span data-stu-id="2053e-120">**Touch Flags**</span></span>](touch-flags-constants.md)<br/>                           | <span data-ttu-id="2053e-121">Значения, которые могут отображаться в поле **таучфлагс** структуры [**POINTER_TOUCH_INFO**](/previous-versions/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="2053e-121">Values that can appear in the **touchFlags** field of the [**POINTER_TOUCH_INFO**](/previous-versions/windows/desktop/api) structure.</span></span><br/>                                                                   |
| [<span data-ttu-id="2053e-122">**Окно проверки нажатия касания**</span><span class="sxs-lookup"><span data-stu-id="2053e-122">**Touch Hit Testing Window**</span></span>](touch-hit-testing-window-constants.md)<br/> | <span data-ttu-id="2053e-123">Указывает, как сообщения для проверки попадания касания обрабатываются окнами, зарегистрированными с помощью функции [**регистертаучхиттестингвиндов**](/windows/win32/api/winuser/nf-winuser-registertouchhittestingwindow) .</span><span class="sxs-lookup"><span data-stu-id="2053e-123">Indicates how messages for touch hit testing are processed by windows that are registered through the [**RegisterTouchHitTestingWindow**](/windows/win32/api/winuser/nf-winuser-registertouchhittestingwindow) function.</span></span><br/> |
| [<span data-ttu-id="2053e-124">**Маска касания**</span><span class="sxs-lookup"><span data-stu-id="2053e-124">**Touch Mask**</span></span>](touch-mask-constants.md)<br/>                             | <span data-ttu-id="2053e-125">Значения, которые могут отображаться в поле **таучмаск** структуры [**POINTER_TOUCH_INFO**](/previous-versions/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="2053e-125">Values that can appear in the **touchMask** field of the [**POINTER_TOUCH_INFO**](/previous-versions/windows/desktop/api) structure.</span></span><br/>                                                                    |



 

## <a name="related-topics"></a><span data-ttu-id="2053e-126">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="2053e-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2053e-127">Ссылка на входящее сообщение указателя</span><span class="sxs-lookup"><span data-stu-id="2053e-127">Pointer Input Message Reference</span></span>](wmpointer-reference.md)
</dt> </dl>

 

