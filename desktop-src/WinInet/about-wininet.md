---
title: О команде WinINet
description: интерфейс прикладного программирования (API) Windows интернета (WinINet) позволяет приложению взаимодействовать с протоколами FTP и HTTP для доступа к интернет-ресурсам.
ms.assetid: 0a06f2af-957a-4dff-a8cc-187370181b5c
keywords:
- О команде WinINet WinINet
- WinINet WinINet, сведения
- WinINet WinINet, начальная страница
- Windows Интернет WinINet
- интернет, Windows internet WinINet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be38840c33735a1e064e9bdc5e044651130d6e15a6fe22d004a2e8d7c29bf140
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051872"
---
# <a name="about-wininet"></a>О команде WinINet

> [!NOTE]
> для контейнеров приложений с Windows 10 версия 1709, HTTP/2 (см. [RFC7540](https://tools.ietf.org/html/rfc7540)) включена по умолчанию.

интерфейс прикладного программирования (API) Windows интернета (WinINet) позволяет приложению взаимодействовать с протоколами FTP и HTTP для доступа к интернет-ресурсам. По мере развития стандартов эти функции обрабатывают изменения в базовых протоколах, позволяя им поддерживать единообразное поведение.

**Windows XP и Windows Server 2003 R2 и более ранних версий:** Также включены приложения для взаимодействия с Gopher.

Дополнительные сведения см. в разделе:

-   [WinINet и WinHTTP](wininet-vs-winhttp.md)
-   [Дескрипторы ХИНТЕРНЕТ](appendix-a-hinternet-handles.md)
-   [Поддержка протокола IP версии 6](ip-version-6-support.md)
-   [\_Кодировка содержимого](content-encoding.md)
-   [Кэширование](caching.md)
-   [Общие функции](common-functions.md)
-   [Сеансы FTP](ftp-sessions.md)
-   [HTTP-сеансы](http-sessions.md)
-   [Файлы cookie HTTP](http-cookies.md)
-   [Асинхронная операция](asynchronous-operation.md)
-   [Обработка проверки подлинности](handling-authentication.md)
-   [Обработка указателей универсальных ресурсов](handling-uniform-resource-locators.md)
-   [Рекомендации по безопасности \_](security-guidelines.md)

## <a name="internet-protocols"></a>Протоколы Интернета

Два основных протокола Интернета — FTP и HTTP. Дополнительные сведения об этих протоколах см. в документах RFC (запрос комментариев) для FTP и HTTP:

-   [RFC 959](https://www.ietf.org/rfc/rfc0959.txt), *протокол FTP (FTP)*.
-   [RFC 1945](ftp://ftp.isi.edu/in-notes/rfc1945.txt), *протокол гипертекста-HTTP/1.0*.
-   [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt), *протокол HTTP/1.1*.

> [!NOTE]  
> (Эти ресурсы могут быть недоступны в некоторых языках и странах.)

**Windows XP и Windows Server 2003 R2 и более ранних версий:** Также поддерживается протокол Gopher. См. [RFC 1436](https://www.ietf.org/rfc/rfc1436.txt), *Протокол Интернета Gopher*.
