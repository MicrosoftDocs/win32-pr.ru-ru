---
description: Изменяет разрешения безопасности для логического файла, указанного в пути к объекту.
ms.assetid: a3caa717-ad37-4e4f-9f4e-f37aed382fa4
ms.tgt_platform: multiple
title: Метод Чанжесекуритипермиссионс класса CIM_LogicalFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalFile.ChangeSecurityPermissions
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0c85bbbe516fba9d86941edbb0a599b0483c4f3a843abab6fc5b13fb38f1d234
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118010369"
---
# <a name="changesecuritypermissions-method-of-the-cim_logicalfile-class"></a>Метод Чанжесекуритипермиссионс \_ класса CIM LogicalFile

Метод **чанжесекуритипермиссионс** изменяет разрешения безопасности для логического файла, указанного в пути объекта. Если логический файл является каталогом, **чанжесекуритипермиссионс** будет работать рекурсивно, изменив разрешения безопасности для всех файлов и подкаталогов, содержащихся в каталоге.

> [!IMPORTANT]
> Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI. В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

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

Указывает сведения о безопасности.

> [!Note]  
> **Пустой** список управления доступом (ACL) в [**\_ дескрипторе безопасности**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) предоставляет неограниченный доступ.

 

</dd> <dt>

*Параметр* \[ окне\]
</dt> <dd>

Права безопасности для изменения. Например, чтобы изменить безопасность владельца и DACL, используйте:

`Option = 1 + 4`

или диспетчер конфигурации служб

`Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`

<dt>

<span id="Change_Owner_Security_Information"></span><span id="change_owner_security_information"></span><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span>

<span id="Change_Owner_Security_Information"></span><span id="change_owner_security_information"></span><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span>**Изменить \_ \_ \_ Сведения о безопасности владельца** (1)


</dt> <dd>

Изменение владельца логического файла.

</dd> <dt>

<span id="Change_Group_Security_Information"></span><span id="change_group_security_information"></span><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span>

<span id="Change_Group_Security_Information"></span><span id="change_group_security_information"></span><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span>**Изменить \_ \_ \_ Сведения о безопасности группы** (2)


</dt> <dd>

Измените группу логического файла.

</dd> <dt>

<span id="Change_Dacl_Security_Information"></span><span id="change_dacl_security_information"></span><span id="CHANGE_DACL_SECURITY_INFORMATION"></span>

<span id="Change_Dacl_Security_Information"></span><span id="change_dacl_security_information"></span><span id="CHANGE_DACL_SECURITY_INFORMATION"></span>**Изменить \_ \_ \_ Сведения о безопасности DACL** (4)


</dt> <dd>

Измените список управления доступом для логического файла.

</dd> <dt>

<span id="Change_Sacl_Security_Information"></span><span id="change_sacl_security_information"></span><span id="CHANGE_SACL_SECURITY_INFORMATION"></span>

<span id="Change_Sacl_Security_Information"></span><span id="change_sacl_security_information"></span><span id="CHANGE_SACL_SECURITY_INFORMATION"></span>**Изменить \_ \_ \_ Сведения о безопасности SACL** (8)


</dt> <dd>

Изменение ACL системы для логического файла.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение 0 в случае успешного выполнения и любое другое число для указания ошибки.

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

Недопустимый объект.

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

Недопустимый параметр.

</dd> </dl>

## <a name="remarks"></a>Remarks

В настоящее время этот метод не реализован инструментарием WMI. Чтобы использовать этот метод, его необходимо реализовать в собственном поставщике.

Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF. Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.

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

[**\_LOGICALFILE CIM**](changesecuritypermissions-method-in-class-cim-logicalfile.md)
</dt> <dt>

[**\_LOGICALFILE CIM**](cim-logicalfile.md)
</dt> </dl>

 

