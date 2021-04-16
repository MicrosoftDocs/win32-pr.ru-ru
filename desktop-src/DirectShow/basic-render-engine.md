---
description: Базовый механизм визуализации
ms.assetid: 0a4fcf2a-dbad-4211-9a85-7741c8dfc95e
title: Базовый механизм визуализации
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb9b51240b43c58de99b7d6fe1f7ad61f754c7ed
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537817"
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

## <a name="related-topics"></a>См. также

<dl> <dt>

[Подготовка проекта](rendering-a-project.md)
</dt> <dt>

[Модуль интеллектуального просмотра](smart-render-engine.md)
</dt> </dl>

 

 



