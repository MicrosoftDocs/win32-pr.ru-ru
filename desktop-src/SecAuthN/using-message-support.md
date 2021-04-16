---
description: Объясняется, как использовать поддержку сообщений SSPI.
ms.assetid: 14d4813e-413e-4ef9-85f0-96986c3c1eca
title: Использование поддержки сообщений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d75a2475609afed1647d99552a3719479d84fbd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664030"
---
# <a name="using-message-support"></a>Использование поддержки сообщений

После завершения подтверждения и установления безопасного подключения приложение может использовать функции [**макесигнатуре**](/windows/desktop/api/Sspi/nf-sspi-makesignature), [**енкриптмессаже (Общие)**](/windows/win32/api/sspi/nf-sspi-encryptmessage), [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature)и [**декриптмессаже (Общие)**](/windows/win32/api/sspi/nf-sspi-decryptmessage) для обмена подписанными или зашифрованными данными приложения с удаленным компьютером.

Примеры использования этих функций после установки [*контекста безопасности*](../secgloss/s-gly.md) демонстрируются в следующих разделах:

-   [Подписывание сообщения](signing-a-message.md)
-   [Проверка сообщения](verifying-a-message.md)
-   [Шифрование сообщения](encrypting-a-message.md)
-   [Расшифровка сообщения](decrypting-a-message.md)

 

 
