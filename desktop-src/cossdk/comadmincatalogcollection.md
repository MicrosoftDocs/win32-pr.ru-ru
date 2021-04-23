---
description: Представляет любую коллекцию в каталоге COM+. Используйте его для перечисления, добавления, удаления и извлечения элементов в коллекции, а также для доступа к связанным коллекциям.
ms.assetid: 2530e44f-c428-4baa-88e1-8d01eaf234cc
title: Класс Комадминкаталогколлектион (Комадмин. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COMAdminCatalogCollection
api_type:
- COM
api_location:
- ComAdmin.Idl
ms.openlocfilehash: 985a6b947708542ec3ce1dc6ecc835c94259b315
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807648"
---
# <a name="comadmincatalogcollection-class"></a><span data-ttu-id="4d992-104">Класс Комадминкаталогколлектион</span><span class="sxs-lookup"><span data-stu-id="4d992-104">COMAdminCatalogCollection class</span></span>

<span data-ttu-id="4d992-105">Представляет любую коллекцию в каталоге COM+.</span><span class="sxs-lookup"><span data-stu-id="4d992-105">Represents any collection in the COM+ catalog.</span></span> <span data-ttu-id="4d992-106">Используйте его для перечисления, добавления, удаления и извлечения элементов в коллекции, а также для доступа к связанным коллекциям.</span><span class="sxs-lookup"><span data-stu-id="4d992-106">Use it to enumerate, add, remove, and retrieve items in a collection and to access related collections.</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="4d992-107">Когда следует реализовывать</span><span class="sxs-lookup"><span data-stu-id="4d992-107">When to implement</span></span>

<span data-ttu-id="4d992-108">Этот класс реализуется с помощью COM+.</span><span class="sxs-lookup"><span data-stu-id="4d992-108">This class is implemented by COM+.</span></span>



| <span data-ttu-id="4d992-109">Требование</span><span class="sxs-lookup"><span data-stu-id="4d992-109">Requirement</span></span> | <span data-ttu-id="4d992-110">Значение</span><span class="sxs-lookup"><span data-stu-id="4d992-110">Value</span></span> |
|------------|--------------------------------------------------|
| <span data-ttu-id="4d992-111">Интерфейсы</span><span class="sxs-lookup"><span data-stu-id="4d992-111">Interfaces</span></span> | [<span data-ttu-id="4d992-112">**икаталогколлектион**</span><span class="sxs-lookup"><span data-stu-id="4d992-112">**ICatalogCollection**</span></span>](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection) |



 

## <a name="when-to-use"></a><span data-ttu-id="4d992-113">Назначение</span><span class="sxs-lookup"><span data-stu-id="4d992-113">When to use</span></span>

<span data-ttu-id="4d992-114">Используйте объекты, созданные из класса **комадминкаталогколлектион** , если требуется программно управлять коллекцией в каталоге COM+.</span><span class="sxs-lookup"><span data-stu-id="4d992-114">Use objects created from the **COMAdminCatalogCollection** class when you want to programmatically manipulate a collection in the COM+ catalog.</span></span> <span data-ttu-id="4d992-115">Эти коллекции соответствуют папкам в средстве администрирования служб компонентов.</span><span class="sxs-lookup"><span data-stu-id="4d992-115">These collections correspond to folders in the Component Services administration tool.</span></span> <span data-ttu-id="4d992-116">Элементы внутри папок соответствуют элементам в коллекциях, которые можно представить с помощью объектов, созданных из класса [**комадминкаталогобжект**](comadmincatalogobject.md) .</span><span class="sxs-lookup"><span data-stu-id="4d992-116">Items inside the folders correspond to items in collections, which you can represent by using objects created from the [**COMAdminCatalogObject**](comadmincatalogobject.md) class.</span></span>

<span data-ttu-id="4d992-117">Сведения о коллекциях в каталоге и их свойствах см. в разделе [com+ Administration Collections](com--administration-collections.md).</span><span class="sxs-lookup"><span data-stu-id="4d992-117">For information regarding the collections on the catalog and their properties, see [COM+ Administration Collections](com--administration-collections.md).</span></span>

<span data-ttu-id="4d992-118">Общие сведения о программном администрировании COM+ см. в разделе [Автоматизация администрирования com+](automating-com--administration.md).</span><span class="sxs-lookup"><span data-stu-id="4d992-118">For an introduction to programmatic administration of COM+, see [Automating COM+ Administration](automating-com--administration.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="4d992-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4d992-119">Remarks</span></span>

<span data-ttu-id="4d992-120">Нельзя напрямую создать объект **комадминкаталогколлектион** .</span><span class="sxs-lookup"><span data-stu-id="4d992-120">You cannot directly create a **COMAdminCatalogCollection** object.</span></span> <span data-ttu-id="4d992-121">Чтобы использовать методы этого объекта, необходимо создать объект [**комадминкаталог**](comadmincatalog.md) , получить ссылку на [**икомадминкаталог**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog), а затем использовать [**икомадминкаталог::-Collection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) , чтобы получить ссылку на интерфейс [**икаталогколлектион**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection) , представляющий коллекцию верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="4d992-121">To use the methods this object, you must create a [**COMAdminCatalog**](comadmincatalog.md) object, obtain a reference to [**ICOMAdminCatalog**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog), and then use [**ICOMAdminCatalog::GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) to get a reference to an [**ICatalogCollection**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection) interface that represents a top-level collection.</span></span> <span data-ttu-id="4d992-122">Это показано в следующем примере, где "Топколлектион" необходимо заменить на имя одной из коллекций администрирования COM+ верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="4d992-122">This is shown in the following example, where "TopCollection" must be replaced by the name of one of the top-level COM+ administration collections.</span></span>


```C++
    HRESULT hr = CoCreateInstance(CLSID_COMAdminCatalog, NULL, 
      CLSCTX_INPROC_SERVER, IID_IUnknown, (void**)&pUnknown);
    if (FAILED (hr)) exit(0);  // Replace with specific error handling.
    hr = pUnknown->QueryInterface(IID_ICOMAdminCatalog, 
      (void**)&pCatalog); 
    if (FAILED (hr)) exit(0);  // Replace with specific error handling.
    hr = pCatalog->GetCollection(L"TopCollection", 
      (IDispatch**)&pTopColl);
    if (FAILED (hr)) exit(0);  // Replace with specific error handling.
```



<span data-ttu-id="4d992-123">Чтобы использовать этот класс из Visual Basic Майкрософт, добавьте ссылку на библиотеку типов администрирования COM+.</span><span class="sxs-lookup"><span data-stu-id="4d992-123">To use this class from Microsoft Visual Basic, add a reference to the COM+ Admin Type Library.</span></span> <span data-ttu-id="4d992-124">Объект Комадминкаталогколлектион можно создать, вызвав метод [**IsCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) для объекта [**комадминкаталог**](comadmincatalog.md) .</span><span class="sxs-lookup"><span data-stu-id="4d992-124">A COMAdminCatalogCollection object can be created by calling [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) on a [**COMAdminCatalog**](comadmincatalog.md) object.</span></span> <span data-ttu-id="4d992-125">Это показано в следующем примере, где "Топколлектион" необходимо заменить на имя одной из коллекций администрирования COM+ верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="4d992-125">This is shown in the following example, where "TopCollection" must be replaced by the name of one of the top-level COM+ administration collections.</span></span>


```VB
Dim objCatalog As COMAdmin.COMAdminCatalog
Set objCatalog = CreateObject("COMAdmin.COMAdminCatalog")
Dim objTopCollection As COMAdmin.COMAdminCatalogCollection
Set objTopCollection = objCatalog.GetCollection("TopCollection")

```



## <a name="requirements"></a><span data-ttu-id="4d992-126">Требования</span><span class="sxs-lookup"><span data-stu-id="4d992-126">Requirements</span></span>



| <span data-ttu-id="4d992-127">Требование</span><span class="sxs-lookup"><span data-stu-id="4d992-127">Requirement</span></span> | <span data-ttu-id="4d992-128">Значение</span><span class="sxs-lookup"><span data-stu-id="4d992-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4d992-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4d992-129">Minimum supported client</span></span><br/> | <span data-ttu-id="4d992-130">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="4d992-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="4d992-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4d992-131">Minimum supported server</span></span><br/> | <span data-ttu-id="4d992-132">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="4d992-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4d992-133">Заголовок</span><span class="sxs-lookup"><span data-stu-id="4d992-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="4d992-134"><dt>Комадмин. h</dt></span><span class="sxs-lookup"><span data-stu-id="4d992-134"><dt>ComAdmin.h</dt></span></span> </dl>   |
| <span data-ttu-id="4d992-135">IDL</span><span class="sxs-lookup"><span data-stu-id="4d992-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4d992-136"><dt>Комадмин. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4d992-136"><dt>ComAdmin.Idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4d992-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4d992-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d992-138">**комадминкаталог**</span><span class="sxs-lookup"><span data-stu-id="4d992-138">**COMAdminCatalog**</span></span>](comadmincatalog.md)
</dt> <dt>

[<span data-ttu-id="4d992-139">**комадминкаталогобжект**</span><span class="sxs-lookup"><span data-stu-id="4d992-139">**COMAdminCatalogObject**</span></span>](comadmincatalogobject.md)
</dt> <dt>

[<span data-ttu-id="4d992-140">**икаталогколлектион**</span><span class="sxs-lookup"><span data-stu-id="4d992-140">**ICatalogCollection**</span></span>](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection)
</dt> </dl>

 

 




