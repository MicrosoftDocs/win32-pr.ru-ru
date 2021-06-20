---
title: InprocHandler32
description: InprocHandler32 указывает, использует ли приложение настраиваемый обработчик в HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID разделе реестра.
ms.assetid: da611bb6-1f69-449a-9821-e2fbbe413a97
keywords:
- COM раздела реестра InprocHandler32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be73a8b2577a554b0bb8b5ba5a851e630edbf90a
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406007"
---
# <a name="inprochandler32"></a><span data-ttu-id="b62b9-104">InprocHandler32</span><span class="sxs-lookup"><span data-stu-id="b62b9-104">InprocHandler32</span></span>

<span data-ttu-id="b62b9-105">Указывает, использует ли приложение пользовательский обработчик.</span><span class="sxs-lookup"><span data-stu-id="b62b9-105">Specifies whether an application uses a custom handler.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="b62b9-106">Запись реестра</span><span class="sxs-lookup"><span data-stu-id="b62b9-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      InprocHandler32 = handler.dll
```

## <a name="remarks"></a><span data-ttu-id="b62b9-107">Remarks</span><span class="sxs-lookup"><span data-stu-id="b62b9-107">Remarks</span></span>

<span data-ttu-id="b62b9-108">Это значение **reg \_ SZ** , указывающее настраиваемый обработчик, используемый приложением.</span><span class="sxs-lookup"><span data-stu-id="b62b9-108">This is a **REG\_SZ** value that specifies the custom handler used by the application.</span></span> <span data-ttu-id="b62b9-109">Если пользовательский обработчик не используется, для записи следует задать значение Ole32.dll.</span><span class="sxs-lookup"><span data-stu-id="b62b9-109">If a custom handler is not used, the entry should be set to Ole32.dll.</span></span>

<span data-ttu-id="b62b9-110">Если контейнер выполняет поиск пользовательского обработчика в реестре, 16-разрядная версия имеет приоритет с 16-разрядным контейнером, а 32-разрядная версия имеет приоритет с 32-битным контейнером.</span><span class="sxs-lookup"><span data-stu-id="b62b9-110">If a container is searching the registry for a custom handler, the 16-bit version has priority with a 16-bit container and the 32-bit version has priority with a 32-bit container.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b62b9-111">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="b62b9-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b62b9-112">**инпрочандлер**</span><span class="sxs-lookup"><span data-stu-id="b62b9-112">**InprocHandler**</span></span>](inprochandler.md)
</dt> </dl>

 

 




