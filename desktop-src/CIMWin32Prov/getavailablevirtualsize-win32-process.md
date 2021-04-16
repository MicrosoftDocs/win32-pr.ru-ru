---
description: Получает текущий размер (в байтах) свободного виртуального адресного пространства, доступного процессу.
ms.assetid: 13b3b347-5db1-484f-bd1d-3a604eb6bc5b
ms.tgt_platform: multiple
title: Метод Жетаваилаблевиртуалсизе класса Win32_Process
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Process.GetAvailableVirtualSize
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: ee6e798b8df32822de481f3af1dc6b21a81d1024
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655796"
---
# <a name="getavailablevirtualsize-method-of-the-win32_process-class"></a>Метод Жетаваилаблевиртуалсизе \_ класса процесса Win32

Получает текущий размер (в байтах) свободного виртуального адресного пространства, доступного процессу.

## <a name="syntax"></a>Синтаксис


```mof
uint32 GetAvailableVirtualSize(
  [out] uint64 AvailableVirtualSize
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Аваилаблевиртуалсизе* \[ заполняет\]
</dt> <dd>

Параметр *аваилаблевиртуалсизе* возвращает свободное пространство виртуального адреса, доступное для этого процесса.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает ноль (0), чтобы указать на успешное выполнение. Любое другое значение указывает на ошибку. Дополнительные коды ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Успешное завершение**
</dt> <dd>

0

Операция выполнена успешно.

</dd> <dt>

**Доступ запрещен**
</dt> <dd>

2

У пользователя нет доступа к запрошенной информации

</dd> <dt>

**Недостаточно прав доступа**
</dt> <dd>

3

У пользователя недостаточно прав.

</dd> <dt>

**Неизвестный сбой**
</dt> <dd>

8

Неизвестный сбой.

</dd> <dt>

**Путь не найден**
</dt> <dd>

9

Указанный путь не существует.

</dd> <dt>

**недопустимый параметр.**
</dt> <dd>

21

Указан недопустимый параметр.

</dd> <dt>

**Другое**
</dt> <dd>

22 4294967295

Для значений, отличных от перечисленных, см. документацию по [кодам системных ошибок](/windows/desktop/Debug/system-error-codes) .

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8.1<br/>                                                                  |
| Минимальная версия сервера<br/> | Windows Server 2012 R2<br/>                                                       |
| Пространство имен<br/>                | Корневой \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Процесс Win32**](win32-process.md)
</dt> </dl>

 

