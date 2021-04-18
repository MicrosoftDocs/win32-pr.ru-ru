---
description: CSP для PROV \_ RSA \_ SChannel должен поддерживать хэш калг \_ SSL3 \_ SHAMD5, совместимый с базовым поставщиком служб шифрования Майкрософт, который используется в проверке подлинности клиента SSL 3,0 и TLS 1,0.
ms.assetid: ca8be4fd-e7ca-4def-927d-b168628c566e
title: Тип подписи RSA для алгоритма SHA/MD5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71dcd515c61a4baf3da1fb35e4b5e6d21d5c849e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682389"
---
# <a name="shamd5-rsa-signature-type"></a>Тип подписи RSA для алгоритма SHA/MD5

CSP для PROV \_ RSA \_ SChannel должен поддерживать хэш калг \_ SSL3 \_ SHAMD5 [](../secgloss/h-gly.md) , совместимый с базовым поставщиком служб шифрования Майкрософт, который используется в проверке подлинности клиента SSL 3,0 и TLS 1,0. Этот хэш состоит из объединения хэша [*MD5*](../secgloss/m-gly.md) и SHA Hash, подписанного с помощью закрытого ключа RSA или Diffie-Hellman. Маркер хэш-значения этого типа создается с помощью функции [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) или [**кпкреатехаш**](https://www.bing.com/search?q=**CPCreateHash**) с калг \_ SSL3 \_ SHAMD5 в качестве параметра *алгид* . Примеры использования хэш-функций можно увидеть в [примере программы на языке c: создание и хэширование ключа сеанса](example-c-program-creating-and-hashing-a-session-key.md) и [Пример программы на языке c: подписывание хэша и проверка хэш-подписи](example-c-program-signing-a-hash-and-verifying-the-hash-signature.md).

 

 
