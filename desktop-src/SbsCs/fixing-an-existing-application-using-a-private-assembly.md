---
description: Начиная с Windows XP, можно создать закрытую сборку и сделать ее доступной для конкретного приложения.
ms.assetid: 08cebffc-6856-4dac-8600-5e7fecb5c69b
title: Исправление существующего приложения с помощью закрытой сборки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 095c3eefc5f166ad09643a363ec4308d190e6586
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072688"
---
# <a name="fixing-an-existing-application-using-a-private-assembly"></a>Исправление существующего приложения с помощью закрытой сборки

Начиная с Windows XP, можно создать закрытую сборку и сделать ее доступной для конкретного приложения. Эту возможность можно использовать для исправления приложения, которое станет несовместимым с обновлением. Примером может быть приложение, которое станет несовместимым с последней версией MSVCRT.DLL после обновления операционной системы. В этом случае нет возможности заменить версию системы, так как MSVCRT.DLL является защищенным файлом Windows. Вместо того чтобы переписывать приложение для работы с новой версией MSVCRT, можно создать закрытую сборку для MSVCRT и установить ее в папке приложения. Обратите внимание, что не каждый общий компонент является подходящим кандидатом для закрытой параллельной сборки, а некоторые компоненты имеют ограничения лицензирования относительно того, где можно установить компоненты. Компонент должен удовлетворять критериям для параллельного компонента. Обратитесь к издателю компонента, если он может предоставить подходящую сборку.

Манифест закрытой сборки и манифест приложения должны быть установлены в той же папке, что и исполняемый файл приложения. При запуске приложения он обращается к манифесту приложения и загружает версию MSVCRT, которая является частной для приложения.

В этом примере частная сборка будет включать как MSVCRT.DLL, так и MSVCIRT.DLL, как в следующем манифесте сборки:

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <assemblyIdentity type="win32"
      name="Microsoft.Windows.PrivateCPlusPlusRuntime" 
version="6.0.0.0" 
processorArchitecture="x86"/>
    <file name="msvcrt.dll"/>
    <file name="msvcirt.dll"/>
</assembly>
```

Ниже приведен пример возможного манифеста приложения.

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0"> 
<assemblyIdentity 
    version="1.0.0.0" 
    processorArchitecture="x86" 
    name="APPLICATION" 
    type="win32" 
/> 
<description>Description of Application</description> 
<dependency> 
    <dependentAssembly> 
       <assemblyIdentity 
           type="win32"
           name="Microsoft.Windows.PrivateCPlusPlusRuntime" 
           version="6.0.0.0" 
           processorArchitecture="x86"/> 
    </dependentAssembly> 
</dependency> 
</assembly>
```

 

 



