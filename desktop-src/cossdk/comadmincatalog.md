---
description: Обращается к данным, хранящимся в каталоге COM+.
ms.assetid: d77123f6-9821-4c80-860c-5f1feaca7987
title: Класс Комадминкаталог (Комадмин. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COMAdminCatalog
api_type:
- COM
api_location:
- ComAdmin.Idl
ms.openlocfilehash: 8be3f0f3f9aa59c2199c50b73b8a4d4488b0c9a65d3e0679b65350d6b8b07fd3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119128996"
---
# <a name="comadmincatalog-class"></a>Класс Комадминкаталог

Обращается к данным, хранящимся в каталоге COM+.

## <a name="when-to-implement"></a>Когда следует реализовывать

Этот класс реализуется с помощью COM+.



| Требование | Значение |
|------------|-------------------------------------------------------------------------------------------------------------------|
| CLSID      | \_КОМАДМИНКАТАЛОГ CLSID                                                                                            |
| ProgID:     | L "Комадмин. Комадминкаталог"                                                                                       |
| Интерфейсы | [**икомадминкаталог**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog)<br/> [**ICOMAdminCatalog2**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2)<br/> |



 

## <a name="when-to-use"></a>Назначение

Объекты, созданные из класса **комадминкаталог** , используются для запуска программного доступа к данным конфигурации com+, хранящимся в каталоге COM+. Эти сведения полагаются на папки и элементы в дереве консоли средства администрирования служб компонентов. Класс **комадминкаталог** позволяет получать доступ к коллекциям в каталоге, устанавливать приложения и компоненты COM+, запускать и прекращать работу служб, а также подключаться к удаленным серверам и администрировать их.

Папки в средстве администрирования служб компонентов соответствуют коллекциям в каталоге, которые можно представить с помощью объектов, созданных из класса [**комадминкаталогколлектион**](comadmincatalogcollection.md) . Элементы в папках соответствуют элементам в коллекциях, которые можно представить с помощью объектов, созданных из класса [**комадминкаталогобжект**](comadmincatalogobject.md) .

Не все коллекции и элементы, предоставляемые через [**комадминкаталогколлектион**](comadmincatalogcollection.md) и [**комадминкаталогобжект**](comadmincatalogobject.md) , доступны в средстве администрирования служб компонентов.

Сведения о конкретных коллекциях и их свойствах см. в разделе [com+ Administration Collections](com--administration-collections.md).

Общие сведения о программном администрировании COM+ см. в разделе [Автоматизация администрирования com+](automating-com--administration.md).

## <a name="remarks"></a>Remarks

Чтобы создать этот объект, вызовите [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).

чтобы использовать этот класс из Visual Basic майкрософт, добавьте ссылку на библиотеку типов администрирования COM+. Объект Комадминкаталог можно объявить с помощью "Комадмин. Комадминкаталог" в качестве имени класса.

в COM+ 1,5, выпущенном с Windows XP, класс **комадминкаталог** реализует интерфейс [**ICOMAdminCatalog2**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2) . однако в COM+ 1,0, выпущенном с Windows 2000, класс **комадминкаталог** реализует только интерфейс [**икомадминкаталог**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                              |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                    |
| Заголовок<br/>                   | <dl> <dt>Комадмин. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Комадмин. idl</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**комадминкаталогколлектион**](comadmincatalogcollection.md)
</dt> <dt>

[**комадминкаталогобжект**](comadmincatalogobject.md)
</dt> <dt>

[**икомадминкаталог**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog)
</dt> <dt>

[**ICOMAdminCatalog2**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2)
</dt> </dl>

 

