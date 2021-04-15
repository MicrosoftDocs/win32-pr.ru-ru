---
title: Стили всплывающих подсказок (Коммктрл. h)
description: В этом разделе перечислены стили элементов управления, используемые с элементами управления ToolTip.
ms.assetid: a6aeac71-6a69-4903-af78-0bfe1f83e632
topic_type:
- apiref
api_name:
- TTS_ALWAYSTIP
- TTS_BALLOON
- TTS_CLOSE
- TTS_NOANIMATE
- TTS_NOFADE
- TTS_NOPREFIX
- TTS_USEVISUALSTYLE
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff8b89aed88caddceae815414b9f2b4d93a550c5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648118"
---
# <a name="tooltip-styles"></a><span data-ttu-id="be628-103">Стили всплывающих подсказок</span><span class="sxs-lookup"><span data-stu-id="be628-103">Tooltip Styles</span></span>

<span data-ttu-id="be628-104">В этом разделе перечислены стили элементов управления, используемые с элементами управления ToolTip.</span><span class="sxs-lookup"><span data-stu-id="be628-104">This section lists the control styles used with tooltip controls.</span></span>



| <span data-ttu-id="be628-105">Константа</span><span class="sxs-lookup"><span data-stu-id="be628-105">Constant</span></span>                                                                                                                                                                     | <span data-ttu-id="be628-106">Описание</span><span class="sxs-lookup"><span data-stu-id="be628-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                                       |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TTS_ALWAYSTIP"></span><span id="tts_alwaystip"></span><dl> <span data-ttu-id="be628-107"><dt>**TTS \_ алвайстип**</dt></span><span class="sxs-lookup"><span data-stu-id="be628-107"><dt>**TTS\_ALWAYSTIP**</dt></span></span> </dl>                | <span data-ttu-id="be628-108">Указывает, что элемент управления ToolTip появляется, когда курсор находится на инструменте, даже если окно-владелец элемента управления ToolTip неактивно.</span><span class="sxs-lookup"><span data-stu-id="be628-108">Indicates that the tooltip control appears when the cursor is on a tool, even if the tooltip control's owner window is inactive.</span></span> <span data-ttu-id="be628-109">Без этого стиля всплывающая подсказка отображается только в том случае, если окно владельца инструмента активно.</span><span class="sxs-lookup"><span data-stu-id="be628-109">Without this style, the tooltip appears only when the tool's owner window is active.</span></span><br/>                                                                                                                                  |
| <span id="TTS_BALLOON"></span><span id="tts_balloon"></span><dl> <span data-ttu-id="be628-110"><dt>**\_выноска TTS**</dt></span><span class="sxs-lookup"><span data-stu-id="be628-110"><dt>**TTS\_BALLOON**</dt></span></span> </dl>                      | <span data-ttu-id="be628-111">[Версия 5,80](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="be628-111">[Version 5.80](common-control-versions.md).</span></span> <span data-ttu-id="be628-112">Указывает, что элемент управления ToolTip имеет внешний вид «всплывающего сообщения» со скругленными углами и, указывающим на элемент.</span><span class="sxs-lookup"><span data-stu-id="be628-112">Indicates that the tooltip control has the appearance of a cartoon "balloon," with rounded corners and a stem pointing to the item.</span></span> <br/>                                                                                                                                                                      |
| <span id="TTS_CLOSE"></span><span id="tts_close"></span><dl> <span data-ttu-id="be628-113"><dt>**\_закрытие TTS**</dt></span><span class="sxs-lookup"><span data-stu-id="be628-113"><dt>**TTS\_CLOSE**</dt></span></span> </dl>                            | <span data-ttu-id="be628-114">Отображает кнопку **Закрыть** в подсказке.</span><span class="sxs-lookup"><span data-stu-id="be628-114">Displays a **Close** button on the tooltip.</span></span> <span data-ttu-id="be628-115">Действует, только если в подсказке есть \_ стиль и заголовок TTS; см. раздел [**ТТМ \_ сеттитле**](ttm-settitle.md).</span><span class="sxs-lookup"><span data-stu-id="be628-115">Valid only when the tooltip has the TTS\_BALLOON style and a title; see [**TTM\_SETTITLE**](ttm-settitle.md).</span></span><br/>                                                                                                                                                                                             |
| <span id="TTS_NOANIMATE"></span><span id="tts_noanimate"></span><dl> <span data-ttu-id="be628-116"><dt>**\_НЕанимированное TTS**</dt></span><span class="sxs-lookup"><span data-stu-id="be628-116"><dt>**TTS\_NOANIMATE**</dt></span></span> </dl>                | <span data-ttu-id="be628-117">[Версия 5,80](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="be628-117">[Version 5.80](common-control-versions.md).</span></span> <span data-ttu-id="be628-118">Отключает анимацию с перемещаемыми подсказками в системах Windows 98 и Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="be628-118">Disables sliding tooltip animation on Windows 98 and Windows 2000 systems.</span></span> <span data-ttu-id="be628-119">Этот стиль не учитывается в более ранних системах.</span><span class="sxs-lookup"><span data-stu-id="be628-119">This style is ignored on earlier systems.</span></span><br/>                                                                                                                                                                                      |
| <span id="TTS_NOFADE"></span><span id="tts_nofade"></span><dl> <span data-ttu-id="be628-120"><dt>**\_Выцветание TTS**</dt></span><span class="sxs-lookup"><span data-stu-id="be628-120"><dt>**TTS\_NOFADE**</dt></span></span> </dl>                         | <span data-ttu-id="be628-121">[Версия 5,80](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="be628-121">[Version 5.80](common-control-versions.md).</span></span> <span data-ttu-id="be628-122">Отключает анимацию всплывающих подсказок.</span><span class="sxs-lookup"><span data-stu-id="be628-122">Disables fading tooltip animation.</span></span> <br/>                                                                                                                                                                                                                                                                       |
| <span id="TTS_NOPREFIX"></span><span id="tts_noprefix"></span><dl> <span data-ttu-id="be628-123"><dt>**\_префикс TTS**</dt></span><span class="sxs-lookup"><span data-stu-id="be628-123"><dt>**TTS\_NOPREFIX**</dt></span></span> </dl>                   | <span data-ttu-id="be628-124">Предотвращает удаление символов амперсанда из строки или завершение строки в символе табуляции.</span><span class="sxs-lookup"><span data-stu-id="be628-124">Prevents the system from stripping ampersand characters from a string or terminating a string at a tab character.</span></span> <span data-ttu-id="be628-125">Без этого стиля система автоматически отделяет символы амперсанда и завершает строку на первом символе табуляции.</span><span class="sxs-lookup"><span data-stu-id="be628-125">Without this style, the system automatically strips ampersand characters and terminates a string at the first tab character.</span></span> <span data-ttu-id="be628-126">Это позволяет приложению использовать ту же строку, что и элемент меню, и как текст в элементе управления ToolTip.</span><span class="sxs-lookup"><span data-stu-id="be628-126">This allows an application to use the same string as both a menu item and as text in a tooltip control.</span></span><br/> |
| <span id="TTS_USEVISUALSTYLE"></span><span id="tts_usevisualstyle"></span><dl> <span data-ttu-id="be628-127"><dt>**TTS \_ усевисуалстиле**</dt></span><span class="sxs-lookup"><span data-stu-id="be628-127"><dt>**TTS\_USEVISUALSTYLE**</dt></span></span> </dl> | <span data-ttu-id="be628-128">Использует гиперссылки темы.</span><span class="sxs-lookup"><span data-stu-id="be628-128">Uses themed hyperlinks.</span></span> <span data-ttu-id="be628-129">Тема определит стили для всех ссылок в подсказке.</span><span class="sxs-lookup"><span data-stu-id="be628-129">The theme will define the styles for any links in the tooltip.</span></span> <span data-ttu-id="be628-130">Для этого стиля всегда требуется \_ установить TTF парселинкс.</span><span class="sxs-lookup"><span data-stu-id="be628-130">This style always requires TTF\_PARSELINKS to be set.</span></span> <br/>                                                                                                                                                                                                          |



## <a name="remarks"></a><span data-ttu-id="be628-131">Комментарии</span><span class="sxs-lookup"><span data-stu-id="be628-131">Remarks</span></span>

<span data-ttu-id="be628-132">Элемент управления ToolTip всегда имеет \_ \_ стили окна Popup и окно панели \_ инструментов WS, независимо от того, указываются ли они при создании элемента управления.</span><span class="sxs-lookup"><span data-stu-id="be628-132">A tooltip control always has the WS\_POPUP and WS\_EX\_TOOLWINDOW window styles, regardless of whether you specify them when creating the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="be628-133">Требования</span><span class="sxs-lookup"><span data-stu-id="be628-133">Requirements</span></span>



| <span data-ttu-id="be628-134">Требование</span><span class="sxs-lookup"><span data-stu-id="be628-134">Requirement</span></span> | <span data-ttu-id="be628-135">Значение</span><span class="sxs-lookup"><span data-stu-id="be628-135">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="be628-136">Header</span><span class="sxs-lookup"><span data-stu-id="be628-136">Header</span></span><br/> | <dl> <span data-ttu-id="be628-137"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="be628-137"><dt>CommCtrl.h</dt></span></span> </dl> |



 

 





