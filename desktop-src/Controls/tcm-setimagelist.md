---
title: Сообщение TCM_SETIMAGELIST (Коммктрл. h)
description: Присваивает список изображений элементу управления "Вкладка". Это сообщение можно отправить явным образом или с помощью \_ макроса табктрл сетимажелист.
ms.assetid: b457c73c-4c38-4bc5-af5d-12bbd24504a6
keywords:
- Элементы управления Windows для TCM_SETIMAGELIST сообщений
topic_type:
- apiref
api_name:
- TCM_SETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59172c677998e816b295939c14effe45ff8aa961
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071102"
---
# <a name="tcm_setimagelist-message"></a><span data-ttu-id="73021-105">\_Сообщение СЕТИМАЖЕЛИСТ TCM</span><span class="sxs-lookup"><span data-stu-id="73021-105">TCM\_SETIMAGELIST message</span></span>

<span data-ttu-id="73021-106">Присваивает список изображений элементу управления "Вкладка".</span><span class="sxs-lookup"><span data-stu-id="73021-106">Assigns an image list to a tab control.</span></span> <span data-ttu-id="73021-107">Это сообщение можно отправить явным образом или с помощью макроса [**табктрл \_ сетимажелист**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setimagelist) .</span><span class="sxs-lookup"><span data-stu-id="73021-107">You can send this message explicitly or by using the [**TabCtrl\_SetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setimagelist) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="73021-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="73021-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73021-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="73021-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="73021-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="73021-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="73021-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="73021-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="73021-112">Обработчик для списка изображений, присваиваемый элементу управления "Вкладка".</span><span class="sxs-lookup"><span data-stu-id="73021-112">Handle to the image list to assign to the tab control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73021-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="73021-113">Return value</span></span>

<span data-ttu-id="73021-114">Возвращает указатель на предыдущий список изображений или **значение NULL** , если предыдущий список изображений отсутствует.</span><span class="sxs-lookup"><span data-stu-id="73021-114">Returns the handle to the previous image list, or **NULL** if there is no previous image list.</span></span>

## <a name="requirements"></a><span data-ttu-id="73021-115">Требования</span><span class="sxs-lookup"><span data-stu-id="73021-115">Requirements</span></span>



| <span data-ttu-id="73021-116">Требование</span><span class="sxs-lookup"><span data-stu-id="73021-116">Requirement</span></span> | <span data-ttu-id="73021-117">Значение</span><span class="sxs-lookup"><span data-stu-id="73021-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="73021-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="73021-118">Minimum supported client</span></span><br/> | <span data-ttu-id="73021-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="73021-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="73021-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="73021-120">Minimum supported server</span></span><br/> | <span data-ttu-id="73021-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="73021-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="73021-122">Header</span><span class="sxs-lookup"><span data-stu-id="73021-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="73021-123"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="73021-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





