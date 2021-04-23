---
title: Сообщение CBEM_SETWINDOWTHEME (Коммктрл. h)
description: Задает визуальный стиль элемента управления ComboBoxEx.
ms.assetid: 064f9a24-42be-42f4-bee3-e7320fe8c366
keywords:
- Элементы управления Windows для CBEM_SETWINDOWTHEME сообщений
topic_type:
- apiref
api_name:
- CBEM_SETWINDOWTHEME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0cda1e5c46bb6216c413737c44b5785ac26925f6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654535"
---
# <a name="cbem_setwindowtheme-message"></a><span data-ttu-id="4c69b-104">\_Сообщение кбем SETWINDOWTHEME</span><span class="sxs-lookup"><span data-stu-id="4c69b-104">CBEM\_SETWINDOWTHEME message</span></span>

<span data-ttu-id="4c69b-105">Задает визуальный стиль элемента управления ComboBoxEx.</span><span class="sxs-lookup"><span data-stu-id="4c69b-105">Sets the visual style of a ComboBoxEx control.</span></span>

## <a name="parameters"></a><span data-ttu-id="4c69b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4c69b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c69b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4c69b-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="4c69b-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="4c69b-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="4c69b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4c69b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4c69b-110">Указатель на строку в Юникоде, содержащую стиль визуального элемента управления, который необходимо задать.</span><span class="sxs-lookup"><span data-stu-id="4c69b-110">A pointer to a Unicode string that contains the control visual style to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c69b-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4c69b-111">Return value</span></span>

<span data-ttu-id="4c69b-112">Возвращаемое значение не используется.</span><span class="sxs-lookup"><span data-stu-id="4c69b-112">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="4c69b-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4c69b-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="4c69b-114">Чтобы использовать это сообщение, необходимо предоставить манифест с указанием Comclt32 версии 6,0.</span><span class="sxs-lookup"><span data-stu-id="4c69b-114">To use this message, you must provide a manifest specifying Comclt32 version 6.0.</span></span> <span data-ttu-id="4c69b-115">Дополнительные сведения о манифестах см. в разделе [Включение визуальных стилей](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="4c69b-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4c69b-116">Требования</span><span class="sxs-lookup"><span data-stu-id="4c69b-116">Requirements</span></span>



| <span data-ttu-id="4c69b-117">Требование</span><span class="sxs-lookup"><span data-stu-id="4c69b-117">Requirement</span></span> | <span data-ttu-id="4c69b-118">Значение</span><span class="sxs-lookup"><span data-stu-id="4c69b-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4c69b-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4c69b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="4c69b-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4c69b-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4c69b-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4c69b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="4c69b-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4c69b-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4c69b-123">Header</span><span class="sxs-lookup"><span data-stu-id="4c69b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="4c69b-124"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="4c69b-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





