---
title: Динамическая сериализация буфера
description: При использовании динамического стиля буфера сериализации буфер маршалинга выделяется заглушкой, а данные кодируются в этот буфер и передаются обратно. При распаковке Вы предоставляете буфер, содержащий данные.
ms.assetid: d2c3805b-47bf-4bca-b904-9414e26dde68
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10c1b97124c502e48c4d3ba18e424770bc936496
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486792"
---
# <a name="dynamic-buffer-serialization"></a>Динамическая сериализация буфера

При использовании динамического стиля буфера сериализации буфер маршалинга выделяется заглушкой, а данные кодируются в этот буфер и передаются обратно. При распаковке Вы предоставляете буфер, содержащий данные.

Динамический стиль буфера для сериализации использует следующие подпрограммы:

-   [**месенкодединбуфферхандлекреате**](/windows/desktop/api/Midles/nf-midles-mesencodedynbufferhandlecreate)
-   [**месдекодебуфферхандлекреате**](/windows/desktop/api/Midles/nf-midles-mesdecodebufferhandlecreate)
-   [**месбуфферхандлересет**](/windows/desktop/api/Midles/nf-midles-mesbufferhandlereset)
-   [**мешандлефри**](/windows/desktop/api/Midles/nf-midles-meshandlefree)

Функция [**месенкодединбуфферхандлекреате**](/windows/desktop/api/Midles/nf-midles-mesencodedynbufferhandlecreate) выделяет память, необходимую для маркера кодирования, а затем инициализирует ее. Приложение может вызвать [**месбуфферхандлересет**](/windows/desktop/api/Midles/nf-midles-mesbufferhandlereset) для повторной инициализации маркера. Он вызывает [**мешандлефри**](/windows/desktop/api/Midles/nf-midles-meshandlefree) для освобождения памяти обработчика. Чтобы создать маркер декодирования, соответствующий маркеру динамической кодировки буфера, используйте [**месдекодебуфферхандлекреате**](/windows/desktop/api/Midles/nf-midles-mesdecodebufferhandlecreate).

 

 




