---
title: Сообщение LVM_SETVIEW (Коммктрл. h)
description: Задает представление элемента управления "представление списка".
ms.assetid: e6d3f16d-52ea-4863-a6c9-9a085d5f794a
keywords:
- Элементы управления Windows для LVM_SETVIEW сообщений
topic_type:
- apiref
api_name:
- LVM_SETVIEW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a159710b3086bcba5298a5a88f9cab15f76e0d89
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137087"
---
# <a name="lvm_setview-message"></a><span data-ttu-id="dd215-104">\_Сообщение LVM сетвиев</span><span class="sxs-lookup"><span data-stu-id="dd215-104">LVM\_SETVIEW message</span></span>

<span data-ttu-id="dd215-105">Задает представление элемента управления "представление списка".</span><span class="sxs-lookup"><span data-stu-id="dd215-105">Sets the view of a list-view control.</span></span>

## <a name="parameters"></a><span data-ttu-id="dd215-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="dd215-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd215-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="dd215-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="dd215-108">Значение **типа DWORD** , указывающее представление.</span><span class="sxs-lookup"><span data-stu-id="dd215-108">**DWORD** that specifies the view.</span></span></dd> <dt>

<span data-ttu-id="dd215-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="dd215-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="dd215-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="dd215-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dd215-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dd215-111">Return value</span></span>

<span data-ttu-id="dd215-112">Возвращает 1, если успешно, или-1 в противном случае.</span><span class="sxs-lookup"><span data-stu-id="dd215-112">Returns 1 if successful, or -1 otherwise.</span></span> <span data-ttu-id="dd215-113">Например, если представление недопустимо, возвращается значение-1.</span><span class="sxs-lookup"><span data-stu-id="dd215-113">For example, -1 is returned if the view is invalid.</span></span>

## <a name="remarks"></a><span data-ttu-id="dd215-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dd215-114">Remarks</span></span>

<span data-ttu-id="dd215-115">Ниже приведены значения для представлений.</span><span class="sxs-lookup"><span data-stu-id="dd215-115">Following are the values for views.</span></span>

-   <span data-ttu-id="dd215-116">\_ \_ сведения о представлении LV</span><span class="sxs-lookup"><span data-stu-id="dd215-116">LV\_VIEW\_DETAILS</span></span>
-   <span data-ttu-id="dd215-117">\_значок представления "Латвия" \_</span><span class="sxs-lookup"><span data-stu-id="dd215-117">LV\_VIEW\_ICON</span></span>
-   <span data-ttu-id="dd215-118">\_список ПРЕДСТАВЛЕНИЙ \_ LV</span><span class="sxs-lookup"><span data-stu-id="dd215-118">LV\_VIEW\_LIST</span></span>
-   <span data-ttu-id="dd215-119">\_представление LV \_ маленькие значки</span><span class="sxs-lookup"><span data-stu-id="dd215-119">LV\_VIEW\_SMALLICON</span></span>
-   <span data-ttu-id="dd215-120">\_плитка представления "Латвия" \_</span><span class="sxs-lookup"><span data-stu-id="dd215-120">LV\_VIEW\_TILE</span></span>

> [!Note]  
> <span data-ttu-id="dd215-121">Чтобы использовать это сообщение, необходимо указать манифест, указывающий Comctl32.dll версии 6,0.</span><span class="sxs-lookup"><span data-stu-id="dd215-121">To use this message, you must provide a manifest specifying Comctl32.dll version 6.0.</span></span> <span data-ttu-id="dd215-122">Дополнительные сведения о манифестах см. в разделе [Включение визуальных стилей](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="dd215-122">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="dd215-123">Требования</span><span class="sxs-lookup"><span data-stu-id="dd215-123">Requirements</span></span>



| <span data-ttu-id="dd215-124">Требование</span><span class="sxs-lookup"><span data-stu-id="dd215-124">Requirement</span></span> | <span data-ttu-id="dd215-125">Значение</span><span class="sxs-lookup"><span data-stu-id="dd215-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dd215-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dd215-126">Minimum supported client</span></span><br/> | <span data-ttu-id="dd215-127">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="dd215-127">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="dd215-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dd215-128">Minimum supported server</span></span><br/> | <span data-ttu-id="dd215-129">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="dd215-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="dd215-130">Header</span><span class="sxs-lookup"><span data-stu-id="dd215-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="dd215-131"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="dd215-131"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





