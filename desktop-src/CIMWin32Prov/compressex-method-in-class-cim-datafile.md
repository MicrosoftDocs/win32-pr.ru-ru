---
description: Метод Компрессекс класса CIM_DataFile — использует сжатие NTFS для сжатия логического файла (или каталога), указанного в пути к объекту. Этот метод наследуется от CIM \_ LogicalFile.
ms.assetid: 553b6a90-d16c-4abb-9015-66fe8e1606f6
ms.tgt_platform: multiple
title: Метод Компрессекс класса CIM_DataFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DataFile.CompressEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: ccc155c04c6c25f38050bd37827eb0c2e2e0e73e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089792"
---
# <a name="compressex-method-of-the-cim_datafile-class"></a>Метод Компрессекс \_ класса CIM File

Метод **компрессекс** использует сжатие NTFS для сжатия логического файла (или каталога), указанного в пути к объекту. Этот метод наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md). Этот метод является расширенной версией метода [**сжатия**](compress-method-in-class-cim-datafile.md) и наследуется от [CIM \_ LogicalFile](/windows/desktop/WmiSdk/calling-a-method).

> [!IMPORTANT]
> Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI. В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

В этом разделе используется синтаксис MOF-файл (MOF). Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Синтаксис


```mof
uint32 CompressEx(
  [out] string  StopFileName,
  [in]  string  StartFileName,
  [in]  boolean Recursive
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Стопфиленаме* \[ заполняет\]
</dt> <dd>

Строка, представляющая имя файла (или каталога), в котором произошел сбой метода. Если метод выполнен, этот параметр имеет значение null.

</dd> <dt>

*StartFileName* \[ окне\]
</dt> <dd>

Строка, представляющая дочерний файл (или каталог), используемый в качестве отправной точки для этого метода. Как правило, параметр *StartFileName* — это параметр *стопфиленаме* , указывающий файл или каталог, в котором произошла ошибка из предыдущего вызова метода. Если этот параметр имеет значение null, операция выполняется над файлом или каталогом, указанным в вызове метода **ExecMethod** .

Если используется параметр *StartFileName* , то для *рекурсии* необходимо также задать значение true.

</dd> <dt>

*Рекурсивно* \[ окне\]
</dt> <dd>

Если **значение — true**, метод также применяется рекурсивно к файлам и каталогам в каталоге, указанном в экземпляре [**\_ файла данных CIM**](cim-datafile.md) . Для экземпляров файлов этот параметр игнорируется.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение 0 (нуль) при успешном выполнении и любое другое число для указания ошибки. Дополнительные коды ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**0**
</dt> <dd>

Успешно.

</dd> <dt>

**2**
</dt> <dd>

Access denied. (Недопустимое значение {значение_утверждения} для утверждения {имя_утверждения}. Доступ запрещен.)

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

## <a name="remarks"></a>Remarks

Метод **компрессекс** в [**\_ файле CIM**](cim-datafile.md) реализуется инструментарием WMI.

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

[\_Файл CIM](compressex-method-in-class-cim-datafile.md)
</dt> <dt>

[**\_Файл CIM**](cim-datafile.md)
</dt> <dt>

[Задачи WMI: файлы и папки](/windows/desktop/WmiSdk/wmi-tasks--files-and-folders)
</dt> <dt>

[**Константы прав доступа к файлам и каталогам**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)
</dt> </dl>

 

