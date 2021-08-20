---
description: Классы RealTimeStylus, GestureRecognizer и DynamicRenderer реализуются как оболочки COM и доступны только в управляемом коде.
ms.assetid: db8f0f25-3650-4843-92e4-af5460841e7e
title: Примечания по реализации для API-интерфейсов Стилусинпут
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c106dd0e940cf6fd9e54235af43901d14e511ead5e8908be56b464c483335b74
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032382"
---
# <a name="implementation-notes-for-the-stylusinput-apis"></a>Примечания по реализации для API-интерфейсов Стилусинпут

Классы [**RealTimeStylus**](realtimestylus-class.md), [GestureRecognizer](/previous-versions/ms575185(v=vs.100))и [DynamicRenderer](/previous-versions/ms575176(v=vs.100)) реализуются как оболочки COM и доступны только в управляемом коде.

Когда объект [**RealTimeStylus**](realtimestylus-class.md), [GestureRecognizer](/previous-versions/ms575185(v=vs.100))или [DynamicRenderer](/previous-versions/ms575176(v=vs.100)) добавляется как подключаемый модуль в объект **RealTimeStylus** , базовые COM-объекты взаимодействуют на уровне com. Поэтому непосредственное обращение к методам интерфейсов [истилуссинкплугин](/previous-versions/ms575201(v=vs.100)) или [истилусасинкплугин](/previous-versions/ms575194(v=vs.100)) не поддерживается. Добавление объекта **RealTimeStylus**, GestureRecognizer или DynamicRenderer в объект **RealTimeStylus** является единственным способом доступа к этим функциям.

 

 
