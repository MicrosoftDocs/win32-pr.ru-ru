---
title: Интерфейс Имсрдпдевицеколлектион
description: Представляет коллекцию объектов Device.
ms.assetid: 9731b16b-12e0-457e-a4e5-a55d8a6db582
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов интерфейса Имсрдпдевицеколлектион
- Службы удаленных рабочих столов интерфейса Имсрдпдевицеколлектион, описание
topic_type:
- apiref
api_name:
- IMsRdpDeviceCollection
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5f7008b0b524150cd106b9bbe97d21a8de890773d8b0b461a6ae3045e847a79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000744"
---
# <a name="imsrdpdevicecollection-interface"></a>Интерфейс Имсрдпдевицеколлектион

Представляет коллекцию объектов Device.

## <a name="members"></a>Элементы

Интерфейс **имсрдпдевицеколлектион** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **Имсрдпдевицеколлектион** также имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="methods"></a>Методы

Интерфейс **имсрдпдевицеколлектион** содержит следующие методы.



| Метод                                                        | Описание                                                 |
|:--------------------------------------------------------------|:------------------------------------------------------------|
| [**рескандевицес**](imsrdpdevicecollection-rescandevices.md) | Обновляет список объектов в коллекции.<br/> |



 

### <a name="properties"></a>Свойства

Интерфейс **имсрдпдевицеколлектион** имеет следующие свойства.



| Свойство                                                                 | Тип доступа          | Описание                                                    |
|:-------------------------------------------------------------------------|:---------------------|:---------------------------------------------------------------|
| [**девицебид**](imsrdpdevicecollection-devicebyid.md)<br/>       | Только для чтения<br/> | Извлекает устройство с указанным идентификатором.<br/> |
| [**девицебиндекс**](imsrdpdevicecollection-devicebyindex.md)<br/> | Только для чтения<br/> | Извлекает устройство по указанному индексу.<br/>        |
| [**DeviceCount**](imsrdpdevicecollection-devicecount.md)<br/>     | Только для чтения<br/> | Возвращает число объектов в коллекции.<br/>   |



 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                  |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                            |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>    |
| IID<br/>                      | IID \_ имсрдпдевицеколлектион определен как 56540617-d281-488c-8738-6a8fdf64a118<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Справочник по веб-подключение к удаленному рабочему столу](remote-desktop-web-connection-reference.md)
</dt> <dt>

[**имсрдпдевице**](imsrdpdevice.md)
</dt> </dl>

 

