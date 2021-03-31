---
description: Функция Рунграфандваит для создания оглавления
ms.assetid: f6eac1cf-05c3-48b6-b9b4-02966facdc95
title: Функция Рунграфандваит для создания оглавления
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d14b71454bd8c47ab22f165ba59951037bf669a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263491"
---
# <a name="rungraphandwait-function-for-generating-a-table-of-contents"></a>Функция Рунграфандваит для создания оглавления

Следующая функция является вспомогательной функцией в примере программы, которая обсуждается в разделе [Создание](generating-a-table-of-contents-automatically.md)оглавления автоматически.


```C++
HRESULT RunGraphAndWait(IGraphBuilder* pGraph)
{
   IMediaControl* pControl = NULL;
   HRESULT hr = pGraph->QueryInterface(IID_IMediaControl, (VOID**)&pControl);

   if(SUCCEEDED(hr))
   {
      hr = pControl->Run();

      if(SUCCEEDED(hr))
      {
         IMediaEvent* pEvent = NULL;
         hr = pControl->QueryInterface(IID_IMediaEvent, (VOID**)&pEvent);

         if(SUCCEEDED(hr))
         {
           long eventCode = 0;
           hr = pEvent->WaitForCompletion(INFINITE, &eventCode);
           pEvent->Release();
           pEvent = NULL;
         }
      }

      pControl->Release();
      pControl = NULL;
   }

   return hr;
}
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Автоматическое формирование оглавления](generating-a-table-of-contents-automatically.md)
</dt> </dl>

 

 



