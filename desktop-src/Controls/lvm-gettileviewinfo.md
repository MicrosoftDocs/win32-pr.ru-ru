---
title: Сообщение LVM_GETTILEVIEWINFO (Коммктрл. h)
description: Извлекает сведения об элементе управления "представление списка" в мозаичном представлении.
ms.assetid: 114990c0-a150-49d8-80e7-b084c648ac34
keywords:
- Элементы управления Windows для LVM_GETTILEVIEWINFO сообщений
topic_type:
- apiref
api_name:
- LVM_GETTILEVIEWINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfe1f34da560d539a9ae12cc7a065b2bf37bc3c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803388"
---
# <a name="lvm_gettileviewinfo-message"></a><span data-ttu-id="4eb1f-104">\_Сообщение LVM жеттилевиевинфо</span><span class="sxs-lookup"><span data-stu-id="4eb1f-104">LVM\_GETTILEVIEWINFO message</span></span>

<span data-ttu-id="4eb1f-105">Извлекает сведения об элементе управления "представление списка" в мозаичном представлении.</span><span class="sxs-lookup"><span data-stu-id="4eb1f-105">Retrieves information about a list-view control in tile view.</span></span>

## <a name="parameters"></a><span data-ttu-id="4eb1f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4eb1f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4eb1f-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4eb1f-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="4eb1f-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="4eb1f-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="4eb1f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4eb1f-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="4eb1f-110">Указатель на структуру <a href="/windows/win32/api/commctrl/ns-commctrl-lvtileviewinfo">**лвтилевиевинфо**</a> , которая получает извлеченные сведения.</span><span class="sxs-lookup"><span data-stu-id="4eb1f-110">Pointer to an <a href="/windows/win32/api/commctrl/ns-commctrl-lvtileviewinfo">**LVTILEVIEWINFO**</a> structure that receives the retrieved information.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4eb1f-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4eb1f-111">Return value</span></span>

<span data-ttu-id="4eb1f-112">Возвращаемое значение не используется.</span><span class="sxs-lookup"><span data-stu-id="4eb1f-112">Return value not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="4eb1f-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4eb1f-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="4eb1f-114">Чтобы использовать это сообщение, необходимо указать манифест, указывающий Comclt32.dll версии 6,0.</span><span class="sxs-lookup"><span data-stu-id="4eb1f-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="4eb1f-115">Дополнительные сведения о манифестах см. в разделе [Включение визуальных стилей](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="4eb1f-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4eb1f-116">Требования</span><span class="sxs-lookup"><span data-stu-id="4eb1f-116">Requirements</span></span>



| <span data-ttu-id="4eb1f-117">Требование</span><span class="sxs-lookup"><span data-stu-id="4eb1f-117">Requirement</span></span> | <span data-ttu-id="4eb1f-118">Значение</span><span class="sxs-lookup"><span data-stu-id="4eb1f-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4eb1f-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4eb1f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="4eb1f-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4eb1f-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4eb1f-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4eb1f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="4eb1f-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4eb1f-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4eb1f-123">Header</span><span class="sxs-lookup"><span data-stu-id="4eb1f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="4eb1f-124"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="4eb1f-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





