---
description: Пакет SDK для регистрации сертификатов можно использовать для создания запросов PKCS \# 10, PKCS \# 7, CMC и самозаверяющих сертификатов.
ms.assetid: 218eafb9-c9c8-49ff-8288-3909ed708ffc
title: Запросы сертификатов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9690f3a5117abfa0ae262f0a8fa38f68528abf02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682900"
---
# <a name="certificate-requests"></a>Запросы сертификатов

Пакет SDK для регистрации сертификатов можно использовать для создания запросов PKCS \# 10, PKCS \# 7, CMC и самозаверяющих сертификатов. Каждый тип запроса представлен одним из интерфейсов, перечисленных в следующей таблице. Все интерфейсы запроса напрямую или косвенно наследуются от интерфейса [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) . 

| Интерфейс                                                                        | Описание                                                                                                                                |
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10)           | Представляет запрос PKCS \# 10. Этот интерфейс наследуется от [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest).                   |
| [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7)             | Представляет запрос PKCS \# 7. Этот интерфейс наследуется от [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest).                    |
| [**IX509CertificateRequestCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcertificate) | Представляет самозаверяющий сертификат. Этот интерфейс наследуется от [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10). |
| [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc)                 | Представляет запрос CMC. Этот интерфейс наследуется от [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7).               |



 

На следующем рисунке показана структура наследования объектов Request, поддерживаемых API регистрации сертификатов. Объект [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) напрямую или косвенно выступает в качестве базового класса для всех доступных объектов запроса.

![Структура наследования интерфейсов запросов](images/certificate-request-inheritance.png)

Независимо от типа запрос на сертификат содержит сведения о субъекте, который делает запрос, Открытый ключ субъекта, набор атрибутов, набор расширений X. 509 версии 3 (которые могут быть отправлены как часть атрибутов) и подпись. Эти проблемы решаются в следующих разделах:

-   [Имена субъектов](subject-names.md)
-   [Атрибуты](attributes.md)
-   [Расширения](extensions.md)

## <a name="related-topics"></a>См. также

<dl> <dt>

[**IX509CertificateRequestCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcertificate)
</dt> <dt>

[**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc)
</dt> <dt>

[**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7)
</dt> <dt>

[**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10)
</dt> </dl>

 

 



