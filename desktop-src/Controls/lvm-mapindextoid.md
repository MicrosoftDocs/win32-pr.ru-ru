---
title: Сообщение LVM_MAPINDEXTOID (Коммктрл. h)
description: Сопоставляет индекс элемента с уникальным ИДЕНТИФИКАТОРом.
ms.assetid: d0486e21-2703-4289-abb0-f5f9c7b60b40
keywords:
- Элементы управления Windows для LVM_MAPINDEXTOID сообщений
topic_type:
- apiref
api_name:
- LVM_MAPINDEXTOID
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6a2a5de558b025e61bef26fd20278f125372769
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489981"
---
# <a name="lvm_mapindextoid-message"></a><span data-ttu-id="1e19a-104">\_Сообщение LVM мапиндекстоид</span><span class="sxs-lookup"><span data-stu-id="1e19a-104">LVM\_MAPINDEXTOID message</span></span>

<span data-ttu-id="1e19a-105">Сопоставляет индекс элемента с уникальным ИДЕНТИФИКАТОРом.</span><span class="sxs-lookup"><span data-stu-id="1e19a-105">Maps the index of an item to a unique ID.</span></span>

## <a name="parameters"></a><span data-ttu-id="1e19a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1e19a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e19a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1e19a-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1e19a-108">Индекс элемента.</span><span class="sxs-lookup"><span data-stu-id="1e19a-108">The index of an item.</span></span>

</dd> <dt>

<span data-ttu-id="1e19a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1e19a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1e19a-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="1e19a-110">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e19a-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1e19a-111">Return value</span></span>

<span data-ttu-id="1e19a-112">Возвращает уникальный идентификатор.</span><span class="sxs-lookup"><span data-stu-id="1e19a-112">Returns a unique ID.</span></span>

## <a name="remarks"></a><span data-ttu-id="1e19a-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1e19a-113">Remarks</span></span>

<span data-ttu-id="1e19a-114">Элементы управления "представление списка" внутренне отслеживание элементов по индексу.</span><span class="sxs-lookup"><span data-stu-id="1e19a-114">List-view controls internally track items by index.</span></span> <span data-ttu-id="1e19a-115">Это может представлять проблемы, так как индексы могут изменяться во время существования элемента управления.</span><span class="sxs-lookup"><span data-stu-id="1e19a-115">This can present problems because indexes can change during the control's lifetime.</span></span>

<span data-ttu-id="1e19a-116">Элемент управления "представление списка" может помечать элемент с ИДЕНТИФИКАТОРом при создании элемента.</span><span class="sxs-lookup"><span data-stu-id="1e19a-116">The list-view control can tag an item with an ID when the item is created.</span></span> <span data-ttu-id="1e19a-117">Этот идентификатор можно использовать для обеспечения уникальности во время существования элемента управления "представление списка".</span><span class="sxs-lookup"><span data-stu-id="1e19a-117">You can use this ID to guarantee uniqueness during the lifetime of the list-view control.</span></span>

<span data-ttu-id="1e19a-118">Чтобы однозначно идентифицировать элемент, возьмите индекс, возвращенный из вызова, например [**IComponent:: жетдисплайинфо**](/windows/desktop/api/mmc/nf-mmc-icomponent-getdisplayinfo) , и вызовите **LVM \_ мапиндекстоид**.</span><span class="sxs-lookup"><span data-stu-id="1e19a-118">To uniquely identify an item, take the index that is returned from a call such as [**IComponent::GetDisplayInfo**](/windows/desktop/api/mmc/nf-mmc-icomponent-getdisplayinfo) and call **LVM\_MAPINDEXTOID**.</span></span> <span data-ttu-id="1e19a-119">Возвращаемое значение является уникальным ИДЕНТИФИКАТОРом.</span><span class="sxs-lookup"><span data-stu-id="1e19a-119">The return value is a unique ID.</span></span>

> [!Note]  
> <span data-ttu-id="1e19a-120">В многопоточной среде индекс гарантированно гарантируется только в потоке, где размещается элемент управления "представление списка", а не в фоновых потоках.</span><span class="sxs-lookup"><span data-stu-id="1e19a-120">In a multithreaded environment, the index is only guaranteed on the thread that hosts the list-view control, not on background threads.</span></span>

 

> [!Note]  
> <span data-ttu-id="1e19a-121">Чтобы использовать это сообщение, необходимо указать манифест, указывающий Comclt32.dll версии 6,0.</span><span class="sxs-lookup"><span data-stu-id="1e19a-121">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="1e19a-122">Дополнительные сведения о манифестах см. в разделе [Включение визуальных стилей](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="1e19a-122">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="1e19a-123">Требования</span><span class="sxs-lookup"><span data-stu-id="1e19a-123">Requirements</span></span>



| <span data-ttu-id="1e19a-124">Требование</span><span class="sxs-lookup"><span data-stu-id="1e19a-124">Requirement</span></span> | <span data-ttu-id="1e19a-125">Значение</span><span class="sxs-lookup"><span data-stu-id="1e19a-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1e19a-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1e19a-126">Minimum supported client</span></span><br/> | <span data-ttu-id="1e19a-127">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1e19a-127">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1e19a-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1e19a-128">Minimum supported server</span></span><br/> | <span data-ttu-id="1e19a-129">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1e19a-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1e19a-130">Header</span><span class="sxs-lookup"><span data-stu-id="1e19a-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="1e19a-131"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="1e19a-131"><dt>Commctrl.h</dt></span></span> </dl> |



 

