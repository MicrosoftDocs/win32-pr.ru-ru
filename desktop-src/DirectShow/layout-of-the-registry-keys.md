---
description: Структура разделов реестра
ms.assetid: c041d094-8165-446f-bf77-0d53b728fe7a
title: Структура разделов реестра
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4473027b2612d16b3c6daee4f8e708d90b993397b133db111aa55c58e9c4ceb0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119502295"
---
# <a name="layout-of-the-registry-keys"></a>Структура разделов реестра

фильтры DirectShow регистрируются в двух местах:

-   Библиотека DLL, содержащая фильтр, регистрируется в качестве сервера COM фильтра. когда приложение вызывает **cocreateinstance** для создания фильтра, библиотека Microsoft Windows COM использует эту запись реестра для нахождение библиотеки DLL.
-   Дополнительные сведения о фильтре можно зарегистрировать в категории фильтров. Эта информация включает [перечислитель системных устройств](system-device-enumerator.md) и средство [сопоставления фильтров](filter-mapper.md) для нахождение фильтра.

Для регистрации дополнительных сведений о фильтрах фильтры не требуются. Пока библиотека DLL зарегистрирована как сервер COM, приложение может создать фильтр и добавить его в граф фильтра. Однако если вы хотите, чтобы фильтр был обнаруживаемым перечислителем системных устройств или средством сопоставления фильтров, необходимо зарегистрировать дополнительные сведения.

Запись реестра для библиотеки DLL имеет следующие ключи:


```
HKEY_CLASSES_ROOT
    CLSID
        Filter CLSID 
            REG_SZ: (Default) = Friendly name

            InprocServer32
                REG_SZ: (Default) = File name of the DLL
                REG_SZ: ThreadingModel = Both
```



Запись реестра для сведений о фильтрах имеет следующие ключи:


```
HKEY_CLASSES_ROOT
    CLSID
        Category
            Instance
                Filter CLSID
                    REG_SZ: CLSID = Filter CLSID
                    REG_BINARY: FilterData = Filter information
                    REG_SZ: FriendlyName = Friendly name
```




```
Category
```



Идентификатор GUID категории фильтра. (См. раздел [Фильтрация категорий](filter-categories.md).) Сведения о фильтре упаковываются в двоичный формат. Интерфейс [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) распаковать эти данные при поиске фильтра в реестре.

Все идентификаторы GUID категорий фильтров перечислены в реестре в следующем разделе:


```C++
HKEY_CLASSES_ROOT\CLSID\{DA4E3DA0-D07D-11d0-BD50-00A0C911CE86}\Instance
```



 

 



