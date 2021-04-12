---
title: Сообщение CCM_SETWINDOWTHEME (Коммктрл. h)
description: Задает визуальный стиль элемента управления.
ms.assetid: 0200fa11-847f-477c-92e0-790b4d1ca0ef
keywords:
- Элементы управления Windows для CCM_SETWINDOWTHEME сообщений
topic_type:
- apiref
api_name:
- CCM_SETWINDOWTHEME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cea8996273a0c9d03123ce58f5fbb0dfb099be94
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491523"
---
# <a name="ccm_setwindowtheme-message"></a><span data-ttu-id="12144-104">\_Сообщение SETWINDOWTHEME CCM</span><span class="sxs-lookup"><span data-stu-id="12144-104">CCM\_SETWINDOWTHEME message</span></span>

<span data-ttu-id="12144-105">Задает визуальный стиль элемента управления.</span><span class="sxs-lookup"><span data-stu-id="12144-105">Sets the visual style of a control.</span></span>

## <a name="parameters"></a><span data-ttu-id="12144-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="12144-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12144-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="12144-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="12144-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="12144-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="12144-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="12144-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="12144-110">Указатель на строку в Юникоде, содержащую стиль визуального элемента управления, который необходимо задать.</span><span class="sxs-lookup"><span data-stu-id="12144-110">A pointer to a Unicode string that contains the control visual style to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12144-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="12144-111">Return value</span></span>

<span data-ttu-id="12144-112">Возвращаемое значение не используется.</span><span class="sxs-lookup"><span data-stu-id="12144-112">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="12144-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="12144-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="12144-114">Чтобы использовать это сообщение, необходимо указать манифест, указывающий Comclt32.dll версии 6,0.</span><span class="sxs-lookup"><span data-stu-id="12144-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="12144-115">Дополнительные сведения о манифестах см. в разделе [Включение визуальных стилей](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="12144-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="12144-116">Требования</span><span class="sxs-lookup"><span data-stu-id="12144-116">Requirements</span></span>



| <span data-ttu-id="12144-117">Требование</span><span class="sxs-lookup"><span data-stu-id="12144-117">Requirement</span></span> | <span data-ttu-id="12144-118">Значение</span><span class="sxs-lookup"><span data-stu-id="12144-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="12144-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="12144-119">Minimum supported client</span></span><br/> | <span data-ttu-id="12144-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="12144-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="12144-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="12144-121">Minimum supported server</span></span><br/> | <span data-ttu-id="12144-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="12144-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="12144-123">Header</span><span class="sxs-lookup"><span data-stu-id="12144-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="12144-124"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="12144-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





