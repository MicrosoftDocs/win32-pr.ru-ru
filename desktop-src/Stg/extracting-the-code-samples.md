---
title: Извлечение примеров кода
description: Хотя примеры кода делятся на ряд учебных занятий, соответствующие примеры группирования можно легко извлечь из коллекции.
ms.assetid: f8e20e40-cfef-4844-8b28-5a11fdcd691a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67093f4cfbbfab2a3c1681462627f02b504124ed15d1483b9f9d91ec5551d0e4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120034954"
---
# <a name="extracting-the-code-samples"></a>Извлечение примеров кода

Хотя примеры кода делятся на ряд учебных занятий, соответствующие примеры группирования можно легко извлечь из коллекции. Большинство отдельных каталогов примеров предназначены для работы в сочетании с одним и тем же каталогом примеров. Примеры, связанные с компонентами, состоят из пары "клиент-сервер" с сервером, требующим использования примера программы REGISTER. Ниже приведена сводка по примерам группирования и способам извлечения каждой группы в качестве единицы сборки. Для каждого примера группировки скопируйте содержимое указанных каталогов. Для указанного \[ родительского \] каталога назначения не требуется содержимое из ветви Samples. Однако меню справки в выполняющихся примерах предполагают, что соответствующие учебники .HTM файлы справки находятся в этом родительском \[ каталоге назначения \] .

Для приложения Win32 РЕАДТУТ:

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    READTUT
```

Для приложения с каркасом Win32 EXE:

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    EXESKEL
```

Для схемы Win32 DLL:

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    DLLSKEL
    DLLUSER
```

Для основных примеров COM-объектов:

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    COMOBJ
    COMUSER
```

Для базового внутрипроцессного компонента DLL клиент/сервер-компонент:

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    DLLSERVE
    DLLCLIEN
```

Для лицензий с лицензированным компонентом "клиент-сервер":

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    LICSERVE
    LICCLIEN
```

Для стандартных примеров маршалирования:

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    MARSHAL
    MARSHAL2
```

Для необработанных примеров локального клиента/сервера:

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    MARSHAL
    LOCSERVE
    LOCCLIEN
```

Для образцов клиент/сервер модели подразделения:

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    MARSHAL
    APTSERVE
    APTCLIEN
```

Для образцов клиент/сервер DCOM (Distributed COM):

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    MARSHAL
    APTSERVE
    REMCLIEN
```

Для бесплатных образцов клиента/сервера:

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    FRESERVE
    FRECLIEN
```

Для подключаемых примеров клиента или сервера COM-объекта:

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    CONSERVE
    CONCLIEN
```

Примеры для клиента или сервера структурированного хранилища:

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    STOSERVE
    STOCLIEN
```

Для примеров "клиент-сервер постоянных объектов":

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    PERSERVE
    PERTEXT
    PERDRAW
    PERCLIEN
```

Примеры для клиента/сервера безопасности DCOM:

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    DCDMARSH
    DCDSERVE
    DCOMDRAW
```

 

 




