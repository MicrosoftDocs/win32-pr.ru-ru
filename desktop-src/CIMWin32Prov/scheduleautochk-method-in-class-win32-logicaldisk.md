---
description: Планирует запуск Autochk на диске, представленном консолью Win32 LogicalDisk при \_ следующей перезагрузке, если установлен бит "грязный".
ms.assetid: 34f4c26b-6bfb-45d9-9d6c-0a9b735355f3
ms.tgt_platform: multiple
title: Метод Счедулеауточк класса Win32_LogicalDisk
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LogicalDisk.ScheduleAutoChk
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7e4920bdded79a7f63cbe7beaf28a70837ad7a47c2b28a1e37d83208b4f4e6f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119588194"
---
# <a name="scheduleautochk-method-of-the-win32_logicaldisk-class"></a>Метод Счедулеауточк \_ класса LogicalDisk Win32

Метод класса **счедулеауточк** планирует выполнение Autochk на диске, представленном в [**Win32 \_ LogicalDisk**](win32-logicaldisk.md) при следующей перезагрузке, если установлен бит "грязный".

В этом разделе используется синтаксис MOF-файл (MOF). Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Синтаксис


```mof
uint32 ScheduleAutoChk(
  [in] string LogicalDisk[]
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Логический* \[ диск окне\]
</dt> <dd>

Указывает список дисков, которые нужно запланировать для выполнения Autochk при следующей перезагрузке. Строковый синтаксис состоит из буквы диска, за которой следует двоеточие для логического диска, например: "C:"

> [!Note]  
> Всегда проверяйте допустимость букв дисков в массиве *LogicalDisk* , когда данные поступают из неизвестного источника или ненадежного источника.

 

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение 0 (нуль) в случае успеха и другое значение, если возникает какая-либо другая ошибка. Значения перечислены в следующем списке. Дополнительные коды ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Без ошибок** (0)
</dt> <dt>

**Ошибка-удаленный диск** (1)
</dt> <dt>

**Ошибка — съемный накопитель** (2)
</dt> <dt>

**Ошибка-диск не является корневым каталогом** (3)
</dt> <dt>

**Ошибка-неизвестный диск** (4)
</dt> </dl>

## <a name="remarks"></a>Remarks

Этот метод применим только к тем экземплярам логического диска, которые представляют физический диск на компьютере. Этот метод неприменим к сопоставленным логическим дискам.

## <a name="examples"></a>Примеры

Следующие примеры VBScript и PowerShell планируются Autochk.exe для запуска на диске C при следующем перезагрузке компьютера.


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set objDisk = objWMIService.Get("Win32_LogicalDisk") 
 
errReturn = objDisk.ScheduleAutoChk(Array("C:")) 
```


```PowerShell

Invoke-WmiMethod -path win32_logicaldisk -Name ScheduleAutoChk -ArgumentList @(&quot;C:&quot;)
```





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

[**Win32 \_ LogicalDisk**](win32-logicaldisk.md)
</dt> </dl>

 

