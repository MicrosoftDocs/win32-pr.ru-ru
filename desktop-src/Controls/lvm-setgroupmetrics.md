---
title: Сообщение LVM_SETGROUPMETRICS (Коммктрл. h)
description: Задает сведения о отображении групп.
ms.assetid: 268b478d-da1f-4efe-9ee9-af3f12e089ee
keywords:
- Элементы управления Windows для LVM_SETGROUPMETRICS сообщений
topic_type:
- apiref
api_name:
- LVM_SETGROUPMETRICS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8215962e6f84aac83a2151b46f489938b575303c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340350"
---
# <a name="lvm_setgroupmetrics-message"></a><span data-ttu-id="0c78c-104">\_Сообщение LVM сетграупметрикс</span><span class="sxs-lookup"><span data-stu-id="0c78c-104">LVM\_SETGROUPMETRICS message</span></span>

<span data-ttu-id="0c78c-105">Задает сведения о отображении групп.</span><span class="sxs-lookup"><span data-stu-id="0c78c-105">Sets information about the display of groups.</span></span>

## <a name="parameters"></a><span data-ttu-id="0c78c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0c78c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c78c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0c78c-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="0c78c-108">Должен иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="0c78c-108">Must be **NULL**.</span></span></dd> <dt>

<span data-ttu-id="0c78c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0c78c-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="0c78c-110">Указатель на структуру <a href="/windows/win32/api/commctrl/ns-commctrl-lvgroupmetrics">**лвграупметрикс**</a> , содержащую метрики, которые необходимо задать.</span><span class="sxs-lookup"><span data-stu-id="0c78c-110">Pointer to an <a href="/windows/win32/api/commctrl/ns-commctrl-lvgroupmetrics">**LVGROUPMETRICS**</a> structure that contains the metrics to set.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0c78c-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0c78c-111">Return value</span></span>

<span data-ttu-id="0c78c-112">Возвращаемое значение не используется.</span><span class="sxs-lookup"><span data-stu-id="0c78c-112">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="0c78c-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0c78c-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="0c78c-114">Чтобы использовать это сообщение, необходимо указать манифест, указывающий Comclt32.dll версии 6,0.</span><span class="sxs-lookup"><span data-stu-id="0c78c-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="0c78c-115">Дополнительные сведения о манифестах см. в разделе [Включение визуальных стилей](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="0c78c-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="0c78c-116">Требования</span><span class="sxs-lookup"><span data-stu-id="0c78c-116">Requirements</span></span>



| <span data-ttu-id="0c78c-117">Требование</span><span class="sxs-lookup"><span data-stu-id="0c78c-117">Requirement</span></span> | <span data-ttu-id="0c78c-118">Значение</span><span class="sxs-lookup"><span data-stu-id="0c78c-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0c78c-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0c78c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="0c78c-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0c78c-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0c78c-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0c78c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="0c78c-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0c78c-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0c78c-123">Header</span><span class="sxs-lookup"><span data-stu-id="0c78c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="0c78c-124"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="0c78c-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





