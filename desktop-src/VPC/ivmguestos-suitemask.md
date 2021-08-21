---
title: Свойство Суитемаск Ивмгуестос (Впккоминтерфацес. h)
description: Получает Суитемаск гостевой операционной системы, работающей на виртуальной машине.
ms.assetid: 11d065c1-9d46-4c81-b843-776db3507a04
keywords:
- Суитемаск свойство Virtual PC
- Суитемаск свойство Virtual PC, интерфейс Ивмгуестос
- Ивмгуестос интерфейс Virtual PC, свойство Суитемаск
topic_type:
- apiref
api_name:
- IVMGuestOS.SuiteMask
- IVMGuestOS.get_SuiteMask
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22075c68ef30fda7360f25e76c84dbffbf7e306335a0ef20bda45559cb6dac09
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119472302"
---
# <a name="ivmguestossuitemask-property"></a>Свойство Ивмгуестос:: Суитемаск

\[Windows Virtual PC больше не доступен для использования в Windows 8. Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Получает Суитемаск гостевой операционной системы, работающей на виртуальной машине.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_SuiteMask(
  [out, retval] BSTR *suiteMask
);
```



## <a name="property-value"></a>Значение свойства

Маска набора. Поддерживаются следующие строковые значения.



| Значение                                                                                   | Значение                                                                                                                                                                |
|-----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0x00000004</dt> </dl> | Компоненты Microsoft BackOffice установлены.<br/>                                                                                                              |
| <dl> <dt>"0x00000400"</dt> </dl> | Windows Установлен сервер 2003, Web Edition.<br/>                                                                                                              |
| <dl> <dt>"0x00004000"</dt> </dl> | Windows Сервер 2003, установлен выпуск Compute Cluster Edition.<br/>                                                                                                  |
| <dl> <dt>"0x00000080"</dt> </dl> | Windows Server 2008 R2 Datacenter, Windows server 2008 datacenter, Windows server 2003, datacenter Edition или Windows 2000 datacenter Server.<br/> |
| <dl> <dt>0x00000002</dt> </dl> | установлен Windows Server 2008 R2 Enterprise Windows server 2008 Enterprise, Windows server 2003, выпуск Enterprise или Windows 2000 Advanced server.<br/>   |
| <dl> <dt>0x00000040</dt> </dl> | Windows Установлен XP Embedded.<br/>                                                                                                                           |
| <dl> <dt>"0x00000200"</dt> </dl> | Windows установлена домашняя Premium Vista, Windows vista home Basic или Windows XP home Edition.<br/>                                                              |
| <dl> <dt>0x00000100</dt> </dl> | Удаленный рабочий стол поддерживается, но поддерживается только один интерактивный сеанс.<br/>                                                                                 |
| <dl> <dt>0x00000001</dt> </dl> | Microsoft Small Business Server был установлен в системе, но может быть обновлен до другой версии Windows.<br/>                                 |
| <dl> <dt>0x00000020</dt> </dl> | Microsoft Small Business Server устанавливается с лицензией на клиентскую лицензию принудительно.<br/>                                                                  |
| <dl> <dt>0x00002000</dt> </dl> | установлен Windows служба хранилища server 2003 R2 или Windows служба хранилища server 2003.<br/>                                                                                 |
| <dl> <dt>0x00000010</dt> </dl> | Службы удаленных рабочих столов установлен. Это значение всегда задано.<br/>                                                                                             |
| <dl> <dt>"0x00008000"</dt> </dl> | Windows Установлен домашний сервер.<br/>                                                                                                                           |



 

## <a name="error-codes"></a>Коды ошибок



| Имя/значение                                                                                                                                                                       | Значение                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>С \_ ОК</dt> <dt>0</dt> </dl>                                          | Операция выполнена успешно.<br/>                        |
| <dl> <dt>Д \_ </dt> <dt>0x80004003</dt> указателя </dl>                            | Параметр имеет **значение NULL**.<br/>                           |
| <dl> <dt>Виртуальная машина \_ \_Виртуальная машина E \_ не \_ работает</dt> <dt>0xA0040206</dt> </dl>               | Виртуальная машина не запущена.<br/>                               |
| <dl> <dt>Виртуальная машина \_ Добавление компонента "E" \_ \_ \_ не \_ </dt> доступно <dt>0xA0040505</dt> </dl> | Компоненты интеграции не установлены в этой виртуальной машине.<br/> |
| <dl> <dt> \_ E \_ Exception</dt> <dt>0x80020009</dt> </dl>                    | Произошла непредвиденная ошибка.<br/>                    |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>                                                    |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                     |
| Окончание поддержки клиента<br/>    | Windows 7<br/>                                                                          |
| Продукт<br/>                  | Windows Virtual PC<br/>                                                                 |
| Заголовок<br/>                   | <dl> <dt>Впккоминтерфацес. h</dt> </dl> |
| IID<br/>                      | IID \_ ивмгуестос определен как 99fea0db-4880-499a-b6d8-73dff9bc91be<br/>                 |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ивмгуестос**](ivmguestos.md)
</dt> </dl>

 

