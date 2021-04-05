---
description: Распаковывает логический файл записи каталога (или каталог), указанный в пути к объекту. Этот метод наследуется от CIM \_ LogicalFile.
ms.assetid: da3616d0-ce45-4e9a-a570-ca9e6bd0a4fa
ms.tgt_platform: multiple
title: Метод uncompressия класса CIM_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Directory.Uncompress
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: d852305d9153fa61f33168303ccb791caad00f28
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990449"
---
# <a name="uncompress-method-of-the-cim_directory-class"></a>Метод uncompressия \_ класса каталога CIM

Метод **uncompressия** распаковывает логический файл записи каталога (или каталог), указанный в пути к объекту. Этот метод наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).

> [!IMPORTANT]
> Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI. В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

В этом разделе используется синтаксис MOF-файл (MOF). Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Синтаксис


```mof
uint32 Uncompress();
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

[**\_Каталог CIM**](uncompress-method-in-class-cim-directory.md)
</dt> <dt>

[**\_Каталог CIM**](cim-directory.md)
</dt> </dl>

 

