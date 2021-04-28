---
title: Сообщение TDM_UPDATE_ELEMENT_TEXT (Коммктрл. h)
description: TDM_UPDATE_ELEMENT_TEXT сообщение — обновляет текстовый элемент в диалоговом окне задачи.
ms.assetid: 2df446c8-db87-42b5-b5bd-40fadbf9d45b
keywords:
- Элементы управления Windows для TDM_UPDATE_ELEMENT_TEXT сообщений
topic_type:
- apiref
api_name:
- TDM_UPDATE_ELEMENT_TEXT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c155b426b92645c0b9cdbabe00c44ffa722b89f3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085812"
---
# <a name="tdm_update_element_text-message"></a><span data-ttu-id="67196-104">\_ \_ Текстовое сообщение элемента обновления TDM \_</span><span class="sxs-lookup"><span data-stu-id="67196-104">TDM\_UPDATE\_ELEMENT\_TEXT message</span></span>

<span data-ttu-id="67196-105">Обновляет текстовый элемент в диалоговом окне задачи.</span><span class="sxs-lookup"><span data-stu-id="67196-105">Updates a text element in a task dialog.</span></span>

## <a name="parameters"></a><span data-ttu-id="67196-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="67196-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67196-107">*wParam* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="67196-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67196-108">Указывает обновляемый элемент.</span><span class="sxs-lookup"><span data-stu-id="67196-108">Indicates the element to update.</span></span> <span data-ttu-id="67196-109">(Иллюстрация элементов см. в разделе [о диалоговых окнах задач](task-dialogs-overview.md).) Этот параметр должен иметь одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="67196-109">(For an illustration of the elements, see [About Task Dialogs](task-dialogs-overview.md).) This parameter must be one of the following values:</span></span>



| <span data-ttu-id="67196-110">Значение</span><span class="sxs-lookup"><span data-stu-id="67196-110">Value</span></span>                                                                                                                                                                                           | <span data-ttu-id="67196-111">Значение</span><span class="sxs-lookup"><span data-stu-id="67196-111">Meaning</span></span>                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="TDE_CONTENT"></span><span id="tde_content"></span><dl> <span data-ttu-id="67196-112"><dt>**TDE \_ содержимое**</dt></span><span class="sxs-lookup"><span data-stu-id="67196-112"><dt>**TDE\_CONTENT**</dt></span></span> </dl>                                         | <span data-ttu-id="67196-113">Содержимое.</span><span class="sxs-lookup"><span data-stu-id="67196-113">Content.</span></span><br/>              |
| <span id="TDE_EXPANDED_INFORMATION"></span><span id="tde_expanded_information"></span><dl> <span data-ttu-id="67196-114"><dt>**TDE \_ Расширенная \_ информация**</dt></span><span class="sxs-lookup"><span data-stu-id="67196-114"><dt>**TDE\_EXPANDED\_INFORMATION**</dt></span></span> </dl> | <span data-ttu-id="67196-115">Расширенная информация.</span><span class="sxs-lookup"><span data-stu-id="67196-115">Expanded information.</span></span><br/> |
| <span id="TDE_FOOTER"></span><span id="tde_footer"></span><dl> <span data-ttu-id="67196-116"><dt>**\_Нижний КОЛОНТИТУЛ TDE**</dt></span><span class="sxs-lookup"><span data-stu-id="67196-116"><dt>**TDE\_FOOTER**</dt></span></span> </dl>                                            | <span data-ttu-id="67196-117">Текст нижнего колонтитула.</span><span class="sxs-lookup"><span data-stu-id="67196-117">Footer text.</span></span><br/>          |
| <span id="TDE_MAIN_INSTRUCTION"></span><span id="tde_main_instruction"></span><dl> <span data-ttu-id="67196-118"><dt>**\_Основная \_ инструкция TDE**</dt></span><span class="sxs-lookup"><span data-stu-id="67196-118"><dt>**TDE\_MAIN\_INSTRUCTION**</dt></span></span> </dl>             | <span data-ttu-id="67196-119">Основная инструкция.</span><span class="sxs-lookup"><span data-stu-id="67196-119">Main instruction.</span></span><br/>     |



 

</dd> <dt>

<span data-ttu-id="67196-120">*lParam* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="67196-120">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67196-121">Указатель на строку в Юникоде, содержащую новый текст.</span><span class="sxs-lookup"><span data-stu-id="67196-121">Pointer to a Unicode string that contains the new text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="67196-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="67196-122">Return value</span></span>

<span data-ttu-id="67196-123">Возвращаемое значение игнорируется.</span><span class="sxs-lookup"><span data-stu-id="67196-123">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="67196-124">Remarks</span><span class="sxs-lookup"><span data-stu-id="67196-124">Remarks</span></span>

<span data-ttu-id="67196-125">Чтобы избежать обрезки, новый текст должен быть больше, чем существующий текст.</span><span class="sxs-lookup"><span data-stu-id="67196-125">To avoid clipping, the new text must be no longer than the existing text.</span></span> <span data-ttu-id="67196-126">Установка более короткой строки текста не приводит к изменению размера диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="67196-126">Setting the text to a shorter string does not cause the dialog box to resize.</span></span>

<span data-ttu-id="67196-127">Если элемент **псзекспандединформатион** структуры [**таскдиалогконфиг**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) , используемый для создания диалогового окна задачи, имел **значение NULL**, и вы отправляете ТЕКСТОВОЕ сообщение об **\_ обновлении \_ \_ TDM** с \_ TDE \_ информацией, ничего не произойдет.</span><span class="sxs-lookup"><span data-stu-id="67196-127">If the **pszExpandedInformation** member of the [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) structure used to create the task dialog was **NULL**, and you send a **TDM\_UPDATE\_ELEMENT\_TEXT** message with TDE\_EXPANDED\_INFORMATION, nothing will happen.</span></span>

<span data-ttu-id="67196-128">Приведенные выше также применяются к нижнему колонтитулу и \_ нижнему колонтитулу TDE.</span><span class="sxs-lookup"><span data-stu-id="67196-128">The above also applies to the footer and TDE\_FOOTER.</span></span>

## <a name="requirements"></a><span data-ttu-id="67196-129">Требования</span><span class="sxs-lookup"><span data-stu-id="67196-129">Requirements</span></span>



| <span data-ttu-id="67196-130">Требование</span><span class="sxs-lookup"><span data-stu-id="67196-130">Requirement</span></span> | <span data-ttu-id="67196-131">Значение</span><span class="sxs-lookup"><span data-stu-id="67196-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="67196-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="67196-132">Minimum supported client</span></span><br/> | <span data-ttu-id="67196-133">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="67196-133">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="67196-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="67196-134">Minimum supported server</span></span><br/> | <span data-ttu-id="67196-135">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="67196-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="67196-136">Header</span><span class="sxs-lookup"><span data-stu-id="67196-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="67196-137"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="67196-137"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67196-138">См. также</span><span class="sxs-lookup"><span data-stu-id="67196-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67196-139">**\_ \_ текст элемента набора \_ TDM**</span><span class="sxs-lookup"><span data-stu-id="67196-139">**TDM\_SET\_ELEMENT\_TEXT**</span></span>](tdm-set-element-text.md)
</dt> </dl>

 

 





