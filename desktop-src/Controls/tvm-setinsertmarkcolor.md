---
title: Сообщение TVM_SETINSERTMARKCOLOR (Коммктрл. h)
description: Задает цвет, используемый для отображения метки вставки для представления в виде дерева. Это сообщение можно отправить явно или с помощью \_ макроса Сетинсертмаркколор TreeView.
ms.assetid: c82304a8-3726-42c0-81e7-90d8f8205ead
keywords:
- Элементы управления Windows для TVM_SETINSERTMARKCOLOR сообщений
topic_type:
- apiref
api_name:
- TVM_SETINSERTMARKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92668b1137b089f9a09cc9a34d63d472742bce4d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136230"
---
# <a name="tvm_setinsertmarkcolor-message"></a><span data-ttu-id="78602-105">\_Сообщение TVM сетинсертмаркколор</span><span class="sxs-lookup"><span data-stu-id="78602-105">TVM\_SETINSERTMARKCOLOR message</span></span>

<span data-ttu-id="78602-106">Задает цвет, используемый для отображения метки вставки для представления в виде дерева.</span><span class="sxs-lookup"><span data-stu-id="78602-106">Sets the color used to draw the insertion mark for the tree view.</span></span> <span data-ttu-id="78602-107">Это сообщение можно отправить явно или с помощью макроса [**\_ сетинсертмаркколор TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setinsertmarkcolor) .</span><span class="sxs-lookup"><span data-stu-id="78602-107">You can send this message explicitly or by using the [**TreeView\_SetInsertMarkColor**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setinsertmarkcolor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="78602-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="78602-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78602-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="78602-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="78602-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="78602-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="78602-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="78602-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="78602-112">Значение [**COLORREF**](/windows/desktop/gdi/colorref) , содержащее новый цвет метки вставки.</span><span class="sxs-lookup"><span data-stu-id="78602-112">[**COLORREF**](/windows/desktop/gdi/colorref) value that contains the new insertion mark color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78602-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="78602-113">Return value</span></span>

<span data-ttu-id="78602-114">Возвращает значение **COLORREF** , содержащее предыдущий цвет отметки вставки.</span><span class="sxs-lookup"><span data-stu-id="78602-114">Returns a **COLORREF** value that contains the previous insertion mark color.</span></span>

## <a name="requirements"></a><span data-ttu-id="78602-115">Требования</span><span class="sxs-lookup"><span data-stu-id="78602-115">Requirements</span></span>



| <span data-ttu-id="78602-116">Требование</span><span class="sxs-lookup"><span data-stu-id="78602-116">Requirement</span></span> | <span data-ttu-id="78602-117">Значение</span><span class="sxs-lookup"><span data-stu-id="78602-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="78602-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="78602-118">Minimum supported client</span></span><br/> | <span data-ttu-id="78602-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="78602-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="78602-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="78602-120">Minimum supported server</span></span><br/> | <span data-ttu-id="78602-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="78602-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="78602-122">Header</span><span class="sxs-lookup"><span data-stu-id="78602-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="78602-123"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="78602-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78602-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="78602-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78602-125">**TVM \_ жетинсертмаркколор**</span><span class="sxs-lookup"><span data-stu-id="78602-125">**TVM\_GETINSERTMARKCOLOR**</span></span>](tvm-getinsertmarkcolor.md)
</dt> </dl>

 

