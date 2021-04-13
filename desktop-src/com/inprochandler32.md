---
title: InprocHandler32
description: Указывает, использует ли приложение пользовательский обработчик.
ms.assetid: da611bb6-1f69-449a-9821-e2fbbe413a97
keywords:
- COM раздела реестра InprocHandler32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82c918669aa3de1c8cf2622e3caf4acc9ae18f0b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104410724"
---
# <a name="inprochandler32"></a><span data-ttu-id="09675-104">InprocHandler32</span><span class="sxs-lookup"><span data-stu-id="09675-104">InprocHandler32</span></span>

<span data-ttu-id="09675-105">Указывает, использует ли приложение пользовательский обработчик.</span><span class="sxs-lookup"><span data-stu-id="09675-105">Specifies whether an application uses a custom handler.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="09675-106">Запись реестра</span><span class="sxs-lookup"><span data-stu-id="09675-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      InprocHandler32 = handler.dll
```

## <a name="remarks"></a><span data-ttu-id="09675-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="09675-107">Remarks</span></span>

<span data-ttu-id="09675-108">Это значение **reg \_ SZ** , указывающее настраиваемый обработчик, используемый приложением.</span><span class="sxs-lookup"><span data-stu-id="09675-108">This is a **REG\_SZ** value that specifies the custom handler used by the application.</span></span> <span data-ttu-id="09675-109">Если пользовательский обработчик не используется, для записи следует задать значение Ole32.dll.</span><span class="sxs-lookup"><span data-stu-id="09675-109">If a custom handler is not used, the entry should be set to Ole32.dll.</span></span>

<span data-ttu-id="09675-110">Если контейнер выполняет поиск пользовательского обработчика в реестре, 16-разрядная версия имеет приоритет с 16-разрядным контейнером, а 32-разрядная версия имеет приоритет с 32-битным контейнером.</span><span class="sxs-lookup"><span data-stu-id="09675-110">If a container is searching the registry for a custom handler, the 16-bit version has priority with a 16-bit container and the 32-bit version has priority with a 32-bit container.</span></span>

## <a name="related-topics"></a><span data-ttu-id="09675-111">См. также</span><span class="sxs-lookup"><span data-stu-id="09675-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="09675-112">**инпрочандлер**</span><span class="sxs-lookup"><span data-stu-id="09675-112">**InprocHandler**</span></span>](inprochandler.md)
</dt> </dl>

 

 




