---
title: инпрочандлер
description: Указывает, использует ли приложение пользовательский обработчик.
ms.assetid: b371b331-148b-46f2-a21e-b88b285bcfc9
keywords:
- COM раздела реестра Инпрочандлер
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a8c19089ece43496465351b44e9faa8793ba893
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411206"
---
# <a name="inprochandler"></a><span data-ttu-id="fc604-104">инпрочандлер</span><span class="sxs-lookup"><span data-stu-id="fc604-104">InprocHandler</span></span>

<span data-ttu-id="fc604-105">Указывает, использует ли приложение пользовательский обработчик.</span><span class="sxs-lookup"><span data-stu-id="fc604-105">Specifies whether an application uses a custom handler.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="fc604-106">Запись реестра</span><span class="sxs-lookup"><span data-stu-id="fc604-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      InprocHandler = handler.dll
```

## <a name="remarks"></a><span data-ttu-id="fc604-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fc604-107">Remarks</span></span>

<span data-ttu-id="fc604-108">Это значение **reg \_ SZ** , указывающее настраиваемый обработчик, используемый приложением.</span><span class="sxs-lookup"><span data-stu-id="fc604-108">This is a **REG\_SZ** value that specifies the custom handler used by the application.</span></span> <span data-ttu-id="fc604-109">Если пользовательский обработчик не используется, для записи следует задать значение Ole32.dll.</span><span class="sxs-lookup"><span data-stu-id="fc604-109">If a custom handler is not used, the entry should be set to Ole32.dll.</span></span>

<span data-ttu-id="fc604-110">Если контейнер выполняет поиск пользовательского обработчика в реестре, 16-разрядная версия имеет приоритет с 16-разрядным контейнером, а 32-разрядная версия имеет приоритет с 32-битным контейнером.</span><span class="sxs-lookup"><span data-stu-id="fc604-110">If a container is searching the registry for a custom handler, the 16-bit version has priority with a 16-bit container and the 32-bit version has priority with a 32-bit container.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fc604-111">См. также</span><span class="sxs-lookup"><span data-stu-id="fc604-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fc604-112">**InprocHandler32**</span><span class="sxs-lookup"><span data-stu-id="fc604-112">**InprocHandler32**</span></span>](inprochandler32.md)
</dt> </dl>

 

 




