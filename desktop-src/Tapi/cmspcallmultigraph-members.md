---
description: Элементы Кмспкаллмултиграф
ms.assetid: 49451585-3084-4426-8617-79b60eb77518
title: Элементы Кмспкаллмултиграф
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de7ee556efbbdaf679e292b6b3a33b4b0a0b6616
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105673852"
---
# <a name="cmspcallmultigraph-members"></a>Элементы Кмспкаллмултиграф

``` syntax
CMSPArray <THREADPOOLWAITBLOCK>     m_ThreadPoolWaitBlocks;
```

Блоки ожидания хранят сведения о времени ожидания, зарегистрированном в пуле потоков. Он включает дескрипторы ожидания, возвращаемые вызовом [**RegisterWaitForSingleObject**](/windows/desktop/api/winbase/nf-winbase-registerwaitforsingleobject) , и указатель на структуру контекста. Каждый блок в массиве предназначен для графа в одном из объектов потока. Смещение блока в этом массиве совпадает со смещением потока, владеющего графом.

 

 
