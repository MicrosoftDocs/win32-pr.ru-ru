---
description: Создает запрос на сертификат CMC и регистрирует компьютер в иерархии сертификатов.
ms.assetid: ef09ef04-8925-4d66-97ad-70b4d7cf78b9
title: енроллкустомкмк
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3799cd70d8f3b70ae32a95b7720a879ddd611fba5e35064d1794d39bdcd7ab9c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117780063"
---
# <a name="enrollcustomcmc"></a>енроллкустомкмк

Пример Енроллкустомкмк создает запрос на сертификат CMC и регистрирует компьютер в иерархии сертификатов.

## <a name="location"></a>Расположение

при установке пакета microsoft Windows Software Development Kit (SDK) образец устанавливается по умолчанию в папке *% ProgramFiles%* \\ Microsoft sdk \\ Windows \\ v 7.0 \\ samples \\ Security ssl \\ Certificate \\ \\ енроллкустомкмк.

## <a name="discussion"></a>Разговор

Пример Енроллкустомкмк:

1.  Обрабатывает следующие аргументы командной строки:
    -   Пользовательская пара "имя-значение", добавляемая в запрос сертификата.
    -   Альтернативное имя субъекта.
    -   Идентификатор объекта (OID) для расширения расширенного использования ключа (EKU).
2.  Создает объект запроса [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) и инициализирует его с помощью контекста компьютера.
3.  Использует запрос PKCS \# 10 для инициализации объекта [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) .
4.  Создает объект [**IX509ExtensionEnhancedKeyUsage**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionenhancedkeyusage) , используя идентификатор объекта, указанный в командной строке, и добавляет его в коллекцию Extensions для запроса CMC.
5.  Создает объект [**иалтернативенаме**](/windows/desktop/api/CertEnroll/nn-certenroll-ialternativename) , используя имя, указанное в командной строке, добавляет его в коллекцию [**иалтернативенамес**](/windows/desktop/api/CertEnroll/nn-certenroll-ialternativenames) , использует коллекцию для инициализации расширения [**IX509ExtensionAlternativeNames**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionalternativenames) и добавляет его в коллекцию Extensions для запроса CMC.
6.  Создает объект [**IX509NameValuePair**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepair) , используя имя и значение, указанные в командной строке, и добавляет его в коллекцию [**IX509NameValuePairs**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepairs) запроса CMC.
7.  Создает объект [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) , инициализирует его с помощью объекта запроса CMC и получает строку, содержащую запрос в кодировке Base64.
8.  Создает объект [**ицертконфиг**](/windows/desktop/api/certcli/nn-certcli-icertconfig) и использует его для получения строки, СОДЕРЖАЩЕЙ конфигурацию ЦС.
9.  Создает объект CryptoAPI [**ICertRequest2**](/windows/desktop/api/certcli/nn-certcli-icertrequest2) и использует его вместе со строками, содержащими конфигурацию ЦС и запросом сертификата для отправки запроса в ЦС.
10. Проверяет состояние отправки и, при успешном выполнении, устанавливает сертификат в хранилище сертификатов.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Запрос CMC](cmc-request.md)
</dt> <dt>

[\#Запрос PKCS 10](pkcs--10-request.md)
</dt> <dt>

[Использование прилагаемых примеров](using-the-included-samples.md)
</dt> </dl>

 

 
