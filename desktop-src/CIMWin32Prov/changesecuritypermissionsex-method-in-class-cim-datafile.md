---
description: Изменяет разрешения безопасности для файла логических данных, указанного в пути к объекту (этот метод является расширенной версией метода Чанжесекуритипермиссионс).
ms.assetid: baf50a6e-f624-464e-946d-975aeba88ac2
ms.tgt_platform: multiple
title: Метод Чанжесекуритипермиссионсекс класса CIM_DataFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DataFile.ChangeSecurityPermissionsEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3c97f9b17fd148a0686a96fb46f77694a2b78b21
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538999"
---
# <a name="changesecuritypermissionsex-method-of-the-cim_datafile-class"></a>Метод Чанжесекуритипермиссионсекс \_ класса CIM File

Метод **чанжесекуритипермиссионсекс** изменяет разрешения безопасности для логического файла данных, указанного в пути к объекту (этот метод является расширенной версией метода [**чанжесекуритипермиссионс**](changesecuritypermissions-method-in-class-cim-datafile.md) ). Если логический файл фактически является каталогом, этот метод будет работать рекурсивно, изменяя разрешения безопасности для всех файлов и подкаталогов, которые содержит каталог.

> [!IMPORTANT]
> Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI. В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

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

Указывает сведения о безопасности.

> [!Note]  
> Список ACL **со значением NULL** в структуре [**\_ дескрипторов безопасности**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) предоставляет неограниченный доступ. Дополнительные сведения о влиянии неограниченного доступа см. в разделе [Создание дескриптора безопасности для нового объекта](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).

 

</dd> <dt>

*Параметр* \[ окне\]
</dt> <dd>

Права безопасности для изменения. Например, чтобы изменить безопасность владельца и DACL, используйте:

`Option = 1 + 4` или `Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`

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

Измените список управления доступом для логического файла.

</dd> <dt>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**Изменить \_ \_ \_ Сведения о безопасности SACL** (8)


</dt> <dd>

Изменение ACL системы для логического файла.

</dd> </dl> </dd> <dt>

*Стопфиленаме* \[ заполняет\]
</dt> <dd>

Строка, представляющая имя файла (или каталога), в котором произошел сбой метода. Если метод выполнен, этот параметр имеет **значение NULL** .

</dd> <dt>

*StartFileName* \[ в необязательное\]
</dt> <dd>

Строка, представляющая дочерний файл (или каталог), используемый в качестве отправной точки для этого метода. Как правило, параметр *StartFileName* — это параметр *стопфиленаме* , указывающий файл или каталог, в котором произошла ошибка из предыдущего вызова метода. Если этот параметр имеет **значение NULL**, операция выполняется над файлом (или каталогом), указанным в вызове метода **ExecMethod** .

Если используется параметр *StartFileName* , то для *рекурсии* необходимо также задать значение true.

</dd> <dt>

*Рекурсивно* \[ в необязательное\]
</dt> <dd>

Если **значение — true**, метод также применяется рекурсивно к файлам и каталогам в каталоге, указанном в экземпляре [**\_ файла данных CIM**](cim-datafile.md) . Для экземпляров файлов этот параметр игнорируется.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение 0 (нуль) при успешном выполнении и любое другое число для указания ошибки. Дополнительные коды ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Успешно**
</dt> <dd>

0

Успешно.

</dd> <dt>

**Доступ запрещен**
</dt> <dd>

2

Доступ запрещен.

</dd> <dt>

**Неопределенный сбой**
</dt> <dd>

8

Неопределенный сбой.

</dd> <dt>

**Недопустимый объект**
</dt> <dd>

9

Указано недопустимое имя объекта.

</dd> <dt>

**Объект уже существует**
</dt> <dd>

10

Объект уже существует.

</dd> <dt>

**Файловая система не NTFS**
</dt> <dd>

11

Файловая система не NTFS.

</dd> <dt>

**Платформа не NT/Windows 2000**
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

Нарушение правил общего доступа.

</dd> <dt>

**Недопустимый файл запуска**
</dt> <dd>

16

Недопустимый начальный файл.

</dd> <dt>

**Привилегия не удерживается**
</dt> <dd>

17

Привилегия не удерживается.

</dd> <dt>

**недопустимый параметр.**
</dt> <dd>

21

Недействительный параметр.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Метод **чанжесекуритипермиссионсекс** в [**\_ файле CIM**](cim-datafile.md) реализуется инструментарием WMI.

Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF. Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.

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

[**\_Файл CIM**](changesecuritypermissionsex-method-in-class-cim-datafile.md)
</dt> <dt>

[**\_Файл CIM**](cim-datafile.md)
</dt> <dt>

[Задачи WMI: файлы и папки](/windows/desktop/WmiSdk/wmi-tasks--files-and-folders)
</dt> <dt>

[**Константы прав доступа к файлам и каталогам**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)
</dt> </dl>

 

