---
title: Сообщение CBEM_GETITEM (Коммктрл. h)
description: Возвращает сведения об элементе для заданного ComboBoxEx элемента.
ms.assetid: 2df07ae8-fa84-487c-a4a7-90244dfdb40e
keywords:
- Элементы управления Windows для CBEM_GETITEM сообщений
topic_type:
- apiref
api_name:
- CBEM_GETITEM
- CBEM_GETITEMA
- CBEM_GETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 940bbf7aea8ec93dd0f808937d959477c964df96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654655"
---
# <a name="cbem_getitem-message"></a><span data-ttu-id="9b550-104">\_Сообщение кбем</span><span class="sxs-lookup"><span data-stu-id="9b550-104">CBEM\_GETITEM message</span></span>

<span data-ttu-id="9b550-105">Возвращает сведения об элементе для заданного ComboBoxEx элемента.</span><span class="sxs-lookup"><span data-stu-id="9b550-105">Gets item information for a given ComboBoxEx item.</span></span>

## <a name="parameters"></a><span data-ttu-id="9b550-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9b550-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b550-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9b550-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="9b550-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="9b550-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="9b550-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9b550-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9b550-110">Указатель на структуру [**комбобоксекситем**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) , которая получает сведения об элементе.</span><span class="sxs-lookup"><span data-stu-id="9b550-110">A pointer to a [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) structure that receives the item information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9b550-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9b550-111">Return value</span></span>

<span data-ttu-id="9b550-112">Возвращает ненулевое значение в случае успеха или ноль в противном случае.</span><span class="sxs-lookup"><span data-stu-id="9b550-112">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="9b550-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9b550-113">Remarks</span></span>

<span data-ttu-id="9b550-114">При отправке сообщения необходимо задать элементы **Член iItem** и **Mask** структуры, чтобы указать индекс целевого элемента и тип извлекаемых данных.</span><span class="sxs-lookup"><span data-stu-id="9b550-114">When the message is sent, the **iItem** and **mask** members of the structure must be set to indicate the index of the target item and the type of information to be retrieved.</span></span> <span data-ttu-id="9b550-115">Другие элементы устанавливаются по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="9b550-115">Other members are set as needed.</span></span> <span data-ttu-id="9b550-116">Например, чтобы получить текст, необходимо установить \_ флаг кбеиф Text в **Mask** и присвоить значение **кчтекстмакс**.</span><span class="sxs-lookup"><span data-stu-id="9b550-116">For example, to retrieve text, you must set the CBEIF\_TEXT flag in **mask**, and assign a value to **cchTextMax**.</span></span> <span data-ttu-id="9b550-117">При установке элемента **Член iItem** в значение-1 будет получен элемент, отображаемый в элементе управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="9b550-117">Setting the **iItem** member to -1 will retrieve the item displayed in the edit control.</span></span>

<span data-ttu-id="9b550-118">Если в элементе \_ **Mask** структуры [**комбобоксекситем**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) задан флаг кбеиф Text, элемент управления может изменить элемент **псзтекст** структуры так, чтобы он указывал на новый текст вместо заполнения буфера запрошенным текстом.</span><span class="sxs-lookup"><span data-stu-id="9b550-118">If the CBEIF\_TEXT flag is set in the **mask** member of the [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) structure, the control may change the **pszText** member of the structure to point to the new text instead of filling the buffer with the requested text.</span></span> <span data-ttu-id="9b550-119">Приложения не должны рассчитывать, что текст всегда будет помещен в запрошенный буфер.</span><span class="sxs-lookup"><span data-stu-id="9b550-119">Applications should not assume that the text will always be placed in the requested buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b550-120">Требования</span><span class="sxs-lookup"><span data-stu-id="9b550-120">Requirements</span></span>



| <span data-ttu-id="9b550-121">Требование</span><span class="sxs-lookup"><span data-stu-id="9b550-121">Requirement</span></span> | <span data-ttu-id="9b550-122">Значение</span><span class="sxs-lookup"><span data-stu-id="9b550-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9b550-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9b550-123">Minimum supported client</span></span><br/> | <span data-ttu-id="9b550-124">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9b550-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9b550-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9b550-125">Minimum supported server</span></span><br/> | <span data-ttu-id="9b550-126">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9b550-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9b550-127">Header</span><span class="sxs-lookup"><span data-stu-id="9b550-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="9b550-128"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="9b550-128"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="9b550-129">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="9b550-129">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="9b550-130">**Кбем \_ ЖЕТИТЕМВ** (Юникод) и **КБЕМ- \_ элемент** a (ANSI)</span><span class="sxs-lookup"><span data-stu-id="9b550-130">**CBEM\_GETITEMW** (Unicode) and **CBEM\_GETITEMA** (ANSI)</span></span><br/>                 |



 

 





