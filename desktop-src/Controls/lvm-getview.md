---
title: Сообщение LVM_GETVIEW (Коммктрл. h)
description: Извлекает текущее представление элемента управления "представление списка".
ms.assetid: dd63e726-3a7f-40e7-8d46-4680816c02a3
keywords:
- Элементы управления Windows для LVM_GETVIEW сообщений
topic_type:
- apiref
api_name:
- LVM_GETVIEW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2da295fa5a5b335de60169ce06b777d9e355121
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137102"
---
# <a name="lvm_getview-message"></a><span data-ttu-id="622e2-104">\_Сообщение LVM</span><span class="sxs-lookup"><span data-stu-id="622e2-104">LVM\_GETVIEW message</span></span>

<span data-ttu-id="622e2-105">Извлекает текущее представление элемента управления "представление списка".</span><span class="sxs-lookup"><span data-stu-id="622e2-105">Retrieves the current view of a list-view control.</span></span>

## <a name="parameters"></a><span data-ttu-id="622e2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="622e2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="622e2-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="622e2-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="622e2-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="622e2-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="622e2-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="622e2-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="622e2-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="622e2-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="622e2-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="622e2-111">Return value</span></span>

<span data-ttu-id="622e2-112">Возвращает значение **типа DWORD** , указывающее текущее представление.</span><span class="sxs-lookup"><span data-stu-id="622e2-112">Returns a **DWORD** that specifies the current view.</span></span>

## <a name="remarks"></a><span data-ttu-id="622e2-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="622e2-113">Remarks</span></span>

<span data-ttu-id="622e2-114">Ниже приведены значения для представлений.</span><span class="sxs-lookup"><span data-stu-id="622e2-114">Following are the values for views.</span></span>

-   <span data-ttu-id="622e2-115">\_ \_ сведения о представлении LV</span><span class="sxs-lookup"><span data-stu-id="622e2-115">LV\_VIEW\_DETAILS</span></span>
-   <span data-ttu-id="622e2-116">\_значок представления "Латвия" \_</span><span class="sxs-lookup"><span data-stu-id="622e2-116">LV\_VIEW\_ICON</span></span>
-   <span data-ttu-id="622e2-117">\_список ПРЕДСТАВЛЕНИЙ \_ LV</span><span class="sxs-lookup"><span data-stu-id="622e2-117">LV\_VIEW\_LIST</span></span>
-   <span data-ttu-id="622e2-118">\_представление LV \_ маленькие значки</span><span class="sxs-lookup"><span data-stu-id="622e2-118">LV\_VIEW\_SMALLICON</span></span>
-   <span data-ttu-id="622e2-119">\_плитка представления "Латвия" \_</span><span class="sxs-lookup"><span data-stu-id="622e2-119">LV\_VIEW\_TILE</span></span>

> [!Note]  
> <span data-ttu-id="622e2-120">Чтобы использовать это сообщение, необходимо указать манифест, указывающий Comclt32.dll версии 6,0.</span><span class="sxs-lookup"><span data-stu-id="622e2-120">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="622e2-121">Дополнительные сведения о манифестах см. в разделе [Включение визуальных стилей](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="622e2-121">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="622e2-122">Требования</span><span class="sxs-lookup"><span data-stu-id="622e2-122">Requirements</span></span>



| <span data-ttu-id="622e2-123">Требование</span><span class="sxs-lookup"><span data-stu-id="622e2-123">Requirement</span></span> | <span data-ttu-id="622e2-124">Значение</span><span class="sxs-lookup"><span data-stu-id="622e2-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="622e2-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="622e2-125">Minimum supported client</span></span><br/> | <span data-ttu-id="622e2-126">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="622e2-126">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="622e2-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="622e2-127">Minimum supported server</span></span><br/> | <span data-ttu-id="622e2-128">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="622e2-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="622e2-129">Header</span><span class="sxs-lookup"><span data-stu-id="622e2-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="622e2-130"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="622e2-130"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





