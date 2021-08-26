---
description: Удаляет имя общего ресурса из списка общих ресурсов сервера, отключая подключения к общему ресурсу.
ms.assetid: 175f9c0e-0017-4a86-8e05-ad78e2c93c11
ms.tgt_platform: multiple
title: Метод Delete класса Win32_Share
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Share.Delete
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: c1331ce9dfa3309c1cfbd0ba0ddc3b4a0c96d431d524d8f0e74f7937c8cdb332
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119918474"
---
# <a name="delete-method-of-the-win32_share-class"></a>Метод DELETE \_ класса общего ресурса Win32

Метод **удаления** [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) удаляет имя общего ресурса из списка общих ресурсов сервера, отключая подключения к общему ресурсу.

В этом разделе используется синтаксис MOF-файл (MOF). Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Синтаксис


```mof
uint32 Delete();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает одно из значений, перечисленных в следующем списке, или любое другое значение, указывающее на ошибку. Дополнительные коды ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Успешно** (0)
</dt> <dt>

**Отказано в доступе** (2)
</dt> <dt>

**Неизвестный сбой** (8)
</dt> <dt>

**Недопустимое имя** (9)
</dt> <dt>

**Недопустимый уровень** (10)
</dt> <dt>

**Недопустимый параметр** (21)
</dt> <dt>

**Повторяющаяся общая папка** (22)
</dt> <dt>

**Путь перенаправления** (23)
</dt> <dt>

**Неизвестное устройство или каталог** (24)
</dt> <dt>

**Не найдено сетевое имя** (25)
</dt> <dt>

**Другие** (26 4294967295)
</dt> </dl>

## <a name="remarks"></a>Remarks

Метод **Delete** является методом объекта и используется в экземпляре класса.

Только члены локальной группы "Администраторы" или "Операторы учетных записей", а также участники группы операторов связи, печати или сервера могут успешно выполнять метод. Оператор Print может удалять только очереди принтера. Оператор связи может удалять только очереди устройств связи.

## <a name="examples"></a>Примеры

В следующем примере кода VBScript удаляется указанная общая папка.


```VB
On Error Resume Next

ComputerName = InputBox("Enter the computer name:", "Delete Share", "localhost")

SName = InputBox("Enter the name of the share:", "Delete Share")



Set Shares = GetObject("winmgmts:\\" & ComputerName & _
 "\root\cimv2").ExecQuery("SELECT * FROM Win32_Share WHERE name = '" & SName & "'")



For Each Share in Shares
 Share.Delete()
Next
```



В следующем примере кода PowerShell удаляются пустые общие папки.


```PowerShell
$Shares = Get-WMIObject Win32_Share | Where {$_.Name -eq ""}

Foreach ($Share in $Shares) {
   $Share.Delete()
}
"{0} blank shares found and removed" -f $shares.count
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

[Классы операционной системы](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**\_Общий ресурс Win32**](win32-share.md)
</dt> </dl>

 

