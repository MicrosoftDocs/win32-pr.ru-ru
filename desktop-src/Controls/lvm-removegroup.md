---
title: Сообщение LVM_REMOVEGROUP (Коммктрл. h)
description: Удаляет группу из элемента управления "представление списка".
ms.assetid: c6f4f54c-4cf8-47d0-8e96-fa8a1df0501b
keywords:
- Элементы управления Windows для LVM_REMOVEGROUP сообщений
topic_type:
- apiref
api_name:
- LVM_REMOVEGROUP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa631593e791f90c76a9f74aa1d967d9678540f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988908"
---
# <a name="lvm_removegroup-message"></a><span data-ttu-id="c43a6-104">\_Сообщение LVM ремовеграуп</span><span class="sxs-lookup"><span data-stu-id="c43a6-104">LVM\_REMOVEGROUP message</span></span>

<span data-ttu-id="c43a6-105">Удаляет группу из элемента управления "представление списка".</span><span class="sxs-lookup"><span data-stu-id="c43a6-105">Removes a group from a list-view control.</span></span>

## <a name="parameters"></a><span data-ttu-id="c43a6-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c43a6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c43a6-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c43a6-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="c43a6-108">Идентификатор, указывающий удаляемую группу.</span><span class="sxs-lookup"><span data-stu-id="c43a6-108">ID that specifies the group to remove.</span></span></dd> <dt>

<span data-ttu-id="c43a6-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c43a6-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c43a6-110">Должен иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="c43a6-110">Must be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c43a6-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c43a6-111">Return value</span></span>

<span data-ttu-id="c43a6-112">Возвращает индекс группы в случае успеха или значение-1 в противном случае.</span><span class="sxs-lookup"><span data-stu-id="c43a6-112">Returns the index of the group if successful, or -1 otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="c43a6-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c43a6-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="c43a6-114">Чтобы использовать это сообщение, необходимо указать манифест, указывающий Comclt32.dll версии 6,0.</span><span class="sxs-lookup"><span data-stu-id="c43a6-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="c43a6-115">Дополнительные сведения о манифестах см. в разделе [Включение визуальных стилей](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="c43a6-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c43a6-116">Требования</span><span class="sxs-lookup"><span data-stu-id="c43a6-116">Requirements</span></span>



| <span data-ttu-id="c43a6-117">Требование</span><span class="sxs-lookup"><span data-stu-id="c43a6-117">Requirement</span></span> | <span data-ttu-id="c43a6-118">Значение</span><span class="sxs-lookup"><span data-stu-id="c43a6-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c43a6-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c43a6-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c43a6-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c43a6-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c43a6-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c43a6-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c43a6-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c43a6-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c43a6-123">Header</span><span class="sxs-lookup"><span data-stu-id="c43a6-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c43a6-124"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="c43a6-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





