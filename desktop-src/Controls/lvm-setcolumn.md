---
title: Сообщение LVM_SETCOLUMN (Коммктрл. h)
description: Задает атрибуты столбца представления списка. Это сообщение можно отправить явно или с помощью \_ макроса Сетколумн ListView.
ms.assetid: 8ca1c269-fd86-4561-940d-b75f8ca2b731
keywords:
- Элементы управления Windows для LVM_SETCOLUMN сообщений
topic_type:
- apiref
api_name:
- LVM_SETCOLUMN
- LVM_SETCOLUMNW
- LVM_SETCOLUMNW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7251da70c7ac1e2cb7bbcf7b3e220a2f6cdf055f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988691"
---
# <a name="lvm_setcolumn-message"></a><span data-ttu-id="3ad14-105">\_Сообщение LVM сетколумн</span><span class="sxs-lookup"><span data-stu-id="3ad14-105">LVM\_SETCOLUMN message</span></span>

<span data-ttu-id="3ad14-106">Задает атрибуты столбца представления списка.</span><span class="sxs-lookup"><span data-stu-id="3ad14-106">Sets the attributes of a list-view column.</span></span> <span data-ttu-id="3ad14-107">Это сообщение можно отправить явно или с помощью макроса [**\_ сетколумн ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setcolumn) .</span><span class="sxs-lookup"><span data-stu-id="3ad14-107">You can send this message explicitly or by using the [**ListView\_SetColumn**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setcolumn) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="3ad14-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="3ad14-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ad14-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3ad14-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3ad14-110">Индекс столбца.</span><span class="sxs-lookup"><span data-stu-id="3ad14-110">Index of the column.</span></span>

</dd> <dt>

<span data-ttu-id="3ad14-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3ad14-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3ad14-112">Указатель на структуру [**LVCOLUMN**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) , содержащую атрибуты нового столбца.</span><span class="sxs-lookup"><span data-stu-id="3ad14-112">Pointer to an [**LVCOLUMN**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) structure that contains the new column attributes.</span></span> <span data-ttu-id="3ad14-113">Элемент **маски** указывает, какие атрибуты столбца задаются.</span><span class="sxs-lookup"><span data-stu-id="3ad14-113">The **mask** member specifies which column attributes to set.</span></span> <span data-ttu-id="3ad14-114">Если элемент **Mask** задает \_ текстовое значение лвкф, то элемент **псзтекст** является адресом строки, завершающейся нулем, а элемент **кчтекстмакс** игнорируется.</span><span class="sxs-lookup"><span data-stu-id="3ad14-114">If the **mask** member specifies the LVCF\_TEXT value, the **pszText** member is the address of a null-terminated string and the **cchTextMax** member is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ad14-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3ad14-115">Return value</span></span>

<span data-ttu-id="3ad14-116">Возвращает **значение true** , если успешно, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="3ad14-116">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ad14-117">Требования</span><span class="sxs-lookup"><span data-stu-id="3ad14-117">Requirements</span></span>



| <span data-ttu-id="3ad14-118">Требование</span><span class="sxs-lookup"><span data-stu-id="3ad14-118">Requirement</span></span> | <span data-ttu-id="3ad14-119">Значение</span><span class="sxs-lookup"><span data-stu-id="3ad14-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3ad14-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3ad14-120">Minimum supported client</span></span><br/> | <span data-ttu-id="3ad14-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3ad14-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3ad14-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3ad14-122">Minimum supported server</span></span><br/> | <span data-ttu-id="3ad14-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3ad14-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3ad14-124">Header</span><span class="sxs-lookup"><span data-stu-id="3ad14-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="3ad14-125"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="3ad14-125"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="3ad14-126">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="3ad14-126">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="3ad14-127">**LVM \_ СЕТКОЛУМНВ** (Юникод) и **LVM \_ сетколумнв** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="3ad14-127">**LVM\_SETCOLUMNW** (Unicode) and **LVM\_SETCOLUMNW** (ANSI)</span></span><br/>               |



 

 





