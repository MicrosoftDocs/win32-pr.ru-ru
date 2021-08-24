---
title: Перечисление объектов в коллекции
description: Перечисление объектов в коллекции
ms.assetid: 664e4d99-48ed-4948-b816-e92ad1ca3ece
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77b0399a75e9301fcdb5e88e6f30b7e0b2ef66160fa05136ed43b51fa8e80eca
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119742114"
---
# <a name="enumerating-objects-in-a-collection"></a>Перечисление объектов в коллекции

> [!Note]  
> служба проверки подлинности в интернете (IAS) переименовала сервер политики сети (NPS), начиная с Windows Server 2008. Содержимое этого раздела относится как к IAS, так и к NPS. По всему тексту NPS используется для ссылки на все версии службы, включая версии, изначально называемые IAS.

 

Следующий код перечисляет протоколы в коллекции протоколов NPS.


```C++
   HRESULT hr;

   //
   // Retrieve the protocols collection object
   //
   _variant_t vtIASProtocolsCollection;
   hr = pSdo->GetProperty(
      PROPERTY_IAS_PROTOCOLS_COLLECTION,
      &vtIASProtocolsCollection
   );
   if (FAILED(hr))
   {
      return hr;
   }

   //
   // Retrieve the ISdoCollection interface 
   // for the object.
   //
   CComPtr<ISdoCollection> pIASProtocolsCollection;
   hr = vtIASProtocolsCollection.pdispVal->QueryInterface(
      __uuidof(ISdoCollection), 
      (void **) &pIASProtocolsCollection
   );
   if (FAILED(hr))
   {
      return hr;
   }

   //
   // Retrieve the enumeration interface, IEnumVARIANT
   //
   CComPtr<IUnknown> pUnknownProtocol;
   hr = pIASProtocolsCollection->get__NewEnum(&pUnknownProtocol);
   if (FAILED(hr))
   {
      return hr;
   }

   CComPtr<IEnumVARIANT> pEnumProtocols;
   hr = pUnknownProtocol->QueryInterface(
      __uuidof(IEnumVARIANT), 
      (void **) &pEnumProtocols
   );
   if (FAILED(hr))
   {
      return hr;
   }

   //
   // Retrieve the first protocol from the collection
   //
   DWORD      dwRetrieved = 1;
   _variant_t vtProtocol;
   hr = pEnumProtocols->Next(1, &vtProtocol, &dwRetrieved);
   if (FAILED(hr))
   {
      return hr;
   }

   while (hr != S_FALSE) {
      // 
      // Retrieve the name of the protocol
      //
      CComPtr<ISdo> pLocalSdo;
      hr = vtProtocol.pdispVal->QueryInterface(
         __uuidof(ISdo), 
         (void**)&pLocalSdo
      );
      if (FAILED(hr))
      {
         return hr;
      }

      _variant_t vtName;
      hr = pLocalSdo->GetProperty(PROPERTY_SDO_NAME, &vtName);
      if (FAILED(hr))
      {
         return hr;
      }

      vtProtocol.Clear();
      vtName.Clear();

      //
      // Retrieve the next protocol from the collection
      //
      dwRetrieved = 1;
      hr = pEnumProtocols->Next(1, &vtProtocol, &dwRetrieved);
      if (FAILED(hr))
      {
         return hr;
      }
   }

```



## <a name="remarks"></a>Remarks

Переменные Втнаме и Втпротокол типа [ \_ Variant \_ t](/previous-versions/visualstudio/visual-studio-6.0/aa278648(v=vs.60)). Объект [ \_ Variant \_ t](/previous-versions/visualstudio/visual-studio-6.0/aa278648(v=vs.60)) инкапсулирует или заключает тип данных **Variant** . Класс управляет выделением и освобождением ресурсов и делает вызовы функций в [**вариантинит**](/windows/win32/api/oleauto/nf-oleauto-variantinit) и [**вариантклеар**](/windows/win32/api/oleauto/nf-oleauto-variantclear) соответствующим образом.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[\_вариант \_ t](/previous-versions/visualstudio/visual-studio-6.0/aa278648(v=vs.60))
</dt> <dt>

[Добавление клиента](/windows/desktop/Nps/sdo-adding-a-client)
</dt> <dt>

[**иаскоммонпропертиес**](/windows/desktop/api/sdoias/ne-sdoias-iascommonproperties)
</dt> <dt>

[**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant)
</dt> <dt>

[**Исдо:: Property**](/windows/desktop/api/sdoias/nf-sdoias-isdo-getproperty)
</dt> <dt>

[Получение SDO службы](/windows/desktop/Nps/sdo-retrieving-a-service-sdo)
</dt> <dt>

[**вариантклеар**](/windows/win32/api/oleauto/nf-oleauto-variantclear)
</dt> <dt>

[**вариантинит**](/windows/win32/api/oleauto/nf-oleauto-variantinit)
</dt> <dt>

[**ЗНАЧЕНИЕ**](/windows/win32/api/oaidl/ns-oaidl-variant)
</dt> </dl>

 

 