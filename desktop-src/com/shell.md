---
title: Оболочка (COM)
description: Предоставляет данные для печати оболочки Windows 3,1 и открытия файлов.
ms.assetid: 15e329f2-ed64-4940-aa00-63edbd283b07
keywords:
- COM-сценарий раздела реестра оболочки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1acf4a62d72892d1cd25a5f2276e71d52ab7f700
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "103800659"
---
# <a name="shell-com"></a><span data-ttu-id="331ff-104">Оболочка (COM)</span><span class="sxs-lookup"><span data-stu-id="331ff-104">Shell (COM)</span></span>

<span data-ttu-id="331ff-105">Предоставляет данные для печати оболочки Windows 3,1 и **открытия файлов** .</span><span class="sxs-lookup"><span data-stu-id="331ff-105">Provides Windows 3.1 shell printing and **File Open** information.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="331ff-106">Запись реестра</span><span class="sxs-lookup"><span data-stu-id="331ff-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes
   {ProgID}
      Shell
         Open
            command = path %1
         Print
            command = path %1
```

## <a name="remarks"></a><span data-ttu-id="331ff-107">Remarks</span><span class="sxs-lookup"><span data-stu-id="331ff-107">Remarks</span></span>

<span data-ttu-id="331ff-108">Эти записи должны предоставить путь и имя файла приложения.</span><span class="sxs-lookup"><span data-stu-id="331ff-108">These entries should provide the path and file name of the application.</span></span>

 

 




