---
title: Сообщение LVM_INSERTCOLUMN (Коммктрл. h)
description: Вставляет новый столбец в элемент управления "представление списка". Это сообщение можно отправить явно или с помощью \_ макроса Инсертколумн ListView.
ms.assetid: 1326e38e-bb45-4d0d-b5bc-ec684b3b92ef
keywords:
- Элементы управления Windows для LVM_INSERTCOLUMN сообщений
topic_type:
- apiref
api_name:
- LVM_INSERTCOLUMN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8be89ff0b4ef417a715085582544112cb90cb6b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535033"
---
# <a name="lvm_insertcolumn-message"></a><span data-ttu-id="e3f93-105">\_Сообщение LVM инсертколумн</span><span class="sxs-lookup"><span data-stu-id="e3f93-105">LVM\_INSERTCOLUMN message</span></span>

<span data-ttu-id="e3f93-106">Вставляет новый столбец в элемент управления "представление списка".</span><span class="sxs-lookup"><span data-stu-id="e3f93-106">Inserts a new column in a list-view control.</span></span> <span data-ttu-id="e3f93-107">Это сообщение можно отправить явно или с помощью макроса [**\_ инсертколумн ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertcolumn) .</span><span class="sxs-lookup"><span data-stu-id="e3f93-107">You can send this message explicitly or by using the [**ListView\_InsertColumn**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertcolumn) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="e3f93-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="e3f93-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3f93-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e3f93-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e3f93-110">Индекс нового столбца.</span><span class="sxs-lookup"><span data-stu-id="e3f93-110">Index of the new column.</span></span>

</dd> <dt>

<span data-ttu-id="e3f93-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e3f93-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e3f93-112">Указатель на структуру [**LVCOLUMN**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) , содержащую атрибуты нового столбца.</span><span class="sxs-lookup"><span data-stu-id="e3f93-112">Pointer to an [**LVCOLUMN**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) structure that contains the attributes of the new column.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3f93-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e3f93-113">Return value</span></span>

<span data-ttu-id="e3f93-114">Возвращает индекс нового столбца, если он выполнен успешно, или значение-1 в противном случае.</span><span class="sxs-lookup"><span data-stu-id="e3f93-114">Returns the index of the new column if successful, or -1 otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="e3f93-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e3f93-115">Remarks</span></span>

<span data-ttu-id="e3f93-116">Столбцы видимы только в представлении отчета (Details).</span><span class="sxs-lookup"><span data-stu-id="e3f93-116">Columns are visible only in report (details) view.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3f93-117">Требования</span><span class="sxs-lookup"><span data-stu-id="e3f93-117">Requirements</span></span>



| <span data-ttu-id="e3f93-118">Требование</span><span class="sxs-lookup"><span data-stu-id="e3f93-118">Requirement</span></span> | <span data-ttu-id="e3f93-119">Значение</span><span class="sxs-lookup"><span data-stu-id="e3f93-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e3f93-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e3f93-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e3f93-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e3f93-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e3f93-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e3f93-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e3f93-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e3f93-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e3f93-124">Header</span><span class="sxs-lookup"><span data-stu-id="e3f93-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="e3f93-125"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="e3f93-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





