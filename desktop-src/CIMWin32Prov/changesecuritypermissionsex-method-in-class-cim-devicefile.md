---
description: Изменяет разрешения безопасности для файла устройства, указанного в пути к объекту (этот метод является расширенной версией метода Чанжесекуритипермиссионс).
ms.assetid: 5ad54470-6961-4c0d-9d2a-d3eaf81d75f4
ms.tgt_platform: multiple
title: Метод Чанжесекуритипермиссионсекс класса CIM_DeviceFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceFile.ChangeSecurityPermissionsEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6c6d70c11077873154040e30cabfb460546f79b1088ff124884e35f3698aaf78
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118959143"
---
# <a name="changesecuritypermissionsex-method-of-the-cim_devicefile-class"></a>Метод Чанжесекуритипермиссионсекс \_ класса CIM девицефиле

Метод **чанжесекуритипермиссионсекс** изменяет разрешения безопасности для файла устройства, указанного в пути к объекту (этот метод является расширенной версией метода [**чанжесекуритипермиссионс**](changesecuritypermissions-method-in-class-cim-devicefile.md) ). Если логический файл является каталогом, этот метод работает рекурсивно, изменяя разрешения безопасности для всех файлов и подкаталогов, которые содержит каталог. Этот метод наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).

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

Задает сведения о безопасности.

> [!Caution]  
> Список ACL **со значением NULL** в структуре [**\_ дескрипторов безопасности**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) предоставляет неограниченный доступ.

 

</dd> <dt>

*Параметр* \[ окне\]
</dt> <dd>

Права безопасности для изменения. Например, чтобы изменить безопасность владельца и DACL, используйте

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

Дочерний файл (или каталог) для использования в качестве отправной точки для этого метода. Как правило, параметр *StartFileName* — это параметр *стопфиленаме* , указывающий файл или каталог, в котором произошла ошибка из предыдущего вызова метода. Если этот параметр имеет **значение NULL**, операция выполняется над файлом (или каталогом), указанным в вызове метода [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) .

</dd> <dt>

*Рекурсивно* \[ в необязательное\]
</dt> <dd>

Если **значение — true**, метод также применяется рекурсивно к файлам и каталогам в каталоге, указанном в экземпляре [**CIM \_ девицефиле**](cim-devicefile.md) . Для экземпляров файлов этот параметр игнорируется.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение 0 (нуль) при успешном выполнении и любое другое число для указания ошибки.

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

Платформа не Windows.

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



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[\_ДЕВИЦЕФИЛЕ CIM](changesecuritypermissionsex-method-in-class-cim-devicefile.md)
</dt> <dt>

[**\_ДЕВИЦЕФИЛЕ CIM**](cim-devicefile.md)
</dt> </dl>

 

