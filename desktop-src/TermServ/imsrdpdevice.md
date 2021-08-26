---
title: Интерфейс Имсрдпдевице
description: Содержит сведения об объекте устройства.
ms.assetid: b486a591-870b-446c-8028-9e4406cdf0ce
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов интерфейса Имсрдпдевице
- Службы удаленных рабочих столов интерфейса Имсрдпдевице, описание
topic_type:
- apiref
api_name:
- IMsRdpDevice
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d545bebde1ed2df8a4c67cdf8d32d0a91499ed42076b2c1b31539d96069d3688
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120033094"
---
# <a name="imsrdpdevice-interface"></a>Интерфейс Имсрдпдевице

Содержит сведения об объекте устройства.

## <a name="members"></a>Элементы

Интерфейс **имсрдпдевице** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **Имсрдпдевице** также имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Интерфейс **имсрдпдевице** имеет следующие свойства.



| Свойство                                                               | Тип доступа           | Описание                                                                                                   |
|:-----------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------|
| [**DeviceDescription**](imsrdpdevice-devicedescription.md)<br/> | Только для чтения<br/>  | Возвращает описание устройства, отображаемое пользователю, если отображаемое имя недоступно.<br/> |
| [**девицеинстанцеид**](imsrdpdevice-deviceinstanceid.md)<br/>   | Только для чтения<br/>  | Возвращает идентификатор экземпляра устройства.<br/>                                            |
| [**FriendlyName**](imsrdpdevice-friendlyname.md)<br/>           | Только для чтения<br/>  | Извлекает отображаемое имя для устройства.<br/>                                                         |
| [**редиректионстате**](imsrdpdevice-redirectionstate.md)<br/>   | Чтение/запись<br/> | Указывает состояние перенаправления устройства.<br/>                                                     |



 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                               |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                         |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ имсрдпдевице определен как 60c3b9c8-9e92-4f5e-a3e7-604a912093ea<br/>        |



## <a name="see-also"></a>См. также

<dl> <dt>

[Справочник по веб-подключение к удаленному рабочему столу](remote-desktop-web-connection-reference.md)
</dt> <dt>

[**имсрдпдевицеколлектион**](imsrdpdevicecollection.md)
</dt> </dl>

 

