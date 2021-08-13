---
description: Расширенные примеры Winsock с использованием расширений SSL
ms.assetid: 9c429363-f9bb-4394-89be-f87507f5cbdd
title: Расширенные примеры Winsock с использованием расширений SSL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ead38a7e62be527e91474ac921803327647ca6cefd1ec68778d03e1c68c1bf3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119412174"
---
# <a name="advanced-winsock-samples-using-secure-socket-extensions"></a>Расширенные примеры Winsock с использованием расширений SSL

## <a name="secure-tcp-client-and-server-sample"></a>Пример защиты клиента и сервера TCP

более сложный пример Winsock, демонстрирующий использование расширений ssl, входит в состав пакета средств разработки Microsoft Windows Software Development Kit (SDK). Этот пример включает клиент TCP и сервер, которые безопасно подключаются с помощью Winsock и расширений SSL.

По умолчанию исходный код примера Winsock устанавливается в следующий каталог:

*C: \\ Program files \\ Microsoft sdks \\ Windows \\ v 6.0 \\ samples \\ нетдс \\ winsock*

Пример находится в следующей папке:

*секуресоккет*

Пример кода разбивается на отдельные каталоги, как описано ниже.

-   сткпклиент — папка, содержащая код защищенного клиента TCP.
-   сткпкоммон — папка, содержащая общий код библиотеки, который является общим для защищенного клиента TCP и сервера.
-   сткпсервер — папка, содержащая код защищенного TCP-сервера.

следует отметить, что образцы предназначены для запуска на двух разных компьютерах с Windows Vista или более поздней версии. Кроме того, учетные данные IPsec должны быть подготовлены на обоих компьютерах для обеспечения успешности подключения, поскольку в примере используется протокол IPsec для защиты своего трафика. Дополнительные сведения о настройке учетных данных IPsec см. в документации по [конфигурации IPSec](/windows/desktop/FWP/ipsec-configuration) .

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

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[сведения о платформе фильтрации Windows](/windows/desktop/FWP/about-windows-filtering-platform)
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

[Windows Функции API платформы фильтрации](/windows/desktop/FWP/fwp-functions)
</dt> <dt>

[Расширения безопасных сокетов Winsock](winsock-secure-socket-extensions.md)
</dt> </dl>

 

 
