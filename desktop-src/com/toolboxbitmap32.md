---
title: ToolBoxBitmap32
description: Определяет имя модуля и идентификатор ресурса для точечного рисунка размером 16 x 16, который будет использоваться для кнопки панели инструментов или панели элементов.
ms.assetid: 87b3d8e1-4d54-465c-9e5e-5e4f7391f313
keywords:
- COM раздела реестра ToolBoxBitmap32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d596c758cb6cc0cc34d4c4fc7b73dfe001345ef660f8d62e0268f65a69cfd0f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117917943"
---
# <a name="toolboxbitmap32"></a>ToolBoxBitmap32

Определяет имя модуля и идентификатор ресурса для точечного рисунка размером 16 x 16, который будет использоваться для кнопки панели инструментов или панели элементов.

## <a name="registry-entry"></a>Запись реестра

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      ToolBoxBitmap32 = filename,  resourceID
```

## <a name="remarks"></a>Remarks

Это значение **reg \_ SZ** , которое указывает имя модуля и идентификатор ресурса для точечного рисунка.

размер значка стандартного Windows слишком велик для использования в этой цели. Для этого требуются контейнеры элементов управления, имеющие режим конструктора, в котором один выбирает элементы управления и помещает их в разрабатываемую форму.

 

 




