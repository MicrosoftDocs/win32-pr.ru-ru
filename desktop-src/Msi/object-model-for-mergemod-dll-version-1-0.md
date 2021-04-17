---
description: Объектная модель для Mergemod.dll версии 1,0.
ms.assetid: f4180fd6-23a2-4cd9-b309-016f7333e381
title: Объектная модель для Mergemod.dll версии 1,0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7fb8e1fc923e1fd6433e196ba4ff3f8714ca9b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673445"
---
# <a name="object-model-for-mergemoddll-version-10"></a>Объектная модель для Mergemod.dll версии 1,0

Объектная модель для Mergemod.dll организована следующим образом:

![Объектная модель для mergemod.dll](images/mergobj.png)

[Объект Merge](merge-object.md) является основным объектом модели. [**Объект GetObjects**](getfiles-object.md) является вторичным объектом. Зависимости представляют собой коллекции [**объектов зависимостей**](dependency-object.md). Ошибки представляют собой коллекции [**объектов ошибок**](error-object.md).

 

 



