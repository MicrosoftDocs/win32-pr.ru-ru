---
title: Control
description: Определяет объект как элемент управления ActiveX.
ms.assetid: 2487e642-1d21-4811-87dd-b280be98a44b
keywords:
- Управление ключом реестра COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3722d85b38399d7e95f226749bda45ccc82d1369
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411391"
---
# <a name="control"></a><span data-ttu-id="8e037-104">Control</span><span class="sxs-lookup"><span data-stu-id="8e037-104">Control</span></span>

<span data-ttu-id="8e037-105">Определяет объект как элемент управления ActiveX.</span><span class="sxs-lookup"><span data-stu-id="8e037-105">Identifies an object as an ActiveX Control.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="8e037-106">Запись реестра</span><span class="sxs-lookup"><span data-stu-id="8e037-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      Control
```

## <a name="remarks"></a><span data-ttu-id="8e037-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8e037-107">Remarks</span></span>

<span data-ttu-id="8e037-108">Эта необязательная запись используется контейнерами для заполнения диалоговых окон.</span><span class="sxs-lookup"><span data-stu-id="8e037-108">This optional entry is used by containers to fill in dialog boxes.</span></span> <span data-ttu-id="8e037-109">Контейнер использует этот подраздел, чтобы определить, следует ли включать объект в диалоговое окно, в котором отображаются элементы управления ActiveX.</span><span class="sxs-lookup"><span data-stu-id="8e037-109">The container uses this subkey to determine whether to include an object in a dialog box that displays ActiveX Controls.</span></span> <span data-ttu-id="8e037-110">Элемент управления может опускать эту запись, если она предназначена для работы только с конкретным контейнером и поэтому не предназначена для вставки в другие контейнеры.</span><span class="sxs-lookup"><span data-stu-id="8e037-110">A control can omit this entry if it is designed to work only with a specific container and therefore does is not intended to be inserted in other containers.</span></span>

 

 




