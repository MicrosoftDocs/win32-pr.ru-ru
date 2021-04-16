---
title: Протокол
description: Указывает, что этот класс OLE 2 может быть вставлен в контейнеры OLE 1.
ms.assetid: 320dff51-ac27-42f3-8c0f-353b29e289d9
keywords:
- Раздел реестра протокола COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 176cb3fce826a6416270fc35a902621521341e6a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105710111"
---
# <a name="protocol"></a><span data-ttu-id="aff13-104">Протокол</span><span class="sxs-lookup"><span data-stu-id="aff13-104">Protocol</span></span>

<span data-ttu-id="aff13-105">Указывает, что этот класс OLE 2 может быть вставлен в контейнеры OLE 1.</span><span class="sxs-lookup"><span data-stu-id="aff13-105">Indicates that this OLE 2 class is insertable in OLE 1 containers.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="aff13-106">Запись реестра</span><span class="sxs-lookup"><span data-stu-id="aff13-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes
   {ProgID}
      Protocol
         StdFileEditing
            Server = path
            Verb
               0 = verb1
               1 = verb2
               ...
```

## <a name="remarks"></a><span data-ttu-id="aff13-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="aff13-107">Remarks</span></span>

<span data-ttu-id="aff13-108">Запись **стдфилидитинг** указывает сведения о совместимости OLE 1.</span><span class="sxs-lookup"><span data-stu-id="aff13-108">The **StdFileEditing** entry specifies OLE 1 compatibility information.</span></span> <span data-ttu-id="aff13-109">Он должен присутствовать только в том случае, если объекты этого класса можно вставлять в контейнеры OLE 1.</span><span class="sxs-lookup"><span data-stu-id="aff13-109">It should be present only if objects of this class are insertable in OLE 1 containers.</span></span>

<span data-ttu-id="aff13-110">**Server** указывает полный путь к приложению сервера OLE 2, а **глагол** задает команды.</span><span class="sxs-lookup"><span data-stu-id="aff13-110">**Server** specifies the full path to the OLE 2 server application and **Verb** specifies the verbs.</span></span> <span data-ttu-id="aff13-111">Глагол 0 является первичной командой, а дополнительные команды должны быть пронумерованы последовательно.</span><span class="sxs-lookup"><span data-stu-id="aff13-111">Verb 0 is the primary verb and additional verbs must be numbered consecutively.</span></span>

 

 




