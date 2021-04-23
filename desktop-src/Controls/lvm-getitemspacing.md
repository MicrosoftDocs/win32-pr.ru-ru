---
title: Сообщение LVM_GETITEMSPACING (Коммктрл. h)
description: Определяет интервал между элементами в элементе управления "представление списка". Это сообщение можно отправить явно или с помощью \_ макроса ЖетитемспаЦинг ListView.
ms.assetid: 4e43fb43-468c-4b8a-9e3b-1694e90ffef8
keywords:
- Элементы управления Windows для LVM_GETITEMSPACING сообщений
topic_type:
- apiref
api_name:
- LVM_GETITEMSPACING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ea08a7fc1004ffb46d710da6d1c2a8b0fb18e57
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989177"
---
# <a name="lvm_getitemspacing-message"></a><span data-ttu-id="350ed-105">\_Сообщение LVM жетитемспаЦинг</span><span class="sxs-lookup"><span data-stu-id="350ed-105">LVM\_GETITEMSPACING message</span></span>

<span data-ttu-id="350ed-106">Определяет интервал между элементами в элементе управления "представление списка".</span><span class="sxs-lookup"><span data-stu-id="350ed-106">Determines the spacing between items in a list-view control.</span></span> <span data-ttu-id="350ed-107">Это сообщение можно отправить явно или с помощью макроса [**\_ жетитемспаЦинг ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemspacing) .</span><span class="sxs-lookup"><span data-stu-id="350ed-107">You can send this message explicitly or by using the [**ListView\_GetItemSpacing**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemspacing) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="350ed-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="350ed-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="350ed-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="350ed-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="350ed-110">Представление, для которого нужно получить сведения о промежутке между элементами.</span><span class="sxs-lookup"><span data-stu-id="350ed-110">View for which to retrieve the item spacing.</span></span> <span data-ttu-id="350ed-111">Этот параметр имеет **значение true** для представления небольшого значка или **значение false** для представления значков.</span><span class="sxs-lookup"><span data-stu-id="350ed-111">This parameter is **TRUE** for small icon view, or **FALSE** for icon view.</span></span>

</dd> <dt>

<span data-ttu-id="350ed-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="350ed-112">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="350ed-113">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="350ed-113">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="350ed-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="350ed-114">Return value</span></span>

<span data-ttu-id="350ed-115">Возвращает величину интервала между элементами.</span><span class="sxs-lookup"><span data-stu-id="350ed-115">Returns the amount of spacing between items.</span></span> <span data-ttu-id="350ed-116">Расстояние по горизонтали содержится в [**ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) , а вертикальное расстояние содержится в [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="350ed-116">The horizontal spacing is contained in the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) and the vertical spacing is contained in the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)).</span></span>

## <a name="requirements"></a><span data-ttu-id="350ed-117">Требования</span><span class="sxs-lookup"><span data-stu-id="350ed-117">Requirements</span></span>



| <span data-ttu-id="350ed-118">Требование</span><span class="sxs-lookup"><span data-stu-id="350ed-118">Requirement</span></span> | <span data-ttu-id="350ed-119">Значение</span><span class="sxs-lookup"><span data-stu-id="350ed-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="350ed-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="350ed-120">Minimum supported client</span></span><br/> | <span data-ttu-id="350ed-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="350ed-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="350ed-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="350ed-122">Minimum supported server</span></span><br/> | <span data-ttu-id="350ed-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="350ed-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="350ed-124">Header</span><span class="sxs-lookup"><span data-stu-id="350ed-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="350ed-125"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="350ed-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

