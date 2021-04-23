---
title: Сообщение LVM_DELETECOLUMN (Коммктрл. h)
description: Удаляет столбец из элемента управления "представление списка". Это сообщение можно отправить явно или с помощью \_ макроса Делетеколумн ListView.
ms.assetid: 1748a70b-9a13-4753-ac23-55b5652164c2
keywords:
- Элементы управления Windows для LVM_DELETECOLUMN сообщений
topic_type:
- apiref
api_name:
- LVM_DELETECOLUMN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: daa9005009ceaf42a01ede4f0f26334ae686c2df
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801127"
---
# <a name="lvm_deletecolumn-message"></a><span data-ttu-id="d20b7-105">\_Сообщение LVM делетеколумн</span><span class="sxs-lookup"><span data-stu-id="d20b7-105">LVM\_DELETECOLUMN message</span></span>

<span data-ttu-id="d20b7-106">Удаляет столбец из элемента управления "представление списка".</span><span class="sxs-lookup"><span data-stu-id="d20b7-106">Removes a column from a list-view control.</span></span> <span data-ttu-id="d20b7-107">Это сообщение можно отправить явно или с помощью макроса [**\_ делетеколумн ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_deletecolumn) .</span><span class="sxs-lookup"><span data-stu-id="d20b7-107">You can send this message explicitly or by using the [**ListView\_DeleteColumn**](/windows/desktop/api/Commctrl/nf-commctrl-listview_deletecolumn) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="d20b7-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="d20b7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d20b7-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d20b7-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d20b7-110">Индекс столбца, который необходимо удалить.</span><span class="sxs-lookup"><span data-stu-id="d20b7-110">The index of the column to delete.</span></span>

</dd> <dt>

<span data-ttu-id="d20b7-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d20b7-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="d20b7-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="d20b7-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d20b7-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d20b7-113">Return value</span></span>

<span data-ttu-id="d20b7-114">Возвращает **значение true** , если успешно, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="d20b7-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="d20b7-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d20b7-115">Remarks</span></span>

<span data-ttu-id="d20b7-116">Удаление нулевого столбца элемента управления "представление списка" поддерживается только в ComCtl32.dll версии 6 и более поздних.</span><span class="sxs-lookup"><span data-stu-id="d20b7-116">Deleting column zero of a list-view control is supported only in ComCtl32.dll version 6 and later.</span></span> <span data-ttu-id="d20b7-117">Версия 5 также поддерживает удаление нулевого столбца, но только после использования [**CCM \_ сетверсион**](ccm-setversion.md) для установки версии 5 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="d20b7-117">Version 5 also supports deleting column zero, but only after you use [**CCM\_SETVERSION**](ccm-setversion.md) to set the version to 5 or later.</span></span> <span data-ttu-id="d20b7-118">В версиях до версии 5, если необходимо удалить нулевой столбец, вставьте пустой столбец пустого типа нулевой длины и удалите столбец один и более.</span><span class="sxs-lookup"><span data-stu-id="d20b7-118">In versions prior to version 5, if you must delete column zero, insert a zero length dummy column zero and delete column one and above.</span></span>

## <a name="requirements"></a><span data-ttu-id="d20b7-119">Требования</span><span class="sxs-lookup"><span data-stu-id="d20b7-119">Requirements</span></span>



| <span data-ttu-id="d20b7-120">Требование</span><span class="sxs-lookup"><span data-stu-id="d20b7-120">Requirement</span></span> | <span data-ttu-id="d20b7-121">Значение</span><span class="sxs-lookup"><span data-stu-id="d20b7-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d20b7-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d20b7-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d20b7-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d20b7-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d20b7-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d20b7-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d20b7-125">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d20b7-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d20b7-126">Header</span><span class="sxs-lookup"><span data-stu-id="d20b7-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="d20b7-127"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="d20b7-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





