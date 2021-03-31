---
title: Сообщение BCM_GETIMAGELIST (Коммктрл. h)
description: Возвращает \_ структуру IMAGELIST, описывающую список изображений, назначенных элементу управления "Кнопка". Это сообщение можно отправить явным образом или воспользоваться макросом "Кнопка" \_ .
ms.assetid: 79383758-53d4-4955-b472-befd338cbec6
keywords:
- Элементы управления Windows для BCM_GETIMAGELIST сообщений
topic_type:
- apiref
api_name:
- BCM_GETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b0c28e997e23d6df63150fe2283d04be1a8c0d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490887"
---
# <a name="bcm_getimagelist-message"></a><span data-ttu-id="8fb45-105">\_Сообщение BCM ImageList</span><span class="sxs-lookup"><span data-stu-id="8fb45-105">BCM\_GETIMAGELIST message</span></span>

<span data-ttu-id="8fb45-106">Возвращает структуру [**\_ IMAGELIST**](/windows/desktop/api/Commctrl/ns-commctrl-button_imagelist) , описывающую список изображений, назначенных элементу управления "Кнопка".</span><span class="sxs-lookup"><span data-stu-id="8fb45-106">Gets the [**BUTTON\_IMAGELIST**](/windows/desktop/api/Commctrl/ns-commctrl-button_imagelist) structure that describes the image list assigned to a button control.</span></span> <span data-ttu-id="8fb45-107">Это сообщение можно отправить явным образом или воспользоваться макросом [**"Кнопка" \_**](/windows/desktop/api/Commctrl/nf-commctrl-button_getimagelist) .</span><span class="sxs-lookup"><span data-stu-id="8fb45-107">You can send this message explicitly or use the [**Button\_GetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-button_getimagelist) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="8fb45-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="8fb45-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8fb45-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8fb45-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8fb45-110">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="8fb45-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="8fb45-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8fb45-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8fb45-112">Указатель на структуру [**\_ IMAGELIST**](/windows/desktop/api/Commctrl/ns-commctrl-button_imagelist) , содержащую сведения о списке изображений.</span><span class="sxs-lookup"><span data-stu-id="8fb45-112">A pointer to a [**BUTTON\_IMAGELIST**](/windows/desktop/api/Commctrl/ns-commctrl-button_imagelist) structure that contains image list information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8fb45-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8fb45-113">Return value</span></span>

<span data-ttu-id="8fb45-114">Если сообщение завершается с ошибкой, возвращается **значение true**.</span><span class="sxs-lookup"><span data-stu-id="8fb45-114">If the message succeeds, it returns **TRUE**.</span></span> <span data-ttu-id="8fb45-115">В противном случае возвращается **значение false**.</span><span class="sxs-lookup"><span data-stu-id="8fb45-115">Otherwise it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="8fb45-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8fb45-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="8fb45-117">Чтобы использовать это сообщение, необходимо указать манифест, указывающий Comclt32.dll версии 6,0.</span><span class="sxs-lookup"><span data-stu-id="8fb45-117">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="8fb45-118">Дополнительные сведения о манифестах см. в разделе [Включение визуальных стилей](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="8fb45-118">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8fb45-119">Требования</span><span class="sxs-lookup"><span data-stu-id="8fb45-119">Requirements</span></span>



| <span data-ttu-id="8fb45-120">Требование</span><span class="sxs-lookup"><span data-stu-id="8fb45-120">Requirement</span></span> | <span data-ttu-id="8fb45-121">Значение</span><span class="sxs-lookup"><span data-stu-id="8fb45-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8fb45-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8fb45-122">Minimum supported client</span></span><br/> | <span data-ttu-id="8fb45-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8fb45-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8fb45-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8fb45-124">Minimum supported server</span></span><br/> | <span data-ttu-id="8fb45-125">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8fb45-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8fb45-126">Header</span><span class="sxs-lookup"><span data-stu-id="8fb45-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="8fb45-127"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="8fb45-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





