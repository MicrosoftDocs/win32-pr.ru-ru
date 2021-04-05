---
description: Службы Microsoft Windows HTTP (WinHTTP) используют дескрипторы для наблюдения за параметрами и сведениями, необходимыми при использовании протокола HTTP.
ms.assetid: 0bd82860-1347-40c8-ae77-c4d865c109be
title: Дескрипторы ХИНТЕРНЕТ в WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf374675ad6f2114dd48e0a3ff1db50cd0dd7f9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104559334"
---
# <a name="hinternet-handles-in-winhttp"></a>Дескрипторы ХИНТЕРНЕТ в WinHTTP

Службы Microsoft Windows HTTP (WinHTTP) используют дескрипторы для наблюдения за параметрами и сведениями, необходимыми при использовании протокола HTTP. Каждый обработчик сохраняет информацию, относящуюся к сеансу HTTP, соединению с HTTP-сервером или определенному ресурсу. В этом разделе описываются различные типы дескрипторов, соглашения об именовании для этих дескрипторов и их иерархическая структура.

-   [О дескрипторах ХИНТЕРНЕТ](#about-hinternet-handles)
-   [Дескрипторы именования](#naming-handles)
-   [Иерархия маркеров](#handle-hierarchy)
-   [Объяснение иерархии маркеров](#explanation-of-the-handle-hierarchy)

## <a name="about-hinternet-handles"></a>О дескрипторах ХИНТЕРНЕТ

Дескрипторы, создаваемые и используемые WinHTTP, называются дескрипторами **хинтернет** . Функции WinHTTP возвращают дескрипторы **хинтернет** , которые не взаимозаменяемы с другими дескрипторами, поэтому их нельзя использовать с такими функциями, как [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) или [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle). Аналогично, другие дескрипторы нельзя использовать с функциями WinHTTP. Например, маркер, возвращаемый [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) , не может быть передан в [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata). Эти дескрипторы **хинтернет** не могут быть закрыты, пока выполняется вызов API, использующий дескриптор. Чтобы избежать состояния гонки, приложения должны защищать обработчик и предотвращать его закрытие до тех пор, пока выполняется вызов API.

Функции Microsoft Win32 Интернета (WinInet) также используют дескрипторы **хинтернет** . Однако дескрипторы, используемые в функциях WinInet, не могут быть взаимозаменяемыми с дескрипторами, используемыми в функциях WinHTTP. Дополнительные сведения о WinInet см. в разделе [About WinInet](/windows/desktop/WinInet/about-wininet).

Функция [**WinHttpCloseHandle**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpclosehandle) закрывает дескрипторы WinHTTP **хинтернет** .

## <a name="naming-handles"></a>Дескрипторы именования

В документации по WinHTTP описаны функции в интерфейсе прикладного программирования (API) и примеры кода, демонстрирующие создание и использование различных типов дескрипторов **хинтернет** . Чтобы контролировать различные типы доступных дескрипторов, имена этих дескрипторов согласуются. В следующей таблице приведены идентификаторы, используемые соглашением в документации.



| Тип обработчика       | Создание маркера                                                                                                          | Идентификатор |
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------|------------|
| Универсальный маркер    | [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen), [**винхттпконнект**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect)или [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) | хинтернет  |
| Обработчик сеанса    | [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen)                                                                                                | хсессион   |
| Маркер подключения | [**винхттпконнект**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect)                                                                                          | хконнект   |
| Маркер запроса    | [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)                                                                                  | хрекуест   |



 

## <a name="handle-hierarchy"></a>Иерархия маркеров

Дескрипторы **хинтернет** поддерживаются в иерархии. Маркер, возвращаемый функцией [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) , представляет собой обработчик **хинтернет** сеанса. Вызов **WinHttpOpen** инициализирует функции WinHTTP и запускает контекст сеанса, который сохраняет сведения о пользователе и параметры на протяжении всего жизненного цикла обработчика сеанса. [**Винхттпконнект**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect) указывает целевой сервер HTTP или HTTPS и создает обработчик соединения **хинтернет** . По умолчанию маркер соединения наследует параметры для обработчика сеанса. Каждому ресурсу, указанному с помощью вызова [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) , присваивается обработчик запроса **хинтернет** .

На следующей схеме показана иерархия дескрипторов **хинтернет** . Каждое поле на схеме представляет функцию WinHTTP, которая возвращает обработчик **хинтернет** .

![функции, создающие дескрипторы](images/art-winhttp2.png)

После закрытия маркера приложение должно быть подготовлено к получению уведомлений о обратном вызове для этого маркера до тех пор, пока не будет возвращено окончательное **\_ состояние обратного вызова \_ \_ \_ WinHTTP** , чтобы показать, что этот маркер полностью закрыт.

Маркер сеанса называется родителем любого используемого для создания обработчика соединения. Аналогичным образом, как маркер соединения, так и его родительский обработчик сеанса являются элементами с терминами любого маркера запроса, который используется для создания.

При закрытии родительского маркера все его дочерние элементы косвенно становятся недействительными, даже если они не закрыты, а последующие запросы, использующие их, завершаются ошибкой с **\_ недопустимым \_ маркером**. Ожидающие асинхронные запросы не могут быть правильно выполнены.

На следующей диаграмме показаны функции, использующие обработчик **хинтернет** , созданный [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest). Затененные поля представляют функции WinHTTP, которые создают дескрипторы, а в обычных полях отображаются функции, которые используют эти дескрипторы **хинтернет** . Схема также упорядочена для отображения порядка, в котором функции WinHTTP обычно вызываются.

![функции, создающие дескрипторы](images/art-winhttp2.png)

## <a name="explanation-of-the-handle-hierarchy"></a>Объяснение иерархии маркеров

Во-первых, создается обработчик сеанса с [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen). [**Винхттпконнект**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect) требует, чтобы обработчик сеанса был первым параметром, и возвращал маркер соединения для указанного сервера. Обработчик запроса создается с помощью [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest), который использует маркер соединения, созданный [**винхттпконнект**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect). Если приложение выбирает Добавление дополнительных заголовков в запрос или требуется, чтобы приложение задали учетные данные для проверки подлинности, [**винхттпаддрекуессеадерс**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) и [**винхттпсеткредентиалс**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) могут быть вызваны с помощью этого обработчика запросов. Запрос отправляется функцией [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest), которая использует этот обработчик запроса. После отправки запроса дополнительные данные могут быть отправлены на сервер с помощью [**WinHttpWriteData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpwritedata), или приложение может сразу же перейти к [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) , чтобы указать, что больше никакой информации не будет отправлено на сервер. На этом этапе, в зависимости от назначения приложения, обработчик запроса можно использовать для вызова [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders), [**винхттпкуеряуссчемес**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes)или получения ресурса с помощью [**винхттпкуеридатааваилабле**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable) и [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata).

 

 
