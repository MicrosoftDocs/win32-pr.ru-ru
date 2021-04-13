---
title: Извлечение примеров кода
description: Хотя примеры кода делятся на ряд учебных занятий, соответствующие примеры группирования можно легко извлечь из коллекции.
ms.assetid: f8e20e40-cfef-4844-8b28-5a11fdcd691a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a593cf36b2fa235813c291eb35307153b28a2aa4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104410817"
---
# <a name="extracting-the-code-samples"></a>Извлечение примеров кода

Хотя примеры кода делятся на ряд учебных занятий, соответствующие примеры группирования можно легко извлечь из коллекции. Большинство отдельных каталогов примеров предназначены для работы в сочетании с одним и тем же каталогом примеров. Примеры, связанные с компонентами, состоят из пары "клиент-сервер" с сервером, требующим использования примера программы REGISTER. Ниже приведена сводка по примерам группирования и способам извлечения каждой группы в качестве единицы сборки. Для каждого примера группировки скопируйте содержимое указанных каталогов. Для указанного \[ родительского \] каталога назначения не требуется содержимое из ветви Samples. Однако меню «Справка» в выполняющихся примерах предполагает, что вам нужно руководство. Файлы справки HTM находятся в этом родительском \[ \] каталоге назначения.

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

 

 




