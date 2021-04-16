---
description: Помимо операций с файлами в очереди, можно также поставить в очередь все файлы, перечисленные в разделе INF.
ms.assetid: 456e1a19-7e9b-40c8-9295-42bb8f740f58
title: Постановка в очередь раздела INF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e5566931131885cf6f300b5a6386639bbd564e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546394"
---
# <a name="queuing-an-inf-section"></a>Постановка в очередь раздела INF

Помимо операций с файлами в очереди, можно также поставить в очередь все файлы, перечисленные в разделе INF.

Вы можете поместить в очередь все файлы, перечисленные в разделе " **копирование файлов** " INF-файла, вызвав [**сетупкуеуекописектион**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopysectiona). Чтобы эта функция была успешной, раздел **Copy Files** должен иметь правильный формат, а INF-файл или один из его добавленных файлов должен содержать разделы **саурцедисксфилес** и **саурцедискснамес** .

Аналогично, если вы хотите удалить все файлы, указанные в разделе **Удаление файлов** INF-файла, можно вызвать [**сетупкуеуеделетесектион**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedeletesectiona). Чтобы переименовать все файлы в разделе " **Переименование файлов** " INF-файла, используйте [**сетупкуеуеренамесектион**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuerenamesectiona).

 

 



