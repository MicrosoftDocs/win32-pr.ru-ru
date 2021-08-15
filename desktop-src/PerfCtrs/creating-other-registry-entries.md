---
description: Функции Опенперформанцедата DLL производительности в качестве входных данных принимают строковый аргумент.
ms.assetid: 8ec0ea45-5789-4801-b486-555779a7303e
title: Создание других записей реестра
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5ad9fe960713a481ba5a9b8f4b73e11bdbdd4d9fe9474b04b994e373ce8e1bd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119683974"
---
# <a name="creating-other-registry-entries"></a>Создание других записей реестра

Функция [**опенперформанцедата**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) библиотеки производительности DLL принимает строковый аргумент в качестве входных данных. Чтобы предоставить входную строку открытой функции, включите ключ **компоновки** в ключ **служб** . Ключ **компоновки** содержит значение **экспорта** . Задайте данные для **экспорта** во входной строке, которую необходимо передать в функцию Open. Тип данных **Export** — **reg \_ Multi \_ SZ**.

Если параметр **Export** не определен (**Экспорт** является необязательным), система передает **значение NULL** в функцию [**опенперформанцедата**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) .

Как правило, если в нескольких приложениях используется одна и та же библиотека производительности, то каждое приложение включает ключ **компоновки** и значение **экспорта** для предоставления контекста, в котором приложение вызывает библиотеку DLL.

Ниже приведены записи реестра.

```
HKEY_LOCAL_MACHINE
   \SYSTEM
      \CurrentControlSet
         \Services
            \application-name-1
               \Linkage
                  Export = app-1 context strings
               \Performance
                  Library = perfctrs.dll
            \application-name-2
               \Linkage
                  Export = app-2 context strings
               \Performance
                  Library = perfctrs.dll
```

По умолчанию функции [**опенперформанцедата**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) и [**коллектперформанцедата**](/windows/win32/api/winperf/nc-winperf-pm_collect_proc) DLL производительности должны возвращать значение в пределах 10 000 миллисекунд. В противном случае система не использует данные, возвращаемые библиотекой DLL. Приложение может увеличить или уменьшить значение времени ожидания, указав в качестве ключа **производительности** время ожидания **открытия** или получения **значения реестра,** как показано в следующем примере.

```
HKEY_LOCAL_MACHINE
   \SYSTEM
      \CurrentControlSet
         \Services
            \application-name
               \Performance
                  Open Timeout = Timeout value for your open function, in milliseconds
                  Collect Timeout = Timeout value for your collect function, in milliseconds
```

Чтобы получить данные о производительности для некоторых приложений (которые возвращают счетчики с помощью функции [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) ), необходимо использовать функцию [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) , чтобы открыть устройство, связанное с приложением. В этом случае имя, указанное в **CreateFile** , также должно быть установлено в узле DOS Devices в реестре, как показано ниже:

```
HKEY_LOCAL_MACHINE
   \SYSTEM
      \CurrentControlSet
         \Control
            \Session Manager
               \DOS Devices
```

 

 
