---
description: Метод Remove объекта Свбемпривилежесет удаляет права доступа из коллекции.
ms.assetid: 4c0b6d49-262c-4840-955b-35b16b68f29f
ms.tgt_platform: multiple
title: Метод Свбемпривилежесет. Remove (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPrivilegeSet.Remove
- ISWbemPrivilegeSet.Remove
- ISWbemPrivilegeSet.Remove
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: f277e291a4296253d7c0b1b11c694952ddc17ddf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910276"
---
# <a name="swbemprivilegesetremove-method"></a>Свбемпривилежесет. Remove, метод

Метод **Remove** объекта [**свбемпривилежесет**](swbemprivilegeset.md) удаляет права доступа из коллекции.

Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Синтаксис


```VB
SWbemPrivilegeSet.Remove( _
  ByVal iPrivilege _
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ипривилеже* 
</dt> <dd>

Обязательный. Это одна из констант WMI из группы [**вбемпривилежеенум**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum) . Эти константы по сути представляют собой целые числа, представляющие определенные привилегии. Например, чтобы удалить привилегию, позволяющую завершить работу системы Windows, используйте константу **вбемпривилежешутдовн** или числовой эквивалент 0x17.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="error-codes"></a>Коды ошибок

После завершения метода **Remove** объект **Err** может содержать один из кодов ошибок из следующего списка.

<dl> <dt>

**вбемеррфаилед** -2147749889 (0x80041001)
</dt> <dd>

Незаданная ошибка.

</dd> <dt>

**вбемеррнотфаунд** -2147749890 (0x80041002)
</dt> <dd>

Указанное право доступа не существует.

</dd> </dl>

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
</dt> </dl>

 

 




