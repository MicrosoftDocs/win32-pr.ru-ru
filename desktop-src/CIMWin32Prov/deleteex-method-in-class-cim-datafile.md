---
description: Метод Делетикс удаляет логический файл (или каталог), указанный в пути к объекту. Этот метод является расширенной версией метода Delete и наследуется от CIM \_ LogicalFile.
ms.assetid: 565d604f-01e0-4cd4-b182-9750c58bae5f
ms.tgt_platform: multiple
title: Метод Делетикс класса CIM_DataFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DataFile.DeleteEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1e52a1d974afdc123e79f85252a68c52aa99e7e78a2b997b6eca1f1bced60997
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119020512"
---
# <a name="deleteex-method-of-the-cim_datafile-class"></a>Метод Делетикс \_ класса CIM File

Метод **делетикс** удаляет логический файл (или каталог), указанный в пути к объекту. Этот метод является расширенной версией метода [**Delete**](delete-method-in-class-cim-datafile.md) и наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).

> [!IMPORTANT]
> Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI. В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

В этом разделе используется синтаксис MOF-файл (MOF). Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Синтаксис


```mof
uint32 DeleteEx(
  [out] string REF StopFileName,
  [in]  string     StartFileName
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

Строка, представляющая дочерний файл (или каталог), используемый в качестве отправной точки для этого метода. Как правило, параметр *StartFileName* — это параметр *стопфиленаме* , указывающий файл или каталог, в котором произошла ошибка из предыдущего вызова метода. Если этот параметр имеет значение null, операция выполняется над файлом (или каталогом), указанным в вызове метода [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) .

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

## <a name="remarks"></a>Remarks

Метод **делетикс** в [**\_ файле CIM**](cim-datafile.md) реализуется инструментарием WMI.

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

[\_Файл CIM](deleteex-method-in-class-cim-datafile.md)
</dt> <dt>

[**\_Файл CIM**](cim-datafile.md)
</dt> <dt>

[Задачи WMI: файлы и папки](/windows/desktop/WmiSdk/wmi-tasks--files-and-folders)
</dt> <dt>

[**Константы прав доступа к файлам и каталогам**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)
</dt> </dl>

 

