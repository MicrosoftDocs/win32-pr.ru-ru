---
description: Метод Delete удаляет логический файл (или каталог), указанный в пути объекта. Этот метод наследуется от CIM \_ LogicalFile.
ms.assetid: 490d0578-a545-423b-9640-ec09f4ef8d96
ms.tgt_platform: multiple
title: Метод Delete класса CIM_DeviceFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceFile.Delete
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 32e29808b60c9933bec927ed7e351fc8c5aa9250
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072415"
---
# <a name="delete-method-of-the-cim_devicefile-class"></a>Метод DELETE \_ класса ДЕВИЦЕФИЛЕ CIM

Метод **Delete** удаляет логический файл (или каталог), указанный в пути объекта. Этот метод наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).

> [!IMPORTANT]
> Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI. В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

В этом разделе используется синтаксис MOF-файл (MOF). Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Синтаксис


```mof
uint32 Delete();
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

[\_ДЕВИЦЕФИЛЕ CIM](delete-method-in-class-cim-devicefile.md)
</dt> <dt>

[**\_ДЕВИЦЕФИЛЕ CIM**](cim-devicefile.md)
</dt> </dl>

 

