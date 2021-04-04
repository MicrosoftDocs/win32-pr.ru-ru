---
title: Сведения об API служб развертывания Windows
description: Службы развертывания Windows (WDS) — это набор компонентов, позволяющих развертывать операционные системы Windows, в частности Windows Vista и более поздние версии, а также Windows Server 2008 и более поздние версии.
ms.assetid: 5742e51a-70e3-4607-bfb7-181362dfb168
keywords:
- Службы развертывания Windows, сведения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eac4a904765f58ccf995c5bbc0a9413f8eb4d13c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103987571"
---
# <a name="about-the-windows-deployment-services-api"></a>Сведения об API служб развертывания Windows

Службы развертывания Windows (WDS) — это набор компонентов, позволяющих развертывать операционные системы Windows, в частности Windows Vista и более поздние версии, а также Windows Server 2008 и более поздние версии. Его можно использовать для настройки новых компьютеров с помощью сетевых установок.

Изготовителям оборудования, сборщикам систем и корпоративным ИТ-специалистам требуются сведения о развертывании Windows на новых компьютерах. сведения о стандартном решении WDS см. в разделе Пошаговое [руководство по обновлению служб развертывания Windows](/previous-versions/windows/it-pro/windows-vista/cc766320(v=ws.10)) и [пакет автоматической установки Windows (WAIK)](https://www.microsoft.com/download/details.aspx?id=10333).

В средах, где стандартное решение WDS не может использоваться, API WDS обеспечивает программный доступ к некоторым компонентам WDS.

-   [Функции сервера служб развертывания Windows](windows-deployment-services-server-functions.md) предоставляют программный доступ к серверу WDS протокол удаленной загрузки PXE (PXE). Серверные компоненты WDS включают сервер PXE и сервер тривиальных протокол FTP (TFTP) для сетевой загрузки компьютера для загрузки и установки операционной системы.
-   [Клиентские функции служб развертывания Windows](windows-deployment-services-client-functions.md) предоставляют программный доступ к клиенту WDS. Клиентские компоненты WDS включают графический пользовательский интерфейс, работающий в среде предустановки Windows (Windows PE), и взаимодействует с серверными компонентами для выбора и установки образа операционной системы.
-   Для компонентов управления WDS нет API. Эти компоненты представляют собой набор средств, используемых для управления сервером, образами операционных систем и учетными записями клиентских компьютеров. Дополнительные сведения о компонентах управления WDS см. [в разделе Пошаговое руководство по обновлению служб развертывания Windows](/previous-versions/windows/it-pro/windows-vista/cc766320(v=ws.10)).

PXE-сервер WDS состоит из PXE-сервера и поставщика PXE. PXE-сервер содержит основные сетевые возможности. PXE-сервер поддерживает интерфейсы подключаемых модулей, известные как поставщики PXE. Эта модель поставщика позволяет разрабатывать пользовательские решения PXE, продолжая использовать основную базу кода PXE-сервера.

-   Разработчики могут использовать [функции сервера служб развертывания Windows](windows-deployment-services-server-functions.md) для создания библиотеки DLL для настраиваемого поставщика, который заменяется или выполняется в сочетании со стандартным уровнем согласованности сведений о загрузке (BINL) на сервере WDS. Например, настраиваемый поставщик может использовать текстовый файл в качестве хранилища данных вместо Active Directory.
-   Разработчики могут использовать [функции сервера служб развертывания Windows](windows-deployment-services-server-functions.md) для записи поставщика фильтра, который упорядочивается перед BINL или любым другим поставщиком PXE в упорядоченном списке зарегистрированных поставщиков. Затем второй поставщик служб выполняет только выбранные PXE-запросы, а первый поставщик обрабатывает другие запросы. Например, можно включить второй зарегистрированный поставщик в упорядоченном списке, чтобы обеспечить новые функциональные возможности без нарушения работы существующего решения WDS, реализованного в первом поставщике.

Клиент WDS включает графический пользовательский интерфейс, работающий в среде предустановки Windows (Windows PE), и взаимодействует с серверными компонентами для выбора и установки образа операционной системы. Клиентская библиотека WDS поддерживает разработку пользовательских клиентских приложений, которые могут использовать сервер WDS.

-   Разработчики могут использовать [клиентские функции служб развертывания Windows](windows-deployment-services-client-functions.md) для записи собственного клиентского приложения, заменяющего клиент WDS. Например, пользовательское приложение может перечислить образы, хранящиеся на сервере WDS, и отправить сообщения о ходе установки в журнал событий PXE-сервера.

## <a name="windows-deployment-services-samples"></a>Примеры служб развертывания Windows

Пример настраиваемого поставщика PXE, поставщика фильтра и клиентского приложения WDS доступен в пакете средств разработки программного обеспечения (SDK) для Microsoft Windows, см. в разделе пакет средств [разработки программного обеспечения Microsoft Windows (SDK)](https://developer.microsoft.com/windows/downloads/windows-10-sdk/).

Следующие примеры WDS можно скачать в Интернете в [коллекции кода для настольных систем](https://github.com/microsoft/Windows-classic-samples).

<dl>

[Образец поставщика фильтра служб развертывания Windows](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/WindowsDeploymentServices/FilterProvider)  
[Пример перечисления образов служб развертывания Windows](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/WindowsDeploymentServices/ImageEnumeration)  
[Пример многоадресного потребителя служб развертывания Windows](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/WindowsDeploymentServices/Multicast/WdsProvider)  
[Пример поставщика многоадресной рассылки служб развертывания Windows](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/WindowsDeploymentServices/Multicast/WdsProvider)  
[Пример поставщика служб развертывания Windows](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/WindowsDeploymentServices/FilterProvider)  
[Пример диспетчера транспорта служб развертывания Windows](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/WindowsDeploymentServices/Management/WDSTransportManager)  
</dl>

## <a name="related-topics"></a>См. также

<dl> <dt>

[Использование API сервера служб развертывания Windows](using-the-windows-deployment-services-server-api.md)
</dt> <dt>

[Использование API клиента служб развертывания Windows](using-the-windows-deployment-services-client-api.md)
</dt> </dl>

 

 