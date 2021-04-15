---
title: Сообщение LVM_FINDITEM (Коммктрл. h)
description: Выполняет поиск элемента представления списка с указанными характеристиками. Это сообщение можно отправить явно или с помощью \_ макроса FindItem в ListView.
ms.assetid: 3b18c8ad-97e6-4f4d-bf89-afb95f925ed1
keywords:
- Элементы управления Windows для LVM_FINDITEM сообщений
topic_type:
- apiref
api_name:
- LVM_FINDITEM
- LVM_FINDITEMA
- LVM_FINDITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1f7dfc19e263a6ab7ad29b5e514fa4e52c1a9ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489078"
---
# <a name="lvm_finditem-message"></a><span data-ttu-id="04f2a-105">\_Сообщение LVM FINDITEM</span><span class="sxs-lookup"><span data-stu-id="04f2a-105">LVM\_FINDITEM message</span></span>

<span data-ttu-id="04f2a-106">Выполняет поиск элемента представления списка с указанными характеристиками.</span><span class="sxs-lookup"><span data-stu-id="04f2a-106">Searches for a list-view item with the specified characteristics.</span></span> <span data-ttu-id="04f2a-107">Это сообщение можно отправить явно или с помощью макроса [**\_ FindItem в ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_finditem) .</span><span class="sxs-lookup"><span data-stu-id="04f2a-107">You can send this message explicitly or by using the [**ListView\_FindItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_finditem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="04f2a-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="04f2a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04f2a-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="04f2a-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="04f2a-110">Индекс элемента, с которого начинается поиск, или-1, чтобы начать с начала.</span><span class="sxs-lookup"><span data-stu-id="04f2a-110">The index of the item to begin the search with or -1 to start from the beginning.</span></span> <span data-ttu-id="04f2a-111">Сам указанный элемент исключен из поиска.</span><span class="sxs-lookup"><span data-stu-id="04f2a-111">The specified item is itself excluded from the search.</span></span>

</dd> <dt>

<span data-ttu-id="04f2a-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="04f2a-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="04f2a-113">Указатель на структуру [**лвфиндинфо**](/windows/win32/api/commctrl/ns-commctrl-lvfindinfoa) , содержащую сведения о том, что искать.</span><span class="sxs-lookup"><span data-stu-id="04f2a-113">A pointer to an [**LVFINDINFO**](/windows/win32/api/commctrl/ns-commctrl-lvfindinfoa) structure that contains information about what to search for.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04f2a-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="04f2a-114">Return value</span></span>

<span data-ttu-id="04f2a-115">Возвращает индекс элемента, если он успешно, или значение-1 в противном случае.</span><span class="sxs-lookup"><span data-stu-id="04f2a-115">Returns the index of the item if successful, or -1 otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="04f2a-116">Требования</span><span class="sxs-lookup"><span data-stu-id="04f2a-116">Requirements</span></span>



| <span data-ttu-id="04f2a-117">Требование</span><span class="sxs-lookup"><span data-stu-id="04f2a-117">Requirement</span></span> | <span data-ttu-id="04f2a-118">Значение</span><span class="sxs-lookup"><span data-stu-id="04f2a-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="04f2a-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="04f2a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="04f2a-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="04f2a-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="04f2a-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="04f2a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="04f2a-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="04f2a-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="04f2a-123">Header</span><span class="sxs-lookup"><span data-stu-id="04f2a-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="04f2a-124"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="04f2a-124"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="04f2a-125">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="04f2a-125">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="04f2a-126">**LVM \_ ФИНДИТЕМВ** (Юникод) и **LVM \_ финдитема** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="04f2a-126">**LVM\_FINDITEMW** (Unicode) and **LVM\_FINDITEMA** (ANSI)</span></span><br/>                 |



 

 





