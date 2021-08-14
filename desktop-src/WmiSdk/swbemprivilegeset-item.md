---
description: Метод Item объекта Свбемпривилежесет возвращает объект Свбемпривилеже из коллекции. Метод Item является методом по умолчанию для объекта Свбемпривилежесет.
ms.assetid: 93a35e65-99ee-40da-9415-4151ac635091
ms.tgt_platform: multiple
title: Метод Свбемпривилежесет. Item (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPrivilegeSet.Item
- ISWbemPrivilegeSet.Item
- ISWbemPrivilegeSet.Item
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 93180f168820acce2bf2564ef108c509713a22e68cfa16fbb8f2abeff17b5bc5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118313526"
---
# <a name="swbemprivilegesetitem-method"></a>Свбемпривилежесет. Item, метод

Метод **Item** объекта [**Свбемпривилежесет**](swbemprivilegeset.md) возвращает объект [**свбемпривилеже**](swbemprivilege.md) из коллекции. Метод **Item** является методом по умолчанию для объекта **свбемпривилежесет** .

Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Синтаксис


```VB
objPrivilege = .Item( _
  ByVal iPrivilege _
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ипривилеже* 
</dt> <dd>

Обязательный. Одна из констант WMI из группы [**вбемпривилежеенум**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum) . Эти константы по сути представляют собой целые числа, представляющие определенные привилегии. например, чтобы получить право на завершение работы Windowsной системы, используйте константу **вбемпривилежешутдовн** или числовой эквивалент, равный 23 (0x17).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

В случае успешного выполнения возвращается запрошенный объект [**свбемпривилеже**](swbemprivilege.md) .

## <a name="error-codes"></a>Коды ошибок

После завершения метода **Item** объект **Err** может содержать один из кодов ошибок из следующего списка.

<dl> <dt>

**вбемеррфаилед** -2147749889 (0x80041001)
</dt> <dd>

Незаданная ошибка.

</dd> <dt>

**вбемеррнотфаунд** -2147749890 (0x80041002)
</dt> <dd>

Указанное право доступа не существует.

</dd> </dl>

## <a name="examples"></a>Примеры

В следующем примере кода VBScript используется метод **Item** .


```VB
strComputer ="."
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate}!\\" & strComputer _
    & "\root\cimv2")
Set colServices = objWMIService.ExecQuery( _
    "Select * from Win32_Service")
For Each objService In colServices
    WScript.Echo objService.Properties_.Item("Caption")
Next
```



## <a name="requirements"></a>Requirements (Требования)



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

[**свбемпривилеже**](swbemprivilege.md)
</dt> </dl>

 

 




