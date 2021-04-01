---
title: Получение SDO службы
description: Получение SDO службы
ms.assetid: bac95c42-8f7e-4011-960c-8f18b4b7c088
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afcea1885e0ed714587e99bc7c2dcd92f2fea422
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104260945"
---
# <a name="retrieving-a-service-sdo"></a><span data-ttu-id="2fb31-103">Получение SDO службы</span><span class="sxs-lookup"><span data-stu-id="2fb31-103">Retrieving a Service SDO</span></span>

> [!Note]  
> <span data-ttu-id="2fb31-104">Служба проверки подлинности в Интернете (IAS) переименовала сервер политики сети (NPS), начиная с Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="2fb31-104">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.</span></span>

 

<span data-ttu-id="2fb31-105">Следующий код получает объект данных сервера (SDO) для сервера политики сети.</span><span class="sxs-lookup"><span data-stu-id="2fb31-105">The following code retrieves a Server Data Object (SDO) for the Network Policy Server .</span></span>


```C++
   HRESULT hr;
   CComPtr<IUnknown> pServiceUnknown;
   _bstr_t bstrServiceName = L"IAS";

   hr = pSdoMachine->GetServiceSDO(
      DATA_STORE_LOCAL,
      bstrServiceName,
      (IUnknown**) &pServiceUnknown
   );
   if (FAILED(hr))
   {
      return hr;
   }

   CComPtr<ISdoServiceControl>  pSdoServiceControl;
   hr = pServiceUnknown->QueryInterface(
      __uuidof(ISdoServiceControl),
      (void**) &pSdoServiceControl
   );
   if (FAILED(hr))
   {
      return hr;
   }
```



## <a name="remarks"></a><span data-ttu-id="2fb31-106">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2fb31-106">Remarks</span></span>

<span data-ttu-id="2fb31-107">Необходимо [присоединиться](/windows/desktop/Nps/sdo-attaching-to-an-sdo-enabled-computer) к компьютеру, прежде чем можно будет вызвать любой из методов [**исдомачине**](/windows/desktop/api/sdoias/nn-sdoias-isdomachine) .</span><span class="sxs-lookup"><span data-stu-id="2fb31-107">You must [attach](/windows/desktop/Nps/sdo-attaching-to-an-sdo-enabled-computer) to a computer before you can call any of the [**ISdoMachine**](/windows/desktop/api/sdoias/nn-sdoias-isdomachine) methods.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2fb31-108">См. также</span><span class="sxs-lookup"><span data-stu-id="2fb31-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2fb31-109">Присоединение к SDO-Enabled компьютеру</span><span class="sxs-lookup"><span data-stu-id="2fb31-109">Attaching to an SDO-Enabled Computer</span></span>](/windows/desktop/Nps/sdo-attaching-to-an-sdo-enabled-computer)
</dt> <dt>

[<span data-ttu-id="2fb31-110">**Исдомачине:: Жетсервицесдо**</span><span class="sxs-lookup"><span data-stu-id="2fb31-110">**ISdoMachine::GetServiceSDO**</span></span>](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getservicesdo)
</dt> <dt>

[<span data-ttu-id="2fb31-111">**исдосервицеконтрол**</span><span class="sxs-lookup"><span data-stu-id="2fb31-111">**ISdoServiceControl**</span></span>](/windows/desktop/api/sdoias/nn-sdoias-isdoservicecontrol)
</dt> </dl>

 

 