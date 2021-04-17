---
description: Метод Аддасстринг объекта Свбемпривилежесет можно использовать для добавления прав доступа к коллекции Свбемпривилежесет с помощью строки привилегий.
ms.assetid: 729ed4e3-2c5c-4bb4-acc6-cf9ad0d5eaf1
ms.tgt_platform: multiple
title: Свбемпривилежесет. Аддасстринг, метод (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPrivilegeSet.AddAsString
- ISWbemPrivilegeSet.AddAsString
- ISWbemPrivilegeSet.AddAsString
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: b3a740141b14766080a09d01b36b5c0202351eda
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703168"
---
# <a name="swbemprivilegesetaddasstring-method"></a>Свбемпривилежесет. Аддасстринг, метод

Метод **аддасстринг** объекта [**свбемпривилежесет**](swbemprivilegeset.md) можно использовать для добавления прав доступа к коллекции **свбемпривилежесет** с помощью строки привилегий. Этот метод используется для добавления привилегий или для разрешения доступа к объектам [**свбемсекурити**](swbemsecurity.md) . См. раздел [выполнение привилегированных операций с помощью VBScript](executing-privileged-operations-using-vbscript.md).

Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Синтаксис


```VB
objPrivilege = .AddAsString( _
  ByVal strPrivilege, _
  [ ByVal bIsEnabled ] _
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*стрпривилеже* 
</dt> <dd>

Обязательный. Одна из строк привилегий. Полный список этих строк и связанные с ними константы WMI см. в разделе [**константы прав**](privilege-constants.md). Каждая строка прав представляет собой конкретную привилегию. Например, чтобы добавить привилегию, которая используется для завершения работы компьютерной системы, используйте строку **сешутдовнпривилеже** .

</dd> <dt>

*бисенаблед* \[ используемых\]
</dt> <dd>

Логическое значение, которое включает или отключает эту привилегию. По умолчанию используется значение **True**.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

В случае успеха этот метод возвращает объект [**свбемпривилеже**](swbemprivilege.md) , представляющий новую привилегию. В противном случае возвращается пустой объект.

## <a name="error-codes"></a>Коды ошибок

После завершения метода **аддасстринг** объект **Err** может содержать код ошибки из следующего списка.

<dl> <dt>

**вбемеррфаилед** -2147749889 (0x80041001)
</dt> <dd>

Незаданная ошибка.

</dd> </dl>

## <a name="examples"></a>Примеры

В следующем примере кода VBScript создается новый порт для сервера печати с помощью [**Win32 \_ ткпиппринтерпорт**](/windows/desktop/CIMWin32Prov/win32-tcpipprinterport). Для этой операции требуется **селоаддриверпривилеже** . См. раздел [выполнение привилегированных операций](executing-privileged-operations.md).


```VB
Set objWMIService = GetObject("Winmgmts:")
objWMIService.Security_.Privileges. _
    AddAsString "SeLoadDriverPrivilege", True
Set objNewPort = objWMIService.Get _
    ("Win32_TCPIPPrinterPort").SpawnInstance_
objNewPort.Name = "IP_111.222.111.11"
objNewPort.Protocol = 1
objNewPort.HostAddress = "111.222.111.11"
objNewPort.PortNumber = "9999"
objNewPort.SNMPEnabled = False
objNewPort.Put_
```



Пример кода, использующий этот метод, также описывается в разделе [**свбемпривилежесет**](swbemprivilegeset.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Библиотека типов<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_СВБЕМПРИВИЛЕЖЕСЕТ CLSID<br/>                                                     |
| IID<br/>                      | IID \_ исвбемпривилежесет<br/>                                                      |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**свбемпривилежесет**](swbemprivilegeset.md)
</dt> <dt>

[**Свбемпривилежесет. Add**](swbemprivilegeset-add.md)
</dt> <dt>

[**Свбемпривилежесет. Remove**](swbemprivilegeset-remove.md)
</dt> <dt>

[**вбемпривилежеенум**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)
</dt> <dt>

[**Константы прав доступа**](privilege-constants.md)
</dt> <dt>

[Выполнение привилегированных операций](executing-privileged-operations.md)
</dt> <dt>

[Выполнение привилегированных операций с помощью VBScript](executing-privileged-operations-using-vbscript.md)
</dt> </dl>

 

