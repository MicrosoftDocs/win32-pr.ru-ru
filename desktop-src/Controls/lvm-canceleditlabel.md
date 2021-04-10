---
title: Сообщение LVM_CANCELEDITLABEL (Коммктрл. h)
description: Отменяет операцию изменения текста элемента.
ms.assetid: 73e9c922-3223-4c49-a33c-df7c09443ccc
keywords:
- Элементы управления Windows для LVM_CANCELEDITLABEL сообщений
topic_type:
- apiref
api_name:
- LVM_CANCELEDITLABEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: edfed26fb3c38d91f7a5b07683079d29ecd4597d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135142"
---
# <a name="lvm_canceleditlabel-message"></a><span data-ttu-id="2277a-104">\_Сообщение LVM канцеледитлабел</span><span class="sxs-lookup"><span data-stu-id="2277a-104">LVM\_CANCELEDITLABEL message</span></span>

<span data-ttu-id="2277a-105">Отменяет операцию изменения текста элемента.</span><span class="sxs-lookup"><span data-stu-id="2277a-105">Cancels an item text editing operation.</span></span>

## <a name="parameters"></a><span data-ttu-id="2277a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2277a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2277a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2277a-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="2277a-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="2277a-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="2277a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2277a-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="2277a-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="2277a-110">Must be zero.</span></span></dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2277a-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2277a-111">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="2277a-112">Чтобы использовать это сообщение, необходимо указать манифест, указывающий Comclt32.dll версии 6,0.</span><span class="sxs-lookup"><span data-stu-id="2277a-112">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="2277a-113">Дополнительные сведения о манифестах см. в разделе [Включение визуальных стилей](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="2277a-113">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

<span data-ttu-id="2277a-114">Это сообщение вызывает отправку уведомления [ЛВН \_ ендлабеледит](lvn-endlabeledit.md) .</span><span class="sxs-lookup"><span data-stu-id="2277a-114">This message causes a an [LVN\_ENDLABELEDIT](lvn-endlabeledit.md) notification to be sent.</span></span>

## <a name="requirements"></a><span data-ttu-id="2277a-115">Требования</span><span class="sxs-lookup"><span data-stu-id="2277a-115">Requirements</span></span>



| <span data-ttu-id="2277a-116">Требование</span><span class="sxs-lookup"><span data-stu-id="2277a-116">Requirement</span></span> | <span data-ttu-id="2277a-117">Значение</span><span class="sxs-lookup"><span data-stu-id="2277a-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2277a-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2277a-118">Minimum supported client</span></span><br/> | <span data-ttu-id="2277a-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2277a-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2277a-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2277a-120">Minimum supported server</span></span><br/> | <span data-ttu-id="2277a-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2277a-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2277a-122">Header</span><span class="sxs-lookup"><span data-stu-id="2277a-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="2277a-123"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="2277a-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





