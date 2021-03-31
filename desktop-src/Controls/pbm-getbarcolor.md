---
title: Сообщение PBM_GETBARCOLOR (Коммктрл. h)
description: Возвращает цвет индикатора выполнения.
ms.assetid: d046f7e4-e21e-4dd9-a7be-2bf820c3c492
keywords:
- Элементы управления Windows для PBM_GETBARCOLOR сообщений
topic_type:
- apiref
api_name:
- PBM_GETBARCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35586d3483d1d487f740a1a3d991c884c814f452
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136646"
---
# <a name="pbm_getbarcolor-message"></a><span data-ttu-id="8ba9d-104">\_Сообщение ЖЕТБАРКОЛОР PBM</span><span class="sxs-lookup"><span data-stu-id="8ba9d-104">PBM\_GETBARCOLOR message</span></span>

<span data-ttu-id="8ba9d-105">Возвращает цвет индикатора выполнения.</span><span class="sxs-lookup"><span data-stu-id="8ba9d-105">Gets the color of the progress bar.</span></span>

## <a name="parameters"></a><span data-ttu-id="8ba9d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8ba9d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ba9d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8ba9d-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="8ba9d-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="8ba9d-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="8ba9d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8ba9d-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="8ba9d-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="8ba9d-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ba9d-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8ba9d-111">Return value</span></span>

<span data-ttu-id="8ba9d-112">Возвращает цвет индикатора выполнения.</span><span class="sxs-lookup"><span data-stu-id="8ba9d-112">Returns the color of the progress bar.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ba9d-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8ba9d-113">Remarks</span></span>

<span data-ttu-id="8ba9d-114">Это цвет, заданный в сообщении [**\_ сетбарколор PBM**](pbm-setbarcolor.md) .</span><span class="sxs-lookup"><span data-stu-id="8ba9d-114">This is the color set by the [**PBM\_SETBARCOLOR**](pbm-setbarcolor.md) message.</span></span> <span data-ttu-id="8ba9d-115">Значение по умолчанию — CLR \_ по умолчанию, которое определено в коммктрл. h.</span><span class="sxs-lookup"><span data-stu-id="8ba9d-115">The default value is CLR\_DEFAULT, which is defined in commctrl.h.</span></span>

<span data-ttu-id="8ba9d-116">Эта функция влияет только на классический режим, а не на визуальный стиль.</span><span class="sxs-lookup"><span data-stu-id="8ba9d-116">This function only affects the classic mode, not any visual style.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ba9d-117">Требования</span><span class="sxs-lookup"><span data-stu-id="8ba9d-117">Requirements</span></span>



| <span data-ttu-id="8ba9d-118">Требование</span><span class="sxs-lookup"><span data-stu-id="8ba9d-118">Requirement</span></span> | <span data-ttu-id="8ba9d-119">Значение</span><span class="sxs-lookup"><span data-stu-id="8ba9d-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8ba9d-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8ba9d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="8ba9d-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8ba9d-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8ba9d-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8ba9d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="8ba9d-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8ba9d-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8ba9d-124">Header</span><span class="sxs-lookup"><span data-stu-id="8ba9d-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="8ba9d-125"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="8ba9d-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





