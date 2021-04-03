---
description: Ниже приведены константы жестов.
ms.assetid: 21aaf8f0-13b7-4f97-ad4a-3557a7020337
title: Константы жестов (Табфликкс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b9a83f9a35a2c1a9cbd7c4b048a8c985f5eea34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104145580"
---
# <a name="flicks-constants"></a><span data-ttu-id="f08a3-103">Константы жестов</span><span class="sxs-lookup"><span data-stu-id="f08a3-103">Flicks Constants</span></span>

<span data-ttu-id="f08a3-104">Ниже приведены константы жестов.</span><span class="sxs-lookup"><span data-stu-id="f08a3-104">The following are the Flicks constants.</span></span>



| <span data-ttu-id="f08a3-105">Константа/значение</span><span class="sxs-lookup"><span data-stu-id="f08a3-105">Constant/value</span></span>                                                                                                                                                                                                                                   | <span data-ttu-id="f08a3-106">Описание</span><span class="sxs-lookup"><span data-stu-id="f08a3-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FLICK_WM_HANDLED_MASK"></span><span id="flick_wm_handled_mask"></span><dl> <span data-ttu-id="f08a3-107"><dt>**Жест \_ \_Обработанные по \_ маске маски**</dt> <dt>0x1</dt></span><span class="sxs-lookup"><span data-stu-id="f08a3-107"><dt>**FLICK\_WM\_HANDLED\_MASK**</dt> <dt>0x1</dt></span></span> </dl> | <span data-ttu-id="f08a3-108">Значение, возвращаемое после обработки сообщения [**с \_ \_ сообщением о жесте планшета WM**](wm-tablet-flick-message.md) .</span><span class="sxs-lookup"><span data-stu-id="f08a3-108">The value to return after handling the [**WM\_TABLET\_FLICK Message**](wm-tablet-flick-message.md) message.</span></span> <span data-ttu-id="f08a3-109">Если **возвращается \_ \_ \_ Маска обработки жестов WM** , дальнейшие действия не выполняются.</span><span class="sxs-lookup"><span data-stu-id="f08a3-109">If **FLICK\_WM\_HANDLED\_MASK** is returned, no further action occurs.</span></span> <span data-ttu-id="f08a3-110">В противном случае Windows отправляет дальнейшие уведомления, такие как [**WM \_ аппкомманд**](/windows/desktop/inputdev/wm-appcommand), [**WM \_ VSCROLL**](/windows/desktop/Controls/wm-vscroll)или [**WM \_ KeyDown**](/windows/desktop/inputdev/wm-keydown), в зависимости от того, какое действие связано с пером.</span><span class="sxs-lookup"><span data-stu-id="f08a3-110">Otherwise, Windows sends follow-up notifications, such as [**WM\_APPCOMMAND**](/windows/desktop/inputdev/wm-appcommand), [**WM\_VSCROLL**](/windows/desktop/Controls/wm-vscroll), or [**WM\_KEYDOWN**](/windows/desktop/inputdev/wm-keydown), depending on which action is associated with the pen flick.</span></span> <br/> |
| <span id="NUM_FLICK_DIRECTIONS"></span><span id="num_flick_directions"></span><dl> <span data-ttu-id="f08a3-111"><dt>**Число \_ \_Направления надвижений**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="f08a3-111"><dt>**NUM\_FLICK\_DIRECTIONS**</dt> <dt>8</dt></span></span> </dl>       | <span data-ttu-id="f08a3-112">Число направлений, определенных в перечислении [**фликкдиректион**](/windows/desktop/api/tabflicks/ne-tabflicks-flickdirection) .</span><span class="sxs-lookup"><span data-stu-id="f08a3-112">The number of directions defined in the [**FLICKDIRECTION**](/windows/desktop/api/tabflicks/ne-tabflicks-flickdirection) enumeration.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                              |



## <a name="requirements"></a><span data-ttu-id="f08a3-113">Требования</span><span class="sxs-lookup"><span data-stu-id="f08a3-113">Requirements</span></span>



| <span data-ttu-id="f08a3-114">Требование</span><span class="sxs-lookup"><span data-stu-id="f08a3-114">Requirement</span></span> | <span data-ttu-id="f08a3-115">Значение</span><span class="sxs-lookup"><span data-stu-id="f08a3-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f08a3-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f08a3-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f08a3-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f08a3-117">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="f08a3-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f08a3-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f08a3-119">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f08a3-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="f08a3-120">Header</span><span class="sxs-lookup"><span data-stu-id="f08a3-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="f08a3-121"><dt>Табфликкс. h</dt></span><span class="sxs-lookup"><span data-stu-id="f08a3-121"><dt>Tabflicks.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f08a3-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f08a3-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f08a3-123">**Перечисление ФЛИККДИРЕКТИОН**</span><span class="sxs-lookup"><span data-stu-id="f08a3-123">**FLICKDIRECTION Enumeration**</span></span>](/windows/desktop/api/tabflicks/ne-tabflicks-flickdirection)
</dt> <dt>

[<span data-ttu-id="f08a3-124">**\_Сообщение пера планшета WM \_**</span><span class="sxs-lookup"><span data-stu-id="f08a3-124">**WM\_TABLET\_FLICK Message**</span></span>](wm-tablet-flick-message.md)
</dt> <dt>

[<span data-ttu-id="f08a3-125">Жесты жестов</span><span class="sxs-lookup"><span data-stu-id="f08a3-125">Flicks Gestures</span></span>](flicks-gestures.md)
</dt> <dt>

<span data-ttu-id="f08a3-126">[Реагирование на жесты пером](/previous-versions//dd356077(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f08a3-126">[Responding to Pen Flicks](/previous-versions//dd356077(v=vs.85))</span></span>
</dt> </dl>

 

