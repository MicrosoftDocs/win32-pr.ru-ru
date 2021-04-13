---
title: Присоединение к SDO-Enabled компьютеру
description: Присоединение к SDO-Enabled компьютеру
ms.assetid: 434e2e0c-075e-48a9-9617-bbe75716380d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 729d8c5609691f1d51598701953c795225c08e4b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413037"
---
# <a name="attaching-to-an-sdo-enabled-computer"></a><span data-ttu-id="286f7-103">Присоединение к SDO-Enabled компьютеру</span><span class="sxs-lookup"><span data-stu-id="286f7-103">Attaching to an SDO-Enabled Computer</span></span>

<span data-ttu-id="286f7-104">Следующий код подключается к локальному компьютеру в качестве компьютера SDO.</span><span class="sxs-lookup"><span data-stu-id="286f7-104">The following code attaches to the local computer as an SDO computer.</span></span>


```C++
   HRESULT  hr;
   CComPtr<ISdoMachine> pSdoMachine;
   CLSID    clsid;

   hr = CLSIDFromProgID(TEXT("IAS.SdoMachine"), &clsid);
   if (FAILED(hr))
   {
      return hr;
   }

   hr = CoCreateInstance(
      clsid,
      NULL,
      CLSCTX_INPROC_SERVER,
      __uuidof(ISdoMachine),
      (void**)&pSdoMachine
   );
   if (FAILED(hr))
   {
      return hr;
   }

   //
   // Pass NULL to specify local computer.
   //
   hr = pSdoMachine->Attach(NULL); 
   if (FAILED(hr))
   {
      return hr;
   }

```



<span data-ttu-id="286f7-105">Подключение к компьютеру в качестве компьютера SDO — это первый шаг в администрировании компьютера с помощью SDO.</span><span class="sxs-lookup"><span data-stu-id="286f7-105">Attaching to a computer as an SDO computer is the first step in administering the computer through SDO.</span></span>

<span data-ttu-id="286f7-106">Дополнительные сведения см. в разделе [**исдомачине**](/windows/desktop/api/sdoias/nn-sdoias-isdomachine), [**Исдомачине:: Attach**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-attach).</span><span class="sxs-lookup"><span data-stu-id="286f7-106">For more information, see [**ISdoMachine**](/windows/desktop/api/sdoias/nn-sdoias-isdomachine), [**ISdoMachine::Attach**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-attach).</span></span>

 

 