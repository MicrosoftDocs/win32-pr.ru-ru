---
description: на сервере Windows 2003 служба WinHTTP реализована как параллельная сборка и должна быть связана как таковая. обратите внимание, что это не относится к Windows Vista и более поздним версиям.
ms.assetid: 524d926d-4d8a-4576-96fd-c533517ba28e
title: Использование WinHTTP в качестве параллельной сборки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c8c6312fb57f210e0324c1ae89bb785fd5b51bcb2b1ea4ba1a4959a3d0fd540
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119614094"
---
# <a name="using-winhttp-as-a-side-by-side-assembly"></a>Использование WinHTTP в качестве параллельной сборки

на сервере Windows 2003 служба WinHTTP реализована как параллельная сборка и должна быть связана как таковая. обратите внимание, что это не относится к Windows Vista и более поздним версиям.

## <a name="side-by-side-assemblies"></a>Параллельные сборки

начиная с Microsoft Windows XP, был предоставлен механизм параллельных сборок для управления связыванием во время выполнения, чтобы избежать конфликтов управления версиями библиотеки динамической компоновки (DLL). Сведения о параллельных сборках см. в разделе [о изолированных приложениях и параллельных сборках](/windows/desktop/SbsCs/about-isolated-applications-and-side-by-side-assemblies).

чтобы использовать этот механизм для связи с WinHTTP 5,1 на сервере Windows 2003, приложение должно включить манифест, который указывает WinHTTP в качестве зависимой сборки. Дополнительные сведения о том, как это сделать, см. в разделе [использование параллельных сборок](/windows/desktop/SbsCs/using-side-by-side-assemblies) .

## <a name="a-sample-winhttp-application-manifest"></a>Пример манифеста приложения WinHTTP

В примере манифеста ниже показан манифест приложения, который можно использовать для связи с WinHTTP.

Все атрибуты, кроме "Type" для " <assembly> <assemblyIdentity> ", должны быть изменены в соответствии с конкретным приложением. То же самое касается содержимого &lt; элемента «Description &gt; ».

Кроме того, убедитесь, что атрибут "processorArchitecture" объекта " <dependentAssembly> <assemblyIdentity> " соответствует атрибуту "processorArchitecture" элемента " <assembly> <assemblyIdentity> ". Ниже, например, для обоих задано значение "x86".

Все значения, не относящиеся к конкретному приложению, должны принять формы, показанные ниже.

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
  <assemblyIdentity
                    version="1.0.0.0"
                    processorArchitecture="x86"
                    name="Microsoft.Windows.Sample"
                    type="win32" />
  <description>Sample WinHttp Application</description>
  <dependency>
    <dependentAssembly>
      <assemblyIdentity 
                    type="win32" 
                    name="Microsoft.Windows.WinHTTP" 
                    version="5.1.0.0"
                    processorArchitecture="x86" 
                    publicKeyToken="6595b64144ccf1df"
                    language="*" />
    </dependentAssembly>
  </dependency>
</assembly>
```

 

 
