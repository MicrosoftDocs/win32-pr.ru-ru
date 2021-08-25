---
description: Объясняет, как создать HMAC.
ms.assetid: b1747b7e-a505-4b23-93bc-cef4e77bf825
title: Создание HMAC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1eb600b00c0bfa3ac8af24cd297b1e2dd67933e2990216dafe84713ee5e831c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876673"
---
# <a name="creating-an-hmac"></a>Создание HMAC

**Вычисление HMAC**

1.  Получите указатель на [*поставщик служб шифрования*](../secgloss/c-gly.md) Майкрософт (CSP), вызвав [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta).
2.  Создайте маркер для [*хэш-объекта*](../secgloss/h-gly.md) [*HMAC*](../secgloss/h-gly.md), вызвав [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash). Передайте КАЛГ \_ HMAC в параметре *алгид* . Передайте маркер [*симметричного ключа*](../secgloss/s-gly.md) в параметре *hKey* . Этот симметричный ключ используется для вычисления HMAC.
3.  Укажите тип хэша, который будет использоваться путем вызова [**криптсесашпарам**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsethashparam) с параметром *двпарам* , для которого задано значение HP \_ HMAC \_ info. Параметр *pbData* должен указывать на инициализированную структуру [**HMAC \_ info**](/windows/desktop/api/Wincrypt/ns-wincrypt-hmac_info) .
4.  Вызовите [**CryptHashData**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata) , чтобы начать вычисление HMAC данных. Первый вызов **CryptHashData** приводит к объединению значения ключа с помощью оператора XOR с внутренней строкой и данными. Результат операции XOR хэшируется, а затем целевые данные для HMAC (на которые указывает параметр *pbData* , переданный в вызове **CryptHashData**) хэшируется. При необходимости можно выполнить последующие вызовы **CryptHashData** , чтобы завершить хэширование целевых данных.
5.  Вызовите [**CryptGetHashParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgethashparam) , указав для параметра *двпарам* значение HP \_ хашвал. Этот вызов приводит к завершению внутреннего хэша и объединению внешней строки с помощью XOR с ключом. Результат операции XOR хэшируется, а затем результат внутреннего хэша (выполненного на предыдущем шаге) хэшируется. Внешний хэш затем завершается и возвращается в параметре *pbData* и длине в параметре *двдатален* .

> [!Note]  
> Не используйте один и тот же [*симметричный*](../secgloss/s-gly.md) ключ ([*сеанс*](../secgloss/s-gly.md)) как для шифрования сообщений, так и для создания [*код проверки подлинности сообщения*](../secgloss/m-gly.md) (Mac). Использование одного и того же ключа позволяет значительно увеличить риск появления сообщений, декодированных злоумышленниками.

 

 

 
