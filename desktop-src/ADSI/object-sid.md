---
title: Идентификатор безопасности объекта (поставщик WinNT)
description: Идентификатор безопасности пользователя (SID) можно получить с помощью атрибута objectSID. ObjectSID возвращается в виде массива вариантов символов, образующих строку идентификатора безопасности.
ms.assetid: 15845e6d-ea30-4d6c-9f35-b2abc1a564ba
ms.tgt_platform: multiple
keywords:
- Службы WinNT Provider ADSI, примеры управления пользователями, идентификатор безопасности объекта
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d5d47e939770b9584a85e4e628c5c168901fc1f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067322"
---
# <a name="object-sid-winnt-provider"></a><span data-ttu-id="f4b96-105">Идентификатор безопасности объекта (поставщик WinNT)</span><span class="sxs-lookup"><span data-stu-id="f4b96-105">Object SID (WinNT Provider)</span></span>

<span data-ttu-id="f4b96-106">Идентификатор безопасности пользователя (SID) можно получить с помощью атрибута **objectSid** .</span><span class="sxs-lookup"><span data-stu-id="f4b96-106">The user security identifier (SID) can be retrieved using the **objectSID** attribute.</span></span> <span data-ttu-id="f4b96-107">**ObjectSid** возвращается в виде массива **вариантов** символов, образующих строку идентификатора безопасности.</span><span class="sxs-lookup"><span data-stu-id="f4b96-107">The **objectSID** is returned as a **VARIANT** array of characters that form the SID string.</span></span>

## <a name="example-code"></a><span data-ttu-id="f4b96-108">Пример кода</span><span class="sxs-lookup"><span data-stu-id="f4b96-108">Example Code</span></span>


```VB
sid = usr.Get("objectSID")
For i = LBound(sid) To UBound(sid)
    Debug.Print sid(i)
Next
```



 

 




