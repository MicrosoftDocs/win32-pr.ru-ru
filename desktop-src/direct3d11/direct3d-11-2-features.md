---
title: Функции Direct3D 11,2
description: в Direct3D 11,2 добавлены следующие функциональные возможности, которые входят в состав Windows 8.1, Windows RT 8,1 и Windows Server 2012 R2.
ms.assetid: 2A2D9BBB-F53A-4187-A25B-F4E58C896EE2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1cd253cf618b3915c4f303691cab86a11cc9268061d536892c0ff5ccf4fffe4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124549"
---
# <a name="direct3d-112-features"></a>Функции Direct3D 11,2

в Direct3D 11,2 добавлены следующие функциональные возможности, которые входят в состав Windows 8.1, Windows RT 8,1 и Windows Server 2012 R2.

-   [Мозаичные ресурсы](#tiled-resources)
    -   [Проверка поддержки мозаичных ресурсов](#check-tiled-resources-support)
-   [Расширенная поддержка деформации устройств](#extended-support-for-warp-devices)
-   [Создание заметка для команд графики](#annotate-graphics-commands)
-   [Связывание шейдера HLSL](#hlsl-shader-linking)
    -   [Граф связывания функций (ФЛГ)](#function-linking-graph-flg)
-   [Компилятор HLSL входящих сообщений](#inbox-hlsl-compiler)
-   [Связанные темы](#related-topics)

## <a name="tiled-resources"></a>Мозаичные ресурсы

Direct3D 11,2 позволяет создавать мозаичные ресурсы, которые можно рассматривать как крупные логические ресурсы, использующие небольшие объемы физической памяти. Мозаичные ресурсы полезны (например,) с ландшафта в играх и пользовательском интерфейсе приложения.

Мозаичные ресурсы создаются путем указания флага [**D3D11 \_ ресурса " \_ Разное \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) ". Для работы с мозаичным ресурсом используйте следующие API:

-   [**ID3D11Device2:: Жетресаурцетилинг**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11device2-getresourcetiling)
-   [**ID3D11DeviceContext2:: Упдатетилес**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetiles)
-   [**ID3D11DeviceContext2:: Упдатетилемаппингс**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetilemappings)
-   [**ID3D11DeviceContext2:: Копитилес**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles)
-   [**ID3D11DeviceContext2:: Копитилемаппингс**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytilemappings)
-   [**ID3D11DeviceContext2:: Ресизетилепул**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-resizetilepool)
-   [**ID3D11DeviceContext2:: Тиледресаурцебарриер**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-tiledresourcebarrier)
-   **D3D11 \_ \_Функция отладки \_ Отключить \_ \_ Отслеживание сопоставления ресурсов мозаики \_ и флаг \_ \_ \_ проверки** с помощью [ **ID3D11Debug:: сетфеатуремаск**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11debug-setfeaturemask)

Дополнительные сведения о мозаичных ресурсах см. в разделе [мозаичные ресурсы](tiled-resources.md).

### <a name="check-tiled-resources-support"></a>Проверка поддержки мозаичных ресурсов

Перед использованием мозаичных ресурсов необходимо выяснить, поддерживает ли устройство мозаичные ресурсы. Вот как проверяется поддержка мозаичных ресурсов:


```C++
HRESULT hr = D3D11CreateDevice(
    nullptr,                    // Specify nullptr to use the default adapter.
    D3D_DRIVER_TYPE_HARDWARE,   // Create a device using the hardware graphics driver.
    0,                          // Should be 0 unless the driver is D3D_DRIVER_TYPE_SOFTWARE.
    creationFlags,              // Set debug and Direct2D compatibility flags.
    featureLevels,              // List of feature levels this app can support.
    ARRAYSIZE(featureLevels),   // Size of the list above.
    D3D11_SDK_VERSION,          // Always set this to D3D11_SDK_VERSION for Windows Store apps.
    &device,                    // Returns the Direct3D device created.
    &m_d3dFeatureLevel,         // Returns feature level of device created.
    &context                    // Returns the device immediate context.
    );

if (SUCCEEDED(hr))
{
    D3D11_FEATURE_DATA_D3D11_OPTIONS1 featureData;
    DX::ThrowIfFailed(
        device->CheckFeatureSupport(D3D11_FEATURE_D3D11_OPTIONS1, &featureData, sizeof(featureData))
        );

    m_tiledResourcesTier = featureData.TiledResourcesTier;
}
```



## <a name="extended-support-for-warp-devices"></a>Расширенная поддержка деформации устройств

Direct3D 11,2 расширяет поддержку [деформации](overviews-direct3d-11-devices-create-warp.md) устройств, которые создаются путем передачи [**\_ \_ \_ искривленного типа драйвера D3D**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type) в параметре *дривертипе* [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice). Модуль обработки ИСКРИВЛЕНного программного обеспечения в Direct3D 11,2 добавляет полную поддержку для [уровня функций](overviews-direct3d-11-devices-downlevel-intro.md) Direct3D 11 \_ 1, включая [мозаичные ресурсы](#tiled-resources), [**IDXGIDevice3:: Trim**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgidevice3-trim), общие поверхности BCn, минбленд и карту по умолчанию. Также включена [Двойная](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_doubles) поддержка в шейдерах HLSL с поддержкой 16x MSAA.

## <a name="annotate-graphics-commands"></a>Создание заметка для команд графики

Direct3D 11,2 позволяет создавать заметки к графическим командам с помощью этих API:

-   [**ID3D11DeviceContext2:: Исаннотатионенаблед**](/windows/desktop/api/d3d11_2/nf-d3d11_2-id3d11devicecontext2-isannotationenabled)
-   [**ID3D11DeviceContext2:: Бегиневентинт**](/windows/desktop/api/d3d11_2/nf-d3d11_2-id3d11devicecontext2-begineventint)
-   [**ID3D11DeviceContext2:: Сетмаркеринт**](/windows/desktop/api/d3d11_2/nf-d3d11_2-id3d11devicecontext2-setmarkerint)
-   [**ID3D11DeviceContext2:: Ендевент**](/windows/desktop/api/d3d11_2/nf-d3d11_2-id3d11devicecontext2-endevent)

## <a name="hlsl-shader-linking"></a>Связывание шейдера HLSL

Windows 8.1 добавляет отдельную компиляцию и связывание шейдеров HLSL, что позволяет графическим программистам создавать предкомпилированные функции HLSL, упаковывать их в библиотеки и связывать их с полными шейдерами во время выполнения. По сути, это эквивалентно отдельной компиляции, библиотекам и компоновке C/C++, а также позволяет программистам создавать предкомпилированный код HLSL, когда становится доступной дополнительная информация для завершения вычислений. Дополнительные сведения об использовании связывания шейдеров см. в разделе [Использование связывания шейдеров](/windows/desktop/direct3dhlsl/using-shader-linking).

Выполните следующие действия, чтобы создать окончательный шейдер с использованием динамической компоновки во время выполнения.

**Создание и использование связывания шейдера**

1.  Создайте объект компоновщика [**ID3D11Linker**](/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11linker) , который представляет контекст компоновки. Один контекст нельзя использовать для создания нескольких шейдеров. контекст компоновки используется для создания одного шейдера, после чего создается контекст компоновки.
2.  Используйте [**D3DLoadModule**](/windows/desktop/api/d3dcompiler/nf-d3dcompiler-d3dloadmodule) для загрузки и установки библиотек из их BLOB-объектов библиотеки.
3.  Используйте [**D3DLoadModule**](/windows/desktop/api/d3dcompiler/nf-d3dcompiler-d3dloadmodule) для загрузки и задания большого двоичного объекта шейдера записи или создания [шейдера флг](#function-linking-graph-flg).
4.  Используйте [**ID3D11Module**](/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11module)::[**CreateInstance**](/windows/desktop/api/D3D11Shader/nf-d3d11shader-id3d11module-createinstance) для создания объектов [**ID3D11ModuleInstance**](/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11moduleinstance) , а затем вызывайте функции для этих объектов, чтобы повторно привязать ресурсы к их конечным слотам.
5.  Добавьте библиотеки в компоновщик, а затем вызовите [**ID3D11Linker**](/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11linker)::[**Link**](/windows/desktop/api/D3D11Shader/nf-d3d11shader-id3d11linker-link) , чтобы создать окончательный байтовый код шейдера, который затем можно загрузить и использовать в среде выполнения так же, как полностью скомпилированный и связанный шейдер.

### <a name="function-linking-graph-flg"></a>Граф связывания функций (ФЛГ)

Windows 8.1 также добавляет Graph связывания функций (флг). ФЛГ можно использовать для создания шейдеров, состоящих из последовательности вызовов предкомпилированных функций, которые передают значения друг другу. При использовании ФЛГ нет необходимости писать HLSL и вызывать компилятор HLSL. Вместо этого структура шейдера задается программно с помощью вызовов API C++. Узлы ФЛГ представляют входные и выходные подписи и вызовы функций предкомпилированных библиотек. Порядок регистрации узлов вызова функции определяет последовательность вызовов. Сначала необходимо указать входной узел подписи, а выходной узел подписи должен быть указан последним. ФЛГ края определяют, как передаются значения из одного узла в другой. Типы данных передаваемых значений должны быть одинаковыми. неявное преобразование типа отсутствует. Правила Shape и группирующие следуют поведению HLSL, и значения могут передаваться в этой последовательности только вперед. Сведения об API ФЛГ см. в разделе [**ID3D11FunctionLinkingGraph**](/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11functionlinkinggraph).

## <a name="inbox-hlsl-compiler"></a>Компилятор HLSL входящих сообщений

компилятор HLSL теперь является папкой "входящие" Windows 8.1 и более поздних версий. теперь большинство api-интерфейсов для программирования шейдеров можно использовать в приложениях Windows Store, созданных для Windows 8.1 и более поздних версий. многие api-интерфейсы для программирования шейдеров не могут использоваться в приложениях Windows Store, созданных для Windows 8; эталонные страницы для этих API были отмечены заметкой. но некоторые api-интерфейсы шейдера (например, [**D3DCompileFromFile**](/windows/desktop/direct3dhlsl/d3dcompilefromfile)) можно использовать только для разработки приложений Windows store, а не в приложениях, которые вы отправляете в хранилище Windows. справочные страницы для этих API по-прежнему отмечены заметкой.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Новые возможности Direct3D 11](dx-graphics-overviews-introduction.md)
</dt> </dl>

 

 