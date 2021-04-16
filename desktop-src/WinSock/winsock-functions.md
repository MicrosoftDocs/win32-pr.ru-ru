---
description: В следующем списке приведены краткие описания каждой функции Winsock. Для получения дополнительных сведений о любой функции щелкните имя функции.
ms.assetid: edafb5f9-09fe-4f8e-9651-4002b6f622f4
title: Функции Winsock
ms.topic: article
ms.date: 10/01/2019
ms.openlocfilehash: 9bf2205c970eeaaf4e64867565d58680b28298c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712340"
---
# <a name="winsock-functions"></a>Функции Winsock

В следующем списке приведены краткие описания каждой функции Winsock. Для получения дополнительных сведений о любой функции щелкните имя функции.

| Функция | Описание |
|-|-|
| [**гласит**](/windows/win32/api/Winsock2/nf-winsock2-accept) | Разрешает попыток входящего подключения на сокете. |
| [**акцептекс**](/windows/win32/api/mswsock/nf-mswsock-acceptex) | Принимает новое соединение, возвращает локальный и удаленный адрес и получает первый блок данных, отправленных клиентским приложением. |
| [**выполняется**](/windows/win32/api/winsock/nf-winsock-bind) | Связывает локальный адрес с сокетом. |
| [**функции closesocket**](/windows/win32/api/winsock/nf-winsock-closesocket) | Закрывает существующий сокет. |
| [**соединиться**](/windows/win32/api/Winsock2/nf-winsock2-connect) | Устанавливает соединение с указанным сокетом. |
| [**коннектекс**](/windows/win32/api/Mswsock/nc-mswsock-lpfn_connectex) | Устанавливает соединение с указанным сокетом и при необходимости отправляет данные после установления соединения. Поддерживается только для сокетов, ориентированных на соединение. |
| [**дисконнектекс**](/previous-versions/windows/desktop/legacy/ms737757(v=vs.85)) | Закрывает соединение на сокете и позволяет повторно использовать его. |
| [**енумпротоколс**](/windows/win32/api/Nspapi/nf-nspapi-enumprotocolsa) | Извлекает сведения об указанном наборе сетевых протоколов, активных на локальном узле. |
| [**фриаддринфо**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-freeaddrinfo) | Освобождает сведения об адресах, динамически выделяемые функцией [**функцию getaddrinfo**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) в структурах [**аддринфо**](/windows/win32/api/ws2def/ns-ws2def-addrinfoa) . |
| [**фриаддринфоекс**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-freeaddrinfoex) | Освобождает сведения об адресах, динамически выделяемые функцией [**жетаддринфоекс**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getaddrinfoexa) в структурах [**аддринфоекс**](/windows/win32/api/Ws2def/ns-ws2def-addrinfoexw) . |
| [**фриаддринфов**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-freeaddrinfow) | Освобождает сведения об адресах, динамически выделяемые функцией [**жетаддринфов**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getaddrinfow) в структурах [**аддринфов**](/windows/win32/api/Ws2def/ns-ws2def-addrinfow) . |
| [**ГАИ \_ strerror**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-gai_strerrora) | Помогает при печати сообщений об ошибках на основе ошибок EAI, \_ \* возвращенных функцией [**функцию getaddrinfo**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) . |
| [**жетакцептекссоккаддрс**](/windows/win32/api/mswsock/nf-mswsock-getacceptexsockaddrs) | Анализирует данные, полученные из вызова функции [**акцептекс**](/windows/win32/api/mswsock/nf-mswsock-acceptex) . |
| [**жетаддрессбинаме**](/windows/win32/api/Nspapi/nf-nspapi-getaddressbynamea) | Запрашивает пространство имен или набор пространств имен по умолчанию, чтобы получить сведения об сетевом адресе для указанной сетевой службы. Этот процесс называется разрешением имен служб. Сетевая служба также может использовать функцию для получения сведений о локальном адресе, которые можно использовать с функцией [**BIND**](/windows/win32/api/winsock/nf-winsock-bind) . |
| [**функцию getaddrinfo**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) | Предоставляет независимый от протокола перевод имени узла ANSI в адрес. |
| [**жетаддринфоекс**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getaddrinfoexa) | Обеспечивает независимое от протокола разрешение имен с дополнительными параметрами для определения того, какие поставщики пространства имен должны выполнять запрос. |
| [**жетаддринфоексканцел**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getaddrinfoexcancel) | Отменяет асинхронную операцию функцией [**жетаддринфоекс**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getaddrinfoexa) . |
| [**жетаддринфоексоверлаппедресулт**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getaddrinfoexoverlappedresult) | Возвращает код возврата для структуры **OVERLAPPED** , используемой асинхронной операцией функции [**жетаддринфоекс**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getaddrinfoexa) . |
| [**жетаддринфов**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getaddrinfow) | Предоставляет независимый от протокола перевод из имени узла Юникода в адрес. |
| [**жесостбяддр**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr) | Извлекает сведения об узле, соответствующие сетевому адресу. |
| [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) | Извлекает сведения об узле, соответствующие имени узла из базы данных узла. Не рекомендуется: используйте [**функцию getaddrinfo**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) . |
| [**имя узла**](/windows/win32/api/winsock/nf-winsock-gethostname) | Возвращает стандартное имя узла для локального компьютера. |
| [**жесостнамев**](/windows/win32/api/Winsock2/nf-winsock2-gethostnamew) | Возвращает стандартное имя узла для локального компьютера в виде строки Юникода. |
| [**getipv4sourcefilter**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getipv4sourcefilter) | Извлекает состояние фильтрации многоадресной рассылки для сокета IPv4. |
| [**жетнамебитипе**](/windows/win32/api/Nspapi/nf-nspapi-getnamebytypea) | Извлекает имя сетевой службы для указанного типа службы. |
| [**жетнамеинфо**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) | Обеспечивает разрешение имен с адреса IPv4 или IPv6 на имя узла ANSI и из номера порта в имя службы ANSI. |
| [**жетнамеинфов**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getnameinfow) | Обеспечивает разрешение имен с адреса IPv4 или IPv6 на имя узла в Юникоде и из номера порта в имя службы Юникода. |
| [**жетпирнаме**](/windows/win32/api/winsock/nf-winsock-getpeername) | Извлекает адрес однорангового узла, к которому подключен сокет. |
| [**жетпротобинаме**](/windows/win32/api/winsock/nf-winsock-getprotobyname) | Возвращает сведения о протоколе, соответствующие имени протокола. |
| [**жетпротобинумбер**](/windows/win32/api/winsock/nf-winsock-getprotobynumber) | Извлекает сведения о протоколе, соответствующие номеру протокола. |
| [**жетсервбинаме**](/windows/win32/api/winsock/nf-winsock-getservbyname) | Извлекает сведения о службе, соответствующие имени службы и протоколу. |
| [**жетсервбипорт**](/windows/win32/api/winsock/nf-winsock-getservbyport) | Извлекает сведения о службе, соответствующие порту и протоколу. |
| [**GetService**](/windows/win32/api/Nspapi/nf-nspapi-getservicea) | Извлекает сведения о сетевой службе в контексте набора пространств имен по умолчанию или указанного пространства имен. |
| [**жетсоккнаме**](/windows/win32/api/winsock/nf-winsock-getsockname) | Возвращает локальное имя для сокета. |
| [**жетсоккопт**](/windows/win32/api/winsock/nf-winsock-getsockopt) | Получает параметр сокета. |
| [**жетсаурцефилтер**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getsourcefilter) | Извлекает состояние фильтрации многоадресной рассылки для сокета IPv4 или IPv6. |
| [**GetTypeByName**](/windows/win32/api/Nspapi/nf-nspapi-gettypebynamea) | Извлекает идентификатор GUID типа службы для сетевой службы, заданной по имени. |
| [**хтонд**](/windows/win32/api/Winsock2/nf-winsock2-htond) | Преобразует значение **типа Double** из узла в порядковый байт сети TCP/IP (с обратным порядком байтов). |
| [**хтонф**](/windows/win32/api/Winsock2/nf-winsock2-htonf) | Преобразует значение **float** из узла в порядковый байт сети TCP/IP (с обратным порядком байтов). |
| [**хтонл**](/windows/win32/api/winsock/nf-winsock-htonl) | Преобразует значение **u \_** из узла в порядковый байт сети TCP/IP (с обратным порядком байтов). |
| [**хтонлл**](/windows/win32/api/Winsock2/nf-winsock2-htonll) | Преобразует **Неподписанное значение типа \_ \_ Int64** из узла в порядковый байт сети TCP/IP (с обратным порядком байтов). |
| [**хтонс**](/windows/win32/api/winsock/nf-winsock-htons) | Преобразует **u- \_ короткий** из узла в порядковый байт сети TCP/IP (с обратным порядком байтов). |
| [**INET \_ АДР**](/windows/win32/api/winsock2/nf-winsock2-inet_addr) | Преобразует строку, содержащую адрес протокола Интернета (IPv4), в соответствующий адрес в структуре [**\_ адреса**](/windows/win32/api/winsock2/ns-winsock2-in_addr) . |
| [**INET \_ нтоа**](/windows/win32/api/winsock2/nf-winsock2-inet_ntoa) | Преобразует адрес сети Интернета (IPv4) в строку в формате "Стандартный точечный формат Интернета". |
| [**инетнтоп**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-inetntopw) | Преобразует адрес сети Интернета IPv4 или IPv6 в строку в стандартном формате Интернета. Версия этой функции в формате ANSI — [**inet \_ нтоп**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-inetntopw). |
| [**инетптон**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-inetptonw) | Преобразует сетевой адрес IPv4 или IPv6 в виде стандартной текстовой формы представления в числовой двоичный формат. Версия этой функции в формате ANSI — [**inet \_ птон**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-inetptonw). |
| [**иоктлсоккет**](/windows/win32/api/winsock/nf-winsock-ioctlsocket) | Управляет режимом ввода-вывода сокета. |
| [**слушивают**](/windows/win32/api/Winsock2/nf-winsock2-listen) | Помещает сокет в состояние ожидания входящего подключения. |
| [**нтохд**](/windows/win32/api/Winsock2/nf-winsock2-ntohd) | Преобразует **Неподписанное значение типа \_ \_ Int64** из порядка TCP/IP в сеть для размещения порядка байтов (с прямым порядком байтов для процессоров Intel) и возвращает значение **типа Double**. |
| [**нтохф**](/windows/win32/api/Winsock2/nf-winsock2-ntohf) | Преобразует **Неподписанное значение \_ \_ Int32** из порядка TCP/IP в сеть для размещения порядка байтов (то есть для процессоров Intel с прямым порядком байтов) и возвращает значение **типа float**. |
| [**нтохл**](/windows/win32/api/winsock/nf-winsock-ntohl) | Преобразует протокол u в \_ сети TCP/IP для размещения порядка байтов (который является прямым порядком байтов на процессорах Intel). |
| [**нтохлл**](/windows/win32/api/Winsock2/nf-winsock2-ntohll) | Преобразует **Неподписанное значение типа \_ \_ Int64** из порядка TCP/IP в сеть для размещения порядка байтов (то есть на процессорах Intel с прямым порядком байтов). |
| [**нтохс**](/windows/win32/api/winsock/nf-winsock-ntohs) | Преобразует \_ байты u из сети TCP/IP в порядковый номер размещения в байтах (что является прямым порядком на процессорах Intel). |
| [**полученных**](/windows/win32/api/winsock/nf-winsock-recv) | Получает данные из подключенного или привязанного сокета. |
| [**реквфром**](/windows/win32/api/winsock/nf-winsock-recvfrom) | Получает датаграмму и сохраняет исходный адрес. |
| [**риоклосекомплетионкуеуе**](/previous-versions/windows/desktop/legacy/hh448837(v=vs.85)) | Закрывает существующую очередь завершения, используемую для уведомлений о завершении ввода-вывода, с помощью запросов send и Receive с зарегистрированными расширениями ввода-вывода Winsock. |
| [**риокреатекомплетионкуеуе**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion) | Создает очередь завершения ввода-вывода определенного размера для использования с зарегистрированными расширениями ввода-вывода Winsock. |
| [**риокреатерекуесткуеуе**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riocreaterequestqueue) | Создает зарегистрированный дескриптор сокета ввода-вывода с использованием указанного сокета и очередей завершения ввода-вывода для использования с зарегистрированными расширениями ввода-вывода Winsock. |
| [**риодекуеуекомплетион**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion) | Удаляет записи из очереди завершения ввода-вывода для использования с зарегистрированными расширениями ввода-вывода Winsock. |
| [**риодерегистербуффер**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioderegisterbuffer) | Отменяет регистрацию зарегистрированного буфера, используемого с зарегистрированными расширениями ввода-вывода Winsock. |
| [**рионотифи**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rionotify) | Регистрирует метод для использования в поведении уведомлений с очередью завершения ввода-вывода для использования с зарегистрированными расширениями ввода-вывода Winsock. |
| [**риорецеиве**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioreceive) | Получает сетевые данные по подключенному зарегистрированному сокету ввода-вывода TCP или привязанному зарегистрированному сокету UDP ввода-вывода для использования с зарегистрированными расширениями ввода-вывода Winsock. |
| [**риорецеивикс**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioreceiveex) | Получает сетевые данные по подключенному зарегистрированному сокету ввода-вывода TCP или привязанному зарегистрированному сокету UDP ввода-вывода с дополнительными параметрами для использования с зарегистрированными расширениями ввода-вывода Winsock. |
| [**риорегистербуффер**](/previous-versions/windows/desktop/legacy/hh437199(v=vs.85)) | Регистрирует [**Рио \_ BUFFERID**](rio-bufferid.md), зарегистрированный дескриптор буфера с заданным буфером для использования с зарегистрированными расширениями ввода-вывода Winsock. |
| [**риоресизекомплетионкуеуе**](/previous-versions/windows/desktop/legacy/hh437202(v=vs.85)) | Изменяет размер очереди завершения ввода-вывода так, чтобы она была больше или меньше для использования с зарегистрированными расширениями ввода-вывода Winsock. |
| [**риоресизерекуесткуеуе**](/previous-versions/windows/desktop/legacy/hh437204(v=vs.85)) | Изменяет размер очереди запросов, чтобы она была либо больше, либо меньше для использования с зарегистрированными расширениями ввода-вывода Winsock. |
| [**риосенд**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riosend) | Отправляет сетевые данные на подключенный зарегистрированный сокет ввода-вывода TCP или связанный зарегистрированный сокет UDP ввода-вывода для использования с зарегистрированными расширениями ввода-вывода Winsock. |
| [**риосендекс**](/previous-versions/windows/desktop/legacy/hh437216(v=vs.85)) | Отправляет сетевые данные по подключенному зарегистрированному сокету ввода-вывода TCP или привязанному зарегистрированному сокету UDP ввода-вывода с дополнительными параметрами для использования с зарегистрированными расширениями ввода-вывода Winsock. |
| [**метьте**](/windows/win32/api/Winsock2/nf-winsock2-select) | Определяет состояние одного или нескольких сокетов, в ожидании, если это необходимо, для выполнения синхронного ввода-вывода. |
| [**Отправить**](/windows/win32/api/Winsock2/nf-winsock2-send) | Отправляет данные на подключенный сокет. |
| [**cервера**](/windows/win32/api/winsock/nf-winsock-sendto) | Отправляет данные в определенное место назначения. |
| [**сетаддринфоекс**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-setaddrinfoexa) | Регистрирует имя узла и службы вместе с связанными адресами с конкретным поставщиком пространства имен. |
| [**setipv4sourcefilter**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-setipv4sourcefilter) | Задает состояние фильтрации многоадресной рассылки для сокета IPv4. |
| [**сетсервице**](/windows/win32/api/Nspapi/nf-nspapi-setservicea) | Регистрирует или удаляет из реестра сетевую службу в одном или нескольких пространствах имен. Также может добавлять или удалять тип сетевой службы в одном или нескольких пространствах имен. |
| [**сетсоккетмедиастреамингмоде**](/windows/win32/api/Socketapi/nf-socketapi-setsocketmediastreamingmode) | Указывает, следует ли использовать сеть для передачи мультимедийных данных, требующих качества обслуживания. |
| [**сетсоккопт**](/windows/win32/api/winsock/nf-winsock-setsockopt) | Задает параметр сокета. |
| [**сетсаурцефилтер**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-setsourcefilter) | Задает состояние фильтрации многоадресной рассылки для сокета IPv4 или IPv6. |
| [**закрытия**](/windows/win32/api/winsock/nf-winsock-shutdown) | Отключает отправку или получение на сокете. |
| [**фиксатор**](/windows/win32/api/Winsock2/nf-winsock2-socket) | Создает сокет, привязанный к определенному поставщику услуг. |
| [**TransmitFile**](/windows/win32/api/mswsock/nf-mswsock-transmitfile) | Передает файловые данные через подключенный маркер сокета. |
| [**трансмитпаккетс**](/windows/win32/api/Mswsock/nc-mswsock-lpfn_transmitpackets) | Передает данные в памяти или файловые данные через подключенный сокет. |
| [**всаакцепт**](/windows/win32/api/Winsock2/nf-winsock2-wsaaccept) | Условно принимает соединение на основе возвращаемого значения функции условия, предоставляет спецификации потока качества обслуживания и разрешает передачу данных соединения. |
| [**всааддресстостринг**](/windows/win32/api/Winsock2/nf-winsock2-wsaaddresstostringa) | Преобразует все компоненты структуры [**SOCKADDR**](sockaddr-2.md) в строковое представление адреса, доступное для чтения. |
| [**всаасинкжесостбяддр**](/windows/win32/api/winsock/nf-winsock-wsaasyncgethostbyaddr) | Асинхронно извлекает сведения об узле, соответствующие адресу. |
| [**всаасинкжесостбинаме**](/windows/win32/api/winsock/nf-winsock-wsaasyncgethostbyname) | Асинхронно извлекает сведения об узле, соответствующие имени узла. |
| [**всаасинкжетпротобинаме**](/windows/win32/api/winsock/nf-winsock-wsaasyncgetprotobyname) | Асинхронно извлекает сведения о протоколе, соответствующие имени протокола. |
| [**всаасинкжетпротобинумбер**](/windows/win32/api/winsock/nf-winsock-wsaasyncgetprotobynumber) | Асинхронно извлекает сведения о протоколе, соответствующие номеру протокола. |
| [**всаасинкжетсервбинаме**](/windows/win32/api/winsock/nf-winsock-wsaasyncgetservbyname) | Асинхронно извлекает сведения о службе, соответствующие имени службы и порту. |
| [**всаасинкжетсервбипорт**](/windows/win32/api/winsock/nf-winsock-wsaasyncgetservbyport) | Асинхронно извлекает сведения о службе, соответствующие порту и протоколу. |
| [**всаасинкселект**](/windows/win32/api/winsock/nf-winsock-wsaasyncselect) | Запрашивает уведомление Windows о сетевых событиях для сокета на основе сообщений. |
| [**всаканцеласинкрекуест**](/windows/win32/api/winsock/nf-winsock-wsacancelasyncrequest) | Отменяет незавершенную асинхронную операцию. |
| [**всаклеануп**](/windows/win32/api/winsock/nf-winsock-wsacleanup) | Прекращает использование \_32.DLL Ws2. |
| [**всаклосивент**](/windows/win32/api/Winsock2/nf-winsock2-wsacloseevent) | Закрывает открытый обработчик объекта события. |
| [**всаконнект**](/windows/win32/api/Winsock2/nf-winsock2-wsaconnect) | Устанавливает соединение с другим приложением сокета, обменивается данными и указывает требуемое качество обслуживания на основе указанной структуры [**фловспек**](/windows/win32/api/qos/ns-qos-flowspec) . |
| [**всаконнектбилист**](/windows/win32/api/Winsock2/nf-winsock2-wsaconnectbylist) | Устанавливает соединение с одной из коллекций возможных конечных точек, представленных набором адресов назначения (имен узлов и портов). |
| [**WSAConnectByName**](/windows/win32/api/Winsock2/nf-winsock2-wsaconnectbynamea) | Устанавливает подключение к другому приложению сокета на указанном узле и порту |
| [**всакреативент**](/windows/win32/api/Winsock2/nf-winsock2-wsacreateevent) | Создает новый объект события. |
| [**всаделетесоккетпиртаржетнаме**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-wsadeletesocketpeertargetname) | Удаляет связь между именем однорангового целевого объекта и IP-адресом для сокета. |
| [**всадупликатесоккет**](/windows/win32/api/Winsock2/nf-winsock2-wsaduplicatesocketa) | Возвращает структуру, которую можно использовать для создания нового дескриптора сокета для общего сокета. |
| [**всаенумнамеспацепровидерс**](/windows/win32/api/Winsock2/nf-winsock2-wsaenumnamespaceprovidersa) | Извлекает сведения о доступных пространствах имен. |
| [**всаенумнамеспацепровидерсекс**](/windows/win32/api/Winsock2/nf-winsock2-wsaenumnamespaceprovidersexa) | Извлекает сведения о доступных пространствах имен. |
| [**всаенумнетворкевентс**](/windows/win32/api/Winsock2/nf-winsock2-wsaenumnetworkevents) | Обнаружение вхождений сетевых событий для указанного сокета, очистка записей внутренних сетевых событий и сброс объектов событий (необязательно). |
| [**всаенумпротоколс**](/windows/win32/api/Winsock2/nf-winsock2-wsaenumprotocolsa) | Извлекает сведения о доступных транспортных протоколах. |
| [**всаевентселект**](/windows/win32/api/Winsock2/nf-winsock2-wsaeventselect) | Указывает объект события, который должен быть связан с указанным набором сетевых событий демона "Демон \ \_ xxx". |
| [**\_\_всафдиссет**](/windows/win32/api/winsock/nf-winsock-__wsafdisset) | Указывает, включен ли сокет в набор дескрипторов сокетов. |
| [**всажетфаилконнектоникмперрор**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetfailconnectonicmperror) | Запрашивает состояние параметра [**TCP_FAIL_CONNECT_ON_ICMP_ERROR**](./ipproto-tcp-socket-options.md) сокета. |
| [**всажетикмперроринфо**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsageticmperrorinfo) | Запрашивает исходный адрес ошибки ICMP, полученной на сокете TCP во время настройки подключения. |
| [**всажетипусермту**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetipusermtu) | Извлекает определяемый пользователем IP-уровень MTU для сокета. |
| [**всажетластеррор**](/windows/win32/api/winsock/nf-winsock-wsagetlasterror) | Возвращает состояние ошибки для последней операции, которая завершилась ошибкой. |
| [**всажетоверлаппедресулт**](/windows/win32/api/Winsock2/nf-winsock2-wsagetoverlappedresult) | Возвращает результаты операции перекрытия для указанного сокета. |
| [**всажеткосбинаме**](/windows/win32/api/Winsock2/nf-winsock2-wsagetqosbyname) | Инициализирует структуру [**QoS**](/windows/win32/api/winsock2/ns-winsock2-qos) на основе именованного шаблона или предоставляет буфер для получения перечисления доступных имен шаблонов. |
| [**всажетсервицеклассинфо**](/windows/win32/api/Winsock2/nf-winsock2-wsagetserviceclassinfoa) | Извлекает сведения о классе (схеме), относящиеся к указанному классу службы, из указанного поставщика пространства имен. |
| [**всажетсервицекласснамебиклассид**](/windows/win32/api/Winsock2/nf-winsock2-wsagetserviceclassnamebyclassida) | Возвращает имя службы, связанной с указанным типом. |
| [**всажетудпреквмакскоалесцедсизе**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetudprecvmaxcoalescedsize) | Возвращает максимальный размер полученного Объединенного сообщения для сокета UDP. |
| [**всажетудпсендмессажесизе**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetudpsendmessagesize) | Получает размер сообщения о сегментации для сокета UDP. |
| [**всахтонл**](/windows/win32/api/Winsock2/nf-winsock2-wsahtonl) | Преобразует значение u \_ из байтового порядка узла в сетевой порядок байтов. |
| [**всахтонс**](/windows/win32/api/Winsock2/nf-winsock2-wsahtons) | Преобразует значение u \_ из байтового порядка узлов в сетевой порядок байтов. |
| [**всаимперсонатесоккетпир**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-wsaimpersonatesocketpeer) | Используется для олицетворения субъекта безопасности, соответствующего узлу сокета, для выполнения авторизации на уровне приложения. |
| [**всаинсталлсервицекласс**](/windows/win32/api/Winsock2/nf-winsock2-wsainstallserviceclassa) | Регистрирует схему класса службы в пространстве имен. |
| [**всаиоктл**](/windows/win32/api/Winsock2/nf-winsock2-wsaioctl) | Управляет режимом сокета. |
| [**всажоинлеаф**](/windows/win32/api/Winsock2/nf-winsock2-wsajoinleaf) | Присоединяет конечный узел к сеансу MultiPoint, обменивается данными и указывает требуемое качество обслуживания на основе указанных структур. |
| [**всалукупсервицебегин**](/windows/win32/api/Winsock2/nf-winsock2-wsalookupservicebegina) | Инициирует клиентский запрос, ограниченный сведениями, содержащимися в структуре [**всакуерисет**](/windows/win32/api/Winsock2/ns-winsock2-wsaquerysetw) . |
| [**всалукупсервицеенд**](/windows/win32/api/Winsock2/nf-winsock2-wsalookupserviceend) | Освобождает маркер, используемый предыдущими вызовами [**всалукупсервицебегин**](/windows/win32/api/Winsock2/nf-winsock2-wsalookupservicebegina) и [**всалукупсервиценекст**](/windows/win32/api/Winsock2/nf-winsock2-wsalookupservicenexta). |
| [**всалукупсервиценекст**](/windows/win32/api/Winsock2/nf-winsock2-wsalookupservicenexta) | Получите запрошенные сведения о службе. |
| [**всанспиоктл**](/windows/win32/api/Winsock2/nf-winsock2-wsanspioctl) | Разработчики делают вызовы контроля ввода-вывода в зарегистрированное пространство имен. |
| [**всантохл**](/windows/win32/api/Winsock2/nf-winsock2-wsantohl) | Преобразует значение u \_ длинного из сетевого байтового порядка в байтовый порядок размещения. |
| [**всантохс**](/windows/win32/api/Winsock2/nf-winsock2-wsantohs) | Преобразует значение u- \_ короткий из сетевого байтового формата в порядок размещения байтов. |
| [**всаполл**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) | Определяет состояние одного или нескольких сокетов. |
| [**всапровидерконфигчанже**](/windows/win32/api/Winsock2/nf-winsock2-wsaproviderconfigchange) | Уведомляет приложение об изменении конфигурации поставщика. |
| [**всакуерисоккетсекурити**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-wsaquerysocketsecurity) | Запрашивает сведения о безопасности, применяемые к соединению на сокете. |
| [**всарекв**](/windows/win32/api/Winsock2/nf-winsock2-wsarecv) | Получает данные из подключенного сокета. |
| [**всареквдисконнект**](/windows/win32/api/Winsock2/nf-winsock2-wsarecvdisconnect) | Прекращает прием на сокете и получает данные об отключении, если сокет ориентирован на соединение. |
| [**всареквекс**](/windows/win32/api/mswsock/nf-mswsock-wsarecvex) | Получает данные из подключенного сокета. |
| [**всареквфром**](/windows/win32/api/Winsock2/nf-winsock2-wsarecvfrom) | Получает датаграмму и сохраняет исходный адрес. |
| [**LPFN_WSARECVMSG (Всареквмсг)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) | Получает данные и дополнительные сведения об элементе управления от подключенных и неподключенных сокетов. |
| [**всаремовесервицекласс**](/windows/win32/api/Winsock2/nf-winsock2-wsaremoveserviceclass) | Окончательно удаляет схему класса службы из реестра. |
| [**всаресетевент**](/windows/win32/api/Winsock2/nf-winsock2-wsaresetevent) | Сбрасывает состояние указанного объекта события на несигнальное. |
| [**всаревертимперсонатион**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-wsarevertimpersonation) | Завершает олицетворение однорангового узла сокета. |
| [**всасенд**](/windows/win32/api/Winsock2/nf-winsock2-wsasend) | Отправляет данные на подключенный сокет. |
| [**всасенддисконнект**](/windows/win32/api/Winsock2/nf-winsock2-wsasenddisconnect) | Инициирует завершение соединения для сокета и отправляет данные отключения. |
| [**всасендмсг**](/windows/win32/api/winsock2/nf-winsock2-wsasendmsg) | Отправляет данные и дополнительные сведения об элементе управления с подключенных и неподключенных сокетов. |
| [**всасендто**](/windows/win32/api/Winsock2/nf-winsock2-wsasendto) | Отправляет данные в определенное место назначения, используя перекрывающиеся операции ввода-вывода, где это применимо. |
| [**всасетевент**](/windows/win32/api/Winsock2/nf-winsock2-wsasetevent) | Задает сигнальное состояние указанного объекта события. |
| [**всасетфаилконнектоникмперрор**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetfailconnectonicmperror) | Задает состояние параметра [**TCP_FAIL_CONNECT_ON_ICMP_ERROR**](./ipproto-tcp-socket-options.md) сокета. |
| [**всасетипусермту**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetipusermtu) | Устанавливает определяемый пользователем IP-уровень MTU на сокете. |
| [**всасетластеррор**](/windows/win32/api/winsock/nf-winsock-wsasetlasterror) | Задает код ошибки. |
| [**всасетсервице**](/windows/win32/api/Winsock2/nf-winsock2-wsasetservicea) | Регистрирует или удаляет из реестра экземпляр службы в одном или нескольких пространствах имен. |
| [**всасетсоккетпиртаржетнаме**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketpeertargetname) | Используется для указания имени однорангового целевого объекта (SPN), соответствующего IP-адресу однорангового узла. Это целевое имя должно быть задано клиентскими приложениями для безопасного определения однорангового узла, который должен пройти проверку подлинности. |
| [**всасетсоккетсекурити**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketsecurity) | Включает и применяет безопасность для сокета. |
| [**всасетудпреквмакскоалесцедсизе**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetudprecvmaxcoalescedsize) | Задает максимальный размер набора Объединенных сообщений для сокета UDP. |
| [**всасетудпсендмессажесизе**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetudpsendmessagesize) | Задает размер сообщения сегментации для сокета UDP. |
| [**всасоккет**](/windows/win32/api/Winsock2/nf-winsock2-wsasocketa) | Создает сокет, привязанный к определенному поставщику транспортной службы. |
| [**Сбой WSAStartup**](/windows/win32/api/winsock/nf-winsock-wsastartup) | Инициирует использование WS2 \_32.DLL процессом. |
| [**всастрингтоаддресс**](/windows/win32/api/Winsock2/nf-winsock2-wsastringtoaddressa) | Преобразует числовую строку в структуру [**SOCKADDR**](sockaddr-2.md) . |
| [**всаваитформултипливентс**](/windows/win32/api/Winsock2/nf-winsock2-wsawaitformultipleevents) | Возвращает значение, если один или все указанные объекты событий находятся в сигнальном состоянии или когда истечет интервал времени ожидания. |
