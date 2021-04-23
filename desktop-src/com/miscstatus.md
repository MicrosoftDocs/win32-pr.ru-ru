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
# <a name="miscstatus"></a><span data-ttu-id="0223e-104">мискстатус</span><span class="sxs-lookup"><span data-stu-id="0223e-104">MiscStatus</span></span>

<span data-ttu-id="0223e-105">Указывает, как создать и отобразить объект.</span><span class="sxs-lookup"><span data-stu-id="0223e-105">Specifies how to create and display an object.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="0223e-106">Запись реестра</span><span class="sxs-lookup"><span data-stu-id="0223e-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      MiscStatus
         (Default) = value
         aspect = value
```

## <a name="remarks"></a><span data-ttu-id="0223e-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0223e-107">Remarks</span></span>

<span data-ttu-id="0223e-108">Дополнительные сведения см. в разделе Перечисление [**олемиск**](/windows/win32/api/oleidl/ne-oleidl-olemisc) и [**Иолеобжект:: жетмискстатус**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getmiscstatus).</span><span class="sxs-lookup"><span data-stu-id="0223e-108">For more information, see the [**OLEMISC**](/windows/win32/api/oleidl/ne-oleidl-olemisc) enumeration and [**IOleObject::GetMiscStatus**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getmiscstatus).</span></span>

<span data-ttu-id="0223e-109">Если подраздел, соответствующий ДВАСПЕКТ, не найден, используется значение по умолчанию **мискстатус** .</span><span class="sxs-lookup"><span data-stu-id="0223e-109">If no subkey that corresponds to a DVASPECT is found, the default value of **MiscStatus** is used.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0223e-110">См. также</span><span class="sxs-lookup"><span data-stu-id="0223e-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0223e-111">**Иолеобжект:: Жетмискстатус**</span><span class="sxs-lookup"><span data-stu-id="0223e-111">**IOleObject::GetMiscStatus**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getmiscstatus)
</dt> </dl>

 

 




