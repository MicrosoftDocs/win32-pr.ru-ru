---
title: Получение объекта из коллекции
description: Получение объекта из коллекции
ms.assetid: df7cbff5-2d09-4031-8f41-3f4eea51598f
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe8d5bfcba8a1671c7824a4b1356e9c8e1dd7567
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104533320"
---
# <a name="retrieving-an-object-from-a-collection"></a>Получение объекта из коллекции

Следующий код получает IP-адрес клиента из коллекции клиентов. Переменная Пклиентсколлектион указывает на интерфейс [**исдоколлектион**](/windows/desktop/api/sdoias/nn-sdoias-isdocollection) для коллекции. Сведения о том, как получить объект коллекции, см. в разделе [Получение коллекции](/windows/desktop/Nps/sdo-retrieving-a-collection) .


```C++
   HRESULT hr
   _variant_t vtClientName = L"Test Client";
   
   //
   // Get the client "Test Client" from the collection of clients
   //
   CComPtr<IDispatch> pFoundClientDispatch;
   hr = pClientsCollection->Item(&vtClientName, &pFoundClientDispatch);
   if (FAILED(hr))
   {
      return hr;
   }

   CComPtr<ISdo> pFoundClientSdo;
   hr = pFoundClientDispatch->QueryInterface(
      __uuidof(ISdo),
      (void **) &pFoundClientSdo
   );
   if (FAILED(hr))
   {
      return hr;
   }

   //
   // Get the IP address of that client 
   //
   _variant_t vtAddress;
   hr = pFoundClientSdo->GetProperty(PROPERTY_CLIENT_ADDRESS ,&vtAddress);
   if (FAILED(hr))
   {
      return hr;
   }
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[**Исдоколлектион:: Item**](/windows/desktop/api/sdoias/nf-sdoias-isdocollection-item)
</dt> <dt>

[Получение коллекции](/windows/desktop/Nps/sdo-retrieving-a-collection)
</dt> <dt>

[**сисаллокстринг**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring)
</dt> <dt>

[**сисфристринг**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring)
</dt> <dt>

[**ЗНАЧЕНИЕ**](/windows/win32/api/oaidl/ns-oaidl-variant)
</dt> </dl>

 

 