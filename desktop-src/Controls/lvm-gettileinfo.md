---
title: Сообщение LVM_GETTILEINFO (Коммктрл. h)
description: Извлекает сведения о плитке в элементе управления "представление списка".
ms.assetid: e89a3eae-0970-488c-ba95-1072aa85bbf4
keywords:
- Элементы управления Windows для LVM_GETTILEINFO сообщений
topic_type:
- apiref
api_name:
- LVM_GETTILEINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db5bfd085cd5cbaced0bf90b17e8862a6c0e159b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071903"
---
# <a name="lvm_gettileinfo-message"></a><span data-ttu-id="c8b5d-104">\_Сообщение LVM жеттилеинфо</span><span class="sxs-lookup"><span data-stu-id="c8b5d-104">LVM\_GETTILEINFO message</span></span>

<span data-ttu-id="c8b5d-105">Извлекает сведения о плитке в элементе управления "представление списка".</span><span class="sxs-lookup"><span data-stu-id="c8b5d-105">Retrieves information about a tile in a list-view control.</span></span>

## <a name="parameters"></a><span data-ttu-id="c8b5d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c8b5d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8b5d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c8b5d-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="c8b5d-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="c8b5d-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="c8b5d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c8b5d-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="c8b5d-110">Указатель на структуру <a href="/windows/win32/api/commctrl/ns-commctrl-lvtileinfo">**лвтилеинфо**</a> , которая получает извлеченные сведения.</span><span class="sxs-lookup"><span data-stu-id="c8b5d-110">Pointer to an <a href="/windows/win32/api/commctrl/ns-commctrl-lvtileinfo">**LVTILEINFO**</a> structure that receives the retrieved information.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8b5d-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c8b5d-111">Return value</span></span>

<span data-ttu-id="c8b5d-112">Возвращаемое значение не используется.</span><span class="sxs-lookup"><span data-stu-id="c8b5d-112">Return value not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="c8b5d-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c8b5d-113">Remarks</span></span>

<span data-ttu-id="c8b5d-114">Мозаичное представление — это новый способ упорядочения и отображения элементов в элементе управления "представление списка".</span><span class="sxs-lookup"><span data-stu-id="c8b5d-114">Tile view is a new way of arranging and displaying items in a list-view control.</span></span> <span data-ttu-id="c8b5d-115">К другим представлениям относятся значок, маленький значок, сведения и список.</span><span class="sxs-lookup"><span data-stu-id="c8b5d-115">The other views are icon, small icon, details, and list.</span></span>

> [!Note]  
> <span data-ttu-id="c8b5d-116">Чтобы использовать это сообщение, необходимо указать манифест, указывающий Comclt32.dll версии 6,0.</span><span class="sxs-lookup"><span data-stu-id="c8b5d-116">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="c8b5d-117">Дополнительные сведения о манифестах см. в разделе [Включение визуальных стилей](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="c8b5d-117">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c8b5d-118">Требования</span><span class="sxs-lookup"><span data-stu-id="c8b5d-118">Requirements</span></span>



| <span data-ttu-id="c8b5d-119">Требование</span><span class="sxs-lookup"><span data-stu-id="c8b5d-119">Requirement</span></span> | <span data-ttu-id="c8b5d-120">Значение</span><span class="sxs-lookup"><span data-stu-id="c8b5d-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c8b5d-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c8b5d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c8b5d-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c8b5d-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c8b5d-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c8b5d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c8b5d-124">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c8b5d-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c8b5d-125">Header</span><span class="sxs-lookup"><span data-stu-id="c8b5d-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="c8b5d-126"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="c8b5d-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





