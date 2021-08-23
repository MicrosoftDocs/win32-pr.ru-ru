---
description: Как создать безопасное подключение с помощью канала Schannel.
ms.assetid: 94eb15c3-225b-4b6f-b29c-41e5d356a847
title: Создание безопасного подключения с помощью канала Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 374955b67bfa0026da5e8f8e9e88ce71da24231e218cb869cb532d05d4171bbf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008912"
---
# <a name="creating-a-secure-connection-using-schannel"></a>Создание безопасного подключения с помощью канала Schannel

[*Пакет безопасности*](/windows/desktop/SecGloss/s-gly) SChannel предоставляет доступ к четырем [*протоколам безопасности*](/windows/desktop/SecGloss/s-gly):

-   [Безопасность транспортного уровня (TLS 1,2)](transport-layer-security-protocol.md)
-   [Безопасность транспортного уровня (TLS 1,1)](transport-layer-security-protocol.md)
-   [Безопасность транспортного уровня (TLS 1,0)](transport-layer-security-protocol.md)
-   [SSL (SSL 3,0)](secure-sockets-layer-protocol.md)
-   [SSL (SSL 2,0)](secure-sockets-layer-protocol.md)

> [!Note]  
> Протоколы PCT и SSL 2,0 были заменены протоколом TLS и не должны использоваться для новой разработки.

 

**Настройка безопасного подключения между клиентом и сервером**

1.  Получение учетных данных Schannel ([Получение учетных данных SChannel](obtaining-schannel-credentials.md)).
2.  Создание контекста безопасности безопасного канала Schannel ([Создание контекста безопасности SChannel](creating-an-schannel-security-context.md)).

После установления соединения можно получить сведения о его атрибутах. Дополнительные сведения см. в разделе [Получение сведений о подключениях SChannel](getting-information-about-schannel-connections.md).

Если после установления подключения происходит потеря требований безопасности приложения или подключение теряется, можно повторно согласовать соединение. Дополнительные сведения см. в разделе повторное [согласование подключения SChannel](renegotiating-an-schannel-connection.md).

После завершения использования подключения SChannel необходимо выполнить необходимую очистку. Дополнительные сведения см. [в разделе Завершение работы подключения SChannel](shutting-down-an-schannel-connection.md).

Сведения о примерах, поставляемых с пакетом средств разработки программного обеспечения для платформы (SDK), демонстрирующих [*пакеты безопасности*](/windows/desktop/SecGloss/s-gly)SChannel, см. в примерах PSDK с использованием канала Schannel.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Указание шифров SChannel и стойкости шифров](specifying-schannel-ciphers-and-cipher-strengths.md)
</dt> </dl>

 

 
