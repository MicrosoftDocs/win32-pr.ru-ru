---
title: Интерфейс IMsRdpDeviceV2
description: Содержит сведения об объекте устройства. Это усовершенствование интерфейса Имсрдпдевице.
ms.assetid: 9a380a1a-d44f-4147-8917-bf1e07dbac15
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов интерфейса IMsRdpDeviceV2
- Службы удаленных рабочих столов интерфейса IMsRdpDeviceV2, описание
topic_type:
- apiref
api_name:
- IMsRdpDeviceV2
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c46e1e4df8f9cd521d67383960e9ccf5060bb2d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681758"
---
# <a name="imsrdpdevicev2-interface"></a>Интерфейс IMsRdpDeviceV2

Содержит сведения об объекте устройства. Это усовершенствование интерфейса [**имсрдпдевице**](imsrdpdevice.md) .

## <a name="members"></a>Элементы

Интерфейс **IMsRdpDeviceV2** наследует от [**имсрдпдевице**](imsrdpdevice.md). **IMsRdpDeviceV2** также имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Интерфейс **IMsRdpDeviceV2** имеет следующие свойства.



| Свойство                                                                 | Тип доступа          | Описание                                                                                        |
|:-------------------------------------------------------------------------|:---------------------|:---------------------------------------------------------------------------------------------------|
| [**кмклассгуид**](imsrdpdevicev2-cmclassguid.md)<br/>             | Только для чтения<br/> | Содержит GUID класса установки Configuration Manager для устройства.<br/>                     |
| [**кмдевицеинстанце**](imsrdpdevicev2-cmdeviceinstance.md)<br/>   | Только для чтения<br/> | Содержит экземпляр устройства Configuration Manager.<br/>                       |
| [**девицетекст**](imsrdpdevicev2-devicetext.md)<br/>               | Только для чтения<br/> | Содержит текст устройства.<br/>                                                               |
| [**дривелеттербитмап**](imsrdpdevicev2-driveletterbitmap.md)<br/> | Только для чтения<br/> | Содержит битовое значение, представляющее собой карту букв диска, содержащихся в устройстве.<br/> |
| [**искомпоситедевице**](imsrdpdevicev2-iscompositedevice.md)<br/> | Только для чтения<br/> | Указывает, является ли устройство составным.<br/>                                          |
| [**исоптионалдевице**](imsrdpdevicev2-isoptionaldevice.md)<br/>   | Только для чтения<br/> | Указывает, является ли устройство необязательным для перенаправления USB.<br/>                                |
| [**исусбдевице**](imsrdpdevicev2-isusbdevice.md)<br/>             | Только для чтения<br/> | Указывает, что устройство предназначено для перенаправления USB.<br/>                                         |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 7 с пакетом обновления 1 (SP1)<br/>                                                          |
| Минимальная версия сервера<br/> | Windows Server 2008 R2 с пакетом обновления 1 (SP1)<br/>                                             |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpDeviceV2 определен как 5fb94466-7661-42a8-98b7-01904c11668f<br/>      |



 

 





