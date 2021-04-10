---
description: Первая функция CryptoAPI, вызываемая приложением, использующей любые API-интерфейсы шифрования, — это функция CryptAcquireContext.
ms.assetid: ad1ff45c-7d02-431b-a287-e9db765476ce
title: Контексты поставщика служб шифрования
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df20df528b0ba0c385c7ab690436351d918f1521
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104144476"
---
# <a name="cryptographic-service-provider-contexts"></a>Контексты поставщика служб шифрования

Первая функция [*CryptoAPI*](../secgloss/c-gly.md) , вызываемая приложением, использующей любые API-интерфейсы шифрования, — это функция [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) . Эта функция возвращает маркер для конкретного CSP, который включает спецификацию определенного [*контейнера ключей*](../secgloss/k-gly.md) в CSP. Этот контейнер ключей является либо специально запрошенным контейнером ключей, либо контейнером ключей по умолчанию для текущего пользователя, вошедшего в систему.

[**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) также может создать новый контейнер ключей. Дополнительные сведения см. в разделе [Пример программы C: создание контейнера ключей и создание ключей](example-c-program-creating-a-key-container-and-generating-keys.md) и [Пример программы C: использование CryptAcquireContext](example-c-program-using-cryptacquirecontext.md).

[*Поставщик служб шифрования*](../secgloss/c-gly.md) (CSP) имеет как имя, так и тип. Например, имя одного из CSP, поставляемое в настоящее время с операционной системой, — [базовый поставщик служб шифрования Майкрософт](microsoft-base-cryptographic-provider.md). Это Prov поставщик [ \_ \_ полных типов RSA](prov-rsa-full.md) . Имя каждого поставщика является уникальным; Тип поставщика — not.

Когда приложение вызывает [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) для получения обработчика CSP, оно указывает тип поставщика и, при необходимости, имя поставщика. Если указаны и тип, и имя, функция загружает CSP с соответствующим типом поставщика и именем поставщика. Функция возвращает маркер CSP, который предоставляет доступ к CSP и [*контейнеру ключей*](../secgloss/k-gly.md) в CSP.

Когда приложение вызывает [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) и указывает тип поставщика, но не имеет имени поставщика, функция ищет именованного поставщика, сначала проверяет список именованных поставщиков по умолчанию, связанных с вошедшим в систему пользователем, и, если это происходит, из списка именованных поставщиков по умолчанию, связанных с компьютером. После определения имени поставщика функция **CryptAcquireContext** ищет CSP для этого поставщика, загружает его и возвращает его обработчик.

После завершения использования обработчика CSP выпустите его, вызвав функцию [**криптрелеасеконтекст**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptreleasecontext) .

 

 
