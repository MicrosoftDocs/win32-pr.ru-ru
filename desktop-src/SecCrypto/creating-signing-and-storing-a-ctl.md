---
description: Создайте подписанный список доверия сертификатов (CTL) и сохраните его в хранилище сертификатов.
ms.assetid: 82d75d60-2343-413c-ba53-ccee02d1ad41
title: Создание, подписывание и хранение списка доверия сертификатов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3f9aac8c75f7c112a09c62bb52d6e554aee7703e7f3e02c101545de5c5196db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876564"
---
# <a name="creating-signing-and-storing-a-ctl"></a>Создание, подписывание и хранение списка доверия сертификатов

Следующие процедуры создают подписанный [*список доверия сертификатов*](../secgloss/c-gly.md) (CTL) и сохраняют его в [*хранилище сертификатов*](../secgloss/c-gly.md).

**Создание и подписание списка доверия сертификатов**

1.  Создайте массив элементов, которые будут храниться в списке [*доверия сертификатов*](../secgloss/c-gly.md). В случае доверенных сертификатов это должны быть хэши SHA1 или MD5 доверенных сертификатов.
2.  Инициализируйте [**структуру \_ сведений CTL**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_info) , содержащую только что созданный массив элементов.
3.  Инициализируйте [**структуру \_ \_ \_ сведений о кодировании со знаком КМСГ**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signed_encode_info) .
4.  Вызовите [**криптмсженкодеандсигнктл**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgencodeandsignctl). Этот вызов функции возвращает указатель на подписанный, закодированный CTL (в формате PKCS \# 7), содержащий список элементов, созданных на шаге 1.

**Добавление CTL в хранилище сертификатов**

1.  Получение указателя на подписанный и закодированный список доверия сертификатов.
2.  Откройте целевое хранилище сертификатов, вызвав [**цертопенсторе**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore).
3.  Вызовите [**цертадденкодедктлтосторе**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddencodedctltostore).

 

 
