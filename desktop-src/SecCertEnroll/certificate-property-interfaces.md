---
description: Для создания свойства сертификата можно использовать следующие интерфейсы.
ms.assetid: c64fca58-fb2f-412f-b7c0-5db1979d051b
title: Интерфейсы свойств сертификата
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e3d0ab8d9f8e9bb73d47b7e112dfa0ff6fb11f70031c64405b660ee5096dd78
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118902610"
---
# <a name="certificate-property-interfaces"></a>Интерфейсы свойств сертификата

Для создания свойства сертификата можно использовать следующие интерфейсы.



| Интерфейс                                                                          | Описание                                                                                                                                                                                                                                               |
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ицертпропертиес**](/windows/desktop/api/CertEnroll/nn-certenroll-icertproperties)                                         | Управление коллекцией объектов [**ицертпроперти**](/windows/desktop/api/CertEnroll/nn-certenroll-icertproperty) .                                                                                                                                                                                    |
| [**ицертпроперти**](/windows/desktop/api/CertEnroll/nn-certenroll-icertproperty)                                             | Связывает внешнее свойство с сертификатом.                                                                                                                                                                                                       |
| [**ицертпропертярчивед**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyarchived)                             | Представляет свойство сертификата, которое определяет, архивируется ли сертификат.                                                                                                                                                                |
| [**ицертпропертярчиведкэйхаш**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyarchivedkeyhash)               | Представляет хэш SHA-1 зашифрованного закрытого ключа, отправленного в центр сертификации для архивирования.                                                                                                                                                  |
| [**ицертпропертяутоенролл**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyautoenroll)                         | Представляет свойство сертификата, идентифицирующее шаблон, настроенный для включения автоматической регистрации сертификата.                                                                                                                        |
| [**ицертпропертибаккедуп**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertybackedup)                             | Представляет свойство сертификата, которое определяет, была ли создана резервная копия сертификата, и, если да, Дата и время сохранения.                                                                                                               |
| [**ицертпропертидескриптион**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertydescription)                       | Позволяет указать и получить строку, содержащую описательные сведения для сертификата.                                                                                                                                                     |
| [**ицертпропертенроллмент**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyenrollment)                         | Представляет свойство сертификата, которое содержит сведения о сертификате и центре сертификации, созданные при вызове клиентом метода [**регистрации**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) в интерфейсе [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) . |
| [**ицертпропертенроллментполицисервер**](/windows/desktop/api/Certenroll/nn-certenroll-icertpropertyenrollmentpolicyserver) | Представляет свойство внешнего сертификата, которое содержит сведения о сервере политики регистрации сертификатов (CEP) и сервере регистрации сертификатов (CES).                                                                                       |
| [**ицертпропертифриендлинаме**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyfriendlyname)                     | Позволяет указать и получить строку, содержащую отображаемое имя сертификата.                                                                                                                                                             |
| [**ицертпропертикэйпровинфо**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertykeyprovinfo)                       | Представляет свойство сертификата, содержащее сведения о закрытом ключе.                                                                                                                                                                          |
| [**ицертпропертиреневал**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyrenewal)                               | Представляет свойство сертификата, которое содержит хэш SHA-1 нового сертификата, созданного при продлении существующего сертификата.                                                                                                                      |
| [**ицертпропертирекуесторигинатор**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyrequestoriginator)           | Представляет свойство сертификата, содержащее имя системы доменных имен (DNS) компьютера, на котором был создан запрос.                                                                                                                     |
| [**ицертпропертирекуесторигинатор**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyrequestoriginator)           | Представляет свойство сертификата, содержащее имя системы доменных имен (DNS) компьютера, на котором был создан запрос.                                                                                                                     |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Интерфейсы Цертенролл](certenroll-interfaces.md)
</dt> </dl>

 

 



