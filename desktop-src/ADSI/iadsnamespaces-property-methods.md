---
title: Методы свойств Иадснамеспацес (iAds. h)
description: Методы свойств интерфейса Иадснамеспацес получают и задают свойства, описанные в следующей таблице. Дополнительные сведения см. в разделе методы свойств интерфейса.
ms.assetid: fe959741-429e-480a-8111-3ebadaf55f77
ms.tgt_platform: multiple
keywords:
- Методы свойств Иадснамеспацес ADSI
topic_type:
- apiref
api_name:
- IADsNamespaces Property Methods
- IADsNamespaces.DefaultContainer
- IADsNamespaces.get_DefaultContainer
- IADsNamespaces.put_DefaultContainer
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b30467e931d7e8790f9a17542d5da2070525fe0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803172"
---
# <a name="iadsnamespaces-property-methods"></a><span data-ttu-id="c8679-105">Методы свойств Иадснамеспацес</span><span class="sxs-lookup"><span data-stu-id="c8679-105">IADsNamespaces Property Methods</span></span>

<span data-ttu-id="c8679-106">Методы свойств интерфейса [**иадснамеспацес**](/windows/desktop/api/Iads/nn-iads-iadsnamespaces) получают и задают свойства, описанные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="c8679-106">The [**IADsNamespaces**](/windows/desktop/api/Iads/nn-iads-iadsnamespaces) interface property methods get and set the properties described in the following table.</span></span> <span data-ttu-id="c8679-107">Дополнительные сведения см. в разделе [методы свойств интерфейса](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="c8679-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="c8679-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="c8679-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="c8679-109">**DefaultContainer**</span><span class="sxs-lookup"><span data-stu-id="c8679-109">**DefaultContainer**</span></span>
<span data-ttu-id="c8679-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="c8679-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="c8679-111">Свойство **дефаултконтаинер** определяет базовый объект контейнера, к которому можно выполнить привязку и использовать в качестве отправной точки при просмотре.</span><span class="sxs-lookup"><span data-stu-id="c8679-111">The **DefaultContainer** property identifies a base container object to which you can bind and use as a starting point when browsing.</span></span> <span data-ttu-id="c8679-112">Эти данные хранятся и извлекаются из следующего значения реестра.</span><span class="sxs-lookup"><span data-stu-id="c8679-112">This data is stored and retrieved from the following registry value.</span></span>

```
HKEY_CURRENT_USER
   Software
      Microsoft
         ADs
            DefaultContainer
```

<span data-ttu-id="c8679-113">ADSI определяет свойство **дефаултконтаинер** , чтобы обеспечить быстрый способ получения указателя на ранее определенный объект контейнера ADSI.</span><span class="sxs-lookup"><span data-stu-id="c8679-113">ADSI defines the **DefaultContainer** property to provide a quick way of getting a pointer to a previously defined ADSI container object.</span></span>

<dt>

<span data-ttu-id="c8679-114">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="c8679-114">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="c8679-115">Тип данных скрипта: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="c8679-115">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_DefaultContainer(
  [out] BSTR* pbstrDefault
);
HRESULT put_DefaultContainer(
  [in] BSTR bstrDefault
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a><span data-ttu-id="c8679-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c8679-116">Remarks</span></span>

<span data-ttu-id="c8679-117">Поставщики должны предоставлять это свойство для каждого пользователя.</span><span class="sxs-lookup"><span data-stu-id="c8679-117">Providers must supply this property on a per-user basis.</span></span> <span data-ttu-id="c8679-118">Контейнер по умолчанию задается сразу после вызова **иадснамеспацес::p UT \_ дефаултконтаинер**.</span><span class="sxs-lookup"><span data-stu-id="c8679-118">The default container is set immediately after the invocation of **IADsNamespaces::put\_DefaultContainer**.</span></span> <span data-ttu-id="c8679-119">Вызов метода [**iAds. сетинфо**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) не требуется.</span><span class="sxs-lookup"><span data-stu-id="c8679-119">Calling [**IADs.SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) is not required.</span></span> <span data-ttu-id="c8679-120">На самом деле объект, предоставляемый системой пространств имен, возвращает **E \_ нотимпл** для метода **iAds. сетинфо** , вызываемого для этого объекта.</span><span class="sxs-lookup"><span data-stu-id="c8679-120">In fact, the system-supplied namespaces object returns **E\_NOTIMPL** for the **IADs.SetInfo** method called on this object.</span></span> <span data-ttu-id="c8679-121">Если контейнер является объектом namespaces, операция перечисления всегда приводит к получению списка объектов пространства имен, относящихся к поставщику.</span><span class="sxs-lookup"><span data-stu-id="c8679-121">When a container is the namespaces object, an enumeration operation always results in a list of provider-specific namespace objects.</span></span> <span data-ttu-id="c8679-122">Если для получения объекта пространства имен используется [**иадсконтаинер. GetObject**](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject) , параметр *бстркласс* игнорируется.</span><span class="sxs-lookup"><span data-stu-id="c8679-122">When [**IADsContainer.GetObject**](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject) is used to obtain a namespace object, the *bstrClass* parameter is ignored.</span></span> <span data-ttu-id="c8679-123">Это связано с тем, что контейнер, то есть объект namespaces, содержит только один тип объекта, а именно, объекты пространства имен, относящиеся к поставщику.</span><span class="sxs-lookup"><span data-stu-id="c8679-123">This is because the container, that is, the namespaces object, contains only one type of object, namely, provider-specific namespace objects.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8679-124">Требования</span><span class="sxs-lookup"><span data-stu-id="c8679-124">Requirements</span></span>



| <span data-ttu-id="c8679-125">Требование</span><span class="sxs-lookup"><span data-stu-id="c8679-125">Requirement</span></span> | <span data-ttu-id="c8679-126">Значение</span><span class="sxs-lookup"><span data-stu-id="c8679-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c8679-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c8679-127">Minimum supported client</span></span><br/> | <span data-ttu-id="c8679-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c8679-128">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c8679-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c8679-129">Minimum supported server</span></span><br/> | <span data-ttu-id="c8679-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c8679-130">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c8679-131">Header</span><span class="sxs-lookup"><span data-stu-id="c8679-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="c8679-132"><dt>IAds. h</dt></span><span class="sxs-lookup"><span data-stu-id="c8679-132"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="c8679-133">DLL</span><span class="sxs-lookup"><span data-stu-id="c8679-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c8679-134"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c8679-134"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="c8679-135">IID</span><span class="sxs-lookup"><span data-stu-id="c8679-135">IID</span></span><br/>                      | <span data-ttu-id="c8679-136">IID \_ иадснамеспацес определен как 28B96BA0-B330-11CF-A9AD-00AA006BC149</span><span class="sxs-lookup"><span data-stu-id="c8679-136">IID\_IADsNamespaces is defined as 28B96BA0-B330-11CF-A9AD-00AA006BC149</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="c8679-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c8679-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8679-138">**Иадсконтаинер. GetObject**</span><span class="sxs-lookup"><span data-stu-id="c8679-138">**IADsContainer.GetObject**</span></span>](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject)
</dt> <dt>

[<span data-ttu-id="c8679-139">**иадснамеспацес**</span><span class="sxs-lookup"><span data-stu-id="c8679-139">**IADsNamespaces**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsnamespaces)
</dt> <dt>

[<span data-ttu-id="c8679-140">Методы свойств интерфейса</span><span class="sxs-lookup"><span data-stu-id="c8679-140">Interface Property Methods</span></span>](interface-property-methods.md)
</dt> </dl>

 

 





