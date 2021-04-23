---
title: Сообщение LVM_SETIMAGELIST (Коммктрл. h)
description: Присваивает список изображений элементу управления "представление списка". Это сообщение можно отправить явно или с помощью \_ макроса Сетимажелист ListView.
ms.assetid: 5241065b-85e4-412e-9868-fd5b15ff7c17
keywords:
- Элементы управления Windows для LVM_SETIMAGELIST сообщений
topic_type:
- apiref
api_name:
- LVM_SETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 779d31fd781a72dbdfbc4738e091482ca4a08528
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988197"
---
# <a name="lvm_setimagelist-message"></a><span data-ttu-id="3f384-105">\_Сообщение LVM сетимажелист</span><span class="sxs-lookup"><span data-stu-id="3f384-105">LVM\_SETIMAGELIST message</span></span>

<span data-ttu-id="3f384-106">Присваивает список изображений элементу управления "представление списка".</span><span class="sxs-lookup"><span data-stu-id="3f384-106">Assigns an image list to a list-view control.</span></span> <span data-ttu-id="3f384-107">Это сообщение можно отправить явно или с помощью макроса [**\_ сетимажелист ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setimagelist) .</span><span class="sxs-lookup"><span data-stu-id="3f384-107">You can send this message explicitly or by using the [**ListView\_SetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setimagelist) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="3f384-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="3f384-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f384-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3f384-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3f384-110">Тип списка изображений.</span><span class="sxs-lookup"><span data-stu-id="3f384-110">Type of image list.</span></span> <span data-ttu-id="3f384-111">Этот параметр может принимать одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="3f384-111">This parameter can be one of the following values:</span></span>



| <span data-ttu-id="3f384-112">Значение</span><span class="sxs-lookup"><span data-stu-id="3f384-112">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="3f384-113">Значение</span><span class="sxs-lookup"><span data-stu-id="3f384-113">Meaning</span></span>                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| <span id="LVSIL_NORMAL"></span><span id="lvsil_normal"></span><dl> <span data-ttu-id="3f384-114"><dt>**ЛВСИЛ, \_ Обычная**</dt></span><span class="sxs-lookup"><span data-stu-id="3f384-114"><dt>**LVSIL\_NORMAL**</dt></span></span> </dl>                | <span data-ttu-id="3f384-115">Список изображений с большими значками.</span><span class="sxs-lookup"><span data-stu-id="3f384-115">Image list with large icons.</span></span><br/>  |
| <span id="LVSIL_SMALL"></span><span id="lvsil_small"></span><dl> <span data-ttu-id="3f384-116"><dt>**ЛВСИЛ \_ малый**</dt></span><span class="sxs-lookup"><span data-stu-id="3f384-116"><dt>**LVSIL\_SMALL**</dt></span></span> </dl>                   | <span data-ttu-id="3f384-117">Список изображений с мелкими значками.</span><span class="sxs-lookup"><span data-stu-id="3f384-117">Image list with small icons.</span></span><br/>  |
| <span id="LVSIL_STATE"></span><span id="lvsil_state"></span><dl> <span data-ttu-id="3f384-118"><dt>**\_состояние лвсил**</dt></span><span class="sxs-lookup"><span data-stu-id="3f384-118"><dt>**LVSIL\_STATE**</dt></span></span> </dl>                   | <span data-ttu-id="3f384-119">Список изображений с изображениями состояний.</span><span class="sxs-lookup"><span data-stu-id="3f384-119">Image list with state images.</span></span><br/> |
| <span id="LVSIL_GROUPHEADER"></span><span id="lvsil_groupheader"></span><dl> <span data-ttu-id="3f384-120"><dt>**ЛВСИЛ \_ грауфеадер**</dt></span><span class="sxs-lookup"><span data-stu-id="3f384-120"><dt>**LVSIL\_GROUPHEADER**</dt></span></span> </dl> | <span data-ttu-id="3f384-121">Список изображений для заголовка группы.</span><span class="sxs-lookup"><span data-stu-id="3f384-121">Image list for group header.</span></span><br/>  |



 

</dd> <dt>

<span data-ttu-id="3f384-122">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3f384-122">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3f384-123">Обработчик списка изображений для назначения.</span><span class="sxs-lookup"><span data-stu-id="3f384-123">Handle to the image list to assign.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f384-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3f384-124">Return value</span></span>

<span data-ttu-id="3f384-125">Возвращает маркер для списка изображений, который ранее был связан с элементом управления в случае успеха, или **значение NULL** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="3f384-125">Returns the handle to the image list previously associated with the control if successful, or **NULL** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="3f384-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3f384-126">Remarks</span></span>

<span data-ttu-id="3f384-127">Текущий список изображений будет уничтожен при уничтожении элемента управления "список-представление", если не задан стиль [**LVS \_ шареимажелистс**](list-view-window-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="3f384-127">The current image list will be destroyed when the list-view control is destroyed unless the [**LVS\_SHAREIMAGELISTS**](list-view-window-styles.md) style is set.</span></span> <span data-ttu-id="3f384-128">Если вы используете это сообщение для замены одного списка изображений другим, приложение должно явным образом уничтожить все списки изображений, кроме текущего.</span><span class="sxs-lookup"><span data-stu-id="3f384-128">If you use this message to replace one image list with another, your application must explicitly destroy all image lists other than the current one.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f384-129">Требования</span><span class="sxs-lookup"><span data-stu-id="3f384-129">Requirements</span></span>



| <span data-ttu-id="3f384-130">Требование</span><span class="sxs-lookup"><span data-stu-id="3f384-130">Requirement</span></span> | <span data-ttu-id="3f384-131">Значение</span><span class="sxs-lookup"><span data-stu-id="3f384-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3f384-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3f384-132">Minimum supported client</span></span><br/> | <span data-ttu-id="3f384-133">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3f384-133">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3f384-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3f384-134">Minimum supported server</span></span><br/> | <span data-ttu-id="3f384-135">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3f384-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3f384-136">Header</span><span class="sxs-lookup"><span data-stu-id="3f384-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="3f384-137"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="3f384-137"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





