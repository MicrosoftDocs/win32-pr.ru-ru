---
description: Метод Такеовнершип класса CIM_Directory — метод Такеовнершип получает владение логическим файлом, указанным в пути объекта.
ms.assetid: 053647d0-3ba0-4cd4-a84a-a1a96ef7151c
ms.tgt_platform: multiple
title: Метод Такеовнершип класса CIM_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Directory.TakeOwnerShip
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 12c328f30e56db348b018b73b02aa4320bf99505
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086062"
---
# <a name="takeownership-method-of-the-cim_directory-class"></a>Метод Такеовнершип \_ класса каталога CIM

Метод **такеовнершип** получает владение логическим файлом, указанным в пути объекта. Если логический файл является каталогом, этот метод работает рекурсивно, принимая во внимание владение всеми файлами и подкаталогами, которые содержит каталог. Этот метод наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).

> [!IMPORTANT]
> Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI. В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

В этом разделе используется синтаксис MOF-файл (MOF). Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Синтаксис


```mof
uint32 TakeOwnerShip();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение 0 (нуль) при успешном выполнении и любое другое число для указания ошибки.

<dl> <dt>

**0**
</dt> <dd>

Успешно.

</dd> <dt>

**2**
</dt> <dd>

Access denied. (Недопустимое значение {значение_утверждения} для утверждения {имя_утверждения}. Доступ запрещен.)

</dd> <dt>

**8**
</dt> <dd>

Неопределенный сбой.

</dd> <dt>

**9**
</dt> <dd>

Недопустимый объект.

</dd> <dt>

**10**
</dt> <dd>

Объект уже существует.

</dd> <dt>

**11**
</dt> <dd>

Файловая система не NTFS.

</dd> <dt>

**12**
</dt> <dd>

Платформа не является Windows.

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

Нарушение правил общего доступа.

</dd> <dt>

**16**
</dt> <dd>

Недопустимый начальный файл.

</dd> <dt>

**17**
</dt> <dd>

Привилегия не удерживается.

</dd> <dt>

**открыт**
</dt> <dd>

Недопустимый параметр.

</dd> </dl>

## <a name="remarks"></a>Remarks

В настоящее время этот метод не реализован инструментарием WMI. Чтобы использовать этот метод, его необходимо реализовать в собственном поставщике.

Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF. Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.

## <a name="examples"></a>Примеры

Следующий код скрипта Visual Basic вызывает метод **такеовнершип** , чтобы стать владельцем папки C: \\ TEMP.


```VB
strComputer = "." 

Set objWMIService = _
    GetObject("winmgmts:\\" & strComputer & "\root\CIMV2") 

' Obtain the definition of the class.
Set objShare = objWMIService.Get("Win32_Directory")

' Execute the method and obtain the return status.
' The OutParameters object in objOutParams
' is created by the provider.
Set objOutParams = objWMIService.ExecMethod( _
    "Win32_Directory.Name='C:\\temp'", "TakeOwnerShip")

wscript.echo objOutParams.ReturnValue
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Пространство имен<br/>                | Корневой \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[\_Каталог CIM](takeownership-method-in-class-cim-directory.md)
</dt> <dt>

[**\_Каталог CIM**](cim-directory.md)
</dt> </dl>

 

