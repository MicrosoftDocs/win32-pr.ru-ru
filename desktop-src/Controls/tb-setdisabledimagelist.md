---
title: Сообщение TB_SETDISABLEDIMAGELIST (Коммктрл. h)
description: Задает список изображений, который будет использоваться элементом управления Toolbar для вывода отключенных кнопок.
ms.assetid: 1e76b3cf-2d06-48c8-8298-ef6caf3d85c3
keywords:
- Элементы управления Windows для TB_SETDISABLEDIMAGELIST сообщений
topic_type:
- apiref
api_name:
- TB_SETDISABLEDIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7cc8c9ec1fdc9658413da5991fa109e7bef27a6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071857"
---
# <a name="tb_setdisabledimagelist-message"></a><span data-ttu-id="614b2-104">\_Сообщение СЕТДИСАБЛЕДИМАЖЕЛИСТ ТБ</span><span class="sxs-lookup"><span data-stu-id="614b2-104">TB\_SETDISABLEDIMAGELIST message</span></span>

<span data-ttu-id="614b2-105">Задает список изображений, который будет использоваться элементом управления Toolbar для вывода отключенных кнопок.</span><span class="sxs-lookup"><span data-stu-id="614b2-105">Sets the image list that the toolbar control will use to display disabled buttons.</span></span>

## <a name="parameters"></a><span data-ttu-id="614b2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="614b2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="614b2-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="614b2-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="614b2-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="614b2-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="614b2-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="614b2-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="614b2-110">Обрабатываемый набор изображений.</span><span class="sxs-lookup"><span data-stu-id="614b2-110">Handle to the image list that will be set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="614b2-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="614b2-111">Return value</span></span>

<span data-ttu-id="614b2-112">Возвращает маркер списка изображений, который ранее использовался для вывода отключенных кнопок, или **значение NULL** , если список изображений ранее не был задан.</span><span class="sxs-lookup"><span data-stu-id="614b2-112">Returns the handle to the image list previously used to display disabled buttons, or **NULL** if no image list was previously set.</span></span>

## <a name="requirements"></a><span data-ttu-id="614b2-113">Требования</span><span class="sxs-lookup"><span data-stu-id="614b2-113">Requirements</span></span>



| <span data-ttu-id="614b2-114">Требование</span><span class="sxs-lookup"><span data-stu-id="614b2-114">Requirement</span></span> | <span data-ttu-id="614b2-115">Значение</span><span class="sxs-lookup"><span data-stu-id="614b2-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="614b2-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="614b2-116">Minimum supported client</span></span><br/> | <span data-ttu-id="614b2-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="614b2-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="614b2-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="614b2-118">Minimum supported server</span></span><br/> | <span data-ttu-id="614b2-119">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="614b2-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="614b2-120">Header</span><span class="sxs-lookup"><span data-stu-id="614b2-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="614b2-121"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="614b2-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





