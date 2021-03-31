---
description: Метод Item объекта Свбемкуалифиерсет Возвращает именованный объект Свбемкуалифиер из коллекции. Это метод по умолчанию для этого объекта.
ms.assetid: 5ed3a336-c06f-446d-85d4-243daddc82a5
ms.tgt_platform: multiple
title: Метод Свбемкуалифиерсет. Item (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemQualifierSet.Item
- ISWbemQualifierSet.Item
- ISWbemQualifierSet.Item
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 9c89ff554b049e6730a64ebf7e5f017fc8a5652f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913191"
---
# <a name="swbemqualifiersetitem-method"></a>Свбемкуалифиерсет. Item, метод

Метод **Item** объекта [**свбемкуалифиерсет**](swbemqualifierset.md) Возвращает именованный объект [**свбемкуалифиер**](swbemqualifier.md) из коллекции. Это метод по умолчанию для этого объекта.

Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Синтаксис


```VB
objQualifier = .Item( _
  ByVal strName, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*strName* \[ окне\]
</dt> <dd>

Обязательный. Имя извлекаемого описателя.

</dd> <dt>

*ифлагс* \[ в необязательное\]
</dt> <dd>

Зарезервировано. Значение по умолчанию — 0 (нуль).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

В случае успешного выполнения возвращается запрошенный объект [**свбемкуалифиер**](swbemqualifier.md) .

## <a name="error-codes"></a>Коды ошибок

После завершения метода **Item** объект **Err** может содержать один из кодов ошибок из следующего списка.

<dl> <dt>

**вбемерринвалидпараметер** -2147749896 (0x80041008)
</dt> <dd>

Недопустимый параметр *ифлагс* .

</dd> <dt>

**вбемеррфаилед** -2147749889 (0x80041001)
</dt> <dd>

Незаданная ошибка.

</dd> <dt>

**вбемеррнотфаунд** -2147749890 (0x80041002)
</dt> <dd>

Указанный квалификатор не существует.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Библиотека типов<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_СВБЕМКУАЛИФИЕРСЕТ CLSID<br/>                                                     |
| IID<br/>                      | IID \_ исвбемкуалифиерсет<br/>                                                      |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**свбемкуалифиерсет**](swbemqualifierset.md)
</dt> <dt>

[**свбемкуалифиер**](swbemqualifier.md)
</dt> </dl>

 

 




