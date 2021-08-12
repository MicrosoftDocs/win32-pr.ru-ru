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
ms.openlocfilehash: bce57021774b3abc2f69a1120862912452629c3e70d9c8fd0ebcc5d39ce5203d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118548591"
---
# <a name="comadmincatalogobject-class"></a>Класс Комадминкаталогобжект

Представляет элементы в коллекциях в каталоге COM+. Используйте его для извлечения и изменения свойств, предоставляемых элементом в коллекции.

## <a name="when-to-implement"></a>Когда следует реализовывать

Этот класс реализуется с помощью COM+.



| Требование | Значение |
|------------|------------------------------------------|
| Интерфейсы | [**икаталогобжект**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogobject) |



 

## <a name="when-to-use"></a>Назначение

Используйте объекты, созданные из класса **комадминкаталогобжект** , для изменения свойств элементов, содержащихся в коллекциях в каталоге COM+. Эти элементы соответствуют элементам, отображаемым в папках дерева консоли средства администрирования служб компонентов. Папки в средстве администрирования служб компонентов соответствуют коллекциям в каталоге, которые можно представить с помощью объектов, созданных из класса [**комадминкаталогколлектион**](comadmincatalogcollection.md) .

Не все коллекции и элементы, предоставляемые через [**комадминкаталогколлектион**](comadmincatalogcollection.md) и **комадминкаталогобжект** , доступны в средстве администрирования служб компонентов.

Сведения о конкретных коллекциях и их свойствах см. в разделе [com+ Administration Collections](com--administration-collections.md).

Общие сведения о программном администрировании COM+ см. в разделе [Автоматизация администрирования com+](automating-com--administration.md).

## <a name="remarks"></a>Remarks

Нельзя напрямую создать объект **комадминкаталогобжект** . Чтобы использовать методы этого объекта, необходимо создать объект [**комадминкаталог**](comadmincatalog.md) , получить ссылку на [**икомадминкаталог**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog), а затем использовать [**икомадминкаталог::-Collection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) для получения ссылки на интерфейс [**икаталогколлектион**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection) , представляющий коллекцию верхнего уровня, или использовать [**икаталогколлектион:: IsCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) для доступа к коллекциям, которые не являются верхним уровнем.

После создания ссылки на интерфейс [**икаталогколлектион**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection) интересующей коллекции вызовите [**икаталогколлектион::P опулате**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) , чтобы заполнить коллекцию всеми ее элементами. Выполните итерацию по каждому элементу в коллекции, вызвав [**икаталогколлектион:: Get \_ Item**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-get_item) , чтобы получить ссылку на каждый интерфейс [**икаталогобжект**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogobject) . Когда вы найдете интересующий элемент, вы можете изменить свойства элемента и выйти из итерации. При внесении любых изменений в элементы коллекции необходимо вызвать метод [**икаталогколлектион:: SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) , чтобы сохранить изменения в каталоге COM+.

Это показано в следующем примере, где "Топколлектион" необходимо заменить на имя одной из коллекций администрирования COM+ верхнего уровня. "ItemName" необходимо заменить на имя интересующего элемента. Значение PropertyName должно быть заменено именем свойства, которое вы изменяете в элементе. и Варневпроп должны быть заменены ВАРИАНТом, который содержит новое значение для свойства.


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



чтобы использовать этот класс из Visual Basic майкрософт, добавьте ссылку на библиотеку типов администрирования COM+. Объект Комадминкаталогколлектион можно создать, вызвав метод [**IsCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) для объекта [**комадминкаталог**](comadmincatalog.md) или [**комадминкаталогколлектион**](comadmincatalogcollection.md) .

Вызовите метод [**заполнения**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) объекта [**комадминкаталогколлектион**](comadmincatalogcollection.md) , чтобы заполнить коллекцию всеми ее элементами. Выполните итерацию по каждому элементу в коллекции. Когда вы найдете интересующий элемент, вы можете изменить свойства элемента и выйти из итерации. При внесении любых изменений в элементы коллекции необходимо вызвать метод [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) объекта **комадминкаталогколлектион** , чтобы сохранить изменения в каталоге COM+.

Это показано в следующем примере, где "Топколлектион" необходимо заменить на имя одной из коллекций администрирования COM+ верхнего уровня. "ItemName" необходимо заменить на имя интересующего элемента. Значение PropertyName должно быть заменено именем свойства, которое вы изменяете в элементе. и Невпропвалуе должны быть заменены новым значением свойства.


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



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                              |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                    |
| Заголовок<br/>                   | <dl> <dt>Комадмин. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Комадмин. idl</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**комадминкаталог**](comadmincatalog.md)
</dt> <dt>

[**комадминкаталогколлектион**](comadmincatalogcollection.md)
</dt> <dt>

[**икаталогобжект**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogobject)
</dt> </dl>

 

 




