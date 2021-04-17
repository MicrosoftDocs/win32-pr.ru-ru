---
description: Объясняет, как выполнить скрепляющую подпись сообщение с помощью Криптмсгкаунтерсигн.
ms.assetid: e1969b43-f50e-4c7d-a7e5-b22db4e05be2
title: Скрепляющая подпись сообщение
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02091d25e7ee22f986a26b8f07abff68ebb8c11c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663624"
---
# <a name="countersigning-a-message"></a>Скрепляющая подпись сообщение

**Выполнить скрепляющую подпись подписанное сообщение с помощью Криптмсгкаунтерсигн**

1.  Вызовите [**криптмсгопентодекоде**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode) , чтобы получить маркер подписанного сообщения.
2.  Инициализируйте [**\_ \_ \_ информационную структуру КМСГ для кодирования подписи**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_encode_info) для каунтерсигнер.
3.  Добавьте структуру [**КМСГ для \_ \_ кодирования подписи \_**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_encode_info) в массив каунтерсигнерс (в настоящее время поддерживается только один каунтерсигнер).
4.  Вызовите [**криптмсгкаунтерсигн**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcountersign) , чтобы добавить подпись или подписи другой стороны.

Если все вызовы функций выполнены успешно, то исходное сообщение теперь имеет [*подпись*](../secgloss/c-gly.md) , входящую в непроверенный атрибут.

**Выполнить скрепляющую подпись подписанное сообщение с помощью Криптмсгкаунтерсигненкодед**

1.  Вызовите [**криптмсгопентодекоде**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode) , чтобы получить маркер подписанного сообщения.
2.  Вызовите [**криптмсгжетпарам**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam) , чтобы получить закодированные сведения о подписанном сообщении.
3.  Инициализируйте [**\_ \_ \_ информационную структуру КМСГ для кодирования подписи**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_encode_info) для каунтерсигнер.
4.  Добавьте структуру [**КМСГ для \_ \_ кодирования подписи \_**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_encode_info) в массив каунтерсигнерс (в настоящее время поддерживается только один каунтерсигнер).
5.  Вызовите [**криптмсгкаунтерсигненкодед**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcountersignencoded) , чтобы создать закодированный атрибут другой стороны.
6.  Вызовите [**криптмсгконтрол**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcontrol) , чтобы добавить атрибут подписи к исходному сообщению в качестве атрибута, не прошедшего проверку подлинности.

Если все вызовы функции выполнены, к исходному сообщению добавляется атрибут [*подписи другой стороны*](../secgloss/c-gly.md) .

 

 
