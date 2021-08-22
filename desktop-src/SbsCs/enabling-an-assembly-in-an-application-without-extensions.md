---
description: Если в приложении не размещена библиотека DLL, расширение, подключаемый модуль или панель управления, можно использовать метод, описанный в этом разделе, чтобы включить сборку для приложения.
ms.assetid: d043ec1b-ac31-45fb-9232-eec42aef4ac3
title: Включение сборки в приложении без расширений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a6666d7b50775438f0d4a3edd13658e5c18127a21c37ec95e46a873682e6f8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142257"
---
# <a name="enabling-an-assembly-in-an-application-without-extensions"></a>Включение сборки в приложении без расширений

Если в приложении не размещена библиотека DLL, расширение, подключаемый модуль или панель управления, можно использовать метод, описанный в этом разделе, чтобы включить сборку для приложения. Дополнительные сведения о добавлении сборки в приложения с расширениями см. [в разделе Включение сборки в приложении, где размещается библиотека DLL, расширение или панель управления](enabling-an-assembly-in-an-application-hosting-a-dll-extension-or-control-panel.md).

**Включение сборки в приложении без размещенных компонентов**

1.  Создайте манифест, описывающий зависимость приложения или расширения для сборки.

    Например, манифест для "Йоураппликатион" можно создать, скопировав следующий пример манифеста и подставив правильные значения для **assemblyIdentity**, **processorArchitecture** и **Description**. Установите значение **processorArchitecture** на x86, если сборка на 32-разрядной платформе, и на ia64 при сборке на 64-разрядной платформе. Элемент **Description** содержит описание параметра приложения. Дополнительные сведения о формате манифеста см. в разделе [манифесты приложений](application-manifests.md).

    ``` syntax
    <?xml version="1.0" encoding="UTF-8" standalone="yes"?>
    <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <assemblyIdentity
        version="1.0.0.0"
        processorArchitecture="x86"
        name="YourCompanyName.YourDivision.YourApp"
        type="win32"
    />
    <description>Your app description here</description>
    <dependency>
        <dependentAssembly>
            <assemblyIdentity
                type="win32"
                name="Proseware.Research.SampleAssembly"
                version="6.0.0.0"
                processorArchitecture="X86"
                publicKeyToken="0000000000000000"
                language="*"
            />
        </dependentAssembly>
    </dependency>
    </assembly>
    ```

2.  Добавьте манифест в приложение в качестве ресурса в двоичный файл заголовка исполняемого файла приложения. Не рекомендуется добавлять манифест в приложение в качестве внешнего файла манифеста.

    Чтобы добавить манифест в качестве ресурса, создайте ресурс в приложении типа "RT \_ manifest ID 1". Например, если имя приложения — Йоурапп, файл заголовка приложения должен содержать следующее:

    ``` syntax
    #define MANIFEST_RESOURCE_ID 1
    MANIFEST_RESOURCE_ID RT_MANIFEST "YourApp.manifest"
    ```

    При добавлении манифеста в качестве внешнего файла манифеста следует убедиться, что установка копирует файл манифеста в папку, содержащую исполняемый файл приложения.

3.  Выполните проверку, чтобы убедиться, что сборки, используемые приложением, работают в приложении правильно.

 

 



