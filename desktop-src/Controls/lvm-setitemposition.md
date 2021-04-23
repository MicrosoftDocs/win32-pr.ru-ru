---
title: Сообщение LVM_SETITEMPOSITION (Коммктрл. h)
description: Перемещает элемент в указанную позицию в элементе управления "представление списка" (должен быть в виде значка или маленького значка). Это сообщение можно отправить явно или с помощью \_ макроса Сетитемпоситион ListView.
ms.assetid: dfb35af4-e6c3-40fc-9d7c-cf0d68a3ea01
keywords:
- Элементы управления Windows для LVM_SETITEMPOSITION сообщений
topic_type:
- apiref
api_name:
- LVM_SETITEMPOSITION
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b95fcf2949f1e19677bd445c0f6c5f762db078d1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892018"
---
# <a name="lvm_setitemposition-message"></a><span data-ttu-id="84be7-105">\_Сообщение LVM сетитемпоситион</span><span class="sxs-lookup"><span data-stu-id="84be7-105">LVM\_SETITEMPOSITION message</span></span>

<span data-ttu-id="84be7-106">Перемещает элемент в указанную позицию в элементе управления "представление списка" (должен быть в виде значка или маленького значка).</span><span class="sxs-lookup"><span data-stu-id="84be7-106">Moves an item to a specified position in a list-view control (must be in icon or small icon view).</span></span> <span data-ttu-id="84be7-107">Это сообщение можно отправить явно или с помощью макроса [**\_ сетитемпоситион ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemposition) .</span><span class="sxs-lookup"><span data-stu-id="84be7-107">You can send this message explicitly or by using the [**ListView\_SetItemPosition**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemposition) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="84be7-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="84be7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84be7-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="84be7-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="84be7-110">Индекс элемента представления списка.</span><span class="sxs-lookup"><span data-stu-id="84be7-110">Index of the list-view item.</span></span>

</dd> <dt>

<span data-ttu-id="84be7-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="84be7-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="84be7-112">[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) указывает новую позицию по оси x верхнего левого угла элемента в координатах представления.</span><span class="sxs-lookup"><span data-stu-id="84be7-112">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the new x-position of the item's upper-left corner, in view coordinates.</span></span> <span data-ttu-id="84be7-113">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) указывает новую позицию y верхнего левого угла элемента в координатах представления.</span><span class="sxs-lookup"><span data-stu-id="84be7-113">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the new y-position of the item's upper-left corner, in view coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84be7-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="84be7-114">Return value</span></span>

<span data-ttu-id="84be7-115">Возвращает **значение true** , если успешно, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="84be7-115">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="84be7-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="84be7-116">Remarks</span></span>

<span data-ttu-id="84be7-117">Если элемент управления "список" имеет стиль [**\_ автоупорядочивания LVS**](list-view-window-styles.md) , элементы в элементе управления "список" упорядочиваются после установки позиции элемента.</span><span class="sxs-lookup"><span data-stu-id="84be7-117">If the list-view control has the [**LVS\_AUTOARRANGE**](list-view-window-styles.md) style, the items in the list-view control are arranged after the position of the item is set.</span></span>

<span data-ttu-id="84be7-118">В Windows Vista отправка этого сообщения в элемент управления "представление списка" с помощью [**стиля \_ авторазмещения LVS**](list-view-window-styles.md) ничего не делает, а возвращаемое значение равно **false**.</span><span class="sxs-lookup"><span data-stu-id="84be7-118">On Windows Vista, sending this message to a list-view control with the [**LVS\_AUTOARRANGE**](list-view-window-styles.md) style does nothing, and the return value is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="84be7-119">Требования</span><span class="sxs-lookup"><span data-stu-id="84be7-119">Requirements</span></span>



| <span data-ttu-id="84be7-120">Требование</span><span class="sxs-lookup"><span data-stu-id="84be7-120">Requirement</span></span> | <span data-ttu-id="84be7-121">Значение</span><span class="sxs-lookup"><span data-stu-id="84be7-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="84be7-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="84be7-122">Minimum supported client</span></span><br/> | <span data-ttu-id="84be7-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="84be7-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="84be7-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="84be7-124">Minimum supported server</span></span><br/> | <span data-ttu-id="84be7-125">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="84be7-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="84be7-126">Header</span><span class="sxs-lookup"><span data-stu-id="84be7-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="84be7-127"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="84be7-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

