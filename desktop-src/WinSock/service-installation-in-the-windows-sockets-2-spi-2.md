---
description: Установка службы в Windows Sockets 2 (Winsock) SPI.
ms.assetid: a303fbcf-9122-422a-9b12-d00a5df0fc0f
title: Установка службы в списке SPI Windows Sockets 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9028f35c21cc7055e8b8dde060c1c178dbf76715
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692836"
---
# <a name="service-installation-in-the-windows-sockets-2-spi"></a>Установка службы в списке SPI Windows Sockets 2

-   [**нспинсталлсервицекласс**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspinstallserviceclass)
-   [**нспремовесервицекласс**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspremoveserviceclass)
-   [**нспсетсервице**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspsetservice)

Если требуемый класс службы еще не существует, клиент SPI пространства имен использует [**нспинсталлсервицекласс**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspinstallserviceclass) для установки нового класса службы путем указания имени класса службы, идентификатора GUID для идентификатора класса службы и ряда структур [**всансклассинфо**](/windows/desktop/api/Winsock2/ns-winsock2-wsansclassinfow) . Эти структуры зависят от конкретного пространства имен и предоставляют общие значения, такие как Рекомендуемые номера TCP-портов или идентификаторы NetWare SAP. Класс службы можно удалить путем вызова [**нспремовесервицекласс**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspremoveserviceclass) и указания идентификатора GUID, соответствующего идентификатору класса.

После существования класса службы определенные экземпляры службы могут быть установлены или удалены через [**нспсетсервице**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspsetservice). Эта функция принимает структуру [**всакуерисет**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) в качестве входного параметра вместе с кодом операции и флагами операций. Код операции указывает, выполняется ли установка или удаление службы. Структура **всакуерисет** предоставляет все необходимые сведения о службе, включая идентификатор класса службы, имя службы (для этого экземпляра), применимый идентификатор пространства имен и сведения о протоколе, а также набор транспортных адресов, на который прослушивается служба.

 

 



