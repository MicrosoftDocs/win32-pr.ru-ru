---
description: При создании процесса с помощью функции CreateProcess можно указать, что процесс наследует обработчики для мьютексов, событий, семафоров или объектов таймера с помощью \_ структуры АТРИБУТОВ безопасности.
ms.assetid: 36491a5c-7599-4f69-ab76-d3a62261a151
title: Наследование объектов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bab6d2380ac0012e0f1005df2dfc4b820bee82a7974f3ca03d856c7df9fb8446
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119661384"
---
# <a name="object-inheritance"></a>Наследование объектов

При создании процесса с помощью функции [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) можно указать, что процесс наследует обработчики для мьютексов, событий, семафоров или объектов таймера с помощью [**структуры \_ атрибутов безопасности**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) . Маркер, наследуемый процессом, имеет тот же доступ к объекту, что и исходный маркер. Унаследованный обработчик отображается в таблице Handle созданного процесса, но необходимо передать значение этого обработчика в созданный процесс. Это можно сделать, указав значение в качестве аргумента командной строки при вызове **CreateProcess**. Затем созданный процесс использует функцию [**GetCommandLine**](/windows/win32/api/processenv/nf-processenv-getcommandlinea) для получения строки командной строки и преобразует аргумент Handle в пригодный для использования описатель. Дополнительные сведения см. в разделе [Наследование](../procthread/inheritance.md).

 

 
