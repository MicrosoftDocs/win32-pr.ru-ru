---
title: Свойство Ивмдвддривеколлектион Count (Впккоминтерфацес. h)
description: Возвращает число дисководов компакт-и DVD в этой коллекции.
ms.assetid: 22e39c42-1f98-4680-a97e-0d329dc608e2
keywords:
- Число свойств Virtual PC
- Число свойств Virtual PC, интерфейс Ивмдвддривеколлектион
- Ивмдвддривеколлектион интерфейс Virtual PC, свойство Count
topic_type:
- apiref
api_name:
- IVMDVDDriveCollection.Count
- IVMDVDDriveCollection.get_Count
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e9ea713810348c0bd78c7de307600fc6ac9adc0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105691871"
---
# <a name="ivmdvddrivecollectioncount-property"></a>Свойство Ивмдвддривеколлектион:: count

\[Windows Virtual PC больше не доступна для использования в Windows 8. Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Возвращает число дисководов компакт-и DVD в этой коллекции.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_Count(
  [out, retval] long *count
);
```



## <a name="property-value"></a>Значение свойства

Число дисководов компакт-дисков и дисков DVD.

## <a name="error-codes"></a>Коды ошибок



| Имя/значение                                                                                                                                                    | Значение                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>С \_ ОК</dt> <dt>0</dt> </dl>                       | Операция выполнена успешно.<br/>     |
| <dl> <dt>Д \_ </dt> <dt>0x80004003</dt> указателя </dl>         | Параметр имеет **значение NULL**.<br/>        |
| <dl> <dt>Д \_ Сбой</dt> <dt>0x80004005</dt> </dl>            | Произошла непредвиденная ошибка.<br/> |
| <dl> <dt>Виртуальная машина \_ \_Неизвестный \_ 0xA0040207 виртуальной машины</dt> <dt></dt> </dl> | Конфигурация неизвестна.<br/>     |
| <dl> <dt> \_ E \_ Exception</dt> <dt>0x80020009</dt> </dl> | Произошла непредвиденная ошибка.<br/> |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/>                                                    |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                     |
| Окончание поддержки клиента<br/>    | Windows 7<br/>                                                                          |
| Продукт<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Впккоминтерфацес. h</dt> </dl> |
| IID<br/>                      | IID \_ ивмдвддривеколлектион определен как bc86e297-e55f-4742-9614-ad11d3131f68<br/>      |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ивмдвддривеколлектион**](ivmdvddrivecollection.md)
</dt> </dl>

 

