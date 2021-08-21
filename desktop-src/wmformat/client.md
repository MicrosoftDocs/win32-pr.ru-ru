---
title: ведение журнала клиента (пакет SDK для Windows Media Format 11)
description: сведения о ведении журнала клиента для Windows пакета SDK для формата мультимедиа 11. Ведение журнала позволяет серверу мультимедиа отвести наблюдение за активностью клиентов, подключающихся к нему.
ms.assetid: 3e0d0fea-4370-41f8-b461-73a37de8d8bc
keywords:
- Windows Пакет SDK для формата мультимедиа, ведение журнала клиента
- Windows Пакет SDK для формата мультимедиа, ведение журнала
- Расширенный формат систем (ASF), ведение журнала клиента
- ASF (Расширенный системный формат), ведение журнала клиента
- Расширенный формат систем (ASF), ведение журнала
- ASF (Расширенный системный формат), ведение журнала
- ведение журнала клиента
- Регистрация клиентов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 460058d6ad4009fab301c6ce322df3144bdd0e5d9bb4732d54126f7675cd9e2a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119028032"
---
# <a name="client-logging-windows-media-format-11-sdk"></a>ведение журнала клиента (пакет SDK для Windows Media Format 11)

Когда объект чтения считывает данные с сервера, он отправляет данные журнала на сервер. Поставщики содержимого обычно используют эти сведения для измерения качества обслуживания, создания сведений о выставлении счетов или объявления. Данные ведения журнала не содержат персональных данных.

Приложение может указать некоторую информацию, которая заносится в журнал, вызвав метод [**ивмреадерадванцед:: SetClientInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setclientinfo) для объекта Reader. Например, можно указать строку агента пользователя, имя приложения проигрывателя или веб-страницу, на которой размещен проигрыватель.

Данные журнала включают идентификатор GUID, который идентифицирует сеанс. По умолчанию средство чтения создает идентификатор анонимного сеанса. При необходимости модуль чтения может вместо этого отправить идентификатор, однозначно определяющий текущего пользователя. Чтобы включить эту функцию, вызовите метод [**IWMReaderAdvanced2:: сетлогклиентид**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setlogclientid) со значением **true**.

Можно настроить объект модуля чтения для отправки сведений о ведении журнала на другой сервер в дополнение к исходному серверу. Для этого вызовите метод [**ивмреадернетворкконфиг:: аддлоггингурл**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-addloggingurl) с URL-адресом сервера. Этот URL-адрес должен указывать на скрипт или исполняемый файл, который может выполнять запросы HTTP GET и POST. Для получения данных журнала можно использовать агент многоадресной рассылки и агента объявления журналов (wmsiislog.dll) или написать пользовательский скрипт ASP или CGI.

> [!Note]  
> Те же функциональные возможности можно получить, создав список воспроизведения на стороне сервера с атрибутом **логурл** .

 

Когда объект модуля чтения отправляет журнал, он выполняет следующие действия:

1.  Отправляет на сервер пустой запрос GET.
2.  Анализирует ответ сервера на наличие одной из следующих строк:
    -   `<body><h1>NetShow ISAPI Log Dll</h1>`
    -   `<body><h1>WMS ISAPI Log Dll/0.0.0.0</h1>` где "0.0.0.0" — любой допустимый номер версии.
3.  Отправляет запрос POST со сведениями журнала.

В следующем коде показан пример скрипта ASP, который получает сведения о ведении журнала и записывает их в файл:


```
<html>
<body>
<h1>WMS ISAPI Log Dll/9.00.00.00.00</h1>
<%@ Language=VBScript %>
<%
  Dim temp, i, post, file, fso

  ' Convert the binary data to a string.
  For i = 1 To Request.TotalBytes
    temp = Request.BinaryRead(1)
    pose = pose & Chr(AscB(temp))
  Next

  Set fso = createobject("Scripting.FileSystemObject")
  Set file = fso.OpenTextFile("C:\log.txt", 8, TRUE)

  file.writeline Now
  file.writeline post
  file.writeBlankLines 2 
%>
</body>
</html>
```



Для получения сведений о ведении журнала можно указать несколько серверов. просто вызовите **аддлоггингурл** один раз с каждым URL-адресом. Чтобы очистить список серверов, которые получают журналы, вызовите метод [**ивмреадернетворкконфиг:: ресетлоггингурллист**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-resetloggingurllist) .

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**Реализация функций сети**](implementing-network-functionality.md)
</dt> <dt>

[**Интерфейс Ивмреадерадванцед**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced)
</dt> <dt>

[**Интерфейс IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2)
</dt> </dl>

 

 




