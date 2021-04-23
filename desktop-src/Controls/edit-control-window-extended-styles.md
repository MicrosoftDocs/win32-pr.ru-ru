---
title: Расширенные стили элемента управления Edit (Коммктрл. h)
description: В этом разделе перечислены расширенные стили, используемые при создании элементов управления "изменение". Значение расширенных стилей является побитовым сочетанием этих стилей.
ms.assetid: 44ef7cbf-6d90-4ea0-8e23-cd84aacd5506
topic_type:
- apiref
api_name:
- ES_EX_ALLOWEOL_CR
- ES_EX_ALLOWEOL_LF
- ES_EX_ALLOWEOL_ALL
- ES_EX_CONVERT_EOL_ON_PASTE
- ES_EX_ZOOMABLE
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 10/19/2018
ms.openlocfilehash: 912a13b0e05d7b12e5058435221b821b50eddf2e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648634"
---
# <a name="edit-control-extended-styles"></a><span data-ttu-id="69a9a-104">Изменение расширенных стилей элемента управления</span><span class="sxs-lookup"><span data-stu-id="69a9a-104">Edit Control Extended Styles</span></span>

<span data-ttu-id="69a9a-105">В этом разделе перечислены расширенные стили, используемые при создании элементов управления "изменение".</span><span class="sxs-lookup"><span data-stu-id="69a9a-105">This section lists extended styles used when creating edit controls.</span></span> <span data-ttu-id="69a9a-106">Значение расширенных стилей является побитовым сочетанием этих стилей.</span><span class="sxs-lookup"><span data-stu-id="69a9a-106">The value of extended styles is a bitwise combination of these styles.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="69a9a-107">Константа</span><span class="sxs-lookup"><span data-stu-id="69a9a-107">Constant</span></span></th>
<th style="text-align: left;"><span data-ttu-id="69a9a-108">Описание</span><span class="sxs-lookup"><span data-stu-id="69a9a-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="ES_EX_ALLOWEOL_CR"></span><span id="es_ex_alloweol_cr"></span><dl> <span data-ttu-id="69a9a-109"><dt><strong>ES_EX_ALLOWEOL_CR</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="69a9a-109"><dt><strong>ES_EX_ALLOWEOL_CR</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="69a9a-110">[Windows Vista и более поздние версии](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="69a9a-110">[Windows Vista and later](common-control-versions.md).</span></span> <span data-ttu-id="69a9a-111">Включает поддержку символов возврата каретки (CR) в конце строки.</span><span class="sxs-lookup"><span data-stu-id="69a9a-111">Enables support for carriage return (CR) end-of-line characters to break lines.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ES_EX_ALLOWEOL_LF"></span><span id="es_ex_alloweol_lf"></span><dl> <span data-ttu-id="69a9a-112"><dt><strong>ES_EX_ALLOWEOL_LF</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="69a9a-112"><dt><strong>ES_EX_ALLOWEOL_LF</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="69a9a-113">[Windows Vista и более поздние версии](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="69a9a-113">[Windows Vista and later](common-control-versions.md).</span></span> <span data-ttu-id="69a9a-114">Включает поддержку символов перевода строки (LF) для разрыва строк.</span><span class="sxs-lookup"><span data-stu-id="69a9a-114">Enables support for linefeed (LF) end-of-line characters to break lines.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="ES_EX_ALLOWEOL_ALL"></span><span id="es_ex_alloweol_all"></span><dl> <span data-ttu-id="69a9a-115"><dt><strong>ES_EX_ALLOWEOL_ALL</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="69a9a-115"><dt><strong>ES_EX_ALLOWEOL_ALL</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="69a9a-116">[Windows Vista и более поздние версии](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="69a9a-116">[Windows Vista and later](common-control-versions.md).</span></span> <span data-ttu-id="69a9a-117">Включает поддержку символов возврата каретки (CR) и перевода строки (LF) для разбиения строк.</span><span class="sxs-lookup"><span data-stu-id="69a9a-117">Enables support for both carriage return (CR) and linefeed (LF) end-of-line characters to break lines.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ES_EX_CONVERT_EOL_ON_PASTE"></span><span id="es_ex_convert_eol_on_paste"></span><dl> <span data-ttu-id="69a9a-118"><dt><strong>ES_EX_CONVERT_EOL_ON_PASTE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="69a9a-118"><dt><strong>ES_EX_CONVERT_EOL_ON_PASTE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="69a9a-119">[Windows Vista и более поздние версии](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="69a9a-119">[Windows Vista and later](common-control-versions.md).</span></span> <span data-ttu-id="69a9a-120">Преобразует символы конца строки, включенные для этого элемента управления "поле ввода", в вставленном содержимом в соответствии с символом конца строки, используемым текущим документом.</span><span class="sxs-lookup"><span data-stu-id="69a9a-120">Converts end-of-line characters enabled for this edit control in pasted content to match the end-of-line character used by the current document.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="ES_EX_ZOOMABLE"></span><span id="es_ex_zoomable"></span><dl> <span data-ttu-id="69a9a-121"><dt><strong>ES_EX_ZOOMABLE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="69a9a-121"><dt><strong>ES_EX_ZOOMABLE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="69a9a-122">[Windows Vista и более поздние версии](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="69a9a-122">[Windows Vista and later](common-control-versions.md).</span></span> <span data-ttu-id="69a9a-123">Позволяет увеличить масштаб с помощью клавиш CTRL + маусевхил [**и \_**](em-getzoom.md)EM / [**EM максимального размера \_ сетзум**](em-setzoom.md) .</span><span class="sxs-lookup"><span data-stu-id="69a9a-123">Enables zooming using Ctrl+MouseWheel and the [**EM\_GETZOOM**](em-getzoom.md)/[**EM\_SETZOOM**](em-setzoom.md) messages.</span></span><br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="69a9a-124">Требования</span><span class="sxs-lookup"><span data-stu-id="69a9a-124">Requirements</span></span>



| <span data-ttu-id="69a9a-125">Требование</span><span class="sxs-lookup"><span data-stu-id="69a9a-125">Requirement</span></span> | <span data-ttu-id="69a9a-126">Значение</span><span class="sxs-lookup"><span data-stu-id="69a9a-126">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="69a9a-127">Header</span><span class="sxs-lookup"><span data-stu-id="69a9a-127">Header</span></span><br/> | <dl> <span data-ttu-id="69a9a-128"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="69a9a-128"><dt>CommCtrl.h</dt></span></span> </dl> |



 

 





