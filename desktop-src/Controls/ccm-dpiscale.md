---
title: Сообщение CCM_DPISCALE (Коммктрл. h)
description: Включает автоматическое масштабирование с высоким числом точек на дюйм в элементах управления Tree-View, List-View элементах управления, элементах управления ComboBoxEx, элементах управления "заголовок", кнопках, элементах управления ToolBar, анимации и списках изображений.
ms.assetid: 3c751f10-992c-41f8-8f0b-3dc58f0591e4
keywords:
- Элементы управления Windows для CCM_DPISCALE сообщений
topic_type:
- apiref
api_name:
- CCM_DPISCALE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56ef978f486f370adf9872d28e1accbacc37a6de
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136458"
---
# <a name="ccm_dpiscale-message"></a><span data-ttu-id="434da-104">\_Сообщение ДПИСКАЛЕ CCM</span><span class="sxs-lookup"><span data-stu-id="434da-104">CCM\_DPISCALE message</span></span>

<span data-ttu-id="434da-105">Включает автоматическое масштабирование с высоким числом точек на дюйм в [древовидном представлении](tree-view-controls.md), [элементах управления "представление списка](list-view-control-reference.md)", [элементах](comboboxex-controls.md)управления "ComboBoxEx", [элементах управления "заголовок](header-controls.md)", [кнопках](buttons.md), [элементах управления ToolBar](toolbar-controls-overview.md), [элементах управления анимации](animation-control-overview.md)и [списках изображений](image-lists.md).</span><span class="sxs-lookup"><span data-stu-id="434da-105">Enables automatic high dots per inch (dpi) scaling in [Tree-View controls](tree-view-controls.md), [List-View controls](list-view-control-reference.md), [ComboBoxEx controls](comboboxex-controls.md), [Header controls](header-controls.md), [Buttons](buttons.md), [Toolbar controls](toolbar-controls-overview.md), [Animation controls](animation-control-overview.md), and [Image Lists](image-lists.md).</span></span>

## <a name="parameters"></a><span data-ttu-id="434da-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="434da-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="434da-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="434da-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="434da-108">Задайте значение **true**.</span><span class="sxs-lookup"><span data-stu-id="434da-108">Set to **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="434da-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="434da-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="434da-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="434da-110">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="434da-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="434da-111">Return value</span></span>

<span data-ttu-id="434da-112">Возвращаемое значение не используется.</span><span class="sxs-lookup"><span data-stu-id="434da-112">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="434da-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="434da-113">Remarks</span></span>

<span data-ttu-id="434da-114">Для быстрого запуска и [панели задач](/windows/desktop/shell/taskbar) не следует указывать масштабирование DPI, так как изображения уже масштабируются.</span><span class="sxs-lookup"><span data-stu-id="434da-114">Quick Launch and [Taskbar](/windows/desktop/shell/taskbar) should not specify a dpi scaling, because the images are already scaled.</span></span>

<span data-ttu-id="434da-115">Любой элемент управления, использующий список изображений, созданный с помощью метрики маленькие значки, не должен масштабировать свои значки.</span><span class="sxs-lookup"><span data-stu-id="434da-115">Any control that uses an image list created with the SmallIcon metric should not scale its icons.</span></span>

> [!Note]  
> <span data-ttu-id="434da-116">Чтобы использовать этот API, необходимо предоставить манифест, указывающий Comclt32.dll версии 6,0.</span><span class="sxs-lookup"><span data-stu-id="434da-116">To use this API, you must provide a manifest that specifies Comclt32.dll version 6.0.</span></span> <span data-ttu-id="434da-117">Дополнительные сведения о манифестах см. в разделе [Включение визуальных стилей](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="434da-117">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="434da-118">Требования</span><span class="sxs-lookup"><span data-stu-id="434da-118">Requirements</span></span>



| <span data-ttu-id="434da-119">Требование</span><span class="sxs-lookup"><span data-stu-id="434da-119">Requirement</span></span> | <span data-ttu-id="434da-120">Значение</span><span class="sxs-lookup"><span data-stu-id="434da-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="434da-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="434da-121">Minimum supported client</span></span><br/> | <span data-ttu-id="434da-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="434da-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="434da-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="434da-123">Minimum supported server</span></span><br/> | <span data-ttu-id="434da-124">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="434da-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="434da-125">Header</span><span class="sxs-lookup"><span data-stu-id="434da-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="434da-126"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="434da-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

