---
title: Изменение предустановок
description: Изменение предустановок
ms.assetid: f8a5565d-676b-4679-a4cb-4bd7551cf41c
keywords:
- визуализации, пример с свечением
- Пользовательские визуализации, пример свечения
- инструкции по программированию, визуализации
- Примеры, Визуализация свечения
- Пример визуализации с свечением
- визуализации, предустановки
- Пользовательские визуализации, предустановки
- предустановки в визуализациях, пример с свечением
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03828614093836c5f9a3b422167b62f11b8f2489eb30556d42a2d80495935ec5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119863914"
---
# <a name="changing-presets"></a>Изменение предустановок

Следующие предварительно заданные разделы кода были изменены, чтобы разрешить три предустановки:

## <a name="getpresettitle"></a>жетпресеттитле

Этот код был вставлен вместо созданного предустановленного кода:


```C++
    switch (nPreset)
    {
    case PRESET_RED:
        bstrTemp.LoadString(IDS_REDPRESETNAME); 
        break;

    case PRESET_GREEN:
        bstrTemp.LoadString(IDS_GREENPRESETNAME); 
        break;

    case PRESET_BLUE:
        bstrTemp.LoadString(IDS_BLUEPRESETNAME); 
        break;
    }

```



## <a name="enumerations"></a>Перечисления

Следующее перечисление в свечении. h было изменено для разрешения трех предустановок:


```C++
enum {
    PRESET_RED = 0,
    PRESET_GREEN,
    PRESET_BLUE,
    PRESET_COUNT
};

```



## <a name="resource-header"></a>Заголовок ресурса

Следующие ресурсы были определены в Resource. h для разрешения трех предустановок:


```C++
#define IDS_REDPRESETNAME               102
#define IDS_GREENPRESETNAME             103
#define IDS_BLUEPRESETNAME              104

```



обратите внимание, что необходимо также изменить номер ресурса **\_ APS \_ следующее \_ \_ значение симед** на 106.

## <a name="resource-file"></a>Файл ресурсов

Следующие строки необходимо изменить в файле Гловдлл. RC, чтобы разрешить три предустановки и присвоить им имена:


```C++
    IDS_REDPRESETNAME       "Glow Red"
    IDS_GREENPRESETNAME     "Glow Green"
    IDS_BLUEPRESETNAME      "Glow Blue"

```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**Пример свечения**](the-glow-sample.md)
</dt> </dl>

 

 




