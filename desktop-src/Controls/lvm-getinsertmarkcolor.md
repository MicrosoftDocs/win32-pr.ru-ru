---
title: Сообщение LVM_GETINSERTMARKCOLOR (Коммктрл. h)
description: Извлекает цвет точки вставки.
ms.assetid: 1e98023a-9d26-4b87-bee4-bee4939ccfca
keywords:
- Элементы управления Windows для LVM_GETINSERTMARKCOLOR сообщений
topic_type:
- apiref
api_name:
- LVM_GETINSERTMARKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b18d6e9ed277f447f5097c0954819029d24b9cbb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137898"
---
# <a name="lvm_getinsertmarkcolor-message"></a><span data-ttu-id="44b69-104">\_Сообщение LVM жетинсертмаркколор</span><span class="sxs-lookup"><span data-stu-id="44b69-104">LVM\_GETINSERTMARKCOLOR message</span></span>

<span data-ttu-id="44b69-105">Извлекает цвет точки вставки.</span><span class="sxs-lookup"><span data-stu-id="44b69-105">Retrieves the color of the insertion point.</span></span>

## <a name="parameters"></a><span data-ttu-id="44b69-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="44b69-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44b69-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="44b69-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="44b69-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="44b69-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="44b69-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="44b69-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="44b69-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="44b69-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44b69-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="44b69-111">Return value</span></span>

<span data-ttu-id="44b69-112">Возвращает структуру **COLORREF** , содержащую цвет точки вставки.</span><span class="sxs-lookup"><span data-stu-id="44b69-112">Returns a **COLORREF** structure that contains the color of the insertion point.</span></span>

## <a name="remarks"></a><span data-ttu-id="44b69-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="44b69-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="44b69-114">Чтобы использовать это сообщение, необходимо указать манифест, указывающий Comclt32.dll версии 6,0.</span><span class="sxs-lookup"><span data-stu-id="44b69-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="44b69-115">Дополнительные сведения о манифестах см. в разделе [Включение визуальных стилей](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="44b69-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="44b69-116">Требования</span><span class="sxs-lookup"><span data-stu-id="44b69-116">Requirements</span></span>



| <span data-ttu-id="44b69-117">Требование</span><span class="sxs-lookup"><span data-stu-id="44b69-117">Requirement</span></span> | <span data-ttu-id="44b69-118">Значение</span><span class="sxs-lookup"><span data-stu-id="44b69-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="44b69-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="44b69-119">Minimum supported client</span></span><br/> | <span data-ttu-id="44b69-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="44b69-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="44b69-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="44b69-121">Minimum supported server</span></span><br/> | <span data-ttu-id="44b69-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="44b69-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="44b69-123">Header</span><span class="sxs-lookup"><span data-stu-id="44b69-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="44b69-124"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="44b69-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





