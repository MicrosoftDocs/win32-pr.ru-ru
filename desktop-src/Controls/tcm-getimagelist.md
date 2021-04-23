---
title: Сообщение TCM_GETIMAGELIST (Коммктрл. h)
description: Извлекает список изображений, связанных с элементом управления "Вкладка". Это сообщение можно отправить явно или с помощью \_ макроса табктрлs.
ms.assetid: 86a0d8c7-ff3d-4e16-994e-4c72d1e62e9f
keywords:
- Элементы управления Windows для TCM_GETIMAGELIST сообщений
topic_type:
- apiref
api_name:
- TCM_GETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c4d471ef4d072e4305507f4f5ebc4a8f2745ed9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892534"
---
# <a name="tcm_getimagelist-message"></a><span data-ttu-id="c87a6-105">Сообщение TCM. \_ ImageList</span><span class="sxs-lookup"><span data-stu-id="c87a6-105">TCM\_GETIMAGELIST message</span></span>

<span data-ttu-id="c87a6-106">Извлекает список изображений, связанных с элементом управления "Вкладка".</span><span class="sxs-lookup"><span data-stu-id="c87a6-106">Retrieves the image list associated with a tab control.</span></span> <span data-ttu-id="c87a6-107">Это сообщение можно отправить явно или с помощью макроса [**табктрлs \_**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getimagelist) .</span><span class="sxs-lookup"><span data-stu-id="c87a6-107">You can send this message explicitly or by using the [**TabCtrl\_GetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getimagelist) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="c87a6-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="c87a6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c87a6-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c87a6-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="c87a6-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="c87a6-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="c87a6-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c87a6-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="c87a6-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="c87a6-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c87a6-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c87a6-113">Return value</span></span>

<span data-ttu-id="c87a6-114">Возвращает маркер в список изображений в случае успеха или **значение NULL** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="c87a6-114">Returns the handle to the image list if successful, or **NULL** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="c87a6-115">Требования</span><span class="sxs-lookup"><span data-stu-id="c87a6-115">Requirements</span></span>



| <span data-ttu-id="c87a6-116">Требование</span><span class="sxs-lookup"><span data-stu-id="c87a6-116">Requirement</span></span> | <span data-ttu-id="c87a6-117">Значение</span><span class="sxs-lookup"><span data-stu-id="c87a6-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c87a6-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c87a6-118">Minimum supported client</span></span><br/> | <span data-ttu-id="c87a6-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c87a6-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c87a6-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c87a6-120">Minimum supported server</span></span><br/> | <span data-ttu-id="c87a6-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c87a6-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c87a6-122">Header</span><span class="sxs-lookup"><span data-stu-id="c87a6-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="c87a6-123"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="c87a6-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





