---
title: Сообщение RB_SETWINDOWTHEME (Коммктрл. h)
description: Задает визуальный стиль элемента управления главной панели.
ms.assetid: 5b32b354-3e25-4d02-9334-cc57acf41a73
keywords:
- Элементы управления Windows для RB_SETWINDOWTHEME сообщений
topic_type:
- apiref
api_name:
- RB_SETWINDOWTHEME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e136562394d26dd56d8d4c0c9ae916948144dbb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136631"
---
# <a name="rb_setwindowtheme-message"></a><span data-ttu-id="cfafb-104">\_Сообщение SETWINDOWTHEME RB</span><span class="sxs-lookup"><span data-stu-id="cfafb-104">RB\_SETWINDOWTHEME message</span></span>

<span data-ttu-id="cfafb-105">Задает визуальный стиль элемента управления главной панели.</span><span class="sxs-lookup"><span data-stu-id="cfafb-105">Sets the visual style of a rebar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="cfafb-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="cfafb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cfafb-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cfafb-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="cfafb-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="cfafb-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="cfafb-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cfafb-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cfafb-110">Указатель на строку в Юникоде, содержащую стиль визуального элемента главной панели, который необходимо задать.</span><span class="sxs-lookup"><span data-stu-id="cfafb-110">Pointer to a Unicode string that contains the rebar visual style to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cfafb-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cfafb-111">Return value</span></span>

<span data-ttu-id="cfafb-112">Возвращаемое значение не используется.</span><span class="sxs-lookup"><span data-stu-id="cfafb-112">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="cfafb-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cfafb-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="cfafb-114">Чтобы использовать это сообщение, необходимо указать манифест, указывающий Comclt32.dll версии 6,0.</span><span class="sxs-lookup"><span data-stu-id="cfafb-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="cfafb-115">Дополнительные сведения о манифестах см. в разделе [Включение визуальных стилей](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="cfafb-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="cfafb-116">Требования</span><span class="sxs-lookup"><span data-stu-id="cfafb-116">Requirements</span></span>



| <span data-ttu-id="cfafb-117">Требование</span><span class="sxs-lookup"><span data-stu-id="cfafb-117">Requirement</span></span> | <span data-ttu-id="cfafb-118">Значение</span><span class="sxs-lookup"><span data-stu-id="cfafb-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cfafb-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cfafb-119">Minimum supported client</span></span><br/> | <span data-ttu-id="cfafb-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cfafb-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cfafb-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cfafb-121">Minimum supported server</span></span><br/> | <span data-ttu-id="cfafb-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="cfafb-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cfafb-123">Header</span><span class="sxs-lookup"><span data-stu-id="cfafb-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="cfafb-124"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="cfafb-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





