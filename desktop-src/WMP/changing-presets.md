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
ms.openlocfilehash: 95d24841c95c3fc1029aa0c405e90b329799fdbe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105691214"
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



Обратите внимание, что необходимо также изменить номер ресурса **\_ ТД \_ Next \_ Симед в \_ значение** 106.

## <a name="resource-file"></a>Файл ресурсов

Следующие строки необходимо изменить в файле Гловдлл. RC, чтобы разрешить три предустановки и присвоить им имена:


```C++
    IDS_REDPRESETNAME       "Glow Red"
    IDS_GREENPRESETNAME     "Glow Green"
    IDS_BLUEPRESETNAME      "Glow Blue"

```



## <a name="related-topics"></a>См. также

<dl> <dt>

[**Пример свечения**](the-glow-sample.md)
</dt> </dl>

 

 




