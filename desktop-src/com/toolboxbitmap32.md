---
title: ToolBoxBitmap32
description: Определяет имя модуля и идентификатор ресурса для точечного рисунка размером 16 x 16, который будет использоваться для кнопки панели инструментов или панели элементов.
ms.assetid: 87b3d8e1-4d54-465c-9e5e-5e4f7391f313
keywords:
- COM раздела реестра ToolBoxBitmap32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2ca6208586e961c0b6f8fa666c5731bab38faa6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067796"
---
# <a name="toolboxbitmap32"></a><span data-ttu-id="b29f1-104">ToolBoxBitmap32</span><span class="sxs-lookup"><span data-stu-id="b29f1-104">ToolBoxBitmap32</span></span>

<span data-ttu-id="b29f1-105">Определяет имя модуля и идентификатор ресурса для точечного рисунка размером 16 x 16, который будет использоваться для кнопки панели инструментов или панели элементов.</span><span class="sxs-lookup"><span data-stu-id="b29f1-105">Identifies the module name and resource ID for a 16 x 16 bitmap to use for the face of a toolbar or toolbox button.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="b29f1-106">Запись реестра</span><span class="sxs-lookup"><span data-stu-id="b29f1-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      ToolBoxBitmap32 = filename,  resourceID
```

## <a name="remarks"></a><span data-ttu-id="b29f1-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b29f1-107">Remarks</span></span>

<span data-ttu-id="b29f1-108">Это значение **reg \_ SZ** , которое указывает имя модуля и идентификатор ресурса для точечного рисунка.</span><span class="sxs-lookup"><span data-stu-id="b29f1-108">This is a **REG\_SZ** value that specifies the module name and resource identifier for the bitmap.</span></span>

<span data-ttu-id="b29f1-109">Стандартный размер значка Windows слишком велик для использования в этой цели.</span><span class="sxs-lookup"><span data-stu-id="b29f1-109">The standard Windows icon size is too large to be used for this purpose.</span></span> <span data-ttu-id="b29f1-110">Для этого требуются контейнеры элементов управления, имеющие режим конструктора, в котором один выбирает элементы управления и помещает их в разрабатываемую форму.</span><span class="sxs-lookup"><span data-stu-id="b29f1-110">This requires control containers that have a design mode in which one selects controls and places them on a form being designed.</span></span>

 

 




