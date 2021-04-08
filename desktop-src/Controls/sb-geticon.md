---
title: Сообщение SB_GETICON (Коммктрл. h)
description: Возвращает значок для части в строке состояния.
ms.assetid: f99508e3-afa8-48fd-b87a-fce41c4410ff
keywords:
- Элементы управления Windows для SB_GETICON сообщений
topic_type:
- apiref
api_name:
- SB_GETICON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab86809df54d796b8e83f05f2a2b9041450ce2fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892354"
---
# <a name="sb_geticon-message"></a><span data-ttu-id="5e835-104">\_Сообщение о ПЕРЕзначке SB</span><span class="sxs-lookup"><span data-stu-id="5e835-104">SB\_GETICON message</span></span>

<span data-ttu-id="5e835-105">Возвращает значок для части в строке состояния.</span><span class="sxs-lookup"><span data-stu-id="5e835-105">Retrieves the icon for a part in a status bar.</span></span>

## <a name="parameters"></a><span data-ttu-id="5e835-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5e835-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e835-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5e835-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5e835-108">Отсчитываемый от нуля индекс части, содержащей извлекаемый значок.</span><span class="sxs-lookup"><span data-stu-id="5e835-108">Zero-based index of the part that contains the icon to be retrieved.</span></span> <span data-ttu-id="5e835-109">Если этот параметр имеет значение-1, строка состояния считается строкой состояния [простого режима](status-bars.md) .</span><span class="sxs-lookup"><span data-stu-id="5e835-109">If this parameter is -1, the status bar is assumed to be a [Simple Mode](status-bars.md) status bar.</span></span>

</dd> <dt>

<span data-ttu-id="5e835-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5e835-110">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="5e835-111">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="5e835-111">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e835-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5e835-112">Return value</span></span>

<span data-ttu-id="5e835-113">Возвращает маркер для значка в случае успеха или **значение NULL** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="5e835-113">Returns the handle to the icon if successful, or **NULL** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e835-114">Требования</span><span class="sxs-lookup"><span data-stu-id="5e835-114">Requirements</span></span>



| <span data-ttu-id="5e835-115">Требование</span><span class="sxs-lookup"><span data-stu-id="5e835-115">Requirement</span></span> | <span data-ttu-id="5e835-116">Значение</span><span class="sxs-lookup"><span data-stu-id="5e835-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5e835-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5e835-117">Minimum supported client</span></span><br/> | <span data-ttu-id="5e835-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5e835-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5e835-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5e835-119">Minimum supported server</span></span><br/> | <span data-ttu-id="5e835-120">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="5e835-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5e835-121">Header</span><span class="sxs-lookup"><span data-stu-id="5e835-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="5e835-122"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="5e835-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





