---
description: После получения обработчика файла с помощью вызова функции Сетупопенфилекуеуе можно добавить файловые операции в очередь, файлы по файлу или постановку в очередь всех файлов в разделе INF.
ms.assetid: ba2f40cd-b0df-4768-8080-4fd80c50f2c2
title: Файлы очереди
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc7b5ab9a9be136e50547076c8daf9bd519ade72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910039"
---
# <a name="queuing-files"></a>Файлы очереди

После получения обработчика файла с помощью вызова функции [**сетупопенфилекуеуе**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue) можно добавить файловые операции в очередь, файлы по файлу или постановку в очередь всех файлов в разделе INF.

Чтобы добавить операцию копирования для отдельного файла в очередь файлов, вызовите функцию [**сетупкуеуекопи**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopya) . Если требуется поставить в очередь операцию копирования файлов с использованием исходного носителя по умолчанию и целевых объектов, указанных в INF-файле, можно вызвать функцию [**сетупкуеуедефаулткопи**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedefaultcopya) .

Можно добавить отдельный файл операция удаления или переименования в очередь открытия файлов, вызвав функцию [**сетупкуеуеделете**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedeletea) или [**сетупкуеуеренаме**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuerenamea) .

 

 



