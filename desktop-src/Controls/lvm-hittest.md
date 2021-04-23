---
title: Сообщение LVM_HITTEST (Коммктрл. h)
description: Определяет, какой элемент списка (если имеется) находится в указанной позиции. Это сообщение можно отправить явно или с помощью \_ макроса HitTest ListView.
ms.assetid: 81df4ed1-30bd-4b63-9cb9-5163cb7cf52c
keywords:
- Элементы управления Windows для LVM_HITTEST сообщений
topic_type:
- apiref
api_name:
- LVM_HITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4fb770c8f5a47f1dcbbf23a11443afa581aea2e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989170"
---
# <a name="lvm_hittest-message"></a><span data-ttu-id="24219-105">\_Сообщение LVM HITTEST</span><span class="sxs-lookup"><span data-stu-id="24219-105">LVM\_HITTEST message</span></span>

<span data-ttu-id="24219-106">Определяет, какой элемент списка (если имеется) находится в указанной позиции.</span><span class="sxs-lookup"><span data-stu-id="24219-106">Determines which list-view item, if any, is at a specified position.</span></span> <span data-ttu-id="24219-107">Это сообщение можно отправить явно или с помощью макроса [**\_ HitTest ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_hittest) .</span><span class="sxs-lookup"><span data-stu-id="24219-107">You can send this message explicitly or by using the [**ListView\_HitTest**](/windows/desktop/api/Commctrl/nf-commctrl-listview_hittest) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="24219-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="24219-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24219-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="24219-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="24219-110">Должно быть равно 0.</span><span class="sxs-lookup"><span data-stu-id="24219-110">Must be 0.</span></span> <span data-ttu-id="24219-111">**Windows Vista.**</span><span class="sxs-lookup"><span data-stu-id="24219-111">**Windows Vista.**</span></span> <span data-ttu-id="24219-112">Должен быть равен-1, если необходимо извлечь элементы **играуп** и **iSubItem** структуры *lParam* .</span><span class="sxs-lookup"><span data-stu-id="24219-112">Should be -1 if the **iGroup** and **iSubItem** members of the *lParam* structure are to be retrieved.</span></span></dd> <dt>

<span data-ttu-id="24219-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="24219-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="24219-114">Указатель на структуру [**лвхиттестинфо**](/windows/win32/api/commctrl/ns-commctrl-lvhittestinfo) , которая содержит позиции для проверки попадания и получает сведения о результатах проверки попадания.</span><span class="sxs-lookup"><span data-stu-id="24219-114">Pointer to an [**LVHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-lvhittestinfo) structure that contains the position to hit test and receives information about the results of the hit test.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24219-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="24219-115">Return value</span></span>

<span data-ttu-id="24219-116">Возвращает индекс элемента в указанной позиции, если таковой имеется, или значение-1 в противном случае.</span><span class="sxs-lookup"><span data-stu-id="24219-116">Returns the index of the item at the specified position, if any, or -1 otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="24219-117">Требования</span><span class="sxs-lookup"><span data-stu-id="24219-117">Requirements</span></span>



| <span data-ttu-id="24219-118">Требование</span><span class="sxs-lookup"><span data-stu-id="24219-118">Requirement</span></span> | <span data-ttu-id="24219-119">Значение</span><span class="sxs-lookup"><span data-stu-id="24219-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="24219-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="24219-120">Minimum supported client</span></span><br/> | <span data-ttu-id="24219-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="24219-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="24219-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="24219-122">Minimum supported server</span></span><br/> | <span data-ttu-id="24219-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="24219-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="24219-124">Header</span><span class="sxs-lookup"><span data-stu-id="24219-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="24219-125"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="24219-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





