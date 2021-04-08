---
title: Сообщение TVM_SETBORDER (Коммктрл. h)
description: Задает размер границы для элементов в элементе управления "представление дерева". Сообщение можно отправить явно или с помощью \_ макроса Сетбордер TreeView.
ms.assetid: 468b46ae-2ab2-4753-a0af-7c644f75ce62
keywords:
- Элементы управления Windows для TVM_SETBORDER сообщений
topic_type:
- apiref
api_name:
- TVM_SETBORDER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b4401959e2579caab7f2cb4b6eed1ea34481ffa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892137"
---
# <a name="tvm_setborder-message"></a><span data-ttu-id="b4bd2-105">\_Сообщение TVM сетбордер</span><span class="sxs-lookup"><span data-stu-id="b4bd2-105">TVM\_SETBORDER message</span></span>

<span data-ttu-id="b4bd2-106">**Предназначен для внутреннего использования; не рекомендуется для использования в приложениях.**</span><span class="sxs-lookup"><span data-stu-id="b4bd2-106">**Intended for internal use; not recommended for use in applications.**</span></span>

<span data-ttu-id="b4bd2-107">Задает размер границы для элементов в элементе управления "представление дерева".</span><span class="sxs-lookup"><span data-stu-id="b4bd2-107">Sets the size of the border for the items in a tree-view control.</span></span> <span data-ttu-id="b4bd2-108">Сообщение можно отправить явно или с помощью макроса [**\_ сетбордер TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setborder) .</span><span class="sxs-lookup"><span data-stu-id="b4bd2-108">You can send the message explicitly or by using the [**TreeView\_SetBorder**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setborder) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="b4bd2-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="b4bd2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4bd2-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b4bd2-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b4bd2-111">Флаги действия.</span><span class="sxs-lookup"><span data-stu-id="b4bd2-111">Action flags.</span></span> <span data-ttu-id="b4bd2-112">Этот параметр может принимать одно или несколько из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="b4bd2-112">This parameter can be one or more of the following values:</span></span>



| <span data-ttu-id="b4bd2-113">Значение</span><span class="sxs-lookup"><span data-stu-id="b4bd2-113">Value</span></span>                                                                                                                                                         | <span data-ttu-id="b4bd2-114">Значение</span><span class="sxs-lookup"><span data-stu-id="b4bd2-114">Meaning</span></span>                                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span id="TVSBF_XBORDER"></span><span id="tvsbf_xborder"></span><dl> <span data-ttu-id="b4bd2-115"><dt>**ТВСБФ \_ ксбордер**</dt></span><span class="sxs-lookup"><span data-stu-id="b4bd2-115"><dt>**TVSBF\_XBORDER**</dt></span></span> </dl> | <span data-ttu-id="b4bd2-116">Применяет указанный размер границы к левой части элементов в элементе управления "дерево-представление".</span><span class="sxs-lookup"><span data-stu-id="b4bd2-116">Applies the specified border size to the left side of the items in the tree-view control.</span></span> <br/> |
| <span id="TVSBF_YBORDER"></span><span id="tvsbf_yborder"></span><dl> <span data-ttu-id="b4bd2-117"><dt>**ТВСБФ \_ ибордер**</dt></span><span class="sxs-lookup"><span data-stu-id="b4bd2-117"><dt>**TVSBF\_YBORDER**</dt></span></span> </dl> | <span data-ttu-id="b4bd2-118">Применяет указанный размер границы к верхней части элементов в элементе управления "дерево-представление".</span><span class="sxs-lookup"><span data-stu-id="b4bd2-118">Applies the specified border size to the top of the items in the tree-view control.</span></span><br/>        |



 

</dd> <dt>

<span data-ttu-id="b4bd2-119">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b4bd2-119">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b4bd2-120">[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) — это **короткое** значение, указывающее размер левой границы в пикселях.</span><span class="sxs-lookup"><span data-stu-id="b4bd2-120">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is a **SHORT** that specifies the size of the left border, in pixels.</span></span> <span data-ttu-id="b4bd2-121">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) — это **короткое** значение, указывающее размер верхней границы (в пикселях).</span><span class="sxs-lookup"><span data-stu-id="b4bd2-121">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) is a **SHORT** that specifies the size of the top border, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4bd2-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b4bd2-122">Return value</span></span>

<span data-ttu-id="b4bd2-123">Возвращает значение **типа Long** , содержащее предыдущий размер границы (в пикселях).</span><span class="sxs-lookup"><span data-stu-id="b4bd2-123">Returns a **LONG** value that contains the previous border size, in pixels.</span></span> <span data-ttu-id="b4bd2-124">[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) содержит предыдущий размер горизонтальной границы, а [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) содержит предыдущий размер вертикальной границы.</span><span class="sxs-lookup"><span data-stu-id="b4bd2-124">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the previous size of the horizontal border, and the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) contains the previous size of the vertical border.</span></span>

## <a name="remarks"></a><span data-ttu-id="b4bd2-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b4bd2-125">Remarks</span></span>

<span data-ttu-id="b4bd2-126">**Предупреждение системы безопасности:** Использование этого сообщения может нарушить безопасность программы.</span><span class="sxs-lookup"><span data-stu-id="b4bd2-126">**Security Warning:** Using this message might compromise the security of your program.</span></span>

<span data-ttu-id="b4bd2-127">Граница элемента задается только для целей разделения.</span><span class="sxs-lookup"><span data-stu-id="b4bd2-127">The item border is set just for spacing purposes.</span></span> <span data-ttu-id="b4bd2-128">Успешный параметр активирует повторное вычисление полос прокрутки.</span><span class="sxs-lookup"><span data-stu-id="b4bd2-128">A successful setting triggers a recalculation of the scroll bars.</span></span>

<span data-ttu-id="b4bd2-129">Это сообщение может не поддерживаться в будущих версиях Comctl32.dll.</span><span class="sxs-lookup"><span data-stu-id="b4bd2-129">This message may not be supported in future versions of Comctl32.dll.</span></span> <span data-ttu-id="b4bd2-130">Кроме того, это сообщение не определено в коммктрл. h.</span><span class="sxs-lookup"><span data-stu-id="b4bd2-130">Also, this message is not defined in commctrl.h.</span></span> <span data-ttu-id="b4bd2-131">Добавьте следующие определения в исходные файлы приложения для использования сообщения:</span><span class="sxs-lookup"><span data-stu-id="b4bd2-131">Add the following definitions to the source files of your application to use the message:</span></span>

``` syntax
#define TVM_SETBORDER (TV_FIRST + 35)
#define TVSBF_XBORDER 0x00000001
#define TVSBF_YBORDER 0x00000002 
```

## <a name="requirements"></a><span data-ttu-id="b4bd2-132">Требования</span><span class="sxs-lookup"><span data-stu-id="b4bd2-132">Requirements</span></span>



| <span data-ttu-id="b4bd2-133">Требование</span><span class="sxs-lookup"><span data-stu-id="b4bd2-133">Requirement</span></span> | <span data-ttu-id="b4bd2-134">Значение</span><span class="sxs-lookup"><span data-stu-id="b4bd2-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b4bd2-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b4bd2-135">Minimum supported client</span></span><br/> | <span data-ttu-id="b4bd2-136">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b4bd2-136">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b4bd2-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b4bd2-137">Minimum supported server</span></span><br/> | <span data-ttu-id="b4bd2-138">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b4bd2-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b4bd2-139">Header</span><span class="sxs-lookup"><span data-stu-id="b4bd2-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="b4bd2-140"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="b4bd2-140"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4bd2-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b4bd2-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4bd2-142">**\_Сетбордер TreeView**</span><span class="sxs-lookup"><span data-stu-id="b4bd2-142">**TreeView\_SetBorder**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setborder)
</dt> </dl>

 

