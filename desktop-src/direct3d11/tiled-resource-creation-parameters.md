---
title: Параметры создания мозаичных ресурсов
description: Существуют некоторые ограничения на тип ресурсов Direct3D, которые можно создать с помощью \_ флага D3D11 ресурса " \_ Разное" \_ . В этом разделе приводятся допустимые параметры для создания мозаичных ресурсов.
ms.assetid: 19A0EA7F-888D-4102-A5D2-F3B54775EDE8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9668c21060cbb8f39884204780ce689b3e67196aef0bdcfef891836768f04af
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119279844"
---
# <a name="tiled-resource-creation-parameters"></a>Параметры создания мозаичных ресурсов

Существуют некоторые ограничения на тип ресурсов Direct3D, которые можно создать с помощью флага [**D3D11 \_ ресурса " \_ Разное \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) ". В этом разделе приводятся допустимые параметры для создания мозаичных ресурсов.

<dl> <dt>

<span id="Supported_Resource_Type"></span><span id="supported_resource_type"></span><span id="SUPPORTED_RESOURCE_TYPE"></span>**Поддерживаемый тип ресурсов**
</dt> <dd>

\[Массив Texture2D \] (включая \[ массив текстурекубе \] , который является вариантом массива Texture2D \[ \] ) или buffer.

**Не поддерживается:** Texture1D \[ array \] или Texture3D, но в будущем может поддерживаться Texture3D.

</dd> <dt>

<span id="Supported_Resource_Usage"></span><span id="supported_resource_usage"></span><span id="SUPPORTED_RESOURCE_USAGE"></span>**Поддерживаемое использование ресурсов**
</dt> <dd>

\_Использование D3D11 \_ по умолчанию.

**Не поддерживается:** \_ \_ Динамическое использование D3D11, D3D11 \_ использование \_ промежуточного хранения или D3D11 \_ использование \_ неизменным.

</dd> <dt>

<span id="Supported_Resource_Misc_Flags"></span><span id="supported_resource_misc_flags"></span><span id="SUPPORTED_RESOURCE_MISC_FLAGS"></span>**Поддерживаемые флаги для ресурсов**
</dt> <dd>

D3D11 \_ ресурсов \_ \_ (по определению), \_ Прочие \_ текстурекубе, \_ дравиндирект \_ args, \_ buffer \_ Разрешить \_ необработанные \_ представления \_ , \_ структурированный буфер, \_ \_ срез ресурсов или \_ Создание \_ MIPS.

**Не поддерживается:** \_ Общий, \_ Общий \_ кэйедмутекс, \_ \_ совместимый с GDI, \_ Общий \_ нсандле, \_ ограниченный \_ контент, \_ ограничение \_ общего \_ ресурса, \_ ограничение общего \_ \_ \_ драйвера ресурса, \_ защищенного или \_ пула плиток \_ .

</dd> <dt>

<span id="Supported_Bind_Flags"></span><span id="supported_bind_flags"></span><span id="SUPPORTED_BIND_FLAGS"></span>**Поддерживаемые флаги привязки**
</dt> <dd>

D3D11 \_ Привязка \_ ресурса шейдера \_ , \_ \_ целевой объект прорисовки, \_ \_ трафарет глубины или \_ неупорядоченный \_ доступ.

**Не поддерживается:** \_ Буфер КОНСТАНТы. \_ \_ \_ \[ Обратите внимание, что привязка мозаичного буфера как SRV/UAV/РТВ по-прежнему продолжается \] , \_ \_ буфер индекса, \_ потоковый \_ выход, \_ \_ декодер привязки или \_ \_ \_ видеокодировщик.

</dd> <dt>

<span id="Supported_Formats"></span><span id="supported_formats"></span><span id="SUPPORTED_FORMATS"></span>**Поддерживаемые форматы**
</dt> <dd>

Все форматы, которые будут доступны для определенной конфигурации независимо от разбиения на плитки с некоторыми исключениями.

</dd> <dt>

<span id="Supported_SampleDesc__Multisample_count__quality_"></span><span id="supported_sampledesc__multisample_count__quality_"></span><span id="SUPPORTED_SAMPLEDESC__MULTISAMPLE_COUNT__QUALITY_"></span>**Поддерживаемые Сампледеск (число многовыборок, качество)**
</dt> <dd>

То, что будет поддерживаться для определенной конфигурации независимо от разбиения на плитки с некоторыми исключениями.

</dd> <dt>

<span id="Supported_Width_Height_MipLevels_ArraySize"></span><span id="supported_width_height_miplevels_arraysize"></span><span id="SUPPORTED_WIDTH_HEIGHT_MIPLEVELS_ARRAYSIZE"></span>**Поддерживаемые значения width/height/Миплевелс/размера массива**
</dt> <dd>

Все экстенты, поддерживаемые Direct3D 11. Ресурсы мозаичного заполнения не имеют ограничений на общий объем памяти, накладываемый на ресурсы без мозаичного заполнения. Ресурсы мозаичного заполнения ограничиваются только общими ограничениями виртуального адресного пространства. Сведения см. в разделе [адресное пространство, доступное для мозаичного заполнения ресурсов](address-space-available-for-tiled-resources.md).

</dd> </dl>

Начальное содержимое пула памяти плиток не определено.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Создание мозаичных ресурсов](creating-tiled-resources.md)
</dt> </dl>

 

 




