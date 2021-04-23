---
title: Сообщение LVM_GETINSERTMARK (Коммктрл. h)
description: Возвращает позицию точки вставки.
ms.assetid: ad00df4c-4b4b-48f1-8821-7849a216df2e
keywords:
- Элементы управления Windows для LVM_GETINSERTMARK сообщений
topic_type:
- apiref
api_name:
- LVM_GETINSERTMARK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8cba96ae7d357e3e1f5a007fa41f6b7e9e3b64f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891705"
---
# <a name="lvm_getinsertmark-message"></a><span data-ttu-id="4a326-104">\_Сообщение LVM жетинсертмарк</span><span class="sxs-lookup"><span data-stu-id="4a326-104">LVM\_GETINSERTMARK message</span></span>

<span data-ttu-id="4a326-105">Возвращает позицию точки вставки.</span><span class="sxs-lookup"><span data-stu-id="4a326-105">Retrieves the position of the insertion point.</span></span>

## <a name="parameters"></a><span data-ttu-id="4a326-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4a326-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a326-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4a326-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="4a326-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="4a326-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="4a326-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4a326-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="4a326-110">Указатель на структуру <a href="/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark">лвинсертмарк</a> , которая получает позицию точки вставки.</span><span class="sxs-lookup"><span data-stu-id="4a326-110">Pointer to a <a href="/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark">LVINSERTMARK</a> structure that receives the position of the insertion point.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a326-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4a326-111">Return value</span></span>

<span data-ttu-id="4a326-112">Возвращает **значение true** , если успешно, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="4a326-112">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span> <span data-ttu-id="4a326-113">**Значение false** возвращается, если размер в элементе **кбсизе** структуры [**лвинсертмарк**](/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark) не равен фактическому размеру структуры.</span><span class="sxs-lookup"><span data-stu-id="4a326-113">**FALSE** is returned if the size in the **cbSize** member of the [**LVINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark) structure does not equal the actual size of the structure.</span></span>

## <a name="remarks"></a><span data-ttu-id="4a326-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4a326-114">Remarks</span></span>

<span data-ttu-id="4a326-115">Точка вставки может отображаться только в том случае, если элемент управления "представление списка" находится в представлении значков, представлении с небольшим значком или мозаичном представлении, а не в режиме просмотра группы.</span><span class="sxs-lookup"><span data-stu-id="4a326-115">An insertion point can appear only if the list-view control is in icon view, small icon view, or tile view, and is not in group-view mode.</span></span>

> [!Note]  
> <span data-ttu-id="4a326-116">Чтобы использовать это сообщение, необходимо указать манифест, указывающий Comclt32.dll версии 6,0.</span><span class="sxs-lookup"><span data-stu-id="4a326-116">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="4a326-117">Дополнительные сведения о манифестах см. в разделе [Включение визуальных стилей](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="4a326-117">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4a326-118">Требования</span><span class="sxs-lookup"><span data-stu-id="4a326-118">Requirements</span></span>



| <span data-ttu-id="4a326-119">Требование</span><span class="sxs-lookup"><span data-stu-id="4a326-119">Requirement</span></span> | <span data-ttu-id="4a326-120">Значение</span><span class="sxs-lookup"><span data-stu-id="4a326-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4a326-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4a326-121">Minimum supported client</span></span><br/> | <span data-ttu-id="4a326-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4a326-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4a326-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4a326-123">Minimum supported server</span></span><br/> | <span data-ttu-id="4a326-124">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4a326-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4a326-125">Header</span><span class="sxs-lookup"><span data-stu-id="4a326-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="4a326-126"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="4a326-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





