---
title: Сообщение CBEM_SETEXTENDEDSTYLE (Коммктрл. h)
description: Задает расширенные стили в элементе управления ComboBoxEx.
ms.assetid: 00848bd0-5a2f-4bfb-ae1f-ee3aa88ac57a
keywords:
- Элементы управления Windows для CBEM_SETEXTENDEDSTYLE сообщений
topic_type:
- apiref
api_name:
- CBEM_SETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0a60518d2f6130c2c89e379125308fc2e647c6a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654693"
---
# <a name="cbem_setextendedstyle-message"></a><span data-ttu-id="223a9-104">\_Сообщение кбем сетекстендедстиле</span><span class="sxs-lookup"><span data-stu-id="223a9-104">CBEM\_SETEXTENDEDSTYLE message</span></span>

<span data-ttu-id="223a9-105">Задает расширенные стили в элементе управления ComboBoxEx.</span><span class="sxs-lookup"><span data-stu-id="223a9-105">Sets extended styles within a ComboBoxEx control.</span></span>

## <a name="parameters"></a><span data-ttu-id="223a9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="223a9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="223a9-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="223a9-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="223a9-108">Значение **типа DWORD** , указывающее, какие стили в *lParam* должны быть затронуты.</span><span class="sxs-lookup"><span data-stu-id="223a9-108">A **DWORD** value that indicates which styles in *lParam* are to be affected.</span></span> <span data-ttu-id="223a9-109">Будут изменены только расширенные стили в параметре *wParam* .</span><span class="sxs-lookup"><span data-stu-id="223a9-109">Only the extended styles in *wParam* will be changed.</span></span> <span data-ttu-id="223a9-110">Если этот параметр равен нулю, будут затронуты все стили в *lParam* .</span><span class="sxs-lookup"><span data-stu-id="223a9-110">If this parameter is zero, then all of the styles in *lParam* will be affected.</span></span>

</dd> <dt>

<span data-ttu-id="223a9-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="223a9-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="223a9-112">Значение **типа DWORD** , содержащее [Расширенные стили элемента управления ComboBoxEx](comboboxex-control-extended-styles.md) , заданные для элемента управления.</span><span class="sxs-lookup"><span data-stu-id="223a9-112">A **DWORD** value that contains the [ComboBoxEx Control Extended Styles](comboboxex-control-extended-styles.md) to set for the control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="223a9-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="223a9-113">Return value</span></span>

<span data-ttu-id="223a9-114">Возвращает значение **типа DWORD** , содержащее расширенные стили, которые использовались ранее для элемента управления.</span><span class="sxs-lookup"><span data-stu-id="223a9-114">Returns a **DWORD** value that contains the extended styles previously used for the control.</span></span>

## <a name="remarks"></a><span data-ttu-id="223a9-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="223a9-115">Remarks</span></span>

<span data-ttu-id="223a9-116">*wParam* позволяет изменять один или несколько расширенных стилей без предварительного получения существующих стилей.</span><span class="sxs-lookup"><span data-stu-id="223a9-116">*wParam* enables you to modify one or more extended styles without having to retrieve the existing styles first.</span></span> <span data-ttu-id="223a9-117">Например, если передать [**кбес \_ ex \_ ноедитимаже**](comboboxex-control-extended-styles.md) для *wParam* и 0 для *lParam*, то стиль **кбес \_ ex \_ ноедитимаже** будет сброшен, но все остальные стили останутся прежними.</span><span class="sxs-lookup"><span data-stu-id="223a9-117">For example, if you pass [**CBES\_EX\_NOEDITIMAGE**](comboboxex-control-extended-styles.md) for *wParam* and 0 for *lParam*, the **CBES\_EX\_NOEDITIMAGE** style will be cleared, but all other styles will remain the same.</span></span>

<span data-ttu-id="223a9-118">Если вы попытаетесь задать расширенный стиль для элемента управления ComboBoxEx, созданного с помощью [**\_ простого стиля CBS**](combo-box-styles.md) , он может не перерисовываться должным образом.</span><span class="sxs-lookup"><span data-stu-id="223a9-118">If you try to set an extended style for a ComboBoxEx control created with the [**CBS\_SIMPLE**](combo-box-styles.md) style, it may not repaint properly.</span></span>

## <a name="requirements"></a><span data-ttu-id="223a9-119">Требования</span><span class="sxs-lookup"><span data-stu-id="223a9-119">Requirements</span></span>



| <span data-ttu-id="223a9-120">Требование</span><span class="sxs-lookup"><span data-stu-id="223a9-120">Requirement</span></span> | <span data-ttu-id="223a9-121">Значение</span><span class="sxs-lookup"><span data-stu-id="223a9-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="223a9-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="223a9-122">Minimum supported client</span></span><br/> | <span data-ttu-id="223a9-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="223a9-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="223a9-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="223a9-124">Minimum supported server</span></span><br/> | <span data-ttu-id="223a9-125">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="223a9-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="223a9-126">Header</span><span class="sxs-lookup"><span data-stu-id="223a9-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="223a9-127"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="223a9-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





