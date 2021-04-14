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
# <a name="create-new-interfaces-to-the-same-object"></a>Создание новых интерфейсов для одного и того же объекта

В этом сценарии сервер отвечает на каждый запрос [**\_ клиента OBJID**](object-identifiers.md) , получая новый указатель интерфейса на тот же объект.

В следующем примере кода *m \_ пуиобж* является указателем на объект, поддерживающий более одного интерфейса модели объектов Component (com). Несмотря на то, что существующий объект используется повторно, новый указатель интерфейса создается при каждом извлечении объекта, поэтому счетчик ссылок должен быть уменьшен.


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



 

 




