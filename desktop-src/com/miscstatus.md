---
title: мискстатус
description: Указывает, как создать и отобразить объект.
ms.assetid: 585b2d1e-3edb-494e-a61e-bbfa6eae2ba1
keywords:
- COM раздела реестра Мискстатус
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abee49776577df61dc8b7d4e94a0621dfdd8b216
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068202"
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

## <a name="remarks"></a>Комментарии

Дополнительные сведения см. в разделе Перечисление [**олемиск**](/windows/win32/api/oleidl/ne-oleidl-olemisc) и [**Иолеобжект:: жетмискстатус**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getmiscstatus).

Если подраздел, соответствующий ДВАСПЕКТ, не найден, используется значение по умолчанию **мискстатус** .

## <a name="related-topics"></a>См. также

<dl> <dt>

[**Иолеобжект:: Жетмискстатус**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getmiscstatus)
</dt> </dl>

 

 




