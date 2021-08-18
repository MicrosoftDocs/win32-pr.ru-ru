---
title: Интерфейс IMsRdpClientTransportSettings2
description: Управляет параметрами транспорта клиента для сервера шлюза удаленный рабочий стол (шлюза удаленных рабочих столов). | Интерфейс IMsRdpClientTransportSettings2
ms.assetid: 4f9f1905-2693-4666-9f6f-6e00b1eb6a0f
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов интерфейса IMsRdpClientTransportSettings2
- Службы удаленных рабочих столов интерфейса IMsRdpClientTransportSettings2, описание
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings2
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 479fdceee0a1fc168725ef9b5acccb471e1b32b8c13a0e0ff6b12096f14ff0ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000954"
---
# <a name="imsrdpclienttransportsettings2-interface"></a>Интерфейс IMsRdpClientTransportSettings2

Управляет параметрами транспорта клиента для сервера шлюза удаленный рабочий стол (шлюза удаленных рабочих столов).

## <a name="members"></a>Элементы

Интерфейс **IMsRdpClientTransportSettings2** наследует от [**имсрдпклиенттранспортсеттингс**](imsrdpclienttransportsettings.md). **IMsRdpClientTransportSettings2** также имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Интерфейс **IMsRdpClientTransportSettings2** имеет следующие свойства.



| Свойство                                                                                                    | Тип доступа           | Описание                                                                                       |
|:------------------------------------------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------|
| [**гатевайкредшаринг**](imsrdpclienttransportsettings2-gatewaycredsharing.md)<br/>                  | Чтение/запись<br/> | Указывает, включен ли компонент единого входа для шлюза удаленных рабочих столов.<br/>                |
| [**гатевайдомаин**](imsrdpclienttransportsettings2-gatewaydomain.md)<br/>                            | Чтение/запись<br/> | Имя домена, которое пользователь предоставляет для подключения к серверу шлюза удаленных рабочих столов.<br/>              |
| [**гатевайенкриптедотпкукие**](imsrdpclienttransportsettings2-gatewaypreauthserveraddr.md)<br/>     | Чтение/запись<br/> | Зашифрованный файл cookie OTP.<br/>                                                              |
| [**гатевайенкриптедотпкукиесизе**](imsrdpclienttransportsettings2-gatewaypreauthserveraddr.md)<br/> | Чтение/запись<br/> | Размер зашифрованного файла cookie OTP (в байтах).<br/>                                       |
| [**гатевайпассворд**](imsrdpclienttransportsettings2-gatewaypassword.md)<br/>                        | Только на запись<br/> | Пароль, предоставляемый пользователем для подключения к серверу шлюза удаленных рабочих столов.<br/>                 |
| [**гатевайпреаусрекуиремент**](imsrdpclienttransportsettings2-gatewaypreauthrequirement.md)<br/>    | Чтение/запись<br/> | Указывает, включена ли функция одноразового пароля для шлюза удаленных рабочих столов (OTP).<br/>           |
| [**гатевайпреауссервераддр**](imsrdpclienttransportsettings2-gatewaypreauthserveraddr.md)<br/>      | Чтение/запись<br/> | Веб-адрес сервера предварительной проверки подлинности.<br/>                                      |
| [**гатевайсуппортурл**](imsrdpclienttransportsettings2-gatewaypreauthserveraddr.md)<br/>             | Чтение/запись<br/> | Веб-адрес сайта, который предоставляет техническую поддержку для сервера шлюза удаленных рабочих столов.<br/> |
| [**гатевайусернаме**](imsrdpclienttransportsettings2-gatewayusername.md)<br/>                        | Чтение/запись<br/> | Имя пользователя, которое предоставляет пользователь для подключения к серверу шлюза удаленных рабочих столов.<br/>                |



 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista с пакетом обновления 1 (SP1)<br/>                                                                 |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                                    |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>            |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>            |
| IID<br/>                      | IID \_ IMsRdpClientTransportSettings2 определен как 67341688-D606-4c73-A5D2-2E0489009319<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**имсрдпклиенттранспортсеттингс**](imsrdpclienttransportsettings.md)
</dt> </dl>

 

 





