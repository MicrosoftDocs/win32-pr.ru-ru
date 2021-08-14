---
title: Свойство Item Ивмдвддривеколлектион (Впккоминтерфацес. h)
description: Извлекает объект CD или DVD-дисковода, соответствующий указанному индексу.
ms.assetid: ecc94eea-9ddc-46c8-87e2-e67aca83eecc
keywords:
- Свойство элемента Virtual PC
- Свойство элемента Virtual PC, интерфейс Ивмдвддривеколлектион
- Интерфейс Ивмдвддривеколлектион Virtual PC, свойство Item
topic_type:
- apiref
api_name:
- IVMDVDDriveCollection.Item
- IVMDVDDriveCollection.get_Item
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55ea8cd86d45827c06f4ef3582cc0d2ff990a176e244483db52101deb596745b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117753745"
---
# <a name="ivmdvddrivecollectionitem-property"></a>Свойство Ивмдвддривеколлектион:: Item

\[Windows Virtual PC больше не доступен для использования в Windows 8. Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Извлекает объект CD или DVD-дисковода, соответствующий указанному индексу.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_Item(
  [in]          long        index,
  [out, retval] IVMDVDDrive **dvdDrive
);
```



## <a name="property-value"></a>Значение свойства

Объект [**ивмдвддриве**](ivmdvddrive.md) .

## <a name="error-codes"></a>Коды ошибок



| Имя/значение                                                                                                                                                    | Значение                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <dl> <dt>С \_ ОК</dt> <dt>0</dt> </dl>                       | Операция выполнена успешно. <br/>                                                      |
| <dl> <dt>Д \_ </dt> <dt>0x80004003</dt> указателя </dl>         | Параметр имеет **значение NULL**.<br/>                                                          |
| <dl> <dt>Д \_ Сбой</dt> <dt>0x80004005</dt> </dl>            | Произошла непредвиденная ошибка.<br/>                                                   |
| <dl> <dt> \_ E \_ бадиндекс</dt> <dt>0x8002000B</dt> </dl>  | Индекс запрошенного элемента не соответствует элементу в этой коллекции. <br/> |
| <dl> <dt>Виртуальная машина \_ \_Неизвестный \_ 0xA0040207 виртуальной машины</dt> <dt></dt> </dl> | Конфигурация неизвестна.<br/>                                                       |
| <dl> <dt> \_ E \_ Exception</dt> <dt>0x80020009</dt> </dl> | Произошла непредвиденная ошибка.<br/>                                                   |



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>                                                    |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                     |
| Окончание поддержки клиента<br/>    | Windows 7<br/>                                                                          |
| Продукт<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Впккоминтерфацес. h</dt> </dl> |
| IID<br/>                      | IID \_ ивмдвддривеколлектион определен как bc86e297-e55f-4742-9614-ad11d3131f68<br/>      |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ивмдвддриве**](ivmdvddrive.md)
</dt> <dt>

[**ивмдвддривеколлектион**](ivmdvddrivecollection.md)
</dt> </dl>

 

