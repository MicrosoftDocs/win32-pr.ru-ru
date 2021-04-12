---
title: Сообщение HDM_GETITEM (Коммктрл. h)
description: Возвращает сведения об элементе в элементе управления "заголовок". Вы можете явно отправить это сообщение или использовать макрос Header \_ .
ms.assetid: fb1330d3-fd28-490c-9caa-4b2b5ff86ba0
keywords:
- Элементы управления Windows для HDM_GETITEM сообщений
topic_type:
- apiref
api_name:
- HDM_GETITEM
- HDM_GETITEMA
- HDM_GETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2073602121480930e0f7d9d2e5a904c0dea77ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135963"
---
# <a name="hdm_getitem-message"></a><span data-ttu-id="4dc87-105">Сообщение о выходе \_ элемента HDM</span><span class="sxs-lookup"><span data-stu-id="4dc87-105">HDM\_GETITEM message</span></span>

<span data-ttu-id="4dc87-106">Возвращает сведения об элементе в элементе управления "заголовок".</span><span class="sxs-lookup"><span data-stu-id="4dc87-106">Gets information about an item in a header control.</span></span> <span data-ttu-id="4dc87-107">Вы можете явно отправить это сообщение или использовать макрос [**Header \_**](/windows/desktop/api/Commctrl/nf-commctrl-header_getitem) .</span><span class="sxs-lookup"><span data-stu-id="4dc87-107">You can send this message explicitly or use the [**Header\_GetItem**](/windows/desktop/api/Commctrl/nf-commctrl-header_getitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="4dc87-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="4dc87-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4dc87-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4dc87-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4dc87-110">Индекс элемента, для которого извлекаются сведения.</span><span class="sxs-lookup"><span data-stu-id="4dc87-110">The index of the item for which information is to be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="4dc87-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4dc87-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4dc87-112">Указатель на структуру [**хдитем**](/windows/win32/api/commctrl/ns-commctrl-hditema) .</span><span class="sxs-lookup"><span data-stu-id="4dc87-112">A pointer to an [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) structure.</span></span> <span data-ttu-id="4dc87-113">При отправке сообщения элемент **Mask** указывает тип запрашиваемой информации.</span><span class="sxs-lookup"><span data-stu-id="4dc87-113">When the message is sent, the **mask** member indicates the type of information being requested.</span></span> <span data-ttu-id="4dc87-114">Когда сообщение возвращается, другие члены получают запрошенные сведения.</span><span class="sxs-lookup"><span data-stu-id="4dc87-114">When the message returns, the other members receive the requested information.</span></span> <span data-ttu-id="4dc87-115">Если элемент **маски** задает ноль, сообщение возвращает **значение true** , но не копирует сведения в структуру.</span><span class="sxs-lookup"><span data-stu-id="4dc87-115">If the **mask** member specifies zero, the message returns **TRUE** but copies no information to the structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4dc87-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4dc87-116">Return value</span></span>

<span data-ttu-id="4dc87-117">Возвращает **значение true** , если успешно, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="4dc87-117">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="4dc87-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4dc87-118">Remarks</span></span>

<span data-ttu-id="4dc87-119">Если в элементе \_ **Mask** структуры [**хдитем**](/windows/win32/api/commctrl/ns-commctrl-hditema) задан флаг HDi Text, элемент управления может изменить элемент **псзтекст** структуры так, чтобы он указывал на новый текст вместо заполнения буфера запрошенным текстом.</span><span class="sxs-lookup"><span data-stu-id="4dc87-119">If the HDI\_TEXT flag is set in the **mask** member of the [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) structure, the control may change the **pszText** member of the structure to point to the new text instead of filling the buffer with the requested text.</span></span> <span data-ttu-id="4dc87-120">Приложения не должны рассчитывать, что текст всегда будет помещен в запрошенный буфер.</span><span class="sxs-lookup"><span data-stu-id="4dc87-120">Applications should not assume that the text will always be placed in the requested buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="4dc87-121">Требования</span><span class="sxs-lookup"><span data-stu-id="4dc87-121">Requirements</span></span>



| <span data-ttu-id="4dc87-122">Требование</span><span class="sxs-lookup"><span data-stu-id="4dc87-122">Requirement</span></span> | <span data-ttu-id="4dc87-123">Значение</span><span class="sxs-lookup"><span data-stu-id="4dc87-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4dc87-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4dc87-124">Minimum supported client</span></span><br/> | <span data-ttu-id="4dc87-125">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4dc87-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4dc87-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4dc87-126">Minimum supported server</span></span><br/> | <span data-ttu-id="4dc87-127">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4dc87-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4dc87-128">Header</span><span class="sxs-lookup"><span data-stu-id="4dc87-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="4dc87-129"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="4dc87-129"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="4dc87-130">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="4dc87-130">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="4dc87-131">**Разъем HDM \_ ЖЕТИТЕМВ** (Юникод) и **HDM- \_ элемент** a (ANSI)</span><span class="sxs-lookup"><span data-stu-id="4dc87-131">**HDM\_GETITEMW** (Unicode) and **HDM\_GETITEMA** (ANSI)</span></span><br/>                   |



 

 





