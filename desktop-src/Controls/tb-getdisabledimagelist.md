---
title: Сообщение TB_GETDISABLEDIMAGELIST (Коммктрл. h)
description: Извлекает список изображений, используемый элементом управления Toolbar для вывода неактивных кнопок.
ms.assetid: 8f6782d5-488b-4906-908a-e4bf8d512e0a
keywords:
- Элементы управления Windows для TB_GETDISABLEDIMAGELIST сообщений
topic_type:
- apiref
api_name:
- TB_GETDISABLEDIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2fc847927ef14312c76e26303bec5de07b788266
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988547"
---
# <a name="tb_getdisabledimagelist-message"></a><span data-ttu-id="32ee9-104">\_Сообщение ЖЕТДИСАБЛЕДИМАЖЕЛИСТ ТБ</span><span class="sxs-lookup"><span data-stu-id="32ee9-104">TB\_GETDISABLEDIMAGELIST message</span></span>

<span data-ttu-id="32ee9-105">Извлекает список изображений, используемый элементом управления Toolbar для вывода неактивных кнопок.</span><span class="sxs-lookup"><span data-stu-id="32ee9-105">Retrieves the image list that a toolbar control uses to display inactive buttons.</span></span>

## <a name="parameters"></a><span data-ttu-id="32ee9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="32ee9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32ee9-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="32ee9-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="32ee9-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="32ee9-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="32ee9-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="32ee9-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="32ee9-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="32ee9-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32ee9-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="32ee9-111">Return value</span></span>

<span data-ttu-id="32ee9-112">Возвращает маркер в неактивный список изображений или **значение NULL** , если Неактивный список изображений не задан.</span><span class="sxs-lookup"><span data-stu-id="32ee9-112">Returns the handle to the inactive image list, or **NULL** if no inactive image list is set.</span></span>

## <a name="requirements"></a><span data-ttu-id="32ee9-113">Требования</span><span class="sxs-lookup"><span data-stu-id="32ee9-113">Requirements</span></span>



| <span data-ttu-id="32ee9-114">Требование</span><span class="sxs-lookup"><span data-stu-id="32ee9-114">Requirement</span></span> | <span data-ttu-id="32ee9-115">Значение</span><span class="sxs-lookup"><span data-stu-id="32ee9-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="32ee9-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="32ee9-116">Minimum supported client</span></span><br/> | <span data-ttu-id="32ee9-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="32ee9-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="32ee9-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="32ee9-118">Minimum supported server</span></span><br/> | <span data-ttu-id="32ee9-119">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="32ee9-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="32ee9-120">Header</span><span class="sxs-lookup"><span data-stu-id="32ee9-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="32ee9-121"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="32ee9-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





