---
title: Сообщение RB_SETBANDWIDTH (Коммктрл. h)
description: Задает ширину закрепленной полосы.
ms.assetid: dca9dfe9-3e5a-40bb-8de7-a296e6be7d06
keywords:
- Элементы управления Windows для RB_SETBANDWIDTH сообщений
topic_type:
- apiref
api_name:
- RB_SETBANDWIDTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 790f42ab977cfc0554c9a0eca737d541e001b6c9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491754"
---
# <a name="rb_setbandwidth-message"></a><span data-ttu-id="ec407-104">\_Сообщение СЕТБАНДВИДС RB</span><span class="sxs-lookup"><span data-stu-id="ec407-104">RB\_SETBANDWIDTH message</span></span>

<span data-ttu-id="ec407-105">Задает ширину закрепленной полосы.</span><span class="sxs-lookup"><span data-stu-id="ec407-105">Sets the width for a docked band.</span></span>

## <a name="parameters"></a><span data-ttu-id="ec407-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ec407-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec407-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ec407-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ec407-108">Индекс полосы.</span><span class="sxs-lookup"><span data-stu-id="ec407-108">Index of the band.</span></span>

</dd> <dt>

<span data-ttu-id="ec407-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ec407-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ec407-110">Новая ширина в пикселях.</span><span class="sxs-lookup"><span data-stu-id="ec407-110">New width in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec407-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ec407-111">Return value</span></span>

<span data-ttu-id="ec407-112">Возвращает значение **true** , если значение было задано, и **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="ec407-112">Returns **TRUE** if the value was set and **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec407-113">Требования</span><span class="sxs-lookup"><span data-stu-id="ec407-113">Requirements</span></span>



| <span data-ttu-id="ec407-114">Требование</span><span class="sxs-lookup"><span data-stu-id="ec407-114">Requirement</span></span> | <span data-ttu-id="ec407-115">Значение</span><span class="sxs-lookup"><span data-stu-id="ec407-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ec407-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ec407-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ec407-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ec407-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ec407-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ec407-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ec407-119">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ec407-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ec407-120">Header</span><span class="sxs-lookup"><span data-stu-id="ec407-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="ec407-121"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="ec407-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





