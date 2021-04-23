---
title: Сообщение EM_SETOPTIONS (RichEdit. h)
description: Задает параметры для элемента управления Rich Edit.
ms.assetid: 98ef2de9-4c34-45ba-8e8a-eaf505f97f56
keywords:
- Элементы управления Windows для EM_SETOPTIONS сообщений
topic_type:
- apiref
api_name:
- EM_SETOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c43dda8268b42dc264a86600826d2a6b550e35c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135726"
---
# <a name="em_setoptions-message"></a><span data-ttu-id="39a38-104">\_Сообщение СЕТОПТИОНС EM</span><span class="sxs-lookup"><span data-stu-id="39a38-104">EM\_SETOPTIONS message</span></span>

<span data-ttu-id="39a38-105">Задает параметры для элемента управления Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="39a38-105">Sets the options for a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="39a38-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="39a38-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39a38-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="39a38-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="39a38-108">Указывает операцию, которая может принимать одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="39a38-108">Specifies the operation, which can be one of these values.</span></span>



| <span data-ttu-id="39a38-109">Значение</span><span class="sxs-lookup"><span data-stu-id="39a38-109">Value</span></span>                                                                                                                                             | <span data-ttu-id="39a38-110">Значение</span><span class="sxs-lookup"><span data-stu-id="39a38-110">Meaning</span></span>                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <span id="ECOOP_SET"></span><span id="ecoop_set"></span><dl> <span data-ttu-id="39a38-111"><dt>**\_набор екуп**</dt></span><span class="sxs-lookup"><span data-stu-id="39a38-111"><dt>**ECOOP\_SET**</dt></span></span> </dl> | <span data-ttu-id="39a38-112">Задает параметры, заданные параметром *lParam*.</span><span class="sxs-lookup"><span data-stu-id="39a38-112">Sets the options to those specified by *lParam*.</span></span><br/>                             |
| <span id="ECOOP_OR"></span><span id="ecoop_or"></span><dl> <span data-ttu-id="39a38-113"><dt>**ЕКУП \_ или**</dt></span><span class="sxs-lookup"><span data-stu-id="39a38-113"><dt>**ECOOP\_OR**</dt></span></span> </dl>    | <span data-ttu-id="39a38-114">Объединяет указанные параметры с текущими параметрами.</span><span class="sxs-lookup"><span data-stu-id="39a38-114">Combines the specified options with the current options.</span></span><br/>                     |
| <span id="ECOOP_AND"></span><span id="ecoop_and"></span><dl> <span data-ttu-id="39a38-115"><dt>**ЕКУП \_ и**</dt></span><span class="sxs-lookup"><span data-stu-id="39a38-115"><dt>**ECOOP\_AND**</dt></span></span> </dl> | <span data-ttu-id="39a38-116">Сохраняются только текущие параметры, которые также задаются параметром *lParam*.</span><span class="sxs-lookup"><span data-stu-id="39a38-116">Retains only those current options that are also specified by *lParam*.</span></span><br/>      |
| <span id="ECOOP_XOR"></span><span id="ecoop_xor"></span><dl> <span data-ttu-id="39a38-117"><dt>**ЕКУП \_ XOR**</dt></span><span class="sxs-lookup"><span data-stu-id="39a38-117"><dt>**ECOOP\_XOR**</dt></span></span> </dl> | <span data-ttu-id="39a38-118">Логически исключающие или текущие параметры с параметрами, указанными как *lParam*.</span><span class="sxs-lookup"><span data-stu-id="39a38-118">Logically exclusive OR the current options with those specified by *lParam*.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="39a38-119">*lParam*</span><span class="sxs-lookup"><span data-stu-id="39a38-119">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="39a38-120">Задает одно или несколько из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="39a38-120">Specifies one or more of the following values.</span></span>



| <span data-ttu-id="39a38-121">Значение</span><span class="sxs-lookup"><span data-stu-id="39a38-121">Value</span></span>                                                                                                                                                                                 | <span data-ttu-id="39a38-122">Значение</span><span class="sxs-lookup"><span data-stu-id="39a38-122">Meaning</span></span>                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span id="ECO_AUTOWORDSELECTION"></span><span id="eco_autowordselection"></span><dl> <span data-ttu-id="39a38-123"><dt>**ЭКОНОМИЧный \_ аутовордселектион**</dt></span><span class="sxs-lookup"><span data-stu-id="39a38-123"><dt>**ECO\_AUTOWORDSELECTION**</dt></span></span> </dl> | <span data-ttu-id="39a38-124">Автоматический выбор слова при двойном щелчке.</span><span class="sxs-lookup"><span data-stu-id="39a38-124">Automatic selection of word on double-click.</span></span><br/>                                                                           |
| <span id="ECO_AUTOVSCROLL"></span><span id="eco_autovscroll"></span><dl> <span data-ttu-id="39a38-125"><dt>**ЭКОНОМИЧный \_ аутовскролл**</dt></span><span class="sxs-lookup"><span data-stu-id="39a38-125"><dt>**ECO\_AUTOVSCROLL**</dt></span></span> </dl>                   | <span data-ttu-id="39a38-126">Аналогично [**\_ аутовскролл**](rich-edit-control-styles.md) стилю.</span><span class="sxs-lookup"><span data-stu-id="39a38-126">Same as [**ES\_AUTOVSCROLL**](rich-edit-control-styles.md) style.</span></span><br/>                                      |
| <span id="ECO_AUTOHSCROLL"></span><span id="eco_autohscroll"></span><dl> <span data-ttu-id="39a38-127"><dt>**ЭКОНОМИЧный \_ аутохскролл**</dt></span><span class="sxs-lookup"><span data-stu-id="39a38-127"><dt>**ECO\_AUTOHSCROLL**</dt></span></span> </dl>                   | <span data-ttu-id="39a38-128">Аналогично [**\_ аутохскролл**](rich-edit-control-styles.md) стилю.</span><span class="sxs-lookup"><span data-stu-id="39a38-128">Same as [**ES\_AUTOHSCROLL**](rich-edit-control-styles.md) style.</span></span><br/>                                      |
| <span id="ECO_NOHIDESEL"></span><span id="eco_nohidesel"></span><dl> <span data-ttu-id="39a38-129"><dt>**ЭКОНОМИЧный \_ нохидесел**</dt></span><span class="sxs-lookup"><span data-stu-id="39a38-129"><dt>**ECO\_NOHIDESEL**</dt></span></span> </dl>                         | <span data-ttu-id="39a38-130">Аналогично [**\_ нохидесел**](rich-edit-control-styles.md) стилю.</span><span class="sxs-lookup"><span data-stu-id="39a38-130">Same as [**ES\_NOHIDESEL**](rich-edit-control-styles.md) style.</span></span><br/>                                          |
| <span id="ECO_READONLY"></span><span id="eco_readonly"></span><dl> <span data-ttu-id="39a38-131"><dt>**ЭКОНОМИЧное \_ чтение**</dt></span><span class="sxs-lookup"><span data-stu-id="39a38-131"><dt>**ECO\_READONLY**</dt></span></span> </dl>                            | <span data-ttu-id="39a38-132">То же, что и стиль [**\_ только для чтения**](rich-edit-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="39a38-132">Same as [**ES\_READONLY**](rich-edit-control-styles.md) style.</span></span><br/>                                            |
| <span id="ECO_WANTRETURN"></span><span id="eco_wantreturn"></span><dl> <span data-ttu-id="39a38-133"><dt>**ЭКОНОМИЧный \_ вантретурн**</dt></span><span class="sxs-lookup"><span data-stu-id="39a38-133"><dt>**ECO\_WANTRETURN**</dt></span></span> </dl>                      | <span data-ttu-id="39a38-134">Аналогично [**\_ вантретурн**](rich-edit-control-styles.md) стилю.</span><span class="sxs-lookup"><span data-stu-id="39a38-134">Same as [**ES\_WANTRETURN**](rich-edit-control-styles.md) style.</span></span><br/>                                        |
| <span id="ECO_SELECTIONBAR"></span><span id="eco_selectionbar"></span><dl> <span data-ttu-id="39a38-135"><dt>**ЭКОНОМИЧный \_ селектионбар**</dt></span><span class="sxs-lookup"><span data-stu-id="39a38-135"><dt>**ECO\_SELECTIONBAR**</dt></span></span> </dl>                | <span data-ttu-id="39a38-136">Аналогично [**\_ селектионбар**](rich-edit-control-styles.md) стилю.</span><span class="sxs-lookup"><span data-stu-id="39a38-136">Same as [**ES\_SELECTIONBAR**](rich-edit-control-styles.md) style.</span></span><br/>                                    |
| <span id="ECO_VERTICAL"></span><span id="eco_vertical"></span><dl> <span data-ttu-id="39a38-137"><dt>**ЭКОНОМИЧный \_ по вертикали**</dt></span><span class="sxs-lookup"><span data-stu-id="39a38-137"><dt>**ECO\_VERTICAL**</dt></span></span> </dl>                            | <span data-ttu-id="39a38-138">То же, что и [**\_ вертикальный стиль ES**](rich-edit-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="39a38-138">Same as [**ES\_VERTICAL**](rich-edit-control-styles.md) style.</span></span> <span data-ttu-id="39a38-139">Доступно только в версиях для азиатских языков.</span><span class="sxs-lookup"><span data-stu-id="39a38-139">Available in Asian-language versions only.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39a38-140">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="39a38-140">Return value</span></span>

<span data-ttu-id="39a38-141">Это сообщение возвращает текущие параметры элемента управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="39a38-141">This message returns the current options of the edit control.</span></span>

## <a name="requirements"></a><span data-ttu-id="39a38-142">Требования</span><span class="sxs-lookup"><span data-stu-id="39a38-142">Requirements</span></span>



| <span data-ttu-id="39a38-143">Требование</span><span class="sxs-lookup"><span data-stu-id="39a38-143">Requirement</span></span> | <span data-ttu-id="39a38-144">Значение</span><span class="sxs-lookup"><span data-stu-id="39a38-144">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="39a38-145">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="39a38-145">Minimum supported client</span></span><br/> | <span data-ttu-id="39a38-146">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="39a38-146">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="39a38-147">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="39a38-147">Minimum supported server</span></span><br/> | <span data-ttu-id="39a38-148">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="39a38-148">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="39a38-149">Header</span><span class="sxs-lookup"><span data-stu-id="39a38-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="39a38-150"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="39a38-150"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39a38-151">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="39a38-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39a38-152">**Стили элемента управления Rich Edit**</span><span class="sxs-lookup"><span data-stu-id="39a38-152">**Rich Edit Control Styles**</span></span>](rich-edit-control-styles.md)
</dt> </dl>

 

 





