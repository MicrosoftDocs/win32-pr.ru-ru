---
title: Bluetooth и Всасетсервице
description: Bluetooth использует функцию Всасетсервице для регистрации или удаления экземпляра службы в пространстве имен Bluetooth (NS \_ БС) из реестра.
ms.assetid: 71c5ed9c-fade-4d15-848e-eb810ad4cbb2
keywords:
- Bluetooth Bluetooth
- Всасетсервице Bluetooth
- Bluetooth и Всасетсервице Bluetooth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70399b73bf24477ee1a0ec0c7585a9f46b7657ef
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104487785"
---
# <a name="bluetooth-and-wsasetservice"></a>Bluetooth и Всасетсервице

Bluetooth использует функцию [**всасетсервице**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) для регистрации или удаления экземпляра службы в пространстве имен Bluetooth (NS \_ БС) из реестра. Маркер, возвращаемый этой операцией, может использоваться только для удаления службы.

Bluetooth имеет два средства рекламы служб, использующих функцию [**всасетсервице**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) :

-   В приложении может быть объявлена простая запись службы SDP для Bluetooth, созданная на основе стандартных членов в структуре [**всакуерисет**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) .
-   В приложении может быть объявлена собственная запись SDP для Bluetooth путем передачи структуры [**службы БС \_ Set \_**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service) в элемент **лпблоб** структуры [**всакуерисет**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) . Это более сложный подход.

> [!Note]  
> Записи SDP, объявленные [**всасетсервице**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) , не сохраняются после завершения процесса, который их опубликовал.

 

Использование [**всасетсервице**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) с Bluetooth имеет следующие требования.

-   Параметр *лпксрегинфо* — это адрес структуры [**всакуерисет**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) , подрегистрируемой.
-   Параметр *ессоператион* является перечислением, которое содержит одну из операций, показанных в следующей таблице.



| Значение                  | Описание                                                                                |
|------------------------|--------------------------------------------------------------------------------------------|
| РНРСЕРВИЦЕ \_ регистр   | Начинает объявлять службу для запросов удаленных радиостанций с помощью протокола Bluetooth SDP. |
| РНРСЕРВИЦЕ \_ Отмена регистрации | Недопустимый. Возвращает ошибку.                                                               |
| РНРСЕРВИЦЕ \_ Удаление     | Останавливает объявление службы.                                                             |



 

> [!Note]  
> Дескрипторы служб, обнаруженные во время вызова [**всалукупсервицебегин**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) или [**всалукупсервиценекст**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) , несовместимы с \_ операцией удаления рнрсервице.

 

-   Параметр *двконтролфлагс* зарезервирован и должен быть равен нулю.

Дополнительные сведения и список параметров сокетов Bluetooth см. в разделе [Параметры Bluetooth и сокета](bluetooth-and-socket-options.md).

## <a name="related-topics"></a>См. также

<dl> <dt>

[Сокеты Windows](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> </dl>

 

 