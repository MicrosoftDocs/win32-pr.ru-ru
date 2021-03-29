---
description: Изменяет разрешения безопасности для логического файла ярлыка, указанного в пути к объекту (этот метод является расширенной версией метода Чанжесекуритипермиссионс).
ms.assetid: 9a5c9fa9-ccd9-4792-969f-28f52ab9bc52
ms.tgt_platform: multiple
title: Метод Чанжесекуритипермиссионсекс класса Win32_ShortcutFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ShortcutFile.ChangeSecurityPermissionsEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 124f8d883b89379e4b36c5dd33b029718fbbd469
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538780"
---
# <a name="changesecuritypermissionsex-method-of-the-win32_shortcutfile-class"></a>Метод Чанжесекуритипермиссионсекс \_ класса Win32 шорткутфиле

Метод  [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) чанжесекуритипермиссионсекс изменяет разрешения безопасности для логического файла ярлыка, указанного в пути объекта (этот метод является расширенной версией метода [**чанжесекуритипермиссионс**](changesecuritypermissions-method-in-class-win32-directory.md) ). Если логический файл является каталогом, этот метод является рекурсивным и изменяет разрешения безопасности для всех файлов и подкаталогов, содержащихся в каталоге.

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

или

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

Изменение списка управления доступом на уровне пользователей (DACL) логического файла.

</dd> <dt>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**Изменить \_ \_ \_ Сведения о безопасности SACL** (8)


</dt> <dd>

Измените системный список управления доступом (SACL) логического файла.

</dd> </dl> </dd> <dt>

*Стопфиленаме* \[ заполняет\]
</dt> <dd>

Имя файла или каталога, в котором произошел сбой метода **чанжесекуритипермиссионсекс** . Если метод выполнен, этот параметр имеет **значение NULL** .

</dd> <dt>

*StartFileName* \[ в необязательное\]
</dt> <dd>

Имя дочернего файла или каталога, который будет использоваться в качестве отправной точки для **чанжесекуритипермиссионсекс**. Как правило, параметр *StartFileName* — это параметр *стопфиленаме* , указывающий файл или каталог, в котором произошла ошибка из предыдущего вызова метода. Если этот параметр имеет **значение NULL**, операция выполняется над файлом или каталогом, указанным в вызове метода [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) .

</dd> <dt>

*Рекурсивно* \[ в необязательное\]
</dt> <dd>

Если **значение — true**, изменение владельца применяется рекурсивно к файлам и каталогам в каталоге, указанном в экземпляре [**CIM \_ LogicalFile**](cim-logicalfile.md) .

> [!Note]  
> Для экземпляров файлов *рекурсивный* параметр игнорируется.

 

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

**Платформа не NT/Windows 2000**
</dt> <dd>

12

Платформа не является Windows.

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

[**\_Шорткутфиле Win32**](win32-shortcutfile.md)
</dt> </dl>

 

