---
title: сведения об API служб развертывания Windows
description: Windows службы развертывания (WDS) — это набор компонентов, позволяющих развертывать операционные системы Windows, в частности Windows Vista и более поздние версии и Windows Server 2008 и более поздних версий.
ms.assetid: 5742e51a-70e3-4607-bfb7-181362dfb168
keywords:
- Windows службы развертывания Windows службы развертывания, сведения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58dd65f18c1628236358d61656c8c3b414d180e43166daa86dfa6562024252a2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098684"
---
# <a name="about-the-windows-deployment-services-api"></a>сведения об API служб развертывания Windows

Windows службы развертывания (WDS) — это набор компонентов, позволяющих развертывать операционные системы Windows, в частности Windows Vista и более поздние версии и Windows Server 2008 и более поздних версий. Его можно использовать для настройки новых компьютеров с помощью сетевых установок.

пвт, сборщики систем и корпоративные ит-специалисты ищут сведения о развертывании Windows на новых компьютерах. сведения о стандартном решении WDS см. в разделе [пошаговое руководство по обновлению служб Windows Deployment Services](/previous-versions/windows/it-pro/windows-vista/cc766320(v=ws.10)) и [пакет автоматической установки Windows (WAIK)](https://www.microsoft.com/download/details.aspx?id=10333).

В средах, где стандартное решение WDS не может использоваться, API WDS обеспечивает программный доступ к некоторым компонентам WDS.

-   [функции сервера служб Windows Deployment Services](windows-deployment-services-server-functions.md) обеспечивают программный доступ к серверу WDS протокол удаленной загрузки PXE (PXE). Серверные компоненты WDS включают сервер PXE и сервер тривиальных протокол FTP (TFTP) для сетевой загрузки компьютера для загрузки и установки операционной системы.
-   [клиентские функции служб развертывания Windows](windows-deployment-services-client-functions.md) обеспечивают программный доступ к клиенту WDS. клиентские компоненты WDS включают графический пользовательский интерфейс, работающий в среде Windows перед установкой (Windows PE) и взаимодействует с серверными компонентами для выбора и установки образа операционной системы.
-   Для компонентов управления WDS нет API. Эти компоненты представляют собой набор средств, используемых для управления сервером, образами операционных систем и учетными записями клиентских компьютеров. дополнительные сведения о компонентах управления службами развертывания windows см. [в разделе пошаговое руководство по обновлению служб Windows](/previous-versions/windows/it-pro/windows-vista/cc766320(v=ws.10)).

PXE-сервер WDS состоит из PXE-сервера и поставщика PXE. PXE-сервер содержит основные сетевые возможности. PXE-сервер поддерживает интерфейсы подключаемых модулей, известные как поставщики PXE. Эта модель поставщика позволяет разрабатывать пользовательские решения PXE, продолжая использовать основную базу кода PXE-сервера.

-   разработчики могут использовать [функции сервера служб Windowsного развертывания](windows-deployment-services-server-functions.md) , чтобы написать библиотеку DLL для пользовательского поставщика, который будет заменен или запущен в сочетании со стандартным уровнем согласования сведений о загрузке (BINL) на сервере WDS. Например, настраиваемый поставщик может использовать текстовый файл в качестве хранилища данных вместо Active Directory.
-   разработчики могут использовать [функции сервера служб Windowsного развертывания](windows-deployment-services-server-functions.md) для записи поставщика фильтра, который упорядочивается перед BINL или любым другим поставщиком PXE в упорядоченном списке зарегистрированных поставщиков. Затем второй поставщик служб выполняет только выбранные PXE-запросы, а первый поставщик обрабатывает другие запросы. Например, можно включить второй зарегистрированный поставщик в упорядоченном списке, чтобы обеспечить новые функциональные возможности без нарушения работы существующего решения WDS, реализованного в первом поставщике.

клиент WDS включает графический пользовательский интерфейс, работающий в среде Windows перед установкой (Windows PE) и взаимодействует с серверными компонентами для выбора и установки образа операционной системы. Клиентская библиотека WDS поддерживает разработку пользовательских клиентских приложений, которые могут использовать сервер WDS.

-   разработчики могут использовать [клиентские функции служб Windowsного развертывания](windows-deployment-services-client-functions.md) , чтобы написать собственное пользовательское клиентское приложение, заменяющее клиент WDS. Например, пользовательское приложение может перечислить образы, хранящиеся на сервере WDS, и отправить сообщения о ходе установки в журнал событий PXE-сервера.

## <a name="windows-deployment-services-samples"></a>Windows Примеры служб развертывания

пример пользовательского поставщика PXE, поставщика фильтра и клиентского приложения WDS доступен в пакете microsoft Windows software development kit (sdk), см. в разделе пакет [средств разработки программного обеспечения](https://developer.microsoft.com/windows/downloads/windows-10-sdk/)(sdk) для microsoft Windows.

Следующие примеры WDS можно скачать в Интернете в [коллекции кода для настольных систем](https://github.com/microsoft/Windows-classic-samples).

<dl>

[Windows Образец поставщика фильтра служб развертывания](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/WindowsDeploymentServices/FilterProvider)  
[Windows Пример перечисления образов служб развертывания](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/WindowsDeploymentServices/ImageEnumeration)  
[Windows Пример многоадресного потребителя служб развертывания](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/WindowsDeploymentServices/Multicast/WdsProvider)  
[Windows Пример поставщика многоадресной рассылки служб развертывания](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/WindowsDeploymentServices/Multicast/WdsProvider)  
[Windows Пример поставщика служб развертывания](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/WindowsDeploymentServices/FilterProvider)  
[Windows Пример диспетчера транспорта служб развертывания](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/WindowsDeploymentServices/Management/WDSTransportManager)  
</dl>

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Использование API сервера служб развертывания Windows](using-the-windows-deployment-services-server-api.md)
</dt> <dt>

[Использование API клиента служб развертывания Windows](using-the-windows-deployment-services-client-api.md)
</dt> </dl>

 

 