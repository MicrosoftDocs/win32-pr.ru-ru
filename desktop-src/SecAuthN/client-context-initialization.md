---
description: Инициализация контекста клиента
ms.assetid: 0c8aad3e-e726-49ce-8fc9-94dbd60cc5cb
title: Инициализация контекста клиента
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0c0f2912de57487c1f30fdac1ef40740553947b993ef6f5179a028625f132af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141187"
---
# <a name="client-context-initialization"></a>Инициализация контекста клиента

Чтобы установить безопасное соединение, клиент получает исходящий обработчик [*учетных данных*](/windows/desktop/SecGloss/c-gly) перед отправкой на сервер запроса проверки подлинности. Сервер создает для клиента контекст безопасности из запроса проверки подлинности. В настройке проверки подлинности участвуют две функции SSPI на стороне клиента:

-   [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) получает ссылку на ранее полученные [*учетные данные*](/windows/desktop/SecGloss/c-gly)для входа.
-   [**InitializeSecurityContext (Общие)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) создает исходные маркеры безопасности запроса проверки подлинности.

код для этого процесса можно увидеть в функции **женклиентконтекст** в [использовании SSPI с клиентом сокетов Windows](using-sspi-with-a-windows-sockets-client.md).

Если клиентская программа должна использовать учетные данные в дополнение к собственным учетным данным, таким как имя пользователя, имя домена и пароль, он предоставляет их в вызове [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) с использованием структуры [**\_ \_ \_ удостоверения WinNT auth**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) с указанием дополнительных учетных данных. Дополнительные сведения о функциях учетных данных см. в разделе [Управление учетными](authentication-functions.md)данными.

> [!Note]  
> Элемент **flags** в структуре [**\_ \_ \_ идентификаторов проверки подлинности в секунду**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) может иметь значение \_ WinNT \_ AUTH \_ Identity ANSI, \_ Если строки в структуре являются асЦи или OEM. Строки ANSI можно использовать с членом **flags** в структуре **\_ \_ \_ удостоверений WinNT auth** с установленным параметром в сек \_ . WinNT Authentication \_ Identity, \_ \_ если они сначала преобразуются в [*Юникод*](/windows/desktop/SecGloss/u-gly) с помощью функции [**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) .

 

Чтобы инициировать первую часть проверки подлинности, клиент вызывает [**InitializeSecurityContext (Общие)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) , чтобы получить исходный маркер безопасности, отправляемый на сервер в сообщении запроса на подключение.

Клиент использует сведения о маркере безопасности, полученные в дескрипторе выходного буфера, для создания сообщения, отправляемого на сервер. Создание сообщения с точки зрения размещения различных буферов и т. д. является частью [*протокола приложения*](/windows/desktop/SecGloss/a-gly) и должно быть понято обеим сторонам.

Клиент проверяет состояние возврата из [**InitializeSecurityContext (Общие)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) , чтобы определить, будет ли проверка подлинности завершена в одном вызове. Состояние возврата в СЕКУНДах \_ , по- \_ прежнему \_ требуется, указывает, что протокол безопасности требует нескольких сообщений проверки подлинности. Дополнительные сведения о контекстных функциях см. в разделе [Управление контекстами](authentication-functions.md).

 

 
