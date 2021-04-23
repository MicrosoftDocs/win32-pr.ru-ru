---
title: Что нового в проигрывателе Windows Media 12
description: В этом разделе перечислены новые возможности проигрывателя Windows Media 12.
ms.assetid: 17f76963-c96d-46c9-82c0-3ed2d8a4e892
keywords:
- Проигрыватель Windows Media, новые возможности
- Проигрыватель Windows Media, новые функции
- пакет средств разработки программного обеспечения (SDK), проигрыватель Windows Media 12
- Пакет SDK (пакет средств разработки программного обеспечения), проигрыватель Windows Media 12
- Документация, Windows Media Player 12 SDK
- новые возможности, проигрыватель Windows Media 12
- новые возможности, проигрыватель Windows Media 12
- интерфейсы, новые возможности проигрывателя Windows Media 12
- атрибуты, новые функции в проигрывателе Windows Media 12
- метаданные, новые функции в проигрывателе Windows Media 12
- перечисления, новые функции в проигрывателе Windows Media 12
- Флаги, новые функции в проигрывателе Windows Media 12
- интерфейсы, устаревшие в проигрывателе Windows Media 12
- методы, устаревшие в проигрывателе Windows Media 11 и не 12
- версии проигрывателя Windows Media, новые функции в версии 12
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d16b21077df1f4a9c11edbfa20032ed473f872a0
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2020
ms.locfileid: "104133606"
---
# <a name="whats-new-in-windows-media-player-12"></a><span data-ttu-id="c2c0a-118">Что нового в проигрывателе Windows Media 12</span><span class="sxs-lookup"><span data-stu-id="c2c0a-118">What's New in Windows Media Player 12</span></span>

<span data-ttu-id="c2c0a-119">В этом разделе перечислены новые возможности проигрывателя Windows Media 12.</span><span class="sxs-lookup"><span data-stu-id="c2c0a-119">This topic lists features that are new in Windows Media Player 12.</span></span>

## <a name="new-interfaces"></a><span data-ttu-id="c2c0a-120">Новые интерфейсы</span><span class="sxs-lookup"><span data-stu-id="c2c0a-120">New Interfaces</span></span>

-   [<span data-ttu-id="c2c0a-121">**ивмпаудиорендерконфиг**</span><span class="sxs-lookup"><span data-stu-id="c2c0a-121">**IWMPAudioRenderConfig**</span></span>](/previous-versions/windows/desktop/api/wmprealestate/nn-wmprealestate-iwmpaudiorenderconfig)
-   [<span data-ttu-id="c2c0a-122">**IWMPEvents4**</span><span class="sxs-lookup"><span data-stu-id="c2c0a-122">**IWMPEvents4**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents4)
-   [<span data-ttu-id="c2c0a-123">**IWMPLibrary2**</span><span class="sxs-lookup"><span data-stu-id="c2c0a-123">**IWMPLibrary2**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrary2)
-   [<span data-ttu-id="c2c0a-124">**IWMPSyncDevice3**</span><span class="sxs-lookup"><span data-stu-id="c2c0a-124">**IWMPSyncDevice3**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice3)

## <a name="new-attributes"></a><span data-ttu-id="c2c0a-125">Новые атрибуты</span><span class="sxs-lookup"><span data-stu-id="c2c0a-125">New Attributes</span></span>

<span data-ttu-id="c2c0a-126">Следующие новые атрибуты для элементов мультимедиа доступны через интерфейсы [**ивмпмедиа**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia) и [**IWMPMedia3**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia3) .</span><span class="sxs-lookup"><span data-stu-id="c2c0a-126">The following new attributes for media items are available through the [**IWMPMedia**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia) and [**IWMPMedia3**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia3) interfaces.</span></span>

-   [<span data-ttu-id="c2c0a-127">**албумковерурл**</span><span class="sxs-lookup"><span data-stu-id="c2c0a-127">**AlbumCoverURL**</span></span>](wm-albumcoverurl-attribute.md)
-   [<span data-ttu-id="c2c0a-128">**алтернатесаурцеурл**</span><span class="sxs-lookup"><span data-stu-id="c2c0a-128">**AlternateSourceURL**</span></span>](alternatesourceurl-attribute.md)
-   [<span data-ttu-id="c2c0a-129">**длнасаурцеури**</span><span class="sxs-lookup"><span data-stu-id="c2c0a-129">**DLNASourceURI**</span></span>](dlnasourceuri-attribute.md)
-   [<span data-ttu-id="c2c0a-130">**длнасерверудн**</span><span class="sxs-lookup"><span data-stu-id="c2c0a-130">**DLNAServerUDN**</span></span>](dlnaserverudn-attribute.md)
-   [<span data-ttu-id="c2c0a-131">**дткпифост**</span><span class="sxs-lookup"><span data-stu-id="c2c0a-131">**DTCPIPHost**</span></span>](dtcpiphost-attribute.md)
-   [<span data-ttu-id="c2c0a-132">**дткпиппорт**</span><span class="sxs-lookup"><span data-stu-id="c2c0a-132">**DTCPIPPort**</span></span>](dtcpipport-attribute.md)
-   [<span data-ttu-id="c2c0a-133">**либрарид**</span><span class="sxs-lookup"><span data-stu-id="c2c0a-133">**LibraryID**</span></span>](libraryid-attribute.md)
-   [<span data-ttu-id="c2c0a-134">**LibraryName**</span><span class="sxs-lookup"><span data-stu-id="c2c0a-134">**LibraryName**</span></span>](libraryname-attribute.md)

## <a name="new-device-metadata"></a><span data-ttu-id="c2c0a-135">Новые метаданные устройства</span><span class="sxs-lookup"><span data-stu-id="c2c0a-135">New Device Metadata</span></span>

<span data-ttu-id="c2c0a-136">Следующие новые элементы метаданных устройства можно получить путем вызова [**ивмпсинкдевице:: getItemInfo**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-getiteminfo).</span><span class="sxs-lookup"><span data-stu-id="c2c0a-136">The following new device metadata items can be retrieved by calling [**IWMPSyncDevice::getItemInfo**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-getiteminfo).</span></span>

-   <span data-ttu-id="c2c0a-137">**баккграундсинкстате**</span><span class="sxs-lookup"><span data-stu-id="c2c0a-137">**BackgroundSyncState**</span></span>
-   <span data-ttu-id="c2c0a-138">**скиппедфилес**</span><span class="sxs-lookup"><span data-stu-id="c2c0a-138">**SkippedFiles**</span></span>
-   <span data-ttu-id="c2c0a-139">**синкфилтер**</span><span class="sxs-lookup"><span data-stu-id="c2c0a-139">**SyncFilter**</span></span>

<span data-ttu-id="c2c0a-140">Следующие новые элементы метаданных устройства можно задать путем вызова [**IWMPSyncDevice2:: сетитеминфо**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice2-setiteminfo).</span><span class="sxs-lookup"><span data-stu-id="c2c0a-140">The following new device metadata items can be set by calling [**IWMPSyncDevice2::setItemInfo**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice2-setiteminfo).</span></span>

-   <span data-ttu-id="c2c0a-141">**аутосинкдефаултрулес**</span><span class="sxs-lookup"><span data-stu-id="c2c0a-141">**AutoSyncDefaultRules**</span></span>
-   <span data-ttu-id="c2c0a-142">**баккграундсинкстате**</span><span class="sxs-lookup"><span data-stu-id="c2c0a-142">**BackgroundSyncState**</span></span>
-   <span data-ttu-id="c2c0a-143">**инклудескиппедфилес**</span><span class="sxs-lookup"><span data-stu-id="c2c0a-143">**IncludeSkippedFiles**</span></span>
-   <span data-ttu-id="c2c0a-144">**синкфилтер**</span><span class="sxs-lookup"><span data-stu-id="c2c0a-144">**SyncFilter**</span></span>
-   <span data-ttu-id="c2c0a-145">**синконконнект**</span><span class="sxs-lookup"><span data-stu-id="c2c0a-145">**SyncOnConnect**</span></span>

## <a name="new-enumeration-member"></a><span data-ttu-id="c2c0a-146">Новый член перечисления</span><span class="sxs-lookup"><span data-stu-id="c2c0a-146">New Enumeration Member</span></span>

<span data-ttu-id="c2c0a-147">Перечисление [**вмпсинкстате**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpsyncstate) имеет следующий новый элемент.</span><span class="sxs-lookup"><span data-stu-id="c2c0a-147">The [**WMPSyncState**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpsyncstate) enumeration has the following new member.</span></span>

-   <span data-ttu-id="c2c0a-148">**вмпссестиматинг**</span><span class="sxs-lookup"><span data-stu-id="c2c0a-148">**wmpssEstimating**</span></span>

## <a name="new-flag"></a><span data-ttu-id="c2c0a-149">Новый флаг</span><span class="sxs-lookup"><span data-stu-id="c2c0a-149">New Flag</span></span>

<span data-ttu-id="c2c0a-150">Метод [**ивмпграфкреатион:: жетграфкреатионфлагс**](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpgraphcreation-getgraphcreationflags) поддерживает следующий новый флаг.</span><span class="sxs-lookup"><span data-stu-id="c2c0a-150">The [**IWMPGraphCreation::GetGraphCreationFlags**](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpgraphcreation-getgraphcreationflags) method supports the following new flag.</span></span>

-   <span data-ttu-id="c2c0a-151">**\_Флаги вмпгк \_ использовать \_ настраиваемый \_ граф**</span><span class="sxs-lookup"><span data-stu-id="c2c0a-151">**WMPGC\_FLAGS\_USE\_CUSTOM\_GRAPH**</span></span>

## <a name="deprecated-interface"></a><span data-ttu-id="c2c0a-152">Устаревший интерфейс</span><span class="sxs-lookup"><span data-stu-id="c2c0a-152">Deprecated Interface</span></span>

<span data-ttu-id="c2c0a-153">Следующий интерфейс является устаревшим.</span><span class="sxs-lookup"><span data-stu-id="c2c0a-153">The following interface is deprecated.</span></span>

-   [<span data-ttu-id="c2c0a-154">**ивмпфолдермониторсервицес**</span><span class="sxs-lookup"><span data-stu-id="c2c0a-154">**IWMPFolderMonitorServices**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpfoldermonitorservices)

## <a name="methods-that-are-no-longer-deprecated"></a><span data-ttu-id="c2c0a-155">Методы, которые больше не являются устаревшими</span><span class="sxs-lookup"><span data-stu-id="c2c0a-155">Methods That Are No Longer Deprecated</span></span>

<span data-ttu-id="c2c0a-156">Следующие методы были устаревшими в пакете SDK для проигрывателя Windows Media 11, но больше не являются устаревшими.</span><span class="sxs-lookup"><span data-stu-id="c2c0a-156">The following methods were deprecated in Windows Media Player 11 SDK, but are no longer deprecated.</span></span>

-   [<span data-ttu-id="c2c0a-157">**Ивмпграфкреатион:: Графкреатионпререндер**</span><span class="sxs-lookup"><span data-stu-id="c2c0a-157">**IWMPGraphCreation::GraphCreationPreRender**</span></span>](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpgraphcreation-graphcreationprerender)
-   [<span data-ttu-id="c2c0a-158">**Ивмпграфкреатион:: Графкреатионпострендер**</span><span class="sxs-lookup"><span data-stu-id="c2c0a-158">**IWMPGraphCreation::GraphCreationPostRender**</span></span>](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpgraphcreation-graphcreationpostrender)

## <a name="related-topics"></a><span data-ttu-id="c2c0a-159">См. также</span><span class="sxs-lookup"><span data-stu-id="c2c0a-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c2c0a-160">Сведения о пакете SDK проигрывателя Windows Media</span><span class="sxs-lookup"><span data-stu-id="c2c0a-160">About the Windows Media Player SDK</span></span>](about-the-windows-media-player-sdk.md)
</dt> </dl>

 

 




