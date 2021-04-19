---
title: Определение корневых подписей в HLSL
description: Указание корневых подписей в модели шейдера HLSL 5,1 является альтернативой указанию их в коде C++.
ms.assetid: 399F5E91-B017-4F5E-9037-DC055407D96F
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dad0da9f84d68fc1acbf53332d1cae4075f0faa
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/14/2021
ms.locfileid: "107492286"
---
# <a name="specifying-root-signatures-in-hlsl"></a>Определение корневых подписей в HLSL

Указание корневых подписей в модели шейдера HLSL 5,1 является альтернативой указанию их в коде C++.

-   [Пример корневой подписи HLSL](#an-example-hlsl-root-signature)
    -   [Корневая подпись версии 1,0](#root-signature-version-10)
    -   [Корневая подпись версии 1.1](#root-signature-version-11)
-   [рутфлагс](#rootflags)
-   [Корневые константы](#root-constants)
-   [Видимость](#visibility)
-   [CBV корневого уровня](#root-level-cbv)
-   [SRV на корневом уровне](#root-level-srv)
-   [UAV корневого уровня](#root-level-uav)
-   [Таблица дескрипторов](#descriptor-table)
-   [Статическая выборка](#static-sampler)
-   [Компиляция корневой подписи HLSL](#compiling-an-hlsl-root-signature)
-   [Управление корневыми сигнатурами с помощью компилятора FXC](#manipulating-root-signatures-with-the-fxc-compiler)
-   [Примечания](#notes)
-   [Связанные темы](#related-topics)

## <a name="an-example-hlsl-root-signature"></a>Пример корневой подписи HLSL

Корневая подпись может быть указана в HLSL в виде строки. Строка содержит коллекцию предложений с разделителями-запятыми, описывающих компоненты, составляющие корневую подпись. Корневая подпись должна быть идентичной в шейдере для любого объекта состояния конвейера (PSO). Пример:

### <a name="root-signature-version-10"></a>Корневая подпись версии 1,0

``` syntax
#define MyRS1 "RootFlags( ALLOW_INPUT_ASSEMBLER_INPUT_LAYOUT | " \
                         "DENY_VERTEX_SHADER_ROOT_ACCESS), " \
              "CBV(b0, space = 1), " \
              "SRV(t0), " \
              "UAV(u0, visibility = SHADER_VISIBILITY_GEOMETRY), " \
              "DescriptorTable( CBV(b0), " \
                               "UAV(u1, numDescriptors = 2), " \
                               "SRV(t1, numDescriptors = unbounded)), " \
              "DescriptorTable(Sampler(s0, numDescriptors = 2)), " \
              "RootConstants(num32BitConstants=1, b9), " \
              "DescriptorTable( UAV(u3), " \
                               "UAV(u4), " \
                               "UAV(u5, offset=1)), " \

              "StaticSampler(s2)," \
              "StaticSampler(s3, " \
                             "addressU = TEXTURE_ADDRESS_CLAMP, " \
                             "filter = FILTER_MIN_MAG_MIP_LINEAR )"
```

Это определение даст следующую корневую подпись, заметив следующее:

-   Использование параметров по умолчанию.
-   B0 и (B0, Space = 1) не конфликтуют
-   U0 виден только для шейдера Geometry
-   U4 и U5 имеют псевдонимы для одного и того же дескриптора в куче.

![Корневая подпись, заданная с помощью языка шейдера высокого уровня](images/hlsl-root-signature.png)

### <a name="root-signature-version-11"></a>Корневая подпись версии 1.1

[Корневая подпись версии 1,1](root-signature-version-1-1.md) включает оптимизацию драйверов для дескрипторов и данных корневой подписи.

``` syntax
#define MyRS1 "RootFlags( ALLOW_INPUT_ASSEMBLER_INPUT_LAYOUT | " \
                         "DENY_VERTEX_SHADER_ROOT_ACCESS), " \
              "CBV(b0, space = 1, flags = DATA_STATIC), " \
              "SRV(t0), " \
              "UAV(u0), " \
              "DescriptorTable( CBV(b1), " \
                               "SRV(t1, numDescriptors = 8, " \
                               "        flags = DESCRIPTORS_VOLATILE), " \
                               "UAV(u1, numDescriptors = unbounded, " \
                               "        flags = DESCRIPTORS_VOLATILE)), " \
              "DescriptorTable(Sampler(s0, space=1, numDescriptors = 4)), " \
              "RootConstants(num32BitConstants=3, b10), " \
              "StaticSampler(s1)," \
              "StaticSampler(s2, " \
                             "addressU = TEXTURE_ADDRESS_CLAMP, " \
                             "filter = FILTER_MIN_MAG_MIP_LINEAR )"
```

Язык подписи HLSL тесно соответствует API-интерфейсам корневой подписи C++ и имеет эквивалентную ковыразительные возможности. Корневая подпись указывается как последовательность предложений, разделенных запятыми. Порядок предложений важен, так как порядок анализа определяет расположение слота в корневой подписи. Каждое предложение принимает один или несколько именованных параметров. Однако порядок параметров не имеет значения.

## <a name="rootflags"></a>рутфлагс

Необязательное предложение *рутфлагс* принимает 0 (значение по умолчанию, указывающее на отсутствие флагов) или одно или несколько предопределенных значений корневых флагов, Соединенных с помощью \| оператора или. Допустимые значения корневого флага определяются [**D3D12 \_ \_ \_ флагами корневой подписи**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags).

Пример:

``` syntax
RootFlags(0) // default value – no flags
RootFlags(ALLOW_INPUT_ASSEMBLER_INPUT_LAYOUT)
RootFlags(ALLOW_INPUT_ASSEMBLER_INPUT_LAYOUT | DENY_VERTEX_SHADER_ROOT_ACCESS)
```

## <a name="root-constants"></a>Корневые константы

Предложение *рутконстантс* задает корневые константы в корневой подписи. Два обязательных параметра: *num32BitConstants* и *Брег* (регистр, соответствующий *басешадеррегистер* в API-интерфейсах C++) *кбуффер*. Параметры Space (*регистерспаце* в API-интерфейсах C++) и Visibility (*шадервисибилити* в c++) являются необязательными, а значения по умолчанию:

``` syntax
RootConstants(num32BitConstants=N, bReg [, space=0, 
              visibility=SHADER_VISIBILITY_ALL ])
```

Пример:

``` syntax
RootConstants(num32BitConstants=3, b3)
```

## <a name="visibility"></a>Видимость

Видимость — это необязательный параметр, который может иметь одно из [**значений \_ \_ видимости шейдера D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility).

Видимость ШЕЙДЕРа выполняет \_ \_ широковещательную рассылку всех корневых аргументов всем шейдерам. На оборудовании это не имеет затрат, но на другом оборудовании есть затраты на разветвление данных на все этапы шейдера. Установка одного из параметров, таких как \_ вершина видимости шейдера \_ , ограничивает корневой аргумент одним этапом шейдера.

Задание для корневых аргументов одного этапа шейдера позволяет использовать одно и то же имя привязки на разных стадиях. Например, привязка SRV к `t0,SHADER_VISIBILITY_VERTEX` и привязке SRV для будет `t0,SHADER_VISIBILITY_PIXEL` допустимой. Но если параметр видимости был `t0,SHADER_VISIBILITY_ALL` для одной из привязок, корневая подпись будет недействительной.

## <a name="root-level-cbv"></a>CBV корневого уровня

В `CBV` предложении (представление буфера констант) указывается запись в формате буфера констант на корневом уровне b-Register. Обратите внимание, что это скалярная запись; невозможно указать диапазон для корневого уровня.

``` syntax
CBV(bReg [, space=0, visibility=SHADER_VISIBILITY_ALL ])    //   Version 1.0
CBV(bReg [, space=0, visibility=SHADER_VISIBILITY_ALL,      // Version 1.1
            flags=DATA_STATIC_WHILE_SET_AT_EXECUTE ])
```

## <a name="root-level-srv"></a>SRV на корневом уровне

`SRV`Предложение (представление ресурсов шейдера) задает запись реестра SRV t-Register на корневом уровне. Обратите внимание, что это скалярная запись; невозможно указать диапазон для корневого уровня.

``` syntax
SRV(tReg [, space=0, visibility=SHADER_VISIBILITY_ALL ])    //   Version 1.0
SRV(tReg [, space=0, visibility=SHADER_VISIBILITY_ALL,      // Version 1.1
            flags=DATA_STATIC_WHILE_SET_AT_EXECUTE ])
```

## <a name="root-level-uav"></a>UAV корневого уровня

В `UAV` предложении (неупорядоченное представление доступа) указана запись reg UAV u-Register. Обратите внимание, что это скалярная запись; невозможно указать диапазон для корневого уровня.

``` syntax
UAV(uReg [, space=0, visibility=SHADER_VISIBILITY_ALL ])    //   Version 1.0
UAV(uReg [, space=0, visibility=SHADER_VISIBILITY_ALL,      // Version 1.1
            flags=DATA_VOLATILE ])
```

Пример:

``` syntax
UAV(u3)
```

## <a name="descriptor-table"></a>Таблица дескрипторов

`DescriptorTable`Предложение само по себе представляет собой список разделенных запятыми предложений табличных таблиц, а также необязательный параметр видимости. Предложения *дескриптортабле* включают CBV, SRV, UAV и образец. Обратите внимание, что их параметры отличаются от параметров в предложениях корневого уровня.

``` syntax
DescriptorTable( DTClause1, [ DTClause2, … DTClauseN,
                 visibility=SHADER_VISIBILITY_ALL ] )
```

Таблица дескрипторов `CBV` имеет следующий синтаксис:

``` syntax
CBV(bReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND ])   // Version 1.0
CBV(bReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND      // Version 1.1
          , flags=DATA_STATIC_WHILE_SET_AT_EXECUTE ])
```

Пример:

``` syntax
DescriptorTable(CBV(b0),SRV(t3, numDescriptors=unbounded))
```

Обязательный параметр *Брег* указывает начальный reg диапазона кбуффер. Параметр *нумдескрипторс* указывает число дескрипторов в смежном диапазоне кбуффер. значение по умолчанию — 1. Запись объявляет диапазон кбуффер ` [Reg, Reg + numDescriptors - 1]` , если *нумдескрипторс* является числом. Если *нумдескрипторс* имеет значение "unboundd", то диапазон равен, а это `[Reg, UINT_MAX]` означает, что приложение должно убедиться, что оно не ссылается на область вне границ. Поле *offset* представляет параметр *оффсетиндескрипторсфромтаблестарт* в API-интерфейсах C++, то есть смещение (в дескрипторах) от начала таблицы. Если для смещения задано значение \_ «Добавление смещения диапазона дескрипторов» \_ \_ (по умолчанию), это означает, что диапазон находится непосредственно после предыдущего диапазона. Однако при вводе отдельных смещений диапазоны могут пересекаться друг с другом, что позволяет использовать псевдонимы регистров.

Таблица дескрипторов `SRV` имеет следующий синтаксис:

``` syntax
SRV(tReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND ])    // Version 1.0
SRV(tReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND,      // Version 1.1
            flags=DATA_STATIC_WHILE_SET_AT_EXECUTE ])
```

Это похоже на запись таблицы дескрипторов `CBV` , за исключением того, что указанный диапазон предназначен для представлений ресурсов шейдера.

Таблица дескрипторов `UAV` имеет следующий синтаксис:

``` syntax
UAV(uReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND ])    // Version 1.0
UAV(uReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND,      // Version 1.1
            flags=DATA_VOLATILE ])
```

Это похоже на запись таблицы дескрипторов `CBV` , за исключением того, что указанный диапазон предназначен для неупорядоченных представлений доступа.

Таблица дескрипторов `Sampler` имеет следующий синтаксис:

``` syntax
Sampler(sReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND ])  // Version 1.0
Sampler(sReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND,    // Version 1.1
                flags=0 ])
```

Это похоже на запись таблицы дескрипторов `CBV` , за исключением того, что указанный диапазон предназначен для образцов шейдера. Обратите внимание, что пробы не могут смешиваться с другими типами дескрипторов в одной и той же таблице дескрипторов (так как они находятся в отдельной куче дескрипторов).

## <a name="static-sampler"></a>Статическая выборка

Статический образец представляет структуру [**D3D12 \_ статической \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) выборки. Обязательный параметр для *статиксамплер* — это скалярный образец s-Register reg. Другие параметры являются необязательными со значениями по умолчанию, показанными ниже. Большинство полей допускают набор предопределенных перечислений.

``` syntax
StaticSampler( sReg,
              [ filter = FILTER_ANISOTROPIC, 
                addressU = TEXTURE_ADDRESS_WRAP,
                addressV = TEXTURE_ADDRESS_WRAP,
                addressW = TEXTURE_ADDRESS_WRAP,
                mipLODBias = 0.f,
                maxAnisotropy = 16,
                comparisonFunc = COMPARISON_LESS_EQUAL,
                borderColor = STATIC_BORDER_COLOR_OPAQUE_WHITE,
                minLOD = 0.f,         
                maxLOD = 3.402823466e+38f,
                space = 0, 
                visibility = SHADER_VISIBILITY_ALL ])
```

Пример:

``` syntax
StaticSampler(s4, filter=FILTER_MIN_MAG_MIP_LINEAR)
```

Параметры параметров очень похожи на вызовы API C++, за исключением *borderColor*, который ограничен перечислением в HLSL.

Поле фильтра может быть одним из [**\_ фильтров D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter).

В качестве полей адреса можно использовать один из [**\_ \_ \_ режимов адресации текстуры D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode).

Функция сравнения может быть одним из [**сравнения D3D12 \_ \_ Func**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func).

Поле цвета границы может быть одним из [**D3D12 \_ статического \_ \_ цвета границы**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_static_border_color).

Видимость может быть одной из [**D3D12ных \_ шейдеров \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility).

## <a name="compiling-an-hlsl-root-signature"></a>Компиляция корневой подписи HLSL

Существует два механизма компиляции корневой подписи HLSL. Во-первых, можно присоединить строку корневой подписи к конкретному шейдеру с помощью атрибута *рутсигнатуре* (в следующем примере используется точка входа **MyRS1** ):

``` syntax
[RootSignature(MyRS1)]
float4 main(float4 coord : COORD) : SV_Target
{
…
}
```

Компилятор создаст и проверит корневой BLOB-объект подписи для шейдера и внедряет его вместе с кодом байта шейдера в большой двоичный объект шейдера. Компилятор поддерживает синтаксис корневой подписи для модели шейдеров 5,0 и более поздних версий. Если корневая подпись внедрена в шейдер модели шейдера 5,0 и что шейдер отправляется в среду выполнения D3D11, в отличие от D3D12, то часть подписи root будет автоматически пропущена D3D11.

Другой механизм — создать изолированный корневой BLOB-объект подписи, который может повторно использовать его с большим набором шейдеров, экономя пространство. [Средство компилятора Effect](/windows/desktop/direct3dtools/fxc) (FXC) поддерживает модели шейдеров **рутсиг \_ 1 \_ 0** и **рутсиг \_ 1 \_ 1** . Имя определения строки указывается с помощью обычного аргумента/E. Пример:

``` syntax
fxc.exe /T rootsig_1_1 MyRS1.hlsl /E MyRS1 /Fo MyRS1.fxo
```

Обратите внимание, что определение строки корневой подписи может также передаваться в командной строке, например/D MyRS1 = "...".

## <a name="manipulating-root-signatures-with-the-fxc-compiler"></a>Управление корневыми сигнатурами с помощью компилятора FXC

Компилятор FXC создает побайтовый код шейдера из исходных файлов HLSL. Существует множество необязательных параметров для этого компилятора, см. [средство компилятора Effect](/windows/desktop/direct3dtools/fxc).

В следующей таблице приведены некоторые примеры использования FXC для управления HLSL, созданными корневыми сигнатурами.



| График | Командная строка                                                                 | Описание                                                                                                                                                                                                                              |
|------|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1    | `fxc /T ps_5_1 shaderWithRootSig.hlsl /Fo rs1.fxo`                           | Компилирует шейдер для целевого объекта шейдера Pixel 5,1, источник шейдера находится в файле Шадервисрутсиг. HLSL, который включает в себя корневую подпись. Шейдер и корневая подпись компилируются как отдельные большие двоичные объекты в двоичном файле RS1. фксо.    |
| 2    | `fxc /dumpbin rs1.fxo /extractrootsignature /Fo rs1.rs.fxo`                  | Извлекает корневую подпись из файла, созданного в строке 1, поэтому файл RS1. RS. фксо содержит только корневую подпись.                                                                                                                      |
| 3    | `fxc /dumpbin rs1.fxo /Qstrip_rootsignature /Fo rs1.stripped.fxo`            | Удаляет корневую подпись из файла, созданного в строке 1, поэтому файл RS1.. фксо содержит шейдер без корневой подписи.                                                                                                       |
| 4    | `fxc /dumpbin rs1.stripped.fxo /setrootsignature rs1.rs.fxo /Fo rs1.new.fxo` | Объединяет шейдер и корневую подпись, которые находятся в отдельных файлах, в двоичный файл, содержащий оба больших двоичных объектов. В этом примере RS1. New. fx0 будет совпадать с RS1. fx0 в строке 1.                                                           |
| 5    | `fxc /T rootsig_1_0 rootSigAndMaybeShaderInHereToo.hlsl /E RS1 /Fo rs2.fxo`  | Создает автономный двоичный файл с корневой подписью из источника, который может содержать не только корневую подпись. Обратите внимание \_ на \_ целевой объект рутсиг 1 0, который RS1 является именем строки макроса корневой подписи ( \# определения) в файле HLSL. |



 

Функциональность, доступная через FXC, также доступна программно с помощью функции [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile) . Этот вызов компилирует шейдер с корневой подписью или автономной корневой подписью (с указанием \_ \_ целевого объекта рутсиг 1 0). [**D3DGetBlobPart**](/windows/desktop/direct3dhlsl/d3dgetblobpart) и [**D3DSetBlobPart**](/windows/desktop/direct3dhlsl/d3dsetblobpart) могут извлекать и подключать корневые подписи к существующему большому двоичному объекту.  \_ \_ Корневая подпись BLOB \_ -объекта D3D используется для указания типа корневой части двоичного объекта подписи. [**D3DStripShader**](/windows/desktop/direct3dhlsl/d3dstripshader) удаляет корневую подпись (с помощью \_ \_ флага подписи корневой папки D3DCOMPILER \_ ) из большого двоичного объекта.

## <a name="notes"></a>Примечания

> [!Note]  
> В то время как настоятельно рекомендуется автономная компиляция шейдеров, если шейдеры должны компилироваться во время выполнения, см. примечания для [**D3DCompile2**](/windows/desktop/direct3dhlsl/d3dcompile2).

 

> [!Note]  
> Для использования существующих ресурсов HLSL не требуется изменять их, чтобы обрабатывать корневые подписи.

 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Динамическое индексирование с помощью HLSL 5.1](dynamic-indexing-using-hlsl-5-1.md)
</dt> <dt>

[Функции HLSL Shader Model 5,1 для Direct3D 12](/windows/desktop/direct3dhlsl/hlsl-shader-model-5-1-features-for-direct3d-12)
</dt> <dt>

[Привязка ресурсов](resource-binding.md)
</dt> <dt>

[Привязка ресурсов в HLSL](resource-binding-in-hlsl.md)
</dt> <dt>

[Корневые подписи](root-signatures.md)
</dt> <dt>

[Модель шейдера 5,1](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> <dt>

[Контрольное значение трафарета в шейдере](shader-specified-stencil-reference-value.md)
</dt> <dt>

[Загружаются неупорядоченные представления доступа](typed-unordered-access-view-loads.md)
</dt> </dl>

 

 
