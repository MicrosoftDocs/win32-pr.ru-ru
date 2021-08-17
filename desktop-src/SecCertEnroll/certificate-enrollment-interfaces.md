---
description: Для регистрации пользователя или компьютера в иерархии сертификатов можно использовать следующие интерфейсы.
ms.assetid: 653bc971-8bda-4e23-a56a-dbeb36eeaf6d
title: Интерфейсы регистрации сертификатов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb71c1240791e26781797b547b0a62aaad1612a2bce06738cecfa02c8173b215
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118902745"
---
# <a name="certificate-enrollment-interfaces"></a>Интерфейсы регистрации сертификатов

Для регистрации пользователя или компьютера в иерархии сертификатов можно использовать следующие интерфейсы.



| Интерфейс                                              | Описание                                                                                                                                                                         |
|--------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment)             | Регистрирует компьютер или пользователя в иерархии сертификатов.                                                                                                                              |
| [**IX509Enrollment2**](/windows/desktop/api/Certenroll/nn-certenroll-ix509enrollment2)           | Расширяет интерфейс [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) , чтобы включить инициализацию из шаблона.                                                                          |
| [**IX509EnrollmentHelper**](/windows/desktop/api/Certenroll/nn-certenroll-ix509enrollmenthelper) | Определяет методы, позволяющие веб-приложению регистрировать сертификат, сохранять учетные данные сервера политики в кэше учетных данных и регистрировать серверы политик и серверы регистрации. |
| [**IX509EnrollmentStatus**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollmentstatus) | Получение подробных сведений об ошибке для транзакции регистрации сертификата.                                                                                                    |
| [**IX509SCEPEnrollment**](/windows/desktop/api/Certenroll/nn-certenroll-ix509scepenrollment)     | Интерфейс протокола регистрации простых компьютеров X. 509<br/>                                                                                                                      |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Интерфейсы Цертенролл](certenroll-interfaces.md)
</dt> </dl>

 

 




