---
description: Набор алгоритмов шифрования. Протоколы Schannel используют алгоритмы из комплекта шифров для создания ключей и шифрования информации.
ms.assetid: 380452e2-a9c8-4380-a3bf-9c7942a0c0c2
title: Наборы шифров TLS в Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbf77d821612093e3015a0f8dee4cf51ae5bd9b95c653b61fe7a36271ba81ba5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118918657"
---
# <a name="tls-cipher-suites-in-windows-vista"></a>Наборы шифров TLS в Windows Vista

Комплект шифров — это набор алгоритмов шифрования. Протоколы Schannel используют алгоритмы из комплекта шифров для создания ключей и шифрования информации. Комплект шифров указывает один алгоритм для каждой из следующих задач:

-   обмена ключами;
-   массового шифрования;
-   проверки подлинности сообщений.

[*Алгоритмы обмена ключами*](../secgloss/k-gly.md) защищают сведения, необходимые для создания общих ключей. Эти алгоритмы являются асимметричными ([*алгоритмы открытого ключа*](../secgloss/p-gly.md)) и хорошо работают для относительно небольших объемов данных.

Алгоритмы блочного шифрования шифруют сообщения, которыми обмениваются клиенты и серверы. Эти алгоритмы являются [*симметричными*](../secgloss/s-gly.md) и хорошо работают для больших объемов данных.

Алгоритмы [проверки подлинности сообщений](message-authentication-codes-in-schannel.md) генерируют [*хэши*](../secgloss/h-gly.md) и подписи сообщений, гарантирующие [*целостность*](../secgloss/i-gly.md) сообщения.

Разработчики указывают эти элементы с помощью типов данных [**\_ идентификаторов ALG**](../seccrypto/alg-id.md) . Дополнительные сведения см. в разделе [Указание шифров SChannel и стойкости шифра](specifying-schannel-ciphers-and-cipher-strengths.md).

Schannel поддерживает следующие комплекты шифров. Наборы перечислены в порядке по умолчанию, в котором они выбираются поставщиком Microsoft SChannel.

> [!IMPORTANT]
> Веб-службы HTTP/2 завершаются сбоем с комплектами шифров, отличными от HTTP и 2. Сведения о том, как обеспечить работу веб-служб с клиентами и браузерами HTTP/2, см. [в разделе Развертывание настраиваемого упорядочения набора шифров](https://support.microsoft.com/help/4032720/how-to-deploy-custom-cipher-suite-ordering-in-windows-server-2016).

 



| Набор шифров                                                 | Режим FIPS включен | Exchange              | Шифрование      | Хэш            | Протоколы                   |
|--------------------------------------------------------------|-------------------|-----------------------|-----------------|-----------------|-----------------------------|
| TLS \_ RSA \_ с \_ AES \_ 128 \_ CBC \_ SHA<br/>                | Да<br/>    | RSA<br/>        | AES<br/>  | SHA1<br/> | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ RSA \_ с \_ AES \_ 256 \_ CBC \_ SHA<br/>                | Да<br/>    | RSA<br/>        | AES<br/>  | SHA1<br/> | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| Алгоритм \_ TLS \_ RSA \_ с \_ \_ алгоритмом SHA 128<br/>                     | Нет<br/>     | RSA<br/>        | RC4;<br/>  | SHA1<br/> | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| TLS \_ RSA \_ с \_ 3DES \_ еде \_ CBC \_ SHA<br/>               | Да<br/>    | RSA<br/>        | 3DES<br/> | SHA1<br/> | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ECDHE \_ ECDSA \_ с \_ AES \_ 128 \_ CBC \_ SHA \_ P256<br/> | Да<br/>    | Алгоритм ECDH \_ P256<br/> | AES<br/>  | SHA1<br/> | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ECDHE \_ ECDSA \_ с \_ AES \_ 128 \_ CBC \_ SHA \_ P384<br/> | Да<br/>    | Алгоритм ECDH \_ P384<br/> | AES<br/>  | SHA1<br/> | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ECDHE \_ ECDSA \_ с \_ AES \_ 128 \_ CBC \_ SHA \_ P521<br/> | Да<br/>    | Алгоритм ECDH \_ P521<br/> | AES<br/>  | SHA1<br/> | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ECDHE \_ ECDSA \_ с \_ AES \_ 256 \_ CBC \_ SHA \_ P256<br/> | Да<br/>    | Алгоритм ECDH \_ P256<br/> | AES<br/>  | SHA1<br/> | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ECDHE \_ ECDSA \_ с \_ AES \_ 256 \_ CBC \_ SHA \_ P384<br/> | Да<br/>    | Алгоритм ECDH \_ P384<br/> | AES<br/>  | SHA1<br/> | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ECDHE \_ ECDSA \_ с \_ AES \_ 256 \_ CBC \_ SHA \_ P521<br/> | Да<br/>    | Алгоритм ECDH \_ P521<br/> | AES<br/>  | SHA1<br/> | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ECDHE \_ RSA \_ с \_ AES \_ 128 \_ CBC \_ SHA \_ P256<br/>   | Да<br/>    | Алгоритм ECDH \_ P256<br/> | AES<br/>  | SHA1<br/> | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ECDHE \_ RSA \_ с \_ AES \_ 128 \_ CBC \_ SHA \_ P384<br/>   | Да<br/>    | Алгоритм ECDH \_ P384<br/> | AES<br/>  | SHA1<br/> | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ECDHE \_ RSA \_ с \_ AES \_ 128 \_ CBC \_ SHA \_ P521<br/>   | Да<br/>    | Алгоритм ECDH \_ P521<br/> | AES<br/>  | SHA1<br/> | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ECDHE \_ RSA \_ с \_ AES \_ 256 \_ CBC \_ SHA \_ P256<br/>   | Да<br/>    | Алгоритм ECDH \_ P256<br/> | AES<br/>  | SHA1<br/> | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ECDHE \_ RSA \_ с \_ AES \_ 256 \_ CBC \_ SHA \_ P384<br/>   | Да<br/>    | Алгоритм ECDH \_ P384<br/> | AES<br/>  | SHA1<br/> | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ECDHE \_ RSA \_ с \_ AES \_ 256 \_ CBC \_ SHA \_ P521<br/>   | Да<br/>    | Алгоритм ECDH \_ P521<br/> | AES<br/>  | SHA1<br/> | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ дхе \_ DSS \_ с \_ AES \_ 128 \_ CBC \_ SHA<br/>           | Да<br/>    | ХЕЛМАНА<br/>         | AES<br/>  | SHA1<br/> | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ дхе \_ DSS \_ с \_ AES \_ 256 \_ CBC \_ SHA<br/>           | Да<br/>    | ХЕЛМАНА<br/>         | AES<br/>  | SHA1<br/> | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ дхе \_ DSS \_ с \_ 3DES \_ еде \_ CBC \_ SHA<br/>          | Да<br/>    | ХЕЛМАНА<br/>         | 3DES<br/> | SHA1<br/> | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| Алгоритм TLS \_ RSA \_ с \_ RC4 \_ 128 \_ MD5<br/>                     | Нет<br/>     | RSA<br/>        | RC4;<br/>  | MD5<br/>  | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| SSL \_ CK \_ RC4 \_ 128 \_ с \_ MD5<br/>                      | Нет<br/>     | RSA<br/>        | RC4;<br/>  | MD5<br/>  | SSL 2.0<br/>          |
| SSL \_ CK \_ Des \_ 192 \_ EDE3 \_ CBC \_ с \_ MD5<br/>           | Нет<br/>     | RSA<br/>        | 3DES<br/> | MD5<br/>  | SSL 2.0<br/>          |
| TLS \_ RSA \_ с \_ неопределенным \_ MD5<br/>                         | Нет<br/>     | RSA<br/>        |                 | MD5<br/>  | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| TLS \_ RSA \_ с \_ нулевым \_ SHA<br/>                         | Нет<br/>     | RSA<br/>        |                 | SHA1<br/> | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |



 

Schannel поддерживает следующие наборы шифров. Тем не менее они отсутствуют по умолчанию. При необходимости они должны быть добавлены. Сведения о том, как добавить комплекты шифров к поставщику SChannel, см. в разделе [Определение приоритетов для комплектов шифров SChannel](prioritizing-schannel-cipher-suites.md).

-   \_Экспорт RSA \_ TLS \_ с \_ помощью \_ \_ алгоритма MD5 40
-   TLS \_ RSA \_ EXPORT1024 \_ с \_ \_ \_ алгоритмом SHA 56
-   TLS \_ RSA \_ EXPORT1024 \_ с \_ Des \_ CBC \_ SHA
-   SSL \_ CK \_ RC4 \_ 128 \_ EXPORT40 \_ MD5
-   SSL \_ CK \_ Des \_ 64 \_ CBC \_ с \_ MD5
-   TLS \_ RSA \_ с \_ Des \_ CBC \_ SHA
-   TLS \_ RSA \_ с \_ неопределенным \_ MD5
-   TLS \_ RSA \_ с \_ нулевым \_ SHA
-   TLS \_ дхе \_ DSS \_ EXPORT1024 \_ с \_ Des \_ CBC \_ SHA
-   TLS \_ дхе \_ DSS \_ с \_ Des \_ CBC \_ SHA

**Windows Server 2003 и Windows XP:** Дополнительные сведения о поддерживаемых комплектах шифров см. в следующих разделах.

| Раздел                                                                         | Описание                                                                                                                        |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [Комплекты шифров TLS](tls-cipher-suites.md)<br/>                         | сведения о комплектах шифров, доступных по протоколу TLS в Windows Server 2003 и Windows XP.<br/>              |
| [Протокол SSL](secure-sockets-layer-protocol.md)<br/> | общие сведения о SSL 2,0 и 3,0, включая доступные комплекты шифров в Windows Server 2003 и Windows XP.<br/> |



 

 

 
