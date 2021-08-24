---
description: Изменяет разрешения безопасности для файла записи каталога, указанного в пути к объекту (этот метод является расширенной версией метода Чанжесекуритипермиссионс).
ms.assetid: 787e48af-7cb4-4d0b-a2f1-ffa696466ef2
ms.tgt_platform: multiple
title: Метод Чанжесекуритипермиссионсекс класса Win32_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory.ChangeSecurityPermissionsEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8d90a6a76067421c3b23c0ec5124fa5da85e029e81d0307a2b4b66d01231fe56
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119323034"
---
# <a name="changesecuritypermissionsex-method-of-the-win32_directory-class"></a>Метод Чанжесекуритипермиссионсекс \_ класса каталога Win32

Метод  [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) чанжесекуритипермиссионсекс изменяет разрешения безопасности для файла записи каталога, указанного в пути к объекту (этот метод является расширенной версией метода [**чанжесекуритипермиссионс**](changesecuritypermissions-method-in-class-win32-directory.md) ). Если логический файл является каталогом, этот метод является рекурсивным и изменяет разрешения безопасности для всех файлов и подкаталогов, содержащихся в каталоге.

В этом разделе используется синтаксис MOF-файл (MOF). Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Синтаксис


```mof
uint32 ChangeSecurityPermissionsEx(
  [in]           Win32_SecurityDescriptor SecurityDescriptor,
  [in]           uint32                   Option,
  [out]          string                   StopFileName,
  [in, optional] string                   StartFileName,
  [in, optional] boolean                  Recursive
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*SecurityDescriptor* \[ окне\]
</dt> <dd>

Выражение, которое разрешается в экземпляре [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor). Этот параметр содержит новые разрешения безопасности для экземпляра [**\_ файла подкачки Win32**](win32-pagefile.md).

</dd> <dt>

*Параметр* \[ окне\]
</dt> <dd>

Права безопасности, которые необходимо изменить. Например, чтобы изменить уровень безопасности владельца и избирательного списка управления доступом (DACL), используйте следующую команду:

`Option = 1 + 4`

-или-

`Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`

<dt>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**Изменить \_ \_ \_ Сведения о безопасности владельца** (1)


</dt> <dd>

Изменение владельца логического файла.

</dd> <dt>

<span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>

<span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**Изменить \_ \_ \_ Сведения о безопасности группы** (2)


</dt> <dd>

Измените группу логического файла.

</dd> <dt>

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**Изменить \_ \_ \_ Сведения о безопасности DACL** (4)


</dt> <dd>

Изменение списка DACL логического файла.

</dd> <dt>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**Изменить \_ \_ \_ Сведения о безопасности SACL** (8)


</dt> <dd>

Измените системный список управления доступом (SACL) логического файла.

</dd> </dl> </dd> <dt>

*Стопфиленаме* \[ заполняет\]
</dt> <dd>

Имя файла или каталога, в котором произошел сбой метода **чанжесекуритипермиссионсекс** . Если метод выполнен, этот параметр имеет значение null.

</dd> <dt>

*StartFileName* \[ в необязательное\]
</dt> <dd>

Имя дочернего файла или каталога, который будет использоваться в качестве отправной точки для **чанжесекуритипермиссионсекс**. Как правило, параметр *StartFileName* — это параметр *стопфиленаме* , указывающий файл или каталог, в котором произошла ошибка из предыдущего вызова метода. Если этот параметр имеет значение null, операция выполняется над файлом или каталогом, указанным в вызове метода **ExecMethod** . Это необязательный параметр.

Если используется параметр *StartFileName* , то для *рекурсии* необходимо также задать значение true.

</dd> <dt>

*Рекурсивно* \[ в необязательное\]
</dt> <dd>

Если **значение — true**, изменение владельца применяется рекурсивно к файлам и каталогам в каталоге, указанном в экземпляре [**CIM \_ LogicalFile**](cim-logicalfile.md) . Для экземпляров файлов *рекурсивный* входной параметр игнорируется. Этот параметр является необязательным.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение 0 (ноль), если разрешения изменяются, и другое число, указывающее на ошибку.

<dl> <dt>

**Успешно**
</dt> <dd>

0

Запрос выполнен успешно.

</dd> <dt>

**Доступ запрещен**
</dt> <dd>

2

Отказано в доступе".

</dd> <dt>

**Неопределенный сбой**
</dt> <dd>

8

Произошла неопределенная ошибка.

</dd> <dt>

**Недопустимый объект**
</dt> <dd>

9

Указано недопустимое имя.

</dd> <dt>

**Объект уже существует**
</dt> <dd>

10

Указанный объект уже существует.

</dd> <dt>

**Файловая система не NTFS**
</dt> <dd>

11

Файловая система не является файловой системой NTFS.

</dd> <dt>

**платформа не NT/Windows 2000**
</dt> <dd>

12

Платформа не Windows.

</dd> <dt>

**Диск не совпадает**
</dt> <dd>

13

Диск не совпадает.

</dd> <dt>

**Каталог не пуст**
</dt> <dd>

14

Каталог не пуст.

</dd> <dt>

**Нарушение общего доступа**
</dt> <dd>

15

Нарушение общего доступа.

</dd> <dt>

**Недопустимый файл запуска**
</dt> <dd>

16

Указан недопустимый файл запуска.

</dd> <dt>

**Привилегия не удерживается**
</dt> <dd>

17

Привилегия, необходимая для операции, не удерживается.

</dd> <dt>

**недопустимый параметр.**
</dt> <dd>

21

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

[**\_Каталог Win32**](win32-directory.md)
</dt> </dl>

 

