---
description: Получает владение файлом записи логического каталога, указанным в пути объекта. Этот метод является расширенной версией метода Такеовнершип.
ms.assetid: 73726207-e885-4957-bff8-6903c4b99278
ms.tgt_platform: multiple
title: Метод Такеовнершипекс класса Win32_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory.TakeOwnerShipEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3893b7acef182005603f4a80a51caf159b54dd31cc2a966d5dc9940a5164681d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118418517"
---
# <a name="takeownershipex-method-of-the-win32_directory-class"></a>Метод Такеовнершипекс \_ класса каталога Win32

Метод  [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) такеовнершипекс получает владение файлом записи логического каталога, указанным в пути объекта. Этот метод является расширенной версией метода [**такеовнершип**](takeownership-method-in-class-win32-directory.md) . Если логический файл фактически является каталогом, этот метод работает рекурсивно, принимая во внимание владение всеми файлами и подкаталогами, которые содержит каталог.

В этом разделе используется синтаксис MOF-файл (MOF). Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Синтаксис


```mof
uint32 TakeOwnerShipEx(
  [out]          string  StopFileName,
  [in, optional] string  StartFileName,
  [in, optional] boolean Recursive
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Стопфиленаме* \[ заполняет\]
</dt> <dd>

Имя файла или каталога, в котором произошел сбой метода **такеовнершипекс** . Если метод выполнен, этот параметр имеет **значение NULL** .

</dd> <dt>

*StartFileName* \[ в необязательное\]
</dt> <dd>

Имя дочернего файла или каталога, который будет использоваться в качестве отправной точки для **такеовнершипекс**. Параметр *StartFileName* обычно представляет собой параметр *стопфиленаме* , указывающий файл или каталог, в котором произошла ошибка из предыдущего вызова метода. Если этот параметр имеет **значение NULL**, операция выполняется над файлом или каталогом, указанным в вызове метода [**ExecMethod**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execmethod) .

Если используется параметр *StartFileName* , то для *рекурсии* необходимо также задать значение true.

</dd> <dt>

*Рекурсивно* \[ в необязательное\]
</dt> <dd>

Если **значение — true**, изменение владельца применяется рекурсивно к файлам и каталогам в каталоге, указанном в экземпляре [**CIM \_ LogicalFile**](cim-logicalfile.md) .

> [!Note]  
> Для экземпляров файлов *рекурсивный* входной параметр игнорируется.

 

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает целочисленное значение 0 (нуль) при успешном выполнении и любое другое число для указания ошибки.

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

## <a name="examples"></a>Примеры

следующий код скрипта Visual Basic вызывает метод [**такеовнершипекс**](takeownershipex-method-in-class-cim-directory.md) , чтобы стать владельцем папки C: \\ temp.


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:\\" & strComputer & "\root\CIMV2") 
' Obtain the definition of the class.
Set objShare = objWMIService.Get("Win32_Directory")
' Obtain an InParameters object specific
' to the method.
Set objInParam = objShare.Methods_("TakeOwnerShipEx").inParameters.SpawnInstance_()

' Add the input parameters.
objInParam.Properties_.Item("Recursive") =  true

' Execute the method and obtain the return status.
' The OutParameters object in objOutParams
' is created by the provider.
Set objOutParams = objWMIService.ExecMethod("Win32_Directory.Name='C:\Temp'", "TakeOwnerShipEx", objInParam)
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

[Классы операционной системы](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**\_Каталог Win32**](win32-directory.md)
</dt> </dl>

 

