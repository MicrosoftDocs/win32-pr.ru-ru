---
title: Расширенные стили панелей инструментов (Коммктрл. h)
description: В этом разделе перечислены расширенные стили, поддерживаемые элементами управления ToolBar.
ms.assetid: da31dbbf-8d0a-4711-a1af-382c62e653cd
topic_type:
- apiref
api_name:
- TBSTYLE_EX_DRAWDDARROWS
- TBSTYLE_EX_HIDECLIPPEDBUTTONS
- TBSTYLE_EX_DOUBLEBUFFER
- TBSTYLE_EX_MIXEDBUTTONS
- TBSTYLE_EX_MULTICOLUMN
- TBSTYLE_EX_VERTICAL
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 056e48753485364017f04f7b84e609b19473bf5a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648120"
---
# <a name="toolbar-extended-styles"></a><span data-ttu-id="95422-103">Расширенные стили панели инструментов</span><span class="sxs-lookup"><span data-stu-id="95422-103">Toolbar Extended Styles</span></span>

<span data-ttu-id="95422-104">В этом разделе перечислены расширенные стили, поддерживаемые элементами управления ToolBar.</span><span class="sxs-lookup"><span data-stu-id="95422-104">This section lists the extended styles supported by toolbar controls.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="95422-105">Константа</span><span class="sxs-lookup"><span data-stu-id="95422-105">Constant</span></span></th>
<th style="text-align: left;"><span data-ttu-id="95422-106">Описание</span><span class="sxs-lookup"><span data-stu-id="95422-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="TBSTYLE_EX_DRAWDDARROWS"></span><span id="tbstyle_ex_drawddarrows"></span><dl> <span data-ttu-id="95422-107"><dt><strong>TBSTYLE_EX_DRAWDDARROWS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="95422-107"><dt><strong>TBSTYLE_EX_DRAWDDARROWS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="95422-108"><a href="common-control-versions.md">Версия 4,71</a>.</span><span class="sxs-lookup"><span data-stu-id="95422-108"><a href="common-control-versions.md">Version 4.71</a>.</span></span> <span data-ttu-id="95422-109">Этот стиль позволяет кнопкам иметь отдельную стрелку раскрывающегося списка.</span><span class="sxs-lookup"><span data-stu-id="95422-109">This style allows buttons to have a separate dropdown arrow.</span></span> <span data-ttu-id="95422-110">Кнопки, имеющие стиль <a href="toolbar-control-and-button-styles.md"><strong>BTNS_DROPDOWN</strong></a> , будут отображаться с помощью раскрывающегося списка в отдельном разделе справа от кнопки.</span><span class="sxs-lookup"><span data-stu-id="95422-110">Buttons that have the <a href="toolbar-control-and-button-styles.md"><strong>BTNS_DROPDOWN</strong></a> style will be drawn with a dropdown arrow in a separate section, to the right of the button.</span></span> <span data-ttu-id="95422-111">Если щелкнуть стрелку, будет Депресс только часть стрелки кнопки, а элемент управления панели инструментов отправит <a href="tbn-dropdown.md">TBN_DROPDOWN</a> код уведомления, чтобы запрос отображался в раскрывающемся меню.</span><span class="sxs-lookup"><span data-stu-id="95422-111">If the arrow is clicked, only the arrow portion of the button will depress, and the toolbar control will send a <a href="tbn-dropdown.md">TBN_DROPDOWN</a> notification code to prompt the application to display the dropdown menu.</span></span> <span data-ttu-id="95422-112">Если нажата основная часть кнопки, элемент управления ToolBar отправляет WM_COMMAND сообщение с ИДЕНТИФИКАТОРом кнопки.</span><span class="sxs-lookup"><span data-stu-id="95422-112">If the main part of the button is clicked, the toolbar control sends a WM_COMMAND message with the button's ID.</span></span> <span data-ttu-id="95422-113">Приложение обычно отвечает, запустив первую команду в меню.</span><span class="sxs-lookup"><span data-stu-id="95422-113">The application normally responds by launching the first command on the menu.</span></span><br/> <span data-ttu-id="95422-114">Существует множество ситуаций, в которых может потребоваться только часть кнопок на панели инструментов с разделенными стрелками.</span><span class="sxs-lookup"><span data-stu-id="95422-114">There are many situations where you may want to have only some of the dropdown buttons on a toolbar with separated arrows.</span></span> <span data-ttu-id="95422-115">Для этого задайте расширенный стиль TBSTYLE_EX_DRAWDDARROWS.</span><span class="sxs-lookup"><span data-stu-id="95422-115">To do so, set the TBSTYLE_EX_DRAWDDARROWS extended style.</span></span> <span data-ttu-id="95422-116">Присвойте этим кнопкам, которые не будут разделены стрелками, <a href="toolbar-control-and-button-styles.md"><strong>BTNS_WHOLEDROPDOWN</strong></a> стиле.</span><span class="sxs-lookup"><span data-stu-id="95422-116">Give those buttons that will not have separated arrows the <a href="toolbar-control-and-button-styles.md"><strong>BTNS_WHOLEDROPDOWN</strong></a> style.</span></span> <span data-ttu-id="95422-117">Кнопки с этим стилем будут отображаться рядом с изображением.</span><span class="sxs-lookup"><span data-stu-id="95422-117">Buttons with this style will have an arrow displayed next to the image.</span></span> <span data-ttu-id="95422-118">Однако стрелка не будет разделяться и при нажатии любой части кнопки элемент управления ToolBar отправит <a href="tbn-dropdown.md">TBN_DROPDOWN</a> код уведомления.</span><span class="sxs-lookup"><span data-stu-id="95422-118">However, the arrow will not be separate and when any part of the button is clicked, the toolbar control will send a <a href="tbn-dropdown.md">TBN_DROPDOWN</a> notification code.</span></span> <span data-ttu-id="95422-119">Чтобы избежать проблем с перерисовкой, этот стиль следует задать до того, как элемент управления ToolBar станет видимым.</span><span class="sxs-lookup"><span data-stu-id="95422-119">To prevent repainting problems, this style should be set before the toolbar control becomes visible.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="TBSTYLE_EX_HIDECLIPPEDBUTTONS"></span><span id="tbstyle_ex_hideclippedbuttons"></span><dl> <span data-ttu-id="95422-120"><dt><strong>TBSTYLE_EX_HIDECLIPPEDBUTTONS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="95422-120"><dt><strong>TBSTYLE_EX_HIDECLIPPEDBUTTONS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="95422-121"><a href="common-control-versions.md">Версия 5,81</a>.</span><span class="sxs-lookup"><span data-stu-id="95422-121"><a href="common-control-versions.md">Version 5.81</a>.</span></span> <span data-ttu-id="95422-122">Этот стиль скрывает частично обрезанные кнопки.</span><span class="sxs-lookup"><span data-stu-id="95422-122">This style hides partially clipped buttons.</span></span> <span data-ttu-id="95422-123">Наиболее часто этот стиль используется для панелей инструментов, которые являются частью элемента управления главной панели.</span><span class="sxs-lookup"><span data-stu-id="95422-123">The most common use of this style is for toolbars that are part of a rebar control.</span></span> <span data-ttu-id="95422-124">Если смежная полоса охватывает часть кнопки, кнопка не будет отображаться.</span><span class="sxs-lookup"><span data-stu-id="95422-124">If an adjacent band covers part of a button, the button will not be displayed.</span></span> <span data-ttu-id="95422-125">Однако если полоса главной панели имеет стиль <a href="/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa"><strong>RBBS_USECHEVRON</strong></a> , то кнопка будет отображаться в раскрывающемся меню шеврона.</span><span class="sxs-lookup"><span data-stu-id="95422-125">However, if the rebar band has the <a href="/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa"><strong>RBBS_USECHEVRON</strong></a> style, the button will be displayed on the chevron's dropdown menu.</span></span> <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="TBSTYLE_EX_DOUBLEBUFFER"></span><span id="tbstyle_ex_doublebuffer"></span><dl> <span data-ttu-id="95422-126"><dt><strong>TBSTYLE_EX_DOUBLEBUFFER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="95422-126"><dt><strong>TBSTYLE_EX_DOUBLEBUFFER</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="95422-127"><a href="common-control-versions.md">Версия 6</a>.</span><span class="sxs-lookup"><span data-stu-id="95422-127"><a href="common-control-versions.md">Version 6</a>.</span></span> <span data-ttu-id="95422-128">Этот стиль требует двойной буферизации панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="95422-128">This style requires the toolbar to be double buffered.</span></span> <span data-ttu-id="95422-129">Двойная буферизация — это механизм, который обнаруживает, что панель инструментов изменилась.</span><span class="sxs-lookup"><span data-stu-id="95422-129">Double buffering is a mechanism that detects when the toolbar has changed.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="95422-130">Версия Comctl32.dll 6 не является распространяемой, но включена в Windows или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="95422-130">Comctl32.dll version 6 is not redistributable but it is included in Windows or later.</span></span> <span data-ttu-id="95422-131">Чтобы использовать Comctl32.dll версии 6, укажите ее в манифесте.</span><span class="sxs-lookup"><span data-stu-id="95422-131">To use Comctl32.dll version 6, specify it in a manifest.</span></span> <span data-ttu-id="95422-132">Дополнительные сведения о манифестах см. в разделе <a href="cookbook-overview.md">Включение визуальных стилей</a>.</span><span class="sxs-lookup"><span data-stu-id="95422-132">For more information on manifests, see <a href="cookbook-overview.md">Enabling Visual Styles</a>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="TBSTYLE_EX_MIXEDBUTTONS"></span><span id="tbstyle_ex_mixedbuttons"></span><dl> <span data-ttu-id="95422-133"><dt><strong>TBSTYLE_EX_MIXEDBUTTONS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="95422-133"><dt><strong>TBSTYLE_EX_MIXEDBUTTONS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="95422-134"><a href="common-control-versions.md">Версия 5,81</a>.</span><span class="sxs-lookup"><span data-stu-id="95422-134"><a href="common-control-versions.md">Version 5.81</a>.</span></span> <span data-ttu-id="95422-135">Этот стиль позволяет задать текст для всех кнопок, но отображать его только для этих кнопок с помощью стиля кнопки <a href="toolbar-control-and-button-styles.md"><strong>BTNS_SHOWTEXT</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="95422-135">This style allows you to set text for all buttons, but only display it for those buttons with the <a href="toolbar-control-and-button-styles.md"><strong>BTNS_SHOWTEXT</strong></a> button style.</span></span> <span data-ttu-id="95422-136">Необходимо также задать стиль <a href="toolbar-control-and-button-styles.md"><strong>TBSTYLE_LIST</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="95422-136">The <a href="toolbar-control-and-button-styles.md"><strong>TBSTYLE_LIST</strong></a> style must also be set.</span></span> <span data-ttu-id="95422-137">Как правило, если кнопка не отображает текст, приложение должно выполнить обработку <a href="tbn-getinfotip.md">TBN_GETINFOTIP</a> или <a href="ttn-getdispinfo.md">TTN_GETDISPINFO</a> , чтобы отобразить подсказку.</span><span class="sxs-lookup"><span data-stu-id="95422-137">Normally, when a button does not display text, your application must handle <a href="tbn-getinfotip.md">TBN_GETINFOTIP</a> or <a href="ttn-getdispinfo.md">TTN_GETDISPINFO</a> to display a tooltip.</span></span> <span data-ttu-id="95422-138">При использовании расширенного стиля TBSTYLE_EX_MIXEDBUTTONS текст, который задается, но не отображается на кнопке, будет автоматически использоваться в качестве текста подсказки для кнопки.</span><span class="sxs-lookup"><span data-stu-id="95422-138">With the TBSTYLE_EX_MIXEDBUTTONS extended style, text that is set but not displayed on a button will automatically be used as the button's tooltip text.</span></span> <span data-ttu-id="95422-139">Приложению требуется только обработку TBN_GETINFOTIP или или TTN_GETDISPINFO, если требуется больше гибкости при указании текста подсказки.</span><span class="sxs-lookup"><span data-stu-id="95422-139">Your application only needs to handle TBN_GETINFOTIP or or TTN_GETDISPINFO if it needs more flexibility in specifying the tooltip text.</span></span> <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="TBSTYLE_EX_MULTICOLUMN"></span><span id="tbstyle_ex_multicolumn"></span><dl> <span data-ttu-id="95422-140"><dt><strong>TBSTYLE_EX_MULTICOLUMN</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="95422-140"><dt><strong>TBSTYLE_EX_MULTICOLUMN</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="95422-141"><a href="common-control-versions.md">Версия 5,82</a>.</span><span class="sxs-lookup"><span data-stu-id="95422-141"><a href="common-control-versions.md">Version 5.82</a>.</span></span> <span data-ttu-id="95422-142"><strong>Предназначен для внутреннего использования; не рекомендуется для использования в приложениях.</strong></span><span class="sxs-lookup"><span data-stu-id="95422-142"><strong>Intended for internal use; not recommended for use in applications.</strong></span></span> <span data-ttu-id="95422-143">Этот стиль дает панели инструментов вертикальную ориентацию и упорядочивает кнопки на панели инструментов в столбцы.</span><span class="sxs-lookup"><span data-stu-id="95422-143">This style gives the toolbar a vertical orientation and organizes the toolbar buttons into columns.</span></span> <span data-ttu-id="95422-144">Кнопки передаются вниз по вертикали, пока кнопка не превысить ограничивающую высоту панели инструментов (см. <a href="tb-setboundingsize.md"><strong>TB_SETBOUNDINGSIZE</strong></a>), а затем создается новый столбец.</span><span class="sxs-lookup"><span data-stu-id="95422-144">The buttons flow down vertically until a button has exceeded the bounding height of the toolbar (see <a href="tb-setboundingsize.md"><strong>TB_SETBOUNDINGSIZE</strong></a>), and then a new column is created.</span></span> <span data-ttu-id="95422-145">Панель инструментов направляет кнопки таким образом, пока не будут размещены все кнопки.</span><span class="sxs-lookup"><span data-stu-id="95422-145">The toolbar flows the buttons in this manner until all buttons are positioned.</span></span> <span data-ttu-id="95422-146">Чтобы использовать этот стиль, необходимо также задать стиль TBSTYLE_EX_VERTICAL.</span><span class="sxs-lookup"><span data-stu-id="95422-146">To use this style, the TBSTYLE_EX_VERTICAL style must also be set.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="95422-147">Этот стиль может не поддерживаться в будущих версиях Comctl32.dll.</span><span class="sxs-lookup"><span data-stu-id="95422-147">This style may not be supported in future versions of Comctl32.dll.</span></span> <span data-ttu-id="95422-148">Кроме того, этот стиль не определен в коммктрл. h.</span><span class="sxs-lookup"><span data-stu-id="95422-148">Also, this style is not defined in commctrl.h.</span></span> <span data-ttu-id="95422-149">Добавьте следующее определение в исходные файлы приложения для использования этого стиля: <code>#define TBSTYLE_EX_MULTICOLUMN 0x00000002</code>
</span><span class="sxs-lookup"><span data-stu-id="95422-149">Add the following definition to the source files of your application to use this style: <code>#define TBSTYLE_EX_MULTICOLUMN 0x00000002</code>
</span></span></blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="TBSTYLE_EX_VERTICAL"></span><span id="tbstyle_ex_vertical"></span><dl> <span data-ttu-id="95422-150"><dt><strong>TBSTYLE_EX_VERTICAL</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="95422-150"><dt><strong>TBSTYLE_EX_VERTICAL</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="95422-151"><a href="common-control-versions.md">Версия 5,82</a>.</span><span class="sxs-lookup"><span data-stu-id="95422-151"><a href="common-control-versions.md">Version 5.82</a>.</span></span> <span data-ttu-id="95422-152"><strong>Предназначен для внутреннего использования; не рекомендуется для использования в приложениях.</strong></span><span class="sxs-lookup"><span data-stu-id="95422-152"><strong>Intended for internal use; not recommended for use in applications.</strong></span></span> <span data-ttu-id="95422-153">Этот стиль дает панели инструментов вертикальную ориентацию.</span><span class="sxs-lookup"><span data-stu-id="95422-153">This style gives the toolbar a vertical orientation.</span></span> <span data-ttu-id="95422-154">Кнопки панели инструментов передаются сверху вниз, а не горизонтально.</span><span class="sxs-lookup"><span data-stu-id="95422-154">Toolbar buttons flow from top to bottom instead of horizontally.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="95422-155">Этот стиль может не поддерживаться в будущих версиях Comctl32.dll.</span><span class="sxs-lookup"><span data-stu-id="95422-155">This style may not be supported in future versions of Comctl32.dll.</span></span> <span data-ttu-id="95422-156">Кроме того, этот стиль не определен в коммктрл. h.</span><span class="sxs-lookup"><span data-stu-id="95422-156">Also, this style is not defined in commctrl.h.</span></span> <span data-ttu-id="95422-157">Добавьте следующее определение в исходные файлы приложения для использования этого стиля: <code>#define TBSTYLE_EX_VERTICAL 0x00000004</code>
</span><span class="sxs-lookup"><span data-stu-id="95422-157">Add the following definition to the source files of your application to use this style: <code>#define TBSTYLE_EX_VERTICAL 0x00000004</code>
</span></span></blockquote>
<br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="95422-158">Комментарии</span><span class="sxs-lookup"><span data-stu-id="95422-158">Remarks</span></span>

<span data-ttu-id="95422-159">Чтобы задать расширенный стиль, отправьте на панель инструментов сообщение [**\_ Сетекстендедстиле (ТБ**](tb-setextendedstyle.md) ).</span><span class="sxs-lookup"><span data-stu-id="95422-159">To set an extended style, send the toolbar control a [**TB\_SETEXTENDEDSTYLE**](tb-setextendedstyle.md) message.</span></span> <span data-ttu-id="95422-160">Чтобы определить, какие расширенные стили в настоящее время заданы, отправьте сообщение [**\_ Жетекстендедстиле в ТБ**](tb-getextendedstyle.md) .</span><span class="sxs-lookup"><span data-stu-id="95422-160">To determine what extended styles are currently set, send a [**TB\_GETEXTENDEDSTYLE**](tb-getextendedstyle.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="95422-161">Требования</span><span class="sxs-lookup"><span data-stu-id="95422-161">Requirements</span></span>



| <span data-ttu-id="95422-162">Требование</span><span class="sxs-lookup"><span data-stu-id="95422-162">Requirement</span></span> | <span data-ttu-id="95422-163">Значение</span><span class="sxs-lookup"><span data-stu-id="95422-163">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="95422-164">Header</span><span class="sxs-lookup"><span data-stu-id="95422-164">Header</span></span><br/> | <dl> <span data-ttu-id="95422-165"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="95422-165"><dt>CommCtrl.h</dt></span></span> </dl> |



 

 





