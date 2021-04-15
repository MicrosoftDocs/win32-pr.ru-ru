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
# <a name="control"></a>Control

Определяет объект как элемент управления ActiveX.

## <a name="registry-entry"></a>Запись реестра

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      Control
```

## <a name="remarks"></a>Комментарии

Эта необязательная запись используется контейнерами для заполнения диалоговых окон. Контейнер использует этот подраздел, чтобы определить, следует ли включать объект в диалоговое окно, в котором отображаются элементы управления ActiveX. Элемент управления может опускать эту запись, если она предназначена для работы только с конкретным контейнером и поэтому не предназначена для вставки в другие контейнеры.

 

 




