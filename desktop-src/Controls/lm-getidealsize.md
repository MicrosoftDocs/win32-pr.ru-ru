---
title: Сообщение LM_GETIDEALSIZE (Коммктрл. h)
description: Извлекает предпочтительную высоту ссылки для текущей ширины элемента управления.
ms.assetid: 63aad7eb-26ee-41d2-90d4-65fdcf0f182a
keywords:
- Элементы управления Windows для LM_GETIDEALSIZE сообщений
topic_type:
- apiref
api_name:
- LM_GETIDEALSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c138e22982116a3b7173f586d96c70cfc91194c3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489099"
---
# <a name="lm_getidealsize-message"></a><span data-ttu-id="b442c-104">\_Сообщение ЖЕТИДЕАЛСИЗЕ LM</span><span class="sxs-lookup"><span data-stu-id="b442c-104">LM\_GETIDEALSIZE message</span></span>

<span data-ttu-id="b442c-105">Извлекает предпочтительную высоту ссылки для текущей ширины элемента управления.</span><span class="sxs-lookup"><span data-stu-id="b442c-105">Retrieves the preferred height of a link for the control's current width.</span></span>

## <a name="parameters"></a><span data-ttu-id="b442c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b442c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b442c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b442c-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="b442c-108">Максимальная ширина ссылки в пикселях.</span><span class="sxs-lookup"><span data-stu-id="b442c-108">Maximum width of the link, in pixels.</span></span></dd> <dt>

<span data-ttu-id="b442c-109">*lParam* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="b442c-109">*lParam* \[out\]</span></span>
</dt> <dd><span data-ttu-id="b442c-110">При возвращении этого сообщения содержит указатель на структуру <a href="/previous-versions//dd145106(v=vs.85)">**размера**</a> .</span><span class="sxs-lookup"><span data-stu-id="b442c-110">When this message returns, contains a pointer to a <a href="/previous-versions//dd145106(v=vs.85)">**SIZE**</a> structure.</span></span> <span data-ttu-id="b442c-111">Элемент **CY** этой структуры указывает идеальную высоту элемента управления для заданной ширины.</span><span class="sxs-lookup"><span data-stu-id="b442c-111">The **cy** member of this structure indicates the ideal height of the control for the given width.</span></span> <span data-ttu-id="b442c-112">Он корректирует элемент **CX** на фактически необходимый объем пространства.</span><span class="sxs-lookup"><span data-stu-id="b442c-112">It adjusts the **cx** member to the amount of space actually needed.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b442c-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b442c-113">Return value</span></span>

<span data-ttu-id="b442c-114">Целое число, представляющее предпочтительную высоту текста ссылки в пикселях.</span><span class="sxs-lookup"><span data-stu-id="b442c-114">Integer that represents the preferred height of the link text, in pixels.</span></span>

## <a name="remarks"></a><span data-ttu-id="b442c-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b442c-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="b442c-116">Чтобы использовать этот API, необходимо предоставить манифест, указывающий Comclt32.dll версии 6,0.</span><span class="sxs-lookup"><span data-stu-id="b442c-116">To use this API, you must provide a manifest that specifies Comclt32.dll version 6.0.</span></span> <span data-ttu-id="b442c-117">Дополнительные сведения о манифестах см. в разделе [Включение визуальных стилей](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="b442c-117">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b442c-118">Требования</span><span class="sxs-lookup"><span data-stu-id="b442c-118">Requirements</span></span>



| <span data-ttu-id="b442c-119">Требование</span><span class="sxs-lookup"><span data-stu-id="b442c-119">Requirement</span></span> | <span data-ttu-id="b442c-120">Значение</span><span class="sxs-lookup"><span data-stu-id="b442c-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b442c-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b442c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b442c-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b442c-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b442c-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b442c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b442c-124">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b442c-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b442c-125">Header</span><span class="sxs-lookup"><span data-stu-id="b442c-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="b442c-126"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="b442c-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

