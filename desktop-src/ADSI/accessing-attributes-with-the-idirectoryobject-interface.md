---
title: Доступ к атрибутам с помощью интерфейса Идиректорйобжект
description: Интерфейс Идиректорйобжект предоставляет клиентское приложение, написанное на C и C++ с прямым доступом к объектам службы каталогов.
ms.assetid: 006be48e-222f-4f77-ac91-58830f2b7363
ms.tgt_platform: multiple
keywords:
- Доступ к атрибутам с помощью интерфейса Идиректорйобжект ADSI
- Идиректорйобжект ADSI, доступ к атрибутам с помощью
- ADSI ADSI, использование, использование интерфейса Идиректорйобжект для доступа к атрибутам
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1da62b6a5cf7e1389276475c46faac6455672790
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986129"
---
# <a name="accessing-attributes-with-the-idirectoryobject-interface"></a><span data-ttu-id="92008-106">Доступ к атрибутам с помощью интерфейса Идиректорйобжект</span><span class="sxs-lookup"><span data-stu-id="92008-106">Accessing Attributes With the IDirectoryObject Interface</span></span>

<span data-ttu-id="92008-107">Интерфейс [**идиректорйобжект**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) предоставляет клиентское приложение, написанное на C и C++ с прямым доступом к объектам службы каталогов.</span><span class="sxs-lookup"><span data-stu-id="92008-107">The [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) interface provides a client application written in C and C++ with direct access to directory service objects.</span></span> <span data-ttu-id="92008-108">Интерфейс обеспечивает доступ посредством прямого сетевого протокола, а не через кэш атрибутов ADSI.</span><span class="sxs-lookup"><span data-stu-id="92008-108">The interface enables access by means of a direct network protocol, rather than through the ADSI attribute cache.</span></span> <span data-ttu-id="92008-109">Вместо свойств, поддерживаемых интерфейсом [**iAds**](/windows/desktop/api/Iads/nn-iads-iads) , **идиректорйобжект** предоставляет методы, которые поддерживают критическое подмножество методов обслуживания объекта и предоставляют доступ к его атрибутам.</span><span class="sxs-lookup"><span data-stu-id="92008-109">In place of the properties supported by the [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) interface, **IDirectoryObject** provides methods that support a critical subset of an object's maintenance methods and provide access to its attributes.</span></span> <span data-ttu-id="92008-110">С помощью **идиректорйобжект** клиент может получить или задать любое количество атрибутов объекта с помощью одного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="92008-110">With **IDirectoryObject**, a client can get or set any number of object attributes with one method call.</span></span> <span data-ttu-id="92008-111">В отличие от соответствующих методов автоматизации, которые являются пакетными, эти **идиректорйобжект** выполняются при вызове метода.</span><span class="sxs-lookup"><span data-stu-id="92008-111">Unlike the corresponding Automation methods, which are batched, those of **IDirectoryObject** are executed when called.</span></span> <span data-ttu-id="92008-112">Поскольку методы этого интерфейса не нуждаются в создании экземпляра объекта каталога службы автоматизации, затраты на производительность невелики.</span><span class="sxs-lookup"><span data-stu-id="92008-112">Because methods on this interface do not require creating an instance of an Automation directory object, the performance overhead is small.</span></span>

<span data-ttu-id="92008-113">Клиенты, написанные на языках C и C++, должны использовать методы интерфейса [**идиректорйобжект**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) для оптимизации производительности и использования преимуществ собственных интерфейсов службы каталогов.</span><span class="sxs-lookup"><span data-stu-id="92008-113">Clients written in languages such as C and C++ should use the methods of the [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) interface to optimize performance and take advantage of native directory service interfaces.</span></span> <span data-ttu-id="92008-114">Клиенты автоматизации не могут использовать **идиректорйобжект**.</span><span class="sxs-lookup"><span data-stu-id="92008-114">Automation clients cannot use **IDirectoryObject**.</span></span> <span data-ttu-id="92008-115">Вместо этого они должны использовать интерфейс [**iAds**](/windows/desktop/api/Iads/nn-iads-iads) .</span><span class="sxs-lookup"><span data-stu-id="92008-115">Instead, they should use the [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) interface.</span></span>

<span data-ttu-id="92008-116">Метод [**идиректорйобжект:: жетобжектаттрибутес**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-getobjectattributes) извлекает атрибуты с одним и несколькими значениями.</span><span class="sxs-lookup"><span data-stu-id="92008-116">The [**IDirectoryObject::GetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-getobjectattributes) method retrieves attributes with both single and multiple values.</span></span> <span data-ttu-id="92008-117">Этот метод принимает список запрошенных атрибутов и возвращает структуру [**\_ \_ сведений о attr в ADS**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) .</span><span class="sxs-lookup"><span data-stu-id="92008-117">This method takes a list of requested attributes and returns an [**ADS\_ATTR\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) structure.</span></span> <span data-ttu-id="92008-118">ADSI выделяет эту структуру; вызывающая сторона должна освободить эту память, если она больше не нужна с помощью функции [**фриадсмем**](/windows/desktop/api/Adshlp/nf-adshlp-freeadsmem) .</span><span class="sxs-lookup"><span data-stu-id="92008-118">ADSI allocates this structure; the caller must free this memory when it is no longer required using the [**FreeADsMem**](/windows/desktop/api/Adshlp/nf-adshlp-freeadsmem) function.</span></span>

<span data-ttu-id="92008-119">Порядок возвращаемых значений атрибутов не обязательно совпадает с порядком, в котором были запрошены атрибуты.</span><span class="sxs-lookup"><span data-stu-id="92008-119">The order of returned attribute values is not necessarily the same as the order in which the attributes were requested.</span></span> <span data-ttu-id="92008-120">Поэтому необходимо сравнить имена атрибутов, возвращенные из ADSI.</span><span class="sxs-lookup"><span data-stu-id="92008-120">Therefore, it is necessary to compare the attribute names returned from ADSI.</span></span>

> [!Note]  
> <span data-ttu-id="92008-121">Структура [**\_ \_ сведений attr для ADS**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) не возвращает все запрошенные атрибуты.</span><span class="sxs-lookup"><span data-stu-id="92008-121">The [**ADS\_ATTR\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) structure does not return all of the attributes requested.</span></span> <span data-ttu-id="92008-122">Только те атрибуты, которые содержат значения, являются частью возвращенной структуры.</span><span class="sxs-lookup"><span data-stu-id="92008-122">Only those attributes that contain values are part of the returned structure.</span></span>

 

<span data-ttu-id="92008-123">Число возвращаемых атрибутов определяется параметром *двнумбераттрибутес* , передаваемым методу [**Идиректорйобжект:: жетобжектаттрибутес**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-getobjectattributes) .</span><span class="sxs-lookup"><span data-stu-id="92008-123">The number of attributes returned is determined by the *dwNumberAttributes* parameter passed to the [**IDirectoryObject::GetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-getobjectattributes) method.</span></span>

<span data-ttu-id="92008-124">В следующем примере кода выполняется привязка к объекту и используется метод [**идиректорйобжект:: жетобжектаттрибутес**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-getobjectattributes) для получения атрибутов объекта.</span><span class="sxs-lookup"><span data-stu-id="92008-124">The following code example binds to an object and uses the [**IDirectoryObject::GetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-getobjectattributes) method to retrieve attributes of the object.</span></span>


```C++
HRESULT hr;
IDirectoryObject *pDirObject;

CoInitialize(NULL);

hr = ADsGetObject(
       L"LDAP://CN=Jeff Smith,OU=Users,DC=Fabrikam,DC=com",
       IID_IDirectoryObject, 
       (void**)&pDirObject);

if(SUCCEEDED(hr))
{
  ADS_ATTR_INFO *pAttrInfo = NULL;
  LPWSTR pAttrNames[] = {L"cn", L"title", L"otherTelephone"};
  DWORD dwNumAttr = sizeof(pAttrNames)/sizeof(LPWSTR);
  DWORD dwReturn;

  //////////////////////////////////////////////////
  // Get attribute values requested.
  // Be aware that the order is not necessarily the 
  // same as requested using pAttrNames.
  //////////////////////////////////////////////////
  hr = pDirObject->GetObjectAttributes(pAttrNames, 
                                       dwNumAttr, 
                                       &pAttrInfo, 
                                       &dwReturn);
     
  if(SUCCEEDED(hr))
  {
    for(DWORD idx = 0; idx < dwReturn; idx++)
      {
        if(_wcsicmp(pAttrInfo[idx].pszAttrName, L"cn") == 0)
        {
          if(pAttrInfo[idx].dwADsType == ADSTYPE_CASE_IGNORE_STRING)
          {
            wprintf(L"Common Name: %s\n", 
                    pAttrInfo[idx].pADsValues[0].CaseIgnoreString);
          }
        }
        else if(_wcsicmp(pAttrInfo[idx].pszAttrName, L"title") == 0)
        {
          if(pAttrInfo->dwADsType == ADSTYPE_CASE_IGNORE_STRING)
          {
            wprintf(L"Title: %s\n", 
                    pAttrInfo[idx].pADsValues[0].CaseIgnoreString);
          }
        }
        else if(_wcsicmp(pAttrInfo[idx].pszAttrName, 
                L"otherTelephone") == 0)
        {  
          // Print the multi-valued property, "Other Telephones".
          if(pAttrInfo[idx].dwADsType == ADSTYPE_CASE_IGNORE_STRING)
        {
          wprintf(L"Other Telephones:");
          for(DWORD val = 0; val < pAttrInfo[idx].dwNumValues; val++) 
          {
            wprintf(L"  %s\n", 
                    pAttrInfo[idx].pADsValues[val].CaseIgnoreString);
          }
        }
      }
    }

    FreeADsMem(pAttrInfo);
  }
     
  pDirObject->Release();
}

CoUninitialize();
```



 

 




