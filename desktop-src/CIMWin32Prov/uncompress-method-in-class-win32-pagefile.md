---
description: Распаковывает логический файл подкачки (или каталог), указанный в пути объекта.
ms.assetid: 9bd98ba8-068e-49af-8dd4-e5ee987eb31d
ms.tgt_platform: multiple
title: Метод uncompressия класса Win32_PageFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PageFile.Uncompress
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9eb9a7729ecf7a414a25ad3156237676681e94bc43a0f394b6bd6f12add0eb22
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119834583"
---
# <a name="uncompress-method-of-the-win32_pagefile-class"></a>Метод uncompressия \_ класса файла подкачки Win32

Метод **uncompressия** [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) распаковывает логический файл подкачки (или каталог), указанный в пути объекта.

В этом разделе используется синтаксис MOF-файл (MOF). Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Синтаксис


```mof
uint32 Uncompress();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение 0 (нуль), если файл был успешно распакован, и любое другое число для указания ошибки.

<dl> <dt>

**0**
</dt> <dd>

Запрос выполнен успешно.

</dd> <dt>

**2**
</dt> <dd>

Отказано в доступе.

</dd> <dt>

**8**
</dt> <dd>

Произошла неопределенная ошибка.

</dd> <dt>

**9**
</dt> <dd>

Указано недопустимое имя.

</dd> <dt>

**10**
</dt> <dd>

Указанный объект уже существует.

</dd> <dt>

**11**
</dt> <dd>

Файловая система не является системой NTFS.

</dd> <dt>

**12**
</dt> <dd>

Платформа не Windows.

</dd> <dt>

**13**
</dt> <dd>

Диск не совпадает.

</dd> <dt>

**14**
</dt> <dd>

Каталог не пуст.

</dd> <dt>

**15**
</dt> <dd>

Нарушение общего доступа.

</dd> <dt>

**16**
</dt> <dd>

Указан недопустимый файл запуска.

</dd> <dt>

**17**
</dt> <dd>

Привилегия, необходимая для операции, не удерживается.

</dd> <dt>

**открыт**
</dt> <dd>

Указан недопустимый параметр.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Пространство имен<br/>                | Корневой \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Классы операционной системы](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**\_Файл подкачки Win32**](win32-pagefile.md)
</dt> </dl>

 

