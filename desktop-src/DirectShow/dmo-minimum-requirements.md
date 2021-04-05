---
description: Минимальные требования DMO
ms.assetid: cd342f0f-a3dc-4623-a18f-c45071795ef4
title: Минимальные требования DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1c26267f50619062fb8396f93b7578db4d3d8c4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103990182"
---
# <a name="dmo-minimum-requirements"></a>Минимальные требования DMO

Каждый DMO должен соответствовать следующим минимальным требованиям:

-   Он должен поддерживать агрегирование.
-   Он должен предоставлять интерфейс [**имедиаобжект**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject) .
-   Потоковая модель должна быть "both". Дмос должен работать правильно в среде с свободной потоковой назначением.

Дмос Audio Effect должен поддерживать интерфейс [**имедиаобжектинплаце**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobjectinplace) для использования в DirectMusic и DirectSound.

Следующие интерфейсы описаны в других местах, но они полезны для многих дмос. Однако они не являются обязательными.

-   **ИспеЦифипропертипажес**, **ипропертипаже**. Эти интерфейсы позволяют DMO предоставить страницу свойств, чтобы пользователь установил свойства.
-   **IPersistStream**: этот интерфейс позволяет DMO сохранять свое состояние в постоянное хранилище.
-   [**Иамстреамконфиг**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**иамвидеокомпрессион**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression). Эти интерфейсы позволяют клиенту настроить формат вывода кодировщика и параметры сжатия. (Эти два интерфейса являются частью API DirectShow, но также рекомендуются для дмос.)

## <a name="related-topics"></a>См. также

<dl> <dt>

[Написание DMO](writing-a-dmo.md)
</dt> </dl>

 

 



