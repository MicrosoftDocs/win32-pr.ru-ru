---
title: инпрочандлер
description: Инпрочандлер указывает, использует ли приложение настраиваемый обработчик в HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID разделе реестра.
ms.assetid: b371b331-148b-46f2-a21e-b88b285bcfc9
keywords:
- COM раздела реестра Инпрочандлер
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aea1ca0d5eb5dec58a36578d268d7020a963a95e
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404737"
---
# <a name="inprochandler"></a><span data-ttu-id="94f64-104">инпрочандлер</span><span class="sxs-lookup"><span data-stu-id="94f64-104">InprocHandler</span></span>

<span data-ttu-id="94f64-105">Указывает, использует ли приложение пользовательский обработчик.</span><span class="sxs-lookup"><span data-stu-id="94f64-105">Specifies whether an application uses a custom handler.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="94f64-106">Запись реестра</span><span class="sxs-lookup"><span data-stu-id="94f64-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      InprocHandler = handler.dll
```

## <a name="remarks"></a><span data-ttu-id="94f64-107">Remarks</span><span class="sxs-lookup"><span data-stu-id="94f64-107">Remarks</span></span>

<span data-ttu-id="94f64-108">Это значение **reg \_ SZ** , указывающее настраиваемый обработчик, используемый приложением.</span><span class="sxs-lookup"><span data-stu-id="94f64-108">This is a **REG\_SZ** value that specifies the custom handler used by the application.</span></span> <span data-ttu-id="94f64-109">Если пользовательский обработчик не используется, для записи следует задать значение Ole32.dll.</span><span class="sxs-lookup"><span data-stu-id="94f64-109">If a custom handler is not used, the entry should be set to Ole32.dll.</span></span>

<span data-ttu-id="94f64-110">Если контейнер выполняет поиск пользовательского обработчика в реестре, 16-разрядная версия имеет приоритет с 16-разрядным контейнером, а 32-разрядная версия имеет приоритет с 32-битным контейнером.</span><span class="sxs-lookup"><span data-stu-id="94f64-110">If a container is searching the registry for a custom handler, the 16-bit version has priority with a 16-bit container and the 32-bit version has priority with a 32-bit container.</span></span>

## <a name="related-topics"></a><span data-ttu-id="94f64-111">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="94f64-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="94f64-112">**InprocHandler32**</span><span class="sxs-lookup"><span data-stu-id="94f64-112">**InprocHandler32**</span></span>](inprochandler32.md)
</dt> </dl>

 

 




