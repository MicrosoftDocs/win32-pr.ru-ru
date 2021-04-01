---
title: Обновление платформы для Windows 7
description: В этом разделе описываются усовершенствования компонентов графического стека Windows 7, которые становятся доступными через обновление платформы для Windows 7.
ms.assetid: C6DC0D38-E17C-4924-AF7C-6AE74C6C50D1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49fd1e6e2681673d2bb2bab7a4a6de42f77988eb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103890981"
---
# <a name="platform-update-for-windows-7"></a>Обновление платформы для Windows 7

В этом разделе описываются усовершенствования компонентов графического стека Windows 7, которые становятся доступными через [обновление платформы для Windows 7](https://support.microsoft.com/kb/2670838).

При установке в Windows 7 обновление платформы для Windows 7 обновляет Windows 7 с функциями, доступными в Windows 8. Например, эти компоненты Windows 8 становятся доступными с полной функциональностью:

-   Direct2D 1,1 (включая эффекты Direct2D)
-   DirectWrite
-   Компонент обработки изображений Windows (WIC)

Они обеспечивают частичную функциональность:

-   Direct3D 11,1
-   DXGI 1,2

Например, этот компонент недоступен.

-   DirectComposition (Дкомп)

Сведения о Direct2D, DirectWrite и WIC с обновлением платформы см. в следующих разделах:

-   [Новые возможности Direct2D для Windows 8 (Windows)](/windows/desktop/Direct2D/what-s-new-in-direct2d-for-windows-8-consumer-preview)
-   [Новые возможности DirectWrite для Windows 8 (Windows)](/windows/desktop/DirectWrite/what-s-new-in-directwrite-for-windows-8-consumer-preview)
-   [Новые возможности WIC в Windows 8 (Windows)](/previous-versions//hh994467(v=vs.85))

Сведения о Direct3D и DXGI с обновлением платформы см. в следующих разделах:

-   [Функции D3D 11.1](/windows/desktop/direct3d11/direct3d-11-1-features)
-   [Усовершенствования DXGI 1,2](/windows/desktop/direct3ddxgi/dxgi-1-2-improvements)

После установки обновления платформы интерфейсы, появившиеся в Direct3D 11.1 и DXGI 1,2, будут доступны с частичной функциональностью. Функции этих графических компонентов связаны непосредственно с компонентами ядра графики, графическими драйверами и графическим оборудованием. Прежде чем использовать Direct3D 11.1 в Windows 7, ознакомьтесь со следующими спецификами:

-   В Windows 8 появилась модель драйвера WDDM 1,2, которая предоставляет улучшения в связанной области API для всех [уровней компонентов](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro). При чтении документации по Direct3D 11.1 необходимо понимать, что *новые драйверы* означают драйверы WDDM 1,2. Эти обновленные версии драйверов, а также большинство дополнительных функций, предоставляемых через [**чеккфеатуресуппорт**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-checkfeaturesupport), недоступны в Windows 7. Поскольку нет никакой гарантии, что эти необязательные функции доступны, убедитесь, что приложения имеют соответствующие резервные поведения в случае недоступности требуемой функциональности.

    Есть одно важное исключение. Некоторые функции, такие как [**PSSetConstantBuffers1**](/windows/desktop/api/d3d11_1/nf-d3d11_1-id3d11devicecontext1-pssetconstantbuffers1) с смещениями постоянного буфера, занимают новые драйверы на [уровне компонентов](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 10 и выше, но на самом деле имитируются на уровне функций 9. Эта Эмуляция доступна в Windows 7 с обновлением платформы. Дополнительные сведения о том, какие функции эмулироваться, см. в статье [**D3D11 \_ Feature \_ Data \_ D3D11 \_ Options**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options) .

-   Модель драйвера WDDM 1,2 для Windows 8 поддерживает новое поколение оборудования, предоставляемое на [уровне функций](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) D3D 11,1. Windows 7 с обновлением платформы поддерживает только модель драйвера WDDM 1,1, поэтому поддержка оборудования на уровне компонентов 11,1 недоступна (через обновление платформы). В Windows 7 с обновлением платформы [**D3D11CreateDevice**](/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice) всегда возвращает уровень компонентов 11,0 или ниже, за исключением устройства с эталонным устройством, которое можно использовать для проверки пути кода 11,1 в Windows 7. Используйте только функции, доступные на целевых уровнях функций, как описано в справочнике по уровню функций.
-   Некоторые новые методы, появившиеся в ДГКСИ 1,2, не полностью поддерживаются в обновлении платформы для Windows 7. можно проверить доступность этих функций, вызвав их напрямую и проверив код ошибки. Убедитесь, что приложения, предназначенные для Windows 7 с обновлением платформы, имеют резервный вариант, если требуемая функциональность недоступна. Эти классы функций недоступны в обновлении платформы для Windows 7:

    -   Stereo
    -   Цепочек переключений не нацелен на HWND
    -   Уведомления о состоянии перекрытия
    -   Дублирование рабочего стола
    -   Ресурсы по обработке NT

    В частности, следующие API-интерфейсы будут возвращать \_ ошибку DXGI \_ , не поддерживаемую, \_ Ошибка DXGI \_ Недопустимый \_ вызов, e \_ нотимпл или e \_ INVALIDARG:

    -   [**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2)::[**креатесвапчаинфоркоревиндов**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcorewindow)
    -   [**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2)::[**креатесвапчаинфоркомпоситион**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcomposition)
    -   [**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2)::[**регистерстереостатусвиндов**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-registerstereostatuswindow)
    -   [**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2)::[**регистерстереостатусевент**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-registerstereostatusevent)
    -   [**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2)::[**унрегистерстереостатус**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-unregisterstereostatus)
    -   [**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2)::[**регистерокклусионстатусвиндов**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-registerocclusionstatuswindow)
    -   [**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2)::[**регистерокклусионстатусевент**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-registerocclusionstatusevent)
    -   [**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2)::[**унрегистерокклусионстатус**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-unregisterocclusionstatus)
    -   [**IDXGISwapChain1**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiswapchain1)::[**жеткоревиндов**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-getcorewindow)
    -   [**IDXGISwapChain1**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiswapchain1)::[**сетротатион**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-setrotation)
    -   [**IDXGISwapChain1**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiswapchain1)::[**вращение**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-getrotation)
    -   [**IDXGIOutput1**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgioutput1)::[**дупликатеаутпут**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgioutput1-duplicateoutput)
    -   [**IDXGIDevice2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgidevice2)::[**енкуеуесетевент**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgidevice2-enqueuesetevent)
    -   [**IDXGIResource1**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiresource1)::[**креатешаредхандле**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiresource1-createsharedhandle)
    -   [**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2)::[**жетшаредресаурцеадаптерлуид**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-getsharedresourceadapterluid)
    -   [**ID3D11Device1**](/windows/desktop/api/d3d11_1/nn-d3d11_1-id3d11device1)::[**OpenSharedResource1**](/windows/desktop/api/d3d11_1/nf-d3d11_1-id3d11device1-opensharedresource1)
    -   [**ID3D11Device1**](/windows/desktop/api/d3d11_1/nn-d3d11_1-id3d11device1)::[**опеншаредресаурцебинаме**](/windows/desktop/api/d3d11_1/nf-d3d11_1-id3d11device1-opensharedresourcebyname)

-   Эти API имеют различия в поведении, как отмечалось:
    -   [**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2)::[**креатесвапчаинфорхвнд**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforhwnd) принимает структуру [**\_ \_ \_ DESC1 цепочки переключения DXGI**](/windows/desktop/api/dxgi1_2/ns-dxgi1_2-dxgi_swap_chain_desc1) , которая содержит поле для **масштабирования**. [**DXGI \_ МАСШТАБИРОВАНие \_ None**](/windows/desktop/api/dxgi1_2/ne-dxgi1_2-dxgi_scaling) не поддерживается в Windows 7 с обновлением платформы и приводит к тому, что **КРЕАТЕСВАПЧАИНФОРХВНД** возвращает \_ ошибку DXGI \_ Недопустимый \_ вызов при вызове.
    -   [**IDXGISwapChain1**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiswapchain1)::[**сетбаккграундколор**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-setbackgroundcolor) полезен только при задании в ИМЕЮЩУЮСЯ ЦЕПОЧКУ БУФЕРОВ с помощью функции DXGI \_ SCALING \_ None. Его значение по-прежнему хранится и может быть извлечено, но не имеет результата.
    -   [**Идксгидисплайконтрол**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgidisplaycontrol)::[**исстереоенаблед**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgidisplaycontrol-isstereoenabled), [**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2)::[**исвиндоведстереоенаблед**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-iswindowedstereoenabled)и [**IDXGISwapChain1**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiswapchain1)::[**истемпораримоносуппортед**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-istemporarymonosupported) ALL возвращают **значение false**.
    -   [**IDXGIOutput1**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgioutput1)::[**GetDisplayModeList1**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgioutput1-getdisplaymodelist1) и **IDXGIOutput1**::[**FindClosestMatchingMode1**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgioutput1-findclosestmatchingmode1) были добавлены для облегчения режимов вывода стерео. Стерео не поддерживается в обновлении платформы для Windows 7, поэтому этот метод эквивалентен [**идксгиаутпут**](/windows/desktop/api/dxgi/nn-dxgi-idxgioutput)::[**Финдклосестматчингмоде**](/windows/desktop/api/dxgi/nf-dxgi-idxgioutput-findclosestmatchingmode) в [**\_ режиме DXGI \_ DESC1**](/windows/desktop/api/dxgi1_2/ns-dxgi1_2-dxgi_mode_desc1). Стерео всегда будет иметь значение FALSE.
    -   [**IDXGIDevice2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgidevice2)::[**офферресаурцес**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgidevice2-offerresources) и **IDXGIDevice2**::[**реклаимресаурцес**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgidevice2-reclaimresources) не поддерживаются в обновлении платформы для Windows 7. Однако среда выполнения по-прежнему позволяет вызывать их и выполняет проверку правильности их использования в ресурсах, не являющихся общими.
    -   Устройства [деформации](/windows/desktop/direct3d11/overviews-direct3d-11-devices-create-warp) поддерживают только [уровень компонентов](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 11,0. Это значит, что устройства, созданные с помощью передачи [ \_ \_ типов \_ драйвера D3D](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_driver_type) , в параметре *дривертипе* [**D3D11CreateDevice**](/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice) не поддерживают 11,1 и не поддерживают общие поверхности.
-   Для разработчиков, работающих с приложениями в Microsoft Visual Studio 2010 или более ранней версии с помощью флага [**D3D11 \_ Create \_ Device \_ Debug**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_create_device_flag) , имейте в виду, что вызовы в [**D3D11CreateDevice**](/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice) завершатся ошибкой. Это обусловлено тем, что среда выполнения D3D 11.1 теперь требует D3D11 \_1SDKLayers.dll вместо D3D11SDKLayers.dll. Чтобы получить новую библиотеку DLL (D3D11 \_1SDKLayers.dll), установите [пакет SDK для Windows 8](https://dev.windows.com/downloads/windows-8-sdk)или [Visual Studio 2012](https://www.microsoft.com/visualstudio/eng/downloads)или средства удаленной отладки Visual Studio 2012. Дополнительные сведения см. в документации по [отладочному слою](/windows/desktop/direct3d11/overviews-direct3d-11-devices-layers) .

 

 