---
title: Интерфейс Имсрдпклиенттранспортсеттингс
description: Управляет параметрами транспорта клиента для сервера шлюза удаленный рабочий стол (шлюза удаленных рабочих столов). | Интерфейс Имсрдпклиенттранспортсеттингс
ms.assetid: d2573727-1dcc-4d4d-af5c-038e9467ba84
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов интерфейса Имсрдпклиенттранспортсеттингс
- Службы удаленных рабочих столов интерфейса Имсрдпклиенттранспортсеттингс, описание
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec240d008ef2f9469fb67f4041cfb33c08383079
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105684841"
---
# <a name="imsrdpclienttransportsettings-interface"></a>Интерфейс Имсрдпклиенттранспортсеттингс

Управляет параметрами транспорта клиента для сервера шлюза удаленный рабочий стол (шлюза удаленных рабочих столов).

## <a name="members"></a>Элементы

Интерфейс **имсрдпклиенттранспортсеттингс** наследует от интерфейса [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **Имсрдпклиенттранспортсеттингс** также имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Интерфейс **имсрдпклиенттранспортсеттингс** имеет следующие свойства.



| Свойство                                                                                                          | Тип доступа           | Описание                                                 |
|:------------------------------------------------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------|
| [**гатевайкредссаурце**](imsrdpclienttransportsettings-gatewaycredssource.md)<br/>                         | Чтение/запись<br/> | Метод проверки подлинности сервера шлюза удаленных рабочих столов.<br/>     |
| [**гатевайдефаултусажемесод**](imsrdpclienttransportsettings-gatewaydefaultusagemethod.md)<br/>           | Только для чтения<br/>  | Метод использования шлюза удаленных рабочих столов по умолчанию.<br/>             |
| [**гатевайхостнаме**](imsrdpclienttransportsettings-gatewayhostname.md)<br/>                               | Чтение/запись<br/> | Имя узла сервера шлюза удаленных рабочих столов.<br/>              |
| [**гатевайиссуппортед**](imsrdpclienttransportsettings-gatewayissupported.md)<br/>                         | Только для чтения<br/>  | Указывает, поддерживается ли шлюз удаленных рабочих столов.<br/>       |
| [**гатевайпрофилеусажемесод**](imsrdpclienttransportsettings-gatewayprofileusagemethod.md)<br/>           | Чтение/запись<br/> | Метод использования профиля шлюза удаленных рабочих столов.<br/>             |
| [**гатевайусажемесод**](imsrdpclienttransportsettings-gatewayusagemethod.md)<br/>                         | Чтение/запись<br/> | Метод использования сервера шлюза удаленных рабочих столов.<br/>              |
| [**гатевайусерселектедкредссаурце**](imsrdpclienttransportsettings-gatewayuserselectedcredssource.md)<br/> | Чтение/запись<br/> | Указанный пользователем источник учетных данных шлюза удаленных рабочих столов.<br/> |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                         |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                                   |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ имсрдпклиенттранспортсеттингс определен как 720298C0-A099-46f5-9F82-96921BAE4701<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[Справочник по веб-подключение к удаленному рабочему столу](remote-desktop-web-connection-reference.md)
</dt> <dt>

[**IMsRdpClientTransportSettings2**](imsrdpclienttransportsettings2.md)
</dt> </dl>

 

