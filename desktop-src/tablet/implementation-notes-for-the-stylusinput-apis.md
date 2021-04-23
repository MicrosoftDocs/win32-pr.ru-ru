---
description: Классы RealTimeStylus, GestureRecognizer и DynamicRenderer реализуются как оболочки COM и доступны только в управляемом коде.
ms.assetid: db8f0f25-3650-4843-92e4-af5460841e7e
title: Примечания по реализации для API-интерфейсов Стилусинпут
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47150d6a9aff5495e89f30d29929fd7d604f9eed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990952"
---
# <a name="implementation-notes-for-the-stylusinput-apis"></a><span data-ttu-id="8e72e-103">Примечания по реализации для API-интерфейсов Стилусинпут</span><span class="sxs-lookup"><span data-stu-id="8e72e-103">Implementation Notes for the StylusInput APIs</span></span>

<span data-ttu-id="8e72e-104">Классы [**RealTimeStylus**](realtimestylus-class.md), [GestureRecognizer](/previous-versions/ms575185(v=vs.100))и [DynamicRenderer](/previous-versions/ms575176(v=vs.100)) реализуются как оболочки COM и доступны только в управляемом коде.</span><span class="sxs-lookup"><span data-stu-id="8e72e-104">The [**RealTimeStylus**](realtimestylus-class.md), [GestureRecognizer](/previous-versions/ms575185(v=vs.100)), and [DynamicRenderer](/previous-versions/ms575176(v=vs.100)) classes are implemented as COM wrappers and are available only in managed code.</span></span>

<span data-ttu-id="8e72e-105">Когда объект [**RealTimeStylus**](realtimestylus-class.md), [GestureRecognizer](/previous-versions/ms575185(v=vs.100))или [DynamicRenderer](/previous-versions/ms575176(v=vs.100)) добавляется как подключаемый модуль в объект **RealTimeStylus** , базовые COM-объекты взаимодействуют на уровне com.</span><span class="sxs-lookup"><span data-stu-id="8e72e-105">When the [**RealTimeStylus**](realtimestylus-class.md), [GestureRecognizer](/previous-versions/ms575185(v=vs.100)), or [DynamicRenderer](/previous-versions/ms575176(v=vs.100)) object is added as a plug-in to a **RealTimeStylus** object, the underlying COM objects interact on the COM level.</span></span> <span data-ttu-id="8e72e-106">Поэтому непосредственное обращение к методам интерфейсов [истилуссинкплугин](/previous-versions/ms575201(v=vs.100)) или [истилусасинкплугин](/previous-versions/ms575194(v=vs.100)) не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="8e72e-106">Therefore, directly calling the methods of the [IStylusSyncPlugin](/previous-versions/ms575201(v=vs.100)) or [IStylusAsyncPlugin](/previous-versions/ms575194(v=vs.100)) interfaces are not supported.</span></span> <span data-ttu-id="8e72e-107">Добавление объекта **RealTimeStylus**, GestureRecognizer или DynamicRenderer в объект **RealTimeStylus** является единственным способом доступа к этим функциям.</span><span class="sxs-lookup"><span data-stu-id="8e72e-107">Adding the **RealTimeStylus**, GestureRecognizer, or DynamicRenderer object to the **RealTimeStylus** object is the only way to access these features.</span></span>

 

 
