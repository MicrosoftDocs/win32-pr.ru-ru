---
description: Обновляет данные для объектов, имеющих данные, предоставляемые поставщиком производительности, например классы счетчиков производительности. Вы можете получать обновленные данные быстрее и без вызова SWbemServices. Get \_ .
ms.assetid: 6aeaa336-fb98-4eda-b746-fc958198d8ae
ms.tgt_platform: multiple
title: Метод SWbemObjectEx.Refresh_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectEx.Refresh_
- ISWbemObjectEx.Refresh_
- ISWbemObjectEx.Refresh_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 904e2b7f9b256596555c8396a699220108d4f37b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711640"
---
# <a name="swbemobjectexrefresh_-method"></a>Свбемобжектекс. Refresh, \_ метод

Метод **Refresh \_** объекта [**свбемобжектекс**](swbemobjectex.md) обновляет данные для объектов, имеющих данные, предоставляемые поставщиком производительности, например [Классы счетчиков производительности](/windows/desktop/CIMWin32Prov/performance-counter-classes). Вы можете получать обновленные данные быстрее и без вызова [**SwbemServices. Get \_**](swbemservices-get.md).

Дополнительные сведения об этом синтаксисе см. [в разделе соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Синтаксис


```VB
SWbemObjectEx.Refresh_( _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ифлагс* \[ в необязательное\]
</dt> <dd>

Зарезервированные флаги операции, если они заданы, должны быть равны 0 (нулю).

</dd> <dt>

*обжвбемнамедвалуесет* \[ в необязательное\]
</dt> <dd>

Объект [**свбемнамедвалуесет**](swbemnamedvalueset.md) , который задает контекст для операции.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="error-codes"></a>Коды ошибок

После завершения метода **Refresh \_** объект **Err** может содержать один из кодов ошибок из следующего списка.

<dl> <dt>

**вбемеррфаилед** -2147749889 (0x80041001)
</dt> <dd>

Произошел сбой внутреннего поставщика, хотя операция была допустимой.

</dd> <dt>

**вбемеррнотфаунд** -2147749890 (0x80041002)
</dt> <dd>

Запрошенный формат не найден.

</dd> <dt>

**вбемерринвалидпараметер** -2147749896 (0x80041008)
</dt> <dd>

Один из параметров вызова указан неправильно.

</dd> <dt>

**вбемерррефрешербуси** -2147749975 (0x80041057)
</dt> <dd>

Обновитель занят другой операцией.

</dd> <dt>

**вбемпартиалресултс** -2147745808 (0x80040010)
</dt> <dd>

Не все объекты, перечислители или вложенные обновления успешно обновлены. Этот возврат не является ошибкой, но указывает на то, что операция была неполной.

</dd> </dl>

## <a name="examples"></a>Примеры

В следующем примере кода скрипта показано, как получить необработанные и обработанные счетчики производительности для системного процесса. Объекты обновляются каждые две секунды и отображаются свойствами.


```VB
' Get the performance counter instance for the System process
set PerfRaw = GetObject( _
    "winmgmts:win32_perfrawdata_perfproc_process.name='system'")
set PerfCooked = GetObject( _
    "winmgmts:win32_perfformatteddata_perfproc_process.name='system'")

' Display some properties in a loop
for I = 1 to 5
    Wscript.Echo "HandleCount = "& PerfRaw.HandleCount & _
         " Raw ThreadCount = " & PerfRaw.ThreadCount & _
        " Cooked ThreadCount = " & PerfCooked.ThreadCount
    
    Wscript.Sleep 2000
    
' Refresh the objects
    PerfRaw.Refresh_
    PerfCooked.Refresh_
next
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Библиотека типов<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_СВБЕМОБЖЕКТЕКС CLSID<br/>                                                         |
| IID<br/>                      | IID \_ исвбемобжектекс<br/>                                                          |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**свбемобжектекс**](swbemobjectex.md)
</dt> <dt>

[Мониторинг данных производительности](monitoring-performance-data.md)
</dt> </dl>

 

