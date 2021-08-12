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
ms.openlocfilehash: a3c7c44acd410566c4f048cdf36bac904c18b21df42f53543051e3b94f49bfbb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118609376"
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

## <a name="remarks"></a>Remarks

Для вызова этого метода необходимо быть членом группы администраторов.

файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI). файлы MOF не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows Software Development Kit (SDK). Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера. Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

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

 

