---
title: Свойство Ивмхарддискконнектионколлектион Count (Впккоминтерфацес. h)
description: Возвращает число подключений к жестким дискам в этой коллекции.
ms.assetid: 913c1bb7-0237-4f11-9873-7b42a94004f8
keywords:
- Число свойств Virtual PC
- Число свойств Virtual PC, интерфейс Ивмхарддискконнектионколлектион
- Ивмхарддискконнектионколлектион интерфейс Virtual PC, свойство Count
topic_type:
- apiref
api_name:
- IVMHardDiskConnectionCollection.Count
- IVMHardDiskConnectionCollection.get_Count
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fccb00cf2388db8a971f5da2f726030b3f793ac878f4a59df2646195eb41ef15
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119974332"
---
# <a name="ivmharddiskconnectioncollectioncount-property"></a>Свойство Ивмхарддискконнектионколлектион:: count

\[Windows Virtual PC больше не доступен для использования в Windows 8. Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Возвращает число подключений к жестким дискам в этой коллекции.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_Count(
  [out, retval] long *count
);
```



## <a name="property-value"></a>Значение свойства

Число подключений к жестким дискам.

## <a name="error-codes"></a>Коды ошибок



| Имя/значение                                                                                                                                                    | Значение                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>С \_ ОК</dt> <dt>0</dt> </dl>                       | Операция выполнена успешно.<br/>     |
| <dl> <dt>Д \_ </dt> <dt>0x80004003</dt> указателя </dl>         | Параметр имеет **значение NULL**.<br/>        |
| <dl> <dt>Виртуальная машина \_ \_Неизвестный \_ 0xA0040207 виртуальной машины</dt> <dt></dt> </dl> | Конфигурация неизвестна.<br/>     |
| <dl> <dt> \_ E \_ Exception</dt> <dt>0x80020009</dt> </dl> | Произошла непредвиденная ошибка.<br/> |



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>                                                         |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                          |
| Окончание поддержки клиента<br/>    | Windows 7<br/>                                                                               |
| Продукт<br/>                  | Windows Virtual PC<br/>                                                                      |
| Заголовок<br/>                   | <dl> <dt>Впккоминтерфацес. h</dt> </dl>      |
| IID<br/>                      | IID \_ ивмхарддискконнектионколлектион определен как b9f2caf4-0aeb-4085-B105-ceddb90dbf62<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**ивмхарддискконнектионколлектион**](ivmharddiskconnectioncollection.md)
</dt> </dl>

 

