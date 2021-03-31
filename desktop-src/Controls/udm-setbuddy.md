---
title: Сообщение UDM_SETBUDDY (Коммктрл. h)
description: Устанавливает окно собеседника для элемента управления "вверх/вниз".
ms.assetid: 66e35acc-95f6-4bc5-b654-690abf2188ba
keywords:
- Элементы управления Windows для UDM_SETBUDDY сообщений
topic_type:
- apiref
api_name:
- UDM_SETBUDDY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0e8bd57727d730c67fe09a52c0bedf121eac982
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136622"
---
# <a name="udm_setbuddy-message"></a><span data-ttu-id="ec73c-104">\_Сообщение СЕТБУДДИ UDM</span><span class="sxs-lookup"><span data-stu-id="ec73c-104">UDM\_SETBUDDY message</span></span>

<span data-ttu-id="ec73c-105">Устанавливает окно собеседника для элемента управления "вверх/вниз".</span><span class="sxs-lookup"><span data-stu-id="ec73c-105">Sets the buddy window for an up-down control.</span></span>

## <a name="parameters"></a><span data-ttu-id="ec73c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ec73c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec73c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ec73c-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ec73c-108">Обработайте с новым дружественным окном.</span><span class="sxs-lookup"><span data-stu-id="ec73c-108">Handle to the new buddy window.</span></span>

</dd> <dt>

<span data-ttu-id="ec73c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ec73c-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="ec73c-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="ec73c-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec73c-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ec73c-111">Return value</span></span>

<span data-ttu-id="ec73c-112">Возвращаемое значение — это маркер предыдущего дружественного окна.</span><span class="sxs-lookup"><span data-stu-id="ec73c-112">The return value is the handle to the previous buddy window.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec73c-113">Требования</span><span class="sxs-lookup"><span data-stu-id="ec73c-113">Requirements</span></span>



| <span data-ttu-id="ec73c-114">Требование</span><span class="sxs-lookup"><span data-stu-id="ec73c-114">Requirement</span></span> | <span data-ttu-id="ec73c-115">Значение</span><span class="sxs-lookup"><span data-stu-id="ec73c-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ec73c-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ec73c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ec73c-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ec73c-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ec73c-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ec73c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ec73c-119">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ec73c-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ec73c-120">Header</span><span class="sxs-lookup"><span data-stu-id="ec73c-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="ec73c-121"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="ec73c-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





