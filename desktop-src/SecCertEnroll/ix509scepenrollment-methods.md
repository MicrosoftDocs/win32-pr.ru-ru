---
description: Интерфейс IX509SCEPEnrollment предоставляет следующие методы.
ms.assetid: B45B68D2-A14D-4D14-AF5F-1A1BB9921A0D
title: Методы IX509SCEPEnrollment
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a15fc7de6392c49bd38381771956685ba6c8427b3562e7c81c372c1bab61db49
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119993544"
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



 

 

 




