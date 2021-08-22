---
description: Распаковывает логический файл (или каталог), указанный в пути объекта.
ms.assetid: 0de01859-4a4b-4d70-802d-c52b2f56d7a1
ms.tgt_platform: multiple
title: Метод uncompressия класса CIM_LogicalFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalFile.Uncompress
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 268b30348ac7cb05d99e4f44dc36b6f887adb05a4d0238f2dd9632549360be78
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119642944"
---
# <a name="uncompress-method-of-the-cim_logicalfile-class"></a>Метод uncompressия класса CIM \_ LogicalFile

Метод **uncompressия** распаковывает логический файл (или каталог), указанный в пути объекта.

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

платформа не Windows NT на основе.

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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Пространство имен<br/>                | Корневой \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[\_LOGICALFILE CIM](uncompress-method-in-class-cim-logicalfile.md)
</dt> <dt>

[**\_LOGICALFILE CIM**](cim-logicalfile.md)
</dt> </dl>

 

