---
title: Интерфейс IMsRdpClientTransportSettings3
description: Определяет дополнительные свойства для сервера шлюза удаленный рабочий стол (шлюза удаленных рабочих столов). | Интерфейс IMsRdpClientTransportSettings3
ms.assetid: c0bdfe23-9a26-4feb-b9b7-e52f04f23aa1
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов интерфейса IMsRdpClientTransportSettings3
- Службы удаленных рабочих столов интерфейса IMsRdpClientTransportSettings3, описание
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings3
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7498db4b39a4ad0e89761cbec439895e4e9a152
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "103914372"
---
# <a name="imsrdpclienttransportsettings3-interface"></a>Интерфейс IMsRdpClientTransportSettings3

Определяет дополнительные свойства для сервера шлюза удаленный рабочий стол (шлюза удаленных рабочих столов).

## <a name="members"></a>Элементы

Интерфейс **IMsRdpClientTransportSettings3** наследует от [**IMsRdpClientTransportSettings2**](imsrdpclienttransportsettings2.md). **IMsRdpClientTransportSettings3** также имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Интерфейс **IMsRdpClientTransportSettings3** имеет следующие свойства.



| Свойство                                                                                                           | Тип доступа           | Описание                                                                                                                                          |
|:-------------------------------------------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**гатевайаускукиесервераддр**](imsrdpclienttransportsettings3-gatewayauthcookieserveraddr.md)<br/>       | Чтение/запись<br/> | Адрес сервера для проверки подлинности на основе файлов cookie.<br/>                                                                                       |
| [**гатевайауслогинпаже**](imsrdpclienttransportsettings3-gatewayauthloginpage.md)<br/>                     | Чтение/запись<br/> | Адрес веб-страницы входа, используемой для проверки подлинности пользователя.<br/>                                                                           |
| [**гатевайкредсаурцекукие**](imsrdpclienttransportsettings3-gatewaycredsourcecookie.md)<br/>               | Чтение/запись<br/> | Указывает, является ли источник учетных данных основанным на файлах cookie.<br/>                                                                                       |
| [**гатевайенкриптедаускукие**](imsrdpclienttransportsettings3-gatewayencryptedauthcookie.md)<br/>         | Чтение/запись<br/> | Зашифрованный файл cookie проверки подлинности.<br/>                                                                                                      |
| [**гатевайенкриптедаускукиесизе**](imsrdpclienttransportsettings3-gatewayencryptedauthcookiesize.md)<br/> | Чтение/запись<br/> | Размер (в символах) свойства [**гатевайенкриптедаускукие**](imsrdpclienttransportsettings3-gatewayencryptedauthcookie.md) .<br/> |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 7<br/>                                                                              |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                                    |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>            |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>            |
| IID<br/>                      | IID \_ IMsRdpClientTransportSettings3 определен как 3D5B21AC-748D-41DE-8F30-E15169586BD4<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**IMsRdpClientTransportSettings2**](imsrdpclienttransportsettings2.md)
</dt> </dl>

 

 





