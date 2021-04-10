---
title: Сообщение LVM_ENABLEGROUPVIEW (Коммктрл. h)
description: Включает или отключает отображение элементов в элементе управления "представление списка" в виде группы.
ms.assetid: 783a5e23-d1cb-4523-a6d2-b2cf93fa7f62
keywords:
- Элементы управления Windows для LVM_ENABLEGROUPVIEW сообщений
topic_type:
- apiref
api_name:
- LVM_ENABLEGROUPVIEW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1d546e1236fa4f0800c0353810beb5b427ba4fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071128"
---
# <a name="lvm_enablegroupview-message"></a><span data-ttu-id="a26aa-104">\_Сообщение LVM енаблеграупвиев</span><span class="sxs-lookup"><span data-stu-id="a26aa-104">LVM\_ENABLEGROUPVIEW message</span></span>

<span data-ttu-id="a26aa-105">Включает или отключает отображение элементов в элементе управления "представление списка" в виде группы.</span><span class="sxs-lookup"><span data-stu-id="a26aa-105">Enables or disables whether the items in a list-view control display as a group.</span></span>

## <a name="parameters"></a><span data-ttu-id="a26aa-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a26aa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a26aa-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a26aa-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="a26aa-108">**Логическое** значение, указывающее, следует ли включить элемент управления "представление списка" для группирования отображаемых элементов.</span><span class="sxs-lookup"><span data-stu-id="a26aa-108">A **BOOL** that indicates whether to enable a list-view control to group displayed items.</span></span> <span data-ttu-id="a26aa-109">Чтобы включить группирование, используйте **значение true** , а для отключения — **значение false** .</span><span class="sxs-lookup"><span data-stu-id="a26aa-109">Use **TRUE** to enable grouping, **FALSE** to disable it.</span></span> </dd> <dt>

<span data-ttu-id="a26aa-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a26aa-110">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="a26aa-111">Должен иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="a26aa-111">Must be **NULL**.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a26aa-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a26aa-112">Return value</span></span>

<span data-ttu-id="a26aa-113">Возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="a26aa-113">Returns one of the following values.</span></span>



| <span data-ttu-id="a26aa-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="a26aa-114">Return code</span></span>                                                                       | <span data-ttu-id="a26aa-115">Описание</span><span class="sxs-lookup"><span data-stu-id="a26aa-115">Description</span></span>                                                                                  |
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a26aa-116"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="a26aa-116"><dt>**0**</dt></span></span> </dl>  | <span data-ttu-id="a26aa-117">Возможность отображения элементов списка в виде группы уже включена или отключена.</span><span class="sxs-lookup"><span data-stu-id="a26aa-117">The ability to display list-view items as a group is already enabled or disabled.</span></span><br/> |
| <dl> <span data-ttu-id="a26aa-118"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="a26aa-118"><dt>**1**</dt></span></span> </dl>  | <span data-ttu-id="a26aa-119">Состояние элемента управления успешно изменено.</span><span class="sxs-lookup"><span data-stu-id="a26aa-119">The state of the control was successfully changed.</span></span><br/>                                |
| <dl> <span data-ttu-id="a26aa-120"><dt>**-1**</dt></span><span class="sxs-lookup"><span data-stu-id="a26aa-120"><dt>**-1**</dt></span></span> </dl> | <span data-ttu-id="a26aa-121">Операция не удалась.</span><span class="sxs-lookup"><span data-stu-id="a26aa-121">The operation failed.</span></span><br/>                                                             |



 

## <a name="remarks"></a><span data-ttu-id="a26aa-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a26aa-122">Remarks</span></span>

<span data-ttu-id="a26aa-123">**LVM \_ ЕНАБЛЕГРАУПВИЕВ** не поддерживается в стиле [**LVS \_ овнердата**](list-view-window-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="a26aa-123">**LVM\_ENABLEGROUPVIEW** is not supported under the [**LVS\_OWNERDATA**](list-view-window-styles.md) style.</span></span>

> [!Note]  
> <span data-ttu-id="a26aa-124">Чтобы использовать это сообщение, необходимо указать манифест, указывающий Comclt32.dll версии 6,0.</span><span class="sxs-lookup"><span data-stu-id="a26aa-124">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="a26aa-125">Дополнительные сведения о манифестах см. в разделе [Включение визуальных стилей](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="a26aa-125">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a26aa-126">Требования</span><span class="sxs-lookup"><span data-stu-id="a26aa-126">Requirements</span></span>



| <span data-ttu-id="a26aa-127">Требование</span><span class="sxs-lookup"><span data-stu-id="a26aa-127">Requirement</span></span> | <span data-ttu-id="a26aa-128">Значение</span><span class="sxs-lookup"><span data-stu-id="a26aa-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a26aa-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a26aa-129">Minimum supported client</span></span><br/> | <span data-ttu-id="a26aa-130">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a26aa-130">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a26aa-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a26aa-131">Minimum supported server</span></span><br/> | <span data-ttu-id="a26aa-132">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a26aa-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a26aa-133">Header</span><span class="sxs-lookup"><span data-stu-id="a26aa-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="a26aa-134"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="a26aa-134"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





