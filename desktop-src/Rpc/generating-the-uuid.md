---
title: Создание UUID
description: Первым шагом в определении интерфейса является использование служебной программы uuidgen для создания универсального уникального идентификатора (UUID).
ms.assetid: 870641b7-affc-4de4-bc7f-4c8ca2873fb6
keywords:
- Удаленный вызов процедур RPC, задачи, создание UUID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e263bfe21c4a564106c0d6328c0de891c18bca1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888303"
---
# <a name="generating-the-uuid"></a><span data-ttu-id="5f5e8-104">Создание UUID</span><span class="sxs-lookup"><span data-stu-id="5f5e8-104">Generating the UUID</span></span>

<span data-ttu-id="5f5e8-105">Первым шагом в определении интерфейса является использование служебной программы **uuidgen** для создания универсального уникального идентификатора (UUID).</span><span class="sxs-lookup"><span data-stu-id="5f5e8-105">The first step in defining the interface is to use the **uuidgen** utility to generate a universally unique identifier (UUID).</span></span> <span data-ttu-id="5f5e8-106">Идентификатор UUID позволяет клиентским и серверным приложениям однозначно находить друг друга.</span><span class="sxs-lookup"><span data-stu-id="5f5e8-106">A UUID enables the client and server applications identify each other.</span></span> <span data-ttu-id="5f5e8-107">Программа **uuidgen** (Uuidgen.exe) автоматически устанавливается при установке пакета SDK для платформы.</span><span class="sxs-lookup"><span data-stu-id="5f5e8-107">The **uuidgen** utility (Uuidgen.exe) is automatically installed when you install the Platform Software Development Kit (SDK).</span></span>

<span data-ttu-id="5f5e8-108">Следующая команда создает UUID и создает файл шаблона с именем Hello. idl.</span><span class="sxs-lookup"><span data-stu-id="5f5e8-108">The following command generates a UUID and creates a template file called Hello.idl.</span></span>

<span data-ttu-id="5f5e8-109">**uuidgen/i/Охелло.ИДЛ**</span><span class="sxs-lookup"><span data-stu-id="5f5e8-109">**uuidgen /i /ohello.idl**</span></span>

<span data-ttu-id="5f5e8-110">Шаблон Hello. idl будет выглядеть так (с другим UUID, конечно).</span><span class="sxs-lookup"><span data-stu-id="5f5e8-110">Your hello.idl template will look like this (with a different UUID, of course).</span></span>

``` syntax
[
    uuid(7a98c250-6808-11cf-b73b-00aa00b677a7),
    version(1.0)
]
interface INTERFACENAME
{
 
}
```

 

 




