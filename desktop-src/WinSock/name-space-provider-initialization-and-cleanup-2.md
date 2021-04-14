---
description: Использование Нспстартуп и Нспклеануп для инициализации поставщика пространства имен и очистки в списке SPI для сокетов Windows (Winsock).
ms.assetid: c9f55845-190d-440f-8b27-1be9585137e2
title: Инициализация и очистка поставщика пространства имен
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fedd7b40d79e755262df581c92e1fe3bdbfb06b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541543"
---
# <a name="namespace-provider-initialization-and-cleanup"></a>Инициализация и очистка поставщика пространства имен

-   [**нспстартуп**](/windows/desktop/api/Ws2spi/nf-ws2spi-nspstartup)
-   [**нспклеануп**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspcleanup)

Как и в случае с транспортным SPI, поставщик пространства имен инициализируется вызовом [**нспстартуп**](/windows/desktop/api/Ws2spi/nf-ws2spi-nspstartup) и завершается окончательным вызовом [**нспклеануп**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspcleanup). Вызовы функции Startup могут быть вложенными, но они будут сопоставляться с помощью соответствующих вызовов функции Cleanup. Поставщик должен использовать подсчет ссылок, чтобы определить, когда произошло окончательное обращение к **нспклеануп** .

 

 



