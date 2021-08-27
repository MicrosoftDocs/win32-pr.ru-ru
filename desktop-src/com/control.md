---
title: Элемент
description: определяет объект как элемент управления ActiveX.
ms.assetid: 2487e642-1d21-4811-87dd-b280be98a44b
keywords:
- Управление ключом реестра COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03aa6a0b131dd5fc2ba10d9aaeabafd06b19b73bb1e9422c28e5bec45ea43cbb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120120514"
---
# <a name="control"></a>Элемент

определяет объект как элемент управления ActiveX.

## <a name="registry-entry"></a>Запись реестра

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      Control
```

## <a name="remarks"></a>Remarks

Эта необязательная запись используется контейнерами для заполнения диалоговых окон. контейнер использует этот подраздел, чтобы определить, следует ли включать объект в диалоговое окно, в котором отображаются элементы управления ActiveX. Элемент управления может опускать эту запись, если она предназначена для работы только с конкретным контейнером и поэтому не предназначена для вставки в другие контейнеры.

 

 




