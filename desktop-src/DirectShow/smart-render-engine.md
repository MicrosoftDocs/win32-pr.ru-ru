---
description: Модуль интеллектуального просмотра
ms.assetid: 279be879-9728-4fa1-bdf7-6b48485fc75f
title: Модуль интеллектуального просмотра
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fa727397f21aeba754cfe41f2dc4f9c1da1c91b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105682272"
---
# <a name="smart-render-engine"></a>Модуль интеллектуального просмотра

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

Объект интеллектуального модуля отрисовки визуализирует выходные данные из временной шкалы. Чтобы создать этот объект, вызовите **CoCreateInstance**. Для несжатых выходных данных используйте базовый механизм визуализации. Идентификатор класса — CLSID \_ смартрендеренгине.

Модуль интеллектуального просмотра предоставляет следующие интерфейсы:

-   [**иамсетеррорлог**](iamseterrorlog.md)
-   **IObjectWithSite**
-   [**ирендеренгине**](irenderengine.md)
-   [**IRenderEngine2**](irenderengine2.md)
-   [**исмартрендеренгине**](ismartrenderengine.md)

## <a name="related-topics"></a>См. также

<dl> <dt>

[Подготовка проекта](rendering-a-project.md)
</dt> <dt>

[Базовый механизм визуализации](basic-render-engine.md)
</dt> </dl>

 

 



