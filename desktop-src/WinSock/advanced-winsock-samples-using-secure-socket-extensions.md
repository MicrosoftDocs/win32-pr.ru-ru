---
description: Расширенные примеры Winsock с использованием расширений SSL
ms.assetid: 9c429363-f9bb-4394-89be-f87507f5cbdd
title: Расширенные примеры Winsock с использованием расширений SSL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6701809ad97c7d39acf1f0eae646e7555e5c967f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991118"
---
# <a name="advanced-winsock-samples-using-secure-socket-extensions"></a>Расширенные примеры Winsock с использованием расширений SSL

## <a name="secure-tcp-client-and-server-sample"></a>Пример защиты клиента и сервера TCP

Более сложный пример Winsock, демонстрирующий использование расширений SSL, входит в состав пакета средств разработки программного обеспечения (SDK) для Microsoft Windows. Этот пример включает клиент TCP и сервер, которые безопасно подключаются с помощью Winsock и расширений SSL.

По умолчанию исходный код примера Winsock устанавливается в следующий каталог:

*C: \\ Program Files \\ Microsoft SDK \\ Windows \\ v 6.0 \\ Samples \\ нетдс \\ Winsock*

Пример находится в следующей папке:

*секуресоккет*

Пример кода разбивается на отдельные каталоги, как описано ниже.

-   сткпклиент — папка, содержащая код защищенного клиента TCP.
-   сткпкоммон — папка, содержащая общий код библиотеки, который является общим для защищенного клиента TCP и сервера.
-   сткпсервер — папка, содержащая код защищенного TCP-сервера.

Следует отметить, что образцы предназначены для запуска на двух разных компьютерах под управлением Windows Vista или более поздней версии. Кроме того, учетные данные IPsec должны быть подготовлены на обоих компьютерах для обеспечения успешности подключения, поскольку в примере используется протокол IPsec для защиты своего трафика. Дополнительные сведения о настройке учетных данных IPsec см. в документации по [конфигурации IPSec](/windows/desktop/FWP/ipsec-configuration) .

При построении образца будут созданы два исполняемых файла:

*stcpclient.exe* и *stcpserver.exe*.

Скопируйте *stcpclient.exe* на компьютер A и скопируйте *stcpserver.exe* на компьютер B. На компьютере B запустите TCP-сервер, выполнив в командной строке следующую команду:

**stcpserver.exe**

Чтобы получить дополнительные параметры использования для сервера, выполните следующую команду:

**stcpserver.exe/?**

Затем на компьютере а запустите TCP-клиент, выполнив в командной строке следующую команду:

**stcpclient.exe <полное DNS-имя-для-Machine-B>**

На этом этапе подключение должно быть установлено безопасно.

Чтобы получить дополнительные параметры использования для клиента, выполните следующую команду:

**stcpclient.exe/?**

## <a name="related-topics"></a>См. также

<dl> <dt>

[О платформе фильтрации Windows](/windows/desktop/FWP/about-windows-filtering-platform)
</dt> <dt>

[Принудительное применение уровня приложения (ALE)](/windows/desktop/FWP/application-layer-enforcement--ale-)
</dt> <dt>

[Конфигурация IPsec](/windows/desktop/FWP/ipsec-configuration)
</dt> <dt>

[Функции IPsec](/windows/desktop/FWP/fwp-ipsec-functions)
</dt> <dt>

[Использование расширений SSL](using-secure-socket-extensions.md)
</dt> <dt>

[интерфейс поставщика поддержки безопасности (SSPI)](/windows/desktop/Rpc/security-support-provider-interface-sspi-)
</dt> <dt>

[Платформа фильтрации Windows](/windows/desktop/FWP/windows-filtering-platform-start-page)
</dt> <dt>

[Функции API платформы фильтрации Windows](/windows/desktop/FWP/fwp-functions)
</dt> <dt>

[Расширения безопасных сокетов Winsock](winsock-secure-socket-extensions.md)
</dt> </dl>

 

 
