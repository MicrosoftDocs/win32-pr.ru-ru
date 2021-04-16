---
description: В графической инфраструктуре Microsoft DirectX (DXGI) 1,2 добавлены следующие функциональные возможности.
ms.assetid: E2D8DA99-4EA2-4847-B699-80A6994C66C0
title: Улучшения в DXGI 1.2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bd274918d179bc7adeb8dd132fe604cf56d80f2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105710575"
---
# <a name="dxgi-12-improvements"></a>Улучшения в DXGI 1.2

В графической инфраструктуре Microsoft DirectX (DXGI) 1,2 добавлены следующие функциональные возможности.

## <a name="presentation-enhancements-and-optimizations"></a>Улучшения и оптимизации представления

DXGI 1,2 расширяет презентацию с помощью новой цепочки перестановки, защиты содержимого, безоконного представления и оптимизированной презентации, где указываются «грязные» прямоугольники и области с прокруткой. Презентация также улучшена с помощью стереоскопик трехмерного отображения.

Для расширенного представления можно использовать следующий API-интерфейс DXGI 1,2.

-   [**Идксгидисплайконтрол:: Исстереоенаблед**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgidisplaycontrol-isstereoenabled)
-   [**Идксгидисплайконтрол:: Сетстереоенаблед**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgidisplaycontrol-setstereoenabled)
-   [**IDXGIFactory2:: Креатесвапчаинфорхвнд**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforhwnd)
-   [**IDXGIFactory2:: Креатесвапчаинфоркоревиндов**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcorewindow)
-   [**IDXGIFactory2:: Креатесвапчаинфоркомпоситион**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcomposition)
-   [**IDXGIFactory2:: Исвиндоведстереоенаблед**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-iswindowedstereoenabled)
-   [**IDXGIFactory2:: Регистерстереостатусвиндов**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-registerstereostatuswindow)
-   [**IDXGIFactory2:: Регистерстереостатусевент**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-registerstereostatusevent)
-   [**IDXGIFactory2:: Унрегистерстереостатус**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-unregisterstereostatus)
-   [**IDXGIFactory2:: Регистерокклусионстатусвиндов**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-registerocclusionstatuswindow)
-   [**IDXGIFactory2:: Регистерокклусионстатусевент**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-registerocclusionstatusevent)
-   [**IDXGIFactory2:: Унрегистерокклусионстатус**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-unregisterocclusionstatus)
-   [**IDXGIOutput1::GetDisplayModeList1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutput1-getdisplaymodelist1)
-   [**IDXGIOutput1::GetDisplaySurfaceData1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutput1-getdisplaysurfacedata1)
-   [**IDXGIOutput1::FindClosestMatchingMode1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutput1-findclosestmatchingmode1)
-   [**IDXGIResource1:: Креатесубресаурцесурфаце**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiresource1-createsubresourcesurface)
-   [**IDXGISurface2:: \ Resource**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgisurface2-getresource)
-   [**IDXGISwapChain1::GetDesc1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-getdesc1)
-   [**IDXGISwapChain1:: Жетфуллскриндеск**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-getfullscreendesc)
-   [**IDXGISwapChain1:: "HWND"**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-gethwnd)
-   [**IDXGISwapChain1:: Жеткоревиндов**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-getcorewindow)
-   [**IDXGISwapChain1::Present1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1)
-   [**IDXGISwapChain1:: Истемпораримоносуппортед**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-istemporarymonosupported)
-   [**IDXGISwapChain1:: Жетрестрикттуутпут**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-getrestricttooutput)
-   [**IDXGISwapChain1:: Сетбаккграундколор**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-setbackgroundcolor)
-   [**IDXGISwapChain1:: Жетбаккграундколор**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-getbackgroundcolor)
-   [**IDXGISwapChain1:: Сетротатион**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-setrotation)
-   [**IDXGISwapChain1:: вращение**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-getrotation)

Дополнительные сведения об использовании API DXGI 1,2 для расширенного представления см. [в разделе Улучшение представления с помощью модели перелистывания, "грязных" прямоугольников и прокрутки областей](dxgi-1-2-presentation-improvements.md).

Сведения о том, как определить, можно ли отобразить в стерео, см. [в разделе Просмотр в стерео и уведомление о состоянии стерео](stereo-rendering-stereo-status-notifying.md).

Сведения о том, как определить изменения в состоянии перекрытия в приложении, см. в разделе [ожидание события, когда подготовка к просмотру не требуется](waiting-when-occluded.md).

Сведения об изменении значений данных при отображении содержимого на экране см. в разделе [Преобразование данных для цветового пространства](converting-data-color-space.md).

## <a name="desktop-duplication"></a>Дублирование рабочего стола

Windows 8 отключает стандартные драйверы для зеркального отображения стандартных драйверов (КСДДМ) Windows 2000. DXGI 1,2 предоставляет в качестве альтернативы API дублирования рабочего стола. API дублирования настольных систем обеспечивает удаленный доступ к образу рабочего стола для сценариев совместной работы.

API дублирования настольных систем состоит из следующих методов.

-   [**IDXGIOutput1::D Упликатеаутпут**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutput1-duplicateoutput)
-   [**Идксгиаутпутдупликатион:: DESC**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getdesc)
-   [**Идксгиаутпутдупликатион:: Аккуиренекстфраме**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe)
-   [**Идксгиаутпутдупликатион:: Жетфрамедиртиректс**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getframedirtyrects)
-   [**Идксгиаутпутдупликатион:: Жетфрамемоверектс**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getframemoverects)
-   [**Идксгиаутпутдупликатион:: Жетфрамепоинтершапе**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getframepointershape)
-   [**Идксгиаутпутдупликатион:: Мапдесктопсурфаце**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-mapdesktopsurface)
-   [**Идксгиаутпутдупликатион:: Унмапдесктопсурфаце**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-unmapdesktopsurface)
-   [**Идксгиаутпутдупликатион:: Релеасефраме**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-releaseframe)

Дополнительные сведения об использовании API дублирования настольных систем см. в разделе [API для дублирования настольных систем](desktop-dup-api.md).

## <a name="improved-usage-of-shared-resources-and-synchronized-events"></a>Улучшенное использование общих ресурсов и синхронизированных событий

В предыдущих версиях Windows приложения используют непрерывный опрос, чтобы определить, завершила ли графический процессор (GPU) обработку произвольных команд. DXGI 1,2 позволяет приложению поместить событие в очередь на устройство DXGI. Затем приложение может подождать, пока устройство DXGI не сообщит о событии, чтобы определить, что GPU завершил исполнение всех команд отрисовки. DXGI 1,2 позволяет нескольким устройствам совместно использовать ресурсы с помощью обработчика NT.

Для совместного использования ресурсов и синхронизации событий можно использовать следующий API-интерфейс DXGI 1,2 и API Direct3D 11,1.

-   [**IDXGIDevice2:: Енкуеуесетевент**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgidevice2-enqueuesetevent)
-   [**IDXGIResource1:: Креатешаредхандле**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiresource1-createsharedhandle)
-   [**IDXGIFactory2:: Жетшаредресаурцеадаптерлуид**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-getsharedresourceadapterluid)
-   [**ID3D11Device1::OpenSharedResource1**](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11device1-opensharedresource1)
-   [**ID3D11Device1:: Опеншаредресаурцебинаме**](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11device1-opensharedresourcebyname)
-   [**\_ \_ \_ Общие \_ нсандле ресурсов D3D11**](/windows/win32/api/d3d11/ne-d3d11-d3d11_resource_misc_flag)

## <a name="offer-the-video-memory-of-resources"></a>Предоставление видео памяти ресурсов

DXGI 1,2 позволяет приложению предложить видеопамять ресурсов с низкой нагрузкой. Предлагая видеопамять, операционная система может освободить видеопамять.

Эта функция DXGI 1,2 состоит из следующих методов.

-   [**IDXGIDevice2:: Офферресаурцес**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgidevice2-offerresources)
-   [**IDXGIDevice2:: Реклаимресаурцес**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgidevice2-reclaimresources)

Можно использовать метод [**ID3D11Debug:: сетфеатуремаск**](/windows/win32/api/d3d11sdklayers/nf-d3d11sdklayers-id3d11debug-setfeaturemask) для установки флагов маски компонентов, которые отлаживать поведение методов [**IDXGIDevice2:: офферресаурцес**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgidevice2-offerresources) и [**IDXGIDevice2:: реклаимресаурцес**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgidevice2-reclaimresources) в приложении.

## <a name="gpu-preemption-at-finer-granularity-levels-for-wddm-12-driver-model"></a>Приоритетное прерывание GPU на более мелких уровнях гранулярности для модели драйвера WDDM 1,2

Начиная с модели драйвера WDDM 1,2, планировщик WDDM может запланировать выполнение задач приложения с более тонкими уровнями детализации GPU. DXGI 1,2 позволяет определить уровни гранулярности при вытеснении GPU.

Эта функция DXGI 1,2 состоит из следующего метода.

-   [**IDXGIAdapter2::GetDesc2**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiadapter2-getdesc2)

## <a name="debugging-apis"></a>Отладка API

Пакет SDK для Windows 8 предоставляет дополнительные возможности отладки. Вы можете использовать следующие API-интерфейсы DXGI из Dxgidebug.dll для отладки приложения:

-   [**дксгижетдебугинтерфаце**](/windows/desktop/api/DXGIDebug/nf-dxgidebug-dxgigetdebuginterface)
-   [**идксгидебуг**](/windows/desktop/api/DXGIDebug/nn-dxgidebug-idxgidebug)
-   [**идксгиинфокуеуе**](/windows/desktop/api/DXGIDebug/nn-dxgidebug-idxgiinfoqueue)

Для доступа к [**дксгижетдебугинтерфаце**](/windows/desktop/api/DXGIDebug/nf-dxgidebug-dxgigetdebuginterface)вызовите функцию [**Ошибка GetModuleHandle**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea) , чтобы получить Dxgidebug.dll и функцию [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) для получения адреса **дксгижетдебугинтерфаце**. Затем можно вызвать **дксгижетдебугинтерфаце** , чтобы получить интерфейс [**идксгидебуг**](/windows/desktop/api/DXGIDebug/nn-dxgidebug-idxgidebug) или [**идксгиинфокуеуе**](/windows/desktop/api/DXGIDebug/nn-dxgidebug-idxgiinfoqueue) .

Сведения об удаленной отладке приложений DirectX см. в разделе [Отладка приложений DirectX удаленно](../direct3dtools/debugging-directx-apps-remotely.md).

## <a name="related-topics"></a>См. также

[Руководством по программированию для DXGI](dx-graphics-dxgi-overviews.md)
