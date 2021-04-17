---
description: Очередь файловых операций полезна, так как позволяет обрабатывать установку в целом, а не в разделе INF.
ms.assetid: 6519c2fb-142d-4071-865f-c00a98c2fe35
title: Создание операций с очередью и файлами в очереди
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f344e9d1c36ecac2d3cd3293196e1d08ff81a05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663564"
---
# <a name="creating-a-queue-and-queuing-file-operations"></a>Создание операций с очередью и файлами в очереди

Очередь файловых операций полезна, так как позволяет обрабатывать установку в целом, а не в разделе INF.

Чтобы создать очередь файлов, объявите переменную для хранения маркера очереди, а затем вызовите функцию [**сетупопенфилекуеуе**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue) . После создания очереди можно ставить в очередь операции копирования, переименования и удаления, а также сканировать очередь файлов для проверки операций, поставленных в очередь.

Чтобы добавить операции с отдельными файлами в очередь, используйте функции [**сетупкуеуекопи**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopya), [**сетупкуеуеренаме**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuerenamea)и [**сетупкуеуеделете**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedeletea) .

Все операции с файлами, перечисленные в разделе **копирование файлов**, **Удаление файлов** или **Переименование файлов** , можно добавить в очередь с помощью [**сетупкуеуекописектион**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopysectiona), [**сетупкуеуеделетесектион**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedeletesectiona)или [**сетупкуеуеренамесектион**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuerenamesectiona)соответственно.

Другой способ поставить в очередь все файлы в разделах " **копирование файлов** ", перечисленных в разделе " **Установка** " INF-файла, — использовать функцию [**сетупинсталлфилесфроминфсектион**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilesfrominfsectiona).

В следующем примере функция [**сетупкуеуекописектион**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopysectiona) используется для постановки в очередь операций копирования для всех файлов, перечисленных в разделе " **копирование файлов** " INF-файла.

``` syntax
test = SetupQueueCopySection(
     MyQueue,                  \\Handle to the open queue
     "A:\",                    \\Source root path
     MyInf,                    \\Inf containing the source info
     NULL,                     \\specifies that MyInf contains 
                               \\  the section to copy as well
     MySection,                \\the name of the section to queue
  
                               \\flags specifying the copy style
     SP_COPY_NOSKIP | SP_COPY_NOBROWSE,
);
```

В этом примере MyQueue — это очередь, в которую добавляются операции копирования, "A: \\ " указывает путь к источнику, а минф — маркер открытого INF-файла. Параметр *листинфхандле* имеет значение **null**, указывающее, что раздел для копирования находится в минф. Мисектион — это раздел в Минф, содержащий файлы, которые нужно поместить в очередь для копирования.

Флаги SP \_ Copy \_ unskip и SP \_ Copy \_ OnBrowse были объединены с помощью оператора или, чтобы указать, что пользователю не следует предлагать варианты пропуска или поиска файлов при возникновении ошибок.

 

 



