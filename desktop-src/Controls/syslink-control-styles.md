---
title: Стили элементов управления SysLink (Коммктрл. h)
description: При создании элементов управления SysLink используются следующие константы стиля.
ms.assetid: e9a8c99b-86c4-4385-ae20-b2b78a07b491
topic_type:
- apiref
api_name:
- LWS_TRANSPARENT
- LWS_IGNORERETURN
- LWS_NOPREFIX
- LWS_USEVISUALSTYLE
- LWS_USECUSTOMTEXT
- LWS_RIGHT
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 490a64a21ec81c1c91cc34ec8bebd2995476db4f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648684"
---
# <a name="syslink-control-styles"></a><span data-ttu-id="6301f-103">Стили элемента управления SysLink</span><span class="sxs-lookup"><span data-stu-id="6301f-103">SysLink Control Styles</span></span>

<span data-ttu-id="6301f-104">При создании элементов управления SysLink используются следующие константы стиля.</span><span class="sxs-lookup"><span data-stu-id="6301f-104">The following style constants are used when creating SysLink controls.</span></span>



| <span data-ttu-id="6301f-105">Константа</span><span class="sxs-lookup"><span data-stu-id="6301f-105">Constant</span></span>                                                                                                                                                                        | <span data-ttu-id="6301f-106">Описание</span><span class="sxs-lookup"><span data-stu-id="6301f-106">Description</span></span>                                                                                                                                                               |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LWS_TRANSPARENT"></span><span id="lws_transparent"></span><dl> <span data-ttu-id="6301f-107"><dt>**\_прозрачный LWS**</dt></span><span class="sxs-lookup"><span data-stu-id="6301f-107"><dt>**LWS\_TRANSPARENT**</dt></span></span> </dl>             | <span data-ttu-id="6301f-108">Режим фонового набора прозрачен.</span><span class="sxs-lookup"><span data-stu-id="6301f-108">The background mix mode is transparent.</span></span> <br/>                                                                                                                       |
| <span id="LWS_IGNORERETURN_"></span><span id="lws_ignorereturn_"></span><dl> <span data-ttu-id="6301f-109"><dt>**LWS \_ ИГНОРЕРЕТУРН**</dt></span><span class="sxs-lookup"><span data-stu-id="6301f-109"><dt>**LWS\_IGNORERETURN** </dt></span></span> </dl>       | <span data-ttu-id="6301f-110">Если ссылка имеет фокус клавиатуры и пользователь нажимает клавишу ВВОД, нажатие клавиши игнорируется элементом управления и передается в диалоговое окно хост.</span><span class="sxs-lookup"><span data-stu-id="6301f-110">When the link has keyboard focus and the user presses Enter, the keystroke is ignored by the control and passed to the host dialog box.</span></span><br/>                        |
| <span id="LWS_NOPREFIX"></span><span id="lws_noprefix"></span><dl> <span data-ttu-id="6301f-111"><dt>**\_префикс LWS**</dt></span><span class="sxs-lookup"><span data-stu-id="6301f-111"><dt>**LWS\_NOPREFIX**</dt></span></span> </dl>                      | <span data-ttu-id="6301f-112">**Windows Vista**.</span><span class="sxs-lookup"><span data-stu-id="6301f-112">**Windows Vista**.</span></span> <span data-ttu-id="6301f-113">Если текст содержит амперсанд, он обрабатывается как литеральный символ, а не как префикс для сочетания клавиш.</span><span class="sxs-lookup"><span data-stu-id="6301f-113">If the text contains an ampersand, it is treated as a literal character rather than the prefix to a shortcut key.</span></span><br/>                           |
| <span id="LWS_USEVISUALSTYLE_"></span><span id="lws_usevisualstyle_"></span><dl> <span data-ttu-id="6301f-114"><dt>**LWS \_ УСЕВИСУАЛСТИЛЕ**</dt></span><span class="sxs-lookup"><span data-stu-id="6301f-114"><dt>**LWS\_USEVISUALSTYLE** </dt></span></span> </dl> | <span data-ttu-id="6301f-115">**Windows Vista**.</span><span class="sxs-lookup"><span data-stu-id="6301f-115">**Windows Vista**.</span></span> <span data-ttu-id="6301f-116">Ссылка отображается в текущем визуальном стиле.</span><span class="sxs-lookup"><span data-stu-id="6301f-116">The link is displayed in the current visual style.</span></span><br/>                                                                                          |
| <span id="LWS_USECUSTOMTEXT"></span><span id="lws_usecustomtext"></span><dl> <span data-ttu-id="6301f-117"><dt>**\_УСЕКУСТОМТЕКСТ LWS**</dt></span><span class="sxs-lookup"><span data-stu-id="6301f-117"><dt>**LWS\_USECUSTOMTEXT**</dt></span></span> </dl>       | <span data-ttu-id="6301f-118">**Windows Vista**.</span><span class="sxs-lookup"><span data-stu-id="6301f-118">**Windows Vista**.</span></span> <span data-ttu-id="6301f-119">При прорисовке элемента управления отправляется уведомление о [NM \_ кустомтекст](nm-customtext.md) , чтобы приложение может предоставить текст динамически.</span><span class="sxs-lookup"><span data-stu-id="6301f-119">An [NM\_CUSTOMTEXT](nm-customtext.md) notification is sent when the control is drawn, so that the application can supply text dynamically.</span></span><br/> |
| <span id="LWS_RIGHT"></span><span id="lws_right"></span><dl> <span data-ttu-id="6301f-120"><dt>**LWS \_ справа**</dt></span><span class="sxs-lookup"><span data-stu-id="6301f-120"><dt>**LWS\_RIGHT**</dt></span></span> </dl>                               | <span data-ttu-id="6301f-121">**Windows Vista**.</span><span class="sxs-lookup"><span data-stu-id="6301f-121">**Windows Vista**.</span></span> <span data-ttu-id="6301f-122">Текст выравнивается по правому краю.</span><span class="sxs-lookup"><span data-stu-id="6301f-122">The text is right-justified.</span></span><br/>                                                                                                                |



## <a name="requirements"></a><span data-ttu-id="6301f-123">Требования</span><span class="sxs-lookup"><span data-stu-id="6301f-123">Requirements</span></span>



| <span data-ttu-id="6301f-124">Требование</span><span class="sxs-lookup"><span data-stu-id="6301f-124">Requirement</span></span> | <span data-ttu-id="6301f-125">Значение</span><span class="sxs-lookup"><span data-stu-id="6301f-125">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6301f-126">Header</span><span class="sxs-lookup"><span data-stu-id="6301f-126">Header</span></span><br/> | <dl> <span data-ttu-id="6301f-127"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="6301f-127"><dt>CommCtrl.h</dt></span></span> </dl> |



 

 





