---
description: CSP для PROV \_ RSA \_ SChannel должен поддерживать хэш калг \_ SSL3 \_ SHAMD5, совместимый с базовым поставщиком служб шифрования Майкрософт, который используется в проверке подлинности клиента SSL 3,0 и TLS 1,0.
ms.assetid: ca8be4fd-e7ca-4def-927d-b168628c566e
title: Тип подписи RSA для алгоритма SHA/MD5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c0f7f412f8baab053fe8668d6360af931d4759924f2eae3168bc425278382ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117974275"
---
# <a name="shamd5-rsa-signature-type"></a>Тип подписи RSA для алгоритма SHA/MD5

CSP для PROV \_ RSA \_ SChannel должен поддерживать хэш калг \_ SSL3 \_ SHAMD5 [](../secgloss/h-gly.md) , совместимый с базовым поставщиком служб шифрования Майкрософт, который используется в проверке подлинности клиента SSL 3,0 и TLS 1,0. Этот хэш состоит из объединения хэша [*MD5*](../secgloss/m-gly.md) и SHA Hash, подписанного с помощью закрытого ключа RSA или Diffie-Hellman. Маркер хэш-значения этого типа создается с помощью функции [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) или [**кпкреатехаш**](https://www.bing.com/search?q=**CPCreateHash**) с калг \_ SSL3 \_ SHAMD5 в качестве параметра *алгид* . Примеры использования хэш-функций можно увидеть в [примере программы на языке c: создание и хэширование ключа сеанса](example-c-program-creating-and-hashing-a-session-key.md) и [Пример программы на языке c: подписывание хэша и проверка хэш-подписи](example-c-program-signing-a-hash-and-verifying-the-hash-signature.md).

 

 
