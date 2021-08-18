---
description: Базовый механизм визуализации
ms.assetid: 0a4fcf2a-dbad-4211-9a85-7741c8dfc95e
title: Базовый механизм визуализации
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8a3e04e1ad32c163db93794e075ff7933f041c3270ab8412cbd5b5a68b4a763
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955580"
---
# <a name="basic-render-engine"></a>Базовый механизм визуализации

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

Базовый объект модуля рендеринга отображает несжатые выходные данные из временной шкалы. Чтобы создать этот объект, вызовите **CoCreateInstance**. Для сжатых выходных данных используйте интеллектуальный механизм визуализации. Идентификатор класса — CLSID \_ рендеренгине.

Базовый механизм визуализации предоставляет следующие интерфейсы:

-   [**иамсетеррорлог**](iamseterrorlog.md)
-   IObjectWithSite
-   [**ирендеренгине**](irenderengine.md)
-   [**IRenderEngine2**](irenderengine2.md)

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Подготовка Project](rendering-a-project.md)
</dt> <dt>

[Модуль интеллектуального просмотра](smart-render-engine.md)
</dt> </dl>

 

 



