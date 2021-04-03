---
title: Сообщение SB_ISSIMPLE (Коммктрл. h)
description: Проверяет, находится ли элемент управления "строка состояния" в простом режиме.
ms.assetid: f4362bc3-1852-4569-af9b-96d2da4f0606
keywords:
- Элементы управления Windows для SB_ISSIMPLE сообщений
topic_type:
- apiref
api_name:
- SB_ISSIMPLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71a5c523bef45065b103051962d7f147816c505d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136830"
---
# <a name="sb_issimple-message"></a><span data-ttu-id="5e824-104">\_Непростое сообщение SB</span><span class="sxs-lookup"><span data-stu-id="5e824-104">SB\_ISSIMPLE message</span></span>

<span data-ttu-id="5e824-105">Проверяет, находится ли элемент управления "строка состояния" в простом режиме.</span><span class="sxs-lookup"><span data-stu-id="5e824-105">Checks a status bar control to determine if it is in simple mode.</span></span>

## <a name="parameters"></a><span data-ttu-id="5e824-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5e824-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e824-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5e824-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="5e824-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="5e824-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="5e824-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5e824-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="5e824-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="5e824-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e824-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5e824-111">Return value</span></span>

<span data-ttu-id="5e824-112">Возвращает ненулевое значение, если элемент управления "строка состояния" находится в простом режиме, или ноль в противном случае.</span><span class="sxs-lookup"><span data-stu-id="5e824-112">Returns nonzero if the status bar control is in simple mode, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e824-113">Требования</span><span class="sxs-lookup"><span data-stu-id="5e824-113">Requirements</span></span>



| <span data-ttu-id="5e824-114">Требование</span><span class="sxs-lookup"><span data-stu-id="5e824-114">Requirement</span></span> | <span data-ttu-id="5e824-115">Значение</span><span class="sxs-lookup"><span data-stu-id="5e824-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5e824-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5e824-116">Minimum supported client</span></span><br/> | <span data-ttu-id="5e824-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5e824-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5e824-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5e824-118">Minimum supported server</span></span><br/> | <span data-ttu-id="5e824-119">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="5e824-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5e824-120">Header</span><span class="sxs-lookup"><span data-stu-id="5e824-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="5e824-121"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="5e824-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





