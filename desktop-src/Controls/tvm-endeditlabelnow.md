---
title: Сообщение TVM_ENDEDITLABELNOW (Коммктрл. h)
description: Завершает редактирование метки элемента древовидного представления. Это сообщение можно отправить явно или с помощью \_ макроса Ендедитлабелнов TreeView.
ms.assetid: 68de2020-9311-4958-859a-de55f5e41fcf
keywords:
- Элементы управления Windows для TVM_ENDEDITLABELNOW сообщений
topic_type:
- apiref
api_name:
- TVM_ENDEDITLABELNOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f059be20560adeb8cbcb0c63a2555283f6b7051
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104533974"
---
# <a name="tvm_endeditlabelnow-message"></a><span data-ttu-id="b70e3-105">\_Сообщение TVM ендедитлабелнов</span><span class="sxs-lookup"><span data-stu-id="b70e3-105">TVM\_ENDEDITLABELNOW message</span></span>

<span data-ttu-id="b70e3-106">Завершает редактирование метки элемента древовидного представления.</span><span class="sxs-lookup"><span data-stu-id="b70e3-106">Ends the editing of a tree-view item's label.</span></span> <span data-ttu-id="b70e3-107">Это сообщение можно отправить явно или с помощью макроса [**\_ ендедитлабелнов TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_endeditlabelnow) .</span><span class="sxs-lookup"><span data-stu-id="b70e3-107">You can send this message explicitly or by using the [**TreeView\_EndEditLabelNow**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_endeditlabelnow) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="b70e3-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="b70e3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b70e3-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b70e3-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b70e3-110">Переменная, которая указывает, отменяется ли редактирование без сохранения в метке.</span><span class="sxs-lookup"><span data-stu-id="b70e3-110">Variable that indicates whether the editing is canceled without being saved to the label.</span></span> <span data-ttu-id="b70e3-111">Если этот параметр имеет **значение true**, система отменяет редактирование без сохранения изменений.</span><span class="sxs-lookup"><span data-stu-id="b70e3-111">If this parameter is **TRUE**, the system cancels editing without saving the changes.</span></span> <span data-ttu-id="b70e3-112">В противном случае система сохранит изменения в метке.</span><span class="sxs-lookup"><span data-stu-id="b70e3-112">Otherwise, the system saves the changes to the label.</span></span>

</dd> <dt>

<span data-ttu-id="b70e3-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b70e3-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="b70e3-114">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="b70e3-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b70e3-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b70e3-115">Return value</span></span>

<span data-ttu-id="b70e3-116">Возвращает **значение true** , если успешно, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="b70e3-116">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="b70e3-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b70e3-117">Remarks</span></span>

<span data-ttu-id="b70e3-118">Это сообщение вызывает отправку кода уведомления [ТВН \_ ендлабеледит](tvn-endlabeledit.md) в родительское окно элемента управления "дерево-представление".</span><span class="sxs-lookup"><span data-stu-id="b70e3-118">This message causes the [TVN\_ENDLABELEDIT](tvn-endlabeledit.md) notification code to be sent to the parent window of the tree-view control.</span></span>

## <a name="requirements"></a><span data-ttu-id="b70e3-119">Требования</span><span class="sxs-lookup"><span data-stu-id="b70e3-119">Requirements</span></span>



| <span data-ttu-id="b70e3-120">Требование</span><span class="sxs-lookup"><span data-stu-id="b70e3-120">Requirement</span></span> | <span data-ttu-id="b70e3-121">Значение</span><span class="sxs-lookup"><span data-stu-id="b70e3-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b70e3-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b70e3-122">Minimum supported client</span></span><br/> | <span data-ttu-id="b70e3-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b70e3-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b70e3-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b70e3-124">Minimum supported server</span></span><br/> | <span data-ttu-id="b70e3-125">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b70e3-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b70e3-126">Header</span><span class="sxs-lookup"><span data-stu-id="b70e3-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="b70e3-127"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="b70e3-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





