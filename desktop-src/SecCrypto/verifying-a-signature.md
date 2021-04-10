---
description: Чтобы проверить подпись, создайте хэш-объект с помощью CryptCreateHash. Этот объект хэша накапливает данные для проверки. Затем данные добавляются в хэш-объект с помощью функции CryptHashData.
ms.assetid: 3779f83b-0d87-4f47-949b-9eb39690adfb
title: Проверка подписи
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9a416dc2c3f7523af781e68fe78b066accbe6d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155071"
---
# <a name="verifying-a-signature"></a>Проверка подписи

Чтобы проверить подпись, создайте [*хэш-объект*](../secgloss/h-gly.md) с помощью [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash). Этот объект хэша накапливает данные для проверки. Затем данные добавляются в хэш-объект с помощью функции [**CryptHashData**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata) .

После добавления последнего блока данных в хэш используйте [**криптверифисигнатуре**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifysignaturea) для проверки подписи. Адрес данных подписи, маркер для хэш-объекта, а также маркер открытых ключей передаются в **криптверифисигнатуре**.

После проверки подписи (или неудачной проверки) удалите хэш-объект с помощью функции [**криптдестройхаш**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroyhash) .

 

 
