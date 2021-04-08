---
title: Предоставление собственного интерфейса объектной модели
description: Если элемент пользовательского интерфейса поддерживает собственную объектную модель, отличную от Microsoft Active Accessibility или модели автоматизации пользовательского интерфейса, он может предоставить пользовательский интерфейс, реагируя на \_ сообщения WM GetObject, которые содержат \_ идентификатор объекта нативеом OBJID.
ms.assetid: 430abeaf-e5ca-48c4-aa35-8d52a8cee2f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e52543908e89a1cea57c981d60bf7cb2b9fbd1fb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068204"
---
# <a name="exposing-a-native-object-model-interface"></a>Предоставление собственного интерфейса объектной модели

Если элемент пользовательского интерфейса поддерживает собственную объектную модель, отличную от Microsoft Active Accessibility или модели автоматизации пользовательского интерфейса, он может предоставить пользовательский интерфейс, реагируя на сообщения [**WM \_ GetObject**](wm-getobject.md) , которые содержат идентификатор объекта [**\_ нативеом OBJID**](object-identifiers.md) . Для ответа элемент пользовательского интерфейса должен возвращать значение, полученное при вызове функции [**функции lresultfromobject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) .

Клиент может получить интерфейс из элемента пользовательского интерфейса, поддерживающего собственную объектную модель, вызвав функцию [**акцессиблеобжектфромвиндов**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) и указав [**OBJID \_ нативеом**](object-identifiers.md) в качестве второго параметра.

 

 




