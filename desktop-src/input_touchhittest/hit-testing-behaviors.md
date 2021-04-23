---
title: Поведение при проверке нажатия касания
description: Следующие константы используются приложениями или платформами пользовательского интерфейса для указания того, как сообщения для проверки попадания касания обрабатываются Windows, зарегистрированными с помощью функции Регистертаучхиттестингвиндов.
ms.assetid: D1ECCBFA-CD01-401E-A42E-4F954F5F0A32
topic_type:
- apiref
api_name:
- TOUCH_HIT_TESTING_DEFAULT
- TOUCH_HIT_TESTING_CLIENT
- TOUCH_HIT_TESTING_NONE
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/07/2020
ms.openlocfilehash: 9b49f61870c6c7041d73d6fa8d5c078887360359
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105719206"
---
# <a name="touch-hit-testing-behaviors"></a><span data-ttu-id="5786f-103">Поведение при проверке нажатия касания</span><span class="sxs-lookup"><span data-stu-id="5786f-103">Touch Hit Testing Behaviors</span></span>

<span data-ttu-id="5786f-104">Следующие константы используются приложениями или платформами пользовательского интерфейса для указания того, как сообщения для проверки попадания касания обрабатываются Windows, зарегистрированными с помощью функции [**регистертаучхиттестингвиндов**](/windows/win32/api/winuser/nf-winuser-registertouchhittestingwindow) .</span><span class="sxs-lookup"><span data-stu-id="5786f-104">The following constants are used by applications or UI frameworks to identify how messages for touch hit testing are processed by windows that are registered through the [**RegisterTouchHitTestingWindow**](/windows/win32/api/winuser/nf-winuser-registertouchhittestingwindow) function.</span></span>

| <span data-ttu-id="5786f-105">Константа/значение</span><span class="sxs-lookup"><span data-stu-id="5786f-105">Constant/value</span></span> | <span data-ttu-id="5786f-106">Описание</span><span class="sxs-lookup"><span data-stu-id="5786f-106">Description</span></span> |
|---|---|
| <span data-ttu-id="5786f-107">**TOUCH_HIT_TESTING_DEFAULT** </dt> <dt>0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="5786f-107">**TOUCH_HIT_TESTING_DEFAULT**</dt> <dt>0 (0x0)</span></span> | <span data-ttu-id="5786f-108">Указывает, что [WM_TOUCHHITTESTING](../inputmsg/wm-touchhittesting.md) сообщения не отправляются в целевое окно, но отправляются в дочерние окна.</span><span class="sxs-lookup"><span data-stu-id="5786f-108">Indicates that [WM_TOUCHHITTESTING](../inputmsg/wm-touchhittesting.md) messages are not sent to the target window but are sent to child windows.</span></span><br/> |
| <span data-ttu-id="5786f-109">**TOUCH_HIT_TESTING_CLIENT** </dt> <dt>1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="5786f-109">**TOUCH_HIT_TESTING_CLIENT**</dt> <dt>1 (0x1)</span></span>    | <span data-ttu-id="5786f-110">Указывает, что [WM_TOUCHHITTESTING](../inputmsg/wm-touchhittesting.md) сообщения отправляются в целевое окно.</span><span class="sxs-lookup"><span data-stu-id="5786f-110">Indicates that [WM_TOUCHHITTESTING](../inputmsg/wm-touchhittesting.md) messages are sent to the target window.</span></span><br/>                                   |
| <span data-ttu-id="5786f-111">**TOUCH_HIT_TESTING_NONE** </dt> <dt>2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="5786f-111">**TOUCH_HIT_TESTING_NONE**</dt> <dt>2 (0x2)</span></span>          | <span data-ttu-id="5786f-112">Указывает, что [WM_TOUCHHITTESTING](../inputmsg/wm-touchhittesting.md) сообщения не отправляются в целевое окно или дочерние окна.</span><span class="sxs-lookup"><span data-stu-id="5786f-112">Indicates that [WM_TOUCHHITTESTING](../inputmsg/wm-touchhittesting.md) messages are not sent to the target window or child windows.</span></span><br/>              |

## <a name="requirements"></a><span data-ttu-id="5786f-113">Требования</span><span class="sxs-lookup"><span data-stu-id="5786f-113">Requirements</span></span>

| <span data-ttu-id="5786f-114">Требование</span><span class="sxs-lookup"><span data-stu-id="5786f-114">Requirement</span></span> | <span data-ttu-id="5786f-115">Значение</span><span class="sxs-lookup"><span data-stu-id="5786f-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="5786f-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5786f-116">Minimum supported client</span></span><br/> | <span data-ttu-id="5786f-117">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="5786f-117">Windows 8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="5786f-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5786f-118">Minimum supported server</span></span><br/> | <span data-ttu-id="5786f-119">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="5786f-119">None supported</span></span><br/>                                                            |
| <span data-ttu-id="5786f-120">Header</span><span class="sxs-lookup"><span data-stu-id="5786f-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="5786f-121"><dt>Winuser. h</span><span class="sxs-lookup"><span data-stu-id="5786f-121"><dt>Winuser.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="5786f-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5786f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5786f-123">Константы</span><span class="sxs-lookup"><span data-stu-id="5786f-123">Constants</span></span>](constants.md)
