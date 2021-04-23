---
title: Сообщение UDM_GETACCEL (Коммктрл. h)
description: Получает сведения о ускорении для элемента управления "вверх/вниз".
ms.assetid: 794538d6-ca01-4f05-82d1-ce7bc0f76f64
keywords:
- Элементы управления Windows для UDM_GETACCEL сообщений
topic_type:
- apiref
api_name:
- UDM_GETACCEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b86a9740e59631b737453763a10ccb9820056d95
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489627"
---
# <a name="udm_getaccel-message"></a><span data-ttu-id="38d01-104">\_Сообщение о неполучении UDM</span><span class="sxs-lookup"><span data-stu-id="38d01-104">UDM\_GETACCEL message</span></span>

<span data-ttu-id="38d01-105">Получает сведения о ускорении для элемента управления "вверх/вниз".</span><span class="sxs-lookup"><span data-stu-id="38d01-105">Retrieves acceleration information for an up-down control.</span></span>

## <a name="parameters"></a><span data-ttu-id="38d01-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="38d01-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38d01-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="38d01-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="38d01-108">Число элементов в массиве, заданном параметром *lParam*.</span><span class="sxs-lookup"><span data-stu-id="38d01-108">Number of elements in the array specified by *lParam*.</span></span>

</dd> <dt>

<span data-ttu-id="38d01-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="38d01-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="38d01-110">Указатель на массив структур [**удакцел**](/windows/desktop/api/Commctrl/ns-commctrl-udaccel) , которые получают сведения о ускорении.</span><span class="sxs-lookup"><span data-stu-id="38d01-110">Pointer to an array of [**UDACCEL**](/windows/desktop/api/Commctrl/ns-commctrl-udaccel) structures that receive acceleration information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38d01-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="38d01-111">Return value</span></span>

<span data-ttu-id="38d01-112">Возвращаемое значение — это число ускорителей, установленных в данный момент для элемента управления.</span><span class="sxs-lookup"><span data-stu-id="38d01-112">The return value is the number of accelerators currently set for the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="38d01-113">Требования</span><span class="sxs-lookup"><span data-stu-id="38d01-113">Requirements</span></span>



| <span data-ttu-id="38d01-114">Требование</span><span class="sxs-lookup"><span data-stu-id="38d01-114">Requirement</span></span> | <span data-ttu-id="38d01-115">Значение</span><span class="sxs-lookup"><span data-stu-id="38d01-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="38d01-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="38d01-116">Minimum supported client</span></span><br/> | <span data-ttu-id="38d01-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="38d01-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="38d01-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="38d01-118">Minimum supported server</span></span><br/> | <span data-ttu-id="38d01-119">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="38d01-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="38d01-120">Header</span><span class="sxs-lookup"><span data-stu-id="38d01-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="38d01-121"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="38d01-121"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38d01-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="38d01-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38d01-123">**\_СЕТАКЦЕЛ UDM**</span><span class="sxs-lookup"><span data-stu-id="38d01-123">**UDM\_SETACCEL**</span></span>](udm-setaccel.md)
</dt> </dl>

 

 





