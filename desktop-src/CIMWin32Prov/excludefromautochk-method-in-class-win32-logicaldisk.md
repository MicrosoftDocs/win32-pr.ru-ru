---
description: Исключает диски из операции Autochk для выполнения при следующей перезагрузке.
ms.assetid: 5df2bc3b-e149-4853-aa02-af4cb8af6da0
ms.tgt_platform: multiple
title: Метод Ексклудефромауточк класса Win32_LogicalDisk
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LogicalDisk.ExcludeFromAutochk
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a37171c594cb3a51b131220bb604234bcae108fa025ea6343da99fdc998a7dc4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118676132"
---
# <a name="excludefromautochk-method-of-the-win32_logicaldisk-class"></a>Метод Ексклудефромауточк \_ класса LogicalDisk Win32

Метод **ексклудефромауточк** исключает диски из операции **Autochk** для выполнения при следующей перезагрузке.

В этом разделе используется синтаксис MOF-файл (MOF). Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Синтаксис


```mof
uint32 ExcludeFromAutochk(
  [in] string LogicalDisk[]
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Логический* \[ диск окне\]
</dt> <dd>

Список дисков, которые следует исключить из **Autochk** при следующей перезагрузке. Строковый синтаксис состоит из буквы диска, за которой следует двоеточие для логического диска.

Пример: "C:"

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение 0 (ноль), если ошибка не возникает. Значения перечислены в следующем списке. Дополнительные коды ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Успешно** (0)
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

Если этот параметр не исключен, на диске выполняется **Autochk** , если для диска задан бит "грязный". Обратите внимание, что вызовы для исключения дисков не являются кумулятивными. Если выполняется вызов для исключения некоторых дисков, новый список не добавляется в список дисков, которые уже отмечены для исключения. Новый список дисков перезаписывает предыдущий список. Этот метод применим только к тем экземплярам логического диска, которые представляют физический диск на компьютере. Он неприменим к сопоставленным логическим дискам.

## <a name="examples"></a>Примеры

Следующий пример кода VBScript гарантирует, что Autochk.exe не будет выполняться для диска C при следующем перезагрузке компьютера, даже если на диске C установлен "грязный бит".


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set objDisk = objWMIService.Get("Win32_LogicalDisk") 
 
errReturn = objDisk.ExcludeFromAutoChk(Array("C:")) 
```



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

[**Win32 \_ LogicalDisk**](win32-logicaldisk.md)
</dt> <dt>

[Аппаратные классы системы компьютера](computer-system-hardware-classes.md)
</dt> </dl>

 

