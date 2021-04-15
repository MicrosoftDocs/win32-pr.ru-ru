---
description: Метод Копекс копирует логический файл (или каталог), указанный в пути к объекту, в расположение, указанное параметром FileName.
ms.assetid: e52c1a0f-e34c-4a61-9e54-ed172976cb61
ms.tgt_platform: multiple
title: Метод Копекс класса CIM_DataFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DataFile.CopyEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a83f1556aeeafbb5cc95eddbd84806bdaef0be14
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655897"
---
# <a name="copyex-method-of-the-cim_datafile-class"></a>Метод Копекс \_ класса CIM File

Метод **копекс** копирует логический файл (или каталог), указанный в пути к объекту, в расположение, указанное параметром *filename* . Копирование не поддерживается, если требуется перезапись существующего логического файла. Этот метод является расширенной версией метода [**Copy**](copy-method-in-class-cim-datafile.md) и наследуется от [CIM \_ LogicalFile](cim-logicalfile.md).

> [!IMPORTANT]
> Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI. В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

В этом разделе используется синтаксис MOF-файл (MOF). Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Синтаксис


```mof
uint32 CopyEx(
  [in]  string     FileName,
  [out] string REF StopFileName,
  [in]  string     StartFileName,
  [in]  boolean    Recursive
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Имя файла* \[ окне\]
</dt> <dd>

Полное имя целевого файла (или каталога).

Пример: "c: \\ temp \\ невдиректори"

</dd> <dt>

*Стопфиленаме* \[ заполняет\]
</dt> <dd>

Строка, представляющая имя файла (или каталога), в котором произошел сбой метода. Если метод завершится с ошибкой, этот параметр будет иметь **значение NULL** .

</dd> <dt>

*StartFileName* \[ окне\]
</dt> <dd>

Строка, представляющая дочерний файл (или каталог), используемый в качестве отправной точки для этого метода. Как правило, параметр *StartFileName* — это параметр *стопфиленаме* , указывающий файл (или каталог), в котором произошла ошибка из предыдущего вызова метода. Если этот параметр имеет **значение NULL**, операция выполняется над файлом (или каталогом), указанным в вызове метода [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) .

Если используется параметр *StartFileName* , то для *рекурсии* необходимо также задать значение true.

</dd> <dt>

*Рекурсивно* \[ окне\]
</dt> <dd>

Если значение — TRUE, метод также применяется рекурсивно к файлам и каталогам в каталоге, указанном в экземпляре [**\_ файла данных CIM**](cim-datafile.md) . Для экземпляров файлов этот параметр игнорируется.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение 0 (нуль) при успешном выполнении и любое другое число для указания ошибки. Дополнительные коды ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).

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

## <a name="remarks"></a>Комментарии

Метод **копекс** в [**\_ файле CIM**](cim-datafile.md) реализуется инструментарием WMI.

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

[**\_Файл CIM**](cim-datafile.md)
</dt> <dt>

[Задачи WMI: файлы и папки](/windows/desktop/WmiSdk/wmi-tasks--files-and-folders)
</dt> <dt>

[**Константы прав доступа к файлам и каталогам**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)
</dt> </dl>

 

