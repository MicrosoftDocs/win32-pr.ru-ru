---
description: Изменяет разрешения безопасности для логического файла ярлыка, указанного в пути объекта.
ms.assetid: abd5aec8-4684-4b8d-8fdf-d3a7a5eec103
ms.tgt_platform: multiple
title: Метод Чанжесекуритипермиссионс класса Win32_ShortcutFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ShortcutFile.ChangeSecurityPermissions
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 43d69f8a04fd937591675fe13fefd9499fe4c0dd59f70da02077cb97f7b06fee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118010106"
---
# <a name="changesecuritypermissions-method-of-the-win32_shortcutfile-class"></a>Метод Чанжесекуритипермиссионс \_ класса Win32 шорткутфиле

Метод  [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) чанжесекуритипермиссионс изменяет разрешения безопасности для логического файла ярлыка, указанного в пути объекта. Если логический файл является каталогом, то **чанжесекуритипермиссионс** является рекурсивным и изменяет разрешения безопасности для всех файлов и подкаталогов, содержащихся в каталоге. **Чанжесекуритипермиссионс** возвращает целочисленное значение 0 (ноль) при изменении разрешений и другое число для указания ошибки.

В этом разделе используется синтаксис MOF-файл (MOF). Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Синтаксис


```mof
uint32 ChangeSecurityPermissions(
  [in] Win32_SecurityDescriptor SecurityDescriptor,
  [in] uint32                   Option
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*SecurityDescriptor* \[ окне\]
</dt> <dd>

Выражение, которое разрешается в экземпляре [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor). Этот дескриптор содержит новые разрешения безопасности для экземпляра [**\_ файла подкачки Win32**](win32-pagefile.md).

</dd> <dt>

*Параметр* \[ окне\]
</dt> <dd>

Фактические права безопасности для изменения. Например, чтобы изменить безопасность владельца и DACL, используйте:

`Option = 1 + 4`

или диспетчер конфигурации служб

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

</dd> </dl> </dd> </dl>

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

[**\_Шорткутфиле Win32**](win32-shortcutfile.md)
</dt> </dl>

 

