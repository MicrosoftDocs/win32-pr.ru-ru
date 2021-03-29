---
description: Создает запрос на сертификат CMC и регистрирует компьютер в иерархии сертификатов.
ms.assetid: ef09ef04-8925-4d66-97ad-70b4d7cf78b9
title: енроллкустомкмк
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2910e6a6ca784aaeb9ca97dc8de106932bd64c9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810702"
---
# <a name="enrollcustomcmc"></a>енроллкустомкмк

Пример Енроллкустомкмк создает запрос на сертификат CMC и регистрирует компьютер в иерархии сертификатов.

## <a name="location"></a>Расположение

При установке пакета средств разработки программного обеспечения (SDK) для Microsoft Windows этот образец устанавливается по умолчанию в папке *% ProgramFiles%* \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ Security SSL \\ Certificate \\ \\ енроллкустомкмк.

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

## <a name="related-topics"></a>См. также

<dl> <dt>

[Запрос CMC](cmc-request.md)
</dt> <dt>

[\#Запрос PKCS 10](pkcs--10-request.md)
</dt> <dt>

[Использование прилагаемых примеров](using-the-included-samples.md)
</dt> </dl>

 

 
