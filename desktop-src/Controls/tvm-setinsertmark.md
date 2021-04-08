---
title: Сообщение TVM_SETINSERTMARK (Коммктрл. h)
description: Задает метку вставки в элементе управления "дерево-представление". Это сообщение можно отправить явно или с помощью \_ макроса Сетинсертмарк TreeView.
ms.assetid: 35441807-406a-408c-ad89-6dd40c907e3c
keywords:
- Элементы управления Windows для TVM_SETINSERTMARK сообщений
topic_type:
- apiref
api_name:
- TVM_SETINSERTMARK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff5a9cc9b05e9cd7dc3281d778734bee1048ffd2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892133"
---
# <a name="tvm_setinsertmark-message"></a><span data-ttu-id="53617-105">\_Сообщение TVM сетинсертмарк</span><span class="sxs-lookup"><span data-stu-id="53617-105">TVM\_SETINSERTMARK message</span></span>

<span data-ttu-id="53617-106">Задает метку вставки в элементе управления "дерево-представление".</span><span class="sxs-lookup"><span data-stu-id="53617-106">Sets the insertion mark in a tree-view control.</span></span> <span data-ttu-id="53617-107">Это сообщение можно отправить явно или с помощью макроса [**\_ сетинсертмарк TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setinsertmark) .</span><span class="sxs-lookup"><span data-stu-id="53617-107">You can send this message explicitly or by using the [**TreeView\_SetInsertMark**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setinsertmark) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="53617-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="53617-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53617-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="53617-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="53617-110">**Логическое** значение, указывающее, размещается ли метка вставки до или после указанного элемента.</span><span class="sxs-lookup"><span data-stu-id="53617-110">**BOOL** value that specifies if the insertion mark is placed before or after the specified item.</span></span> <span data-ttu-id="53617-111">Если этот аргумент не равен нулю, то после элемента будет помещен знак вставки.</span><span class="sxs-lookup"><span data-stu-id="53617-111">If this argument is nonzero, the insertion mark will be placed after the item.</span></span> <span data-ttu-id="53617-112">Если этот аргумент равен нулю, то метка вставки будет помещена перед элементом.</span><span class="sxs-lookup"><span data-stu-id="53617-112">If this argument is zero, the insertion mark will be placed before the item.</span></span>

</dd> <dt>

<span data-ttu-id="53617-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="53617-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="53617-114">**Хтриитем** , указывающий, в какой элемент будет помещена метка вставки.</span><span class="sxs-lookup"><span data-stu-id="53617-114">**HTREEITEM** that specifies at which item the insertion mark will be placed.</span></span> <span data-ttu-id="53617-115">Если этот аргумент имеет **значение NULL**, то метка вставки удаляется.</span><span class="sxs-lookup"><span data-stu-id="53617-115">If this argument is **NULL**, the insertion mark is removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53617-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="53617-116">Return value</span></span>

<span data-ttu-id="53617-117">Возвращает ненулевое значение в случае успеха или ноль в противном случае.</span><span class="sxs-lookup"><span data-stu-id="53617-117">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="53617-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="53617-118">Remarks</span></span>

<span data-ttu-id="53617-119">В некоторых случаях знак вставки может отображаться в двух местах после развертывания узла.</span><span class="sxs-lookup"><span data-stu-id="53617-119">In some circumstances, the insert mark can appear in two places after a node is expanded.</span></span> <span data-ttu-id="53617-120">Если вы используете метки вставки, рекомендуется принудительно обновить элемент управления после развертывания узла.</span><span class="sxs-lookup"><span data-stu-id="53617-120">If you are using insertion marks, it is recommended that you force a refresh of the control after expanding a node.</span></span>

## <a name="requirements"></a><span data-ttu-id="53617-121">Требования</span><span class="sxs-lookup"><span data-stu-id="53617-121">Requirements</span></span>



| <span data-ttu-id="53617-122">Требование</span><span class="sxs-lookup"><span data-stu-id="53617-122">Requirement</span></span> | <span data-ttu-id="53617-123">Значение</span><span class="sxs-lookup"><span data-stu-id="53617-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="53617-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="53617-124">Minimum supported client</span></span><br/> | <span data-ttu-id="53617-125">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="53617-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="53617-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="53617-126">Minimum supported server</span></span><br/> | <span data-ttu-id="53617-127">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="53617-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="53617-128">Header</span><span class="sxs-lookup"><span data-stu-id="53617-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="53617-129"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="53617-129"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





