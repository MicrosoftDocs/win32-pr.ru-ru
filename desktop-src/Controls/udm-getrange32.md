---
title: Сообщение UDM_GETRANGE32 (Коммктрл. h)
description: Извлекает 32-разрядный диапазон элемента управления "вверх/вниз".
ms.assetid: a94b50c9-cd2f-430d-875f-720e51f544f1
keywords:
- Элементы управления Windows для UDM_GETRANGE32 сообщений
topic_type:
- apiref
api_name:
- UDM_GETRANGE32
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca418cd08dc4c81b3ff734d74f3ca9deeef7d848
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490182"
---
# <a name="udm_getrange32-message"></a><span data-ttu-id="3e7c5-104">\_Сообщение GETRANGE32 UDM</span><span class="sxs-lookup"><span data-stu-id="3e7c5-104">UDM\_GETRANGE32 message</span></span>

<span data-ttu-id="3e7c5-105">Извлекает 32-разрядный диапазон элемента управления "вверх/вниз".</span><span class="sxs-lookup"><span data-stu-id="3e7c5-105">Retrieves the 32-bit range of an up-down control.</span></span>

## <a name="parameters"></a><span data-ttu-id="3e7c5-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3e7c5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e7c5-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3e7c5-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3e7c5-108">Указатель на целое число со знаком, которое получает нижнюю границу диапазона управления "вверх/вниз".</span><span class="sxs-lookup"><span data-stu-id="3e7c5-108">Pointer to a signed integer that receives the lower limit of the up-down control range.</span></span> <span data-ttu-id="3e7c5-109">Этот параметр может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="3e7c5-109">This parameter may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="3e7c5-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3e7c5-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3e7c5-111">Указатель на целое число со знаком, которое получает верхний предел диапазона управления "вверх/вниз".</span><span class="sxs-lookup"><span data-stu-id="3e7c5-111">Pointer to a signed integer that receives the upper limit of the up-down control range.</span></span> <span data-ttu-id="3e7c5-112">Этот параметр может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="3e7c5-112">This parameter may be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e7c5-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3e7c5-113">Return value</span></span>

<span data-ttu-id="3e7c5-114">Возвращаемое значение для этого сообщения не используется.</span><span class="sxs-lookup"><span data-stu-id="3e7c5-114">The return value for this message is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e7c5-115">Требования</span><span class="sxs-lookup"><span data-stu-id="3e7c5-115">Requirements</span></span>



| <span data-ttu-id="3e7c5-116">Требование</span><span class="sxs-lookup"><span data-stu-id="3e7c5-116">Requirement</span></span> | <span data-ttu-id="3e7c5-117">Значение</span><span class="sxs-lookup"><span data-stu-id="3e7c5-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3e7c5-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3e7c5-118">Minimum supported client</span></span><br/> | <span data-ttu-id="3e7c5-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3e7c5-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3e7c5-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3e7c5-120">Minimum supported server</span></span><br/> | <span data-ttu-id="3e7c5-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3e7c5-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3e7c5-122">Header</span><span class="sxs-lookup"><span data-stu-id="3e7c5-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e7c5-123"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="3e7c5-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





