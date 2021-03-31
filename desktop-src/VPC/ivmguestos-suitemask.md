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
ms.openlocfilehash: 348384dd729c5c7e63a45fcb8b3f05d0189a7fec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803844"
---
# <a name="ivmguestossuitemask-property"></a>Свойство Ивмгуестос:: Суитемаск

\[Windows Virtual PC больше не доступна для использования в Windows 8. Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

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
| <dl> <dt>"0x00000400"</dt> </dl> | Установлен выпуск Windows Server 2003, Web Edition.<br/>                                                                                                              |
| <dl> <dt>"0x00004000"</dt> </dl> | Windows Server 2003, выпуски Compute Cluster Edition установлены.<br/>                                                                                                  |
| <dl> <dt>"0x00000080"</dt> </dl> | Windows Server 2008 R2 Datacenter, установлен Windows Server 2008 Datacenter, Windows Server 2003, Datacenter Edition или Windows 2000 Datacenter Server.<br/> |
| <dl> <dt>0x00000002</dt> </dl> | Установлен Windows Server 2008 R2 Enterprise, Windows Server 2008 Enterprise, Windows Server 2003, Enterprise Edition или Windows 2000 Advanced Server.<br/>   |
| <dl> <dt>0x00000040</dt> </dl> | Установлена операционная система Windows XP Embedded.<br/>                                                                                                                           |
| <dl> <dt>"0x00000200"</dt> </dl> | Установлена ОС Windows Vista Home Premium, Windows Vista Домашняя базовая или Windows XP Home Edition.<br/>                                                              |
| <dl> <dt>0x00000100</dt> </dl> | Удаленный рабочий стол поддерживается, но поддерживается только один интерактивный сеанс.<br/>                                                                                 |
| <dl> <dt>0x00000001</dt> </dl> | Microsoft Small Business Server был установлен в системе, но может быть обновлен до другой версии Windows.<br/>                                 |
| <dl> <dt>0x00000020</dt> </dl> | Microsoft Small Business Server устанавливается с лицензией на клиентскую лицензию принудительно.<br/>                                                                  |
| <dl> <dt>0x00002000</dt> </dl> | Установлен Windows Storage Server 2003 R2 или Windows Storage Server 2003.<br/>                                                                                 |
| <dl> <dt>0x00000010</dt> </dl> | Службы удаленных рабочих столов установлен. Это значение всегда задано.<br/>                                                                                             |
| <dl> <dt>"0x00008000"</dt> </dl> | Установлен Windows Home Server.<br/>                                                                                                                           |



 

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
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/>                                                    |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                     |
| Окончание поддержки клиента<br/>    | Windows 7<br/>                                                                          |
| Продукт<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Впккоминтерфацес. h</dt> </dl> |
| IID<br/>                      | IID \_ ивмгуестос определен как 99fea0db-4880-499a-b6d8-73dff9bc91be<br/>                 |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ивмгуестос**](ivmguestos.md)
</dt> </dl>

 

