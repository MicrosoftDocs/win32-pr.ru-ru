---
title: Сообщение UDM_SETACCEL (Коммктрл. h)
description: Задает ускорение для элемента управления "вверх/вниз".
ms.assetid: af1d0a34-13ba-4bda-82f5-d7afab6bb1ed
keywords:
- Элементы управления Windows для UDM_SETACCEL сообщений
topic_type:
- apiref
api_name:
- UDM_SETACCEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b43ed290ce1668ffcaa9fb086a99ad52e5129ad6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104072021"
---
# <a name="udm_setaccel-message"></a><span data-ttu-id="74f85-104">\_Сообщение СЕТАКЦЕЛ UDM</span><span class="sxs-lookup"><span data-stu-id="74f85-104">UDM\_SETACCEL message</span></span>

<span data-ttu-id="74f85-105">Задает ускорение для элемента управления "вверх/вниз".</span><span class="sxs-lookup"><span data-stu-id="74f85-105">Sets the acceleration for an up-down control.</span></span>

## <a name="parameters"></a><span data-ttu-id="74f85-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="74f85-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74f85-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="74f85-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="74f85-108">Число структур [**удакцел**](/windows/desktop/api/Commctrl/ns-commctrl-udaccel) , заданных параметром *аакцелс*.</span><span class="sxs-lookup"><span data-stu-id="74f85-108">Number of [**UDACCEL**](/windows/desktop/api/Commctrl/ns-commctrl-udaccel) structures specified by *aAccels*.</span></span>

</dd> <dt>

<span data-ttu-id="74f85-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="74f85-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="74f85-110">Указатель на массив структур [**удакцел**](/windows/desktop/api/Commctrl/ns-commctrl-udaccel) , содержащих сведения об ускорении.</span><span class="sxs-lookup"><span data-stu-id="74f85-110">Pointer to an array of [**UDACCEL**](/windows/desktop/api/Commctrl/ns-commctrl-udaccel) structures that contain acceleration information.</span></span> <span data-ttu-id="74f85-111">Элементы должны быть отсортированы в порядке возрастания на основе элемента **NSEC** .</span><span class="sxs-lookup"><span data-stu-id="74f85-111">Elements should be sorted in ascending order based on the **nSec** member.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74f85-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="74f85-112">Return value</span></span>

<span data-ttu-id="74f85-113">Возвращает **значение true** , если успешно, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="74f85-113">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="74f85-114">Требования</span><span class="sxs-lookup"><span data-stu-id="74f85-114">Requirements</span></span>



| <span data-ttu-id="74f85-115">Требование</span><span class="sxs-lookup"><span data-stu-id="74f85-115">Requirement</span></span> | <span data-ttu-id="74f85-116">Значение</span><span class="sxs-lookup"><span data-stu-id="74f85-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="74f85-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="74f85-117">Minimum supported client</span></span><br/> | <span data-ttu-id="74f85-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="74f85-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="74f85-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="74f85-119">Minimum supported server</span></span><br/> | <span data-ttu-id="74f85-120">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="74f85-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="74f85-121">Header</span><span class="sxs-lookup"><span data-stu-id="74f85-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="74f85-122"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="74f85-122"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="74f85-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="74f85-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74f85-124">**\_UDM**</span><span class="sxs-lookup"><span data-stu-id="74f85-124">**UDM\_GETACCEL**</span></span>](udm-getaccel.md)
</dt> </dl>

 

 





