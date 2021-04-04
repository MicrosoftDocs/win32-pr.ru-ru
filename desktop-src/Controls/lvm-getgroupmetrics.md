---
title: Сообщение LVM_GETGROUPMETRICS (Коммктрл. h)
description: Возвращает сведения о отображении групп.
ms.assetid: 75e7da66-50c6-4834-ae66-e43b8f9b0b34
keywords:
- Элементы управления Windows для LVM_GETGROUPMETRICS сообщений
topic_type:
- apiref
api_name:
- LVM_GETGROUPMETRICS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5af8ec50fe74ab90a0f3e44a69e2cbc7dda583e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989181"
---
# <a name="lvm_getgroupmetrics-message"></a><span data-ttu-id="c0838-104">\_Сообщение LVM жетграупметрикс</span><span class="sxs-lookup"><span data-stu-id="c0838-104">LVM\_GETGROUPMETRICS message</span></span>

<span data-ttu-id="c0838-105">Возвращает сведения о отображении групп.</span><span class="sxs-lookup"><span data-stu-id="c0838-105">Gets information about the display of groups.</span></span>

## <a name="parameters"></a><span data-ttu-id="c0838-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c0838-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0838-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c0838-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="c0838-108">Должен иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="c0838-108">Must be **NULL**.</span></span></dd> <dt>

<span data-ttu-id="c0838-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c0838-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="c0838-110">Указатель на структуру <a href="/windows/win32/api/commctrl/ns-commctrl-lvgroupmetrics">**лвграупметрикс**</a> , которая получает извлеченные метрики.</span><span class="sxs-lookup"><span data-stu-id="c0838-110">A pointer to an <a href="/windows/win32/api/commctrl/ns-commctrl-lvgroupmetrics">**LVGROUPMETRICS**</a> structure that receives the retrieved metrics.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0838-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c0838-111">Return value</span></span>

<span data-ttu-id="c0838-112">Возвращаемое значение не используется.</span><span class="sxs-lookup"><span data-stu-id="c0838-112">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="c0838-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c0838-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="c0838-114">Чтобы использовать это сообщение, необходимо указать манифест, указывающий Comclt32.dll версии 6,0.</span><span class="sxs-lookup"><span data-stu-id="c0838-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="c0838-115">Дополнительные сведения о манифестах см. в разделе [Включение визуальных стилей](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="c0838-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c0838-116">Требования</span><span class="sxs-lookup"><span data-stu-id="c0838-116">Requirements</span></span>



| <span data-ttu-id="c0838-117">Требование</span><span class="sxs-lookup"><span data-stu-id="c0838-117">Requirement</span></span> | <span data-ttu-id="c0838-118">Значение</span><span class="sxs-lookup"><span data-stu-id="c0838-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c0838-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c0838-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c0838-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c0838-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c0838-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c0838-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c0838-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c0838-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c0838-123">Header</span><span class="sxs-lookup"><span data-stu-id="c0838-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c0838-124"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="c0838-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





