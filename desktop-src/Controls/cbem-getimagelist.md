---
title: Сообщение CBEM_GETIMAGELIST (Коммктрл. h)
description: Возвращает маркер для списка изображений, назначенного элементу управления ComboBoxEx.
ms.assetid: d577f920-b8f7-4d51-9507-765b7f925408
keywords:
- Элементы управления Windows для CBEM_GETIMAGELIST сообщений
topic_type:
- apiref
api_name:
- CBEM_GETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d143b8483fb5fb97ebd65fa2a98640089f6d548
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654657"
---
# <a name="cbem_getimagelist-message"></a><span data-ttu-id="58947-104">Сообщение КБЕМ/ \_ ImageList</span><span class="sxs-lookup"><span data-stu-id="58947-104">CBEM\_GETIMAGELIST message</span></span>

<span data-ttu-id="58947-105">Возвращает маркер для списка изображений, назначенного элементу управления ComboBoxEx.</span><span class="sxs-lookup"><span data-stu-id="58947-105">Gets the handle to an image list assigned to a ComboBoxEx control.</span></span>

## <a name="parameters"></a><span data-ttu-id="58947-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="58947-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58947-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="58947-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="58947-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="58947-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="58947-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="58947-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="58947-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="58947-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58947-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="58947-111">Return value</span></span>

<span data-ttu-id="58947-112">Возвращает маркер в список изображений, назначенный элементу управления в случае успеха, или **значение NULL** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="58947-112">Returns the handle to the image list assigned to the control if successful, or **NULL** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="58947-113">Требования</span><span class="sxs-lookup"><span data-stu-id="58947-113">Requirements</span></span>



| <span data-ttu-id="58947-114">Требование</span><span class="sxs-lookup"><span data-stu-id="58947-114">Requirement</span></span> | <span data-ttu-id="58947-115">Значение</span><span class="sxs-lookup"><span data-stu-id="58947-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="58947-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="58947-116">Minimum supported client</span></span><br/> | <span data-ttu-id="58947-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="58947-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="58947-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="58947-118">Minimum supported server</span></span><br/> | <span data-ttu-id="58947-119">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="58947-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="58947-120">Header</span><span class="sxs-lookup"><span data-stu-id="58947-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="58947-121"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="58947-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





