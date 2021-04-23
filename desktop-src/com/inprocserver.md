---
title: инпроксервер
description: Указывает путь к DLL внутрипроцессного сервера.
ms.assetid: f14cc8f7-e93e-4db8-8b0d-ea77a6301f33
keywords:
- COM раздела реестра Инпроксервер
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5682693d711f734bbc60def8a711f11e2bad0ef9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986463"
---
# <a name="inprocserver"></a><span data-ttu-id="6c092-104">инпроксервер</span><span class="sxs-lookup"><span data-stu-id="6c092-104">InprocServer</span></span>

<span data-ttu-id="6c092-105">Указывает путь к DLL внутрипроцессного сервера.</span><span class="sxs-lookup"><span data-stu-id="6c092-105">Specifies the path to the in-process server DLL.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="6c092-106">Запись реестра</span><span class="sxs-lookup"><span data-stu-id="6c092-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      InprocServer
         (Default) = path
```

## <a name="remarks"></a><span data-ttu-id="6c092-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6c092-107">Remarks</span></span>

<span data-ttu-id="6c092-108">Запись **инпроксервер** сравнительно редко используется для вставляемых классов.</span><span class="sxs-lookup"><span data-stu-id="6c092-108">The **InprocServer** entry is relatively rare for insertable classes.</span></span>

<span data-ttu-id="6c092-109">Внутрипроцессный сервер в настоящее время зарегистрирован с помощью записи реестра **инпроксервер** .</span><span class="sxs-lookup"><span data-stu-id="6c092-109">In-process servers are currently registered using the **InprocServer** registry entry.</span></span> <span data-ttu-id="6c092-110">32-разрядные и 64-битные внутрипроцессный серверы должны использовать запись [**InprocServer32**](inprocserver32.md) .</span><span class="sxs-lookup"><span data-stu-id="6c092-110">The 32-bit and 64-bit in-process servers should use the [**InprocServer32**](inprocserver32.md) entry.</span></span> <span data-ttu-id="6c092-111">Если контейнер выполняет поиск в реестре внутрипроцессного сервера, 16-разрядная версия имеет приоритет с 16-разрядным контейнером, а 32-разрядная версия имеет приоритет с 32-битным контейнером.</span><span class="sxs-lookup"><span data-stu-id="6c092-111">If a container is searching the registry for an in-process server, the 16-bit version has priority with a 16-bit container and 32-bit version has priority with a 32-bit container.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6c092-112">См. также</span><span class="sxs-lookup"><span data-stu-id="6c092-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6c092-113">**InprocServer32**</span><span class="sxs-lookup"><span data-stu-id="6c092-113">**InprocServer32**</span></span>](inprocserver32.md)
</dt> </dl>

 

 




