---
description: Создает пользовательский запрос PKCS \# 10, отправляет его в автономный центр сертификации (ЦС) и устанавливает выданный сертификат в хранилище сертификатов.
ms.assetid: dcb69d7e-457e-457b-9eea-15676ed710aa
title: enrollCustomPKCS10
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86ad95f483d4bc82136865e94a70ad46e90e1c24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105647199"
---
# <a name="enrollcustompkcs10"></a>enrollCustomPKCS10

Пример enrollCustomPKCS10 создает пользовательский \# запрос PKCS 10, отправляет его в автономный центр сертификации (ЦС) и устанавливает выданный сертификат в хранилище сертификатов. Изолированный ЦС не требует Active Directory и не использует шаблоны.

## <a name="location"></a>Расположение

При установке пакета средств разработки программного обеспечения (SDK) для Microsoft Windows этот образец устанавливается по умолчанию в папке *% ProgramFiles%* \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ Security SSL \\ Certificate \\ \\ enrollCustomPKCS10.

## <a name="discussion"></a>Разговор

Пример enrollCustomPKCS10:

1.  Обрабатывает аргументы командной строки. Командная строка должна содержать имя субъекта сертификата X. 500, имя электронной почты (RFC822) и идентификатор объекта расширенного использования ключа (OID). Например, можно указать следующие аргументы для регистрации *user1@example.com* :
    -   Имя субъекта: "*CN = User1, DC = example, DC = com*"
    -   Имя RFC822: *user1@example.com*
    -   Идентификатор объекта EKU проверки подлинности клиента: 1.3.6.1.5.5.7.3.2
2.  Создает объект [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) и инициализирует его для конечного пользователя, указывая значение **контекстусер** перечисления [**X509CertificateEnrollmentContext**](/windows/desktop/api/CertEnroll/ne-certenroll-x509certificateenrollmentcontext) .
3.  Создает объект [**IX500DistinguishedName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname) , использует объект для кодирования имени субъекта в массив байтов и добавляет массив в \# объект запроса PKCS 10.
4.  Создает объект [**иобжектид**](/windows/desktop/api/CertEnroll/nn-certenroll-iobjectid) , инициализирует его с помощью идентификатора объекта EKU (OID), указанного в командной строке, создает коллекцию [**иобжектидс**](/windows/desktop/api/CertEnroll/nn-certenroll-iobjectids) , добавляет новый объект **иобжектид** (EKU) в коллекцию, использует коллекцию для инициализации объекта [**IX509ExtensionEnhancedKeyUsage**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionenhancedkeyusage) и добавляет этот объект в запрос.
5.  Создает объект [**иалтернативенаме**](/windows/desktop/api/CertEnroll/nn-certenroll-ialternativename) , инициализирует его с помощью имени RFC822, указанного в командной строке, создает коллекцию [**иалтернативенамес**](/windows/desktop/api/CertEnroll/nn-certenroll-ialternativenames) , добавляет в коллекцию новый объект **иалтернативенаме** (RFC822 имя), создает объект [**IX509ExtensionAlternativeNames**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionalternativenames) и добавляет этот объект в запрос.
6.  Создает объект [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) , инициализирует его с помощью объекта [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) и получает строку, содержащую запрос в кодировке Base64.
7.  Создает объект [**ицертконфиг**](/windows/desktop/api/certcli/nn-certcli-icertconfig) и использует его для получения строки, СОДЕРЖАЩЕЙ конфигурацию ЦС.
8.  Создает объект CryptoAPI [**ICertRequest2**](/windows/desktop/api/certcli/nn-certcli-icertrequest2) и использует его вместе со строками, содержащими конфигурацию ЦС и запросом сертификата для отправки запроса в ЦС.
9.  Проверяет состояние отправки, и, если регистрация прошла успешно, устанавливает сертификат в хранилище сертификатов.

## <a name="related-topics"></a>См. также

<dl> <dt>

[\#Запрос PKCS 10](pkcs--10-request.md)
</dt> <dt>

[Использование прилагаемых примеров](using-the-included-samples.md)
</dt> </dl>

 

 
