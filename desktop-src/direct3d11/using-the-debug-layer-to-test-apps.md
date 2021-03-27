---
title: Использование слоя отладки для отладки приложений
description: Здесь мы поговорим о том, как включить слой отладки и некоторые проблемы, которые можно предотвратить с помощью слоя отладки.
ms.assetid: 3C2B0A12-FB57-4400-BE39-05ED23F552C7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aaa3f4748da6893470e3bb6631c4228ec1ae3d48
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773712"
---
# <a name="using-the-debug-layer-to-debug-apps"></a>Использование слоя отладки для отладки приложений

Рекомендуется использовать [отладочный уровень](overviews-direct3d-11-devices-layers.md) для отладки приложений, чтобы гарантировать, что они будут очищать ошибки и предупреждения. Слой отладки помогает писать код Direct3D. Кроме того, производительность может увеличиться при использовании слоя отладки, поскольку можно сразу увидеть причины ошибок скрытой отрисовки или даже черные экраны в источнике. Отладочный слой предоставляет предупреждения для многих проблем. Например, уровень отладки выдает предупреждения для этих проблем:

-   Забыли установить текстуру, но прочесть ее в шейдере пикселей
-   Глубина вывода, но не имеет привязки состояния шаблона глубины
-   Не удалось создать текстуру с помощью INVALIDARG

Здесь мы поговорим о том, как включить [слой отладки](overviews-direct3d-11-devices-layers.md) и некоторые проблемы, которые можно предотвратить с помощью слоя отладки.

-   [Включение слоя отладки](#enabling-the-debug-layer)
-   [Предотвращение ошибок в приложении с помощью слоя отладки](#preventing-errors-in-your-app-with-the-debug-layer)
    -   [Не передавать пустые указатели в Map](#dont-pass-null-pointers-to-map)
    -   [Ограничить исходное поле в исходных и целевых ресурсах](#confine-source-box-within-source-and-destination-resources)
    -   [Не удалять Дискардресаурце или Дискардвиев](#dont-drop-discardresource-or-discardview)
-   [См. также](#related-topics)

## <a name="enabling-the-debug-layer"></a>Включение слоя отладки

Чтобы включить [слой отладки](overviews-direct3d-11-devices-layers.md), укажите в параметре *flags* флаг [**D3D11 \_ Create \_ Device \_ Debug**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_create_device_flag) , если вызывается функция [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) для создания устройства отрисовки. В этом примере кода показано, как включить слой отладки, если проект Microsoft Visual Studio находится в отладочной сборке:


```C++
        UINT creationFlags = D3D11_CREATE_DEVICE_BGRA_SUPPORT;
#if defined(_DEBUG)
        // If the project is in a debug build, enable the debug layer.
        creationFlags |= D3D11_CREATE_DEVICE_DEBUG;
#endif
        // Define the ordering of feature levels that Direct3D attempts to create.
        D3D_FEATURE_LEVEL featureLevels[] =
        {
            D3D_FEATURE_LEVEL_11_1,
            D3D_FEATURE_LEVEL_11_0,
            D3D_FEATURE_LEVEL_10_1,
            D3D_FEATURE_LEVEL_10_0,
            D3D_FEATURE_LEVEL_9_3,
            D3D_FEATURE_LEVEL_9_1
        };

        ComPtr<ID3D11Device> d3dDevice;
        ComPtr<ID3D11DeviceContext> d3dDeviceContext;
        DX::ThrowIfFailed(
            D3D11CreateDevice(
                nullptr,                    // specify nullptr to use the default adapter
                D3D_DRIVER_TYPE_HARDWARE,
                nullptr,                    // specify nullptr because D3D_DRIVER_TYPE_HARDWARE 
                                            // indicates that this function uses hardware
                creationFlags,              // optionally set debug and Direct2D compatibility flags
                featureLevels,
                ARRAYSIZE(featureLevels),
                D3D11_SDK_VERSION,          // always set this to D3D11_SDK_VERSION
                &d3dDevice,
                nullptr,
                &d3dDeviceContext
                )
            );
```



## <a name="preventing-errors-in-your-app-with-the-debug-layer"></a>Предотвращение ошибок в приложении с помощью слоя отладки

При неправильном использовании API Direct3D 11 или при передаче неправильных параметров отладочный вывод [слоя отладки](overviews-direct3d-11-devices-layers.md) сообщает об ошибке или предупреждении. После этого можно исправить ошибку. Далее мы рассмотрим некоторые проблемы с кодированием, которые могут вызвать неопределенное поведение или даже сбой операционной системы. Можно перехватывать и предотвращать эти проблемы с помощью слоя отладки.

### <a name="dont-pass-null-pointers-to-map"></a>Не передавать пустые указатели в Map

Если **значение NULL** передается *в* параметре *Пмаппедресаурце* или в методе [**ссылку ID3D11DeviceContext:: Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) , поведение **Map** не определено. Если вы создали устройство, которое только поддерживает [основной уровень](overviews-direct3d-11-devices-layers.md), недопустимые параметры для **Map** могут вызвать сбой операционной системы. Если вы создали устройство, которое поддерживает [отладочный слой](overviews-direct3d-11-devices-layers.md), отладочный вывод сообщает об ошибке в этом неверном вызове **Map** .

### <a name="confine-source-box-within-source-and-destination-resources"></a>Ограничить исходное поле в исходных и целевых ресурсах

При вызове метода [**ссылку ID3D11DeviceContext:: кописубресаурцерегион**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copysubresourceregion) исходное поле должно находиться в пределах исходного ресурса. Смещение назначения (x, y и z) разрешает смещение исходного поля при записи в целевой ресурс, но размеры исходного поля и смещения должны быть в пределах размера ресурса. При попытке копирования за пределами целевого ресурса или указания исходного поля, которое больше, чем исходный ресурс, поведение **кописубресаурцерегион** не определено. Если вы создали устройство, которое поддерживает [отладочный слой](overviews-direct3d-11-devices-layers.md), выходные данные отладки будут сообщать об ошибке в этом недействительном вызове **кописубресаурцерегион** . Недопустимые параметры **кописубресаурцерегион** приводят к неопределенному поведению и могут привести к неправильной отрисовке, обрезке, отсутствию копии или даже удалению устройства отрисовки.

### <a name="dont-drop-discardresource-or-discardview"></a>Не удалять Дискардресаурце или Дискардвиев

Среда выполнения удаляет вызов [**ID3D11DeviceContext1::D искардресаурце**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardresource) или [**ID3D11DeviceContext1::D искардвиев**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardview) , если ресурс не был правильно создан.

Ресурс, который передается в [**ID3D11DeviceContext1::D искардресаурце**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardresource) , должен быть создан с помощью [**D3D11 \_ использования \_ по умолчанию**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage) или [**\_ \_ динамического использования D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage). в противном случае среда выполнения удаляет вызов **дискардресаурце**.

Ресурс, лежащий в основе представления, передаваемого в [**ID3D11DeviceContext1::D искардвиев**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardview) , должен быть создан с помощью [**D3D11 \_ использования \_ по умолчанию**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage) или [**\_ \_ динамического использования D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage). в противном случае среда выполнения удаляет вызов **дискардвиев**.

Если вы создали устройство, которое поддерживает [уровень отладки](overviews-direct3d-11-devices-layers.md), отладочный вывод сообщает об ошибке в отношении удаленного вызова.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Программные уровни](overviews-direct3d-11-devices-layers.md)
</dt> </dl>

 

 




