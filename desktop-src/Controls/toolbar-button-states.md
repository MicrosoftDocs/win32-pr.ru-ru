---
title: Состояния кнопок панели инструментов (Коммктрл. h)
description: В этом разделе перечислены состояния, которые может иметь кнопка панели инструментов.
ms.assetid: 422e0d81-bd80-45dc-b843-82fc5d5c2a9a
topic_type:
- apiref
api_name:
- TBSTATE_CHECKED
- TBSTATE_ELLIPSES
- TBSTATE_ENABLED
- TBSTATE_HIDDEN
- TBSTATE_INDETERMINATE
- TBSTATE_MARKED
- TBSTATE_PRESSED
- TBSTATE_WRAP
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45262197c4432d9e3bb5c0884b3f76c986e4acfe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648683"
---
# <a name="toolbar-button-states"></a><span data-ttu-id="ea2a3-103">Состояния кнопок панели инструментов</span><span class="sxs-lookup"><span data-stu-id="ea2a3-103">Toolbar Button States</span></span>

<span data-ttu-id="ea2a3-104">В этом разделе перечислены состояния, которые может иметь кнопка панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="ea2a3-104">This section lists the states a toolbar button can have.</span></span>



| <span data-ttu-id="ea2a3-105">Константа</span><span class="sxs-lookup"><span data-stu-id="ea2a3-105">Constant</span></span>                                                                                                                                                                              | <span data-ttu-id="ea2a3-106">Описание</span><span class="sxs-lookup"><span data-stu-id="ea2a3-106">Description</span></span>                                                                                                                                           |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TBSTATE_CHECKED"></span><span id="tbstate_checked"></span><dl> <span data-ttu-id="ea2a3-107"><dt>**ТБСТАТЕ \_ Проверено**</dt></span><span class="sxs-lookup"><span data-stu-id="ea2a3-107"><dt>**TBSTATE\_CHECKED**</dt></span></span> </dl>                   | <span data-ttu-id="ea2a3-108">Кнопка имеет стиль [**\_ проверки тбстиле**](toolbar-control-and-button-styles.md) и нажата.</span><span class="sxs-lookup"><span data-stu-id="ea2a3-108">The button has the [**TBSTYLE\_CHECK**](toolbar-control-and-button-styles.md) style and is being clicked.</span></span><br/>                   |
| <span id="TBSTATE_ELLIPSES"></span><span id="tbstate_ellipses"></span><dl> <span data-ttu-id="ea2a3-109"><dt>**ТБСТАТЕ \_ многоточия**</dt></span><span class="sxs-lookup"><span data-stu-id="ea2a3-109"><dt>**TBSTATE\_ELLIPSES**</dt></span></span> </dl>                | <span data-ttu-id="ea2a3-110">[Версия 4,70](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="ea2a3-110">[Version 4.70](common-control-versions.md).</span></span> <span data-ttu-id="ea2a3-111">Текст кнопки обрезан и отображается многоточие.</span><span class="sxs-lookup"><span data-stu-id="ea2a3-111">The button's text is cut off and an ellipsis is displayed.</span></span><br/>                                    |
| <span id="TBSTATE_ENABLED"></span><span id="tbstate_enabled"></span><dl> <span data-ttu-id="ea2a3-112"><dt>**ТБСТАТЕ \_ включен**</dt></span><span class="sxs-lookup"><span data-stu-id="ea2a3-112"><dt>**TBSTATE\_ENABLED**</dt></span></span> </dl>                   | <span data-ttu-id="ea2a3-113">Кнопка принимает введенные пользователем данные.</span><span class="sxs-lookup"><span data-stu-id="ea2a3-113">The button accepts user input.</span></span> <span data-ttu-id="ea2a3-114">Кнопка, которая не имеет этого состояния, отображается серым цветом.</span><span class="sxs-lookup"><span data-stu-id="ea2a3-114">A button that does not have this state is grayed.</span></span><br/>                                                           |
| <span id="TBSTATE_HIDDEN"></span><span id="tbstate_hidden"></span><dl> <span data-ttu-id="ea2a3-115"><dt>**ТБСТАТЕ \_ скрыто**</dt></span><span class="sxs-lookup"><span data-stu-id="ea2a3-115"><dt>**TBSTATE\_HIDDEN**</dt></span></span> </dl>                      | <span data-ttu-id="ea2a3-116">Кнопка невидима и не может принимать данные, вводимые пользователем.</span><span class="sxs-lookup"><span data-stu-id="ea2a3-116">The button is not visible and cannot receive user input.</span></span><br/>                                                                                   |
| <span id="TBSTATE_INDETERMINATE"></span><span id="tbstate_indeterminate"></span><dl> <span data-ttu-id="ea2a3-117"><dt>**ТБСТАТЕ \_ неопределенный**</dt></span><span class="sxs-lookup"><span data-stu-id="ea2a3-117"><dt>**TBSTATE\_INDETERMINATE**</dt></span></span> </dl> | <span data-ttu-id="ea2a3-118">Кнопка неактивна.</span><span class="sxs-lookup"><span data-stu-id="ea2a3-118">The button is grayed.</span></span><br/>                                                                                                                      |
| <span id="TBSTATE_MARKED"></span><span id="tbstate_marked"></span><dl> <span data-ttu-id="ea2a3-119"><dt>**ТБСТАТЕ \_ помечено**</dt></span><span class="sxs-lookup"><span data-stu-id="ea2a3-119"><dt>**TBSTATE\_MARKED**</dt></span></span> </dl>                      | <span data-ttu-id="ea2a3-120">[Версия 4,71](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="ea2a3-120">[Version 4.71](common-control-versions.md).</span></span> <span data-ttu-id="ea2a3-121">Кнопка помечена.</span><span class="sxs-lookup"><span data-stu-id="ea2a3-121">The button is marked.</span></span> <span data-ttu-id="ea2a3-122">Интерпретация помеченного элемента зависит от приложения.</span><span class="sxs-lookup"><span data-stu-id="ea2a3-122">The interpretation of a marked item is dependent upon the application.</span></span> <br/> |
| <span id="TBSTATE_PRESSED"></span><span id="tbstate_pressed"></span><dl> <span data-ttu-id="ea2a3-123"><dt>**ТБСТАТЕ \_ нажата**</dt></span><span class="sxs-lookup"><span data-stu-id="ea2a3-123"><dt>**TBSTATE\_PRESSED**</dt></span></span> </dl>                   | <span data-ttu-id="ea2a3-124">Нажата кнопка.</span><span class="sxs-lookup"><span data-stu-id="ea2a3-124">The button is being clicked.</span></span><br/>                                                                                                               |
| <span id="TBSTATE_WRAP"></span><span id="tbstate_wrap"></span><dl> <span data-ttu-id="ea2a3-125"><dt>**ТБСТАТЕ \_ Перенос**</dt></span><span class="sxs-lookup"><span data-stu-id="ea2a3-125"><dt>**TBSTATE\_WRAP**</dt></span></span> </dl>                            | <span data-ttu-id="ea2a3-126">За кнопкой следует разрыв строки.</span><span class="sxs-lookup"><span data-stu-id="ea2a3-126">The button is followed by a line break.</span></span> <span data-ttu-id="ea2a3-127">Кнопка также должна иметь \_ состояние тбстате Enabled (включено).</span><span class="sxs-lookup"><span data-stu-id="ea2a3-127">The button must also have the TBSTATE\_ENABLED state.</span></span><br/>                                              |



## <a name="remarks"></a><span data-ttu-id="ea2a3-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ea2a3-128">Remarks</span></span>

<span data-ttu-id="ea2a3-129">Панель инструментов может иметь сочетание состояний.</span><span class="sxs-lookup"><span data-stu-id="ea2a3-129">A toolbar may have a combination of states.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea2a3-130">Требования</span><span class="sxs-lookup"><span data-stu-id="ea2a3-130">Requirements</span></span>



| <span data-ttu-id="ea2a3-131">Требование</span><span class="sxs-lookup"><span data-stu-id="ea2a3-131">Requirement</span></span> | <span data-ttu-id="ea2a3-132">Значение</span><span class="sxs-lookup"><span data-stu-id="ea2a3-132">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ea2a3-133">Header</span><span class="sxs-lookup"><span data-stu-id="ea2a3-133">Header</span></span><br/> | <dl> <span data-ttu-id="ea2a3-134"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="ea2a3-134"><dt>CommCtrl.h</dt></span></span> </dl> |



 

 





