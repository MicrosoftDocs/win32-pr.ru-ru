---
title: Создание новых интерфейсов для одного и того же объекта
description: Создание новых интерфейсов для одного и того же объекта
ms.assetid: 127c44b6-51a6-4fd6-9edc-9fbe0d08d458
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b641eed3918af3acbf399427ad5f7427112f399
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105661565"
---
# <a name="create-new-interfaces-to-the-same-object"></a><span data-ttu-id="8c355-103">Создание новых интерфейсов для одного и того же объекта</span><span class="sxs-lookup"><span data-stu-id="8c355-103">Create New Interfaces to the Same Object</span></span>

<span data-ttu-id="8c355-104">В этом сценарии сервер отвечает на каждый запрос [**\_ клиента OBJID**](object-identifiers.md) , получая новый указатель интерфейса на тот же объект.</span><span class="sxs-lookup"><span data-stu-id="8c355-104">In this scenario, the server responds to each [**OBJID\_CLIENT**](object-identifiers.md) request by obtaining a new interface pointer to the same object.</span></span>

<span data-ttu-id="8c355-105">В следующем примере кода *m \_ пуиобж* является указателем на объект, поддерживающий более одного интерфейса модели объектов Component (com).</span><span class="sxs-lookup"><span data-stu-id="8c355-105">In the following example code, *m\_pUIObj* is a pointer to an object that supports more than one Component Object Model (COM) interface.</span></span> <span data-ttu-id="8c355-106">Несмотря на то, что существующий объект используется повторно, новый указатель интерфейса создается при каждом извлечении объекта, поэтому счетчик ссылок должен быть уменьшен.</span><span class="sxs-lookup"><span data-stu-id="8c355-106">Even though an existing object is reused, a new interface pointer is created each time the object is retrieved, so the reference count must be decremented.</span></span>


```C++
case WM_GETOBJECT:
   if ((DWORD)lParam == OBJID_CLIENT)
   {
      // Get a new interface to the same object. 
      IAccessible *pAcc = NULL;
      // The following increments the reference count. 
      m_pUIObj->QueryInterface(IID_IAccessible, (LPVOID*)&pAcc); 
      LRESULT lAcc = LresultFromObject(IID_IAccessible, wParam, 
            (LPUNKNOWN) &pAcc); 
      // Release our reference to the object.             
      pAcc->Release();               
      return lAcc;
   }
   break;  // Fall through to DefWindowProc. 
   
```



 

 




