---
description: Определяет идентификаторы ресурсов для общих строковых ресурсов.
MS-HAID: vspixengine.Resource\_Id
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Перечисление Resource_Id
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: CC04FDC4-CD35-4A87-8EE8-48FFA07B8FC0
api_name:
- Resource_Id
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 1e7d93111defb01000e32e4f5ade0c9eb09c827e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537571"
---
# <a name="span-idvspixengineresource_idspanresource_id-enumeration"></a><span data-ttu-id="60bc3-103"><span id="vspixengine.resource_id"></span>\_Перечисление идентификаторов ресурсов</span><span class="sxs-lookup"><span data-stu-id="60bc3-103"><span id="vspixengine.resource_id"></span>Resource\_Id enumeration</span></span>

<span data-ttu-id="60bc3-104">Определяет идентификаторы ресурсов для общих строковых ресурсов.</span><span class="sxs-lookup"><span data-stu-id="60bc3-104">Defines resource IDs for shared string resources.</span></span> <span data-ttu-id="60bc3-105">Они передаются подсистеме захвата из узла.</span><span class="sxs-lookup"><span data-stu-id="60bc3-105">These are passed to the capture engine from the host.</span></span> <span data-ttu-id="60bc3-106">Они используются для отображения строк в наложение HUD передаваемого приложения или для передачи значений реестра из параметров Visual Studio в запись Енги</span><span class="sxs-lookup"><span data-stu-id="60bc3-106">They are used to display strings to the HUD overlay of the app being captured or to pass registry values from Visual Studio options to the capture engi</span></span>

## <a name="syntax"></a><span data-ttu-id="60bc3-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="60bc3-107">Syntax</span></span>


```C++
};
```

## <a name="constants"></a><span data-ttu-id="60bc3-108">Константы</span><span class="sxs-lookup"><span data-stu-id="60bc3-108">Constants</span></span>

<span data-ttu-id="60bc3-109"><span id="IDS_ENGINEDISCONNECTED"></span><span id="ids_enginedisconnected"></span>**ИДЕНТИФИКАТОРы \_ енгинедисконнектед**</span><span class="sxs-lookup"><span data-stu-id="60bc3-109"><span id="IDS_ENGINEDISCONNECTED"></span><span id="ids_enginedisconnected"></span>**IDS\_ENGINEDISCONNECTED**</span></span>  
<span data-ttu-id="60bc3-110">Не используется.</span><span class="sxs-lookup"><span data-stu-id="60bc3-110">Not used.</span></span> <span data-ttu-id="60bc3-111">Идентификатор ресурса для строки ранее использовался, чтобы указать, что принтскрин был достигнут после завершения сеанса записи.</span><span class="sxs-lookup"><span data-stu-id="60bc3-111">Resource id for string formerly used to indicate that printscreen was hit after the capture session was complete.</span></span>

<span data-ttu-id="60bc3-112"><span id="IDR_RCDATA1"></span><span id="idr_rcdata1"></span>**IDR \_ RCDATA1**</span><span class="sxs-lookup"><span data-stu-id="60bc3-112"><span id="IDR_RCDATA1"></span><span id="idr_rcdata1"></span>**IDR\_RCDATA1**</span></span>  
<span data-ttu-id="60bc3-113">Не используется.</span><span class="sxs-lookup"><span data-stu-id="60bc3-113">Not used.</span></span>

<span data-ttu-id="60bc3-114"><span id="IDS_DEFAULTEXPFILE_CONTENT"></span><span id="ids_defaultexpfile_content"></span>**ИДЕНТИФИКАТОРы \_ дефаултекспфиле \_ содержимого**</span><span class="sxs-lookup"><span data-stu-id="60bc3-114"><span id="IDS_DEFAULTEXPFILE_CONTENT"></span><span id="ids_defaultexpfile_content"></span>**IDS\_DEFAULTEXPFILE\_CONTENT**</span></span>  
<span data-ttu-id="60bc3-115">Не используется.</span><span class="sxs-lookup"><span data-stu-id="60bc3-115">Not used.</span></span> <span data-ttu-id="60bc3-116">Идентификатор ресурса для строки ранее использовался для XML-данных в сценариях записи прежних версий.</span><span class="sxs-lookup"><span data-stu-id="60bc3-116">Resource id for string formerly used for XML data in legacy capture scenarios.</span></span>

<span data-ttu-id="60bc3-117"><span id="IDS_CAPTURE_MESSAGE"></span><span id="ids_capture_message"></span>**\_сообщение захвата идентификаторов \_**</span><span class="sxs-lookup"><span data-stu-id="60bc3-117"><span id="IDS_CAPTURE_MESSAGE"></span><span id="ids_capture_message"></span>**IDS\_CAPTURE\_MESSAGE**</span></span>  
<span data-ttu-id="60bc3-118">Идентификатор ресурса для строки "захваченный кадр".</span><span class="sxs-lookup"><span data-stu-id="60bc3-118">Resource ID for string "Captured frame."</span></span>

<span data-ttu-id="60bc3-119"><span id="IDS_CAPTURE_NOT_SUPPORTED"></span><span id="ids_capture_not_supported"></span>**запись ИДЕНТИФИКАТОРов \_ \_ не \_ поддерживается**</span><span class="sxs-lookup"><span data-stu-id="60bc3-119"><span id="IDS_CAPTURE_NOT_SUPPORTED"></span><span id="ids_capture_not_supported"></span>**IDS\_CAPTURE\_NOT\_SUPPORTED**</span></span>  
<span data-ttu-id="60bc3-120">Идентификатор ресурса для строки "Эта программа сообщила, что ее нельзя использовать с диагностика графики инструментами".</span><span class="sxs-lookup"><span data-stu-id="60bc3-120">Resource ID for string "This program has indicated that it cannot be used with Graphics Diagnostics tools."</span></span>

<span data-ttu-id="60bc3-121"><span id="IDS_CAPTURE_NOT_SUPPORTED_TITLE"></span><span id="ids_capture_not_supported_title"></span>**Заголовок "запись ИДЕНТИФИКАТОРов \_ \_ не \_ поддерживается \_ "**</span><span class="sxs-lookup"><span data-stu-id="60bc3-121"><span id="IDS_CAPTURE_NOT_SUPPORTED_TITLE"></span><span id="ids_capture_not_supported_title"></span>**IDS\_CAPTURE\_NOT\_SUPPORTED\_TITLE**</span></span>  
<span data-ttu-id="60bc3-122">Идентификатор ресурса для строки "неподдерживаемые функции"</span><span class="sxs-lookup"><span data-stu-id="60bc3-122">Resource ID for string "Unsupported functionality"</span></span>

<span data-ttu-id="60bc3-123"><span id="IDS_FEATURE_NOT_SUPPORTED"></span><span id="ids_feature_not_supported"></span>**Функция ИДЕНТИФИКАТОРов \_ \_ не \_ поддерживается**</span><span class="sxs-lookup"><span data-stu-id="60bc3-123"><span id="IDS_FEATURE_NOT_SUPPORTED"></span><span id="ids_feature_not_supported"></span>**IDS\_FEATURE\_NOT\_SUPPORTED**</span></span>  
<span data-ttu-id="60bc3-124">Идентификатор ресурса для строки "уровень компонентов устройства не поддерживается"</span><span class="sxs-lookup"><span data-stu-id="60bc3-124">Resource ID for string "Device feature level not supported"</span></span>

<span data-ttu-id="60bc3-125"><span id="IDS_DXVERSION_NOT_SUPPORTED"></span><span id="ids_dxversion_not_supported"></span>**ИДЕНТИФИКАТОРы \_ дксверсион \_ не \_ поддерживаются**</span><span class="sxs-lookup"><span data-stu-id="60bc3-125"><span id="IDS_DXVERSION_NOT_SUPPORTED"></span><span id="ids_dxversion_not_supported"></span>**IDS\_DXVERSION\_NOT\_SUPPORTED**</span></span>  
<span data-ttu-id="60bc3-126">Идентификатор ресурса для строки "версия DirectX не подписывается"</span><span class="sxs-lookup"><span data-stu-id="60bc3-126">Resource ID for string "DirectX version not capturable"</span></span>

<span data-ttu-id="60bc3-127"><span id="IDS_DCOMP_NOT_SUPPORTED"></span><span id="ids_dcomp_not_supported"></span>**ИДЕНТИФИКАТОРы \_ дкомп \_ не \_ поддерживаются**</span><span class="sxs-lookup"><span data-stu-id="60bc3-127"><span id="IDS_DCOMP_NOT_SUPPORTED"></span><span id="ids_dcomp_not_supported"></span>**IDS\_DCOMP\_NOT\_SUPPORTED**</span></span>  
<span data-ttu-id="60bc3-128">Идентификатор ресурса для строки "ДКОМП используется приложением, но не поддерживается в этой ОС"</span><span class="sxs-lookup"><span data-stu-id="60bc3-128">Resource ID for string "DCOMP in use by app but not supported on this OS"</span></span>

<span data-ttu-id="60bc3-129"><span id="IDS_DWRITE_NOT_SUPPORTED"></span><span id="ids_dwrite_not_supported"></span>**ИДЕНТИФИКАТОРы \_ дврите \_ не \_ поддерживаются**</span><span class="sxs-lookup"><span data-stu-id="60bc3-129"><span id="IDS_DWRITE_NOT_SUPPORTED"></span><span id="ids_dwrite_not_supported"></span>**IDS\_DWRITE\_NOT\_SUPPORTED**</span></span>  
<span data-ttu-id="60bc3-130">Идентификатор ресурса для строки "ДВРИТЕ используется приложением, но не поддерживается в этой ОС"</span><span class="sxs-lookup"><span data-stu-id="60bc3-130">Resource ID for string "DWRITE in use by app but not supported on this OS"</span></span>

<span data-ttu-id="60bc3-131"><span id="IDS_EXPECTED_FAILURE_FORMAT"></span><span id="ids_expected_failure_format"></span>**ИДЕНТИФИКАТОРы \_ ожидаемого \_ \_ формата сбоя**</span><span class="sxs-lookup"><span data-stu-id="60bc3-131"><span id="IDS_EXPECTED_FAILURE_FORMAT"></span><span id="ids_expected_failure_format"></span>**IDS\_EXPECTED\_FAILURE\_FORMAT**</span></span>  
<span data-ttu-id="60bc3-132">Идентификатор ресурса для строки "% s" вернул ошибку во время воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="60bc3-132">Resource ID for string "%s returned an error during playback.</span></span> <span data-ttu-id="60bc3-133">(HRESULT =% s) \\ r \\ n ".</span><span class="sxs-lookup"><span data-stu-id="60bc3-133">(HRESULT=%s)\\r\\n".</span></span>

<span data-ttu-id="60bc3-134"><span id="IDS_CAPTURETOOLTIP_MESSAGE"></span><span id="ids_capturetooltip_message"></span>**Идентификатор \_ \_ сообщения каптуретултип**</span><span class="sxs-lookup"><span data-stu-id="60bc3-134"><span id="IDS_CAPTURETOOLTIP_MESSAGE"></span><span id="ids_capturetooltip_message"></span>**IDS\_CAPTURETOOLTIP\_MESSAGE**</span></span>  
<span data-ttu-id="60bc3-135">Идентификатор ресурса для строки "используйте параметр" Печать экрана "для записи кадра."</span><span class="sxs-lookup"><span data-stu-id="60bc3-135">Resource ID for string "Use 'Print Screen' key to capture a frame."</span></span>

<span data-ttu-id="60bc3-136"><span id="IDS_D2D_AND_D10_NOT_SUPPORTED"></span><span id="ids_d2d_and_d10_not_supported"></span>**ИДЕНТИФИКАТОРы \_ D2D \_ и \_ D10 \_ не \_ поддерживаются**</span><span class="sxs-lookup"><span data-stu-id="60bc3-136"><span id="IDS_D2D_AND_D10_NOT_SUPPORTED"></span><span id="ids_d2d_and_d10_not_supported"></span>**IDS\_D2D\_AND\_D10\_NOT\_SUPPORTED**</span></span>  
<span data-ttu-id="60bc3-137">Идентификатор ресурса для строки "D2D и D10 не поддерживаются вместе в этой ОС"</span><span class="sxs-lookup"><span data-stu-id="60bc3-137">Resource ID for string "D2D and D10 not supported together on this OS"</span></span>

<span data-ttu-id="60bc3-138"><span id="IDS_HUD_STATISTICS"></span><span id="ids_hud_statistics"></span>**\_Статистика HUDности идентификаторов \_**</span><span class="sxs-lookup"><span data-stu-id="60bc3-138"><span id="IDS_HUD_STATISTICS"></span><span id="ids_hud_statistics"></span>**IDS\_HUD\_STATISTICS**</span></span>  
<span data-ttu-id="60bc3-139">Идентификатор ресурса для строки "кадров перехвачено% d".</span><span class="sxs-lookup"><span data-stu-id="60bc3-139">Resource ID for string "Frames captured %d.</span></span> <span data-ttu-id="60bc3-140">Время кадра (МС)% 0.00 f "</span><span class="sxs-lookup"><span data-stu-id="60bc3-140">Frame time (ms) %0.00f"</span></span>

<span data-ttu-id="60bc3-141"><span id="IDS_INTERNAL_METHOD"></span><span id="ids_internal_method"></span>**\_внутренний \_ метод ID**</span><span class="sxs-lookup"><span data-stu-id="60bc3-141"><span id="IDS_INTERNAL_METHOD"></span><span id="ids_internal_method"></span>**IDS\_INTERNAL\_METHOD**</span></span>  
<span data-ttu-id="60bc3-142">Идентификатор ресурса для строки "внутренний метод DirectX"</span><span class="sxs-lookup"><span data-stu-id="60bc3-142">Resource ID for string "Directx Internal Method"</span></span>

<span data-ttu-id="60bc3-143"><span id="IDS_CAPTURE_FRAME_MARK"></span><span id="ids_capture_frame_mark"></span>**\_ \_ метки кадра захвата идентификаторов \_**</span><span class="sxs-lookup"><span data-stu-id="60bc3-143"><span id="IDS_CAPTURE_FRAME_MARK"></span><span id="ids_capture_frame_mark"></span>**IDS\_CAPTURE\_FRAME\_MARK**</span></span>  
<span data-ttu-id="60bc3-144">Идентификатор ресурса для строки "захваченный кадр% ld"</span><span class="sxs-lookup"><span data-stu-id="60bc3-144">Resource ID for string "Captured Frame %ld"</span></span>

<span data-ttu-id="60bc3-145"><span id="PIPELINESTAGE_INPUTASSEMBLER"></span><span id="pipelinestage_inputassembler"></span>**ПИПЕЛИНЕСТАЖЕ \_ инпутассемблер**</span><span class="sxs-lookup"><span data-stu-id="60bc3-145"><span id="PIPELINESTAGE_INPUTASSEMBLER"></span><span id="pipelinestage_inputassembler"></span>**PIPELINESTAGE\_INPUTASSEMBLER**</span></span>  
<span data-ttu-id="60bc3-146">Не используется.</span><span class="sxs-lookup"><span data-stu-id="60bc3-146">Not used.</span></span>

<span data-ttu-id="60bc3-147"><span id="PIPELINESTAGE_VERTEXSHADER"></span><span id="pipelinestage_vertexshader"></span>**ПИПЕЛИНЕСТАЖЕ \_ вертексшадер**</span><span class="sxs-lookup"><span data-stu-id="60bc3-147"><span id="PIPELINESTAGE_VERTEXSHADER"></span><span id="pipelinestage_vertexshader"></span>**PIPELINESTAGE\_VERTEXSHADER**</span></span>  
<span data-ttu-id="60bc3-148">Не используется.</span><span class="sxs-lookup"><span data-stu-id="60bc3-148">Not used.</span></span>

<span data-ttu-id="60bc3-149"><span id="PIPELINESTAGE_HULLSHADER"></span><span id="pipelinestage_hullshader"></span>**ПИПЕЛИНЕСТАЖЕ \_ хуллшадер**</span><span class="sxs-lookup"><span data-stu-id="60bc3-149"><span id="PIPELINESTAGE_HULLSHADER"></span><span id="pipelinestage_hullshader"></span>**PIPELINESTAGE\_HULLSHADER**</span></span>  
<span data-ttu-id="60bc3-150">Не используется.</span><span class="sxs-lookup"><span data-stu-id="60bc3-150">Not used.</span></span>

<span data-ttu-id="60bc3-151"><span id="PIPELINESTAGE_TESSELATOR"></span><span id="pipelinestage_tesselator"></span>**ПИПЕЛИНЕСТАЖЕ \_ тесселатор**</span><span class="sxs-lookup"><span data-stu-id="60bc3-151"><span id="PIPELINESTAGE_TESSELATOR"></span><span id="pipelinestage_tesselator"></span>**PIPELINESTAGE\_TESSELATOR**</span></span>  
<span data-ttu-id="60bc3-152">Не используется.</span><span class="sxs-lookup"><span data-stu-id="60bc3-152">Not used.</span></span>

<span data-ttu-id="60bc3-153"><span id="PIPELINESTAGE_DOMAINSHADER"></span><span id="pipelinestage_domainshader"></span>**ПИПЕЛИНЕСТАЖЕ \_ домаиншадер**</span><span class="sxs-lookup"><span data-stu-id="60bc3-153"><span id="PIPELINESTAGE_DOMAINSHADER"></span><span id="pipelinestage_domainshader"></span>**PIPELINESTAGE\_DOMAINSHADER**</span></span>  
<span data-ttu-id="60bc3-154">Не используется.</span><span class="sxs-lookup"><span data-stu-id="60bc3-154">Not used.</span></span>

<span data-ttu-id="60bc3-155"><span id="PIPELINESTAGE_GEOMETRYSHADER"></span><span id="pipelinestage_geometryshader"></span>**ПИПЕЛИНЕСТАЖЕ \_ жеометришадер**</span><span class="sxs-lookup"><span data-stu-id="60bc3-155"><span id="PIPELINESTAGE_GEOMETRYSHADER"></span><span id="pipelinestage_geometryshader"></span>**PIPELINESTAGE\_GEOMETRYSHADER**</span></span>  
<span data-ttu-id="60bc3-156">Не используется.</span><span class="sxs-lookup"><span data-stu-id="60bc3-156">Not used.</span></span>

<span data-ttu-id="60bc3-157"><span id="PIPELINESTAGE_STREAMOUTPUT"></span><span id="pipelinestage_streamoutput"></span>**ПИПЕЛИНЕСТАЖЕ \_ стреамаутпут**</span><span class="sxs-lookup"><span data-stu-id="60bc3-157"><span id="PIPELINESTAGE_STREAMOUTPUT"></span><span id="pipelinestage_streamoutput"></span>**PIPELINESTAGE\_STREAMOUTPUT**</span></span>  
<span data-ttu-id="60bc3-158">Не используется.</span><span class="sxs-lookup"><span data-stu-id="60bc3-158">Not used.</span></span>

<span data-ttu-id="60bc3-159"><span id="PIPELINESTAGE_RASTERIZER"></span><span id="pipelinestage_rasterizer"></span>**средство программной \_ прорисовки пипелинестаже**</span><span class="sxs-lookup"><span data-stu-id="60bc3-159"><span id="PIPELINESTAGE_RASTERIZER"></span><span id="pipelinestage_rasterizer"></span>**PIPELINESTAGE\_RASTERIZER**</span></span>  
<span data-ttu-id="60bc3-160">Не используется.</span><span class="sxs-lookup"><span data-stu-id="60bc3-160">Not used.</span></span>

<span data-ttu-id="60bc3-161"><span id="PIPELINESTAGE_PIXELSHADER"></span><span id="pipelinestage_pixelshader"></span>**ПИПЕЛИНЕСТАЖЕ \_ PIXELSHADER**</span><span class="sxs-lookup"><span data-stu-id="60bc3-161"><span id="PIPELINESTAGE_PIXELSHADER"></span><span id="pipelinestage_pixelshader"></span>**PIPELINESTAGE\_PIXELSHADER**</span></span>  
<span data-ttu-id="60bc3-162">Не используется.</span><span class="sxs-lookup"><span data-stu-id="60bc3-162">Not used.</span></span>

<span data-ttu-id="60bc3-163"><span id="PIPELINESTAGE_OUTPUTMERGER"></span><span id="pipelinestage_outputmerger"></span>**ПИПЕЛИНЕСТАЖЕ \_ аутпутмержер**</span><span class="sxs-lookup"><span data-stu-id="60bc3-163"><span id="PIPELINESTAGE_OUTPUTMERGER"></span><span id="pipelinestage_outputmerger"></span>**PIPELINESTAGE\_OUTPUTMERGER**</span></span>  
<span data-ttu-id="60bc3-164">Не используется.</span><span class="sxs-lookup"><span data-stu-id="60bc3-164">Not used.</span></span>

<span data-ttu-id="60bc3-165"><span id="PIPELINESTAGE_COMPUTESHADER"></span><span id="pipelinestage_computeshader"></span>**ПИПЕЛИНЕСТАЖЕ \_ компутешадер**</span><span class="sxs-lookup"><span data-stu-id="60bc3-165"><span id="PIPELINESTAGE_COMPUTESHADER"></span><span id="pipelinestage_computeshader"></span>**PIPELINESTAGE\_COMPUTESHADER**</span></span>  
<span data-ttu-id="60bc3-166">Не используется.</span><span class="sxs-lookup"><span data-stu-id="60bc3-166">Not used.</span></span>

<span data-ttu-id="60bc3-167"><span id="BUFFEROBJECT_SUPPORTEDFORMAT"></span><span id="bufferobject_supportedformat"></span>**БУФФЕРОБЖЕКТ \_ суппортедформат**</span><span class="sxs-lookup"><span data-stu-id="60bc3-167"><span id="BUFFEROBJECT_SUPPORTEDFORMAT"></span><span id="bufferobject_supportedformat"></span>**BUFFEROBJECT\_SUPPORTEDFORMAT**</span></span>  
<span data-ttu-id="60bc3-168">Не используется.</span><span class="sxs-lookup"><span data-stu-id="60bc3-168">Not used.</span></span>

<span data-ttu-id="60bc3-169"><span id="BUFFEROBJECT_CURRENTFORMAT"></span><span id="bufferobject_currentformat"></span>**БУФФЕРОБЖЕКТ \_ куррентформат**</span><span class="sxs-lookup"><span data-stu-id="60bc3-169"><span id="BUFFEROBJECT_CURRENTFORMAT"></span><span id="bufferobject_currentformat"></span>**BUFFEROBJECT\_CURRENTFORMAT**</span></span>  
<span data-ttu-id="60bc3-170">Не используется.</span><span class="sxs-lookup"><span data-stu-id="60bc3-170">Not used.</span></span>

<span data-ttu-id="60bc3-171"><span id="BUFFEROBJECT_HEADER"></span><span id="bufferobject_header"></span>**\_заголовок буфферобжект**</span><span class="sxs-lookup"><span data-stu-id="60bc3-171"><span id="BUFFEROBJECT_HEADER"></span><span id="bufferobject_header"></span>**BUFFEROBJECT\_HEADER**</span></span>  
<span data-ttu-id="60bc3-172">Не используется.</span><span class="sxs-lookup"><span data-stu-id="60bc3-172">Not used.</span></span>

<span data-ttu-id="60bc3-173"><span id="BUFFEROBJECT_LINE"></span><span id="bufferobject_line"></span>**БУФФЕРОБЖЕКТ \_ строка**</span><span class="sxs-lookup"><span data-stu-id="60bc3-173"><span id="BUFFEROBJECT_LINE"></span><span id="bufferobject_line"></span>**BUFFEROBJECT\_LINE**</span></span>  
<span data-ttu-id="60bc3-174">Не используется.</span><span class="sxs-lookup"><span data-stu-id="60bc3-174">Not used.</span></span>

<span data-ttu-id="60bc3-175"><span id="BUFFEROBJECT_INVALIDFORMAT"></span><span id="bufferobject_invalidformat"></span>**БУФФЕРОБЖЕКТ \_ инвалидформат**</span><span class="sxs-lookup"><span data-stu-id="60bc3-175"><span id="BUFFEROBJECT_INVALIDFORMAT"></span><span id="bufferobject_invalidformat"></span>**BUFFEROBJECT\_INVALIDFORMAT**</span></span>  
<span data-ttu-id="60bc3-176">Не используется.</span><span class="sxs-lookup"><span data-stu-id="60bc3-176">Not used.</span></span>

<span data-ttu-id="60bc3-177"><span id="BUFFEROBJECT_INVALIDEMPTYFORMAT"></span><span id="bufferobject_invalidemptyformat"></span>**БУФФЕРОБЖЕКТ \_ инвалидемптиформат**</span><span class="sxs-lookup"><span data-stu-id="60bc3-177"><span id="BUFFEROBJECT_INVALIDEMPTYFORMAT"></span><span id="bufferobject_invalidemptyformat"></span>**BUFFEROBJECT\_INVALIDEMPTYFORMAT**</span></span>  
<span data-ttu-id="60bc3-178">Не используется.</span><span class="sxs-lookup"><span data-stu-id="60bc3-178">Not used.</span></span>

<span data-ttu-id="60bc3-179"><span id="BUFFEROBJECT_INVALIDFORMATSIZE"></span><span id="bufferobject_invalidformatsize"></span>**БУФФЕРОБЖЕКТ \_ инвалидформатсизе**</span><span class="sxs-lookup"><span data-stu-id="60bc3-179"><span id="BUFFEROBJECT_INVALIDFORMATSIZE"></span><span id="bufferobject_invalidformatsize"></span>**BUFFEROBJECT\_INVALIDFORMATSIZE**</span></span>  
<span data-ttu-id="60bc3-180">Не используется.</span><span class="sxs-lookup"><span data-stu-id="60bc3-180">Not used.</span></span>

<span data-ttu-id="60bc3-181"><span id="SUMMARYINFO_TARGETAPPLICATION"></span><span id="summaryinfo_targetapplication"></span>**СУММАРИНФО \_ таржетаппликатион**</span><span class="sxs-lookup"><span data-stu-id="60bc3-181"><span id="SUMMARYINFO_TARGETAPPLICATION"></span><span id="summaryinfo_targetapplication"></span>**SUMMARYINFO\_TARGETAPPLICATION**</span></span>  
<span data-ttu-id="60bc3-182">Текст, отображаемый в окне "свойства vsglog" — целевое приложение</span><span class="sxs-lookup"><span data-stu-id="60bc3-182">Text shown in the vsglog properties window - Target Application</span></span>

<span data-ttu-id="60bc3-183"><span id="SUMMARYINFO_PATH"></span><span id="summaryinfo_path"></span>**\_путь суммаринфо**</span><span class="sxs-lookup"><span data-stu-id="60bc3-183"><span id="SUMMARYINFO_PATH"></span><span id="summaryinfo_path"></span>**SUMMARYINFO\_PATH**</span></span>  
<span data-ttu-id="60bc3-184">Текст, отображаемый в vsglog окно свойств-Path</span><span class="sxs-lookup"><span data-stu-id="60bc3-184">Text shown in the vsglog Properties window - Path</span></span>

<span data-ttu-id="60bc3-185"><span id="SUMMARYINFO_TARGETVERSION"></span><span id="summaryinfo_targetversion"></span>**СУММАРИНФО \_ TARGETVERSION**</span><span class="sxs-lookup"><span data-stu-id="60bc3-185"><span id="SUMMARYINFO_TARGETVERSION"></span><span id="summaryinfo_targetversion"></span>**SUMMARYINFO\_TARGETVERSION**</span></span>  
<span data-ttu-id="60bc3-186">Текст, отображаемый в vsglog окно свойств — Целевая версия</span><span class="sxs-lookup"><span data-stu-id="60bc3-186">Text shown in the vsglog Properties window - Target Version</span></span>

<span data-ttu-id="60bc3-187"><span id="SUMMARYINFO_LASTMODIFIEDDATE"></span><span id="summaryinfo_lastmodifieddate"></span>**СУММАРИНФО \_ LASTMODIFIEDDATE**</span><span class="sxs-lookup"><span data-stu-id="60bc3-187"><span id="SUMMARYINFO_LASTMODIFIEDDATE"></span><span id="summaryinfo_lastmodifieddate"></span>**SUMMARYINFO\_LASTMODIFIEDDATE**</span></span>  
<span data-ttu-id="60bc3-188">Текст, отображаемый в vsglog окно свойств — Дата последнего изменения</span><span class="sxs-lookup"><span data-stu-id="60bc3-188">Text shown in the vsglog Properties window - Last Modified Date</span></span>

<span data-ttu-id="60bc3-189"><span id="SUMMARYINFO_PROCESSID"></span><span id="summaryinfo_processid"></span>**Идентификатор \_ процесса суммаринфо**</span><span class="sxs-lookup"><span data-stu-id="60bc3-189"><span id="SUMMARYINFO_PROCESSID"></span><span id="summaryinfo_processid"></span>**SUMMARYINFO\_PROCESSID**</span></span>  
<span data-ttu-id="60bc3-190">Текст, отображаемый в vsglog окно свойств — идентификатор процесса</span><span class="sxs-lookup"><span data-stu-id="60bc3-190">Text shown in the vsglog Properties window - Process ID</span></span>

<span data-ttu-id="60bc3-191"><span id="SUMMARYINFO_EXPERIMENTFILE"></span><span id="summaryinfo_experimentfile"></span>**СУММАРИНФО \_ експериментфиле**</span><span class="sxs-lookup"><span data-stu-id="60bc3-191"><span id="SUMMARYINFO_EXPERIMENTFILE"></span><span id="summaryinfo_experimentfile"></span>**SUMMARYINFO\_EXPERIMENTFILE**</span></span>  
<span data-ttu-id="60bc3-192">Текст, отображаемый в файле vsglog окно свойств-эксперименте</span><span class="sxs-lookup"><span data-stu-id="60bc3-192">Text shown in the vsglog Properties window - Experiment File</span></span>

<span data-ttu-id="60bc3-193"><span id="SUMMARYINFO_RUNFILE"></span><span id="summaryinfo_runfile"></span>**СУММАРИНФО \_ рунфиле**</span><span class="sxs-lookup"><span data-stu-id="60bc3-193"><span id="SUMMARYINFO_RUNFILE"></span><span id="summaryinfo_runfile"></span>**SUMMARYINFO\_RUNFILE**</span></span>  
<span data-ttu-id="60bc3-194">Текст, отображаемый в файле vsglog окно свойств-Run</span><span class="sxs-lookup"><span data-stu-id="60bc3-194">Text shown in the vsglog Properties window - Run File</span></span>

<span data-ttu-id="60bc3-195"><span id="SUMMARYINFO_SIZE"></span><span id="summaryinfo_size"></span>**\_Размер суммаринфо**</span><span class="sxs-lookup"><span data-stu-id="60bc3-195"><span id="SUMMARYINFO_SIZE"></span><span id="summaryinfo_size"></span>**SUMMARYINFO\_SIZE**</span></span>  
<span data-ttu-id="60bc3-196">Текст, отображаемый в vsglog окно свойств-size</span><span class="sxs-lookup"><span data-stu-id="60bc3-196">Text shown in the vsglog Properties window - Size</span></span>

<span data-ttu-id="60bc3-197"><span id="SUMMARYINFO_CREATEDBYPIXVERSION"></span><span id="summaryinfo_createdbypixversion"></span>**СУММАРИНФО \_ креатедбипиксверсион**</span><span class="sxs-lookup"><span data-stu-id="60bc3-197"><span id="SUMMARYINFO_CREATEDBYPIXVERSION"></span><span id="summaryinfo_createdbypixversion"></span>**SUMMARYINFO\_CREATEDBYPIXVERSION**</span></span>  
<span data-ttu-id="60bc3-198">Текст, отображаемый в vsglog окно свойств, созданная по версии</span><span class="sxs-lookup"><span data-stu-id="60bc3-198">Text shown in the vsglog Properties window - Created By Version</span></span>

<span data-ttu-id="60bc3-199"><span id="SUMMARYINFO_SESSIONSTARTTIME"></span><span id="summaryinfo_sessionstarttime"></span>**СУММАРИНФО \_ сессионстарттиме**</span><span class="sxs-lookup"><span data-stu-id="60bc3-199"><span id="SUMMARYINFO_SESSIONSTARTTIME"></span><span id="summaryinfo_sessionstarttime"></span>**SUMMARYINFO\_SESSIONSTARTTIME**</span></span>  
<span data-ttu-id="60bc3-200">Текст, отображаемый в vsglog окно свойств — время начала сеанса</span><span class="sxs-lookup"><span data-stu-id="60bc3-200">Text shown in the vsglog Properties window - Session Start time</span></span>

<span data-ttu-id="60bc3-201"><span id="SUMMARYINFO_SYSTEMINFORMATION"></span><span id="summaryinfo_systeminformation"></span>**СУММАРИНФО \_ SYSTEMINFORMATION**</span><span class="sxs-lookup"><span data-stu-id="60bc3-201"><span id="SUMMARYINFO_SYSTEMINFORMATION"></span><span id="summaryinfo_systeminformation"></span>**SUMMARYINFO\_SYSTEMINFORMATION**</span></span>  
<span data-ttu-id="60bc3-202">Текст, отображаемый в vsglog окно свойств-системная информация</span><span class="sxs-lookup"><span data-stu-id="60bc3-202">Text shown in the vsglog Properties window - System Information</span></span>

<span data-ttu-id="60bc3-203"><span id="SUMMARYINFO_PROCESSOR"></span><span id="summaryinfo_processor"></span>**\_процессор суммаринфо**</span><span class="sxs-lookup"><span data-stu-id="60bc3-203"><span id="SUMMARYINFO_PROCESSOR"></span><span id="summaryinfo_processor"></span>**SUMMARYINFO\_PROCESSOR**</span></span>  
<span data-ttu-id="60bc3-204">Текст, отображаемый в vsglog окно свойств-Processor</span><span class="sxs-lookup"><span data-stu-id="60bc3-204">Text shown in the vsglog Properties window - Processor</span></span>

<span data-ttu-id="60bc3-205"><span id="SUMMARYINFO_MEMORY"></span><span id="summaryinfo_memory"></span>**\_память суммаринфо**</span><span class="sxs-lookup"><span data-stu-id="60bc3-205"><span id="SUMMARYINFO_MEMORY"></span><span id="summaryinfo_memory"></span>**SUMMARYINFO\_MEMORY**</span></span>  
<span data-ttu-id="60bc3-206">Текст, отображаемый в vsglog окно свойств-Memory</span><span class="sxs-lookup"><span data-stu-id="60bc3-206">Text shown in the vsglog Properties window - Memory</span></span>

<span data-ttu-id="60bc3-207"><span id="SUMMARYINFO_OSVERSION"></span><span id="summaryinfo_osversion"></span>**СУММАРИНФО \_ OSVersion**</span><span class="sxs-lookup"><span data-stu-id="60bc3-207"><span id="SUMMARYINFO_OSVERSION"></span><span id="summaryinfo_osversion"></span>**SUMMARYINFO\_OSVERSION**</span></span>  
<span data-ttu-id="60bc3-208">Текст, отображаемый в vsglog окно свойств — версия ОС</span><span class="sxs-lookup"><span data-stu-id="60bc3-208">Text shown in the vsglog Properties window - OS Version</span></span>

<span data-ttu-id="60bc3-209"><span id="SUMMARYINFO_OSARCHITECTURE"></span><span id="summaryinfo_osarchitecture"></span>**СУММАРИНФО \_ осарчитектуре**</span><span class="sxs-lookup"><span data-stu-id="60bc3-209"><span id="SUMMARYINFO_OSARCHITECTURE"></span><span id="summaryinfo_osarchitecture"></span>**SUMMARYINFO\_OSARCHITECTURE**</span></span>  
<span data-ttu-id="60bc3-210">Текст, отображаемый в архитектуре окно свойств vsglog-OS</span><span class="sxs-lookup"><span data-stu-id="60bc3-210">Text shown in the vsglog Properties window - OS Architecture</span></span>

<span data-ttu-id="60bc3-211"><span id="SUMMARYINFO_TARGETAPPARCHITECTURE"></span><span id="summaryinfo_targetapparchitecture"></span>**СУММАРИНФО \_ таржетаппарчитектуре**</span><span class="sxs-lookup"><span data-stu-id="60bc3-211"><span id="SUMMARYINFO_TARGETAPPARCHITECTURE"></span><span id="summaryinfo_targetapparchitecture"></span>**SUMMARYINFO\_TARGETAPPARCHITECTURE**</span></span>  
<span data-ttu-id="60bc3-212">Текст, отображаемый в архитектуре vsglog окно свойств-Target App</span><span class="sxs-lookup"><span data-stu-id="60bc3-212">Text shown in the vsglog Properties window - Target App Architecture</span></span>

<span data-ttu-id="60bc3-213"><span id="SUMMARYINFO_MAXHWFEATURELEVEL"></span><span id="summaryinfo_maxhwfeaturelevel"></span>**СУММАРИНФО \_ максхвфеатурелевел**</span><span class="sxs-lookup"><span data-stu-id="60bc3-213"><span id="SUMMARYINFO_MAXHWFEATURELEVEL"></span><span id="summaryinfo_maxhwfeaturelevel"></span>**SUMMARYINFO\_MAXHWFEATURELEVEL**</span></span>  
<span data-ttu-id="60bc3-214">Текст, отображаемый в vsglog окно свойств — максимальный уровень компонентов оборудования</span><span class="sxs-lookup"><span data-stu-id="60bc3-214">Text shown in the vsglog Properties window - Max Hardware Feature Level</span></span>

<span data-ttu-id="60bc3-215"><span id="SUMMARYINFO_DRIVERCONCURRENTCREATES"></span><span id="summaryinfo_driverconcurrentcreates"></span>**СУММАРИНФО \_ дриверконкурренткреатес**</span><span class="sxs-lookup"><span data-stu-id="60bc3-215"><span id="SUMMARYINFO_DRIVERCONCURRENTCREATES"></span><span id="summaryinfo_driverconcurrentcreates"></span>**SUMMARYINFO\_DRIVERCONCURRENTCREATES**</span></span>  
<span data-ttu-id="60bc3-216">Текст, отображаемый в параллельном создании драйвера vsglog окно свойств-Driver</span><span class="sxs-lookup"><span data-stu-id="60bc3-216">Text shown in the vsglog Properties window - Driver Concurrent Creates</span></span>

<span data-ttu-id="60bc3-217"><span id="SUMMARYINFO_DRIVERCOMMANDLISTS"></span><span id="summaryinfo_drivercommandlists"></span>**СУММАРИНФО \_ дриверкоммандлистс**</span><span class="sxs-lookup"><span data-stu-id="60bc3-217"><span id="SUMMARYINFO_DRIVERCOMMANDLISTS"></span><span id="summaryinfo_drivercommandlists"></span>**SUMMARYINFO\_DRIVERCOMMANDLISTS**</span></span>  
<span data-ttu-id="60bc3-218">Текст, отображаемый в списках команд vsglog окно свойств-Driver</span><span class="sxs-lookup"><span data-stu-id="60bc3-218">Text shown in the vsglog Properties window - Driver Command Lists</span></span>

<span data-ttu-id="60bc3-219"><span id="SUMMARYINFO_DOUBLEPRECISIONSHADERS"></span><span id="summaryinfo_doubleprecisionshaders"></span>**СУММАРИНФО \_ даублепреЦисионшадерс**</span><span class="sxs-lookup"><span data-stu-id="60bc3-219"><span id="SUMMARYINFO_DOUBLEPRECISIONSHADERS"></span><span id="summaryinfo_doubleprecisionshaders"></span>**SUMMARYINFO\_DOUBLEPRECISIONSHADERS**</span></span>  
<span data-ttu-id="60bc3-220">Текст, отображаемый в vsglog окно свойств-шейдеры двойной точности</span><span class="sxs-lookup"><span data-stu-id="60bc3-220">Text shown in the vsglog Properties window - Double Precision Shaders</span></span>

<span data-ttu-id="60bc3-221"><span id="SUMMARYINFO_DIRECTCOMPUTECS4X"></span><span id="summaryinfo_directcomputecs4x"></span>**СУММАРИНФО \_ DIRECTCOMPUTECS4X**</span><span class="sxs-lookup"><span data-stu-id="60bc3-221"><span id="SUMMARYINFO_DIRECTCOMPUTECS4X"></span><span id="summaryinfo_directcomputecs4x"></span>**SUMMARYINFO\_DIRECTCOMPUTECS4X**</span></span>  
<span data-ttu-id="60bc3-222">Текст, отображаемый в vsglog окно свойств-Direct COMPUTE CS 4. x</span><span class="sxs-lookup"><span data-stu-id="60bc3-222">Text shown in the vsglog Properties window - Direct Compute CS 4.x</span></span>

<span data-ttu-id="60bc3-223"><span id="SUMMARYINFO_10BITXRHIGHCOLORFORMAT"></span><span id="summaryinfo_10bitxrhighcolorformat"></span>**СУММАРИНФО \_ 10BITXRHIGHCOLORFORMAT**</span><span class="sxs-lookup"><span data-stu-id="60bc3-223"><span id="SUMMARYINFO_10BITXRHIGHCOLORFORMAT"></span><span id="summaryinfo_10bitxrhighcolorformat"></span>**SUMMARYINFO\_10BITXRHIGHCOLORFORMAT**</span></span>  
<span data-ttu-id="60bc3-224">Текст, отображаемый в vsglog окно свойств-10BITXRHIGHCOLORFORMAT</span><span class="sxs-lookup"><span data-stu-id="60bc3-224">Text shown in the vsglog Properties window - 10BITXRHIGHCOLORFORMAT</span></span>

<span data-ttu-id="60bc3-225"><span id="SUMMARYINFO_EXTENDEDCOLORFORMATSUPPORT"></span><span id="summaryinfo_extendedcolorformatsupport"></span>**СУММАРИНФО \_ екстендедколорформатсуппорт**</span><span class="sxs-lookup"><span data-stu-id="60bc3-225"><span id="SUMMARYINFO_EXTENDEDCOLORFORMATSUPPORT"></span><span id="summaryinfo_extendedcolorformatsupport"></span>**SUMMARYINFO\_EXTENDEDCOLORFORMATSUPPORT**</span></span>  
<span data-ttu-id="60bc3-226">Текст, отображаемый в окно свойств vsglog. Поддержка расширенного формата цвета</span><span class="sxs-lookup"><span data-stu-id="60bc3-226">Text shown in the vsglog Properties window - Extended Color Format Support</span></span>

<span data-ttu-id="60bc3-227"><span id="SUMMARYINFO_DISPLAYINFORMATION"></span><span id="summaryinfo_displayinformation"></span>**СУММАРИНФО \_ DISPLAYINFORMATION**</span><span class="sxs-lookup"><span data-stu-id="60bc3-227"><span id="SUMMARYINFO_DISPLAYINFORMATION"></span><span id="summaryinfo_displayinformation"></span>**SUMMARYINFO\_DISPLAYINFORMATION**</span></span>  
<span data-ttu-id="60bc3-228">Текст, отображаемый в vsglog окно свойств-Отображение информации</span><span class="sxs-lookup"><span data-stu-id="60bc3-228">Text shown in the vsglog Properties window - Display Information</span></span>

<span data-ttu-id="60bc3-229"><span id="SUMMARYINFO_DISPLAYNINFORMATION"></span><span id="summaryinfo_displayninformation"></span>**СУММАРИНФО \_ дисплайнинформатион**</span><span class="sxs-lookup"><span data-stu-id="60bc3-229"><span id="SUMMARYINFO_DISPLAYNINFORMATION"></span><span id="summaryinfo_displayninformation"></span>**SUMMARYINFO\_DISPLAYNINFORMATION**</span></span>  
<span data-ttu-id="60bc3-230">Текст, отображаемый в vsglog окно свойств-дисплей N, сведения</span><span class="sxs-lookup"><span data-stu-id="60bc3-230">Text shown in the vsglog Properties window - Display N Information</span></span>

<span data-ttu-id="60bc3-231"><span id="SUMMARYINFO_NAME"></span><span id="summaryinfo_name"></span>**\_имя суммаринфо**</span><span class="sxs-lookup"><span data-stu-id="60bc3-231"><span id="SUMMARYINFO_NAME"></span><span id="summaryinfo_name"></span>**SUMMARYINFO\_NAME**</span></span>  
<span data-ttu-id="60bc3-232">Текст, отображаемый в vsglog окно свойств-Name</span><span class="sxs-lookup"><span data-stu-id="60bc3-232">Text shown in the vsglog Properties window - Name</span></span>

<span data-ttu-id="60bc3-233"><span id="SUMMARYINFO_DESCRIPTION"></span><span id="summaryinfo_description"></span>**\_Описание суммаринфо**</span><span class="sxs-lookup"><span data-stu-id="60bc3-233"><span id="SUMMARYINFO_DESCRIPTION"></span><span id="summaryinfo_description"></span>**SUMMARYINFO\_DESCRIPTION**</span></span>  
<span data-ttu-id="60bc3-234">Текст, отображаемый в vsglog окно свойств-Description</span><span class="sxs-lookup"><span data-stu-id="60bc3-234">Text shown in the vsglog Properties window - Description</span></span>

<span data-ttu-id="60bc3-235"><span id="SUMMARYINFO_DISPLAYMEMORY"></span><span id="summaryinfo_displaymemory"></span>**СУММАРИНФО \_ дисплаймемори**</span><span class="sxs-lookup"><span data-stu-id="60bc3-235"><span id="SUMMARYINFO_DISPLAYMEMORY"></span><span id="summaryinfo_displaymemory"></span>**SUMMARYINFO\_DISPLAYMEMORY**</span></span>  
<span data-ttu-id="60bc3-236">Текст, отображаемый в vsglog окно свойств-отображать память</span><span class="sxs-lookup"><span data-stu-id="60bc3-236">Text shown in the vsglog Properties window - Display Memory</span></span>

<span data-ttu-id="60bc3-237"><span id="SUMMARYINFO_DRIVERNAME"></span><span id="summaryinfo_drivername"></span>**СУММАРИНФО \_ имя_драйвера**</span><span class="sxs-lookup"><span data-stu-id="60bc3-237"><span id="SUMMARYINFO_DRIVERNAME"></span><span id="summaryinfo_drivername"></span>**SUMMARYINFO\_DRIVERNAME**</span></span>  
<span data-ttu-id="60bc3-238">Текст, отображаемый в vsglog окно свойств-Driver Name</span><span class="sxs-lookup"><span data-stu-id="60bc3-238">Text shown in the vsglog Properties window - Driver Name</span></span>

<span data-ttu-id="60bc3-239"><span id="SUMMARYINFO_DRIVERVERSION"></span><span id="summaryinfo_driverversion"></span>**СУММАРИНФО \_ дриверверсион**</span><span class="sxs-lookup"><span data-stu-id="60bc3-239"><span id="SUMMARYINFO_DRIVERVERSION"></span><span id="summaryinfo_driverversion"></span>**SUMMARYINFO\_DRIVERVERSION**</span></span>  
<span data-ttu-id="60bc3-240">Текст, отображаемый в версии драйвера окно свойств vsglog</span><span class="sxs-lookup"><span data-stu-id="60bc3-240">Text shown in the vsglog Properties window - Driver Version</span></span>

<span data-ttu-id="60bc3-241"><span id="SUMMARYINFO_MODULEINFORMATION"></span><span id="summaryinfo_moduleinformation"></span>**СУММАРИНФО \_ модулеинформатион**</span><span class="sxs-lookup"><span data-stu-id="60bc3-241"><span id="SUMMARYINFO_MODULEINFORMATION"></span><span id="summaryinfo_moduleinformation"></span>**SUMMARYINFO\_MODULEINFORMATION**</span></span>  
<span data-ttu-id="60bc3-242">Текст, отображаемый в сведениях о модуле окно свойств vsglog-Module</span><span class="sxs-lookup"><span data-stu-id="60bc3-242">Text shown in the vsglog Properties window - Module Information</span></span>

<span data-ttu-id="60bc3-243"><span id="SUMMARYINFO_DIRECT3DINFORMATION"></span><span id="summaryinfo_direct3dinformation"></span>**СУММАРИНФО \_ DIRECT3DINFORMATION**</span><span class="sxs-lookup"><span data-stu-id="60bc3-243"><span id="SUMMARYINFO_DIRECT3DINFORMATION"></span><span id="summaryinfo_direct3dinformation"></span>**SUMMARYINFO\_DIRECT3DINFORMATION**</span></span>  
<span data-ttu-id="60bc3-244">Текст, отображаемый в vsglog окно свойств — сведения о Direct3D</span><span class="sxs-lookup"><span data-stu-id="60bc3-244">Text shown in the vsglog Properties window - Direct3D Information</span></span>

<span data-ttu-id="60bc3-245"><span id="SUMMARYINFO_VSGVERSION"></span><span id="summaryinfo_vsgversion"></span>**СУММАРИНФО \_ всгверсион**</span><span class="sxs-lookup"><span data-stu-id="60bc3-245"><span id="SUMMARYINFO_VSGVERSION"></span><span id="summaryinfo_vsgversion"></span>**SUMMARYINFO\_VSGVERSION**</span></span>  
<span data-ttu-id="60bc3-246">Текст, отображаемый в vsglog окно свойств — версия VSG</span><span class="sxs-lookup"><span data-stu-id="60bc3-246">Text shown in the vsglog Properties window - VSG Version</span></span>

<span data-ttu-id="60bc3-247"><span id="SUMMARYINFO_CAPTUREMACHINE"></span><span id="summaryinfo_capturemachine"></span>**СУММАРИНФО \_ каптуремачине**</span><span class="sxs-lookup"><span data-stu-id="60bc3-247"><span id="SUMMARYINFO_CAPTUREMACHINE"></span><span id="summaryinfo_capturemachine"></span>**SUMMARYINFO\_CAPTUREMACHINE**</span></span>  
<span data-ttu-id="60bc3-248">Текст, отображаемый на компьютере vsglog окно свойств-Capture</span><span class="sxs-lookup"><span data-stu-id="60bc3-248">Text shown in the vsglog Properties window - Capture Machine</span></span>

<span data-ttu-id="60bc3-249"><span id="SUMMARYINFO_PLAYBACKMACHINE"></span><span id="summaryinfo_playbackmachine"></span>**СУММАРИНФО \_ плайбаккмачине**</span><span class="sxs-lookup"><span data-stu-id="60bc3-249"><span id="SUMMARYINFO_PLAYBACKMACHINE"></span><span id="summaryinfo_playbackmachine"></span>**SUMMARYINFO\_PLAYBACKMACHINE**</span></span>  
<span data-ttu-id="60bc3-250">Текст, отображаемый на компьютере vsglog окно свойств-воспроизведения</span><span class="sxs-lookup"><span data-stu-id="60bc3-250">Text shown in the vsglog Properties window - Playback Machine</span></span>

<span data-ttu-id="60bc3-251"><span id="SUMMARYINFO_REMOTEDATA"></span><span id="summaryinfo_remotedata"></span>**СУММАРИНФО \_ REMOTEDATA**</span><span class="sxs-lookup"><span data-stu-id="60bc3-251"><span id="SUMMARYINFO_REMOTEDATA"></span><span id="summaryinfo_remotedata"></span>**SUMMARYINFO\_REMOTEDATA**</span></span>  
<span data-ttu-id="60bc3-252">Текст, отображаемый в vsglog окно свойств — удаленные данные</span><span class="sxs-lookup"><span data-stu-id="60bc3-252">Text shown in the vsglog Properties window - Remote Data</span></span>

<span data-ttu-id="60bc3-253"><span id="SUMMARYINFO_OtherDirect3DInformation"></span><span id="summaryinfo_otherdirect3dinformation"></span><span id="SUMMARYINFO_OTHERDIRECT3DINFORMATION"></span>**СУММАРИНФО \_ OtherDirect3DInformation**</span><span class="sxs-lookup"><span data-stu-id="60bc3-253"><span id="SUMMARYINFO_OtherDirect3DInformation"></span><span id="summaryinfo_otherdirect3dinformation"></span><span id="SUMMARYINFO_OTHERDIRECT3DINFORMATION"></span>**SUMMARYINFO\_OtherDirect3DInformation**</span></span>  
<span data-ttu-id="60bc3-254">Текст, отображаемый в vsglog окно свойств — другие сведения о Direct3D</span><span class="sxs-lookup"><span data-stu-id="60bc3-254">Text shown in the vsglog Properties window - Other Direct3D Information</span></span>

<span data-ttu-id="60bc3-255"><span id="SUMMARYINFO_SIZEGB"></span><span id="summaryinfo_sizegb"></span>**СУММАРИНФО \_ сизегб**</span><span class="sxs-lookup"><span data-stu-id="60bc3-255"><span id="SUMMARYINFO_SIZEGB"></span><span id="summaryinfo_sizegb"></span>**SUMMARYINFO\_SIZEGB**</span></span>  
<span data-ttu-id="60bc3-256">Текст, отображаемый в vsglog окно свойств-size ГБ</span><span class="sxs-lookup"><span data-stu-id="60bc3-256">Text shown in the vsglog Properties window - Size GB</span></span>

<span data-ttu-id="60bc3-257"><span id="SUMMARYINFO_SIZEMB"></span><span id="summaryinfo_sizemb"></span>**СУММАРИНФО \_ сиземб**</span><span class="sxs-lookup"><span data-stu-id="60bc3-257"><span id="SUMMARYINFO_SIZEMB"></span><span id="summaryinfo_sizemb"></span>**SUMMARYINFO\_SIZEMB**</span></span>  
<span data-ttu-id="60bc3-258">Текст, отображаемый в vsglog окно свойств — размер Мб</span><span class="sxs-lookup"><span data-stu-id="60bc3-258">Text shown in the vsglog Properties window - Size MB</span></span>

<span data-ttu-id="60bc3-259"><span id="SUMMARYINFO_SIZEBYTES"></span><span id="summaryinfo_sizebytes"></span>**СУММАРИНФО \_ сизебитес**</span><span class="sxs-lookup"><span data-stu-id="60bc3-259"><span id="SUMMARYINFO_SIZEBYTES"></span><span id="summaryinfo_sizebytes"></span>**SUMMARYINFO\_SIZEBYTES**</span></span>  
<span data-ttu-id="60bc3-260">Текст, отображаемый в vsglog окно свойств размером байт</span><span class="sxs-lookup"><span data-stu-id="60bc3-260">Text shown in the vsglog Properties window - Size Bytes</span></span>

<span data-ttu-id="60bc3-261"><span id="SUMMARYINFO_MEMORYMB"></span><span id="summaryinfo_memorymb"></span>**СУММАРИНФО \_ MEMORYMB**</span><span class="sxs-lookup"><span data-stu-id="60bc3-261"><span id="SUMMARYINFO_MEMORYMB"></span><span id="summaryinfo_memorymb"></span>**SUMMARYINFO\_MEMORYMB**</span></span>  
<span data-ttu-id="60bc3-262">Текст, отображаемый в vsglog окно свойств памяти, МБ</span><span class="sxs-lookup"><span data-stu-id="60bc3-262">Text shown in the vsglog Properties window - Memory MB</span></span>

<span data-ttu-id="60bc3-263"><span id="SUMMARYINFO_X86"></span><span id="summaryinfo_x86"></span>**СУММАРИНФО \_ x86**</span><span class="sxs-lookup"><span data-stu-id="60bc3-263"><span id="SUMMARYINFO_X86"></span><span id="summaryinfo_x86"></span>**SUMMARYINFO\_X86**</span></span>  
<span data-ttu-id="60bc3-264">Текст, отображаемый в vsglog окно свойств — x86</span><span class="sxs-lookup"><span data-stu-id="60bc3-264">Text shown in the vsglog Properties window - X86</span></span>

<span data-ttu-id="60bc3-265"><span id="SUMMARYINFO_X64"></span><span id="summaryinfo_x64"></span>**СУММАРИНФО \_ x64**</span><span class="sxs-lookup"><span data-stu-id="60bc3-265"><span id="SUMMARYINFO_X64"></span><span id="summaryinfo_x64"></span>**SUMMARYINFO\_X64**</span></span>  
<span data-ttu-id="60bc3-266">Текст, отображаемый в vsglog окно свойств x64</span><span class="sxs-lookup"><span data-stu-id="60bc3-266">Text shown in the vsglog Properties window - X64</span></span>

<span data-ttu-id="60bc3-267"><span id="SUMMARYINFO_TRUE"></span><span id="summaryinfo_true"></span>**СУММАРИНФО \_ true**</span><span class="sxs-lookup"><span data-stu-id="60bc3-267"><span id="SUMMARYINFO_TRUE"></span><span id="summaryinfo_true"></span>**SUMMARYINFO\_TRUE**</span></span>  
<span data-ttu-id="60bc3-268">Текст, отображаемый в vsglog окно свойств — true</span><span class="sxs-lookup"><span data-stu-id="60bc3-268">Text shown in the vsglog Properties window - True</span></span>

<span data-ttu-id="60bc3-269"><span id="SUMMARYINFO_FALSE"></span><span id="summaryinfo_false"></span>**СУММАРИНФО \_ false**</span><span class="sxs-lookup"><span data-stu-id="60bc3-269"><span id="SUMMARYINFO_FALSE"></span><span id="summaryinfo_false"></span>**SUMMARYINFO\_FALSE**</span></span>  
<span data-ttu-id="60bc3-270">Текст, отображаемый в vsglog окно свойств-false</span><span class="sxs-lookup"><span data-stu-id="60bc3-270">Text shown in the vsglog Properties window - False</span></span>

<span data-ttu-id="60bc3-271"><span id="SUMMARYINFO_ARM32"></span><span id="summaryinfo_arm32"></span>**СУММАРИНФО \_ ARM32**</span><span class="sxs-lookup"><span data-stu-id="60bc3-271"><span id="SUMMARYINFO_ARM32"></span><span id="summaryinfo_arm32"></span>**SUMMARYINFO\_ARM32**</span></span>  
<span data-ttu-id="60bc3-272">Текст, отображаемый в vsglog окно свойств-ARM 32</span><span class="sxs-lookup"><span data-stu-id="60bc3-272">Text shown in the vsglog Properties window - ARM 32</span></span>

<span data-ttu-id="60bc3-273"><span id="SUMMARYINFO_UNKNOWNCPUARCHITECTURE"></span><span id="summaryinfo_unknowncpuarchitecture"></span>**СУММАРИНФО \_ ункновнкпуарчитектуре**</span><span class="sxs-lookup"><span data-stu-id="60bc3-273"><span id="SUMMARYINFO_UNKNOWNCPUARCHITECTURE"></span><span id="summaryinfo_unknowncpuarchitecture"></span>**SUMMARYINFO\_UNKNOWNCPUARCHITECTURE**</span></span>  
<span data-ttu-id="60bc3-274">Текст, отображаемый в vsglog окно свойств — Неизвестная архитектура ЦП</span><span class="sxs-lookup"><span data-stu-id="60bc3-274">Text shown in the vsglog Properties window - Unknown CPU Architecture</span></span>

<span data-ttu-id="60bc3-275"><span id="SUMMARYINFO_AllDXGIFormatValues"></span><span id="summaryinfo_alldxgiformatvalues"></span><span id="SUMMARYINFO_ALLDXGIFORMATVALUES"></span>**СУММАРИНФО \_ аллдксгиформатвалуес**</span><span class="sxs-lookup"><span data-stu-id="60bc3-275"><span id="SUMMARYINFO_AllDXGIFormatValues"></span><span id="summaryinfo_alldxgiformatvalues"></span><span id="SUMMARYINFO_ALLDXGIFORMATVALUES"></span>**SUMMARYINFO\_AllDXGIFormatValues**</span></span>  
<span data-ttu-id="60bc3-276">Текст, отображаемый в vsglog окно свойств — все значения формата DXGI</span><span class="sxs-lookup"><span data-stu-id="60bc3-276">Text shown in the vsglog Properties window - All DXGI Format Values</span></span>

<span data-ttu-id="60bc3-277"><span id="SUMMARYINFO_AllD3D11FormatSupportValues"></span><span id="summaryinfo_alld3d11formatsupportvalues"></span><span id="SUMMARYINFO_ALLD3D11FORMATSUPPORTVALUES"></span>**СУММАРИНФО \_ AllD3D11FormatSupportValues**</span><span class="sxs-lookup"><span data-stu-id="60bc3-277"><span id="SUMMARYINFO_AllD3D11FormatSupportValues"></span><span id="summaryinfo_alld3d11formatsupportvalues"></span><span id="SUMMARYINFO_ALLD3D11FORMATSUPPORTVALUES"></span>**SUMMARYINFO\_AllD3D11FormatSupportValues**</span></span>  
<span data-ttu-id="60bc3-278">Текст, отображаемый в vsglog окно свойств — все значения поддержки формата D3D11</span><span class="sxs-lookup"><span data-stu-id="60bc3-278">Text shown in the vsglog Properties window - All D3D11 Format Support Values</span></span>

<span data-ttu-id="60bc3-279"><span id="SUMMARYINFO_D3D11_FEATURE_THREADING"></span><span id="summaryinfo_d3d11_feature_threading"></span>**\_ \_ Потоки функций суммаринфо \_ D3D11**</span><span class="sxs-lookup"><span data-stu-id="60bc3-279"><span id="SUMMARYINFO_D3D11_FEATURE_THREADING"></span><span id="summaryinfo_d3d11_feature_threading"></span>**SUMMARYINFO\_D3D11\_FEATURE\_THREADING**</span></span>  
<span data-ttu-id="60bc3-280">Текст, отображаемый в \_ многопоточной функции vsglog окно свойств-D3D11 \_</span><span class="sxs-lookup"><span data-stu-id="60bc3-280">Text shown in the vsglog Properties window - D3D11\_FEATURE\_THREADING</span></span>

<span data-ttu-id="60bc3-281"><span id="SUMMARYINFO_DriverConcurrentCreates1"></span><span id="summaryinfo_driverconcurrentcreates1"></span><span id="SUMMARYINFO_DRIVERCONCURRENTCREATES1"></span>**СУММАРИНФО \_ DriverConcurrentCreates1**</span><span class="sxs-lookup"><span data-stu-id="60bc3-281"><span id="SUMMARYINFO_DriverConcurrentCreates1"></span><span id="summaryinfo_driverconcurrentcreates1"></span><span id="SUMMARYINFO_DRIVERCONCURRENTCREATES1"></span>**SUMMARYINFO\_DriverConcurrentCreates1**</span></span>  
<span data-ttu-id="60bc3-282">Текст, отображаемый в параллельном vsglog окно свойств-драйвере, создает 1</span><span class="sxs-lookup"><span data-stu-id="60bc3-282">Text shown in the vsglog Properties window - Driver Concurrent Creates 1</span></span>

<span data-ttu-id="60bc3-283"><span id="SUMMARYINFO_DriverCommandLists1"></span><span id="summaryinfo_drivercommandlists1"></span><span id="SUMMARYINFO_DRIVERCOMMANDLISTS1"></span>**СУММАРИНФО \_ DriverCommandLists1**</span><span class="sxs-lookup"><span data-stu-id="60bc3-283"><span id="SUMMARYINFO_DriverCommandLists1"></span><span id="summaryinfo_drivercommandlists1"></span><span id="SUMMARYINFO_DRIVERCOMMANDLISTS1"></span>**SUMMARYINFO\_DriverCommandLists1**</span></span>  
<span data-ttu-id="60bc3-284">Текст, отображаемый в команде vsglog окно свойств-Driver, содержит список 1</span><span class="sxs-lookup"><span data-stu-id="60bc3-284">Text shown in the vsglog Properties window - Driver Command Lists 1</span></span>

<span data-ttu-id="60bc3-285"><span id="SUMMARYINFO_D3D11_FEATURE_DOUBLES"></span><span id="summaryinfo_d3d11_feature_doubles"></span>**СУММАРИНФО \_ D3D11 \_ функция \_ Double**</span><span class="sxs-lookup"><span data-stu-id="60bc3-285"><span id="SUMMARYINFO_D3D11_FEATURE_DOUBLES"></span><span id="summaryinfo_d3d11_feature_doubles"></span>**SUMMARYINFO\_D3D11\_FEATURE\_DOUBLES**</span></span>  
<span data-ttu-id="60bc3-286">Текст, отображаемый в функции vsglog окно свойств-D3D11, \_ \_ удваивается</span><span class="sxs-lookup"><span data-stu-id="60bc3-286">Text shown in the vsglog Properties window - D3D11\_FEATURE\_DOUBLES</span></span>

<span data-ttu-id="60bc3-287"><span id="SUMMARYINFO_DoublePrecisionFloatShaderOps"></span><span id="summaryinfo_doubleprecisionfloatshaderops"></span><span id="SUMMARYINFO_DOUBLEPRECISIONFLOATSHADEROPS"></span>**СУММАРИНФО \_ даублепреЦисионфлоатшадеропс**</span><span class="sxs-lookup"><span data-stu-id="60bc3-287"><span id="SUMMARYINFO_DoublePrecisionFloatShaderOps"></span><span id="summaryinfo_doubleprecisionfloatshaderops"></span><span id="SUMMARYINFO_DOUBLEPRECISIONFLOATSHADEROPS"></span>**SUMMARYINFO\_DoublePrecisionFloatShaderOps**</span></span>  
<span data-ttu-id="60bc3-288">Текст, отображаемый в операциях шейдера vsglog окно свойств с двойной точностью с плавающей запятой</span><span class="sxs-lookup"><span data-stu-id="60bc3-288">Text shown in the vsglog Properties window - Double Precision Float Shader Ops</span></span>

<span data-ttu-id="60bc3-289"><span id="SUMMARYINFO_D3D11_FEATURE_D3D10_X_HARDWARE_OPTIONS"></span><span id="summaryinfo_d3d11_feature_d3d10_x_hardware_options"></span>**СУММАРИНФО \_ D3D11 \_ Feature \_ D3D10 \_ X \_ \_ Параметры оборудования**</span><span class="sxs-lookup"><span data-stu-id="60bc3-289"><span id="SUMMARYINFO_D3D11_FEATURE_D3D10_X_HARDWARE_OPTIONS"></span><span id="summaryinfo_d3d11_feature_d3d10_x_hardware_options"></span>**SUMMARYINFO\_D3D11\_FEATURE\_D3D10\_X\_HARDWARE\_OPTIONS**</span></span>  
<span data-ttu-id="60bc3-290">Текст, отображаемый в vsglog окно свойств- \_ D3D11 \_ Feature \_ D3D10 \_ X \_ Параметры оборудования</span><span class="sxs-lookup"><span data-stu-id="60bc3-290">Text shown in the vsglog Properties window - D3D11\_FEATURE\_D3D10\_X\_HARDWARE\_OPTIONS</span></span>

<span data-ttu-id="60bc3-291"><span id="SUMMARYINFO_ComputeShaders_Plus_RawAndStructuredBuffers_Via_Shader_4_x"></span><span id="summaryinfo_computeshaders_plus_rawandstructuredbuffers_via_shader_4_x"></span><span id="SUMMARYINFO_COMPUTESHADERS_PLUS_RAWANDSTRUCTUREDBUFFERS_VIA_SHADER_4_X"></span>**СУММАРИНФО \_ компутешадерс \_ Plus \_ равандструктуредбуфферс \_ через \_ шейдер \_ 4 \_ x**</span><span class="sxs-lookup"><span data-stu-id="60bc3-291"><span id="SUMMARYINFO_ComputeShaders_Plus_RawAndStructuredBuffers_Via_Shader_4_x"></span><span id="summaryinfo_computeshaders_plus_rawandstructuredbuffers_via_shader_4_x"></span><span id="SUMMARYINFO_COMPUTESHADERS_PLUS_RAWANDSTRUCTUREDBUFFERS_VIA_SHADER_4_X"></span>**SUMMARYINFO\_ComputeShaders\_Plus\_RawAndStructuredBuffers\_Via\_Shader\_4\_x**</span></span>  
<span data-ttu-id="60bc3-292">Текст, отображаемый в vsglog окно свойств-Компутешадерс + RAW и Structure Дбуфферс через шейдер 4. x</span><span class="sxs-lookup"><span data-stu-id="60bc3-292">Text shown in the vsglog Properties window - ComputeShaders + Raw and Structure dBuffers via Shader 4.x</span></span>

<span data-ttu-id="60bc3-293"><span id="SUMMARYINFO_D3D11_FEATURE_D3D11_OPTIONS"></span><span id="summaryinfo_d3d11_feature_d3d11_options"></span>**\_ \_ Параметры D3D11 для функции суммаринфо D3D11 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="60bc3-293"><span id="SUMMARYINFO_D3D11_FEATURE_D3D11_OPTIONS"></span><span id="summaryinfo_d3d11_feature_d3d11_options"></span>**SUMMARYINFO\_D3D11\_FEATURE\_D3D11\_OPTIONS**</span></span>  
<span data-ttu-id="60bc3-294">Текст, отображаемый в \_ \_ параметрах D3D11 vsglog окно свойств-D3D11 Feature \_</span><span class="sxs-lookup"><span data-stu-id="60bc3-294">Text shown in the vsglog Properties window - D3D11\_FEATURE\_D3D11\_OPTIONS</span></span>

<span data-ttu-id="60bc3-295"><span id="SUMMARYINFO_OutputMergerLogicOp"></span><span id="summaryinfo_outputmergerlogicop"></span><span id="SUMMARYINFO_OUTPUTMERGERLOGICOP"></span>**СУММАРИНФО \_ аутпутмержерлогикоп**</span><span class="sxs-lookup"><span data-stu-id="60bc3-295"><span id="SUMMARYINFO_OutputMergerLogicOp"></span><span id="summaryinfo_outputmergerlogicop"></span><span id="SUMMARYINFO_OUTPUTMERGERLOGICOP"></span>**SUMMARYINFO\_OutputMergerLogicOp**</span></span>  
<span data-ttu-id="60bc3-296">Текст, отображаемый в операции логики слияния vsglog окно свойств-Output</span><span class="sxs-lookup"><span data-stu-id="60bc3-296">Text shown in the vsglog Properties window - Output Merger Logic Op</span></span>

<span data-ttu-id="60bc3-297"><span id="SUMMARYINFO_UAVOnlyRenderingForcedSampleCount"></span><span id="summaryinfo_uavonlyrenderingforcedsamplecount"></span><span id="SUMMARYINFO_UAVONLYRENDERINGFORCEDSAMPLECOUNT"></span>**СУММАРИНФО \_ уавонлирендерингфорцедсамплекаунт**</span><span class="sxs-lookup"><span data-stu-id="60bc3-297"><span id="SUMMARYINFO_UAVOnlyRenderingForcedSampleCount"></span><span id="summaryinfo_uavonlyrenderingforcedsamplecount"></span><span id="SUMMARYINFO_UAVONLYRENDERINGFORCEDSAMPLECOUNT"></span>**SUMMARYINFO\_UAVOnlyRenderingForcedSampleCount**</span></span>  
<span data-ttu-id="60bc3-298">Текст, отображаемый в vsglog окно свойств-UAV, выводит число принудительных выборок.</span><span class="sxs-lookup"><span data-stu-id="60bc3-298">Text shown in the vsglog Properties window - UAV Only Rendering Forced Sample Count</span></span>

<span data-ttu-id="60bc3-299"><span id="SUMMARYINFO_DiscardAPIsSeenByDriver"></span><span id="summaryinfo_discardapisseenbydriver"></span><span id="SUMMARYINFO_DISCARDAPISSEENBYDRIVER"></span>**СУММАРИНФО \_ дискардаписсинбидривер**</span><span class="sxs-lookup"><span data-stu-id="60bc3-299"><span id="SUMMARYINFO_DiscardAPIsSeenByDriver"></span><span id="summaryinfo_discardapisseenbydriver"></span><span id="SUMMARYINFO_DISCARDAPISSEENBYDRIVER"></span>**SUMMARYINFO\_DiscardAPIsSeenByDriver**</span></span>  
<span data-ttu-id="60bc3-300">Текст, отображаемый в API vsglog окно свойств-Discard, показанный драйвером</span><span class="sxs-lookup"><span data-stu-id="60bc3-300">Text shown in the vsglog Properties window - Discard APIs Seen By Driver</span></span>

<span data-ttu-id="60bc3-301"><span id="SUMMARYINFO_FlagsForUpdateAndCopySeenByDriver"></span><span id="summaryinfo_flagsforupdateandcopyseenbydriver"></span><span id="SUMMARYINFO_FLAGSFORUPDATEANDCOPYSEENBYDRIVER"></span>**СУММАРИНФО \_ флагсфорупдатеандкописинбидривер**</span><span class="sxs-lookup"><span data-stu-id="60bc3-301"><span id="SUMMARYINFO_FlagsForUpdateAndCopySeenByDriver"></span><span id="summaryinfo_flagsforupdateandcopyseenbydriver"></span><span id="SUMMARYINFO_FLAGSFORUPDATEANDCOPYSEENBYDRIVER"></span>**SUMMARYINFO\_FlagsForUpdateAndCopySeenByDriver**</span></span>  
<span data-ttu-id="60bc3-302">Текст, отображаемый в vsglog окно свойств-флаги для обновления и копирования, отображаемый драйвером</span><span class="sxs-lookup"><span data-stu-id="60bc3-302">Text shown in the vsglog Properties window - Flags For Update And Copy Seen By Driver</span></span>

<span data-ttu-id="60bc3-303"><span id="SUMMARYINFO_ClearView"></span><span id="summaryinfo_clearview"></span><span id="SUMMARYINFO_CLEARVIEW"></span>**СУММАРИНФО \_ клеарвиев**</span><span class="sxs-lookup"><span data-stu-id="60bc3-303"><span id="SUMMARYINFO_ClearView"></span><span id="summaryinfo_clearview"></span><span id="SUMMARYINFO_CLEARVIEW"></span>**SUMMARYINFO\_ClearView**</span></span>  
<span data-ttu-id="60bc3-304">Текст, отображаемый в vsglog окно свойств — очистить представление</span><span class="sxs-lookup"><span data-stu-id="60bc3-304">Text shown in the vsglog Properties window - Clear View</span></span>

<span data-ttu-id="60bc3-305"><span id="SUMMARYINFO_CopyWithOverlap"></span><span id="summaryinfo_copywithoverlap"></span><span id="SUMMARYINFO_COPYWITHOVERLAP"></span>**СУММАРИНФО \_ копивисоверлап**</span><span class="sxs-lookup"><span data-stu-id="60bc3-305"><span id="SUMMARYINFO_CopyWithOverlap"></span><span id="summaryinfo_copywithoverlap"></span><span id="SUMMARYINFO_COPYWITHOVERLAP"></span>**SUMMARYINFO\_CopyWithOverlap**</span></span>  
<span data-ttu-id="60bc3-306">Текст, отображаемый в vsglog окно свойств-Copy с перекрытием</span><span class="sxs-lookup"><span data-stu-id="60bc3-306">Text shown in the vsglog Properties window - Copy With Overlap</span></span>

<span data-ttu-id="60bc3-307"><span id="SUMMARYINFO_ConstantBufferPartialUpdate"></span><span id="summaryinfo_constantbufferpartialupdate"></span><span id="SUMMARYINFO_CONSTANTBUFFERPARTIALUPDATE"></span>**СУММАРИНФО \_ константбуфферпартиалупдате**</span><span class="sxs-lookup"><span data-stu-id="60bc3-307"><span id="SUMMARYINFO_ConstantBufferPartialUpdate"></span><span id="summaryinfo_constantbufferpartialupdate"></span><span id="SUMMARYINFO_CONSTANTBUFFERPARTIALUPDATE"></span>**SUMMARYINFO\_ConstantBufferPartialUpdate**</span></span>  
<span data-ttu-id="60bc3-308">Текст, отображаемый в частичном обновлении буфера vsglog окно свойств-Constant</span><span class="sxs-lookup"><span data-stu-id="60bc3-308">Text shown in the vsglog Properties window - Constant Buffer Partial Update</span></span>

<span data-ttu-id="60bc3-309"><span id="SUMMARYINFO_ConstantBufferOffsetting"></span><span id="summaryinfo_constantbufferoffsetting"></span><span id="SUMMARYINFO_CONSTANTBUFFEROFFSETTING"></span>**СУММАРИНФО \_ константбуффероффсеттинг**</span><span class="sxs-lookup"><span data-stu-id="60bc3-309"><span id="SUMMARYINFO_ConstantBufferOffsetting"></span><span id="summaryinfo_constantbufferoffsetting"></span><span id="SUMMARYINFO_CONSTANTBUFFEROFFSETTING"></span>**SUMMARYINFO\_ConstantBufferOffsetting**</span></span>  
<span data-ttu-id="60bc3-310">Текст, отображаемый в vsglog окно свойств-константном буфере смещения</span><span class="sxs-lookup"><span data-stu-id="60bc3-310">Text shown in the vsglog Properties window - Constant Buffer Offsetting</span></span>

<span data-ttu-id="60bc3-311"><span id="SUMMARYINFO_MapNoOverwriteOnDynamicConstantBuffer"></span><span id="summaryinfo_mapnooverwriteondynamicconstantbuffer"></span><span id="SUMMARYINFO_MAPNOOVERWRITEONDYNAMICCONSTANTBUFFER"></span>**СУММАРИНФО \_ мапнувервритеондинамикконстантбуффер**</span><span class="sxs-lookup"><span data-stu-id="60bc3-311"><span id="SUMMARYINFO_MapNoOverwriteOnDynamicConstantBuffer"></span><span id="summaryinfo_mapnooverwriteondynamicconstantbuffer"></span><span id="SUMMARYINFO_MAPNOOVERWRITEONDYNAMICCONSTANTBUFFER"></span>**SUMMARYINFO\_MapNoOverwriteOnDynamicConstantBuffer**</span></span>  
<span data-ttu-id="60bc3-312">Текст, отображаемый в vsglog окно свойств-Map без перезаписи в динамическом буфере константы</span><span class="sxs-lookup"><span data-stu-id="60bc3-312">Text shown in the vsglog Properties window - Map No Overwrite On Dynamic Constant Buffer</span></span>

<span data-ttu-id="60bc3-313"><span id="SUMMARYINFO_MapNoOverwriteOnDynamicBufferSRV"></span><span id="summaryinfo_mapnooverwriteondynamicbuffersrv"></span><span id="SUMMARYINFO_MAPNOOVERWRITEONDYNAMICBUFFERSRV"></span>**СУММАРИНФО \_ мапнувервритеондинамикбуфферсрв**</span><span class="sxs-lookup"><span data-stu-id="60bc3-313"><span id="SUMMARYINFO_MapNoOverwriteOnDynamicBufferSRV"></span><span id="summaryinfo_mapnooverwriteondynamicbuffersrv"></span><span id="SUMMARYINFO_MAPNOOVERWRITEONDYNAMICBUFFERSRV"></span>**SUMMARYINFO\_MapNoOverwriteOnDynamicBufferSRV**</span></span>  
<span data-ttu-id="60bc3-314">Текст, отображаемый в vsglog окно свойств-Map без перезаписи в динамическом буфере SRV</span><span class="sxs-lookup"><span data-stu-id="60bc3-314">Text shown in the vsglog Properties window - Map No Overwrite On Dynamic Buffer SRV</span></span>

<span data-ttu-id="60bc3-315"><span id="SUMMARYINFO_MultisampleRTVWithForcedSampleCountOne"></span><span id="summaryinfo_multisamplertvwithforcedsamplecountone"></span><span id="SUMMARYINFO_MULTISAMPLERTVWITHFORCEDSAMPLECOUNTONE"></span>**СУММАРИНФО \_ мултисамплертввисфорцедсамплекаунтоне**</span><span class="sxs-lookup"><span data-stu-id="60bc3-315"><span id="SUMMARYINFO_MultisampleRTVWithForcedSampleCountOne"></span><span id="summaryinfo_multisamplertvwithforcedsamplecountone"></span><span id="SUMMARYINFO_MULTISAMPLERTVWITHFORCEDSAMPLECOUNTONE"></span>**SUMMARYINFO\_MultisampleRTVWithForcedSampleCountOne**</span></span>  
<span data-ttu-id="60bc3-316">Текст, отображаемый в vsglog окно свойств — многопримерный РТВ с принудительным числом выборок, один</span><span class="sxs-lookup"><span data-stu-id="60bc3-316">Text shown in the vsglog Properties window - Multisample RTV With Forced Sample Count One</span></span>

<span data-ttu-id="60bc3-317"><span id="SUMMARYINFO_SAD4ShaderInstructions"></span><span id="summaryinfo_sad4shaderinstructions"></span><span id="SUMMARYINFO_SAD4SHADERINSTRUCTIONS"></span>**СУММАРИНФО \_ SAD4ShaderInstructions**</span><span class="sxs-lookup"><span data-stu-id="60bc3-317"><span id="SUMMARYINFO_SAD4ShaderInstructions"></span><span id="summaryinfo_sad4shaderinstructions"></span><span id="SUMMARYINFO_SAD4SHADERINSTRUCTIONS"></span>**SUMMARYINFO\_SAD4ShaderInstructions**</span></span>  
<span data-ttu-id="60bc3-318">Текст, отображаемый в инструкциях шейдера vsglog окно свойств-SAD4</span><span class="sxs-lookup"><span data-stu-id="60bc3-318">Text shown in the vsglog Properties window - SAD4 Shader Instructions</span></span>

<span data-ttu-id="60bc3-319"><span id="SUMMARYINFO_ExtendedDoublesShaderInstructions"></span><span id="summaryinfo_extendeddoublesshaderinstructions"></span><span id="SUMMARYINFO_EXTENDEDDOUBLESSHADERINSTRUCTIONS"></span>**СУММАРИНФО \_ екстендеддаублесшадеринструктионс**</span><span class="sxs-lookup"><span data-stu-id="60bc3-319"><span id="SUMMARYINFO_ExtendedDoublesShaderInstructions"></span><span id="summaryinfo_extendeddoublesshaderinstructions"></span><span id="SUMMARYINFO_EXTENDEDDOUBLESSHADERINSTRUCTIONS"></span>**SUMMARYINFO\_ExtendedDoublesShaderInstructions**</span></span>  
<span data-ttu-id="60bc3-320">Текст, отображаемый в инструкциях vsglog окно свойств — расширенные двойные шейдеры</span><span class="sxs-lookup"><span data-stu-id="60bc3-320">Text shown in the vsglog Properties window - Extended Doubles Shader Instructions</span></span>

<span data-ttu-id="60bc3-321"><span id="SUMMARYINFO_ExtendedResourceSharing"></span><span id="summaryinfo_extendedresourcesharing"></span><span id="SUMMARYINFO_EXTENDEDRESOURCESHARING"></span>**СУММАРИНФО \_ екстендедресаурцешаринг**</span><span class="sxs-lookup"><span data-stu-id="60bc3-321"><span id="SUMMARYINFO_ExtendedResourceSharing"></span><span id="summaryinfo_extendedresourcesharing"></span><span id="SUMMARYINFO_EXTENDEDRESOURCESHARING"></span>**SUMMARYINFO\_ExtendedResourceSharing**</span></span>  
<span data-ttu-id="60bc3-322">Текст, отображаемый в vsglog окно свойств — расширенный общий доступ к ресурсам</span><span class="sxs-lookup"><span data-stu-id="60bc3-322">Text shown in the vsglog Properties window - Extended Resource Sharing</span></span>

<span data-ttu-id="60bc3-323"><span id="SUMMARYINFO_D3D11_FEATURE_ARCHITECTURE_INFO"></span><span id="summaryinfo_d3d11_feature_architecture_info"></span>**\_ \_ \_ Сведения об архитектуре функций суммаринфо D3D11 \_**</span><span class="sxs-lookup"><span data-stu-id="60bc3-323"><span id="SUMMARYINFO_D3D11_FEATURE_ARCHITECTURE_INFO"></span><span id="summaryinfo_d3d11_feature_architecture_info"></span>**SUMMARYINFO\_D3D11\_FEATURE\_ARCHITECTURE\_INFO**</span></span>  
<span data-ttu-id="60bc3-324">Текст, отображаемый в \_ \_ сведениях об архитектуре функций vsglog окно свойств-D3D11 \_</span><span class="sxs-lookup"><span data-stu-id="60bc3-324">Text shown in the vsglog Properties window - D3D11\_FEATURE\_ARCHITECTURE\_INFO</span></span>

<span data-ttu-id="60bc3-325"><span id="SUMMARYINFO_TileBasedDeferredRenderer"></span><span id="summaryinfo_tilebaseddeferredrenderer"></span><span id="SUMMARYINFO_TILEBASEDDEFERREDRENDERER"></span>**СУММАРИНФО \_ тилебаседдеферредрендерер**</span><span class="sxs-lookup"><span data-stu-id="60bc3-325"><span id="SUMMARYINFO_TileBasedDeferredRenderer"></span><span id="summaryinfo_tilebaseddeferredrenderer"></span><span id="SUMMARYINFO_TILEBASEDDEFERREDRENDERER"></span>**SUMMARYINFO\_TileBasedDeferredRenderer**</span></span>  
<span data-ttu-id="60bc3-326">Текст, отображаемый в окно свойств vsglog отложенного модуля подготовки отчетов на основе плиток</span><span class="sxs-lookup"><span data-stu-id="60bc3-326">Text shown in the vsglog Properties window - Tile Based Deferred Renderer</span></span>

<span data-ttu-id="60bc3-327"><span id="SUMMARYINFO_D3D11_FEATURE_D3D9_OPTIONS"></span><span id="summaryinfo_d3d11_feature_d3d9_options"></span>**\_ \_ Параметры d3d9 для функции суммаринфо D3D11 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="60bc3-327"><span id="SUMMARYINFO_D3D11_FEATURE_D3D9_OPTIONS"></span><span id="summaryinfo_d3d11_feature_d3d9_options"></span>**SUMMARYINFO\_D3D11\_FEATURE\_D3D9\_OPTIONS**</span></span>  
<span data-ttu-id="60bc3-328">Текст, отображаемый в \_ \_ параметрах D3D9 vsglog окно свойств-D3D11 Feature \_</span><span class="sxs-lookup"><span data-stu-id="60bc3-328">Text shown in the vsglog Properties window - D3D11\_FEATURE\_D3D9\_OPTIONS</span></span>

<span data-ttu-id="60bc3-329"><span id="SUMMARYINFO_FullNonPow2TextureSupport"></span><span id="summaryinfo_fullnonpow2texturesupport"></span><span id="SUMMARYINFO_FULLNONPOW2TEXTURESUPPORT"></span>**СУММАРИНФО \_ FullNonPow2TextureSupport**</span><span class="sxs-lookup"><span data-stu-id="60bc3-329"><span id="SUMMARYINFO_FullNonPow2TextureSupport"></span><span id="summaryinfo_fullnonpow2texturesupport"></span><span id="SUMMARYINFO_FULLNONPOW2TEXTURESUPPORT"></span>**SUMMARYINFO\_FullNonPow2TextureSupport**</span></span>  
<span data-ttu-id="60bc3-330">Текст, отображаемый в vsglog окно свойств — полная поддержка текстур без Pow2</span><span class="sxs-lookup"><span data-stu-id="60bc3-330">Text shown in the vsglog Properties window - Full Non-Pow2 Texture Support</span></span>

<span data-ttu-id="60bc3-331"><span id="SUMMARYINFO_D3D11_FEATURE_SHADER_MIN_PRECISION_SUPPORT"></span><span id="summaryinfo_d3d11_feature_shader_min_precision_support"></span>**\_ \_ \_ \_ Поддержка min суммаринфо для шейдера функций D3D11 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="60bc3-331"><span id="SUMMARYINFO_D3D11_FEATURE_SHADER_MIN_PRECISION_SUPPORT"></span><span id="summaryinfo_d3d11_feature_shader_min_precision_support"></span>**SUMMARYINFO\_D3D11\_FEATURE\_SHADER\_MIN\_PRECISION\_SUPPORT**</span></span>  
<span data-ttu-id="60bc3-332">Текст, отображаемый в vsglog окно свойств-D3D11, \_ Поддержка функции \_ \_ min Shader \_ \_</span><span class="sxs-lookup"><span data-stu-id="60bc3-332">Text shown in the vsglog Properties window - D3D11\_FEATURE\_SHADER\_MIN\_PRECISION\_SUPPORT</span></span>

<span data-ttu-id="60bc3-333"><span id="SUMMARYINFO_PixelShaderMinPrecision"></span><span id="summaryinfo_pixelshaderminprecision"></span><span id="SUMMARYINFO_PIXELSHADERMINPRECISION"></span>**СУММАРИНФО \_ пикселшадерминпреЦисион**</span><span class="sxs-lookup"><span data-stu-id="60bc3-333"><span id="SUMMARYINFO_PixelShaderMinPrecision"></span><span id="summaryinfo_pixelshaderminprecision"></span><span id="SUMMARYINFO_PIXELSHADERMINPRECISION"></span>**SUMMARYINFO\_PixelShaderMinPrecision**</span></span>  
<span data-ttu-id="60bc3-334">Текст, отображаемый в окно свойств vsglog, минимальная точность шейдера пикселей</span><span class="sxs-lookup"><span data-stu-id="60bc3-334">Text shown in the vsglog Properties window - Pixel Shader Min Precision</span></span>

<span data-ttu-id="60bc3-335"><span id="SUMMARYINFO_AllOtherShaderStagesMinPrecision"></span><span id="summaryinfo_allothershaderstagesminprecision"></span><span id="SUMMARYINFO_ALLOTHERSHADERSTAGESMINPRECISION"></span>**СУММАРИНФО \_ аллосершадерстажесминпреЦисион**</span><span class="sxs-lookup"><span data-stu-id="60bc3-335"><span id="SUMMARYINFO_AllOtherShaderStagesMinPrecision"></span><span id="summaryinfo_allothershaderstagesminprecision"></span><span id="SUMMARYINFO_ALLOTHERSHADERSTAGESMINPRECISION"></span>**SUMMARYINFO\_AllOtherShaderStagesMinPrecision**</span></span>  
<span data-ttu-id="60bc3-336">Текст, отображаемый на vsglog окно свойств-все остальные этапы минимальной точности шейдеров</span><span class="sxs-lookup"><span data-stu-id="60bc3-336">Text shown in the vsglog Properties window - All Other Shader Stages Min Precision</span></span>

<span data-ttu-id="60bc3-337"><span id="SUMMARYINFO_D3D11_FEATURE_D3D9_SHADOW_SUPPORT"></span><span id="summaryinfo_d3d11_feature_d3d9_shadow_support"></span>**\_ \_ \_ \_ Поддержка теневого копирования d3d9 компонентов суммаринфо D3D11 \_**</span><span class="sxs-lookup"><span data-stu-id="60bc3-337"><span id="SUMMARYINFO_D3D11_FEATURE_D3D9_SHADOW_SUPPORT"></span><span id="summaryinfo_d3d11_feature_d3d9_shadow_support"></span>**SUMMARYINFO\_D3D11\_FEATURE\_D3D9\_SHADOW\_SUPPORT**</span></span>  
<span data-ttu-id="60bc3-338">Текст, отображаемый в vsglog окно свойств-D3D11 \_ Feature \_ d3d9, \_ Поддержка теневого копирования \_</span><span class="sxs-lookup"><span data-stu-id="60bc3-338">Text shown in the vsglog Properties window - D3D11\_FEATURE\_D3D9\_SHADOW\_SUPPORT</span></span>

<span data-ttu-id="60bc3-339"><span id="SUMMARYINFO_SupportsDepthAsTextureWithLessEqualComparisonFilter"></span><span id="summaryinfo_supportsdepthastexturewithlessequalcomparisonfilter"></span><span id="SUMMARYINFO_SUPPORTSDEPTHASTEXTUREWITHLESSEQUALCOMPARISONFILTER"></span>**СУММАРИНФО \_ суппортсдепсастекстуревислессекуалкомпарисонфилтер**</span><span class="sxs-lookup"><span data-stu-id="60bc3-339"><span id="SUMMARYINFO_SupportsDepthAsTextureWithLessEqualComparisonFilter"></span><span id="summaryinfo_supportsdepthastexturewithlessequalcomparisonfilter"></span><span id="SUMMARYINFO_SUPPORTSDEPTHASTEXTUREWITHLESSEQUALCOMPARISONFILTER"></span>**SUMMARYINFO\_SupportsDepthAsTextureWithLessEqualComparisonFilter**</span></span>  
<span data-ttu-id="60bc3-340">Текст, отображаемый в vsglog окно свойств, поддерживает глубину в виде текстуры с фильтром сравнения "меньше чем равно"</span><span class="sxs-lookup"><span data-stu-id="60bc3-340">Text shown in the vsglog Properties window - Supports Depth As Texture With Less Equal Comparison Filter</span></span>

<span data-ttu-id="60bc3-341"><span id="SUMMARYINFO_D3D11_FEATURE_D3D11_OPTIONS1"></span><span id="summaryinfo_d3d11_feature_d3d11_options1"></span>**СУММАРИНФО \_ D3D11 \_ Feature \_ D3D11 \_ OPTIONS1**</span><span class="sxs-lookup"><span data-stu-id="60bc3-341"><span id="SUMMARYINFO_D3D11_FEATURE_D3D11_OPTIONS1"></span><span id="summaryinfo_d3d11_feature_d3d11_options1"></span>**SUMMARYINFO\_D3D11\_FEATURE\_D3D11\_OPTIONS1**</span></span>  
<span data-ttu-id="60bc3-342">Текст, отображаемый в vsglog окно свойств-D3D11 \_ Feature \_ D3D11 \_ OPTIONS1</span><span class="sxs-lookup"><span data-stu-id="60bc3-342">Text shown in the vsglog Properties window - D3D11\_FEATURE\_D3D11\_OPTIONS1</span></span>

<span data-ttu-id="60bc3-343"><span id="SUMMARYINFO_TiledResourcesTier"></span><span id="summaryinfo_tiledresourcestier"></span><span id="SUMMARYINFO_TILEDRESOURCESTIER"></span>**СУММАРИНФО \_ тиледресаурцестиер**</span><span class="sxs-lookup"><span data-stu-id="60bc3-343"><span id="SUMMARYINFO_TiledResourcesTier"></span><span id="summaryinfo_tiledresourcestier"></span><span id="SUMMARYINFO_TILEDRESOURCESTIER"></span>**SUMMARYINFO\_TiledResourcesTier**</span></span>  
<span data-ttu-id="60bc3-344">Текст, отображаемый на уровне vsglog окно свойств-мозаичных ресурсов</span><span class="sxs-lookup"><span data-stu-id="60bc3-344">Text shown in the vsglog Properties window - Tiled Resources Tier</span></span>

<span data-ttu-id="60bc3-345"><span id="SUMMARYINFO_MinMaxFiltering"></span><span id="summaryinfo_minmaxfiltering"></span><span id="SUMMARYINFO_MINMAXFILTERING"></span>**СУММАРИНФО \_ минмаксфилтеринг**</span><span class="sxs-lookup"><span data-stu-id="60bc3-345"><span id="SUMMARYINFO_MinMaxFiltering"></span><span id="summaryinfo_minmaxfiltering"></span><span id="SUMMARYINFO_MINMAXFILTERING"></span>**SUMMARYINFO\_MinMaxFiltering**</span></span>  
<span data-ttu-id="60bc3-346">Текст, отображаемый в vsglog окно свойств-min max Filter</span><span class="sxs-lookup"><span data-stu-id="60bc3-346">Text shown in the vsglog Properties window - Min Max Filtering</span></span>

<span data-ttu-id="60bc3-347"><span id="SUMMARYINFO_ClearViewAlsoSupportsDepthOnlyFormats"></span><span id="summaryinfo_clearviewalsosupportsdepthonlyformats"></span><span id="SUMMARYINFO_CLEARVIEWALSOSUPPORTSDEPTHONLYFORMATS"></span>**СУММАРИНФО \_ клеарвиевалсосуппортсдепсонлиформатс**</span><span class="sxs-lookup"><span data-stu-id="60bc3-347"><span id="SUMMARYINFO_ClearViewAlsoSupportsDepthOnlyFormats"></span><span id="summaryinfo_clearviewalsosupportsdepthonlyformats"></span><span id="SUMMARYINFO_CLEARVIEWALSOSUPPORTSDEPTHONLYFORMATS"></span>**SUMMARYINFO\_ClearViewAlsoSupportsDepthOnlyFormats**</span></span>  
<span data-ttu-id="60bc3-348">Текст, отображаемый в vsglog окно свойств-Clear представление, также поддерживает форматы только глубины</span><span class="sxs-lookup"><span data-stu-id="60bc3-348">Text shown in the vsglog Properties window - Clear View Also Supports Depth Only Formats</span></span>

<span data-ttu-id="60bc3-349"><span id="SUMMARYINFO_MapOnDefaultBuffers"></span><span id="summaryinfo_mapondefaultbuffers"></span><span id="SUMMARYINFO_MAPONDEFAULTBUFFERS"></span>**СУММАРИНФО \_ мапондефаултбуфферс**</span><span class="sxs-lookup"><span data-stu-id="60bc3-349"><span id="SUMMARYINFO_MapOnDefaultBuffers"></span><span id="summaryinfo_mapondefaultbuffers"></span><span id="SUMMARYINFO_MAPONDEFAULTBUFFERS"></span>**SUMMARYINFO\_MapOnDefaultBuffers**</span></span>  
<span data-ttu-id="60bc3-350">Текст, отображаемый в vsglog окно свойств-Map в буферах по умолчанию</span><span class="sxs-lookup"><span data-stu-id="60bc3-350">Text shown in the vsglog Properties window - Map On Default Buffers</span></span>

<span data-ttu-id="60bc3-351"><span id="SUMMARYINFO_D3D11_FEATURE_D3D9_SIMPLE_INSTANCING_SUPPORT"></span><span id="summaryinfo_d3d11_feature_d3d9_simple_instancing_support"></span>**\_ \_ \_ \_ Поддержка простого создания \_ экземпляров \_ в суммаринфо D3D11 Feature d3d9**</span><span class="sxs-lookup"><span data-stu-id="60bc3-351"><span id="SUMMARYINFO_D3D11_FEATURE_D3D9_SIMPLE_INSTANCING_SUPPORT"></span><span id="summaryinfo_d3d11_feature_d3d9_simple_instancing_support"></span>**SUMMARYINFO\_D3D11\_FEATURE\_D3D9\_SIMPLE\_INSTANCING\_SUPPORT**</span></span>  
<span data-ttu-id="60bc3-352">Текст, отображаемый в функции vsglog окно свойств-D3D11 \_ \_ d3d9 Simple для создания \_ \_ экземпляров \_</span><span class="sxs-lookup"><span data-stu-id="60bc3-352">Text shown in the vsglog Properties window - D3D11\_FEATURE\_D3D9\_SIMPLE\_INSTANCING\_SUPPORT</span></span>

<span data-ttu-id="60bc3-353"><span id="SUMMARYINFO_SimpleInstancingSupported0"></span><span id="summaryinfo_simpleinstancingsupported0"></span><span id="SUMMARYINFO_SIMPLEINSTANCINGSUPPORTED0"></span>**СУММАРИНФО \_ SimpleInstancingSupported0**</span><span class="sxs-lookup"><span data-stu-id="60bc3-353"><span id="SUMMARYINFO_SimpleInstancingSupported0"></span><span id="summaryinfo_simpleinstancingsupported0"></span><span id="SUMMARYINFO_SIMPLEINSTANCINGSUPPORTED0"></span>**SUMMARYINFO\_SimpleInstancingSupported0**</span></span>  
<span data-ttu-id="60bc3-354">Текст, отображаемый в vsglog окно свойств — простой создание экземпляров, поддерживается 0</span><span class="sxs-lookup"><span data-stu-id="60bc3-354">Text shown in the vsglog Properties window - Simple Instancing Supported 0</span></span>

<span data-ttu-id="60bc3-355"><span id="SUMMARYINFO_D3D11_FEATURE_MARKER_SUPPORT"></span><span id="summaryinfo_d3d11_feature_marker_support"></span>**\_ \_ \_ Поддержка маркеров компонентов D3D11 \_ суммаринфо**</span><span class="sxs-lookup"><span data-stu-id="60bc3-355"><span id="SUMMARYINFO_D3D11_FEATURE_MARKER_SUPPORT"></span><span id="summaryinfo_d3d11_feature_marker_support"></span>**SUMMARYINFO\_D3D11\_FEATURE\_MARKER\_SUPPORT**</span></span>  
<span data-ttu-id="60bc3-356">Текст, отображаемый в окно свойств vsglog-D3D11, \_ \_ поддерживает маркеры компонентов. \_</span><span class="sxs-lookup"><span data-stu-id="60bc3-356">Text shown in the vsglog Properties window - D3D11\_FEATURE\_MARKER\_SUPPORT</span></span>

<span data-ttu-id="60bc3-357"><span id="SUMMARYINFO_Profile"></span><span id="summaryinfo_profile"></span><span id="SUMMARYINFO_PROFILE"></span>**\_Профиль суммаринфо**</span><span class="sxs-lookup"><span data-stu-id="60bc3-357"><span id="SUMMARYINFO_Profile"></span><span id="summaryinfo_profile"></span><span id="SUMMARYINFO_PROFILE"></span>**SUMMARYINFO\_Profile**</span></span>  
<span data-ttu-id="60bc3-358">Текст, отображаемый в vsglog окно свойств-Profile</span><span class="sxs-lookup"><span data-stu-id="60bc3-358">Text shown in the vsglog Properties window - Profile</span></span>

<span data-ttu-id="60bc3-359"><span id="SUMMARYINFO_D3D11_FEATURE_D3D9_OPTIONS1"></span><span id="summaryinfo_d3d11_feature_d3d9_options1"></span>**СУММАРИНФО \_ D3D11 \_ Feature \_ d3d9 \_ OPTIONS1**</span><span class="sxs-lookup"><span data-stu-id="60bc3-359"><span id="SUMMARYINFO_D3D11_FEATURE_D3D9_OPTIONS1"></span><span id="summaryinfo_d3d11_feature_d3d9_options1"></span>**SUMMARYINFO\_D3D11\_FEATURE\_D3D9\_OPTIONS1**</span></span>  
<span data-ttu-id="60bc3-360">Текст, отображаемый в vsglog окно свойств-D3D11 \_ Feature \_ d3d9 \_ OPTIONS1</span><span class="sxs-lookup"><span data-stu-id="60bc3-360">Text shown in the vsglog Properties window - D3D11\_FEATURE\_D3D9\_OPTIONS1</span></span>

<span data-ttu-id="60bc3-361"><span id="SUMMARYINFO_FullNonPow2TextureSupported"></span><span id="summaryinfo_fullnonpow2texturesupported"></span><span id="SUMMARYINFO_FULLNONPOW2TEXTURESUPPORTED"></span>**СУММАРИНФО \_ FullNonPow2TextureSupported**</span><span class="sxs-lookup"><span data-stu-id="60bc3-361"><span id="SUMMARYINFO_FullNonPow2TextureSupported"></span><span id="summaryinfo_fullnonpow2texturesupported"></span><span id="SUMMARYINFO_FULLNONPOW2TEXTURESUPPORTED"></span>**SUMMARYINFO\_FullNonPow2TextureSupported**</span></span>  
<span data-ttu-id="60bc3-362">Текст, отображаемый в vsglog окно свойств-Full (неPow2ная текстура)</span><span class="sxs-lookup"><span data-stu-id="60bc3-362">Text shown in the vsglog Properties window - Full Non-Pow2 Texture Supported</span></span>

<span data-ttu-id="60bc3-363"><span id="SUMMARYINFO_DepthAsTextureWithLessEqualComparisonFilterSupported"></span><span id="summaryinfo_depthastexturewithlessequalcomparisonfiltersupported"></span><span id="SUMMARYINFO_DEPTHASTEXTUREWITHLESSEQUALCOMPARISONFILTERSUPPORTED"></span>**СУММАРИНФО \_ депсастекстуревислессекуалкомпарисонфилтерсуппортед**</span><span class="sxs-lookup"><span data-stu-id="60bc3-363"><span id="SUMMARYINFO_DepthAsTextureWithLessEqualComparisonFilterSupported"></span><span id="summaryinfo_depthastexturewithlessequalcomparisonfiltersupported"></span><span id="SUMMARYINFO_DEPTHASTEXTUREWITHLESSEQUALCOMPARISONFILTERSUPPORTED"></span>**SUMMARYINFO\_DepthAsTextureWithLessEqualComparisonFilterSupported**</span></span>  
<span data-ttu-id="60bc3-364">Текст, отображаемый в vsglog окно свойств-Depth как текстура с поддержкой фильтра менее одинаковых сравнений</span><span class="sxs-lookup"><span data-stu-id="60bc3-364">Text shown in the vsglog Properties window - Depth As Texture With Less Equal Comparison Filter Supported</span></span>

<span data-ttu-id="60bc3-365"><span id="SUMMARYINFO_SimpleInstancingSupported1"></span><span id="summaryinfo_simpleinstancingsupported1"></span><span id="SUMMARYINFO_SIMPLEINSTANCINGSUPPORTED1"></span>**СУММАРИНФО \_ SimpleInstancingSupported1**</span><span class="sxs-lookup"><span data-stu-id="60bc3-365"><span id="SUMMARYINFO_SimpleInstancingSupported1"></span><span id="summaryinfo_simpleinstancingsupported1"></span><span id="SUMMARYINFO_SIMPLEINSTANCINGSUPPORTED1"></span>**SUMMARYINFO\_SimpleInstancingSupported1**</span></span>  
<span data-ttu-id="60bc3-366">Текст, отображаемый в vsglog окно свойств — поддержка простого создания экземпляров 1</span><span class="sxs-lookup"><span data-stu-id="60bc3-366">Text shown in the vsglog Properties window - Simple Instancing Supported 1</span></span>

<span data-ttu-id="60bc3-367"><span id="SUMMARYINFO_TextureCubeFaceRenderTargetWithNonCubeDepthStencilSupported"></span><span id="summaryinfo_texturecubefacerendertargetwithnoncubedepthstencilsupported"></span><span id="SUMMARYINFO_TEXTURECUBEFACERENDERTARGETWITHNONCUBEDEPTHSTENCILSUPPORTED"></span>**СУММАРИНФО \_ текстурекубефацерендертаржетвиснонкубедепсстенЦилсуппортед**</span><span class="sxs-lookup"><span data-stu-id="60bc3-367"><span id="SUMMARYINFO_TextureCubeFaceRenderTargetWithNonCubeDepthStencilSupported"></span><span id="summaryinfo_texturecubefacerendertargetwithnoncubedepthstencilsupported"></span><span id="SUMMARYINFO_TEXTURECUBEFACERENDERTARGETWITHNONCUBEDEPTHSTENCILSUPPORTED"></span>**SUMMARYINFO\_TextureCubeFaceRenderTargetWithNonCubeDepthStencilSupported**</span></span>  
<span data-ttu-id="60bc3-368">Текст, отображаемый на поверхности vsglog окно свойств-текстурный куб, не поддерживает набор элементов глубины Куба</span><span class="sxs-lookup"><span data-stu-id="60bc3-368">Text shown in the vsglog Properties window - Texture Cube Face Render Target With Non-Cube Depth Stencil Supported</span></span>

<span data-ttu-id="60bc3-369"><span id="SUMMARYINFO_DXGIFormat"></span><span id="summaryinfo_dxgiformat"></span><span id="SUMMARYINFO_DXGIFORMAT"></span>**СУММАРИНФО \_ дксгиформат**</span><span class="sxs-lookup"><span data-stu-id="60bc3-369"><span id="SUMMARYINFO_DXGIFormat"></span><span id="summaryinfo_dxgiformat"></span><span id="SUMMARYINFO_DXGIFORMAT"></span>**SUMMARYINFO\_DXGIFormat**</span></span>  
<span data-ttu-id="60bc3-370">Текст, отображаемый в vsglog окно свойств-Дксгиформат</span><span class="sxs-lookup"><span data-stu-id="60bc3-370">Text shown in the vsglog Properties window - DXGIFormat</span></span>

<span data-ttu-id="60bc3-371"><span id="SUMMARYINFO_DXGIFormat1"></span><span id="summaryinfo_dxgiformat1"></span><span id="SUMMARYINFO_DXGIFORMAT1"></span>**СУММАРИНФО \_ DXGIFormat1**</span><span class="sxs-lookup"><span data-stu-id="60bc3-371"><span id="SUMMARYINFO_DXGIFormat1"></span><span id="summaryinfo_dxgiformat1"></span><span id="SUMMARYINFO_DXGIFORMAT1"></span>**SUMMARYINFO\_DXGIFormat1**</span></span>  
<span data-ttu-id="60bc3-372">Текст, отображаемый в vsglog окно свойств-DXGIFormat1</span><span class="sxs-lookup"><span data-stu-id="60bc3-372">Text shown in the vsglog Properties window - DXGIFormat1</span></span>

<span data-ttu-id="60bc3-373"><span id="SUMMARYINFO_MODULENAME"></span><span id="summaryinfo_modulename"></span>**СУММАРИНФО \_ ModuleName**</span><span class="sxs-lookup"><span data-stu-id="60bc3-373"><span id="SUMMARYINFO_MODULENAME"></span><span id="summaryinfo_modulename"></span>**SUMMARYINFO\_MODULENAME**</span></span>  
<span data-ttu-id="60bc3-374">Текст, отображаемый в vsglog окно свойств-MODULENAME</span><span class="sxs-lookup"><span data-stu-id="60bc3-374">Text shown in the vsglog Properties window - MODULENAME</span></span>

<span data-ttu-id="60bc3-375"><span id="IDD_CONFIGURATION"></span><span id="idd_configuration"></span>**\_Конфигурация Идд**</span><span class="sxs-lookup"><span data-stu-id="60bc3-375"><span id="IDD_CONFIGURATION"></span><span id="idd_configuration"></span>**IDD\_CONFIGURATION**</span></span>  
<span data-ttu-id="60bc3-376">Текст, отображаемый в диалоговом окне настройки брандмауэра в Всграфиксремотингине</span><span class="sxs-lookup"><span data-stu-id="60bc3-376">Text shown in the Configure Firewall dialog in the VsGraphicsRemoteEngine</span></span>

<span data-ttu-id="60bc3-377"><span id="IDC_STATIC_HEADER_ICON"></span><span id="idc_static_header_icon"></span>**\_значок статического \_ заголовка \_ IDC**</span><span class="sxs-lookup"><span data-stu-id="60bc3-377"><span id="IDC_STATIC_HEADER_ICON"></span><span id="idc_static_header_icon"></span>**IDC\_STATIC\_HEADER\_ICON**</span></span>  
<span data-ttu-id="60bc3-378">Текст, отображаемый в элементе управления диалогового окна "Настройка брандмауэра-статический заголовок"</span><span class="sxs-lookup"><span data-stu-id="60bc3-378">Text shown in the Configure Firewall dialog control - Static Header Icon</span></span>

<span data-ttu-id="60bc3-379"><span id="IDC_STATIC_HEADER"></span><span id="idc_static_header"></span>**\_статический \_ заголовок IDC**</span><span class="sxs-lookup"><span data-stu-id="60bc3-379"><span id="IDC_STATIC_HEADER"></span><span id="idc_static_header"></span>**IDC\_STATIC\_HEADER**</span></span>  
<span data-ttu-id="60bc3-380">Текст, отображаемый в элементе управления диалогового окна "Настройка брандмауэра" — статический заголовок</span><span class="sxs-lookup"><span data-stu-id="60bc3-380">Text shown in the Configure Firewall dialog control - Static Header</span></span>

<span data-ttu-id="60bc3-381"><span id="IDC_STATIC_FW_CONFIGURATION"></span><span id="idc_static_fw_configuration"></span>**\_Конфигурация статического \_ встроенного по IDC \_**</span><span class="sxs-lookup"><span data-stu-id="60bc3-381"><span id="IDC_STATIC_FW_CONFIGURATION"></span><span id="idc_static_fw_configuration"></span>**IDC\_STATIC\_FW\_CONFIGURATION**</span></span>  
<span data-ttu-id="60bc3-382">Текст, отображаемый в элементе управления диалогового окна "Настройка брандмауэра" — Конфигурация статического брандмауэра</span><span class="sxs-lookup"><span data-stu-id="60bc3-382">Text shown in the Configure Firewall dialog control - Static Firewall Configuration</span></span>

<span data-ttu-id="60bc3-383"><span id="IDC_STATIC_FW_ICON"></span><span id="idc_static_fw_icon"></span>**\_значок статического \_ встроенного по IDC \_**</span><span class="sxs-lookup"><span data-stu-id="60bc3-383"><span id="IDC_STATIC_FW_ICON"></span><span id="idc_static_fw_icon"></span>**IDC\_STATIC\_FW\_ICON**</span></span>  
<span data-ttu-id="60bc3-384">Текст, отображаемый в элементе управления диалогового окна "Настройка брандмауэра" — значок "статический брандмауэр"</span><span class="sxs-lookup"><span data-stu-id="60bc3-384">Text shown in the Configure Firewall dialog control - Static Firewall Icon</span></span>

<span data-ttu-id="60bc3-385"><span id="IDC_STATIC_FW_HEADER"></span><span id="idc_static_fw_header"></span>**\_заголовок статического \_ встроенного по IDC \_**</span><span class="sxs-lookup"><span data-stu-id="60bc3-385"><span id="IDC_STATIC_FW_HEADER"></span><span id="idc_static_fw_header"></span>**IDC\_STATIC\_FW\_HEADER**</span></span>  
<span data-ttu-id="60bc3-386">Текст, отображаемый в элементе управления диалогового окна "Настройка брандмауэра" — статический заголовок брандмауэра</span><span class="sxs-lookup"><span data-stu-id="60bc3-386">Text shown in the Configure Firewall dialog control - Static Firewall Header</span></span>

<span data-ttu-id="60bc3-387"><span id="IDC_STATIC_GROUPBOX_FW"></span><span id="idc_static_groupbox_fw"></span>**\_встроенное по "static GROUPBOX" IDC \_ \_**</span><span class="sxs-lookup"><span data-stu-id="60bc3-387"><span id="IDC_STATIC_GROUPBOX_FW"></span><span id="idc_static_groupbox_fw"></span>**IDC\_STATIC\_GROUPBOX\_FW**</span></span>  
<span data-ttu-id="60bc3-388">Текст, отображаемый в элементе управления диалогового окна "Настройка брандмауэра" — "статическая группа" брандмауэр</span><span class="sxs-lookup"><span data-stu-id="60bc3-388">Text shown in the Configure Firewall dialog control - Static Groupbox Firewall</span></span>

<span data-ttu-id="60bc3-389"><span id="IDC_CHECK_FW_DOMAIN_NETWORKS"></span><span id="idc_check_fw_domain_networks"></span>**\_Проверка наличия \_ \_ доменных \_ сетей FW**</span><span class="sxs-lookup"><span data-stu-id="60bc3-389"><span id="IDC_CHECK_FW_DOMAIN_NETWORKS"></span><span id="idc_check_fw_domain_networks"></span>**IDC\_CHECK\_FW\_DOMAIN\_NETWORKS**</span></span>  
<span data-ttu-id="60bc3-390">Текст, отображаемый в элементе управления диалогового окна "Настройка брандмауэра" — Проверка доменных сетей брандмауэра</span><span class="sxs-lookup"><span data-stu-id="60bc3-390">Text shown in the Configure Firewall dialog control - Check Firewall Domain Networks</span></span>

<span data-ttu-id="60bc3-391"><span id="IDC_CHECK_FW_PRIVATE_NETWORKS"></span><span id="idc_check_fw_private_networks"></span>**\_Проверка наличия \_ \_ частных \_ сетей FW**</span><span class="sxs-lookup"><span data-stu-id="60bc3-391"><span id="IDC_CHECK_FW_PRIVATE_NETWORKS"></span><span id="idc_check_fw_private_networks"></span>**IDC\_CHECK\_FW\_PRIVATE\_NETWORKS**</span></span>  
<span data-ttu-id="60bc3-392">Текст, отображаемый в элементе управления диалогового окна настройки брандмауэра — проверка частных сетей брандмауэра</span><span class="sxs-lookup"><span data-stu-id="60bc3-392">Text shown in the Configure Firewall dialog control - Check Firewall Private Networks</span></span>

<span data-ttu-id="60bc3-393"><span id="IDC_CHECK_FW_PUBLIC_NETWORKS"></span><span id="idc_check_fw_public_networks"></span>**\_Проверка наличия \_ \_ общедоступных \_ сетей FW**</span><span class="sxs-lookup"><span data-stu-id="60bc3-393"><span id="IDC_CHECK_FW_PUBLIC_NETWORKS"></span><span id="idc_check_fw_public_networks"></span>**IDC\_CHECK\_FW\_PUBLIC\_NETWORKS**</span></span>  
<span data-ttu-id="60bc3-394">Текст, отображаемый в элементе управления диалогового окна "Настройка брандмауэра". Проверка общедоступных сетей брандмауэра</span><span class="sxs-lookup"><span data-stu-id="60bc3-394">Text shown in the Configure Firewall dialog control - Check Firewall Public Networks</span></span>

<span data-ttu-id="60bc3-395"><span id="IDC_BUTTON_CONFIGURE"></span><span id="idc_button_configure"></span>**\_Настройка кнопки \_ IDC**</span><span class="sxs-lookup"><span data-stu-id="60bc3-395"><span id="IDC_BUTTON_CONFIGURE"></span><span id="idc_button_configure"></span>**IDC\_BUTTON\_CONFIGURE**</span></span>  
<span data-ttu-id="60bc3-396">Текст, отображаемый в диалоговом окне настройки брандмауэра — кнопка Настройка</span><span class="sxs-lookup"><span data-stu-id="60bc3-396">Text shown in the Configure Firewall dialog control - Button Configure</span></span>

<span data-ttu-id="60bc3-397"><span id="ID_CONFIGURATION_CANCEL"></span><span id="id_configuration_cancel"></span>**\_Отмена настройки \_ идентификатора**</span><span class="sxs-lookup"><span data-stu-id="60bc3-397"><span id="ID_CONFIGURATION_CANCEL"></span><span id="id_configuration_cancel"></span>**ID\_CONFIGURATION\_CANCEL**</span></span>  
<span data-ttu-id="60bc3-398">Текст, отображаемый в элементе управления диалогового окна "Настройка брандмауэра" — Конфигурация Отмена</span><span class="sxs-lookup"><span data-stu-id="60bc3-398">Text shown in the Configure Firewall dialog control - Configuration Cancel</span></span>

<span data-ttu-id="60bc3-399"><span id="IDS_TEXT_FW_NOT_CONFIGURED"></span><span id="ids_text_fw_not_configured"></span>**\_ \_ \_ не \_ настроено FW для текста идентификаторов**</span><span class="sxs-lookup"><span data-stu-id="60bc3-399"><span id="IDS_TEXT_FW_NOT_CONFIGURED"></span><span id="ids_text_fw_not_configured"></span>**IDS\_TEXT\_FW\_NOT\_CONFIGURED**</span></span>  
<span data-ttu-id="60bc3-400">Текст, отображаемый в диалоговом окне "Настройка брандмауэра-текст", брандмауэр не настроен</span><span class="sxs-lookup"><span data-stu-id="60bc3-400">Text shown in the Configure Firewall dialog - Text Firewall Not Configured</span></span>

<span data-ttu-id="60bc3-401"><span id="IDS_TEXT_FW_CONFIGURED"></span><span id="ids_text_fw_configured"></span>**\_настроенное притекание текста идентификаторов \_ \_**</span><span class="sxs-lookup"><span data-stu-id="60bc3-401"><span id="IDS_TEXT_FW_CONFIGURED"></span><span id="ids_text_fw_configured"></span>**IDS\_TEXT\_FW\_CONFIGURED**</span></span>  
<span data-ttu-id="60bc3-402">Текст, отображаемый в диалоговом окне настройки брандмауэра — текст настройки брандмауэра</span><span class="sxs-lookup"><span data-stu-id="60bc3-402">Text shown in the Configure Firewall dialog - Text Firewall Configured</span></span>

<span data-ttu-id="60bc3-403"><span id="IDS_FIREWALL_RULE_NAME"></span><span id="ids_firewall_rule_name"></span>**\_ \_ имя правила брандмауэра идентификаторов \_**</span><span class="sxs-lookup"><span data-stu-id="60bc3-403"><span id="IDS_FIREWALL_RULE_NAME"></span><span id="ids_firewall_rule_name"></span>**IDS\_FIREWALL\_RULE\_NAME**</span></span>  
<span data-ttu-id="60bc3-404">Текст, отображаемый в диалоговом окне настройки брандмауэра — имя правила брандмауэра</span><span class="sxs-lookup"><span data-stu-id="60bc3-404">Text shown in the Configure Firewall dialog - Firewall Rule Name</span></span>

<span data-ttu-id="60bc3-405"><span id="IDS_FIREWALL_RULE_DESCRIPTION"></span><span id="ids_firewall_rule_description"></span>**\_ \_ Описание правила брандмауэра идентификаторов \_**</span><span class="sxs-lookup"><span data-stu-id="60bc3-405"><span id="IDS_FIREWALL_RULE_DESCRIPTION"></span><span id="ids_firewall_rule_description"></span>**IDS\_FIREWALL\_RULE\_DESCRIPTION**</span></span>  
<span data-ttu-id="60bc3-406">Текст, отображаемый в диалоговом окне настройки брандмауэра — описание правила брандмауэра</span><span class="sxs-lookup"><span data-stu-id="60bc3-406">Text shown in the Configure Firewall dialog - Firewall Rule Description</span></span>

<span data-ttu-id="60bc3-407"><span id="IDS_STATIC_HEADER"></span><span id="ids_static_header"></span>**\_статический \_ заголовок ID**</span><span class="sxs-lookup"><span data-stu-id="60bc3-407"><span id="IDS_STATIC_HEADER"></span><span id="ids_static_header"></span>**IDS\_STATIC\_HEADER**</span></span>  
<span data-ttu-id="60bc3-408">Текст, отображаемый в статическом заголовке диалогового окна настройки брандмауэра</span><span class="sxs-lookup"><span data-stu-id="60bc3-408">Text shown in the Configure Firewall dialog - Static Header</span></span>

<span data-ttu-id="60bc3-409"><span id="IDS_CONFIGURATION_TITLE"></span><span id="ids_configuration_title"></span>**\_название конфигурации идентификаторов \_**</span><span class="sxs-lookup"><span data-stu-id="60bc3-409"><span id="IDS_CONFIGURATION_TITLE"></span><span id="ids_configuration_title"></span>**IDS\_CONFIGURATION\_TITLE**</span></span>  
<span data-ttu-id="60bc3-410">Текст, отображаемый в диалоговом окне настройки брандмауэра — название конфигурации</span><span class="sxs-lookup"><span data-stu-id="60bc3-410">Text shown in the Configure Firewall dialog - Configuration Title</span></span>

<span data-ttu-id="60bc3-411"><span id="IDS_STATIC_FW_HEADER"></span><span id="ids_static_fw_header"></span>**\_заголовок статического \_ FW \_ ID**</span><span class="sxs-lookup"><span data-stu-id="60bc3-411"><span id="IDS_STATIC_FW_HEADER"></span><span id="ids_static_fw_header"></span>**IDS\_STATIC\_FW\_HEADER**</span></span>  
<span data-ttu-id="60bc3-412">Текст, отображаемый в диалоговом окне настройки брандмауэра — статический заголовок брандмауэра</span><span class="sxs-lookup"><span data-stu-id="60bc3-412">Text shown in the Configure Firewall dialog - Static Firewall Header</span></span>

<span data-ttu-id="60bc3-413"><span id="IDS_STATIC_GROUPBOX_FW"></span><span id="ids_static_groupbox_fw"></span>**\_встроенное по ID статической \_ GROUPBOX \_**</span><span class="sxs-lookup"><span data-stu-id="60bc3-413"><span id="IDS_STATIC_GROUPBOX_FW"></span><span id="ids_static_groupbox_fw"></span>**IDS\_STATIC\_GROUPBOX\_FW**</span></span>  
<span data-ttu-id="60bc3-414">Текст, отображаемый в диалоговом окне настройки брандмауэра — статический брандмауэр-группа</span><span class="sxs-lookup"><span data-stu-id="60bc3-414">Text shown in the Configure Firewall dialog - Static Groupbox Firewall</span></span>

<span data-ttu-id="60bc3-415"><span id="IDS_CHECK_FW_DOMAIN_NETWORKS"></span><span id="ids_check_fw_domain_networks"></span>**ИДЕНТИФИКАТОРы \_ Проверка \_ \_ доменных \_ сетей FW**</span><span class="sxs-lookup"><span data-stu-id="60bc3-415"><span id="IDS_CHECK_FW_DOMAIN_NETWORKS"></span><span id="ids_check_fw_domain_networks"></span>**IDS\_CHECK\_FW\_DOMAIN\_NETWORKS**</span></span>  
<span data-ttu-id="60bc3-416">Текст, отображаемый в диалоговом окне настройки брандмауэра. Проверьте доменные сети брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="60bc3-416">Text shown in the Configure Firewall dialog - Check Firewall Domain Networks</span></span>

<span data-ttu-id="60bc3-417"><span id="IDS_CHECK_FW_PRIVATE_NETWORKS"></span><span id="ids_check_fw_private_networks"></span>**Проверка ИДЕНТИФИКАТОРов \_ \_ \_ частные \_ сети FW**</span><span class="sxs-lookup"><span data-stu-id="60bc3-417"><span id="IDS_CHECK_FW_PRIVATE_NETWORKS"></span><span id="ids_check_fw_private_networks"></span>**IDS\_CHECK\_FW\_PRIVATE\_NETWORKS**</span></span>  
<span data-ttu-id="60bc3-418">Текст, отображаемый в диалоговом окне настройки брандмауэра. Проверьте частные сети брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="60bc3-418">Text shown in the Configure Firewall dialog - Check Firewall Private Networks</span></span>

<span data-ttu-id="60bc3-419"><span id="IDS_CHECK_FW_PUBLIC_NETWORKS"></span><span id="ids_check_fw_public_networks"></span>**ИД \_ Проверка \_ \_ общедоступных \_ сетей FW**</span><span class="sxs-lookup"><span data-stu-id="60bc3-419"><span id="IDS_CHECK_FW_PUBLIC_NETWORKS"></span><span id="ids_check_fw_public_networks"></span>**IDS\_CHECK\_FW\_PUBLIC\_NETWORKS**</span></span>  
<span data-ttu-id="60bc3-420">Текст, отображаемый в диалоговом окне настройки брандмауэра. Проверьте общедоступные сети брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="60bc3-420">Text shown in the Configure Firewall dialog - Check Firewall public Networks</span></span>

<span data-ttu-id="60bc3-421"><span id="IDS_BUTTON_CONFIGURE"></span><span id="ids_button_configure"></span>**\_Настройка кнопки идентификаторов \_**</span><span class="sxs-lookup"><span data-stu-id="60bc3-421"><span id="IDS_BUTTON_CONFIGURE"></span><span id="ids_button_configure"></span>**IDS\_BUTTON\_CONFIGURE**</span></span>  
<span data-ttu-id="60bc3-422">Текст, отображаемый в диалоговом окне настройки брандмауэра — Буттом Конфитуре</span><span class="sxs-lookup"><span data-stu-id="60bc3-422">Text shown in the Configure Firewall dialog - Buttom Confiture</span></span>

<span data-ttu-id="60bc3-423"><span id="IDS_CONFIGURATION_CANCEL"></span><span id="ids_configuration_cancel"></span>**\_Отмена настройки идентификаторов \_**</span><span class="sxs-lookup"><span data-stu-id="60bc3-423"><span id="IDS_CONFIGURATION_CANCEL"></span><span id="ids_configuration_cancel"></span>**IDS\_CONFIGURATION\_CANCEL**</span></span>  
<span data-ttu-id="60bc3-424">Текст, отображаемый в диалоговом окне настройки брандмауэра — конфигурация Отмена</span><span class="sxs-lookup"><span data-stu-id="60bc3-424">Text shown in the Configure Firewall dialog - Configuration Cancel</span></span>

<span data-ttu-id="60bc3-425"><span id="IDS_CAPTURETOOLTIP_MESSAGE_CORESYSTEM"></span><span id="ids_capturetooltip_message_coresystem"></span>**ИДЕНТИФИКАТОРы \_ \_ сообщения каптуретултип \_ коресистем**</span><span class="sxs-lookup"><span data-stu-id="60bc3-425"><span id="IDS_CAPTURETOOLTIP_MESSAGE_CORESYSTEM"></span><span id="ids_capturetooltip_message_coresystem"></span>**IDS\_CAPTURETOOLTIP\_MESSAGE\_CORESYSTEM**</span></span>  
<span data-ttu-id="60bc3-426">Идентификатор ресурса для строки "для захвата кадров используйте кнопку" запись "в Visual Studio."</span><span class="sxs-lookup"><span data-stu-id="60bc3-426">Resource ID for string "Use the capture button in Visual Studio to capture frame(s)."</span></span>

<span data-ttu-id="60bc3-427"><span id="IDS_ET_NONE"></span><span id="ids_et_none"></span>**ИДЕНТИФИКАТОРы \_ \_ нет**</span><span class="sxs-lookup"><span data-stu-id="60bc3-427"><span id="IDS_ET_NONE"></span><span id="ids_et_none"></span>**IDS\_ET\_NONE**</span></span>  
<span data-ttu-id="60bc3-428">Не используется.</span><span class="sxs-lookup"><span data-stu-id="60bc3-428">Not used.</span></span>

<span data-ttu-id="60bc3-429"><span id="IDS_ET_SESSIONSTART"></span><span id="ids_et_sessionstart"></span>**ИДЕНТИФИКАТОРы \_ et \_ SESSIONSTART**</span><span class="sxs-lookup"><span data-stu-id="60bc3-429"><span id="IDS_ET_SESSIONSTART"></span><span id="ids_et_sessionstart"></span>**IDS\_ET\_SESSIONSTART**</span></span>  
<span data-ttu-id="60bc3-430">Не используется.</span><span class="sxs-lookup"><span data-stu-id="60bc3-430">Not used.</span></span>

<span data-ttu-id="60bc3-431"><span id="IDS_ET_SESSIONEND"></span><span id="ids_et_sessionend"></span>**ИДЕНТИФИКАТОРы \_ et \_ сессионенд**</span><span class="sxs-lookup"><span data-stu-id="60bc3-431"><span id="IDS_ET_SESSIONEND"></span><span id="ids_et_sessionend"></span>**IDS\_ET\_SESSIONEND**</span></span>  
<span data-ttu-id="60bc3-432">Не используется.</span><span class="sxs-lookup"><span data-stu-id="60bc3-432">Not used.</span></span>

<span data-ttu-id="60bc3-433"><span id="IDS_ET_PROCESSSTART"></span><span id="ids_et_processstart"></span>**ИДЕНТИФИКАТОРы \_ et \_ процессстарт**</span><span class="sxs-lookup"><span data-stu-id="60bc3-433"><span id="IDS_ET_PROCESSSTART"></span><span id="ids_et_processstart"></span>**IDS\_ET\_PROCESSSTART**</span></span>  
<span data-ttu-id="60bc3-434">Не используется.</span><span class="sxs-lookup"><span data-stu-id="60bc3-434">Not used.</span></span>

<span data-ttu-id="60bc3-435"><span id="IDS_ET_PROCESSEND"></span><span id="ids_et_processend"></span>**ИДЕНТИФИКАТОРы \_ et \_ процессенд**</span><span class="sxs-lookup"><span data-stu-id="60bc3-435"><span id="IDS_ET_PROCESSEND"></span><span id="ids_et_processend"></span>**IDS\_ET\_PROCESSEND**</span></span>  
<span data-ttu-id="60bc3-436">Не используется.</span><span class="sxs-lookup"><span data-stu-id="60bc3-436">Not used.</span></span>

<span data-ttu-id="60bc3-437"><span id="IDS_ET_FRAMEBEGIN"></span><span id="ids_et_framebegin"></span>**ИДЕНТИФИКАТОРы \_ et \_ фрамебегин**</span><span class="sxs-lookup"><span data-stu-id="60bc3-437"><span id="IDS_ET_FRAMEBEGIN"></span><span id="ids_et_framebegin"></span>**IDS\_ET\_FRAMEBEGIN**</span></span>  
<span data-ttu-id="60bc3-438">Не используется.</span><span class="sxs-lookup"><span data-stu-id="60bc3-438">Not used.</span></span>

<span data-ttu-id="60bc3-439"><span id="IDS_ET_FRAMEEND"></span><span id="ids_et_frameend"></span>**ИДЕНТИФИКАТОРы \_ et \_ фраминд**</span><span class="sxs-lookup"><span data-stu-id="60bc3-439"><span id="IDS_ET_FRAMEEND"></span><span id="ids_et_frameend"></span>**IDS\_ET\_FRAMEEND**</span></span>  
<span data-ttu-id="60bc3-440">Не используется.</span><span class="sxs-lookup"><span data-stu-id="60bc3-440">Not used.</span></span>

<span data-ttu-id="60bc3-441"><span id="IDS_ET_USEREVENTBEGIN"></span><span id="ids_et_usereventbegin"></span>**ИДЕНТИФИКАТОРы \_ et \_ усеревентбегин**</span><span class="sxs-lookup"><span data-stu-id="60bc3-441"><span id="IDS_ET_USEREVENTBEGIN"></span><span id="ids_et_usereventbegin"></span>**IDS\_ET\_USEREVENTBEGIN**</span></span>  
<span data-ttu-id="60bc3-442">Не используется.</span><span class="sxs-lookup"><span data-stu-id="60bc3-442">Not used.</span></span>

<span data-ttu-id="60bc3-443"><span id="IDS_ET_USEREVENTEND"></span><span id="ids_et_usereventend"></span>**ИДЕНТИФИКАТОРы \_ et \_ усеревентенд**</span><span class="sxs-lookup"><span data-stu-id="60bc3-443"><span id="IDS_ET_USEREVENTEND"></span><span id="ids_et_usereventend"></span>**IDS\_ET\_USEREVENTEND**</span></span>  
<span data-ttu-id="60bc3-444">Не используется.</span><span class="sxs-lookup"><span data-stu-id="60bc3-444">Not used.</span></span>

<span data-ttu-id="60bc3-445"><span id="IDS_ET_USERMARKER"></span><span id="ids_et_usermarker"></span>**ИДЕНТИФИКАТОРы \_ et \_ усермаркер**</span><span class="sxs-lookup"><span data-stu-id="60bc3-445"><span id="IDS_ET_USERMARKER"></span><span id="ids_et_usermarker"></span>**IDS\_ET\_USERMARKER**</span></span>  
<span data-ttu-id="60bc3-446">Не используется.</span><span class="sxs-lookup"><span data-stu-id="60bc3-446">Not used.</span></span>

<span data-ttu-id="60bc3-447"><span id="IDS_ET_CALL"></span><span id="ids_et_call"></span>**ИДЕНТИФИКАТОРы, \_ \_ вызов et**</span><span class="sxs-lookup"><span data-stu-id="60bc3-447"><span id="IDS_ET_CALL"></span><span id="ids_et_call"></span>**IDS\_ET\_CALL**</span></span>  
<span data-ttu-id="60bc3-448">Не используется.</span><span class="sxs-lookup"><span data-stu-id="60bc3-448">Not used.</span></span>

<span data-ttu-id="60bc3-449"><span id="IDS_ET_OBJECTPOPULATION"></span><span id="ids_et_objectpopulation"></span>**ИДЕНТИФИКАТОРы \_ et \_ обжектпопулатион**</span><span class="sxs-lookup"><span data-stu-id="60bc3-449"><span id="IDS_ET_OBJECTPOPULATION"></span><span id="ids_et_objectpopulation"></span>**IDS\_ET\_OBJECTPOPULATION**</span></span>  
<span data-ttu-id="60bc3-450">Не используется.</span><span class="sxs-lookup"><span data-stu-id="60bc3-450">Not used.</span></span>

<span data-ttu-id="60bc3-451"><span id="IDS_ET_OBJECTCREATION"></span><span id="ids_et_objectcreation"></span>**ИДЕНТИФИКАТОРы \_ et \_ обжекткреатион**</span><span class="sxs-lookup"><span data-stu-id="60bc3-451"><span id="IDS_ET_OBJECTCREATION"></span><span id="ids_et_objectcreation"></span>**IDS\_ET\_OBJECTCREATION**</span></span>  
<span data-ttu-id="60bc3-452">Не используется.</span><span class="sxs-lookup"><span data-stu-id="60bc3-452">Not used.</span></span>

<span data-ttu-id="60bc3-453"><span id="IDS_ET_CALLSYNC"></span><span id="ids_et_callsync"></span>**ИДЕНТИФИКАТОРы \_ et \_ каллсинк**</span><span class="sxs-lookup"><span data-stu-id="60bc3-453"><span id="IDS_ET_CALLSYNC"></span><span id="ids_et_callsync"></span>**IDS\_ET\_CALLSYNC**</span></span>  
<span data-ttu-id="60bc3-454">Не используется.</span><span class="sxs-lookup"><span data-stu-id="60bc3-454">Not used.</span></span>

<span data-ttu-id="60bc3-455"><span id="IDS_ET_UNKNOWN"></span><span id="ids_et_unknown"></span>**ИДЕНТИФИКАТОРы \_ \_ неизвестны**</span><span class="sxs-lookup"><span data-stu-id="60bc3-455"><span id="IDS_ET_UNKNOWN"></span><span id="ids_et_unknown"></span>**IDS\_ET\_UNKNOWN**</span></span>  
<span data-ttu-id="60bc3-456">Не используется.</span><span class="sxs-lookup"><span data-stu-id="60bc3-456">Not used.</span></span>

<span data-ttu-id="60bc3-457"><span id="IDS_TRIGGER_NONE"></span><span id="ids_trigger_none"></span>**ИДЕНТИФИКАТОРы \_ активируют \_ нет**</span><span class="sxs-lookup"><span data-stu-id="60bc3-457"><span id="IDS_TRIGGER_NONE"></span><span id="ids_trigger_none"></span>**IDS\_TRIGGER\_NONE**</span></span>  
<span data-ttu-id="60bc3-458">Не используется.</span><span class="sxs-lookup"><span data-stu-id="60bc3-458">Not used.</span></span>

<span data-ttu-id="60bc3-459"><span id="IDS_TRIGGER_PROGRAMSTART"></span><span id="ids_trigger_programstart"></span>**ИДЕНТИФИКАТОРы \_ триггера \_ програмстарт**</span><span class="sxs-lookup"><span data-stu-id="60bc3-459"><span id="IDS_TRIGGER_PROGRAMSTART"></span><span id="ids_trigger_programstart"></span>**IDS\_TRIGGER\_PROGRAMSTART**</span></span>  
<span data-ttu-id="60bc3-460">Не используется.</span><span class="sxs-lookup"><span data-stu-id="60bc3-460">Not used.</span></span>

<span data-ttu-id="60bc3-461"><span id="IDS_TRIGGER_FRAME"></span><span id="ids_trigger_frame"></span>**\_кадр триггера идентификаторов \_**</span><span class="sxs-lookup"><span data-stu-id="60bc3-461"><span id="IDS_TRIGGER_FRAME"></span><span id="ids_trigger_frame"></span>**IDS\_TRIGGER\_FRAME**</span></span>  
<span data-ttu-id="60bc3-462">Не используется.</span><span class="sxs-lookup"><span data-stu-id="60bc3-462">Not used.</span></span>

<span data-ttu-id="60bc3-463"><span id="IDS_TRIGGER_TIME"></span><span id="ids_trigger_time"></span>**\_время активации идентификаторов \_**</span><span class="sxs-lookup"><span data-stu-id="60bc3-463"><span id="IDS_TRIGGER_TIME"></span><span id="ids_trigger_time"></span>**IDS\_TRIGGER\_TIME**</span></span>  
<span data-ttu-id="60bc3-464">Не используется.</span><span class="sxs-lookup"><span data-stu-id="60bc3-464">Not used.</span></span>

<span data-ttu-id="60bc3-465"><span id="IDS_TRIGGER_USERMARKER"></span><span id="ids_trigger_usermarker"></span>**ИДЕНТИФИКАТОРы \_ триггера \_ усермаркер**</span><span class="sxs-lookup"><span data-stu-id="60bc3-465"><span id="IDS_TRIGGER_USERMARKER"></span><span id="ids_trigger_usermarker"></span>**IDS\_TRIGGER\_USERMARKER**</span></span>  
<span data-ttu-id="60bc3-466">Не используется.</span><span class="sxs-lookup"><span data-stu-id="60bc3-466">Not used.</span></span>

<span data-ttu-id="60bc3-467"><span id="IDS_TRIGGER_BEGINUSEREVENT"></span><span id="ids_trigger_beginuserevent"></span>**ИДЕНТИФИКАТОРы \_ триггера \_ бегинусеревент**</span><span class="sxs-lookup"><span data-stu-id="60bc3-467"><span id="IDS_TRIGGER_BEGINUSEREVENT"></span><span id="ids_trigger_beginuserevent"></span>**IDS\_TRIGGER\_BEGINUSEREVENT**</span></span>  
<span data-ttu-id="60bc3-468">Не используется.</span><span class="sxs-lookup"><span data-stu-id="60bc3-468">Not used.</span></span>

<span data-ttu-id="60bc3-469"><span id="IDS_TRIGGER_ENDUSEREVENT"></span><span id="ids_trigger_enduserevent"></span>**ИДЕНТИФИКАТОРы \_ триггера \_ ендусеревент**</span><span class="sxs-lookup"><span data-stu-id="60bc3-469"><span id="IDS_TRIGGER_ENDUSEREVENT"></span><span id="ids_trigger_enduserevent"></span>**IDS\_TRIGGER\_ENDUSEREVENT**</span></span>  
<span data-ttu-id="60bc3-470">Не используется.</span><span class="sxs-lookup"><span data-stu-id="60bc3-470">Not used.</span></span>

<span data-ttu-id="60bc3-471"><span id="IDS_TRIGGER_CAPTUREFRAME"></span><span id="ids_trigger_captureframe"></span>**ИДЕНТИФИКАТОРы \_ триггера \_ каптурефраме**</span><span class="sxs-lookup"><span data-stu-id="60bc3-471"><span id="IDS_TRIGGER_CAPTUREFRAME"></span><span id="ids_trigger_captureframe"></span>**IDS\_TRIGGER\_CAPTUREFRAME**</span></span>  
<span data-ttu-id="60bc3-472">Не используется.</span><span class="sxs-lookup"><span data-stu-id="60bc3-472">Not used.</span></span>

<span data-ttu-id="60bc3-473"><span id="IDS_TRIGGER_APICAPTURE"></span><span id="ids_trigger_apicapture"></span>**ИДЕНТИФИКАТОРы \_ триггера \_ апикаптуре**</span><span class="sxs-lookup"><span data-stu-id="60bc3-473"><span id="IDS_TRIGGER_APICAPTURE"></span><span id="ids_trigger_apicapture"></span>**IDS\_TRIGGER\_APICAPTURE**</span></span>  
<span data-ttu-id="60bc3-474">Не используется.</span><span class="sxs-lookup"><span data-stu-id="60bc3-474">Not used.</span></span>

<span data-ttu-id="60bc3-475"><span id="IDS_ERROR_CALLDATA"></span><span id="ids_error_calldata"></span>**ИДЕНТИФИКАТОРы \_ ошибки \_ каллдата**</span><span class="sxs-lookup"><span data-stu-id="60bc3-475"><span id="IDS_ERROR_CALLDATA"></span><span id="ids_error_calldata"></span>**IDS\_ERROR\_CALLDATA**</span></span>  
<span data-ttu-id="60bc3-476">Не используется.</span><span class="sxs-lookup"><span data-stu-id="60bc3-476">Not used.</span></span>

<span data-ttu-id="60bc3-477"><span id="IDS_ERROR_CREATINGLOG"></span><span id="ids_error_creatinglog"></span>**ИДЕНТИФИКАТОРы \_ ошибки \_ креатинглог**</span><span class="sxs-lookup"><span data-stu-id="60bc3-477"><span id="IDS_ERROR_CREATINGLOG"></span><span id="ids_error_creatinglog"></span>**IDS\_ERROR\_CREATINGLOG**</span></span>  
<span data-ttu-id="60bc3-478">Не используется.</span><span class="sxs-lookup"><span data-stu-id="60bc3-478">Not used.</span></span>

<span data-ttu-id="60bc3-479"><span id="IDS_UNKNOWNCALL"></span><span id="ids_unknowncall"></span>**ИДЕНТИФИКАТОРы \_ ункновнкалл**</span><span class="sxs-lookup"><span data-stu-id="60bc3-479"><span id="IDS_UNKNOWNCALL"></span><span id="ids_unknowncall"></span>**IDS\_UNKNOWNCALL**</span></span>  
<span data-ttu-id="60bc3-480">Не используется.</span><span class="sxs-lookup"><span data-stu-id="60bc3-480">Not used.</span></span>

<span data-ttu-id="60bc3-481"><span id="IDS_WARN_FEATURE_LEVEL_CHANGED"></span><span id="ids_warn_feature_level_changed"></span>**Идентификатор \_ предупреждения \_ об \_ изменении уровня компонента \_**</span><span class="sxs-lookup"><span data-stu-id="60bc3-481"><span id="IDS_WARN_FEATURE_LEVEL_CHANGED"></span><span id="ids_warn_feature_level_changed"></span>**IDS\_WARN\_FEATURE\_LEVEL\_CHANGED**</span></span>  
<span data-ttu-id="60bc3-482">Не используется.</span><span class="sxs-lookup"><span data-stu-id="60bc3-482">Not used.</span></span>

<span data-ttu-id="60bc3-483"><span id="ID_STATUS_FREQUENCY"></span><span id="id_status_frequency"></span>**\_Частота состояния \_ идентификатора**</span><span class="sxs-lookup"><span data-stu-id="60bc3-483"><span id="ID_STATUS_FREQUENCY"></span><span id="id_status_frequency"></span>**ID\_STATUS\_FREQUENCY**</span></span>  

<span data-ttu-id="60bc3-484"><span id="ID_DISABLE_HUD"></span><span id="id_disable_hud"></span>**ID \_ disable \_ HUD**</span><span class="sxs-lookup"><span data-stu-id="60bc3-484"><span id="ID_DISABLE_HUD"></span><span id="id_disable_hud"></span>**ID\_DISABLE\_HUD**</span></span>  

<span data-ttu-id="60bc3-485"><span id="ID_DISABLE_COMPAT"></span><span id="id_disable_compat"></span>**Идентификатор \_ Отключить \_ Совместимость**</span><span class="sxs-lookup"><span data-stu-id="60bc3-485"><span id="ID_DISABLE_COMPAT"></span><span id="id_disable_compat"></span>**ID\_DISABLE\_COMPAT**</span></span>  

<span data-ttu-id="60bc3-486"><span id="ID_COLLECT_CALLSTACKS"></span><span id="id_collect_callstacks"></span>**Идентификатор, \_ собирающий \_ стеки вызовов**</span><span class="sxs-lookup"><span data-stu-id="60bc3-486"><span id="ID_COLLECT_CALLSTACKS"></span><span id="id_collect_callstacks"></span>**ID\_COLLECT\_CALLSTACKS**</span></span>  

<span data-ttu-id="60bc3-487"><span id="ID_ENABLE_SDKERROR_STOP"></span><span id="id_enable_sdkerror_stop"></span>**Идентификатор \_ включить \_ сдкеррор \_**</span><span class="sxs-lookup"><span data-stu-id="60bc3-487"><span id="ID_ENABLE_SDKERROR_STOP"></span><span id="id_enable_sdkerror_stop"></span>**ID\_ENABLE\_SDKERROR\_STOP**</span></span>  

## <a name="requirements"></a><span data-ttu-id="60bc3-488">Требования</span><span class="sxs-lookup"><span data-stu-id="60bc3-488">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="60bc3-489">Header</span><span class="sxs-lookup"><span data-stu-id="60bc3-489">Header</span></span></p></td><td><span data-ttu-id="60bc3-490">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="60bc3-490">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



