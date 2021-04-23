---
title: Сообщение TB_GETPRESSEDIMAGELIST (Коммктрл. h)
description: Возвращает список изображений, используемый элементом управления Toolbar для отображения кнопок в нажатом состоянии.
ms.assetid: 116d4212-48ea-4b00-a752-21e5e1f10e36
keywords:
- Элементы управления Windows для TB_GETPRESSEDIMAGELIST сообщений
topic_type:
- apiref
api_name:
- TB_GETPRESSEDIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3028b119eb7f84a66caf0b6978382cee569b4a21
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137739"
---
# <a name="tb_getpressedimagelist-message"></a><span data-ttu-id="41fb3-104">\_Сообщение ЖЕТПРЕССЕДИМАЖЕЛИСТ ТБ</span><span class="sxs-lookup"><span data-stu-id="41fb3-104">TB\_GETPRESSEDIMAGELIST message</span></span>

<span data-ttu-id="41fb3-105">Возвращает список изображений, используемый элементом управления Toolbar для отображения кнопок в нажатом состоянии.</span><span class="sxs-lookup"><span data-stu-id="41fb3-105">Gets the image list that a toolbar control uses to display buttons in a pressed state.</span></span>

## <a name="parameters"></a><span data-ttu-id="41fb3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="41fb3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41fb3-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="41fb3-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="41fb3-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="41fb3-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="41fb3-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="41fb3-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="41fb3-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="41fb3-110">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41fb3-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="41fb3-111">Return value</span></span>

<span data-ttu-id="41fb3-112">Возвращает маркер в список изображений или **значение NULL** , если список изображений не задан.</span><span class="sxs-lookup"><span data-stu-id="41fb3-112">Returns the handle to the image list, or **NULL** if no image list is set.</span></span>

## <a name="requirements"></a><span data-ttu-id="41fb3-113">Требования</span><span class="sxs-lookup"><span data-stu-id="41fb3-113">Requirements</span></span>



| <span data-ttu-id="41fb3-114">Требование</span><span class="sxs-lookup"><span data-stu-id="41fb3-114">Requirement</span></span> | <span data-ttu-id="41fb3-115">Значение</span><span class="sxs-lookup"><span data-stu-id="41fb3-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="41fb3-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="41fb3-116">Minimum supported client</span></span><br/> | <span data-ttu-id="41fb3-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="41fb3-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="41fb3-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="41fb3-118">Minimum supported server</span></span><br/> | <span data-ttu-id="41fb3-119">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="41fb3-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="41fb3-120">Header</span><span class="sxs-lookup"><span data-stu-id="41fb3-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="41fb3-121"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="41fb3-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





