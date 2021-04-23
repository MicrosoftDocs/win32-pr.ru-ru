---
title: Сообщение LVM_SETINSERTMARKCOLOR (Коммктрл. h)
description: Задает цвет точки вставки.
ms.assetid: dce2c266-672b-4682-ba23-51d9a8e1102b
keywords:
- Элементы управления Windows для LVM_SETINSERTMARKCOLOR сообщений
topic_type:
- apiref
api_name:
- LVM_SETINSERTMARKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 260d21d083e2c70d8e82a27628e42596bd1b37eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988196"
---
# <a name="lvm_setinsertmarkcolor-message"></a><span data-ttu-id="91e44-104">\_Сообщение LVM сетинсертмаркколор</span><span class="sxs-lookup"><span data-stu-id="91e44-104">LVM\_SETINSERTMARKCOLOR message</span></span>

<span data-ttu-id="91e44-105">Задает цвет точки вставки.</span><span class="sxs-lookup"><span data-stu-id="91e44-105">Sets the color of the insertion point.</span></span>

## <a name="parameters"></a><span data-ttu-id="91e44-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="91e44-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91e44-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="91e44-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="91e44-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="91e44-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="91e44-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="91e44-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="91e44-110">Структура **COLORREF** , указывающая цвет для установки точки вставки.</span><span class="sxs-lookup"><span data-stu-id="91e44-110">**COLORREF** structure that specifies the color to set the insertion point.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91e44-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="91e44-111">Return value</span></span>

<span data-ttu-id="91e44-112">Возвращает структуру **COLORREF** , установленную на предыдущий цвет.</span><span class="sxs-lookup"><span data-stu-id="91e44-112">Returns **COLORREF** structure set to the previous color.</span></span>

## <a name="remarks"></a><span data-ttu-id="91e44-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="91e44-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="91e44-114">Чтобы использовать это сообщение, необходимо указать манифест, указывающий Comclt32.dll версии 6,0.</span><span class="sxs-lookup"><span data-stu-id="91e44-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="91e44-115">Дополнительные сведения о манифестах см. в разделе [Включение визуальных стилей](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="91e44-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="91e44-116">Требования</span><span class="sxs-lookup"><span data-stu-id="91e44-116">Requirements</span></span>



| <span data-ttu-id="91e44-117">Требование</span><span class="sxs-lookup"><span data-stu-id="91e44-117">Requirement</span></span> | <span data-ttu-id="91e44-118">Значение</span><span class="sxs-lookup"><span data-stu-id="91e44-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="91e44-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="91e44-119">Minimum supported client</span></span><br/> | <span data-ttu-id="91e44-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="91e44-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="91e44-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="91e44-121">Minimum supported server</span></span><br/> | <span data-ttu-id="91e44-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="91e44-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="91e44-123">Header</span><span class="sxs-lookup"><span data-stu-id="91e44-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="91e44-124"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="91e44-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





