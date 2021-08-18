---
description: Следующая процедура используется для разработки нового приложения или обновления существующего приложения для использования параллельных сборок, доступных в Microsoft или других издателях параллельных сборок.
ms.assetid: da6b6767-8a30-4a76-a030-615067a2cb17
title: Использование параллельных сборок
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a60170dc4873f03dfc17769f91106e02b591e0b1db81695d773a35b392a2c7dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141717"
---
# <a name="using-side-by-side-assemblies"></a>Использование параллельных сборок

Следующая процедура используется для разработки нового приложения или обновления существующего приложения для использования [параллельных сборок](about-side-by-side-assemblies-.md) , доступных в Microsoft или других издателях параллельных сборок. Список параллельных сборок, предоставляемых корпорацией Майкрософт, см. в разделе [Поддерживаемые параллельные сборки Майкрософт](supported-microsoft-side-by-side-assemblies.md). обратите внимание, что приложение должно выполняться по крайней мере Windows XP для установки сборок в качестве параллельных сборок. Дополнительные сведения см. в разделе [рекомендации по созданию параллельных сборок](guidelines-for-creating-side-by-side-assemblies.md).

**Добавление параллельной сборки в приложение**

1.  Определяет параллельные сборки, необходимые для приложения. начиная с Windows XP эти параллельные сборки и их манифесты сборок устанавливаются вместе с операционной системой, но не регистрируются глобально.
2.  Используйте редактор XML для создания [манифеста приложения](application-manifests.md). См. пример манифеста приложения ниже. Дополнительные сведения см. в разделе [манифесты приложений](application-manifests.md) в [справочнике по файлам манифеста](manifest-files-reference.md).
3.  Введите значения атрибутов в вложенный элемент [*assemblyIdentity-context*](d-sbscs-gly.md) в манифесте приложения, который уникальным образом определяет приложение. Дополнительные сведения о **теге**"DEF-контекст" см. в разделе [манифесты приложений](application-manifests.md).
4.  Если сборка содержит зависимые сборки, введите значения атрибутов в соответствующие вложенные элементы [*assemblyIdentity ref-context*](r-sbscs-gly.md) манифеста приложения. Дополнительные сведения о **ТЕГЕ** ref-context см. в разделе [манифесты приложений](application-manifests.md).

    ``` syntax
    <dependentAssembly>
      <assemblyIdentity type="win32"
                        name="Microsoft.Windows.SampleAssembly"
                        version="6.0.0.0" processorArchitecture="x86"
                        publicKeyToken="a5aaf5ba15723d5"/>
    ```

5.  Манифест приложения можно включить в файл заголовков двоичного файла приложения.

    В этом случае добавьте в файл заголовка приложения следующую строку:

    <dl> \_Манифест для \_ ИД ресурса манифеста CREATEPROCESS \_ \_ "YourApp.exe. manifest"  
    </dl>

    В качестве альтернативы можно поместить отдельный файл манифеста в тот же каталог, где находится исполняемый файл приложения. Операционная система сначала загружает манифест из файловой системы, а затем проверяет раздел ресурсов исполняемого файла. Версия файловой системы имеет приоритет.

6.  [общие сборки](/windows/desktop/Msi/shared-assemblies) следует устанавливать с помощью [установщик Windows](../msi/windows-installer-portal.md) версии 2,0. создайте пакет установщик Windows, как описано в разделе [как установить сборки Win32 для параллельного совместного использования в Windows XP](../msi/installing-win32-assemblies-for-side-by-side-sharing-on-windows-xp.md).
7.  [закрытые сборки](/windows/desktop/Msi/private-assemblies) можно устанавливать с помощью [установщик Windows](../msi/windows-installer-portal.md) версии 2,0. создайте пакет установщик Windows, как описано в разделе [как установить сборки Win32 для частного использования приложения в Windows XP](../msi/installing-win32-assemblies-for-the-private-use-of-an-application-on-windows-xp.md). Можно также использовать любой другой установщик для копирования закрытой сборки и ее манифеста в ту же папку, что и исполняемый файл приложения.
8.  Тестирование приложения для проверки результатов. Обратите внимание, что на тестовом компьютере не должна быть зарегистрирована параллельная сборка.
9.  разверните приложение или обновите его как пакет установщик Windows.

## <a name="example-application-manifest"></a>Пример манифеста приложения

Ниже приведен пример манифеста приложения.

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
  <assemblyIdentity type="win32" name="Microsoft.Windows.mysampleapp" version="1.0.0.0" processorArchitecture="x86"/>
  <dependency>
    <dependentAssembly>
      <assemblyIdentity type="win32" name="Microsoft.Windows.SampleAssembly" version="6.0.0.0" processorArchitecture="x86" publicKeyToken="a5aaf5ba15723d5"/>
    </dependentAssembly>
  </dependency>
  <dependency>
    <dependentAssembly>
      <assemblyIdentity type="win32" name="Microsoft.Tools.MyPrivateDll" version="2.5.0.0" processorArchitecture="x86"/>
    </dependentAssembly>
  </dependency>
</assembly>
```

 

 
