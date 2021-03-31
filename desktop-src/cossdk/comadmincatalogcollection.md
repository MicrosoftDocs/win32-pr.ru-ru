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
# <a name="comadmincatalogcollection-class"></a>Класс Комадминкаталогколлектион

Представляет любую коллекцию в каталоге COM+. Используйте его для перечисления, добавления, удаления и извлечения элементов в коллекции, а также для доступа к связанным коллекциям.

## <a name="when-to-implement"></a>Когда следует реализовывать

Этот класс реализуется с помощью COM+.



| Требование | Значение |
|------------|--------------------------------------------------|
| Интерфейсы | [**икаталогколлектион**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection) |



 

## <a name="when-to-use"></a>Назначение

Используйте объекты, созданные из класса **комадминкаталогколлектион** , если требуется программно управлять коллекцией в каталоге COM+. Эти коллекции соответствуют папкам в средстве администрирования служб компонентов. Элементы внутри папок соответствуют элементам в коллекциях, которые можно представить с помощью объектов, созданных из класса [**комадминкаталогобжект**](comadmincatalogobject.md) .

Сведения о коллекциях в каталоге и их свойствах см. в разделе [com+ Administration Collections](com--administration-collections.md).

Общие сведения о программном администрировании COM+ см. в разделе [Автоматизация администрирования com+](automating-com--administration.md).

## <a name="remarks"></a>Комментарии

Нельзя напрямую создать объект **комадминкаталогколлектион** . Чтобы использовать методы этого объекта, необходимо создать объект [**комадминкаталог**](comadmincatalog.md) , получить ссылку на [**икомадминкаталог**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog), а затем использовать [**икомадминкаталог::-Collection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) , чтобы получить ссылку на интерфейс [**икаталогколлектион**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection) , представляющий коллекцию верхнего уровня. Это показано в следующем примере, где "Топколлектион" необходимо заменить на имя одной из коллекций администрирования COM+ верхнего уровня.


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



Чтобы использовать этот класс из Visual Basic Майкрософт, добавьте ссылку на библиотеку типов администрирования COM+. Объект Комадминкаталогколлектион можно создать, вызвав метод [**IsCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) для объекта [**комадминкаталог**](comadmincatalog.md) . Это показано в следующем примере, где "Топколлектион" необходимо заменить на имя одной из коллекций администрирования COM+ верхнего уровня.


```VB
Dim objCatalog As COMAdmin.COMAdminCatalog
Set objCatalog = CreateObject("COMAdmin.COMAdminCatalog")
Dim objTopCollection As COMAdmin.COMAdminCatalogCollection
Set objTopCollection = objCatalog.GetCollection("TopCollection")

```



## <a name="requirements"></a>Требования



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

[**комадминкаталогобжект**](comadmincatalogobject.md)
</dt> <dt>

[**икаталогколлектион**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection)
</dt> </dl>

 

 




