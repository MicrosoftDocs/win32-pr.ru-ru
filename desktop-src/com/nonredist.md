---
title: нонредист
description: Добавляет имена в список файлов, которые не должны экспортироваться при упаковке приложений COM+ для установки на других компьютерах. Обратите внимание, что это подраздел, а не значение.
ms.assetid: c50e20e4-1a25-4978-ab84-8f7b4b2f6069
keywords:
- COM-значение реестра НОНРЕДИСТ
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d537208ecaf98cec46591966e4ae7d9c205850a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068665"
---
# <a name="nonredist"></a><span data-ttu-id="b9320-105">нонредист</span><span class="sxs-lookup"><span data-stu-id="b9320-105">NONREDIST</span></span>

<span data-ttu-id="b9320-106">Добавляет имена в список файлов, которые не должны экспортироваться при упаковке приложений COM+ для установки на других компьютерах.</span><span class="sxs-lookup"><span data-stu-id="b9320-106">Adds names to the list of files that should not be exported when COM+ applications are packaged for installation on other computers.</span></span> <span data-ttu-id="b9320-107">Обратите внимание, что это подраздел, а не значение.</span><span class="sxs-lookup"><span data-stu-id="b9320-107">Note that this is a subkey, not a value.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="b9320-108">Запись реестра</span><span class="sxs-lookup"><span data-stu-id="b9320-108">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   NONREDIST
      name1
      name2
```

## <a name="remarks"></a><span data-ttu-id="b9320-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b9320-109">Remarks</span></span>

<span data-ttu-id="b9320-110">Файлы, добавляемые в список, представлены парами «имя-значение», которые хранятся в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="b9320-110">The files you add to the list are represented by name/value pairs stored under this key.</span></span> <span data-ttu-id="b9320-111">В каждой паре «имя-значение» именем является имя файла, а значение зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="b9320-111">In each name/value pair, the name is the file name and the value is reserved.</span></span>

 

 




