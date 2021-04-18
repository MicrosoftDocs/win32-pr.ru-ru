---
description: Для регистрации пользователя или компьютера в иерархии сертификатов можно использовать следующие интерфейсы.
ms.assetid: 653bc971-8bda-4e23-a56a-dbeb36eeaf6d
title: Интерфейсы регистрации сертификатов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6e13e8db7d2938b7facb0b055303c1bdc18392a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684535"
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



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Интерфейсы Цертенролл](certenroll-interfaces.md)
</dt> </dl>

 

 




