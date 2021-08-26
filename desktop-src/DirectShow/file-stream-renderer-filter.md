---
description: Фильтр модуля подготовки к потоку файлов
ms.assetid: e26462bb-e67f-4522-bec2-88378c4ff442
title: Фильтр модуля подготовки к потоку файлов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3da8651d61559a9b22b722f91563426cb067f7a3
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122470569"
---
# <a name="file-stream-renderer-filter"></a>Фильтр модуля подготовки к потоку файлов

Фильтр модуля подготовки отчетов File Stream подготавливает к просмотру имена файлов, которые анализируются фильтром [синтаксического анализатора с несколькими файлами](multi-file-parser-filter.md) . Дополнительные сведения см. в документации по этому фильтру.

Использование этого фильтра является устаревшим. Для отрисовки нескольких файлов в одном графе фильтра приложение должно просто вызвать **RenderFile** или **аддсаурцефилтер** несколько раз.




| | | Интерфейсы фильтра | <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>Ибасефилтер</strong></a> | | Типы входных закрепления <ul><li>Основной тип: MEDIATYPE_File</li><li>Подтип: GUID_NULL</li><li>Тип формата: MEDIATYPE_File</li></ul> | | Интерфейсы входных закрепления | <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ипин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>икуалитиконтрол</strong></a> | | Типы выходных закрепления Нет | | Интерфейсы выходного ПИН-кода | <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ипин</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>икуалитиконтрол</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-istreambuilder"><strong>истреамбуилдер</strong></a> | | Фильтровать CLSID | CLSID_FileRend | | Исполняемый файл | Quartz.dll | | <a href="merit.md"></a> Кому | MERIT_UNLIKELY | | <a href="filter-categories.md">Категория фильтра</a> | CLSID_LegacyAmFilterCategory | 




 

## <a name="remarks"></a>Комментарии

CLSID фильтра не определен в UUIDs. h. Используйте этот макрос в своем собственном файле заголовка:


```C++
// {D51BD5A5-7548-11cf-A520-0080C77EF58A}
DEFINE_GUID(CLSID_FileRend,
0xd51bd5A5, 0x7548, 0x11cf, 0xa5, 0x20, 0x0, 0x80, 0xc7, 0x7e, 0xf5, 0x8a);
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[DirectShow Фильтрующ](directshow-filters.md)
</dt> </dl>

 

 



