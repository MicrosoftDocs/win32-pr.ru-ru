---
title: Хранение наборов свойств
description: Приложения могут предоставлять некоторые данные о состоянии своих документов, чтобы другие приложения могли разыскать и считывать эти данные.
ms.assetid: 2e0b5f6c-da1d-47f2-a50d-1ac7f2f0c45d
keywords:
- Хранение наборов свойств структурированного хранилища
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60710b84b52fcc709f8ba3ad1e930d6f5a50a4cd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103887832"
---
# <a name="storing-property-sets"></a><span data-ttu-id="90dc0-104">Хранение наборов свойств</span><span class="sxs-lookup"><span data-stu-id="90dc0-104">Storing Property Sets</span></span>

<span data-ttu-id="90dc0-105">Приложения могут предоставлять некоторые данные о состоянии своих документов, чтобы другие приложения могли разыскать и считывать эти данные.</span><span class="sxs-lookup"><span data-stu-id="90dc0-105">Applications can expose some of the state data of their documents so that other applications can locate and read that data.</span></span> <span data-ttu-id="90dc0-106">В качестве примера можно привести набор свойств, описывающих автора, заголовок и ключевые слова документа, созданного с помощью текстового процессора, или список шрифтов, используемых в документе.</span><span class="sxs-lookup"><span data-stu-id="90dc0-106">Some examples are a property set describing the author, title, and keywords of a document created with a word processor, or the list of fonts used in a document.</span></span> <span data-ttu-id="90dc0-107">Это средство не ограничено документами. его также можно использовать для внедренных объектов.</span><span class="sxs-lookup"><span data-stu-id="90dc0-107">This facility is not restricted to documents; it can also be used on embedded objects.</span></span> <span data-ttu-id="90dc0-108">Как правило, доступ к наборам свойств должен осуществляться через интерфейсы [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) и [**ипропертистораже**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) , но в этом разделе описан ранее рекомендуемый способ.</span><span class="sxs-lookup"><span data-stu-id="90dc0-108">Generally, access to property sets should be through the [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) and [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) interfaces, but this section describes the previously recommended way.</span></span>

> [!Note]  
> <span data-ttu-id="90dc0-109">При хранении набора свойств, который является внутренним для приложения, вы можете не использовать следующие рекомендации.</span><span class="sxs-lookup"><span data-stu-id="90dc0-109">If storing a property set that is internal to your application, you may not want to use the following guidelines.</span></span> <span data-ttu-id="90dc0-110">Чтобы предоставить свойству значение другие приложения, следуйте приведенным ниже рекомендациям.</span><span class="sxs-lookup"><span data-stu-id="90dc0-110">To expose your property set to other applications, follow these guidelines.</span></span>

 

<span data-ttu-id="90dc0-111">**Сохранение набора свойств в составном файле**</span><span class="sxs-lookup"><span data-stu-id="90dc0-111">**To store a property set in a compound file**</span></span>

1.  <span data-ttu-id="90dc0-112">Создайте экземпляр [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) или [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) на том же уровне структуры хранения, что и его потоки данных.</span><span class="sxs-lookup"><span data-stu-id="90dc0-112">Create an [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) or [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) instance in the same level of the storage structure as its data streams.</span></span> <span data-ttu-id="90dc0-113">Подпишитесь на имя экземпляра **IStorage** или **IStream** с помощью " \\ 005".</span><span class="sxs-lookup"><span data-stu-id="90dc0-113">Follow the name of your **IStorage** or **IStream** instance with "\\005."</span></span> <span data-ttu-id="90dc0-114">Имена потоков и хранилищ, начинающиеся с 0x05, зарезервированы для общих наборов свойств, которые могут совместно использоваться приложениями.</span><span class="sxs-lookup"><span data-stu-id="90dc0-114">Stream and storage names that begin with 0x05 are reserved for common property sets that can be shared among applications.</span></span> <span data-ttu-id="90dc0-115">Кроме того, потоки, начинающиеся с этого значения, имеют ограничение в 256 КБ.</span><span class="sxs-lookup"><span data-stu-id="90dc0-115">Also, streams beginning with that value are limited to 256 KB.</span></span> <span data-ttu-id="90dc0-116">Имена можно выбрать либо из опубликованных имен, либо из форматов, либо путем присвоения свойству значения FMTID и наследования имени из FMTID в соответствии с соглашениями, описанными в разделе [соглашения об именовании объектов хранилища](storage-object-naming-conventions.md).</span><span class="sxs-lookup"><span data-stu-id="90dc0-116">The names can be selected from either published names and formats, or by assigning the property set a FMTID and deriving the name from the FMTID according to the conventions described in [Storage Object Naming Conventions](storage-object-naming-conventions.md).</span></span>
2.  <span data-ttu-id="90dc0-117">Набор свойств может храниться в одном экземпляре [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) или в экземпляре [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) , содержащем несколько потоков и хранилищ.</span><span class="sxs-lookup"><span data-stu-id="90dc0-117">A property set may be stored in a single [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) instance or in an [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) instance containing multiple streams and storages.</span></span> <span data-ttu-id="90dc0-118">В случае экземпляра **IStorage** вложенный поток с именем Content является основным потоком, содержащим значения свойств, где некоторые значения могут быть именами других потоков или экземпляров хранилища в хранилище для этого набора свойств.</span><span class="sxs-lookup"><span data-stu-id="90dc0-118">In the case of an **IStorage** instance, the contained stream named Contents is the primary stream containing property values, where some values may be names of other streams or storage instances within the storage for this property set.</span></span>
3.  <span data-ttu-id="90dc0-119">Укажите идентификатор CLSID класса объекта, который может отображать или предоставлять программный доступ к значениям свойств.</span><span class="sxs-lookup"><span data-stu-id="90dc0-119">Specify the CLSID of the object class that can display or provide programmatic access to the property values.</span></span> <span data-ttu-id="90dc0-120">Если такого класса нет, то для идентификатора CLSID должен быть задан идентификатор формата набора свойств.</span><span class="sxs-lookup"><span data-stu-id="90dc0-120">If there is no such class, the CLSID should be set to the format identifier of the property set.</span></span> <span data-ttu-id="90dc0-121">Для набора свойств, использующего экземпляр [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) , либо установите идентификатор CLSID экземпляра **IStorage** так, чтобы он совпадал со значением, хранящимся в потоке содержимого, или на **CLSID \_ null**; значение в только что созданном экземпляре **IStorage** .</span><span class="sxs-lookup"><span data-stu-id="90dc0-121">For a property set that uses an [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) instance, either set the CLSID of the **IStorage** instance to be the same as that stored in the Contents stream or to **CLSID\_NULL**; the value in a newly created **IStorage** instance.</span></span>
4.  <span data-ttu-id="90dc0-122">Можно указать отображаемые имена, которые формируют содержимое словаря.</span><span class="sxs-lookup"><span data-stu-id="90dc0-122">You have the option of specifying displayable names that form the contents of the dictionary.</span></span>

<span data-ttu-id="90dc0-123">Некоторые приложения могут считывать только реализации наборов свойств, хранимых в виде экземпляров [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) .</span><span class="sxs-lookup"><span data-stu-id="90dc0-123">Some applications can read only implementations of property sets stored as [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) instances.</span></span> <span data-ttu-id="90dc0-124">Приложения должны быть написаны так, что набор свойств может храниться в экземпляре [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) или **IStream** , если только определение набора свойств не указывает иное.</span><span class="sxs-lookup"><span data-stu-id="90dc0-124">Applications should be written to expect that a property set may be stored in either an [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) or **IStream** instance, unless the property set definition indicates otherwise.</span></span> <span data-ttu-id="90dc0-125">Например, определение набора свойств сводных данных указывает, что оно может храниться только в именованном экземпляре **IStream** .</span><span class="sxs-lookup"><span data-stu-id="90dc0-125">For example, the Summary Information property set definition states that it can only be stored in a named **IStream** instance.</span></span> <span data-ttu-id="90dc0-126">В случаях, когда выполняется поиск набора свойств и неизвестно, является ли он хранилищем или потоком, сначала найдите экземпляр **IStream** с именем набора свойств.</span><span class="sxs-lookup"><span data-stu-id="90dc0-126">In cases where you are searching for a property set and do not know whether it is a storage or stream, look for an **IStream** instance with your property set name first.</span></span> <span data-ttu-id="90dc0-127">Если это не удается, найдите экземпляр **IStorage** .</span><span class="sxs-lookup"><span data-stu-id="90dc0-127">If that fails, look for an **IStorage** instance.</span></span>

<span data-ttu-id="90dc0-128">Чтобы лучше понять хранение наборов свойств в реализации [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) , предположим, что существует класс приложений, изменяющий информацию о животных.</span><span class="sxs-lookup"><span data-stu-id="90dc0-128">To better understand storing property sets in an [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) implementation, suppose there is a class of applications that edit information about animals.</span></span> <span data-ttu-id="90dc0-129">Во-первых, \_ для этого набора приложений ОПРЕДЕЛЕН CLSID (CLSID анималапп), чтобы они могли указать, что они понимают наборы свойств, содержащие сведения о животном (**FMTID \_ анималинфо**), а также другие, которые содержат медицинские сведения (**FMTID \_ медикалинфо**).</span><span class="sxs-lookup"><span data-stu-id="90dc0-129">First, a CLSID (CLSID\_AnimalApp) is defined for this set of applications, so they can indicate that they understand property sets that contain animal information (**FMTID\_AnimalInfo**), and others that contain medical information (**FMTID\_MedicalInfo**).</span></span>

``` syntax
IStorage (File): "C:\OLE\REVO.DOC" 
  IStorage: "\005AnimalInfo", CLSID = CLSID_AnimalApp 
    IStream: "Contents" 
      WORD wByteOrder, WORD wFmtVersion, DWORD dwOSVer, 
      CLSID CLSID_AnimalApp, DWORD cSections... 
      ... 
      FMTID = FMTID_AnimalInfo 
      Property: Type = PID_ANIMALTYPE, Type = VT_LPWSTR, 
              Value = L"Dog" 
      Property: Type = PID_ANIMALNAME, Type = VT_LPWSTR, 
              Value = L"Revo" 
      Property: Type = PID_MEDICALHISTORY, Type = VT_STREAMED_OBJECT, 
              Value = "MedicalInfo" 
      ... 
    IStream: "MedicalInfo" 
      WORD wByteOrder, WORD wFmtVersion, DWORD dwOSVer, 
      CLSID CLSID_AnimalApp, DWORD cSections... 
      ... 
      FMTID = CLSID_MedicalInfo 
      Property: Type = PID_VETNAME, Type = VT_LPWSTR, 
              Value = L"Dr. Woof" 
      Property: Type = PID_LASTEXAM, Type = VT_DATE, Value = ...
```

<span data-ttu-id="90dc0-130">Имейте в виду, что идентификаторы CLSID интерфейса [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) и обоих наборов свойств — это **CLSID \_ анималапп**.</span><span class="sxs-lookup"><span data-stu-id="90dc0-130">Be aware that the CLSID of the [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) interface and both property sets is **CLSID\_AnimalApp**.</span></span> <span data-ttu-id="90dc0-131">Это определяет любое приложение, которое может отображать и (или) предоставлять программный доступ к этим наборам свойств.</span><span class="sxs-lookup"><span data-stu-id="90dc0-131">This identifies any application that can display and/or provide programmatic access to these property sets.</span></span> <span data-ttu-id="90dc0-132">Любое приложение может считывать данные в наборах свойств (точки, находящиеся за набором свойств), но только приложения, идентифицируемые с помощью идентификатора класса CLSID \_ анималапп, могут понимать смысл данных в наборах свойств.</span><span class="sxs-lookup"><span data-stu-id="90dc0-132">Any application can read the data within the property sets (the point behind property sets), but only applications identified with the class identifier of CLSID\_AnimalApp can understand the meaning of the data in the property sets.</span></span>

 

 




