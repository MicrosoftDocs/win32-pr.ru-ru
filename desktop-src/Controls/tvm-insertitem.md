---
title: Сообщение TVM_INSERTITEM (Коммктрл. h)
description: Вставляет новый элемент в элемент управления представлением в виде дерева. Это сообщение можно отправить явно или с помощью \_ макроса InsertItem TreeView.
ms.assetid: c5e5f88f-6ec8-4b95-89ea-97f6f1fd735e
keywords:
- Элементы управления Windows для TVM_INSERTITEM сообщений
topic_type:
- apiref
api_name:
- TVM_INSERTITEM
- TVM_INSERTITEMA
- TVM_INSERTITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 719de4c2391ff924c9f6deb8cb4206cfdb56c3ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891641"
---
# <a name="tvm_insertitem-message"></a><span data-ttu-id="057d3-105">\_Сообщение TVM INSERTITEM</span><span class="sxs-lookup"><span data-stu-id="057d3-105">TVM\_INSERTITEM message</span></span>

<span data-ttu-id="057d3-106">Вставляет новый элемент в элемент управления представлением в виде дерева.</span><span class="sxs-lookup"><span data-stu-id="057d3-106">Inserts a new item in a tree-view control.</span></span> <span data-ttu-id="057d3-107">Это сообщение можно отправить явно или с помощью макроса [**\_ InsertItem TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_insertitem) .</span><span class="sxs-lookup"><span data-stu-id="057d3-107">You can send this message explicitly or by using the [**TreeView\_InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_insertitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="057d3-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="057d3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="057d3-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="057d3-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="057d3-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="057d3-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="057d3-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="057d3-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="057d3-112">Указатель на структуру [**твинсертструкт**](/windows/win32/api/commctrl/ns-commctrl-tvinsertstructa) , указывающую атрибуты элемента представления дерева.</span><span class="sxs-lookup"><span data-stu-id="057d3-112">Pointer to a [**TVINSERTSTRUCT**](/windows/win32/api/commctrl/ns-commctrl-tvinsertstructa) structure that specifies the attributes of the tree-view item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="057d3-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="057d3-113">Return value</span></span>

<span data-ttu-id="057d3-114">Возвращает маркер **хтриитем** для нового элемента, если он успешно, или **значение NULL** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="057d3-114">Returns the **HTREEITEM** handle to the new item if successful, or **NULL** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="057d3-115">Требования</span><span class="sxs-lookup"><span data-stu-id="057d3-115">Requirements</span></span>



| <span data-ttu-id="057d3-116">Требование</span><span class="sxs-lookup"><span data-stu-id="057d3-116">Requirement</span></span> | <span data-ttu-id="057d3-117">Значение</span><span class="sxs-lookup"><span data-stu-id="057d3-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="057d3-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="057d3-118">Minimum supported client</span></span><br/> | <span data-ttu-id="057d3-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="057d3-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="057d3-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="057d3-120">Minimum supported server</span></span><br/> | <span data-ttu-id="057d3-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="057d3-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="057d3-122">Header</span><span class="sxs-lookup"><span data-stu-id="057d3-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="057d3-123"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="057d3-123"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="057d3-124">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="057d3-124">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="057d3-125">**TVM \_ ИНСЕРТИТЕМВ** (Юникод) и **TVM \_ инсертитема** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="057d3-125">**TVM\_INSERTITEMW** (Unicode) and **TVM\_INSERTITEMA** (ANSI)</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="057d3-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="057d3-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="057d3-127">ТВН \_ ендлабеледит</span><span class="sxs-lookup"><span data-stu-id="057d3-127">TVN\_ENDLABELEDIT</span></span>](tvn-endlabeledit.md)
</dt> </dl>

 

 





