---
description: Интерфейс IX509SCEPEnrollment предоставляет следующие методы.
ms.assetid: B45B68D2-A14D-4D14-AF5F-1A1BB9921A0D
title: Методы IX509SCEPEnrollment
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a33c3bdee14b865211b53649075dec6d4617a4c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683827"
---
# <a name="ix509scepenrollment-methods"></a>Методы IX509SCEPEnrollment

Интерфейс [**IX509SCEPEnrollment**](/windows/desktop/api/Certenroll/nn-certenroll-ix509scepenrollment) предоставляет следующие методы.

## <a name="in-this-section"></a>В этом разделе



| Раздел                                                                                                              | Описание                                                                                                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Метод Креатерекуестмессаже**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-createrequestmessage)<br/>                         | Создайте сообщение запроса PKCS10 с паролем вызова. Сообщение запроса находится в конверте PKCS7, зашифрованном с помощью сертификата шифрования сервера SCEP и подписанного сертификатом подписи сервера.<br/> |
| [**Метод Креатеретриевецертификатемессаже**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-createretrievecertificatemessage)<br/> | Получение ранее выданного сертификата.<br/>                                                                                                                                                                   |
| [**Метод Креатеретриевепендингмессаже**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-createretrievependingmessage)<br/>         | Создайте сообщение для опроса сертификатов (регистрация вручную).<br/>                                                                                                                                               |
| [**Метод Делетерекуест**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-deleterequest)<br/>                                       | Удалите все сертификаты или ключи, созданные для запроса.<br/>                                                                                                                                                    |
| [**Метод Initialize**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-initialize)<br/>                                             | Инициализируйте экземпляр при подготовке для нового запроса.<br/>                                                                                                                                                   |
| [**Метод Инитиализефорпендинг**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-initializeforpending)<br/>                         | Инициализируйте экземпляр, чтобы подготовиться к формированию сообщения для получения выданного сертификата, или установите ответ на предыдущий запрос от издателя.<br/>                                              |
| [**Метод Процессреспонсемессаже**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-processresponsemessage)<br/>                     | Обработка ответного сообщения и возврат метода обработки сообщения.<br/>                                                                                                                                       |



 

 

 




