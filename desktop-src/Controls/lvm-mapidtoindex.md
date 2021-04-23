---
title: Сообщение LVM_MAPIDTOINDEX (Коммктрл. h)
description: Сопоставляет идентификатор элемента с индексом.
ms.assetid: vs|controls|~\controls\listview\messages\lvm_mapidtoindex.htm
keywords:
- Элементы управления Windows для LVM_MAPIDTOINDEX сообщений
topic_type:
- apiref
api_name:
- LVM_MAPIDTOINDEX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb4cb8aa49b37186ef689ed8cb319bbb92b62d75
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654635"
---
# <a name="lvm_mapidtoindex-message"></a><span data-ttu-id="fe8dd-104">\_Сообщение LVM мапидтоиндекс</span><span class="sxs-lookup"><span data-stu-id="fe8dd-104">LVM\_MAPIDTOINDEX message</span></span>

<span data-ttu-id="fe8dd-105">Сопоставляет идентификатор элемента с индексом.</span><span class="sxs-lookup"><span data-stu-id="fe8dd-105">Maps the ID of an item to an index.</span></span>

## <a name="parameters"></a><span data-ttu-id="fe8dd-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="fe8dd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe8dd-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fe8dd-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fe8dd-108">Уникальный идентификатор элемента.</span><span class="sxs-lookup"><span data-stu-id="fe8dd-108">The unique ID of an item.</span></span>

</dd> <dt>

<span data-ttu-id="fe8dd-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fe8dd-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fe8dd-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="fe8dd-110">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe8dd-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fe8dd-111">Return value</span></span>

<span data-ttu-id="fe8dd-112">Возвращает самый текущий индекс.</span><span class="sxs-lookup"><span data-stu-id="fe8dd-112">Returns the most current index.</span></span>

## <a name="remarks"></a><span data-ttu-id="fe8dd-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fe8dd-113">Remarks</span></span>

<span data-ttu-id="fe8dd-114">Элементы управления "представление списка" внутренне отслеживание элементов по индексу.</span><span class="sxs-lookup"><span data-stu-id="fe8dd-114">List-view controls internally track items by index.</span></span> <span data-ttu-id="fe8dd-115">Это может представлять проблемы, так как индексы могут изменяться во время существования элемента управления.</span><span class="sxs-lookup"><span data-stu-id="fe8dd-115">This can present problems because indexes can change during the control's lifetime.</span></span>

<span data-ttu-id="fe8dd-116">Элемент управления "представление списка" может помечать элемент с ИДЕНТИФИКАТОРом при создании элемента.</span><span class="sxs-lookup"><span data-stu-id="fe8dd-116">The list-view control can tag an item with an ID when the item is created.</span></span> <span data-ttu-id="fe8dd-117">Этот идентификатор можно использовать для обеспечения уникальности во время существования элемента управления "представление списка".</span><span class="sxs-lookup"><span data-stu-id="fe8dd-117">You can use this ID to guarantee uniqueness during the lifetime of the list-view control.</span></span>

<span data-ttu-id="fe8dd-118">Чтобы однозначно идентифицировать элемент, возьмите индекс, возвращенный из вызова, например [**IComponent:: жетдисплайинфо**](/windows/desktop/api/mmc/nf-mmc-icomponent-getdisplayinfo) , и вызовите [**LVM \_ мапиндекстоид**](lvm-mapindextoid.md).</span><span class="sxs-lookup"><span data-stu-id="fe8dd-118">To uniquely identify an item, take the index that is returned from a call such as [**IComponent::GetDisplayInfo**](/windows/desktop/api/mmc/nf-mmc-icomponent-getdisplayinfo) and call [**LVM\_MAPINDEXTOID**](lvm-mapindextoid.md).</span></span> <span data-ttu-id="fe8dd-119">Возвращаемое значение является уникальным ИДЕНТИФИКАТОРом.</span><span class="sxs-lookup"><span data-stu-id="fe8dd-119">The return value is a unique ID.</span></span>

<span data-ttu-id="fe8dd-120">Если требуется индекс элемента после создания идентификатора, можно вызвать **LVM \_ мапидтоиндекс** с уникальным идентификатором и возвратить самый актуальный индекс.</span><span class="sxs-lookup"><span data-stu-id="fe8dd-120">If you need the index of an item after an ID is created you can call **LVM\_MAPIDTOINDEX** with the unique ID and it returns the most current index.</span></span>

<span data-ttu-id="fe8dd-121">**LVM \_ МАПИДТОИНДЕКС** не поддерживается в стиле [**LVS \_ овнердата**](list-view-window-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="fe8dd-121">**LVM\_MAPIDTOINDEX** is not supported under the [**LVS\_OWNERDATA**](list-view-window-styles.md) style.</span></span>

> [!Note]  
> <span data-ttu-id="fe8dd-122">В многопоточной среде индекс гарантированно гарантируется только в потоке, где размещается элемент управления "представление списка", а не в фоновых потоках.</span><span class="sxs-lookup"><span data-stu-id="fe8dd-122">In a multithreaded environment, the index is only guaranteed on the thread that hosts the list-view control, not on background threads.</span></span>

 

> [!Note]  
> <span data-ttu-id="fe8dd-123">Чтобы использовать это сообщение, необходимо указать манифест, указывающий Comclt32.dll версии 6,0.</span><span class="sxs-lookup"><span data-stu-id="fe8dd-123">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="fe8dd-124">Дополнительные сведения о манифестах см. в разделе [Включение визуальных стилей](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="fe8dd-124">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="fe8dd-125">Требования</span><span class="sxs-lookup"><span data-stu-id="fe8dd-125">Requirements</span></span>



| <span data-ttu-id="fe8dd-126">Требование</span><span class="sxs-lookup"><span data-stu-id="fe8dd-126">Requirement</span></span> | <span data-ttu-id="fe8dd-127">Значение</span><span class="sxs-lookup"><span data-stu-id="fe8dd-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fe8dd-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fe8dd-128">Minimum supported client</span></span><br/> | <span data-ttu-id="fe8dd-129">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fe8dd-129">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fe8dd-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fe8dd-130">Minimum supported server</span></span><br/> | <span data-ttu-id="fe8dd-131">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="fe8dd-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fe8dd-132">Header</span><span class="sxs-lookup"><span data-stu-id="fe8dd-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="fe8dd-133"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="fe8dd-133"><dt>Commctrl.h</dt></span></span> </dl> |



 

