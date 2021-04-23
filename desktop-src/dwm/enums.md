---
title: Константы и перечисления DWM
description: В этом разделе содержатся сведения о константах и перечислениях, используемых в интерфейсах API диспетчер окон рабочего стола (DWM).
ms.assetid: b01f620d-ac87-4e93-88ab-f4297d8cf1d5
keywords:
- Диспетчер окон рабочего стола (DWM), справочные материалы
- DWM (диспетчер окон рабочего стола), Справочник
- Диспетчер окон рабочего стола (DWM), константы
- DWM (диспетчер окон рабочего стола), константы
- Диспетчер окон рабочего стола (DWM), перечисления
- DWM (диспетчер окон рабочего стола), перечисления
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 280fff527f95176b47fc99f88d09453dbf579f38
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103776721"
---
# <a name="dwm-constants-and-enumerations"></a><span data-ttu-id="25702-109">Константы и перечисления DWM</span><span class="sxs-lookup"><span data-stu-id="25702-109">DWM Constants and Enumerations</span></span>

<span data-ttu-id="25702-110">В этом разделе содержатся сведения о константах и перечислениях, используемых в интерфейсах API диспетчер окон рабочего стола (DWM).</span><span class="sxs-lookup"><span data-stu-id="25702-110">This section contains information about the constants and enumerations used in the Desktop Window Manager (DWM) APIs.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="25702-111">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="25702-111">In this section</span></span>



| <span data-ttu-id="25702-112">Раздел</span><span class="sxs-lookup"><span data-stu-id="25702-112">Topic</span></span>                                                                                     | <span data-ttu-id="25702-113">Описание</span><span class="sxs-lookup"><span data-stu-id="25702-113">Description</span></span>                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="25702-114">**Размытия в DWM за константами**</span><span class="sxs-lookup"><span data-stu-id="25702-114">**DWM Blur Behind Constants**</span></span>](dwm-bb-constants.md)<br/>                          | <span data-ttu-id="25702-115">Флаги, используемые структурой [**\_ блурбехинд DWM**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_blurbehind) для указания того, какие из его членов содержат действительные сведения.</span><span class="sxs-lookup"><span data-stu-id="25702-115">Flags used by the [**DWM\_BLURBEHIND**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_blurbehind) structure to indicate which of its members contain valid information.</span></span><br/>                                                                    |
| [<span data-ttu-id="25702-116">**DWM включает константы композиции**</span><span class="sxs-lookup"><span data-stu-id="25702-116">**DWM Enable Composition Constants**</span></span>](dwm-ec-constants.md)<br/>                   | <span data-ttu-id="25702-117">Флаги, используемые функцией [**двменаблекомпоситион**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablecomposition)  для изменения состояния композиции DWM.</span><span class="sxs-lookup"><span data-stu-id="25702-117">Flags used by the [**DwmEnableComposition**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablecomposition)  function to change the state of DWM composition.</span></span><br/>                                                                             |
| [<span data-ttu-id="25702-118">**\_ \_ выборка исходного ФРЕЙМа DWM \_**</span><span class="sxs-lookup"><span data-stu-id="25702-118">**DWM\_SOURCE\_FRAME\_SAMPLING**</span></span>](/windows/desktop/api/Dwmapi/ne-dwmapi-dwm_source_frame_sampling)<br/>              | <span data-ttu-id="25702-119">Флаги, используемые функцией [**двмсетпресентпараметерс**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetpresentparameters) для указания типа выборки кадров.</span><span class="sxs-lookup"><span data-stu-id="25702-119">Flags used by the [**DwmSetPresentParameters**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetpresentparameters) function to specify the frame sampling type.</span></span><br/>                                                                            |
| [<span data-ttu-id="25702-120">**\_ \_ требования к ОКНУ вкладки DWM \_**</span><span class="sxs-lookup"><span data-stu-id="25702-120">**DWM\_TAB\_WINDOW\_REQUIREMENTS**</span></span>](/windows/desktop/api/dwmapi/ne-dwmapi-dwm_tab_window_requirements)<br/>          | <span data-ttu-id="25702-121">Возвращается функцией Двмжетунметтабрекуирементс для указания требований, необходимых окну для размещения вкладок в заголовке окна приложения.</span><span class="sxs-lookup"><span data-stu-id="25702-121">Returned by DwmGetUnmetTabRequirements to indicate the requirements needed for a window to put tabs in the application title bar.</span></span><br/>                                                                    |
| [<span data-ttu-id="25702-122">**\_Константы DWM ТНП**</span><span class="sxs-lookup"><span data-stu-id="25702-122">**DWM\_TNP Constants**</span></span>](dwm-tnp-constants.md)<br/>                                | <span data-ttu-id="25702-123">Флаги, используемые структурой [**\_ \_ свойств эскиза DWM**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_thumbnail_properties) для указания того, какие из его элементов содержат допустимые сведения.</span><span class="sxs-lookup"><span data-stu-id="25702-123">Flags used by the [**DWM\_THUMBNAIL\_PROPERTIES**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_thumbnail_properties) structure to indicate which of its members contain valid information.</span></span><br/>                                               |
| [<span data-ttu-id="25702-124">**DWMFLIP3DWINDOWPOLICY**</span><span class="sxs-lookup"><span data-stu-id="25702-124">**DWMFLIP3DWINDOWPOLICY**</span></span>](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmflip3dwindowpolicy)<br/>                         | <span data-ttu-id="25702-125">Флаги, используемые функцией [**двмсетвиндоваттрибуте**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute) для указания политики окна Flip3D.</span><span class="sxs-lookup"><span data-stu-id="25702-125">Flags used by the [**DwmSetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute) function to specify the Flip3D window policy.</span></span><br/>                                                                               |
| [<span data-ttu-id="25702-126">**двмнкрендерингполици**</span><span class="sxs-lookup"><span data-stu-id="25702-126">**DWMNCRENDERINGPOLICY**</span></span>](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmncrenderingpolicy)<br/>                           | <span data-ttu-id="25702-127">Флаги, используемые функцией [**двмсетвиндоваттрибуте**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute) для указания политики визуализации неклиентской области.</span><span class="sxs-lookup"><span data-stu-id="25702-127">Flags used by the [**DwmSetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute) function to specify the non-client area rendering policy.</span></span><br/>                                                                   |
| [<span data-ttu-id="25702-128">**\_ \_ целевой объект овнедвиндов двмтранситион**</span><span class="sxs-lookup"><span data-stu-id="25702-128">**DWMTRANSITION\_OWNEDWINDOW\_TARGET**</span></span>](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmtransition_ownedwindow_target)<br/> | <span data-ttu-id="25702-129">Определяет целевой объект.</span><span class="sxs-lookup"><span data-stu-id="25702-129">Identifies the target.</span></span><br/>                                                                                                                                                                               |
| [<span data-ttu-id="25702-130">**двмвиндоваттрибуте**</span><span class="sxs-lookup"><span data-stu-id="25702-130">**DWMWINDOWATTRIBUTE**</span></span>](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmwindowattribute)<br/>                               | <span data-ttu-id="25702-131">Флаги, используемые функциями [**двмжетвиндоваттрибуте**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetwindowattribute) и [**двмсетвиндоваттрибуте**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute) для указания атрибутов окна для отрисовки без клиента.</span><span class="sxs-lookup"><span data-stu-id="25702-131">Flags used by the [**DwmGetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetwindowattribute) and [**DwmSetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute) functions to specify window attributes for non-client rendering.</span></span><br/> |
| [<span data-ttu-id="25702-132">**Тип ЖЕСТа \_**</span><span class="sxs-lookup"><span data-stu-id="25702-132">**GESTURE\_TYPE**</span></span>](/windows/desktop/api/Dwmapi/ne-dwmapi-gesture_type)<br/>                                          | <span data-ttu-id="25702-133">Идентифицирует тип жеста, указанный в [**двмрендержестуре**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmrendergesture).</span><span class="sxs-lookup"><span data-stu-id="25702-133">Identifies the gesture type specified in [**DwmRenderGesture**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmrendergesture).</span></span><br/>                                                                                                               |



 

 

 





