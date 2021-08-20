---
description: Помимо операций с файлами в очереди, можно также поставить в очередь все файлы, перечисленные в разделе INF.
ms.assetid: 456e1a19-7e9b-40c8-9295-42bb8f740f58
title: Постановка в очередь раздела INF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c419f23fe48057eec382c83b4da5e219114c186a9b7bc07c04fc5d7088b17e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117964961"
---
# <a name="queuing-an-inf-section"></a>Постановка в очередь раздела INF

Помимо операций с файлами в очереди, можно также поставить в очередь все файлы, перечисленные в разделе INF.

Вы можете поместить в очередь все файлы, перечисленные в разделе " **копирование файлов** " INF-файла, вызвав [**сетупкуеуекописектион**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopysectiona). Чтобы эта функция была успешной, раздел **Copy Files** должен иметь правильный формат, а INF-файл или один из его добавленных файлов должен содержать разделы **саурцедисксфилес** и **саурцедискснамес** .

Аналогично, если вы хотите удалить все файлы, указанные в разделе **Удаление файлов** INF-файла, можно вызвать [**сетупкуеуеделетесектион**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedeletesectiona). Чтобы переименовать все файлы в разделе " **Переименование файлов** " INF-файла, используйте [**сетупкуеуеренамесектион**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuerenamesectiona).

 

 



