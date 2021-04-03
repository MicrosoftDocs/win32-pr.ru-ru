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
# <a name="retrieving-a-collection"></a><span data-ttu-id="42c3d-103">Получение коллекции</span><span class="sxs-lookup"><span data-stu-id="42c3d-103">Retrieving a Collection</span></span>

> [!Note]  
> <span data-ttu-id="42c3d-104">Служба проверки подлинности в Интернете (IAS) переименовала сервер политики сети (NPS), начиная с Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="42c3d-104">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.</span></span> <span data-ttu-id="42c3d-105">Содержимое этого раздела относится как к IAS, так и к NPS.</span><span class="sxs-lookup"><span data-stu-id="42c3d-105">The content of this topic applies to both IAS and NPS.</span></span> <span data-ttu-id="42c3d-106">По всему тексту NPS используется для ссылки на все версии службы, включая версии, изначально называемые IAS.</span><span class="sxs-lookup"><span data-stu-id="42c3d-106">Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</span></span>

 

<span data-ttu-id="42c3d-107">Следующий код извлекает коллекцию клиентов для сервера политики сети.</span><span class="sxs-lookup"><span data-stu-id="42c3d-107">The following code retrieves the clients collection for the Network Policy Server.</span></span>


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



## <a name="remarks"></a><span data-ttu-id="42c3d-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="42c3d-108">Remarks</span></span>

<span data-ttu-id="42c3d-109">Переменная Псдосервицеконтрол содержит указатель на объект данных сервера для NPS.</span><span class="sxs-lookup"><span data-stu-id="42c3d-109">The pSdoServiceControl variable contains a pointer to a Server Data Object for NPS.</span></span> <span data-ttu-id="42c3d-110">Дополнительные сведения см. в разделе [Получение службы SDO](/windows/desktop/Nps/sdo-retrieving-a-service-sdo).</span><span class="sxs-lookup"><span data-stu-id="42c3d-110">For more information, see the topic [Retrieving a Service SDO](/windows/desktop/Nps/sdo-retrieving-a-service-sdo).</span></span>

<span data-ttu-id="42c3d-111">Переменная Втклиентсколлектион имеет тип [ \_ Variant \_ t](/previous-versions/visualstudio/visual-studio-6.0/aa278648(v=vs.60)).</span><span class="sxs-lookup"><span data-stu-id="42c3d-111">The vtClientsCollection variable is of type [\_variant\_t](/previous-versions/visualstudio/visual-studio-6.0/aa278648(v=vs.60)).</span></span> <span data-ttu-id="42c3d-112">\_Объект Variant \_ t инкапсулирует или заключает тип данных [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) .</span><span class="sxs-lookup"><span data-stu-id="42c3d-112">A \_variant\_t object encapsulates, or encloses, the [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) data type.</span></span> <span data-ttu-id="42c3d-113">Класс управляет выделением и освобождением ресурсов и делает вызовы функций в [**вариантинит**](/windows/win32/api/oleauto/nf-oleauto-variantinit) и [**вариантклеар**](/windows/win32/api/oleauto/nf-oleauto-variantclear) соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="42c3d-113">The class manages resource allocation and deallocation, and makes function calls to [**VariantInit**](/windows/win32/api/oleauto/nf-oleauto-variantinit) and [**VariantClear**](/windows/win32/api/oleauto/nf-oleauto-variantclear) as appropriate.</span></span>

<span data-ttu-id="42c3d-114">После вызова "Псдо->GetObject ()" переменная Втпротоколсколлектион указывает объект.</span><span class="sxs-lookup"><span data-stu-id="42c3d-114">After the call to "pSdo->GetProperty()", the vtProtocolsCollection variable specifies an object.</span></span> <span data-ttu-id="42c3d-115">Элемент **пдиспвал** объекта втпротоколсколлектион содержит указатель на интерфейс [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) для объекта.</span><span class="sxs-lookup"><span data-stu-id="42c3d-115">The **pdispVal** member of vtProtocolsCollection contains a pointer to the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface for the object.</span></span>

<span data-ttu-id="42c3d-116">Приведенный выше пример кода можно адаптировать для получения других коллекций NPS, например для коллекций обработчиков запросов NPS.</span><span class="sxs-lookup"><span data-stu-id="42c3d-116">The above sample code can be adapted to retrieve other NPS collections, for example the NPS Request Handlers collections.</span></span> <span data-ttu-id="42c3d-117">Тип перечисления [**иаспропертиес**](/windows/desktop/api/sdoias/ne-sdoias-iasproperties) перечисляет значения, соответствующие доступным коллекциям NPS.</span><span class="sxs-lookup"><span data-stu-id="42c3d-117">The [**IASPROPERTIES**](/windows/desktop/api/sdoias/ne-sdoias-iasproperties) enumeration type enumerated values that correspond to the available NPS collections.</span></span>

## <a name="related-topics"></a><span data-ttu-id="42c3d-118">См. также</span><span class="sxs-lookup"><span data-stu-id="42c3d-118">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="42c3d-119">[\_вариант \_ t](/previous-versions/visualstudio/visual-studio-6.0/aa278648(v=vs.60))</span><span class="sxs-lookup"><span data-stu-id="42c3d-119">[\_variant\_t](/previous-versions/visualstudio/visual-studio-6.0/aa278648(v=vs.60))</span></span>
</dt> <dt>

[<span data-ttu-id="42c3d-120">**иаспропертиес**</span><span class="sxs-lookup"><span data-stu-id="42c3d-120">**IASPROPERTIES**</span></span>](/windows/desktop/api/sdoias/ne-sdoias-iasproperties)
</dt> <dt>

[<span data-ttu-id="42c3d-121">**Исдо:: Property**</span><span class="sxs-lookup"><span data-stu-id="42c3d-121">**ISdo::GetProperty**</span></span>](/windows/desktop/api/sdoias/nf-sdoias-isdo-getproperty)
</dt> <dt>

[<span data-ttu-id="42c3d-122">**исдоколлектион**</span><span class="sxs-lookup"><span data-stu-id="42c3d-122">**ISdoCollection**</span></span>](/windows/desktop/api/sdoias/nn-sdoias-isdocollection)
</dt> <dt>

[<span data-ttu-id="42c3d-123">Получение SDO службы</span><span class="sxs-lookup"><span data-stu-id="42c3d-123">Retrieving a Service SDO</span></span>](/windows/desktop/Nps/sdo-retrieving-a-service-sdo)
</dt> <dt>

[<span data-ttu-id="42c3d-124">**вариантклеар**</span><span class="sxs-lookup"><span data-stu-id="42c3d-124">**VariantClear**</span></span>](/windows/win32/api/oleauto/nf-oleauto-variantclear)
</dt> <dt>

[<span data-ttu-id="42c3d-125">**вариантинит**</span><span class="sxs-lookup"><span data-stu-id="42c3d-125">**VariantInit**</span></span>](/windows/win32/api/oleauto/nf-oleauto-variantinit)
</dt> <dt>

[<span data-ttu-id="42c3d-126">**ЗНАЧЕНИЕ**</span><span class="sxs-lookup"><span data-stu-id="42c3d-126">**VARIANT**</span></span>](/windows/win32/api/oaidl/ns-oaidl-variant)
</dt> </dl>

 

 