---
title: мискстатус
description: Указывает, как создать и отобразить объект.
ms.assetid: 585b2d1e-3edb-494e-a61e-bbfa6eae2ba1
keywords:
- COM раздела реестра Мискстатус
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41aa5a5ab7f777eb6aa19d919c69ca219c9364cd1d6e5e9471cb677300d4ebb5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992354"
---
# <a name="miscstatus"></a>мискстатус

Указывает, как создать и отобразить объект.

## <a name="registry-entry"></a>Запись реестра

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      MiscStatus
         (Default) = value
         aspect = value
```

## <a name="remarks"></a>Remarks

Дополнительные сведения см. в разделе Перечисление [**олемиск**](/windows/win32/api/oleidl/ne-oleidl-olemisc) и [**Иолеобжект:: жетмискстатус**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getmiscstatus).

Если подраздел, соответствующий ДВАСПЕКТ, не найден, используется значение по умолчанию **мискстатус** .

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**Иолеобжект:: Жетмискстатус**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getmiscstatus)
</dt> </dl>

 

 




