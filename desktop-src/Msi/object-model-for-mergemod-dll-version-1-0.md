---
description: Объектная модель для Mergemod.dll версии 1,0.
ms.assetid: f4180fd6-23a2-4cd9-b309-016f7333e381
title: Объектная модель для Mergemod.dll версии 1,0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a53c3bc1cae79d1280172265fe0c1bce665a488a89a00f3367cf69455a68d210
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118943350"
---
# <a name="object-model-for-mergemoddll-version-10"></a>Объектная модель для Mergemod.dll версии 1,0

Объектная модель для Mergemod.dll организована следующим образом:

![Объектная модель для mergemod.dll](images/mergobj.png)

[Объект Merge](merge-object.md) является основным объектом модели. [**Объект GetObjects**](getfiles-object.md) является вторичным объектом. Зависимости представляют собой коллекции [**объектов зависимостей**](dependency-object.md). Ошибки представляют собой коллекции [**объектов ошибок**](error-object.md).

 

 



