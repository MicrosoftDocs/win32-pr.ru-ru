---
description: Некоторые параметры сокетов для сокетов Windows Sockets 2 приведены в следующей таблице.
ms.assetid: 6731d27c-fb7d-421a-badf-0cad6a4712ea
title: Параметры сокета и IOCTL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 472d37bd8d2d97eead66d7c9d2319e57fc5dafde
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712536"
---
# <a name="socket-options-and-ioctls"></a>Параметры сокета и IOCTL

Некоторые параметры сокетов для сокетов Windows Sockets 2 приведены в следующей таблице. Более подробные сведения приведены в разделе 4 раздела [**вспжетсоккопт**](/previous-versions/windows/hardware/network/ff566292(v=vs.85)) and/or [**вспсетсоккопт**](/previous-versions/windows/hardware/network/ff566318(v=vs.85)). Существуют другие новые параметры сокета, относящиеся к протоколу, которые можно найти в Protocol-Specific приложении. Полный список [**параметров сокета**](socket-options.md) для сокетов Windows можно найти в справочнике по Winsock.

Общие сведения о некоторых параметрах WinSock ioctl см. в разделе [Общие сведения о коде операций сокета ioctl](summary-of-socket-ioctl-opcodes-2.md). Полный список [**Winsock ioctl**](winsock-ioctls.md) можно найти в справочнике по Winsock.

## <a name="summary-of-common-socket-options"></a>Сводка общих параметров сокета

Поставщик службы Winsock должен распознать все эти параметры, а (для [**вспжетсоккопт**](/previous-versions/windows/hardware/network/ff566292(v=vs.85))) возвращать значения правдоподобные для каждого из них. Значение по умолчанию для каждого параметра показано в следующей таблице.

Значение

Тип

Значение

Значение по умолчанию

Примечание

<span id="SO_ACCEPTCONN"></span><span id="so_acceptconn"></span>Итак, \_ акцептконн

BOOL

Сокет прослушивается.

Значение FALSE, если не выполнено [**всплистен**](/previous-versions/windows/hardware/network/ff566297(v=vs.85)) .

<span id="SO_BROADCAST"></span><span id="so_broadcast"></span>\_вещание

BOOL

Сокет настроен для передачи и получения широковещательных сообщений.

FALSE

<span id="SO_DEBUG"></span><span id="so_debug"></span>Итак, \_ Отладка

BOOL

Отладка включена.

FALSE

сохранении

<span id="SO_DONTLINGER"></span><span id="so_dontlinger"></span>Итак, \_ донтлинжер

BOOL

Если задано значение true, \_ параметр so-on отключен.

true

<span id="SO_DONTROUTE"></span><span id="so_dontroute"></span>Итак, \_ донтрауте

BOOL

Маршрутизация отключена. Выполняется успешно, но пропускается на \_ сокетах AF inet; сбой в \_ сокетах INET6 с [всаенопротупт](windows-sockets-error-codes-2.md). Не поддерживается на сокетах ATM (приводит к ошибке).

FALSE

сохранении

<span id="SO_ERROR"></span><span id="so_error"></span>\_Ошибка

INT

Извлекает состояние ошибки и очищается.

0

<span id="SO_GROUP_ID"></span><span id="so_group_id"></span>так \_ что \_ идентификатор группы

GROUP

Зарезервировано.

NULL

Только получение

<span id="SO_GROUP_PRIORITY"></span><span id="so_group_priority"></span>Итак \_ , \_ приоритет группы

INT

Зарезервировано.

0

[**Итак, \_ KeepAlive**](so-keepalive.md)

BOOL

Проверку активности отправляются. Не поддерживается на сокетах ATM (приводит к ошибке).

FALSE

сохранении

<span id="SO_LINGER"></span><span id="so_linger"></span>т. д. \_

Структура — ожидание

Возвращает текущие параметры "ожидание".

l \_ онофф равен 0

<span id="SO_MAX_MSG_SIZE"></span><span id="so_max_msg_size"></span>\_максимальный \_ размер сообщения \_

INT

Максимальный исходящий размер сообщения для типов сокетов сообщений. Для определения максимального размера входящего сообщения нет необходимости. Не имеет смысла для ориентированных на поток сокетов.

Зависит от реализации

Только получение

<span id="SO_OOBINLINE"></span><span id="so_oobinline"></span>Итак, \_ убинлине

BOOL

Данные OOB получаются в потоке обычных данных.

FALSE

<span id="SO_PROTOCOL_INFOW"></span><span id="so_protocol_infow"></span>\_инфов протокола \_

[ **\_ сведения о структуре всапротокол**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa)

Описание протокола для протокола, привязанного к этому сокету.

Зависит от протокола

Только получение

<span id="SO_RCVBUF"></span><span id="so_rcvbuf"></span>Итак, \_ рквбуф

INT

Общее количество буферных пространств сокета, зарезервированных для получения. Это не связано с \_ максимальным \_ размером сообщения \_ и не обязательно соответствует размеру окна приема TCP.

Зависит от реализации

сохранении

<span id="SO_REUSEADDR"></span><span id="so_reuseaddr"></span>Итак, \_ реусеаддр

BOOL

Адрес, к которому привязан этот сокет, может использоваться другими пользователями. Неприменимо к сокетам ATM.

FALSE

<span id="SO_SNDBUF"></span><span id="so_sndbuf"></span>Итак, \_ сндбуф

INT

Общее количество буферных пространств сокета, зарезервированных для отправки. Это не связано с \_ максимальным \_ размером сообщения \_ и не обязательно соответствует размеру окна TCP-отправки.

Зависит от реализации

сохранении

<span id="SO_TYPE"></span><span id="so_type"></span>Поэтому \_ тип

INT

Тип сокета (например, \_ поток Сокк).

Как создано через сокет.

<span id="PVD_CONFIG"></span><span id="pvd_config"></span>\_Конфигурация ПВД

знак FAR \*

Объект структуры непрозрачных данных, содержащий сведения о конфигурации поставщика услуг.

Зависит от реализации

<span id="TCP_NODELAY"></span><span id="tcp_nodelay"></span>\_Задержка TCP

BOOL

Отключить алгоритм Nagle для отправки объединенных пакетов.

Зависит от реализации

(i) поставщик услуг может автоматически игнорировать этот параметр в [**вспсетсоккопт**](/previous-versions/windows/hardware/network/ff566318(v=vs.85)) и вернуть значение константы для [**вспжетсоккопт**](/previous-versions/windows/hardware/network/ff566292(v=vs.85)), либо может принимать значение для **вспсетсоккопт** и возвращать соответствующее значение в **вспжетсоккопт** без использования значения каким-либо образом.



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[**Параметры сокета**](socket-options.md)
</dt> <dt>

[**\_Параметры сокета сокета Sol**](sol-socket-socket-options.md)
</dt> <dt>

[**\_Параметры TCP-сокета иппрото**](ipproto-tcp-socket-options.md)
</dt> <dt>

[**\_Параметры сокета UDP иппрото**](ipproto-udp-socket-options.md)
</dt> <dt>

[**Winsock IOCTL**](winsock-ioctls.md)
</dt> </dl>

 

 
