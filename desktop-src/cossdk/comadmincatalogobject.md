---
description: Представляет элементы в коллекциях в каталоге COM+. Используйте его для извлечения и изменения свойств, предоставляемых элементом в коллекции.
ms.assetid: 1d7f248b-20ec-4b34-88ab-3c68bef72b5a
title: Класс Комадминкаталогобжект (Комадмин. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COMAdminCatalogObject
api_type:
- COM
api_location:
- ComAdmin.Idl
ms.openlocfilehash: 19fb873e29ad235b11dfe6e7a95b2ad47a8405b2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141463"
---
# <a name="comadmincatalogobject-class"></a><span data-ttu-id="87ac0-104">Класс Комадминкаталогобжект</span><span class="sxs-lookup"><span data-stu-id="87ac0-104">COMAdminCatalogObject class</span></span>

<span data-ttu-id="87ac0-105">Представляет элементы в коллекциях в каталоге COM+.</span><span class="sxs-lookup"><span data-stu-id="87ac0-105">Represents items in collections in the COM+ catalog.</span></span> <span data-ttu-id="87ac0-106">Используйте его для извлечения и изменения свойств, предоставляемых элементом в коллекции.</span><span class="sxs-lookup"><span data-stu-id="87ac0-106">Use it to retrieve and modify properties exposed by an item in a collection.</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="87ac0-107">Когда следует реализовывать</span><span class="sxs-lookup"><span data-stu-id="87ac0-107">When to implement</span></span>

<span data-ttu-id="87ac0-108">Этот класс реализуется с помощью COM+.</span><span class="sxs-lookup"><span data-stu-id="87ac0-108">This class is implemented by COM+.</span></span>



| <span data-ttu-id="87ac0-109">Требование</span><span class="sxs-lookup"><span data-stu-id="87ac0-109">Requirement</span></span> | <span data-ttu-id="87ac0-110">Значение</span><span class="sxs-lookup"><span data-stu-id="87ac0-110">Value</span></span> |
|------------|------------------------------------------|
| <span data-ttu-id="87ac0-111">Интерфейсы</span><span class="sxs-lookup"><span data-stu-id="87ac0-111">Interfaces</span></span> | [<span data-ttu-id="87ac0-112">**икаталогобжект**</span><span class="sxs-lookup"><span data-stu-id="87ac0-112">**ICatalogObject**</span></span>](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogobject) |



 

## <a name="when-to-use"></a><span data-ttu-id="87ac0-113">Назначение</span><span class="sxs-lookup"><span data-stu-id="87ac0-113">When to use</span></span>

<span data-ttu-id="87ac0-114">Используйте объекты, созданные из класса **комадминкаталогобжект** , для изменения свойств элементов, содержащихся в коллекциях в каталоге COM+.</span><span class="sxs-lookup"><span data-stu-id="87ac0-114">Use objects created from the **COMAdminCatalogObject** class to modify the properties of items contained in collections in the COM+ catalog.</span></span> <span data-ttu-id="87ac0-115">Эти элементы соответствуют элементам, отображаемым в папках дерева консоли средства администрирования служб компонентов.</span><span class="sxs-lookup"><span data-stu-id="87ac0-115">These items correspond to items shown inside folders in the console tree of the Component Services administration tool.</span></span> <span data-ttu-id="87ac0-116">Папки в средстве администрирования служб компонентов соответствуют коллекциям в каталоге, которые можно представить с помощью объектов, созданных из класса [**комадминкаталогколлектион**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="87ac0-116">Folders in the Component Services administration tool correspond to collections in the catalog, which you can represent by using objects created from the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) class.</span></span>

<span data-ttu-id="87ac0-117">Не все коллекции и элементы, предоставляемые через [**комадминкаталогколлектион**](comadmincatalogcollection.md) и **комадминкаталогобжект** , доступны в средстве администрирования служб компонентов.</span><span class="sxs-lookup"><span data-stu-id="87ac0-117">Not all of the collections and items exposed through [**COMAdminCatalogCollection**](comadmincatalogcollection.md) and **COMAdminCatalogObject** are available in the Component Services administration tool.</span></span>

<span data-ttu-id="87ac0-118">Сведения о конкретных коллекциях и их свойствах см. в разделе [com+ Administration Collections](com--administration-collections.md).</span><span class="sxs-lookup"><span data-stu-id="87ac0-118">For information regarding specific collections and their properties, see [COM+ Administration Collections](com--administration-collections.md).</span></span>

<span data-ttu-id="87ac0-119">Общие сведения о программном администрировании COM+ см. в разделе [Автоматизация администрирования com+](automating-com--administration.md).</span><span class="sxs-lookup"><span data-stu-id="87ac0-119">For an introduction to programmatic administration of COM+, see [Automating COM+ Administration](automating-com--administration.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="87ac0-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="87ac0-120">Remarks</span></span>

<span data-ttu-id="87ac0-121">Нельзя напрямую создать объект **комадминкаталогобжект** .</span><span class="sxs-lookup"><span data-stu-id="87ac0-121">You cannot directly create a **COMAdminCatalogObject** object.</span></span> <span data-ttu-id="87ac0-122">Чтобы использовать методы этого объекта, необходимо создать объект [**комадминкаталог**](comadmincatalog.md) , получить ссылку на [**икомадминкаталог**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog), а затем использовать [**икомадминкаталог::-Collection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) для получения ссылки на интерфейс [**икаталогколлектион**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection) , представляющий коллекцию верхнего уровня, или использовать [**икаталогколлектион:: IsCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) для доступа к коллекциям, которые не являются верхним уровнем.</span><span class="sxs-lookup"><span data-stu-id="87ac0-122">To use the methods this object, you must create a [**COMAdminCatalog**](comadmincatalog.md) object, obtain a reference to [**ICOMAdminCatalog**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog), and then use [**ICOMAdminCatalog::GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) to get a reference to an [**ICatalogCollection**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection) interface that represents a top-level collection or use [**ICatalogCollection::GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) to access collections that are not top-level.</span></span>

<span data-ttu-id="87ac0-123">После создания ссылки на интерфейс [**икаталогколлектион**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection) интересующей коллекции вызовите [**икаталогколлектион::P опулате**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) , чтобы заполнить коллекцию всеми ее элементами.</span><span class="sxs-lookup"><span data-stu-id="87ac0-123">After you have a reference to the [**ICatalogCollection**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection) interface of the collection in which you are interested, call [**ICatalogCollection::Populate**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) to populate the collection with all of its items.</span></span> <span data-ttu-id="87ac0-124">Выполните итерацию по каждому элементу в коллекции, вызвав [**икаталогколлектион:: Get \_ Item**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-get_item) , чтобы получить ссылку на каждый интерфейс [**икаталогобжект**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogobject) .</span><span class="sxs-lookup"><span data-stu-id="87ac0-124">Iterate through each of the items in the collection by calling [**ICatalogCollection::get\_Item**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-get_item) to get a reference to each [**ICatalogObject**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogobject) interface.</span></span> <span data-ttu-id="87ac0-125">Когда вы найдете интересующий элемент, вы можете изменить свойства элемента и выйти из итерации.</span><span class="sxs-lookup"><span data-stu-id="87ac0-125">When you find the item of interest, you can modify the item's properties and exit the iteration.</span></span> <span data-ttu-id="87ac0-126">При внесении любых изменений в элементы коллекции необходимо вызвать метод [**икаталогколлектион:: SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) , чтобы сохранить изменения в каталоге COM+.</span><span class="sxs-lookup"><span data-stu-id="87ac0-126">If you make any changes to any items in a collection, you must call [**ICatalogCollection::SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) to save the changes to the COM+ catalog.</span></span>

<span data-ttu-id="87ac0-127">Это показано в следующем примере, где "Топколлектион" необходимо заменить на имя одной из коллекций администрирования COM+ верхнего уровня. "ItemName" необходимо заменить на имя интересующего элемента. Значение PropertyName должно быть заменено именем свойства, которое вы изменяете в элементе. и Варневпроп должны быть заменены ВАРИАНТом, который содержит новое значение для свойства.</span><span class="sxs-lookup"><span data-stu-id="87ac0-127">This is shown in the following example, where "TopCollection" must be replaced by the name of one of the top-level COM+ administration collections; "ItemName" must be replaced by the name of the item that you are interested in; "PropertyName" must be replaced by the name of the property that you are modifying in the item; and varNewProp must be replaced by a VARIANT that contains the new value for the property.</span></span>


```C++
// Convert ItemName to a BSTR.
bstrItemName = SysAllocString(L"ItemName");
HRESULT hr = CoCreateInstance(CLSID_COMAdminCatalog, NULL, 
  CLSCTX_INPROC_SERVER, IID_IUnknown, (void**)&pUnknown);
if (FAILED(hr)) exit(0);  // Replace with specific error handling.
hr = pUnknown->QueryInterface(IID_ICOMAdminCatalog, 
  (void**)&pCatalog); 
if (FAILED(hr)) exit(0);  // Replace with specific error handling.
hr = pCatalog->GetCollection(L"TopCollection", 
  (IDispatch**)&pTopColl);
if (FAILED(hr)) exit(0);  // Replace with specific error handling.
// Populate the TopCollection collection.
hr = pTopColl->Populate();
if (FAILED(hr)) exit(0);  // Replace with specific error handling.
// Get the number of items in the collection.
hr = pTopColl->get_Count(&lCount);
if (FAILED(hr)) exit(0);  // Replace with specific error handling.
VARIANT varName;
VariantInit(&varName);
// Iterate through each item in the collection.
for (LONG lIdx = 0; lIdx < lCount; lIdx++) {
    hr = pTopColl->get_Item(lIdx, (IDispatch**)&pItem);
    if (FAILED(hr)) exit(0);  // Replace with specific error handling.
    hr = pItem->get_Name(&varName);
    if (FAILED(hr)) exit(0);  // Replace with specific error handling.
    // Compare the item name to bstrItemName.
    hr = VarBstrCmp(varName.bstrVal, bstrItemName, 1024L, NULL);
    if (FAILED(hr)) exit(0);  // Replace with specific error handling.
    if (VARCMP_EQ == hr) {  // The strings are equal.
        // Use the put_Value method to modify properties of the item.
        hr = pItem->put_Value(L"PropertyName", varNewProp);
        if (FAILED(hr)) exit(0);  // Replace with specific error handling.
        break;  // Exit the iteration.
    }
}
hr = pTopColl->SaveChanges(&lNum);
if (FAILED(hr)) exit(0);  // Replace with specific error handling.
SysFreeString(bstrItemName);


```



<span data-ttu-id="87ac0-128">Чтобы использовать этот класс из Visual Basic Майкрософт, добавьте ссылку на библиотеку типов администрирования COM+.</span><span class="sxs-lookup"><span data-stu-id="87ac0-128">To use this class from Microsoft Visual Basic, add a reference to the COM+ Admin Type Library.</span></span> <span data-ttu-id="87ac0-129">Объект Комадминкаталогколлектион можно создать, вызвав метод [**IsCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) для объекта [**комадминкаталог**](comadmincatalog.md) или [**комадминкаталогколлектион**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="87ac0-129">A COMAdminCatalogCollection object can be created by calling [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) on a [**COMAdminCatalog**](comadmincatalog.md) or [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

<span data-ttu-id="87ac0-130">Вызовите метод [**заполнения**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) объекта [**комадминкаталогколлектион**](comadmincatalogcollection.md) , чтобы заполнить коллекцию всеми ее элементами.</span><span class="sxs-lookup"><span data-stu-id="87ac0-130">Call the [**Populate**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) method of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object to populate the collection with all of its items.</span></span> <span data-ttu-id="87ac0-131">Выполните итерацию по каждому элементу в коллекции.</span><span class="sxs-lookup"><span data-stu-id="87ac0-131">Iterate through each of the items in the collection.</span></span> <span data-ttu-id="87ac0-132">Когда вы найдете интересующий элемент, вы можете изменить свойства элемента и выйти из итерации.</span><span class="sxs-lookup"><span data-stu-id="87ac0-132">When you find the item of interest, you can modify the item's properties and exit the iteration.</span></span> <span data-ttu-id="87ac0-133">При внесении любых изменений в элементы коллекции необходимо вызвать метод [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) объекта **комадминкаталогколлектион** , чтобы сохранить изменения в каталоге COM+.</span><span class="sxs-lookup"><span data-stu-id="87ac0-133">If you make any changes to any items in a collection, you must call the [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) method of the **COMAdminCatalogCollection** object to save the changes to the COM+ catalog.</span></span>

<span data-ttu-id="87ac0-134">Это показано в следующем примере, где "Топколлектион" необходимо заменить на имя одной из коллекций администрирования COM+ верхнего уровня. "ItemName" необходимо заменить на имя интересующего элемента. Значение PropertyName должно быть заменено именем свойства, которое вы изменяете в элементе. и Невпропвалуе должны быть заменены новым значением свойства.</span><span class="sxs-lookup"><span data-stu-id="87ac0-134">This is shown in the following example, where "TopCollection" must be replaced by the name of one of the top-level COM+ administration collections; "ItemName" must be replaced by the name of the item that you are interested in; "PropertyName" must be replaced by the name of the property that you are modifying in the item; and NewPropValue must be replaced by the new value for the property.</span></span>


```VB
Dim objCatalog As COMAdmin.COMAdminCatalog
Set objCatalog = CreateObject("COMAdmin.COMAdminCatalog")
Dim objTopCollection As COMAdmin.COMAdminCatalogCollection
Set objTopCollection = objCatalog.GetCollection("TopCollection")
objTopCollection.Populate
Dim objItem As COMAdmin.COMAdminCatalogObject
For Each objItem in objTopCollection
    If objItem.Name = "ItemName" Then
        objItem.Value("PropertyName") = NewPropValue
        Exit For
    End If
Next
objAppCollection.SaveChanges

```



## <a name="requirements"></a><span data-ttu-id="87ac0-135">Требования</span><span class="sxs-lookup"><span data-stu-id="87ac0-135">Requirements</span></span>



| <span data-ttu-id="87ac0-136">Требование</span><span class="sxs-lookup"><span data-stu-id="87ac0-136">Requirement</span></span> | <span data-ttu-id="87ac0-137">Значение</span><span class="sxs-lookup"><span data-stu-id="87ac0-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="87ac0-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="87ac0-138">Minimum supported client</span></span><br/> | <span data-ttu-id="87ac0-139">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="87ac0-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="87ac0-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="87ac0-140">Minimum supported server</span></span><br/> | <span data-ttu-id="87ac0-141">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="87ac0-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="87ac0-142">Заголовок</span><span class="sxs-lookup"><span data-stu-id="87ac0-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="87ac0-143"><dt>Комадмин. h</dt></span><span class="sxs-lookup"><span data-stu-id="87ac0-143"><dt>ComAdmin.h</dt></span></span> </dl>   |
| <span data-ttu-id="87ac0-144">IDL</span><span class="sxs-lookup"><span data-stu-id="87ac0-144">IDL</span></span><br/>                      | <dl> <span data-ttu-id="87ac0-145"><dt>Комадмин. idl</dt></span><span class="sxs-lookup"><span data-stu-id="87ac0-145"><dt>ComAdmin.Idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87ac0-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="87ac0-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87ac0-147">**комадминкаталог**</span><span class="sxs-lookup"><span data-stu-id="87ac0-147">**COMAdminCatalog**</span></span>](comadmincatalog.md)
</dt> <dt>

[<span data-ttu-id="87ac0-148">**комадминкаталогколлектион**</span><span class="sxs-lookup"><span data-stu-id="87ac0-148">**COMAdminCatalogCollection**</span></span>](comadmincatalogcollection.md)
</dt> <dt>

[<span data-ttu-id="87ac0-149">**икаталогобжект**</span><span class="sxs-lookup"><span data-stu-id="87ac0-149">**ICatalogObject**</span></span>](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogobject)
</dt> </dl>

 

 




