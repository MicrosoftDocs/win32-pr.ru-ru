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
# <a name="retrieving-a-service-sdo"></a>Получение SDO службы

> [!Note]  
> Служба проверки подлинности в Интернете (IAS) переименовала сервер политики сети (NPS), начиная с Windows Server 2008.

 

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



## <a name="remarks"></a>Комментарии

Необходимо [присоединиться](/windows/desktop/Nps/sdo-attaching-to-an-sdo-enabled-computer) к компьютеру, прежде чем можно будет вызвать любой из методов [**исдомачине**](/windows/desktop/api/sdoias/nn-sdoias-isdomachine) .

## <a name="related-topics"></a>См. также

<dl> <dt>

[Присоединение к SDO-Enabled компьютеру](/windows/desktop/Nps/sdo-attaching-to-an-sdo-enabled-computer)
</dt> <dt>

[**Исдомачине:: Жетсервицесдо**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getservicesdo)
</dt> <dt>

[**исдосервицеконтрол**](/windows/desktop/api/sdoias/nn-sdoias-isdoservicecontrol)
</dt> </dl>

 

 