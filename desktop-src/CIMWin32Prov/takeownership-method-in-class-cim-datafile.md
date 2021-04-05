---
description: Метод Такеовнершип получает владение логическим файлом, указанным в пути к объекту.
ms.assetid: 0835c335-0ada-44c1-9e71-44ba2041d8e2
ms.tgt_platform: multiple
title: Метод Такеовнершип класса CIM_DataFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DataFile.TakeOwnerShip
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1ade501db9b6af21b3761b70f638faa20d699401
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990566"
---
# <a name="takeownership-method-of-the-cim_datafile-class"></a>Метод Такеовнершип \_ класса CIM File

Метод **такеовнершип** получает владение логическим файлом, указанным в пути к объекту. Если логический файл является каталогом, этот метод будет выполняться рекурсивно, при этом становится владельцем всех файлов и подкаталогов, содержащихся в каталоге. Этот метод наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).

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

Возвращает значение 0 в случае успешного выполнения и любое другое число для указания ошибки. Дополнительные коды ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**0**
</dt> <dd>

Успешно.

</dd> <dt>

**2**
</dt> <dd>

Доступ запрещен.

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

## <a name="remarks"></a>Комментарии

Метод **такеовнершип** в [**\_ файле CIM**](cim-datafile.md) реализуется инструментарием WMI.

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

[\_Файл CIM](takeownership-method-in-class-cim-datafile.md)
</dt> <dt>

[**\_Файл CIM**](cim-datafile.md)
</dt> <dt>

[Задачи WMI: файлы и папки](/windows/desktop/WmiSdk/wmi-tasks--files-and-folders)
</dt> <dt>

[**Константы прав доступа к файлам и каталогам**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)
</dt> </dl>

 

