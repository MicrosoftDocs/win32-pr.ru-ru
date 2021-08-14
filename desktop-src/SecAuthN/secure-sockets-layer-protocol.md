---
description: сведения в этом разделе относятся к Windows Server 2003 и Windows XP.
ms.assetid: 45536902-af80-4dca-b3ce-207086844763
title: Протокол SSL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: faf8e6b7232db8bef98d5170887d6be75c9770927954a40b606450bf214efdf5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118918387"
---
# <a name="secure-sockets-layer-protocol"></a>Протокол SSL

сведения в этом разделе относятся к Windows Server 2003 и Windows XP. сведения о комплектах шифров для Windows Server 2008 и Windows Vista см. в разделе комплекты [шифров в Schannel](cipher-suites-in-schannel.md).

Schannel поддерживает версии 2,0 и 3,0 [*протокола SSL (SSL)*](../secgloss/s-gly.md).

> [!Note]  
> начиная с Windows 10 версии 1607 и Windows Server 2016, протокол SSL 2,0 был удален и больше не поддерживается.

 

## <a name="ssl-30"></a>SSL 3.0

SSL 3,0 является предшественником [протокола](transport-layer-security-protocol.md)TLS.

Schannel поддерживает комплекты шифров, перечисленные в разделе комплекты [шифров TLS](tls-cipher-suites.md) для SSL 3,0. SSL 3,0 поддерживает все комплекты шифров, перечисленные в разделе комплекты шифров TLS, а также SSL \_ Fortezza \_ Кеа \_ с помощью технологии \_ Fortezza \_ CBC \_ SHA.

## <a name="ssl-20"></a>SSL 2.0

Протокол SSL 2,0 был заменен протоколом TLS и не должен использоваться для новой разработки.

Schannel поддерживает следующие комплекты шифров для SSL 2,0. Эти наборы перечислены в порядке от наиболее безопасного до наименьшего уровня безопасности.

-   SSL \_ RC4 \_ 128 \_ с \_ MD5
-   SSL \_ DES \_ 192 \_ EDE3 \_ CBC \_ с \_ MD5
-   SSL \_ RC2 \_ CBC \_ 128 \_ CBC \_ с \_ MD5
-   SSL \_ DES \_ 64 \_ CBC \_ с \_ MD5
-   SSL \_ RC4 \_ 128 \_ EXPORT40 \_ с \_ MD5

 

 
