---
description: Как создавать, извлекать и экспортировать ключи RSA/SChannel.
ms.assetid: 3069232f-d016-4973-ae39-89b0e2a03cd7
title: Ключи RSA/SChannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93c9d23de40f32a499013928086ccb52fc1d1e67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541794"
---
# <a name="rsaschannel-keys"></a>Ключи RSA/SChannel

## <a name="generating-and-retrieving-rsaschannel-keys"></a>Создание и получение ключей RSA/SChannel

[*RSA*](../secgloss/r-gly.md) / Ключи [*SChannel*](../secgloss/s-gly.md) можно создавать путем вызова функции [**криптженкэй**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) . Для вызова **криптженкэй** требуется \_ идентификатор алгоритма кэйексчанже, переданный в параметре *алгид* .

**Создание пары открытого и закрытого ключей RSA/SChannel**

1.  Вызовите функцию [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) , чтобы получить маркер [поставщика служб шифрования Microsoft RSA/SChannel](microsoft-rsa-schannel-cryptographic-provider.md).
2.  Вызовите функцию [**криптженкэй**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) для создания ключей. \_Для параметра *алгид* в параметре кэйексчанже должно быть передано значение, а верхние 16 разрядов параметра *dwFlags* должны иметь требуемый размер ключа (512 бит). В параметре *hKey* возвращается маркер структуры [**хкрипткэй**](hcryptkey.md) .

**Получение указателя на ранее созданные ключи пользователей RSA/SChannel**

1.  Вызовите функцию [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) , чтобы получить маркер [поставщика служб шифрования Microsoft RSA/SChannel](microsoft-rsa-schannel-cryptographic-provider.md).
2.  Вызовите функцию [**криптжетусеркэй**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) с параметром *двкэйспек* , для которого задано значение, равное \_ кэйексчанже.

## <a name="exporting-rsaschannel-keys"></a>Экспорт ключей RSA/SChannel

[*Главные ключи*](../secgloss/m-gly.md) можно экспортировать в простые ключевые структуры больших двоичных объектов. Это должно быть реализовано таким же образом, как экспорт стандартных [*ключей шифрования*](../secgloss/b-gly.md) [*RC4*](../secgloss/r-gly.md) [*или DES*](../secgloss/d-gly.md) , как описано в разделе [простой ключ BLOB](https://www.bing.com/search?q=Simple+Key+BLOB). Элементу **аикэйалг** структуры [**публиккэйструк**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) присваивается идентификатор алгоритма для главного ключа (КАЛГ \_ PCT1 \_ master, калг \_ SSL2 \_ master, калг \_ SSL3 \_ master или калг \_ TLS1 \_ master).

Если функция [**кпекспорткэй**](https://www.bing.com/search?q=**CPExportKey**) экспортирует главный ключ SSL2 и \_ \_ установлен флаг шифрования SSL2, то для предотвращения атак отката версий установите первые восемь байт блока шифрования в 0x03, а не в случайные данные. [](../secgloss/p-gly.md)

Если в параметре *dwFlags* функции [**кпекспорткэй**](https://www.bing.com/search?q=**CPExportKey**) указывается константа **шифрования \_ дестройкэй** , то CSP уничтожает ключ или маркер ключа после экспорта ключа. Этот флаг предназначен для использования только с [*непрозрачными BLOB-объектами*](../secgloss/o-gly.md).

 

 
