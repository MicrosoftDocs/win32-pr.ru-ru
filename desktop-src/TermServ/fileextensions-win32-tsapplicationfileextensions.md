---
title: Метод FileExtensions класса Win32_TSApplicationFileExtensions
description: Предоставляет список расширений имен файлов, обрабатываемых приложением.
ms.assetid: 833a1b68-86ed-4361-bbcb-a8d1c4a9306d
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода FileExtensions
- Службы удаленных рабочих столов метода FileExtensions, класс Win32_TSApplicationFileExtensions
- Класс Win32_TSApplicationFileExtensions службы удаленных рабочих столов, метод FileExtensions
topic_type:
- apiref
api_name:
- Win32_TSApplicationFileExtensions.FileExtensions
api_location:
- TsPubWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5aa0bff92cdc274c8dba56aa11a44791e3ad9f01
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989253"
---
# <a name="fileextensions-method-of-the-win32_tsapplicationfileextensions-class"></a>Метод FileExtensions \_ класса Win32 тсаппликатионфиликстенсионс

Предоставляет список расширений имен файлов, обрабатываемых приложением.

## <a name="syntax"></a>Синтаксис


```mof
uint32 FileExtensions(
  [in]  string AppPath,
  [out] string Extensions[]
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Апппас* \[ окне\]
</dt> <dd>

Путь к приложению.

</dd> <dt>

*Расширения* \[ заполняет\]
</dt> <dd>

Расширения имен файлов, обрабатываемые приложением.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Для вызова этого метода необходимо быть членом группы администраторов.

Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI). MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK). Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера. Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                               |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Пространство имен<br/>                | Корневой \\ CIMv2 \\ терминалсервицес<br/>                                                |
| MOF<br/>                      | <dl> <dt>Тсаллов. mof</dt> </dl>  |
| DLL<br/>                      | <dl> <dt>TsPubWmi.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Тсаппликатионфиликстенсионс Win32**](win32-tsapplicationfileextensions.md)
</dt> </dl>

 

