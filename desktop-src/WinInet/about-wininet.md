---
title: О команде WinINet
description: Прикладной программный интерфейс (API) Windows Internet (WinINet) позволяет приложению взаимодействовать с протоколами FTP и HTTP для доступа к Интернет-ресурсам.
ms.assetid: 0a06f2af-957a-4dff-a8cc-187370181b5c
keywords:
- О команде WinINet WinINet
- WinINet WinINet, сведения
- WinINet WinINet, начальная страница
- Windows Internet WinINet
- Интернет, Windows Internet WinINet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4513e5c3912a483fd4dbef96f452c5712717c8a5
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/20/2020
ms.locfileid: "103987232"
---
# <a name="about-wininet"></a>О команде WinINet

> [!NOTE]
> Для контейнеров приложений, начиная с Windows 10, версия 1709, HTTP/2 (см. [RFC7540](https://tools.ietf.org/html/rfc7540)) включена по умолчанию.

Прикладной программный интерфейс (API) Windows Internet (WinINet) позволяет приложению взаимодействовать с протоколами FTP и HTTP для доступа к Интернет-ресурсам. По мере развития стандартов эти функции обрабатывают изменения в базовых протоколах, позволяя им поддерживать единообразное поведение.

**Windows XP и Windows Server 2003 R2 и более ранних версий:** Также включены приложения для взаимодействия с Gopher.

Дополнительные сведения можно найти в разделе

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
