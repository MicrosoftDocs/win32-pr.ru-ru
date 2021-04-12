---
description: Для создания запросов на сертификаты можно использовать следующие интерфейсы.
ms.assetid: 6021db79-ac90-4e0c-afbd-0f926abcab78
title: Интерфейсы запросов сертификатов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43e18a4f8e1ce60348ffdf52afe210247f6d20a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154738"
---
# <a name="certificate-request-interfaces"></a>Интерфейсы запросов сертификатов

Для создания запросов на сертификаты можно использовать следующие интерфейсы.



| Интерфейс                                                                          | Описание                                                                                                                                                   |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest)                         | Представляет абстрактный интерфейс верхнего уровня для запроса сертификата.                                                                                        |
| [**IX509CertificateRequestCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcertificate)   | Позволяет создавать сертификаты напрямую, не обращаясь к центру регистрации или сертификации.                                                  |
| [**IX509CertificateRequestCertificate2**](/windows/desktop/api/Certenroll/nn-certenroll-ix509certificaterequestcertificate2) | Расширяет интерфейс [**IX509CertificateRequestCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcertificate) , чтобы включить инициализацию из шаблона.              |
| [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc)                   | Представляет запрос CMC.                                                                                                                                     |
| [**IX509CertificateRequestCmc2**](/windows/desktop/api/Certenroll/nn-certenroll-ix509certificaterequestcmc2)                 | Расширяет интерфейс [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) , чтобы включить инициализацию из шаблона.                              |
| [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10)             | Представляет запрос PKCS \# 10.                                                                                                                               |
| [**IX509CertificateRequestPkcs10V2**](/windows/desktop/api/Certenroll/nn-certenroll-ix509certificaterequestpkcs10v2)         | Расширяет интерфейс [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) , чтобы включить инициализацию из шаблона.                        |
| [**IX509CertificateRequestPkcs10V3**](/windows/desktop/api/Certenroll/nn-certenroll-ix509certificaterequestpkcs10v3)         | Расширяет интерфейс [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) и добавляет свойства, обеспечивающие аттестацию сертификатов TPM. |
| [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7)               | Представляет запрос PKCS \# 7.                                                                                                                                |
| [**IX509CertificateRequestPkcs7V2**](/windows/desktop/api/Certenroll/nn-certenroll-ix509certificaterequestpkcs7v2)           | Расширяет интерфейс [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7) , чтобы включить инициализацию из шаблона.                          |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Интерфейсы Цертенролл](certenroll-interfaces.md)
</dt> </dl>

 

 



