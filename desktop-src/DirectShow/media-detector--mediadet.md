---
description: Детектор мультимедиа (Медиадет)
ms.assetid: 5cdbb6ca-d2c3-4123-b545-198863fed25f
title: Детектор мультимедиа (Медиадет)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a072a5d70cf392a1b81fc8387d976bea1db2ddaa5ca2328df914be96a791d19
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119684974"
---
# <a name="media-detector-mediadet"></a>Детектор мультимедиа (Медиадет)

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

Объект детектора мультимедиа (Медиадет) получает сведения о форматировании и все еще кадры из исходных файлов. для работы средства обнаружения мультимедийных файлов не требуется использовать фильтр Graph Manager. Чтобы создать этот объект, вызовите **CoCreateInstance**. Идентификатор класса — CLSID \_ медиадет.

для чтения Windows файлов мультимедиа™, приложение должно предоставить сертификат программного обеспечения, также называемый ключом. Зарегистрируйте приложение в качестве поставщика ключей через интерфейс **IObjectWithSite** средства обнаружения носителей. дополнительные сведения см. [в разделе разблокировка пакета SDK для Windows Media Format](unlocking-the-windows-media-format-sdk.md).

Объект Медиадет предоставляет следующие интерфейсы:

-   [**имедиадет**](imediadet.md)
-   **IObjectWithSite**

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Работа с источниками](working-with-sources.md)
</dt> </dl>

 

 



