---
description: Главный ключ — это материал основных данных, из которого производятся другие ключи.
ms.assetid: c8445f74-659a-470b-9007-07ea98d36dcd
title: Создание главного ключа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dea47c64348f89563340a4e25d411ed3174ee9d18ba1705d9707eab6b39633b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876534"
---
# <a name="creating-the-master-key"></a>Создание главного ключа

[*Главный ключ*](../secgloss/m-gly.md) — это материал основных данных, из которого производятся другие ключи. В зависимости от используемого протокола и набора шифров главный ключ может иметь длину от 5 до 48 байт. Для CSP [*RSA*](../secgloss/r-gly.md) / [*SChannel*](../secgloss/s-gly.md) этот главный ключ создается на стороне клиента и передается на сервер на конверте RSA. Для CSP/Счаннел [*Диффи-Хелмана*](../secgloss/d-gly.md)главный ключ создается путем выполнения Diffie-Hellman обмена ключами.

Код для создания и обмена главными ключами демонстрируется в:

-   [Код клиента Диффи-Хелмана для создания главного ключа](diffie-hellman-client-code-for-creating-the-master-key.md)
-   [Серверный код Диффи-Хелмана для создания главного ключа](diffie-hellman-server-code-for-creating-the-master-key.md)
-   [Код клиента RSA для создания главного ключа](rsa-client-code-for-creating-the-master-key.md)
-   [Код сервера RSA для создания главного ключа](rsa-server-code-for-creating-the-master-key.md)
-   [Указание алгоритмов](specifying-the-algorithms.md)

 

 
