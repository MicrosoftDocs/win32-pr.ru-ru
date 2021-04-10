---
description: Получает владение файлом записи логического каталога, указанным в пути объекта. Этот метод является расширенной версией метода Такеовнершип и наследуется от CIM \_ LogicalFile.
ms.assetid: a13acaa2-2203-470a-b989-15f8276e46c6
ms.tgt_platform: multiple
title: Метод Такеовнершипекс класса CIM_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Directory.TakeOwnerShipEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: b02a6c40e99405c150a372f8eb15fe648f2df60a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104140987"
---
# <a name="takeownershipex-method-of-the-cim_directory-class"></a>Метод Такеовнершипекс \_ класса каталога CIM

Метод **такеовнершипекс** получает владение файлом записи логического каталога, указанным в пути объекта. Этот метод является расширенной версией метода [**такеовнершип**](takeownership-method-in-class-cim-directory.md) и наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md). Если логический файл является каталогом, этот метод работает рекурсивно, принимая во внимание владение всеми файлами и подкаталогами, которые содержит каталог.

> [!IMPORTANT]
> Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI. В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

В этом разделе используется синтаксис MOF-файл (MOF). Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Синтаксис


```mof
uint32 TakeOwnerShipEx(
  [out] string REF StopFileName,
  [in]  string     StartFileName,
  [in]  boolean    Recursive
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Стопфиленаме* \[ заполняет\]
</dt> <dd>

Строка, представляющая имя файла (или каталога), в котором произошел сбой метода. Если метод выполнен, этот параметр имеет значение null.

</dd> <dt>

*StartFileName* \[ окне\]
</dt> <dd>

Строка, представляющая дочерний файл (или каталог), используемый в качестве отправной точки для этого метода. Как правило, этот параметр представляет собой параметр *стопфиленаме* , указывающий файл или каталог, в котором произошла ошибка из предыдущего вызова метода. Если этот параметр имеет значение null, операция выполняется над файлом (или каталогом), указанным в вызове метода [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) .

</dd> <dt>

*Рекурсивно* \[ окне\]
</dt> <dd>

Если **значение — true**, метод применяется рекурсивно к файлам и каталогам в каталоге, указанном экземпляром [**\_ каталога CIM**](cim-directory.md) . Для экземпляров файлов этот параметр игнорируется.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение 0 в случае успешного выполнения и любое другое число для указания ошибки.

<dl> <dt>


</dt> <dd>

0

Успешно.

</dd> <dt>


</dt> <dd>

2

Доступ запрещен.

</dd> <dt>


</dt> <dd>

8

Неопределенный сбой.

</dd> <dt>


</dt> <dd>

9

Недопустимый объект.

</dd> <dt>


</dt> <dd>

10

Объект уже существует.

</dd> <dt>


</dt> <dd>

11

Файловая система не NTFS.

</dd> <dt>


</dt> <dd>

12

Платформа не является Windows.

</dd> <dt>


</dt> <dd>

13

Диск не совпадает.

</dd> <dt>


</dt> <dd>

14

Каталог не пуст.

</dd> <dt>


</dt> <dd>

15

Нарушение правил общего доступа.

</dd> <dt>


</dt> <dd>

16

Недопустимый начальный файл.

</dd> <dt>


</dt> <dd>

17

Привилегия не удерживается.

</dd> <dt>


</dt> <dd>

21

Недопустимый параметр.

</dd> </dl>

## <a name="remarks"></a>Комментарии

В настоящее время этот метод не реализован инструментарием WMI. Чтобы использовать этот метод, его необходимо реализовать в собственном поставщике.

Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF. Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.

## <a name="examples"></a>Примеры

Следующий код скрипта Visual Basic вызывает метод **такеовнершипекс** , чтобы стать владельцем папки C: \\ TEMP.


```VB
strComputer = "." 
Set objWMIService = GetObject( _
    "winmgmts:\\" & strComputer & "\root\CIMV2") 
' Obtain the definition of the class.
Set objShare = objWMIService.Get("Win32_Directory")
' Obtain an InParameters object specific
' to the method.
Set objInParam = objShare.Methods_("TakeOwnerShipEx"). _
    inParameters.SpawnInstance_()

' Add the input parameters.
objInParam.Properties_.Item("Recursive") =  true

' Execute the method and obtain the return status.
' The OutParameters object in objOutParams
' is created by the provider.
Set objOutParams = objWMIService.ExecMethod( _
    "Win32_Directory.Name='C:\Temp'", "TakeOwnerShipEx", objInParam)
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



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[\_Каталог CIM](takeownershipex-method-in-class-cim-directory.md)
</dt> <dt>

[**\_Каталог CIM**](cim-directory.md)
</dt> </dl>

 

