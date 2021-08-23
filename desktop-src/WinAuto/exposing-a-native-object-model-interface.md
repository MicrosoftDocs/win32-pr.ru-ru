---
title: Предоставление собственного интерфейса объектной модели
description: Если элемент пользовательского интерфейса поддерживает собственную объектную модель, отличную от Microsoft Active Accessibility или модели автоматизации пользовательского интерфейса, он может предоставить пользовательский интерфейс, реагируя на \_ сообщения WM GetObject, которые содержат \_ идентификатор объекта нативеом OBJID.
ms.assetid: 430abeaf-e5ca-48c4-aa35-8d52a8cee2f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 701ed721e8259aa3b707fa1d7a6f2e80b9da13a3760b9850edef22b169d772e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119644924"
---
# <a name="exposing-a-native-object-model-interface"></a>Предоставление собственного интерфейса объектной модели

Если элемент пользовательского интерфейса поддерживает собственную объектную модель, отличную от Microsoft Active Accessibility или модели автоматизации пользовательского интерфейса, он может предоставить пользовательский интерфейс, реагируя на сообщения [**WM \_ GetObject**](wm-getobject.md) , которые содержат идентификатор объекта [**\_ нативеом OBJID**](object-identifiers.md) . Для ответа элемент пользовательского интерфейса должен возвращать значение, полученное при вызове функции [**функции lresultfromobject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) .

Клиент может получить интерфейс из элемента пользовательского интерфейса, поддерживающего собственную объектную модель, вызвав функцию [**акцессиблеобжектфромвиндов**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) и указав [**OBJID \_ нативеом**](object-identifiers.md) в качестве второго параметра.

 

 




