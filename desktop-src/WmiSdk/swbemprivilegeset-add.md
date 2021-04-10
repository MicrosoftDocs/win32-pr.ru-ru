---
description: Метод Add объекта Свбемпривилежесет добавляет объект Свбемпривилеже в коллекцию Свбемпривилежесет. Если в коллекции уже есть привилегия с таким именем, она будет заменена.
ms.assetid: 7d44193f-60e1-4e83-8640-31d8df509d98
ms.tgt_platform: multiple
title: Метод Свбемпривилежесет. Add (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPrivilegeSet.Add
- ISWbemPrivilegeSet.Add
- ISWbemPrivilegeSet.Add
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 080b9d3e3ab6dbfc0ed8afc8ac0476981b7c26e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080527"
---
# <a name="swbemprivilegesetadd-method"></a>Свбемпривилежесет. Add, метод

Метод **Add** объекта [**Свбемпривилежесет**](swbemprivilegeset.md) добавляет объект [**свбемпривилеже**](swbemprivilege.md) в коллекцию **свбемпривилежесет** . Если в коллекции уже есть привилегия с таким именем, она будет заменена.

Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Синтаксис


```VB
objPrivilege = .Add( _
  ByVal iPrivilege, _
  [ ByVal bIsEnabled ] _
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ипривилеже* 
</dt> <dd>

Обязательный. Одна из констант WMI из группы [**вбемпривилежеенум**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum) . Эти константы по сути представляют собой целые числа, представляющие определенные привилегии. Например, чтобы добавить привилегию, позволяющую завершить работу компьютера, используйте константу **вбемпривилежешутдовн** . В скрипте необходимо использовать числовой эквивалент 23 (0x17). Полный список этих констант и связанные строки прав доступа см. в разделе [**константы прав**](privilege-constants.md).

</dd> <dt>

*бисенаблед* \[ используемых\]
</dt> <dd>

Логическое значение, которое включает или отключает эту привилегию. Значение по умолчанию — **true**.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

В случае успеха метод возвращает объект [**свбемпривилеже**](swbemprivilege.md) , представляющий новую привилегию. В противном случае возвращается пустой объект.

## <a name="error-codes"></a>Коды ошибок

После завершения метода **Add** объект **Err** может содержать код ошибки из следующего списка.

<dl> <dt>

**вбемеррфаилед** -2147749889 (0x80041001)
</dt> <dd>

Незаданная ошибка.

</dd> </dl>

## <a name="examples"></a>Примеры

Пример кода с использованием этого метода описан в разделе [**свбемпривилежесет**](swbemprivilegeset.md) .

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

[Выполнение привилегированных операций](executing-privileged-operations.md)
</dt> <dt>

[Выполнение привилегированных операций с помощью VBScript](executing-privileged-operations-using-vbscript.md)
</dt> <dt>

[**Свбемпривилежесет. Аддасстринг**](swbemprivilegeset-addasstring.md)
</dt> <dt>

[**Свбемпривилежесет. Remove**](swbemprivilegeset-remove.md)
</dt> <dt>

[**вбемпривилежеенум**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)
</dt> <dt>

[**Константы прав доступа**](privilege-constants.md)
</dt> </dl>

 

 




