---
title: Сообщение LVM_GETIMAGELIST (Коммктрл. h)
description: Получает маркер для списка изображений, используемого для отображения элементов списка. Это сообщение можно отправить явным образом или с помощью \_ макроса ListView.
ms.assetid: dd48d8b5-6dbd-48ab-95c3-0fcf1e8c24f0
keywords:
- Элементы управления Windows для LVM_GETIMAGELIST сообщений
topic_type:
- apiref
api_name:
- LVM_GETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0abc68c5e5dd9a18c3ec203ad7fe3db97a542845
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136414"
---
# <a name="lvm_getimagelist-message"></a><span data-ttu-id="f0825-105">Сообщение LVM/ \_ ImageList</span><span class="sxs-lookup"><span data-stu-id="f0825-105">LVM\_GETIMAGELIST message</span></span>

<span data-ttu-id="f0825-106">Получает маркер для списка изображений, используемого для отображения элементов списка.</span><span class="sxs-lookup"><span data-stu-id="f0825-106">Retrieves the handle to an image list used for drawing list-view items.</span></span> <span data-ttu-id="f0825-107">Это сообщение можно отправить явным образом или с помощью макроса [**ListView \_**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getimagelist) .</span><span class="sxs-lookup"><span data-stu-id="f0825-107">You can send this message explicitly or by using the [**ListView\_GetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getimagelist) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="f0825-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="f0825-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0825-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f0825-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f0825-110">Список изображений для извлечения.</span><span class="sxs-lookup"><span data-stu-id="f0825-110">Image list to retrieve.</span></span> <span data-ttu-id="f0825-111">Этот параметр может принимать одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="f0825-111">This parameter can be one of the following values:</span></span>



| <span data-ttu-id="f0825-112">Значение</span><span class="sxs-lookup"><span data-stu-id="f0825-112">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="f0825-113">Значение</span><span class="sxs-lookup"><span data-stu-id="f0825-113">Meaning</span></span>                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| <span id="LVSIL_NORMAL"></span><span id="lvsil_normal"></span><dl> <span data-ttu-id="f0825-114"><dt>**ЛВСИЛ, \_ Обычная**</dt></span><span class="sxs-lookup"><span data-stu-id="f0825-114"><dt>**LVSIL\_NORMAL**</dt></span></span> </dl>                | <span data-ttu-id="f0825-115">Список изображений с большими значками.</span><span class="sxs-lookup"><span data-stu-id="f0825-115">Image list with large icons.</span></span><br/>  |
| <span id="LVSIL_SMALL"></span><span id="lvsil_small"></span><dl> <span data-ttu-id="f0825-116"><dt>**ЛВСИЛ \_ малый**</dt></span><span class="sxs-lookup"><span data-stu-id="f0825-116"><dt>**LVSIL\_SMALL**</dt></span></span> </dl>                   | <span data-ttu-id="f0825-117">Список изображений с мелкими значками.</span><span class="sxs-lookup"><span data-stu-id="f0825-117">Image list with small icons.</span></span><br/>  |
| <span id="LVSIL_STATE"></span><span id="lvsil_state"></span><dl> <span data-ttu-id="f0825-118"><dt>**\_состояние лвсил**</dt></span><span class="sxs-lookup"><span data-stu-id="f0825-118"><dt>**LVSIL\_STATE**</dt></span></span> </dl>                   | <span data-ttu-id="f0825-119">Список изображений с изображениями состояний.</span><span class="sxs-lookup"><span data-stu-id="f0825-119">Image list with state images.</span></span><br/> |
| <span id="LVSIL_GROUPHEADER"></span><span id="lvsil_groupheader"></span><dl> <span data-ttu-id="f0825-120"><dt>**ЛВСИЛ \_ грауфеадер**</dt></span><span class="sxs-lookup"><span data-stu-id="f0825-120"><dt>**LVSIL\_GROUPHEADER**</dt></span></span> </dl> | <span data-ttu-id="f0825-121">Список изображений для заголовка группы.</span><span class="sxs-lookup"><span data-stu-id="f0825-121">Image list for group header.</span></span><br/>  |



 

</dd> <dt>

<span data-ttu-id="f0825-122">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f0825-122">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="f0825-123">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="f0825-123">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0825-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f0825-124">Return value</span></span>

<span data-ttu-id="f0825-125">Возвращает маркер в указанный список изображений в случае успешного выполнения или **значение NULL** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="f0825-125">Returns the handle to the specified image list if successful, or **NULL** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0825-126">Требования</span><span class="sxs-lookup"><span data-stu-id="f0825-126">Requirements</span></span>



| <span data-ttu-id="f0825-127">Требование</span><span class="sxs-lookup"><span data-stu-id="f0825-127">Requirement</span></span> | <span data-ttu-id="f0825-128">Значение</span><span class="sxs-lookup"><span data-stu-id="f0825-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f0825-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f0825-129">Minimum supported client</span></span><br/> | <span data-ttu-id="f0825-130">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f0825-130">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f0825-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f0825-131">Minimum supported server</span></span><br/> | <span data-ttu-id="f0825-132">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f0825-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f0825-133">Header</span><span class="sxs-lookup"><span data-stu-id="f0825-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="f0825-134"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="f0825-134"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





