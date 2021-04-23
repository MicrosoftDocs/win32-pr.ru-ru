---
title: Сообщение TCM_REMOVEIMAGE (Коммктрл. h)
description: Удаляет изображение из списка изображений элемента управления "Вкладка". Это сообщение можно отправить явным образом или с помощью \_ макроса табктрл ремовеимаже.
ms.assetid: f2761338-0afa-47d8-9d9c-1d5a4a7f7bcf
keywords:
- Элементы управления Windows для TCM_REMOVEIMAGE сообщений
topic_type:
- apiref
api_name:
- TCM_REMOVEIMAGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6cbc51aa0efed847e39e735443c0d42e288bbaab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654684"
---
# <a name="tcm_removeimage-message"></a><span data-ttu-id="5535f-105">\_Сообщение РЕМОВЕИМАЖЕ TCM</span><span class="sxs-lookup"><span data-stu-id="5535f-105">TCM\_REMOVEIMAGE message</span></span>

<span data-ttu-id="5535f-106">Удаляет изображение из списка изображений элемента управления "Вкладка".</span><span class="sxs-lookup"><span data-stu-id="5535f-106">Removes an image from a tab control's image list.</span></span> <span data-ttu-id="5535f-107">Это сообщение можно отправить явным образом или с помощью макроса [**табктрл \_ ремовеимаже**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_removeimage) .</span><span class="sxs-lookup"><span data-stu-id="5535f-107">You can send this message explicitly or by using the [**TabCtrl\_RemoveImage**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_removeimage) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="5535f-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="5535f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5535f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5535f-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5535f-110">Индекс удаляемого изображения.</span><span class="sxs-lookup"><span data-stu-id="5535f-110">Index of the image to remove.</span></span>

</dd> <dt>

<span data-ttu-id="5535f-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5535f-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="5535f-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="5535f-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5535f-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5535f-113">Return value</span></span>

<span data-ttu-id="5535f-114">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="5535f-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5535f-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5535f-115">Remarks</span></span>

<span data-ttu-id="5535f-116">Элемент управления "Вкладка" обновляет индекс изображения каждой вкладки, поэтому каждая вкладка остается связанной с тем же изображением, что и раньше.</span><span class="sxs-lookup"><span data-stu-id="5535f-116">The tab control updates each tab's image index, so each tab remains associated with the same image as before.</span></span> <span data-ttu-id="5535f-117">Если на вкладке используется удаляемое изображение, то на вкладке будет задано отсутствие изображения.</span><span class="sxs-lookup"><span data-stu-id="5535f-117">If a tab is using the image being removed, the tab will be set to have no image.</span></span>

## <a name="requirements"></a><span data-ttu-id="5535f-118">Требования</span><span class="sxs-lookup"><span data-stu-id="5535f-118">Requirements</span></span>



| <span data-ttu-id="5535f-119">Требование</span><span class="sxs-lookup"><span data-stu-id="5535f-119">Requirement</span></span> | <span data-ttu-id="5535f-120">Значение</span><span class="sxs-lookup"><span data-stu-id="5535f-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5535f-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5535f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="5535f-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5535f-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5535f-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5535f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="5535f-124">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="5535f-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5535f-125">Header</span><span class="sxs-lookup"><span data-stu-id="5535f-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="5535f-126"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="5535f-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





