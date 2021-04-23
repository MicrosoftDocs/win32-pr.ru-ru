---
title: Сообщение LVM_ISGROUPVIEWENABLED (Коммктрл. h)
description: Проверяет, включено ли представление группы в элементе управления "представление списка".
ms.assetid: 7c6ffa1f-300c-4e5e-900f-93a41e06c951
keywords:
- Элементы управления Windows для LVM_ISGROUPVIEWENABLED сообщений
topic_type:
- apiref
api_name:
- LVM_ISGROUPVIEWENABLED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f8f7af79a1b0594ba6ebb100c1c975f09898d35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989167"
---
# <a name="lvm_isgroupviewenabled-message"></a><span data-ttu-id="55e79-104">\_Сообщение LVM исграупвиевенаблед</span><span class="sxs-lookup"><span data-stu-id="55e79-104">LVM\_ISGROUPVIEWENABLED message</span></span>

<span data-ttu-id="55e79-105">Проверяет, включено ли представление группы в элементе управления "представление списка".</span><span class="sxs-lookup"><span data-stu-id="55e79-105">Checks whether the list-view control has group view enabled.</span></span>

## <a name="parameters"></a><span data-ttu-id="55e79-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="55e79-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55e79-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="55e79-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="55e79-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="55e79-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="55e79-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="55e79-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="55e79-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="55e79-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55e79-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="55e79-111">Return value</span></span>

<span data-ttu-id="55e79-112">Возвращает **значение true** , если представление группы включено, или **значение false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="55e79-112">Returns **TRUE** if group view is enabled, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="55e79-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="55e79-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="55e79-114">Чтобы использовать это сообщение, необходимо указать манифест, указывающий Comclt32.dll версии 6,0.</span><span class="sxs-lookup"><span data-stu-id="55e79-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="55e79-115">Дополнительные сведения о манифестах см. в разделе [Включение визуальных стилей](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="55e79-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="55e79-116">Требования</span><span class="sxs-lookup"><span data-stu-id="55e79-116">Requirements</span></span>



| <span data-ttu-id="55e79-117">Требование</span><span class="sxs-lookup"><span data-stu-id="55e79-117">Requirement</span></span> | <span data-ttu-id="55e79-118">Значение</span><span class="sxs-lookup"><span data-stu-id="55e79-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="55e79-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="55e79-119">Minimum supported client</span></span><br/> | <span data-ttu-id="55e79-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="55e79-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="55e79-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="55e79-121">Minimum supported server</span></span><br/> | <span data-ttu-id="55e79-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="55e79-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="55e79-123">Header</span><span class="sxs-lookup"><span data-stu-id="55e79-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="55e79-124"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="55e79-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





