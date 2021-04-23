---
title: Сообщение TCM_SETITEM (Коммктрл. h)
description: Задает некоторые или все атрибуты вкладки. Это сообщение можно отправить явным образом или с помощью \_ макроса табктрл сетитем.
ms.assetid: 1d9c6607-d8ec-4644-a714-22bc2677aa78
keywords:
- Элементы управления Windows для TCM_SETITEM сообщений
topic_type:
- apiref
api_name:
- TCM_SETITEM
- TCM_SETITEMA
- TCM_SETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee86cd0737c3c50c89a97d3881e2cdfd3850f481
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801066"
---
# <a name="tcm_setitem-message"></a><span data-ttu-id="ec34f-105">\_Сообщение СЕТИТЕМ TCM</span><span class="sxs-lookup"><span data-stu-id="ec34f-105">TCM\_SETITEM message</span></span>

<span data-ttu-id="ec34f-106">Задает некоторые или все атрибуты вкладки.</span><span class="sxs-lookup"><span data-stu-id="ec34f-106">Sets some or all of a tab's attributes.</span></span> <span data-ttu-id="ec34f-107">Это сообщение можно отправить явным образом или с помощью макроса [**табктрл \_ сетитем**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setitem) .</span><span class="sxs-lookup"><span data-stu-id="ec34f-107">You can send this message explicitly or by using the [**TabCtrl\_SetItem**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="ec34f-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="ec34f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec34f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ec34f-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ec34f-110">Индекс элемента.</span><span class="sxs-lookup"><span data-stu-id="ec34f-110">Index of the item.</span></span>

</dd> <dt>

<span data-ttu-id="ec34f-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ec34f-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ec34f-112">Указатель на структуру [**тЦитем**](/windows/win32/api/commctrl/ns-commctrl-tcitema) , содержащую новые атрибуты элемента.</span><span class="sxs-lookup"><span data-stu-id="ec34f-112">Pointer to a [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) structure that contains the new item attributes.</span></span> <span data-ttu-id="ec34f-113">Элемент **маски** указывает, какие атрибуты задаются.</span><span class="sxs-lookup"><span data-stu-id="ec34f-113">The **mask** member specifies which attributes to set.</span></span> <span data-ttu-id="ec34f-114">Если элемент **Mask** задает \_ текстовое значение тЦиф, то элемент **псзтекст** является адресом строки, завершающейся нулем, а элемент **кчтекстмакс** игнорируется.</span><span class="sxs-lookup"><span data-stu-id="ec34f-114">If the **mask** member specifies the TCIF\_TEXT value, the **pszText** member is the address of a null-terminated string and the **cchTextMax** member is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec34f-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ec34f-115">Return value</span></span>

<span data-ttu-id="ec34f-116">Возвращает **значение true** , если успешно, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="ec34f-116">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec34f-117">Требования</span><span class="sxs-lookup"><span data-stu-id="ec34f-117">Requirements</span></span>



| <span data-ttu-id="ec34f-118">Требование</span><span class="sxs-lookup"><span data-stu-id="ec34f-118">Requirement</span></span> | <span data-ttu-id="ec34f-119">Значение</span><span class="sxs-lookup"><span data-stu-id="ec34f-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ec34f-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ec34f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ec34f-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ec34f-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ec34f-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ec34f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ec34f-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ec34f-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ec34f-124">Header</span><span class="sxs-lookup"><span data-stu-id="ec34f-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="ec34f-125"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="ec34f-125"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="ec34f-126">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="ec34f-126">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="ec34f-127">**TCM \_ СЕТИТЕМВ** (Юникод) и **TCM \_ сетитема** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="ec34f-127">**TCM\_SETITEMW** (Unicode) and **TCM\_SETITEMA** (ANSI)</span></span><br/>                   |



 

 





