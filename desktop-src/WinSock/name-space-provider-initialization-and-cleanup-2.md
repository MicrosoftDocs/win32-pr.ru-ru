---
description: использование нспстартуп и нспклеануп для инициализации и очистки поставщика пространства имен в Windows сокетах (Winsock) SPI.
ms.assetid: c9f55845-190d-440f-8b27-1be9585137e2
title: Инициализация и очистка поставщика пространства имен
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc4007533bb1456268ee3a1110da4681a7041a56ed80c0d9a522790c8a0c9a94
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119612984"
---
# <a name="namespace-provider-initialization-and-cleanup"></a>Инициализация и очистка поставщика пространства имен

-   [**нспстартуп**](/windows/desktop/api/Ws2spi/nf-ws2spi-nspstartup)
-   [**нспклеануп**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspcleanup)

Как и в случае с транспортным SPI, поставщик пространства имен инициализируется вызовом [**нспстартуп**](/windows/desktop/api/Ws2spi/nf-ws2spi-nspstartup) и завершается окончательным вызовом [**нспклеануп**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspcleanup). Вызовы функции Startup могут быть вложенными, но они будут сопоставляться с помощью соответствующих вызовов функции Cleanup. Поставщик должен использовать подсчет ссылок, чтобы определить, когда произошло окончательное обращение к **нспклеануп** .

 

 



