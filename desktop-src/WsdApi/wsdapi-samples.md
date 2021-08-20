---
description: существует два примера WSDAPI, входящих в состав Windows SDK для Windows Server 2008.
ms.assetid: 156b79ef-1f05-4ef1-9df9-81fe81c73ca7
title: Примеры WSDAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06cf4c1ff36195e667c55d9fb5206c0cee2afcf15d1bad7f0139911b3f702a37
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117919961"
---
# <a name="wsdapi-samples"></a>Примеры WSDAPI

существует два примера WSDAPI, входящих в состав Windows SDK для Windows Server 2008. Исходный код для образцов можно найти в <Windows SDK Install Folder> \\ примерах \\ веб- \\ WSDAPI. Эта версия пакета SDK доступна в [центре загрузки](https://www.microsoft.com/downloads/details.aspx?FamilyID=f26b1aa4-741a-433a-9be5-fa919850bdbf). образцы недоступны в пакете SDK для Windows Vista.

Образец котировки котировок (расположенный в <Windows SDK Install Folder> \\ примерах \\ Web \\ WSDAPI \\ стокккуоте) демонстрирует службу с базовой функциональностью обмена сообщениями. Пример службы файлов (расположенный в <Windows SDK Install Folder> \\ примерах \\ Web \\ WSDAPI \\ FileService) демонстрирует службу с расширенными функциями, такими как асинхронный обмен сообщениями, вложения и события.

Оба образца включают следующие типы файлов.

-   WSDL-файлы, содержащие описания служб.
-   [Файлы конфигурации всдкодежен](wsdcodegen-configuration-file.md) , используемые для создания кода WSDAPI.
-   Созданный заголовок и исходные файлы C++.
-   Файлы реализации клиента и службы.
-   Visual Studio файлы проекта и решения.

Оба примера реализуют узлы устройств ([**ивсддевицехост**](/windows/desktop/api/WsdHost/nn-wsdhost-iwsddevicehost)), прокси-серверы устройств ([**ивсддевицепрокси**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsddeviceproxy)) и прокси-серверы служб ([**ивсдсервицепрокси**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsdserviceproxy)). Кроме того, в примере службы файлов демонстрируется использование асинхронного обмена сообщениями ([**ивсдасинккаллбакк**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsdasynccallback), [**ивсдасинкресулт**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsdasyncresult)), вложений ([**ивсдинбаундаттачмент**](/windows/desktop/api/WsdAttachment/nn-wsdattachment-iwsdinboundattachment), [**ивсдаутбаундаттачмент**](/windows/desktop/api/WsdAttachment/nn-wsdattachment-iwsdoutboundattachment)) и событий.

Файлы Филесервицеконтракт. vcproj и Стокккуотеконтракт. vcproj, содержащиеся в примерах, вызывают [всдкодежен](web-services-for-devices-code-generator.md) для создания заголовка и исходных файлов C++ из WSDL-файла, указанного в файле конфигурации всдкодежен. Это означает, что при изменении образца файла конфигурации WSDL или Всдкодежен и перестроении примера проекта Всдкодежен автоматически создает новые заголовочные и исходные файлы, отражающие изменения. Это предпочтительный метод создания приложений WSDAPI. Всдкодежен обычно вызывается из командной строки. Откройте соответствующий \* файл. vcproj, чтобы просмотреть пример вызовов командной строки всдкодежен.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Разработка приложений WSD на Windows](wsd-application-development-on-windows.md)
</dt> </dl>

 

 



