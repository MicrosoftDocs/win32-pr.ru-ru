---
description: Описывает, как проверить подпись другой стороны с помощью Криптмсгверификаунтерсигнатуринкодед.
ms.assetid: b7be0d4c-338f-4319-bd82-5cf3d158d6fe
title: Проверка подписи другой стороны
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 711e15388144fbf674cbb0c42ff41883edbb5af0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682976"
---
# <a name="verifying-a-countersignature"></a>Проверка подписи другой стороны

**Проверка подписи другой стороны**

1.  Вызовите [**криптмсгопентодекоде**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode) , чтобы получить маркер подписанного сообщения.
2.  Получение указателя на сертификат каунтерсигнер ( [**\_ сведения о**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info)сертификате).
3.  Вызовите [**криптмсгжетпарам**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam) , чтобы получить сведения о подписавшем из сообщения.
4.  Вызовите [**криптмсгжетпарам**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam) , чтобы получить [*подпись*](../secgloss/c-gly.md) от сообщения.
5.  Вызовите [**криптмсгверификаунтерсигнатуринкодед**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgverifycountersignatureencoded) , чтобы проверить подпись другой стороны.

Если вызов функции [**криптмсгверификаунтерсигнатуринкодед**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgverifycountersignatureencoded) выполнен, [*подпись другой стороны*](../secgloss/c-gly.md) проверяется.

 

 
