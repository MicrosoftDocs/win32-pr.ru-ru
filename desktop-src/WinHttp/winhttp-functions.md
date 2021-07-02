---
description: В этом разделе определяются функции, предоставляемые WinHTTP.
ms.assetid: dcb56d5d-ed0d-49bb-95bf-940a49c033f1
title: Функции WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41e45289230c1cc22a7f8799dfbbe1dafddccf38
ms.sourcegitcommit: 8e3d8594fa073a9c43eb5dcc7babea03ea30f10f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/01/2021
ms.locfileid: "113174972"
---
# <a name="winhttp-functions"></a>Функции WinHTTP

Службы WinHTTP предоставляют следующие функции.

<dl> <dt>

[**винхттпаддрекуессеадерс**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)
</dt> <dd>

Добавляет один или несколько заголовков HTTP-запроса в обработчик HTTP-запроса.

</dd> <dt>

[**винхттпаддрекуессеадерсекс**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheadersex)
</dt> <dd>

Добавляет один или несколько заголовков HTTP-запроса в обработчик HTTP-запросов, что позволяет использовать отдельные строки имени и значения.

</dd> <dt>

[**винхттпчеккплатформ**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcheckplatform)
</dt> <dd>

Определяет, поддерживается ли в WinHTTP текущая платформа.

</dd> <dt>

[**WinHttpCloseHandle**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpclosehandle)
</dt> <dd>

Закрывает один [хинтернет](hinternet-handles-in-winhttp.md) -маркер.

</dd> <dt>

[**винхттпконнект**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect)
</dt> <dd>

Указывает начальный целевой сервер HTTP-запроса.

</dd> <dt>

[**винхттпкраккурл**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl)
</dt> <dd>

Разделяет URL-адрес на части его компонентов, например имя узла и путь.

</dd> <dt>

[**винхттпкреатепроксиресолвер**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateproxyresolver)
</dt> <dd>

Создает маркер для использования [**винхттпжетпроксифорурлекс**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex).

</dd> <dt>

[**винхттпкреатеурл**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl)
</dt> <dd>

Создает URL-адрес из частей компонента, например имя узла и путь.

</dd> <dt>

[**винхттпдетектаутопроксиконфигурл**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpdetectautoproxyconfigurl)
</dt> <dd>

Поиск URL-адреса для файла автоматической настройки прокси-сервера (PAC). Эта функция сообщает URL-адрес файла PAC, но не скачивает файл.

</dd> <dt>

[**винхттпфрипроксиресулт**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpfreeproxyresult)
</dt> <dd>

Освобождает данные, полученные из предыдущего вызова [**винхттпжетпроксиресулт**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult).

</dd> <dt>

[**винхттпфрикуериконнектионграупресулт**](/windows/win32/api/Winhttp/nf-winhttp-winhttpfreequeryconnectiongroupresult)
</dt> <dd>

Освобождает память, выделенную предыдущим вызовом [винхттпкуериконнектионграуп](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryconnectiongroup).

</dd> <dt>

[**винхттпжетдефаултпроксиконфигуратион**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetdefaultproxyconfiguration)
</dt> <dd>

Извлекает конфигурацию прокси WinHTTP по умолчанию из реестра.

</dd> <dt>

[**винхттпжетиепроксиконфигфоркуррентусер**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser)
</dt> <dd>

Получает конфигурацию прокси-сервера Internet Explorer (IE) для текущего пользователя.

</dd> <dt>

[**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl)
</dt> <dd>

Получает сведения о прокси-сервере для указанного URL-адреса.

</dd> <dt>

[**винхттпжетпроксифорурлекс**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex)
</dt> <dd>

Получает сведения о прокси-сервере для указанного URL-адреса.

</dd> <dt>

[**винхттпжетпроксиресулт**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult)
</dt> <dd>

Получает результаты вызова [**винхттпжетпроксифорурлекс**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex).

</dd> <dt>

[**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen)
</dt> <dd>

Инициализирует использование приложением функций WinHTTP.

</dd> <dt>

[**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)
</dt> <dd>

Создает обработчик HTTP-запроса.

</dd> <dt>

[**винхттпкуеряуссчемес**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes)
</dt> <dd>

Возвращает схемы авторизации, поддерживаемые сервером.

</dd> <dt>

[**винхттпкуериконнектионграуп**](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryconnectiongroup)
</dt> <dd>

Извлекает описание текущего состояния соединений WinHttp.

</dd> <dt>

[**WinHttpQueryDataAvailable**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable)
</dt> <dd>

Возвращает число байтов данных, которые сразу же читаются с помощью [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata).

</dd> <dt>

[**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders)
</dt> <dd>

Получает сведения о заголовке, связанные с HTTP-запросом.

</dd> <dt>

[**винхттпкуерихеадерсекс**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheadersex)
</dt> <dd>

Получает сведения о заголовке, связанные с HTTP-запросом; предоставляет способ получения проанализированных строк имени и значения заголовка.

</dd> <dt>

[**винхттпкуерйоптион**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption)
</dt> <dd>

Запрашивает параметр Интернета для указанного маркера.

</dd> <dt>

[**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata)
</dt> <dd>

Считывает данные из маркера, открытого функцией [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) .

</dd> <dt>

[**винхттпреаддатаекс**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddataex)
</dt> <dd>

Считывает данные из маркера, открытого функцией [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) .

</dd> <dt>

[**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse)
</dt> <dd>

Завершает HTTP-запрос, инициированный [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).

</dd> <dt>

[**винхттпресетаутопрокси**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpresetautoproxy)
</dt> <dd>

Сбрасывает параметр Auto-proxy.

</dd> <dt>

[**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)
</dt> <dd>

Отправляет указанный запрос на HTTP-сервер.

</dd> <dt>

[**винхттпсеткредентиалс**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials)
</dt> <dd>

Передает на сервер необходимые учетные данные авторизации.

</dd> <dt>

[**винхттпсетдефаултпроксиконфигуратион**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetdefaultproxyconfiguration)
</dt> <dd>

Задает конфигурацию WinHTTP прокси по умолчанию в реестре.

</dd> <dt>

[**винхттпсетоптион**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption)
</dt> <dd>

Задает параметр Интернета.

</dd> <dt>

[**WinHttpSetStatusCallback**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetstatuscallback)
</dt> <dd>

Настраивает функцию обратного вызова, которую WinHTTP может вызвать во время выполнения операции.

</dd> <dt>

[**винхттпсеттимеаутс**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsettimeouts)
</dt> <dd>

Задает различные тайм-ауты, связанные с HTTP-транзакциями.

</dd> <dt>

[**винхттптимефромсистемтиме**](/windows/desktop/api/Winhttp/nf-winhttp-winhttptimefromsystemtime)
</dt> <dd>

Форматирует дату и время согласно спецификации HTTP версии 1,0.

</dd> <dt>

[**винхттптиметосистемтиме**](/windows/desktop/api/Winhttp/nf-winhttp-winhttptimetosystemtime)
</dt> <dd>

Принимает строку времени или даты HTTP и преобразует ее в структуру [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) .

</dd> <dt>

[**WinHttpWriteData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpwritedata)
</dt> <dd>

Записывает данные запроса на HTTP-сервер.

</dd> <dt>

[**винхттпвебсоккетклосе**](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketclose)
</dt> <dd>

Закрывает соединение WebSocket.

</dd> <dt>

[**винхттпвебсоккеткомплетеупграде**](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketcompleteupgrade)
</dt> <dd>

Завершает подтверждение соединения WebSocket, запущенное [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).

</dd> <dt>

[**винхттпвебсоккеткуериклосестатус**](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketqueryclosestatus)
</dt> <dd>

Возвращает состояние закрытия, отправленное сервером.

</dd> <dt>

[**винхттпвебсоккетрецеиве**](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketreceive)
</dt> <dd>

Получает данные из соединения WebSocket.

</dd> <dt>

[**винхттпвебсоккетсенд**](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketsend)
</dt> <dd>

Отправляет данные через соединение WebSocket.

</dd> <dt>

[**винхттпвебсоккетшутдовн**](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketshutdown)
</dt> <dd>

Отправляет закрывающий кадр в соединение WebSocket.

</dd> </dl>


