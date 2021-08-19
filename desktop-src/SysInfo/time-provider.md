---
description: операционная система Microsoft Windows обеспечивает поддержку различных аппаратных устройств и сетевых протоколов, использующих архитектуру поставщика времени.
ms.assetid: a7575373-eeda-4f2a-85e5-d1b50994e7ae
title: Поставщик времени
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67f2073e94bdf893793b4ae1df2974226aa197de4ff429be9ce8f2a2e4b5f597
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117957908"
---
# <a name="time-provider"></a>Поставщик времени

операционная система Microsoft Windows обеспечивает поддержку различных аппаратных устройств и сетевых протоколов, использующих архитектуру *поставщика времени* . Поставщики входного времени получают точные отметки времени от оборудования или сети, а поставщики времени вывода предоставляют метки времени другим клиентам в сети.

Поставщики времени управляются *диспетчером поставщиков времени*. Он отвечает за загрузку, запуск и остановку поставщиков времени, направляемых диспетчером управления службами. Этот интерфейс упрощает написание поставщика времени, чем запись полной службы.

-   [Создание поставщика времени](creating-a-time-provider.md)
-   [Регистрация поставщика времени](registering-a-time-provider.md)
-   [Пример поставщика времени](sample-time-provider.md)

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Служба времени Windows](https://www.microsoft.com/technet/prodtechnol/windowsserver2003/technologies/security/ws03mngd/26_s3wts.mspx)
</dt> </dl>

 

 



