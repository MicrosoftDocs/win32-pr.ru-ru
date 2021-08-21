---
description: Учетные данные SChannel представляются внутренне как \_ структуры контекста сертификата.
ms.assetid: 3d2deb61-8e86-4461-8f2a-4880ca5b9d34
title: CryptoAPI 2.0 закрытых ключей
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 653ca6356849894ac5d15c07a0116bee7c2a2ba84df8c79de360d96f1e147fef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008692"
---
# <a name="cryptoapi-20-private-keys"></a>CryptoAPI 2.0 закрытых ключей

Учетные данные SChannel представляются внутренне как структуры [**\_ контекста сертификата**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) . Schannel находит [*закрытый ключ*](/windows/desktop/SecGloss/p-gly) , связанный с определенным контекстом сертификата, с помощью \_ \_ \_ свойства ID Prov info ИД сертификата \_ \_ . С помощью этого свойства SChannel обращается к *закрытому ключу* , вызывая функцию [**CryptAcquireContext**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptacquirecontexta) . Дополнительные сведения см. в разделе [пары открытого и закрытого ключей](/windows/desktop/SecCrypto/public-private-key-pairs).

Все учетные данные SChannel содержат ссылку на один или несколько закрытых ключей, каждый из которых связан с определенным сертификатом. [*Закрытые ключи*](/windows/desktop/SecGloss/p-gly) обрабатываются совершенно по-разному в зависимости от того, предназначены ли учетные данные для клиента или сервера.

## <a name="client-private-keys"></a>Закрытые ключи клиента

[*Закрытые ключи*](/windows/desktop/SecGloss/p-gly) клиента управляются [*поставщиком служб шифрования*](/windows/desktop/SecGloss/c-gly) (CSP). Закрытые ключи клиента обычно хранятся CSP типа [Prov \_ RSA \_ Full](/windows/desktop/SecCrypto/prov-rsa-full) или Prov \_ RSA \_ Signature.

Если клиентское приложение выполняет вызов [**CryptAcquireContext**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptacquirecontexta) вручную перед вызовом [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea), клиент должен привязать маркер CSP к контексту сертификата, используя \_ \_ \_ \_ \_ свойство идентификатора свойства ID Prov Handle. Если канал Schannel находит этот набор свойств, он не использует \_ \_ \_ \_ \_ свойство ID Prov info ИД параметра CERT.

## <a name="server-private-keys"></a>Закрытые ключи сервера

Закрытые ключи сервера хранятся одним из следующих CSP:

-   PROV \_ RSA \_ SChannel
-   PROV \_ DH \_ SChannel
-   PROV \_ Fortezza CSP

Выбор CSP зависит от выбранного [*алгоритма обмена ключами*](/windows/desktop/SecGloss/k-gly). Закрытые ключи сервера должны иметь тип по адресу \_ кэйексчанже.

 

 
