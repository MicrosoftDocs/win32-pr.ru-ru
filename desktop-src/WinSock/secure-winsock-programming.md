---
description: ниже приведено краткое справочное занятие по обеспечению безопасности Windows сокетов.
ms.assetid: 70210e86-ead6-4b0c-ae47-66b2ef0a8d11
title: Безопасное программирование Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2c3644e18a45da4a1d4fa9c20bd2d023ba41d02fed3014f2992c219601bf963
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118559722"
---
# <a name="secure-winsock-programming"></a>Безопасное программирование Winsock

ниже приведено краткое справочное занятие по обеспечению безопасности Windows сокетов. Он предназначен для понимания безопасности Winsock и вариантов, доступных разработчику защищенных сетевых приложений.

-   [Использование \_ реусеаддр и так далее \_ ексклусивеаддрусе](using-so-reuseaddr-and-so-exclusiveaddruse.md)
-   [Расширения безопасных сокетов Winsock](winsock-secure-socket-extensions.md)

Связь с помощью сокетов также может быть зашифрована с помощью стандартов SSL/TLS с помощью защищенного канала, также известного как технология SChannel. Schannel — это поставщик поддержки безопасности (SSP), который содержит набор протоколов безопасности, обеспечивающих проверку подлинности и безопасную закрытую связь с помощью шифрования. Schannel в основном используется для Интернет-приложений, требующих обмена данными по протоколу HTTP. Дополнительные сведения см. в разделе [безопасный канал](../secauthn/secure-channel.md).

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Secure Channel](../secauthn/secure-channel.md)
</dt> </dl>

 

 
