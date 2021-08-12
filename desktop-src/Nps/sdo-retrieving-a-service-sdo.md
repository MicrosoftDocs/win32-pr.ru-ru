---
title: Получение SDO службы
description: Получение SDO службы
ms.assetid: bac95c42-8f7e-4011-960c-8f18b4b7c088
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51f1ec3f8537cbf6e9a7be82f8152bc764a263093fe0ebeee46ed1499abfd346
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118618960"
---
# <a name="retrieving-a-service-sdo"></a>Получение SDO службы

> [!Note]  
> служба проверки подлинности в интернете (IAS) переименовала сервер политики сети (NPS), начиная с Windows Server 2008.

 

Следующий код получает объект данных сервера (SDO) для сервера политики сети.


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



## <a name="remarks"></a>Remarks

Необходимо [присоединиться](/windows/desktop/Nps/sdo-attaching-to-an-sdo-enabled-computer) к компьютеру, прежде чем можно будет вызвать любой из методов [**исдомачине**](/windows/desktop/api/sdoias/nn-sdoias-isdomachine) .

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Присоединение к SDO-Enabled компьютеру](/windows/desktop/Nps/sdo-attaching-to-an-sdo-enabled-computer)
</dt> <dt>

[**Исдомачине:: Жетсервицесдо**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getservicesdo)
</dt> <dt>

[**исдосервицеконтрол**](/windows/desktop/api/sdoias/nn-sdoias-isdoservicecontrol)
</dt> </dl>

 

 