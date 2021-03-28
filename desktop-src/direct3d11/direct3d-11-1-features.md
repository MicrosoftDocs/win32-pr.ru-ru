---
title: Функции Direct3D 11,1
description: В Direct3D 11,1 добавлены следующие функциональные возможности, которые входят в состав Windows 8, Windows RT и Windows Server 2012.
ms.assetid: 2203D2D2-ECF6-4753-90FA-12A52678DFBB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dece9ed6e0a40ade28857277c344be0e9f2e7ce1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103791772"
---
# <a name="direct3d-111-features"></a>Функции Direct3D 11,1

В Direct3D 11,1 добавлены следующие функциональные возможности, которые входят в состав Windows 8, Windows RT и Windows Server 2012. Частичная поддержка [Direct3D 11,1](direct3d-11-features.md) доступна в Windows 7 и windows Server 2008 R2 через [обновление платформы для Windows 7](/windows/desktop/direct3darticles/platform-update-for-windows-7), которое доступно в [обновлении платформы для Windows 7](https://support.microsoft.com/kb/2670838).

-   [Усовершенствования трассировки шейдеров и компилятора](#shader-tracing-and-compiler-enhancements)
-   [Общий доступ к устройствам Direct3D](#direct3d-device-sharing)
-   [Проверка поддержки новых функций и форматов Direct3D 11,1](#check-support-of-new-direct3d-111-features-and-formats)
-   [Использовать минимальную точность HLSL](#use-hlsl-minimum-precision)
-   [Указать пользовательские плоскости в HLSL на уровне компонентов 9 и выше](#specify-user-clip-planes-in-hlsl-on-feature-level-9-and-higher)
-   [Создавать большие буферы констант, чем шейдер может получить доступ](#create-larger-constant-buffers-than-a-shader-can-access)
-   [Использование логических операций в целевом объекте прорисовки](#use-logical-operations-in-a-render-target)
-   [Принудительное создание состояния средства программной прорисовки для счетчика выборки](#force-the-sample-count-to-create-a-rasterizer-state)
-   [Обработка видеоресурсов с помощью шейдеров](#process-video-resources-with-shaders)
-   [Расширенная поддержка общих ресурсов Texture2D](#extended-support-for-shared-texture2d-resources)
-   [Изменение подресурсов с помощью новых параметров копирования](#change-subresources-with-new-copy-options)
-   [Удалить ресурсы и представления ресурсов](#discard-resources-and-resource-views)
-   [Поддержка большего числа Уавс](#support-a-larger-number-of-uavs)
-   [Привязка поддиапазона буфера константы к шейдеру](#bind-a-subrange-of-a-constant-buffer-to-a-shader)
-   [Получение поддиапазона буфера констант, привязанного к шейдеру](#retrieve-the-subrange-of-a-constant-buffer-that-is-bound-to-a-shader)
-   [Очистка представления ресурсов или его части](#clear-all-or-part-of-a-resource-view)
-   [Сопоставьте СРВС динамических буферов без \_ ПЕРЕзаписи](/windows)
-   [Использование Уавс на каждом этапе конвейера](#use-uavs-at-every-pipeline-stage)
-   [Расширенная поддержка деформации устройств](#extended-support-for-warp-devices)
-   [Использование Direct3D в процессах сеанса 0](#use-direct3d-in-session-0-processes)
-   [Поддержка теневого буфера на уровне функций 9](#support-for-shadow-buffer-on-feature-level-9)
-   [См. также](#related-topics)

## <a name="shader-tracing-and-compiler-enhancements"></a>Усовершенствования трассировки шейдеров и компилятора

Direct3D 11,1 позволяет использовать трассировку шейдера, чтобы убедиться в том, что код выполняется как задуманный, и если это не удается обнаружить и устранить проблему. Пакет средств разработки программного обеспечения (SDK) для Windows 8 содержит улучшения компилятора HLSL. Трассировка шейдеров и компилятор HLSL реализуются в D3dcompiler \_nn.dll.

API трассировки шейдеров и усовершенствования компилятора HLSL состоят из следующих методов и функций.

-   [**ID3D11RefDefaultTrackingOptions:: Сеттраккингоптионс**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11refdefaulttrackingoptions-settrackingoptions)
-   [**ID3D11RefTrackingOptions:: Сеттраккингоптионс**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11reftrackingoptions-settrackingoptions)
-   [**ID3D11TracingDevice:: Сетшадертраккингоптионс**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11tracingdevice-setshadertrackingoptionsbytype)
-   [**ID3D11TracingDevice:: Сетшадертраккингоптионсбитипе**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11tracingdevice-setshadertrackingoptionsbytype)
-   [**ID3D11ShaderTraceFactory:: Креатешадертраце**](/windows/desktop/api/D3D11ShaderTracing/nf-d3d11shadertracing-id3d11shadertracefactory-createshadertrace)
-   [**ID3D11ShaderTrace:: Трацереади**](/windows/desktop/api/D3D11ShaderTracing/nf-d3d11shadertracing-id3d11shadertrace-traceready)
-   [**ID3D11ShaderTrace:: Ресеттраце**](/windows/desktop/api/D3D11ShaderTracing/nf-d3d11shadertracing-id3d11shadertrace-resettrace)
-   [**ID3D11ShaderTrace:: Жеттрацестатс**](/windows/desktop/api/D3D11ShaderTracing/nf-d3d11shadertracing-id3d11shadertrace-gettracestats)
-   [**ID3D11ShaderTrace::P Сселектстамп**](/windows/desktop/api/D3D11ShaderTracing/nf-d3d11shadertracing-id3d11shadertrace-psselectstamp)
-   [**ID3D11ShaderTrace:: Жетинитиалрегистерконтентс**](/windows/desktop/api/D3D11ShaderTracing/nf-d3d11shadertracing-id3d11shadertrace-getinitialregistercontents)
-   [**ID3D11ShaderTrace:: onstep**](/windows/desktop/api/D3D11ShaderTracing/nf-d3d11shadertracing-id3d11shadertrace-getstep)
-   [**ID3D11ShaderTrace:: Жетвриттенрегистер**](/windows/desktop/api/D3D11ShaderTracing/nf-d3d11shadertracing-id3d11shadertrace-getwrittenregister)
-   [**ID3D11ShaderTrace:: Жетреадрегистер**](/windows/desktop/api/D3D11ShaderTracing/nf-d3d11shadertracing-id3d11shadertrace-getreadregister)
-   [**D3DCompile2**](/windows/desktop/direct3dhlsl/d3dcompile2)
-   [**D3DCompileFromFile**](/windows/desktop/direct3dhlsl/d3dcompilefromfile)
-   [**D3DDisassemble11Trace**](/windows/desktop/direct3dhlsl/d3ddisassemble11trace)
-   [**D3DDisassembleRegion**](/windows/desktop/direct3dhlsl/d3ddisassembleregion)
-   [**D3DGetTraceInstructionOffsets**](/windows/desktop/direct3dhlsl/d3dgettraceinstructionoffsets)
-   [**D3DReadFileToBlob**](/windows/desktop/direct3dhlsl/d3dreadfiletoblob)
-   [**D3DSetBlobPart**](/windows/desktop/direct3dhlsl/d3dsetblobpart)
-   [**D3DWriteBlobToFile**](/windows/desktop/direct3dhlsl/d3dwriteblobtofile)

Для библиотеки D3dcompiler. lib требуется D3dcompiler \_nn.dll. Эта библиотека DLL не является частью Windows 8; Он находится в \\ папке bin Windows SDK для Windows 8 вместе с Fxc.exe версией КОМПИЛЯТОРА HLSL в командной строке.

> [!Note]  
> Хотя эту библиотеку и библиотеку DLL можно использовать для разработки, нельзя развертывать приложения Магазина Windows, использующие это сочетание. Поэтому перед догрузкой приложения для Магазина Windows необходимо скомпилировать Шейдеры HLSL. Можно записать двоичные файлы компиляции HLSL на диск или компилятор может создавать заголовки со статическими массивами байтов, содержащими данные BLOB-объектов шейдера. Для доступа к данным большого двоичного объекта используется интерфейс [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)) . Чтобы разработать приложение для Магазина Windows, вызовите [**D3DCompile2**](/windows/desktop/direct3dhlsl/d3dcompile2) или [**D3DCompileFromFile**](/windows/desktop/direct3dhlsl/d3dcompilefromfile) , чтобы скомпилировать необработанный источник HLSL, а затем передать полученные данные большого двоичного объекта в Direct3D.

 

## <a name="direct3d-device-sharing"></a>Общий доступ к устройствам Direct3D

Direct3D 11,1 включает API Direct3D 10 и API Direct3D 11 для использования одного базового устройства отрисовки.

Эта функция Direct3D 11,1 состоит из следующих методов и интерфейса.

-   [**ID3D11Device1:: Креатедевицеконтекстстате**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11device1-createdevicecontextstate)
-   [**ID3D11DeviceContext1:: Свапдевицеконтекстстате**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-swapdevicecontextstate)
-   [**ID3DDeviceContextState**](/windows/win32/api/d3d11_1/nn-d3d11_1-id3ddevicecontextstate)

## <a name="check-support-of-new-direct3d-111-features-and-formats"></a>Проверка поддержки новых функций и форматов Direct3D 11,1

Direct3D 11,1 позволяет проверять наличие новых функций, поддерживаемых графическим драйвером, и новых способов поддержки формата на устройстве. В графической инфраструктуре Microsoft DirectX (DXGI) 1,2 также указываются новые значения [**\_ формата DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) .

Эта функция Direct3D 11,1 состоит из следующего API.

-   [**ID3D11Device:: чеккфеатуресуппорт**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) с [**\_ параметрами D3D11 \_ Data \_ D3D11 \_**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options), [**D3D11, \_ \_ \_ \_ сведения об архитектуре данных**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_architecture_info), D3D11 возможности [**\_ \_ \_ d3d9 \_**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d9_options)возможности, [**D3D11 функции, \_ \_ \_ Поддержка функций шейдера данных \_ \_ \_**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_shader_min_precision_support)о функциях, минимальная точность и [**D3D11 \_ компонентов \_ \_ \_ \_**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d9_shadow_support) d3d9
-   [**ID3D11Device:: чеккформатсуппорт**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkformatsupport) с [**\_ форматом D3D11, \_ \_ \_ выходными данными декодера support**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support), поддержка [**формата D3D11, \_ \_ \_ \_ \_ выходные данные видеопроцессора**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support), [**\_ \_ Поддержка формата \_ видео \_ \_ входные видеопроцессоры**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support), [**\_ кодировщик D3D11 Format \_ Поддержка \_ видео \_ ENCODER**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support)и [**D3D11 \_ Format \_ D3D11 \_ выходные данные \_ \_ \_ логики слияния**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support2) .

## <a name="use-hlsl-minimum-precision"></a>Использовать минимальную точность HLSL

Начиная с Windows 8, графические драйверы могут реализовывать [скалярные типы данных](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-scalar) с минимальной точностью HLSL, используя любую точность, большую или равную указанной точности. Если на оборудовании, реализующем минимальную точность HLSL, используется код шейдера минимальной точности, используется меньше пропускной способности памяти, и в результате уменьшается энергопотребление системы.

Вы можете запросить поддержку минимальной точности, предоставляемую графическим драйвером, вызвав [**ID3D11Device:: чеккфеатуресуппорт**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) с параметром [**\_ \_ \_ \_ \_ поддержки минимальной точности для шейдера функций D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature) . В этом вызове **ID3D11Device:: чеккфеатуресуппорт** передайте указатель на структуру [**\_ \_ \_ \_ \_ \_ поддержки min Precision шейдера данных функции D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_shader_min_precision_support) , **ID3D11Device:: чеккфеатуресуппорт** заполняется минимальными уровнями точности, поддерживаемыми драйвером для этапа шейдера пикселей и для других стадий шейдера. Возвращенные сведения просто указывают, что графическое оборудование может выполнять операции HLSL с более низкой точностью, чем стандартная 32-разрядная точность чисел с плавающей запятой, но не гарантирует, что графическое оборудование будет работать с низкой точностью.

Вам не нужно создавать несколько шейдеров, которые выполняют и не используют минимальную точность. Вместо этого создайте шейдер с минимальной точностью, и переменные точности с точностью работают при полной 32-разрядной точности, если графический драйвер сообщает о том, что он не поддерживает какую-либо минимальную точность. Дополнительные сведения о минимальной точности HLSL см. [в разделе Использование HLSL минимальной точности](/windows/desktop/direct3dhlsl/using-hlsl-minimum-precision).

HLSLные шейдеры точности не работают в операционных системах, предшествующих Windows 8.

## <a name="specify-user-clip-planes-in-hlsl-on-feature-level-9-and-higher"></a>Указать пользовательские плоскости в HLSL на уровне компонентов 9 и выше

Начиная с Windows 8, атрибут функции **клиппланес** можно использовать в [ОБЪЯВЛЕНии функции](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-function-syntax) HLSL, а не в [SV \_ клипдистанце](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics) , чтобы сделать шейдер на [уровне функций](overviews-direct3d-11-devices-downlevel-intro.md) 9 x, а \_ также на уровне функций 10 и выше. Дополнительные сведения см. [в статье пользовательские ролики на устройствах на уровне компонентов 9](/windows/desktop/direct3dhlsl/user-clip-planes-on-10level9).

## <a name="create-larger-constant-buffers-than-a-shader-can-access"></a>Создавать большие буферы констант, чем шейдер может получить доступ

Direct3D 11,1 позволяет создавать буферы констант, размер которых превышает максимальный размер постоянного буфера, к которому может обращаться шейдер (4096 32-бит \* 4 — константы компонентов – 64 КБ). Позже, при привязке буферов к конвейеру, например с помощью [**пссетконстантбуфферс**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-pssetconstantbuffers) или [**PSSetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-pssetconstantbuffers1), можно указать диапазон буферов, к которым может получить доступ шейдер, который помещается в пределах 4096.

Direct3D 11,1 обновляет метод [**ID3D11Device:: CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) для этой функции.

## <a name="use-logical-operations-in-a-render-target"></a>Использование логических операций в целевом объекте прорисовки

Direct3D 11,1 позволяет использовать логические операции вместо смешения в целевом объекте прорисовки. Однако нельзя смешивать логические операции с переходом между несколькими целевыми объектами отрисовки.

Эта функция Direct3D 11,1 состоит из следующего API.

-   [**ID3D11Device1:: CreateBlendState1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11device1-createblendstate1) WITH [ **D3D11 \_ Logic \_ Op**](/windows/desktop/api/D3D11_1/ne-d3d11_1-d3d11_logic_op)

## <a name="force-the-sample-count-to-create-a-rasterizer-state"></a>Принудительное создание состояния средства программной прорисовки для счетчика выборки

Direct3D 11,1 позволяет указать счетчик принудительных выборок при создании состояния средства создания программной прорисовки.

Эта функция Direct3D 11,1 состоит из следующего API.

-   [**ID3D11Device1::CreateRasterizerState1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11device1-createrasterizerstate1)

> [!Note]  
>
> Если вы хотите подготовиться к просмотру с числом выборок, равным 1 или выше, необходимо следовать приведенным ниже рекомендациям.
>
> -   Не привязывать представления элементов глубины.
> -   Отключите тестирование глубины.
> -   Убедитесь, что шейдер не имеет глубины вывода.
> -   При наличии привязанных представлений для подготовки к просмотру [**( \_ \_ \_ целевой объект рендеринга D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag)) и принудительном количестве выборки больше 1, убедитесь, что у каждого целевого объекта отрисовки есть только один пример.
> -   Не следует использовать шейдер с частотой выборки. Таким образом, [**ID3D11ShaderReflection:: иссамплефрекуенцишадер**](/windows/desktop/api/D3D11Shader/nf-d3d11shader-id3d11shaderreflection-issamplefrequencyshader) возвращает **значение false**.
>
> В противном случае режим отрисовки не определен. Дополнительные сведения о настройке элементов глубины см. в разделе [Настройка функций Depth-Stencil](d3d10-graphics-programming-guide-depth-stencil.md).

 

## <a name="process-video-resources-with-shaders"></a>Обработка видеоресурсов с помощью шейдеров

Direct3D 11,1 позволяет создавать представления (SRV/РТВ/UAV) для видеоресурсов, чтобы шейдеры Direct3D могли обрабатывать эти видеоматериалы. Формат базового видеоресурса позволяет ограничивать форматы, которые может использовать представление. Перечисление [**\_ форматов DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) содержит новые значения формата ресурсов видео. Эти **значения \_ формата DXGI** указывают допустимые форматы представления, которые можно создать, а также то, как среда выполнения Direct3D 11,1 сопоставляет представление. Можно создать несколько представлений различных частей одной и той же поверхности, и в зависимости от формата размеры представлений могут отличаться друг от друга.

В Direct3D 11,1 для этой функции обновляются следующие методы.

-   [**ID3D11Device:: Креатешадерресаурцевиев**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createshaderresourceview)
-   [**ID3D11Device:: Креатерендертаржетвиев**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createrendertargetview)
-   [**ID3D11Device:: Креатеунордередакцессвиев**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createunorderedaccessview)

## <a name="extended-support-for-shared-texture2d-resources"></a>Расширенная поддержка общих ресурсов Texture2D

Direct3D 11,1 гарантирует, что вы сможете совместно использовать ресурсы Texture2D, созданные с определенными типами ресурсов и форматами. Чтобы предоставить общий доступ к ресурсам Texture2D, используйте флаги совместного использования [**\_ \_ \_ общих**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)ресурсов, [**D3D11 \_ ресурса \_ \_ \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)D3D11 или сочетание общих **D3D11 \_ ресурсов \_ \_ \_** кэйедмутекс и [**D3D11 \_ ресурсов \_ \_ \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) общего нсандле (New для Windows 8) при создании этих ресурсов.

Direct3D 11,1 гарантирует, что вы можете предоставить общий доступ к Texture2D ресурсам, созданным с помощью этих значений [**\_ формата DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) :

-   \_Формат DXGI \_ R8G8B8A8 \_ UNORM
-   \_Формат DXGI \_ R8G8B8A8 \_ UNORM \_ sRGB
-   \_Формат DXGI \_ B8G8R8A8 \_ UNORM
-   \_Формат DXGI \_ B8G8R8A8 \_ UNORM \_ sRGB
-   \_Формат DXGI \_ B8G8R8X8 \_ UNORM
-   \_Формат DXGI \_ B8G8R8X8 \_ UNORM \_ sRGB
-   \_Формат DXGI \_ R10G10B10A2 \_ UNORM
-   \_Формат DXGI \_ R16G16B16A16 \_ float

Кроме того, Direct3D 11,1 гарантирует, что вы можете предоставить общий доступ к Texture2D ресурсам, созданным с mipmap уровнем 1, размером массива 1, флагами [**привязки \_ \_ \_ ресурса шейдера привязки D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag) и [**D3D11 \_ привязки \_ \_ целевого объекта визуализации**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag) , по умолчанию используется значение Default ([**\_ Использование D3D11 \_ по умолчанию**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)) и только следующие значения [**\_ \_ \_ флага ресурсов D3D11 ресурса**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) :

-   [**\_Общие ресурсы \_ D3D11 \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)
-   [**\_ \_ \_ Общие \_ кэйедмутекс ресурсов D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)
-   [**\_ \_ \_ Общие \_ нсандле ресурсов D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)
-   [**\_ \_ \_ Совместимый с GDI \_ ресурс D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)

Direct3D 11,1 позволяет использовать более разнообразные типы ресурсов и форматы Texture2D. Вы можете запросить, поддерживает ли драйвер графики и оборудование расширенный общий доступ к ресурсам Texture2D, вызвав [**ID3D11Device:: чеккфеатуресуппорт**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) с параметром [**D3D11 \_ Feature \_ D3D11 \_ Options**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature) . В этом вызове **ID3D11Device:: чеккфеатуресуппорт** передайте указатель на структуру [**\_ \_ \_ \_ параметров D3D11 данных функции D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options) . **ID3D11Device:: чеккфеатуресуппорт** задает **значение true** для элемента **екстендедресаурцешаринг** в **\_ \_ \_ \_ параметре D3D11 Data D3D11** , если оборудование и драйвер поддерживают расширенное совместное использование ресурсов Texture2D.

Если [**ID3D11Device:: чеккфеатуресуппорт**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) возвращает **true** в **екстендедресаурцешаринг**, вы можете предоставить общий доступ к созданным ресурсам со следующими значениями [**\_ формата DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) :

-   \_Формат DXGI \_ R32G32B32A32 \_ тип
-   \_Формат DXGI \_ R32G32B32A32 \_ float
-   \_Формат DXGI \_ R32G32B32A32 \_ uint
-   \_Формат DXGI \_ R32G32B32A32 \_ Синт
-   \_Формат DXGI \_ R16G16B16A16 \_ тип
-   \_Формат DXGI \_ R16G16B16A16 \_ float
-   \_Формат DXGI \_ R16G16B16A16 \_ UNORM
-   \_Формат DXGI \_ R16G16B16A16 \_ uint
-   \_Формат DXGI \_ R16G16B16A16 \_ снорм
-   \_Формат DXGI \_ R16G16B16A16 \_ Синт
-   \_Формат DXGI \_ R10G10B10A2 \_ UNORM
-   \_Формат DXGI \_ R10G10B10A2 \_ uint
-   \_Формат DXGI \_ R8G8B8A8 \_ тип
-   \_Формат DXGI \_ R8G8B8A8 \_ UNORM
-   \_Формат DXGI \_ R8G8B8A8 \_ UNORM \_ sRGB
-   \_Формат DXGI \_ R8G8B8A8 \_ uint
-   \_Формат DXGI \_ R8G8B8A8 \_ снорм
-   \_Формат DXGI \_ R8G8B8A8 \_ Синт
-   \_Формат DXGI \_ B8G8R8A8 \_ тип
-   \_Формат DXGI \_ B8G8R8A8 \_ UNORM
-   \_Формат DXGI \_ B8G8R8X8 \_ UNORM
-   \_Формат DXGI \_ B8G8R8A8 \_ UNORM \_ sRGB
-   \_Формат DXGI \_ B8G8R8X8 \_ тип
-   \_Формат DXGI \_ B8G8R8X8 \_ UNORM \_ sRGB
-   \_Формат DXGI \_ R32 \_ тип
-   \_Формат DXGI \_ R32 \_ float
-   \_Формат DXGI \_ R32 \_ uint
-   \_Формат DXGI \_ R32 \_ Синт
-   \_Формат DXGI \_ R16 \_ тип
-   \_Формат DXGI \_ R16 \_ float
-   \_Формат DXGI \_ R16 \_ UNORM
-   \_Формат DXGI \_ R16 \_ uint
-   \_Формат DXGI \_ R16 \_ снорм
-   \_Формат DXGI \_ R16 \_ Синт
-   \_Формат DXGI \_ R8 \_ тип
-   \_Формат DXGI \_ R8 \_ UNORM
-   \_Формат DXGI \_ R8 \_ uint
-   \_Формат DXGI \_ R8 \_ снорм
-   \_Формат DXGI \_ R8 \_ Синт
-   \_Формат DXGI \_ a8 \_ UNORM
-   \_айув формата \_ DXGI
-   \_YUY2 формата \_ DXGI
-   \_NV12 формата \_ DXGI
-   \_NV11 формата \_ DXGI
-   \_P016 формата \_ DXGI
-   \_P010 формата \_ DXGI
-   \_Y216 формата \_ DXGI
-   \_Y210 формата \_ DXGI
-   \_Y416 формата \_ DXGI
-   \_Y410 формата \_ DXGI

Если [**ID3D11Device:: чеккфеатуресуппорт**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) возвращает **true** в **екстендедресаурцешаринг**, вы можете предоставить общий доступ к созданным ресурсам с помощью этих функций и флагов:

-   [**\_Использование D3D11 \_ по умолчанию**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)
-   [**\_ \_ Ресурс шейдера привязки \_ D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag)
-   [**\_ \_ Целевой объект прорисовки привязки D3D11 \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag)
-   [**D3D11 \_ ресурсов \_ , \_ Создание \_ MIPS**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)
-   [**D3D11 \_ привязать \_ неупорядоченный \_ доступ**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag)
-   Уровни mipmap (один или несколько уровней) в ресурсах двухмерной текстуры (указанные в элементе **Миплевелс** [**D3D11 \_ TEXTURE2D \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture2d_desc))
-   Массивы ресурсов двумерных текстур (одна или несколько текстур) (заданные в элементе **размера массива** элемента [**D3D11 \_ TEXTURE2D \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture2d_desc))
-   [**\_Декодер привязки \_ D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag)
-   [**D3D11 \_ ресурс \_ с \_ ограниченным \_ содержимым**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)
-   [**D3D11 \_ ресурс " \_ Разное \_ ограничение \_ общего \_ ресурса"**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)
-   [**\_ \_ \_ \_ \_ Драйвер общего ресурса с ограничением \_ ресурсов D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)

> [!Note]  
> Если **екстендедресаурцешаринг** имеет **значение true**, вы получаете большую гибкость при указании флагов привязки для совместного использования ресурсов Texture2D. Графический драйвер и оборудование поддерживают не только дополнительные флаги привязки, но и более возможности сочетания флагов привязки. Например, можно указать только [**\_ \_ \_ целевой объект рендеринга D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag) или без флагов привязки и т. д.

 

Даже если [**ID3D11Device:: чеккфеатуресуппорт**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) возвращает **true** в **екстендедресаурцешаринг**, вы по-прежнему не можете предоставлять общий доступ к ресурсам, созданным с помощью этих функций и флагов:

-   [**\_ \_ Набор элементов глубины привязки D3D11 \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag)
-   ресурсы двухмерной текстуры в режиме многовыборочного сглаживания (MSAA) (задается [**с \_ примером \_ DESC**](/windows/desktop/api/dxgicommon/ns-dxgicommon-dxgi_sample_desc))
-   [**D3D11 ресурс с \_ \_ прочим \_ ресурсом \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)
-   [**D3D11 \_ \_НЕизменяемое использование**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage), [**\_ \_ Динамическое использование D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)или [**D3D11 \_ использование \_ промежуточного хранения**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage) (т. е. сопоставляемые)
-   [**\_Текстурекубе ресурсов \_ D3D11 \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)

## <a name="change-subresources-with-new-copy-options"></a>Изменение подресурсов с помощью новых параметров копирования

Direct3D 11,1 позволяет использовать новые флаги копирования для копирования и обновления подресурсов. При копировании подресурса исходный и конечный ресурсы могут быть идентичными, а исходный и целевой регионы могут перекрываться.

Эта функция Direct3D 11,1 состоит из следующего API.

-   [**ID3D11DeviceContext1::CopySubresourceRegion1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-copysubresourceregion1)
-   [**ID3D11DeviceContext1::UpdateSubresource1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-updatesubresource1)

## <a name="discard-resources-and-resource-views"></a>Удалить ресурсы и представления ресурсов

Direct3D 11,1 позволяет удалять ресурсы и представления ресурсов из контекста устройства. Эта новая функция информирует GPU о том, что существующее содержимое в ресурсах или представлениях ресурсов больше не требуется.

Эта функция Direct3D 11,1 состоит из следующего API.

-   [**ID3D11DeviceContext1::D Искардресаурце**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardresource)
-   [**ID3D11DeviceContext1::D Искардвиев**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardview)
-   [**ID3D11DeviceContext1::D iscardView1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardview1)

## <a name="support-a-larger-number-of-uavs"></a>Поддержка большего числа Уавс

Direct3D 11,1 позволяет использовать большее количество Уавс при привязке ресурсов к [этапу слияния вывода](d3d10-graphics-programming-guide-output-merger-stage.md) , а также при задании массива представлений для неупорядоченного ресурса.

В Direct3D 11,1 для этой функции обновляются следующие методы.

-   [**Ссылку ID3D11DeviceContext:: Омсетрендертаржетсандунордередакцессвиевс**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetrendertargetsandunorderedaccessviews)
-   [**Ссылку ID3D11DeviceContext:: Кссетунордередакцессвиевс**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-cssetunorderedaccessviews)

## <a name="bind-a-subrange-of-a-constant-buffer-to-a-shader"></a>Привязка поддиапазона буфера константы к шейдеру

Direct3D 11,1 позволяет привязать поддиапазон буфера константы для доступа к шейдеру. Можно указать больший буфер константы и указать поддиапазон, который может использовать шейдер.

Эта функция Direct3D 11,1 состоит из следующего API.

-   [**ID3D11DeviceContext1::CSSetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-cssetconstantbuffers1)
-   [**ID3D11DeviceContext1::D SSetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-dssetconstantbuffers1)
-   [**ID3D11DeviceContext1::GSSetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-gssetconstantbuffers1)
-   [**ID3D11DeviceContext1::HSSetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-hssetconstantbuffers1)
-   [**ID3D11DeviceContext1::P SSetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-pssetconstantbuffers1)
-   [**ID3D11DeviceContext1::VSSetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-vssetconstantbuffers1)

## <a name="retrieve-the-subrange-of-a-constant-buffer-that-is-bound-to-a-shader"></a>Получение поддиапазона буфера констант, привязанного к шейдеру

Direct3D 11,1 позволяет получить поддиапазон буфера констант, привязанного к шейдеру.

Эта функция Direct3D 11,1 состоит из следующего API.

-   [**ID3D11DeviceContext1::CSGetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-csgetconstantbuffers1)
-   [**ID3D11DeviceContext1::D SGetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-dsgetconstantbuffers1)
-   [**ID3D11DeviceContext1::GSGetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-gsgetconstantbuffers1)
-   [**ID3D11DeviceContext1::HSGetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-hsgetconstantbuffers1)
-   [**ID3D11DeviceContext1::P SGetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-psgetconstantbuffers1)
-   [**ID3D11DeviceContext1::VSGetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-vsgetconstantbuffers1)

## <a name="clear-all-or-part-of-a-resource-view"></a>Очистка представления ресурсов или его части

Direct3D 11,1 позволяет очистить представление ресурсов (РТВ, UAV или любое видео-представление Texture2D Surface). Одно и то же значение цвета применяется ко всем частям представления.

Эта функция Direct3D 11,1 состоит из следующего API.

-   [**ID3D11DeviceContext1:: Клеарвиев**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-clearview)

## <a name="map-srvs-of-dynamic-buffers-with-no_overwrite"></a>Сопоставьте СРВС динамических буферов без \_ ПЕРЕзаписи

Direct3D 11,1 позволяет сопоставлять представления ресурсов шейдера (SRV) динамических буферов с D3D11 \_ Map \_ \_ без \_ перезаписи. Среда выполнения Direct3D 11 и более ранних версий ограничивает сопоставление с буферами вершин или индексов.

Direct3D 11,1 обновляет метод [**ссылку ID3D11DeviceContext:: Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) для этой функции.

## <a name="use-uavs-at-every-pipeline-stage"></a>Использование Уавс на каждом этапе конвейера

Direct3D 11,1 позволяет использовать следующие инструкции в модели шейдера 5,0 на всех стадиях шейдера, которые ранее использовались только в шейдерах пикселей и шейдере вычислений.

-   [дкл \_ UAV \_ типизированный](/windows/desktop/direct3dhlsl/dcl-uav-typed--sm5---asm-)
-   [дкл \_ UAV \_ RAW](/windows/desktop/direct3dhlsl/dcl-uav-raw--sm5---asm-)
-   [дкл \_ UAV \_ Structured](/windows/desktop/direct3dhlsl/dcl-uav-structured--sm5---asm-)
-   [LD \_ необработанных](/windows/desktop/direct3dhlsl/ld-raw--sm5---asm-)
-   [\_Структура LD](/windows/desktop/direct3dhlsl/ld-structured--sm5---asm-)
-   [\_UAV, \_ тип LD](/windows/desktop/direct3dhlsl/ld-uav-typed--sm5---asm-)
-   [хранить \_ необработанные](/windows/desktop/direct3dhlsl/store-raw--sm5---asm-)
-   [\_структурированное хранилище](/windows/desktop/direct3dhlsl/store-structured--sm5---asm-)
-   [Сохранить \_ UAV \_](/windows/desktop/direct3dhlsl/store-uav-typed--sm5---asm-)
-   [\_углобал синхронизации](/windows/desktop/direct3dhlsl/sync--sm5---asm-)
-   Все атомарные и непосредственные атомарные (например [, \_ атомарные](/windows/desktop/direct3dhlsl/atomic-and--sm5---asm-) и [IMM \_ Atomic \_ и](/windows/desktop/direct3dhlsl/imm-atomic-and--sm5---asm-))

В Direct3D 11,1 для этой функции обновляются следующие методы.

-   [**Ссылку ID3D11DeviceContext:: Креатедомаиншадер**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdomainshader)
-   [**Ссылку ID3D11DeviceContext:: Креатежеометришадер**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshader)
-   [**Ссылку ID3D11DeviceContext:: Креатежеометришадервисстреамаутпут**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput)
-   [**Ссылку ID3D11DeviceContext:: Креатехуллшадер**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createhullshader)
-   [**Ссылку ID3D11DeviceContext:: Креатевертексшадер**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createvertexshader)

Эти инструкции существовали в Direct3D 11,0 в PS \_ 5 \_ 0 и CS \_ 5 \_ 0. Поскольку Direct3D 11,1 делает Уавс доступным на всех стадиях шейдера, эти инструкции доступны на всех стадиях шейдера.

При передаче скомпилированных шейдеров (VS/HS/DS/HS), которые используют любую из этих инструкций, в функцию создания шейдера, например [**креатевертексшадер**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createvertexshader), на устройствах, которые не поддерживают уавс на каждом этапе (включая существующие драйверы, не реализованные с помощью этой функции), функция Create-Shader завершается ошибкой. Функция Create-Shader также завершается ошибкой, если шейдер пытается использовать слот UAV за пределами набора слотов UAV, поддерживаемых оборудованием.

Уавс, на которые ссылаются эти инструкции, являются общими для всех стадий конвейера. Например, UAV, привязанный к слоту 0 на [этапе Output-слияния](d3d10-graphics-programming-guide-output-merger-stage.md) , доступен в слоте 0 в VS/HS/DS/GS/PS.

UAV обращается к этапам шейдера, выполняемым внутри или за пределами построителя текстуры, которые выполняются в заданной отрисовке \* () или что выдается из шейдера вычислений в диспетчеризации \* (), не гарантируется завершение в порядке их возникновения. Но все доступ к UAV завершается в конце рисования \* () или диспетчеризации \* ().

## <a name="extended-support-for-warp-devices"></a>Расширенная поддержка деформации устройств

Direct3D 11,1 расширяет поддержку [деформации](overviews-direct3d-11-devices-create-warp.md) устройств, которые создаются путем передачи [**\_ \_ \_ искривленного типа драйвера D3D**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type) в параметре *дривертипе* [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice).

Начиная с Direct3D 11,1, поддержка ИСКРИВЛЕНия устройств:

-   Все [уровни функций](overviews-direct3d-11-devices-downlevel-intro.md) Direct3D от 9,1 до 11,1
-   [Вычисление шейдеров](direct3d-11-advanced-stages-compute-shader.md) и [тесселяция](direct3d-11-advanced-stages-tessellation.md)
-   Общие поверхности. То есть вы можете полностью совместно использовать поверхности между устройством деформации, а также между устройством деформации в разных процессах.

Устройства деформации не поддерживают следующие дополнительные функции:

-   [удваивает](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_doubles)
-   [кодирование видео или декодирование](/windows/desktop/api/D3D11/ne-d3d11-d3d11_create_device_flag)
-   [Поддержка шейдера минимальной точности](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_shader_min_precision_support)

При запуске виртуальной машины, Hyper-V с отключенным графическим процессором или без драйвера монитора вы получаете устройство деформации, понятное имя которого — "базовый видеоадаптер Майкрософт". Это устройство деформации может выполнять все функции Windows, в том числе DWM, Internet Explorer и приложения Магазина Windows. Это устройство деформации также поддерживает запуск устаревших приложений, использующих [DirectDraw](/windows/desktop/directdraw/directdraw) или работающих приложений, использующих Direct3D 3 через Direct3D 11,1.

## <a name="use-direct3d-in-session-0-processes"></a>Использование Direct3D в процессах сеанса 0

Начиная с Windows 8 и Windows Server 2012, большинство интерфейсов API Direct3D можно использовать в процессах сеанса 0.

> [!Note]  
> Эти выходные данные, окна, цепочки буферов и API-интерфейсы, связанные с презентацией, недоступны в процессах сеанса 0, так как они не применяются к среде сеанса 0:
>
> -   [**Идксгифактори:: Креатесвапчаин**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-createswapchain)
> -   [**Идксгифактори:: ЖетвиндовассоЦиатион**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-getwindowassociation)
> -   [**Идксгифактори:: МакевиндовассоЦиатион**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-makewindowassociation)
> -   [**Идксгиадаптер:: Енумаутпутс**](/windows/desktop/api/dxgi/nf-dxgi-idxgiadapter-enumoutputs)
> -   [**ID3D11Debug:: Сетфеатуремаск**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11debug-setfeaturemask)
> -   [**ID3D11Debug:: Сетпресентперрендеропделай**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11debug-setpresentperrenderopdelay)
> -   [**ID3D11Debug:: Сетсвапчаин**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11debug-setswapchain)
> -   [**ID3D10Debug:: Сетфеатуремаск**](/windows/desktop/api/d3d10sdklayers/nf-d3d10sdklayers-id3d10debug-setfeaturemask)
> -   [**ID3D10Debug:: Сетпресентперрендеропделай**](/windows/desktop/api/d3d10sdklayers/nf-d3d10sdklayers-id3d10debug-setpresentperrenderopdelay)
> -   [**ID3D10Debug:: Сетсвапчаин**](/windows/desktop/api/d3d10sdklayers/nf-d3d10sdklayers-id3d10debug-setswapchain)
> -   [**D3D10CreateDeviceAndSwapChain**](/windows/desktop/api/d3d10misc/nf-d3d10misc-d3d10createdeviceandswapchain)
> -   [**D3D10CreateDeviceAndSwapChain1**](/windows/desktop/api/d3d10_1/nf-d3d10_1-d3d10createdeviceandswapchain1)
> -   [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain)
>
> Если вы вызываете один из предыдущих API в процессе сеанса 0, он возвращает [**ошибку DXGI \_ , \_ \_ которая в настоящее время \_ недоступна**](/windows/desktop/direct3ddxgi/dxgi-error).

 

## <a name="support-for-shadow-buffer-on-feature-level-9"></a>Поддержка теневого буфера на уровне функций 9

Используйте подмножество \_ функций теневого буфера Direct3D 10 0, чтобы реализовать эффекты тени на [уровне функций](overviews-direct3d-11-devices-downlevel-intro.md) 9 \_ x. Сведения о том, что необходимо сделать для реализации эффектов тени на уровне функций 9 \_ x, см. в разделе [Реализация теневых буферов для уровня функций Direct3D 9](/previous-versions/windows/apps/jj262110(v=win.10)).

## <a name="related-topics"></a>См. также

<dl> <dt>

[Новые возможности Direct3D 11](dx-graphics-overviews-introduction.md)
</dt> </dl>

 

 