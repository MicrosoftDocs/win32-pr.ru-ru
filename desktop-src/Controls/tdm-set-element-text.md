---
title: Сообщение TDM_SET_ELEMENT_TEXT (Коммктрл. h)
description: TDM_SET_ELEMENT_TEXT сообщение — обновляет текстовый элемент в диалоговом окне задачи.
ms.assetid: e3f15805-5d48-4549-9959-69ec01345e57
keywords:
- Элементы управления Windows для TDM_SET_ELEMENT_TEXT сообщений
topic_type:
- apiref
api_name:
- TDM_SET_ELEMENT_TEXT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6d0c8830a6d8a1057ab283a9e096434a6184151
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104032"
---
# <a name="tdm_set_element_text-message"></a><span data-ttu-id="88243-104">\_ \_ Текстовое сообщение для элемента набора TDM \_</span><span class="sxs-lookup"><span data-stu-id="88243-104">TDM\_SET\_ELEMENT\_TEXT message</span></span>

<span data-ttu-id="88243-105">Обновляет текстовый элемент в диалоговом окне задачи.</span><span class="sxs-lookup"><span data-stu-id="88243-105">Updates a text element in a task dialog.</span></span>

## <a name="parameters"></a><span data-ttu-id="88243-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="88243-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88243-107">*wParam* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="88243-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="88243-108">Указывает обновляемый элемент.</span><span class="sxs-lookup"><span data-stu-id="88243-108">Indicates the element to update.</span></span> <span data-ttu-id="88243-109">(Иллюстрация см. в разделе [о диалоговых окнах задач](task-dialogs-overview.md).) Этот параметр должен иметь одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="88243-109">(For an illustration, see [About Task Dialogs](task-dialogs-overview.md).) This parameter must be one of the following values.</span></span>



| <span data-ttu-id="88243-110">Значение</span><span class="sxs-lookup"><span data-stu-id="88243-110">Value</span></span>                                                                                                                                                                                           | <span data-ttu-id="88243-111">Значение</span><span class="sxs-lookup"><span data-stu-id="88243-111">Meaning</span></span>                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="TDE_CONTENT"></span><span id="tde_content"></span><dl> <span data-ttu-id="88243-112"><dt>**TDE \_ содержимое**</dt></span><span class="sxs-lookup"><span data-stu-id="88243-112"><dt>**TDE\_CONTENT**</dt></span></span> </dl>                                         | <span data-ttu-id="88243-113">Содержимое.</span><span class="sxs-lookup"><span data-stu-id="88243-113">Content.</span></span><br/>              |
| <span id="TDE_EXPANDED_INFORMATION"></span><span id="tde_expanded_information"></span><dl> <span data-ttu-id="88243-114"><dt>**TDE \_ Расширенная \_ информация**</dt></span><span class="sxs-lookup"><span data-stu-id="88243-114"><dt>**TDE\_EXPANDED\_INFORMATION**</dt></span></span> </dl> | <span data-ttu-id="88243-115">Расширенная информация.</span><span class="sxs-lookup"><span data-stu-id="88243-115">Expanded information.</span></span><br/> |
| <span id="TDE_FOOTER"></span><span id="tde_footer"></span><dl> <span data-ttu-id="88243-116"><dt>**\_Нижний КОЛОНТИТУЛ TDE**</dt></span><span class="sxs-lookup"><span data-stu-id="88243-116"><dt>**TDE\_FOOTER**</dt></span></span> </dl>                                            | <span data-ttu-id="88243-117">Текст нижнего колонтитула.</span><span class="sxs-lookup"><span data-stu-id="88243-117">Footer text.</span></span><br/>          |
| <span id="TDE_MAIN_INSTRUCTION"></span><span id="tde_main_instruction"></span><dl> <span data-ttu-id="88243-118"><dt>**\_Основная \_ инструкция TDE**</dt></span><span class="sxs-lookup"><span data-stu-id="88243-118"><dt>**TDE\_MAIN\_INSTRUCTION**</dt></span></span> </dl>             | <span data-ttu-id="88243-119">Основная инструкция.</span><span class="sxs-lookup"><span data-stu-id="88243-119">Main instruction.</span></span><br/>     |



 

</dd> <dt>

<span data-ttu-id="88243-120">*lParam* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="88243-120">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="88243-121">Новый текст для использования.</span><span class="sxs-lookup"><span data-stu-id="88243-121">The new text to use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="88243-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="88243-122">Return value</span></span>

<span data-ttu-id="88243-123">Возвращаемое значение игнорируется.</span><span class="sxs-lookup"><span data-stu-id="88243-123">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="88243-124">Remarks</span><span class="sxs-lookup"><span data-stu-id="88243-124">Remarks</span></span>

<span data-ttu-id="88243-125">Размер или структура диалогового окна задачи может измениться для размещения нового текста.</span><span class="sxs-lookup"><span data-stu-id="88243-125">The size or layout of the task dialog may change to accommodate the new text.</span></span>

## <a name="examples"></a><span data-ttu-id="88243-126">Примеры</span><span class="sxs-lookup"><span data-stu-id="88243-126">Examples</span></span>

<span data-ttu-id="88243-127">В следующем примере кода показано, как задать текст нижнего колонтитула в диалоговом окне задачи, представленном *HWND*.</span><span class="sxs-lookup"><span data-stu-id="88243-127">The following example code shows how to set the footer text in the task dialog represented by *hwnd*.</span></span>


```C++
SendMessage(hwnd, TDM_SET_ELEMENT_TEXT, (WPARAM)TDE_FOOTER, (LPARAM)L"New footer text.");
```



## <a name="requirements"></a><span data-ttu-id="88243-128">Требования</span><span class="sxs-lookup"><span data-stu-id="88243-128">Requirements</span></span>



| <span data-ttu-id="88243-129">Требование</span><span class="sxs-lookup"><span data-stu-id="88243-129">Requirement</span></span> | <span data-ttu-id="88243-130">Значение</span><span class="sxs-lookup"><span data-stu-id="88243-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="88243-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="88243-131">Minimum supported client</span></span><br/> | <span data-ttu-id="88243-132">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="88243-132">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="88243-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="88243-133">Minimum supported server</span></span><br/> | <span data-ttu-id="88243-134">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="88243-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="88243-135">Header</span><span class="sxs-lookup"><span data-stu-id="88243-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="88243-136"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="88243-136"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88243-137">См. также</span><span class="sxs-lookup"><span data-stu-id="88243-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88243-138">**\_ \_ текст элемента обновления \_ TDM**</span><span class="sxs-lookup"><span data-stu-id="88243-138">**TDM\_UPDATE\_ELEMENT\_TEXT**</span></span>](tdm-update-element-text.md)
</dt> </dl>

 

 





