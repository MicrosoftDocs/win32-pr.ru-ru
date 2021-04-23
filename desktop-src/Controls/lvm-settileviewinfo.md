---
title: Сообщение LVM_SETTILEVIEWINFO (Коммктрл. h)
description: Задает сведения, используемые элементом управления "представление списка" в мозаичном представлении.
ms.assetid: 1c4f2aff-1ce1-484a-9360-3efbe870b39b
keywords:
- Элементы управления Windows для LVM_SETTILEVIEWINFO сообщений
topic_type:
- apiref
api_name:
- LVM_SETTILEVIEWINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25d6c728d92bb931837eca440af679b5bcb98d1e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135586"
---
# <a name="lvm_settileviewinfo-message"></a><span data-ttu-id="ef1e3-104">\_Сообщение LVM сеттилевиевинфо</span><span class="sxs-lookup"><span data-stu-id="ef1e3-104">LVM\_SETTILEVIEWINFO message</span></span>

<span data-ttu-id="ef1e3-105">Задает сведения, используемые элементом управления "представление списка" в мозаичном представлении.</span><span class="sxs-lookup"><span data-stu-id="ef1e3-105">Sets information that a list-view control uses in tile view.</span></span>

## <a name="parameters"></a><span data-ttu-id="ef1e3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ef1e3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef1e3-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ef1e3-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="ef1e3-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="ef1e3-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="ef1e3-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ef1e3-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="ef1e3-110">Указатель на структуру <a href="/windows/win32/api/commctrl/ns-commctrl-lvtileviewinfo">**лвтилевиевинфо**</a> , содержащую сведения, которые необходимо задать.</span><span class="sxs-lookup"><span data-stu-id="ef1e3-110">Pointer to an <a href="/windows/win32/api/commctrl/ns-commctrl-lvtileviewinfo">**LVTILEVIEWINFO**</a> structure that contains the information to set.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef1e3-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ef1e3-111">Return value</span></span>

<span data-ttu-id="ef1e3-112">Возвращает **значение true** , если успешно, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="ef1e3-112">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="ef1e3-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ef1e3-113">Remarks</span></span>

<span data-ttu-id="ef1e3-114">Чтобы использовать это сообщение, необходимо указать манифест, указывающий Comclt32.dll версии 6,0.</span><span class="sxs-lookup"><span data-stu-id="ef1e3-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="ef1e3-115">Дополнительные сведения о манифестах см. в разделе [Включение визуальных стилей](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="ef1e3-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ef1e3-116">Требования</span><span class="sxs-lookup"><span data-stu-id="ef1e3-116">Requirements</span></span>



| <span data-ttu-id="ef1e3-117">Требование</span><span class="sxs-lookup"><span data-stu-id="ef1e3-117">Requirement</span></span> | <span data-ttu-id="ef1e3-118">Значение</span><span class="sxs-lookup"><span data-stu-id="ef1e3-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ef1e3-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ef1e3-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ef1e3-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ef1e3-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ef1e3-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ef1e3-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ef1e3-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ef1e3-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ef1e3-123">Header</span><span class="sxs-lookup"><span data-stu-id="ef1e3-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="ef1e3-124"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="ef1e3-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





