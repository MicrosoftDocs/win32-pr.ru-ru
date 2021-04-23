---
title: Сообщение LVM_HASGROUP (Коммктрл. h)
description: Определяет, имеет ли элемент управления "представление списка" указанную группу.
ms.assetid: 0b8a9208-5221-4f66-8b26-7de55afe485f
keywords:
- Элементы управления Windows для LVM_HASGROUP сообщений
topic_type:
- apiref
api_name:
- LVM_HASGROUP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb05fed8466188aa0025d2128ce64ad7f1512c07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492393"
---
# <a name="lvm_hasgroup-message"></a><span data-ttu-id="cb5ae-104">\_Сообщение LVM хасграуп</span><span class="sxs-lookup"><span data-stu-id="cb5ae-104">LVM\_HASGROUP message</span></span>

<span data-ttu-id="cb5ae-105">Определяет, имеет ли элемент управления "представление списка" указанную группу.</span><span class="sxs-lookup"><span data-stu-id="cb5ae-105">Determines whether the list-view control has a specified group.</span></span>

## <a name="parameters"></a><span data-ttu-id="cb5ae-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="cb5ae-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb5ae-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cb5ae-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="cb5ae-108">Идентификатор группы.</span><span class="sxs-lookup"><span data-stu-id="cb5ae-108">ID of the group.</span></span></dd> <dt>

<span data-ttu-id="cb5ae-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cb5ae-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="cb5ae-110">Должен иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="cb5ae-110">Must be **NULL**.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb5ae-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cb5ae-111">Return value</span></span>

<span data-ttu-id="cb5ae-112">Возвращает **значение true** , если элемент управления "представление списка" имеет указанную группу, или **значение false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="cb5ae-112">Returns **TRUE** if the list-view control has the specified group, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="cb5ae-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cb5ae-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="cb5ae-114">Чтобы использовать это сообщение, необходимо указать манифест, указывающий Comclt32.dll версии 6,0.</span><span class="sxs-lookup"><span data-stu-id="cb5ae-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="cb5ae-115">Дополнительные сведения о манифестах см. в разделе [Включение визуальных стилей](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="cb5ae-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="cb5ae-116">Требования</span><span class="sxs-lookup"><span data-stu-id="cb5ae-116">Requirements</span></span>



| <span data-ttu-id="cb5ae-117">Требование</span><span class="sxs-lookup"><span data-stu-id="cb5ae-117">Requirement</span></span> | <span data-ttu-id="cb5ae-118">Значение</span><span class="sxs-lookup"><span data-stu-id="cb5ae-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cb5ae-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cb5ae-119">Minimum supported client</span></span><br/> | <span data-ttu-id="cb5ae-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cb5ae-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cb5ae-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cb5ae-121">Minimum supported server</span></span><br/> | <span data-ttu-id="cb5ae-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="cb5ae-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cb5ae-123">Header</span><span class="sxs-lookup"><span data-stu-id="cb5ae-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="cb5ae-124"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="cb5ae-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





