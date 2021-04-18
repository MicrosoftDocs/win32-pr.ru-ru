---
title: Сообщение TCM_GETITEM (Коммктрл. h)
description: Извлекает сведения о вкладке в элементе управления "Вкладка". Это сообщение можно отправить явным образом или с помощью \_ макроса табктрл.
ms.assetid: 41774f14-c4e9-4c98-bc25-3522b2125ed5
keywords:
- Элементы управления Windows для TCM_GETITEM сообщений
topic_type:
- apiref
api_name:
- TCM_GETITEM
- TCM_GETITEMA
- TCM_GETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6f94f26a0893416847df052ff47731391a86f5f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654669"
---
# <a name="tcm_getitem-message"></a><span data-ttu-id="eaee6-105">Сообщение для TCM \_ Item</span><span class="sxs-lookup"><span data-stu-id="eaee6-105">TCM\_GETITEM message</span></span>

<span data-ttu-id="eaee6-106">Извлекает сведения о вкладке в элементе управления "Вкладка".</span><span class="sxs-lookup"><span data-stu-id="eaee6-106">Retrieves information about a tab in a tab control.</span></span> <span data-ttu-id="eaee6-107">Это сообщение можно отправить явным образом или с помощью макроса [**табктрл \_**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getitem) .</span><span class="sxs-lookup"><span data-stu-id="eaee6-107">You can send this message explicitly or by using the [**TabCtrl\_GetItem**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="eaee6-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="eaee6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eaee6-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="eaee6-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="eaee6-110">Индекс вкладки.</span><span class="sxs-lookup"><span data-stu-id="eaee6-110">Index of the tab.</span></span>

</dd> <dt>

<span data-ttu-id="eaee6-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="eaee6-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="eaee6-112">Указатель на структуру [**тЦитем**](/windows/win32/api/commctrl/ns-commctrl-tcitema) , указывающую сведения для извлечения и получения сведений об этой вкладке. При отправке сообщения элемент **Mask** указывает, какие атрибуты должны быть возвращены.</span><span class="sxs-lookup"><span data-stu-id="eaee6-112">Pointer to a [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) structure that specifies the information to retrieve and receives information about the tab. When the message is sent, the **mask** member specifies which attributes to return.</span></span> <span data-ttu-id="eaee6-113">Если элемент **маски** задает \_ текстовое значение тЦиф, то элемент **псзтекст** должен содержать адрес буфера, который получает текст элемента, а элемент **кчтекстмакс** должен задавать размер буфера.</span><span class="sxs-lookup"><span data-stu-id="eaee6-113">If the **mask** member specifies the TCIF\_TEXT value, the **pszText** member must contain the address of the buffer that receives the item text, and the **cchTextMax** member must specify the size of the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eaee6-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="eaee6-114">Return value</span></span>

<span data-ttu-id="eaee6-115">Возвращает **значение true** , если успешно, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="eaee6-115">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="eaee6-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="eaee6-116">Remarks</span></span>

<span data-ttu-id="eaee6-117">Если в элементе \_ **Mask** структуры [**тЦитем**](/windows/win32/api/commctrl/ns-commctrl-tcitema) задан флаг тЦиф Text, элемент управления может изменить элемент **псзтекст** структуры так, чтобы он указывал на новый текст вместо заполнения буфера запрошенным текстом.</span><span class="sxs-lookup"><span data-stu-id="eaee6-117">If the TCIF\_TEXT flag is set in the **mask** member of the [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) structure, the control may change the **pszText** member of the structure to point to the new text instead of filling the buffer with the requested text.</span></span> <span data-ttu-id="eaee6-118">Элемент управления может установить для элемента **Псзтекст** **значение NULL** , чтобы указать, что с элементом не связана ни один текст.</span><span class="sxs-lookup"><span data-stu-id="eaee6-118">The control may set the **pszText** member to **NULL** to indicate that no text is associated with the item.</span></span>

## <a name="requirements"></a><span data-ttu-id="eaee6-119">Требования</span><span class="sxs-lookup"><span data-stu-id="eaee6-119">Requirements</span></span>



| <span data-ttu-id="eaee6-120">Требование</span><span class="sxs-lookup"><span data-stu-id="eaee6-120">Requirement</span></span> | <span data-ttu-id="eaee6-121">Значение</span><span class="sxs-lookup"><span data-stu-id="eaee6-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="eaee6-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="eaee6-122">Minimum supported client</span></span><br/> | <span data-ttu-id="eaee6-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="eaee6-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="eaee6-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="eaee6-124">Minimum supported server</span></span><br/> | <span data-ttu-id="eaee6-125">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="eaee6-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="eaee6-126">Header</span><span class="sxs-lookup"><span data-stu-id="eaee6-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="eaee6-127"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="eaee6-127"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="eaee6-128">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="eaee6-128">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="eaee6-129">**TCM \_ ЖЕТИТЕМВ** (Юникод) и **TCM- \_ Item** a (ANSI)</span><span class="sxs-lookup"><span data-stu-id="eaee6-129">**TCM\_GETITEMW** (Unicode) and **TCM\_GETITEMA** (ANSI)</span></span><br/>                   |



 

 





