---
title: Сообщение BCM_SETIMAGELIST (Коммктрл. h)
description: Присваивает список изображений элементу управления "Кнопка". Это сообщение можно отправить явным образом или воспользоваться \_ макросом кнопки сетимажелист.
ms.assetid: 805d2d9b-3e8f-4323-abaf-0dd5765cd740
keywords:
- Элементы управления Windows для BCM_SETIMAGELIST сообщений
topic_type:
- apiref
api_name:
- BCM_SETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9bdf29735958f3c40af544bca4b946458df8431
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071526"
---
# <a name="bcm_setimagelist-message"></a><span data-ttu-id="db7ad-105">\_Сообщение СЕТИМАЖЕЛИСТ BCM</span><span class="sxs-lookup"><span data-stu-id="db7ad-105">BCM\_SETIMAGELIST message</span></span>

<span data-ttu-id="db7ad-106">Присваивает список изображений элементу управления "Кнопка".</span><span class="sxs-lookup"><span data-stu-id="db7ad-106">Assigns an image list to a button control.</span></span> <span data-ttu-id="db7ad-107">Это сообщение можно отправить явным образом или воспользоваться макросом [**кнопки \_ сетимажелист**](/windows/desktop/api/Commctrl/nf-commctrl-button_setimagelist) .</span><span class="sxs-lookup"><span data-stu-id="db7ad-107">You can send this message explicitly or use the [**Button\_SetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-button_setimagelist) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="db7ad-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="db7ad-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db7ad-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="db7ad-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="db7ad-110">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="db7ad-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="db7ad-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="db7ad-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="db7ad-112">Указатель на структуру [**\_ IMAGELIST**](/windows/desktop/api/Commctrl/ns-commctrl-button_imagelist) , содержащую сведения о списке изображений.</span><span class="sxs-lookup"><span data-stu-id="db7ad-112">A pointer to a [**BUTTON\_IMAGELIST**](/windows/desktop/api/Commctrl/ns-commctrl-button_imagelist) structure that contains image list information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db7ad-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="db7ad-113">Return value</span></span>

<span data-ttu-id="db7ad-114">Если сообщение завершается с ошибкой, возвращается **значение true**.</span><span class="sxs-lookup"><span data-stu-id="db7ad-114">If the message succeeds, it returns **TRUE**.</span></span> <span data-ttu-id="db7ad-115">В противном случае возвращается **значение false**.</span><span class="sxs-lookup"><span data-stu-id="db7ad-115">Otherwise it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="db7ad-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="db7ad-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="db7ad-117">Чтобы использовать это сообщение, необходимо указать манифест, указывающий Comclt32.dll версии 6,0.</span><span class="sxs-lookup"><span data-stu-id="db7ad-117">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="db7ad-118">Дополнительные сведения о манифестах см. в разделе [Включение визуальных стилей](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="db7ad-118">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

<span data-ttu-id="db7ad-119">Список изображений, на который ссылается элемент **химл** в структуре [**\_ IMAGELIST**](/windows/desktop/api/Commctrl/ns-commctrl-button_imagelist) , должен содержать один образ, используемый для всех состояний или отдельных изображений для каждого состояния.</span><span class="sxs-lookup"><span data-stu-id="db7ad-119">The image list referred to in the **himl** member of the [**BUTTON\_IMAGELIST**](/windows/desktop/api/Commctrl/ns-commctrl-button_imagelist) structure should contain either a single image to be used for all states or individual images for each state.</span></span> <span data-ttu-id="db7ad-120">В vssym32. h определены следующие состояния.</span><span class="sxs-lookup"><span data-stu-id="db7ad-120">The following states are defined in vssym32.h.</span></span>

``` syntax
enum PUSHBUTTONSTATES {
    PBS_NORMAL = 1,
    PBS_HOT = 2,
    PBS_PRESSED = 3,
    PBS_DISABLED = 4,
    PBS_DEFAULTED = 5,
    PBS_STYLUSHOT = 6,
};
```

<span data-ttu-id="db7ad-121">Обратите внимание, что PBS \_ стилушот используется только на планшетных компьютерах.</span><span class="sxs-lookup"><span data-stu-id="db7ad-121">Note that PBS\_STYLUSHOT is used only on tablet computers.</span></span>

<span data-ttu-id="db7ad-122">Каждое значение является индексом соответствующего изображения в списке изображений.</span><span class="sxs-lookup"><span data-stu-id="db7ad-122">Each value is an index to the appropriate image in the image list.</span></span> <span data-ttu-id="db7ad-123">Если имеется только одно изображение, оно используется для всех состояний.</span><span class="sxs-lookup"><span data-stu-id="db7ad-123">If only one image is present, it is used for all states.</span></span> <span data-ttu-id="db7ad-124">Если список изображений содержит более одного изображения, каждый индекс соответствует одному состоянию кнопки.</span><span class="sxs-lookup"><span data-stu-id="db7ad-124">If the image list contains more than one image, each index corresponds to one state of the button.</span></span> <span data-ttu-id="db7ad-125">Если изображение не предоставляется для каждого состояния, для этих состояний ничего не отображается без изображений.</span><span class="sxs-lookup"><span data-stu-id="db7ad-125">If an image is not provided for each state, nothing is drawn for those states without images.</span></span>

## <a name="requirements"></a><span data-ttu-id="db7ad-126">Требования</span><span class="sxs-lookup"><span data-stu-id="db7ad-126">Requirements</span></span>



| <span data-ttu-id="db7ad-127">Требование</span><span class="sxs-lookup"><span data-stu-id="db7ad-127">Requirement</span></span> | <span data-ttu-id="db7ad-128">Значение</span><span class="sxs-lookup"><span data-stu-id="db7ad-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="db7ad-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="db7ad-129">Minimum supported client</span></span><br/> | <span data-ttu-id="db7ad-130">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="db7ad-130">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="db7ad-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="db7ad-131">Minimum supported server</span></span><br/> | <span data-ttu-id="db7ad-132">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="db7ad-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="db7ad-133">Header</span><span class="sxs-lookup"><span data-stu-id="db7ad-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="db7ad-134"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="db7ad-134"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





