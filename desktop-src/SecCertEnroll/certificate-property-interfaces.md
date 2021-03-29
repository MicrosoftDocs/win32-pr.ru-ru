---
description: Для создания свойства сертификата можно использовать следующие интерфейсы.
ms.assetid: c64fca58-fb2f-412f-b7c0-5db1979d051b
title: Интерфейсы свойств сертификата
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00d0052675436a28438d5f1600a5b0097f8e177a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808333"
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



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Интерфейсы Цертенролл](certenroll-interfaces.md)
</dt> </dl>

 

 



