---
description: Объясняется, как защитить сообщения с помощью Microsoft Digest.
ms.assetid: 15509d51-80c0-4d5c-aa24-4dc17de3f12c
title: Защита сообщений с помощью Microsoft Digest
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 573eafcf66e23188546abd3acd316095ec100187
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105650872"
---
# <a name="protecting-messages-using-microsoft-digest"></a>Защита сообщений с помощью Microsoft Digest

## <a name="http-and-sasl"></a>HTTP и SASL

В качестве средства обнаружения определенных типов нарушений безопасности клиент и сервер используют функции [*проверки целостности*](../secgloss/i-gly.md) сообщений [**макесигнатуре**](/windows/desktop/api/Sspi/nf-sspi-makesignature) и [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) для защиты сообщений в [интерфейсе поставщика поддержки безопасности](sspi.md) (SSPI).

Клиент вызывает функцию [**макесигнатуре**](/windows/desktop/api/Sspi/nf-sspi-makesignature) для подписывания сообщения с помощью [*контекста безопасности*](../secgloss/s-gly.md). Сервер использует функцию [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) для проверки источника сообщения. Кроме проверки [*подписи*](../secgloss/d-gly.md) , сопровождающей сообщение, функция **VerifySignature** также проверяет, что число [*nonce*](../secgloss/n-gly.md) (заданное директивой NC) больше, чем Последнее число, отправленное для nonce. Если это не так, функция **VerifySignature** возвращает \_ \_ \_ код ошибки с непоследовательной последовательностью.

## <a name="sasl-only"></a>Только SASL

Функции [**енкриптмессаже (General)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) и [**декриптмессаже (General)**](/windows/win32/api/sspi/nf-sspi-decryptmessage) предоставляют конфиденциальность сообщений после проверки подлинности, которыми обмениваются клиент и сервер.

Чтобы использовать функции обеспечения конфиденциальности сообщений, сервер и клиент должны установить [*контекст безопасности*](../secgloss/s-gly.md) со следующими атрибутами:

-   Качество защиты, заданное директивой КОП, должно иметь значение "auth-conf".
-   Механизм шифрования должен быть указан с помощью директивы шифра.

 

 
