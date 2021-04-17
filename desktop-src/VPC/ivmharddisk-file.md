---
title: Свойство файла Ивмхарддиск (Впккоминтерфацес. h)
description: Получает полный путь к файлу виртуального жесткого диска.
ms.assetid: 8c1f028a-32e6-4b70-b19c-bed7c2d53de1
keywords:
- Свойство файла Virtual PC
- Свойство файла Virtual PC, интерфейс Ивмхарддиск
- Ивмхарддиск интерфейс Virtual PC, свойство File
topic_type:
- apiref
api_name:
- IVMHardDisk.File
- IVMHardDisk.get_File
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43b2a83b92bb5d02049066f9be90543a34a2fe7d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105691925"
---
# <a name="ivmharddiskfile-property"></a>Ивмхарддиск:: File, свойство

\[Windows Virtual PC больше не доступна для использования в Windows 8. Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Получает полный путь к файлу виртуального жесткого диска.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_File(
  [out, retval] BSTR *hardDiskfile
);
```



## <a name="property-value"></a>Значение свойства

Полный путь к текущему файлу образа жесткого диска.

## <a name="error-codes"></a>Коды ошибок



| Имя/значение                                                                                                                                                    | Значение                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>С \_ ОК</dt> <dt>0</dt> </dl>                       | Операция выполнена успешно.<br/>     |
| <dl> <dt>Д \_ </dt> <dt>0x80004003</dt> указателя </dl>         | Параметр имеет **значение NULL**.<br/>        |
| <dl> <dt> \_ E \_ Exception</dt> <dt>0x80020009</dt> </dl> | Произошла непредвиденная ошибка.<br/> |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/>                                                    |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                     |
| Окончание поддержки клиента<br/>    | Windows 7<br/>                                                                          |
| Продукт<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Впккоминтерфацес. h</dt> </dl> |
| IID<br/>                      | IID \_ ивмхарддиск определен как ffa14ae6-48f5-42a4-8a22-186f2e5c7db0<br/>                |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ивмхарддиск**](ivmharddisk.md)
</dt> </dl>

 

