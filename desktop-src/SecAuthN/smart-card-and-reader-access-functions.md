---
description: Подключение к определенной смарт-карте и взаимодействие с ней.
ms.assetid: 37d92491-174b-471e-b36e-46d9285dd404
title: Функции смарт-карт и доступа для чтения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7202b2d6165b49bfe80e55f15c4d69cb4a6909a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664168"
---
# <a name="smart-card-and-reader-access-functions"></a>Функции смарт-карт и доступа для чтения

Следующие функции подключаются к определенной [*смарт-карте*](../secgloss/s-gly.md)и обмениваются данными с ней. Операции ввода-вывода на карточке используют буфер для отправки или получения данных, а также структуру, содержащую сведения об управлении протоколом. Структура сведений об управлении протоколом всегда начинается с [**структуры \_ \_ запроса ввода-вывода бросить**](scard-io-request.md) .



| Раздел                                                  | Описание                                                                                                                                                                                                                                |
|--------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**скардконнект**](/windows/desktop/api/Winscard/nf-winscard-scardconnecta)                   | Подключитесь к карточке.                                                                                                                                                                                                                         |
| [**скардреконнект**](/windows/desktop/api/Winscard/nf-winscard-scardreconnect)               | Повторное создание соединения.                                                                                                                                                                                                                  |
| [**скарддисконнект**](/windows/desktop/api/Winscard/nf-winscard-scarddisconnect)             | Завершение соединения.                                                                                                                                                                                                                    |
| [**SCardBeginTransaction**](/windows/desktop/api/Winscard/nf-winscard-scardbegintransaction) | Запуск [*транзакции*](../secgloss/t-gly.md)с блокированием доступа других приложений к карточке.                                                                                            |
| [**скардендтрансактион**](/windows/desktop/api/Winscard/nf-winscard-scardendtransaction)     | Завершение транзакции, что позволяет другим приложениям получить доступ к карточке.                                                                                                                                                                           |
| [**SCardStatus**](/windows/desktop/api/Winscard/nf-winscard-scardstatusa)                     | Укажите текущее состояние модуля чтения.                                                                                                                                                                                                  |
| [**SCardTransmit**](/windows/desktop/api/Winscard/nf-winscard-scardtransmit)                 | Запрашивает службу и получает данные из карточки с помощью [*t = 0*](../secgloss/t-gly.md), [*T = 1*](../secgloss/t-gly.md)и необработанных протоколов. |



 

 

 
