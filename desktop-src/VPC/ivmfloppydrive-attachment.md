---
title: Свойство вложения Ивмфлоппидриве (Впккоминтерфацес. h)
description: Возвращает тип носителя, подключенного к дисководу гибких дисков в виртуальной машине.
ms.assetid: 0b7e43ac-de56-4c4b-82e6-75877aea06f2
keywords:
- Свойство вложения Virtual PC
- Свойство вложения Virtual PC, интерфейс Ивмфлоппидриве
- Ивмфлоппидриве интерфейс Virtual PC, свойство вложения
topic_type:
- apiref
api_name:
- IVMFloppyDrive.Attachment
- IVMFloppyDrive.get_Attachment
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44814148baf27672f30b8e3c5015d841aaaba4b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105691858"
---
# <a name="ivmfloppydriveattachment-property"></a>Свойство Ивмфлоппидриве:: вложение

\[Windows Virtual PC больше не доступна для использования в Windows 8. Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Возвращает тип носителя, подключенного к дисководу гибких дисков виртуальной машины.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_Attachment(
  [out, retval] VMFloppyDriveAttachmentType *driveAttachment
);
```



## <a name="property-value"></a>Значение свойства

Тип носителя. Список значений см. в разделе [**вмфлоппидривеаттачменттипе**](vmfloppydriveattachmenttype.md).

## <a name="error-codes"></a>Коды ошибок



| Имя/значение                                                                                                                                                    | Значение                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>С \_ ОК</dt> <dt>0</dt> </dl>                       | Операция выполнена успешно.<br/>                                  |
| <dl> <dt>Д \_ </dt> <dt>0x80004003</dt> указателя </dl>         | Параметр имеет **значение NULL**.<br/>                                     |
| <dl> <dt>Виртуальная машина \_ \_Неизвестный \_ 0xA0040207 виртуальной машины</dt> <dt></dt> </dl> | Конфигурация для этой виртуальной машины недопустима или не найдена.<br/> |
| <dl> <dt> \_ E \_ Exception</dt> <dt>0x80020009</dt> </dl> | Произошла непредвиденная ошибка.<br/>                              |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/>                                                    |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                     |
| Окончание поддержки клиента<br/>    | Windows 7<br/>                                                                          |
| Продукт<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Впккоминтерфацес. h</dt> </dl> |
| IID<br/>                      | IID \_ ивмфлоппидриве определен как 661abee6-112a-4ed9-babf-3c874969f10e<br/>             |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ивмфлоппидриве**](ivmfloppydrive.md)
</dt> </dl>

 

