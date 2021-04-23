---
title: Сообщение IPM_ISBLANK (Коммктрл. h)
description: Определяет, являются ли все поля в элементе управления "IP-адрес" пустыми.
ms.assetid: 6e35b848-943a-4475-890a-01fc3d8ed97d
keywords:
- Элементы управления Windows для IPM_ISBLANK сообщений
topic_type:
- apiref
api_name:
- IPM_ISBLANK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19f5a33ee3c35779a02cdfcb0fcb7066098f3160
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892241"
---
# <a name="ipm_isblank-message"></a><span data-ttu-id="60e11-104">\_Сообщение IPM</span><span class="sxs-lookup"><span data-stu-id="60e11-104">IPM\_ISBLANK message</span></span>

<span data-ttu-id="60e11-105">Определяет, являются ли все поля в элементе управления "IP-адрес" пустыми.</span><span class="sxs-lookup"><span data-stu-id="60e11-105">Determines if all fields in the IP address control are blank.</span></span>

## <a name="parameters"></a><span data-ttu-id="60e11-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="60e11-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60e11-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="60e11-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="60e11-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="60e11-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="60e11-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="60e11-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="60e11-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="60e11-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60e11-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="60e11-111">Return value</span></span>

<span data-ttu-id="60e11-112">Возвращает ненулевое значение, если все поля пусты, или ноль в противном случае.</span><span class="sxs-lookup"><span data-stu-id="60e11-112">Returns nonzero if all fields are blank, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="60e11-113">Требования</span><span class="sxs-lookup"><span data-stu-id="60e11-113">Requirements</span></span>



| <span data-ttu-id="60e11-114">Требование</span><span class="sxs-lookup"><span data-stu-id="60e11-114">Requirement</span></span> | <span data-ttu-id="60e11-115">Значение</span><span class="sxs-lookup"><span data-stu-id="60e11-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="60e11-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="60e11-116">Minimum supported client</span></span><br/> | <span data-ttu-id="60e11-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="60e11-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="60e11-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="60e11-118">Minimum supported server</span></span><br/> | <span data-ttu-id="60e11-119">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="60e11-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="60e11-120">Header</span><span class="sxs-lookup"><span data-stu-id="60e11-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="60e11-121"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="60e11-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





