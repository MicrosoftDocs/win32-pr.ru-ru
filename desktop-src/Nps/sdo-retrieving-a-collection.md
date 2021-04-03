---
title: Получение коллекции
description: Получение коллекции
ms.assetid: b9090ad5-564c-4f48-b7bd-24617d582d2e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 517acfa320069f9c94ee291e9215459d27ba25ad
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103987690"
---
# <a name="retrieving-a-collection"></a>Получение коллекции

> [!Note]  
> Служба проверки подлинности в Интернете (IAS) переименовала сервер политики сети (NPS), начиная с Windows Server 2008. Содержимое этого раздела относится как к IAS, так и к NPS. По всему тексту NPS используется для ссылки на все версии службы, включая версии, изначально называемые IAS.

 

Следующий код извлекает коллекцию клиентов для сервера политики сети.


```C++
// Retrieve the clients collection 
   HRESULT hr;
   CComPtr<ISdo>  pSdo;
   hr = pSdoServiceControl->QueryInterface(
      __uuidof(ISdo),
      (void**) &pSdo
   );
   if (FAILED(hr))
   {
      return hr;
   }

   //
   // First Retrieve the protocols collection
   //
   _variant_t  vtProtocolsCollection;
   hr = pSdo->GetProperty(
      PROPERTY_IAS_PROTOCOLS_COLLECTION,
      &vtProtocolsCollection
   );
   if (FAILED(hr))
   {
      return hr;
   }

   //
   // Get the ISdoCollection interface 
   // for the object.
   //
   CComPtr<ISdoCollection>  pProtocolsCollection;
   hr = vtProtocolsCollection.pdispVal->QueryInterface(
      __uuidof(ISdoCollection), 
      (void **) &pProtocolsCollection
   );
   if (FAILED(hr))
   {
      return hr;
   }

   //
   // Then retrieve the RADIUS protocol
   //
   CComPtr<IDispatch> pRadiusDispatch;
   _variant_t  vtProtocolName = L"Microsoft Radius Protocol";
   hr = pProtocolsCollection->Item(&vtProtocolName, &pRadiusDispatch);
   if (FAILED(hr))
   {
      return hr;
   }

   CComPtr<ISdo> pRadiusSdo;
   hr = pRadiusDispatch->QueryInterface(      
      __uuidof(ISdo), 
      (void **) &pRadiusSdo
   );

   if (FAILED(hr))
   {
      return hr;
   }

   //
   // Then retrieve the clients collection
   //
   _variant_t  vtClientsCollection;
   hr = pRadiusSdo->GetProperty(PROPERTY_RADIUS_CLIENTS_COLLECTION, &vtClientsCollection);
   if (FAILED(hr))
   {
      return hr;
   }

   CComPtr<ISdoCollection> pClientsCollection;
   hr = vtClientsCollection.pdispVal->QueryInterface(      
      __uuidof(ISdoCollection), 
      (void **) &pClientsCollection
   );

   if (FAILED(hr))
   {
      return hr;
   }

```



## <a name="remarks"></a>Комментарии

Переменная Псдосервицеконтрол содержит указатель на объект данных сервера для NPS. Дополнительные сведения см. в разделе [Получение службы SDO](/windows/desktop/Nps/sdo-retrieving-a-service-sdo).

Переменная Втклиентсколлектион имеет тип [ \_ Variant \_ t](/previous-versions/visualstudio/visual-studio-6.0/aa278648(v=vs.60)). \_Объект Variant \_ t инкапсулирует или заключает тип данных [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) . Класс управляет выделением и освобождением ресурсов и делает вызовы функций в [**вариантинит**](/windows/win32/api/oleauto/nf-oleauto-variantinit) и [**вариантклеар**](/windows/win32/api/oleauto/nf-oleauto-variantclear) соответствующим образом.

После вызова "Псдо->GetObject ()" переменная Втпротоколсколлектион указывает объект. Элемент **пдиспвал** объекта втпротоколсколлектион содержит указатель на интерфейс [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) для объекта.

Приведенный выше пример кода можно адаптировать для получения других коллекций NPS, например для коллекций обработчиков запросов NPS. Тип перечисления [**иаспропертиес**](/windows/desktop/api/sdoias/ne-sdoias-iasproperties) перечисляет значения, соответствующие доступным коллекциям NPS.

## <a name="related-topics"></a>См. также

<dl> <dt>

[\_вариант \_ t](/previous-versions/visualstudio/visual-studio-6.0/aa278648(v=vs.60))
</dt> <dt>

[**иаспропертиес**](/windows/desktop/api/sdoias/ne-sdoias-iasproperties)
</dt> <dt>

[**Исдо:: Property**](/windows/desktop/api/sdoias/nf-sdoias-isdo-getproperty)
</dt> <dt>

[**исдоколлектион**](/windows/desktop/api/sdoias/nn-sdoias-isdocollection)
</dt> <dt>

[Получение SDO службы](/windows/desktop/Nps/sdo-retrieving-a-service-sdo)
</dt> <dt>

[**вариантклеар**](/windows/win32/api/oleauto/nf-oleauto-variantclear)
</dt> <dt>

[**вариантинит**](/windows/win32/api/oleauto/nf-oleauto-variantinit)
</dt> <dt>

[**ЗНАЧЕНИЕ**](/windows/win32/api/oaidl/ns-oaidl-variant)
</dt> </dl>

 

 