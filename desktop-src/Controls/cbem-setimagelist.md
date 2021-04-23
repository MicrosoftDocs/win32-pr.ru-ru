---
title: Сообщение CBEM_SETIMAGELIST (Коммктрл. h)
description: Задает список изображений для элемента управления ComboBoxEx.
ms.assetid: a4a8ed61-a532-4cf8-8291-c157ab0e7f31
keywords:
- Элементы управления Windows для CBEM_SETIMAGELIST сообщений
topic_type:
- apiref
api_name:
- CBEM_SETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33816abe36e2d1e1593e6365061a500d072c155b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989296"
---
# <a name="cbem_setimagelist-message"></a><span data-ttu-id="91d78-104">\_Сообщение кбем сетимажелист</span><span class="sxs-lookup"><span data-stu-id="91d78-104">CBEM\_SETIMAGELIST message</span></span>

<span data-ttu-id="91d78-105">Задает список изображений для элемента управления ComboBoxEx.</span><span class="sxs-lookup"><span data-stu-id="91d78-105">Sets an image list for a ComboBoxEx control.</span></span>

## <a name="parameters"></a><span data-ttu-id="91d78-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="91d78-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91d78-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="91d78-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="91d78-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="91d78-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="91d78-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="91d78-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="91d78-110">Описатель для списка изображений, который должен быть задан для элемента управления.</span><span class="sxs-lookup"><span data-stu-id="91d78-110">A handle to the image list to be set for the control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91d78-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="91d78-111">Return value</span></span>

<span data-ttu-id="91d78-112">Возвращает маркер для списка изображений, который ранее был связан с элементом управления, или возвращает **значение NULL** , если список изображений ранее не был задан.</span><span class="sxs-lookup"><span data-stu-id="91d78-112">Returns the handle to the image list previously associated with the control, or returns **NULL** if no image list was previously set.</span></span>

## <a name="remarks"></a><span data-ttu-id="91d78-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="91d78-113">Remarks</span></span>

> [!IMPORTANT]
> <span data-ttu-id="91d78-114">Высота изображений в списке изображений может изменить требования к размеру элемента управления ComboBoxEx.</span><span class="sxs-lookup"><span data-stu-id="91d78-114">The height of images in your image list might change the size requirements of the ComboBoxEx control.</span></span> <span data-ttu-id="91d78-115">Рекомендуется изменить размер элемента управления после отправки этого сообщения, чтобы убедиться, что оно отображается правильно.</span><span class="sxs-lookup"><span data-stu-id="91d78-115">It is recommended that you resize the control after sending this message to ensure that it is displayed properly.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="91d78-116">Требования</span><span class="sxs-lookup"><span data-stu-id="91d78-116">Requirements</span></span>



| <span data-ttu-id="91d78-117">Требование</span><span class="sxs-lookup"><span data-stu-id="91d78-117">Requirement</span></span> | <span data-ttu-id="91d78-118">Значение</span><span class="sxs-lookup"><span data-stu-id="91d78-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="91d78-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="91d78-119">Minimum supported client</span></span><br/> | <span data-ttu-id="91d78-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="91d78-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="91d78-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="91d78-121">Minimum supported server</span></span><br/> | <span data-ttu-id="91d78-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="91d78-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="91d78-123">Header</span><span class="sxs-lookup"><span data-stu-id="91d78-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="91d78-124"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="91d78-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





