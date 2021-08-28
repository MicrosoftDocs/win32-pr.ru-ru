---
description: Переименовывает файл кодека, указанный в пути объекта.
ms.assetid: fd6ce02c-d513-4643-ac27-313c32732f1e
ms.tgt_platform: multiple
title: Метод Rename класса Win32_CodecFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CodecFile.Rename
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: c1054ffe0c016c5e06159a13cbdf68d5cfa7521e96727867a74d25a635888165
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120077464"
---
# <a name="rename-method-of-the-win32_codecfile-class"></a>Метод Rename класса Win32 \_ кодекфиле

Метод класса **Rename** [WMI](/windows/desktop/WmiSdk/retrieving-a-class) переименовывает файл кодека, указанный в пути объекта. Переименование не поддерживается, если место назначения находится на другом диске или требуется перезапись существующего логического файла.

В этом разделе используется синтаксис MOF-файл (MOF). Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Синтаксис


```mof
uint32 Rename(
   string FileName
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*FileName* 
</dt> <dd>

Полное новое имя файла (или каталога). Пример: c: \\ temp \\newfile.txt.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает целочисленное значение 0 (ноль), если файл был успешно переименован, и любое другое число для указания ошибки.

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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Пространство имен<br/>                | Корневой \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Классы операционной системы](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**\_Кодекфиле Win32**](win32-codecfile.md)
</dt> </dl>

 

