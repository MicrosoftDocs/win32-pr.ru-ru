---
description: Интерфейс Исканпрофиле представляет один профиль сканирования и позволяет приложениям устанавливать и получать свойства профиля.
ms.assetid: 5cd76256-d64e-4934-8cc2-0a467c7e34a9
title: Интерфейс Исканпрофиле
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile
api_type:
- COM
api_location:
- Scanprofiles.idl
ms.openlocfilehash: 1de80ac23ffa3e2687e2e6d0449f7a273067d5899204c479f9b62e8571190d61
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119450834"
---
# <a name="iscanprofile-interface"></a>Интерфейс Исканпрофиле

Интерфейс **исканпрофиле** представляет один профиль сканирования и позволяет приложениям устанавливать и получать свойства профиля.

## <a name="members"></a>Элементы

Интерфейс **исканпрофиле** наследует от интерфейса [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **Исканпрофиле** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **исканпрофиле** содержит следующие методы.



| Метод                                                     | Описание                                                                                                                                         |
|:-----------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**жеталлпропидс**](-wia-iscanprofile-getallpropids.md)   | Возвращает все доступные идентификаторы свойств в профиле.<br/>                                                                                            |
| [**GetDeviceID**](-wia-iscanprofile-getdeviceid.md)       | Возвращает идентификатор устройства.<br/>                                                                                                            |
| [**GetGUID**](-wia-iscanprofile-getguid.md)               | Возвращает идентификатор GUID профиля.<br/>                                                                                                         |
| [**GetItem**](-wia-iscanprofile-getitem.md)               | Возвращает идентификатор GUID категории элемента WIA 2,0, с которым связан профиль.<br/>                                                   |
| [**GetName**](-wia-iscanprofile-getname.md)               | Возвращает понятное имя профиля.<br/>                                                                                                   |
| [**жетнумпропидс**](-wia-iscanprofile-getnumpropids.md)   | Возвращает число идентификаторов свойств в профиле.<br/>                                                                                            |
| [**GetProperty**](-wia-iscanprofile-getproperty.md)       | Возвращает значение указанных дочерних свойств в `<Properties>` элементе профиля сканирования.<br/>                                            |
| [**IsDefault**](-wia-iscanprofile-isdefault.md)           | Возвращает значение, указывающее, является ли профиль профилем сканирования по умолчанию для связанного устройства [**IWiaItem2**](-wia-iwiaitem2.md) .<br/> |
| [**RemoveProperty**](-wia-iscanprofile-removeproperty.md) | Удаляет указанный список дочерних свойств `<Properties>` элемента профиля сканирования.<br/>                                            |
| [**Сохранить**](-wia-iscanprofile-save.md)                     | Сохраняет изменения профиля на диск.<br/>                                                                                                      |
| [**сетитем**](-wia-iscanprofile-setitem.md)               | Задает идентификатор GUID категории элемента WIA 2,0, с которым связан профиль.<br/>                                                       |
| [**SetName**](-wia-iscanprofile-setname.md)               | Задает понятное имя профиля.<br/>                                                                                                   |
| [**SetProperty**](-wia-iscanprofile-setproperty.md)       | Задает значение указанных дочерних свойств в `<Properties>` элементе профиля сканирования.<br/>                                            |



 

## <a name="remarks"></a>Remarks

У любого устройства [**IWiaItem2**](-wia-iwiaitem2.md) может быть профиль сканирования. Однако **IWiaItem2** элементы типов \_ Категория WIA \_ Finished \_ File и WIA \_ Category \_ не могут иметь профили.

Если профиль сканирования сохранен с помощью метода [**исканпрофиле:: Save**](-wia-iscanprofile-save.md) , он сохраняется как XML-файл в% UserProfile% \\ Application Data \\ \\ Center \\ усерсканпрофилес.

Чтобы создать экземпляр объекта **исканпрофиле** , используйте метод [**Исканпрофилемгр:: креатепрофиле**](-wia-iscanprofilemgr-createprofile.md) . Чтобы получить ссылку на профиль сканирования, который уже был сохранен на диске, используйте метод [**исканпрофилемгр:: опенпрофиле**](-wia-iscanprofilemgr-openprofile.md) .

Все профили сканирования имеют следующие элементы: `<ProfileGUID>, <DeviceID>, <ProfileName>, <WiaItem>` , и `<Properties>` . Профиль по умолчанию для устройства также имеет `<Default>` элемент.

`<ProfileGUID>`Элементы и `<DeviceID>` не могут быть изменены после создания профиля. Значения `<ProfileName>` элемента и `<WiaItem>` элемента можно изменить после создания профиля. `<Default>`Элемент можно добавить или удалить. Это можно сделать программно с помощью методов [**исканпрофиле:: SetName**](-wia-iscanprofile-setname.md), [**Исканпрофиле:: сетитем**](-wia-iscanprofile-setitem.md)и [**исканпрофилемгр:: сетдефаулт**](-wia-iscanprofilemgr-setdefault.md) . Эти свойства также могут быть изменены пользователями с помощью метода [**исканпрофилеуи:: сканпрофиледиалог**](-wia-iscanprofileui-scanprofiledialog.md) .

`<Properties>`Элемент содержит `<Property>` дочерние элементы. Используйте их, чтобы добавить в профиль любое свойство элемента WIA 2,0 или устройства. Вы также можете разработать собственные `<Property>` дочерние элементы приобретения Image. Это делает схему профиля сканирования расширяемой. (Дополнительные сведения о расширении схемы см. в разделе [Определение пользовательских свойств](-wia-defining-custom-properties.md), [**исканпрофиле::-Property**](-wia-iscanprofile-getproperty.md)и [**исканпрофиле:: SetProperty**](-wia-iscanprofile-setproperty.md).)

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                              |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                        |
| IDL<br/>                      | <dl> <dt>Сканпрофилес. idl</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[Схема профиля сканирования](-wia-scan-profile-schema.md)
</dt> </dl>

 

 
