---
title: Сообщение LVM_INSERTMARKHITTEST (Коммктрл. h)
description: Извлекает точку вставки, ближайшую к заданной точке.
ms.assetid: 901bb770-a36d-4d9f-a53b-d497b4df39e5
keywords:
- Элементы управления Windows для LVM_INSERTMARKHITTEST сообщений
topic_type:
- apiref
api_name:
- LVM_INSERTMARKHITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3bdb82e924b4a5d74d152917f52c4039e0aca81b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137098"
---
# <a name="lvm_insertmarkhittest-message"></a><span data-ttu-id="df04c-104">\_Сообщение LVM инсертмаркхиттест</span><span class="sxs-lookup"><span data-stu-id="df04c-104">LVM\_INSERTMARKHITTEST message</span></span>

<span data-ttu-id="df04c-105">Извлекает точку вставки, ближайшую к заданной точке.</span><span class="sxs-lookup"><span data-stu-id="df04c-105">Retrieves the insertion point closest to a specified point.</span></span>

## <a name="parameters"></a><span data-ttu-id="df04c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="df04c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df04c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="df04c-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="df04c-108">Указатель на структуру **точек** , содержащую координаты проверки попадания.</span><span class="sxs-lookup"><span data-stu-id="df04c-108">Pointer to a **POINT** structure that contains the hit test coordinates.</span></span></dd> <dt>

<span data-ttu-id="df04c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="df04c-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="df04c-110">Указатель на структуру <a href="/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark">лвинсертмарк</a> , указывающую точку вставки, ближайшую к координатам, определенным параметром *wParam* .</span><span class="sxs-lookup"><span data-stu-id="df04c-110">Pointer to an <a href="/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark">LVINSERTMARK</a> structure that specifies the insertion point closest to the coordinates defined by the *wParam* parameter.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df04c-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="df04c-111">Return value</span></span>

<span data-ttu-id="df04c-112">Возвращает **значение true** , если успешно, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="df04c-112">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span> <span data-ttu-id="df04c-113">**Значение false** возвращается, если размер элемента **кбсизе** структуры [**лвинсертмарк**](/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark) не равен фактическому размеру структуры или если точка вставки не применяется в текущем представлении.</span><span class="sxs-lookup"><span data-stu-id="df04c-113">**FALSE** is returned if the size in the **cbSize** member of the [**LVINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark) structure does not equal the actual size of the structure, or when an insertion point does not apply in the current view.</span></span>

## <a name="remarks"></a><span data-ttu-id="df04c-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="df04c-114">Remarks</span></span>

<span data-ttu-id="df04c-115">Точка вставки может отображаться только в том случае, если элемент управления "представление списка" находится в представлении значков, представлении с небольшим значком или мозаичном представлении, а не в режиме просмотра группы.</span><span class="sxs-lookup"><span data-stu-id="df04c-115">An insertion point can only appear if the list-view control is in icon view, small icon view, or tile view and is not in group-view mode.</span></span>

<span data-ttu-id="df04c-116">Если точки вставки не применяются к представлению, структура [**лвинсертмарк**](/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark) содержит значение-1 в элементе **Член iItem** .</span><span class="sxs-lookup"><span data-stu-id="df04c-116">If insertion points do not apply for the view, the [**LVINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark) structure contains a -1 in the **iItem** member.</span></span>

> [!Note]  
> <span data-ttu-id="df04c-117">Чтобы использовать это сообщение, необходимо указать манифест, указывающий Comclt32.dll версии 6,0.</span><span class="sxs-lookup"><span data-stu-id="df04c-117">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="df04c-118">Дополнительные сведения о манифестах см. в разделе [Включение визуальных стилей](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="df04c-118">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="df04c-119">Требования</span><span class="sxs-lookup"><span data-stu-id="df04c-119">Requirements</span></span>



| <span data-ttu-id="df04c-120">Требование</span><span class="sxs-lookup"><span data-stu-id="df04c-120">Requirement</span></span> | <span data-ttu-id="df04c-121">Значение</span><span class="sxs-lookup"><span data-stu-id="df04c-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="df04c-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="df04c-122">Minimum supported client</span></span><br/> | <span data-ttu-id="df04c-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="df04c-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="df04c-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="df04c-124">Minimum supported server</span></span><br/> | <span data-ttu-id="df04c-125">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="df04c-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="df04c-126">Header</span><span class="sxs-lookup"><span data-stu-id="df04c-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="df04c-127"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="df04c-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





