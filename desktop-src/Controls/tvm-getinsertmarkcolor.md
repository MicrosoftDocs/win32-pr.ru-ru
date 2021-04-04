---
title: Сообщение TVM_GETINSERTMARKCOLOR (Коммктрл. h)
description: Извлекает цвет, используемый для рисования метки вставки в представлении в виде дерева. Это сообщение можно отправить явно или с помощью \_ макроса Жетинсертмаркколор TreeView.
ms.assetid: d1fba4bb-1bdb-44e0-8083-b564cdafc055
keywords:
- Элементы управления Windows для TVM_GETINSERTMARKCOLOR сообщений
topic_type:
- apiref
api_name:
- TVM_GETINSERTMARKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61416a428fed88ece8f50ca640dd9a05ec131614
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989282"
---
# <a name="tvm_getinsertmarkcolor-message"></a><span data-ttu-id="51725-105">\_Сообщение TVM жетинсертмаркколор</span><span class="sxs-lookup"><span data-stu-id="51725-105">TVM\_GETINSERTMARKCOLOR message</span></span>

<span data-ttu-id="51725-106">Извлекает цвет, используемый для рисования метки вставки в представлении в виде дерева.</span><span class="sxs-lookup"><span data-stu-id="51725-106">Retrieves the color used to draw the insertion mark for the tree view.</span></span> <span data-ttu-id="51725-107">Это сообщение можно отправить явно или с помощью макроса [**\_ жетинсертмаркколор TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getinsertmarkcolor) .</span><span class="sxs-lookup"><span data-stu-id="51725-107">You can send this message explicitly or by using the [**TreeView\_GetInsertMarkColor**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getinsertmarkcolor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="51725-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="51725-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51725-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="51725-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="51725-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="51725-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="51725-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="51725-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="51725-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="51725-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="51725-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="51725-113">Return value</span></span>

<span data-ttu-id="51725-114">Возвращает значение [**COLORREF**](/windows/desktop/gdi/colorref) , содержащее текущий цвет отметки вставки.</span><span class="sxs-lookup"><span data-stu-id="51725-114">Returns a [**COLORREF**](/windows/desktop/gdi/colorref) value that contains the current insertion mark color.</span></span>

## <a name="requirements"></a><span data-ttu-id="51725-115">Требования</span><span class="sxs-lookup"><span data-stu-id="51725-115">Requirements</span></span>



| <span data-ttu-id="51725-116">Требование</span><span class="sxs-lookup"><span data-stu-id="51725-116">Requirement</span></span> | <span data-ttu-id="51725-117">Значение</span><span class="sxs-lookup"><span data-stu-id="51725-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="51725-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="51725-118">Minimum supported client</span></span><br/> | <span data-ttu-id="51725-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="51725-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="51725-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="51725-120">Minimum supported server</span></span><br/> | <span data-ttu-id="51725-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="51725-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="51725-122">Header</span><span class="sxs-lookup"><span data-stu-id="51725-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="51725-123"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="51725-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51725-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="51725-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51725-125">**TVM \_ сетинсертмаркколор**</span><span class="sxs-lookup"><span data-stu-id="51725-125">**TVM\_SETINSERTMARKCOLOR**</span></span>](tvm-setinsertmarkcolor.md)
</dt> </dl>

 

