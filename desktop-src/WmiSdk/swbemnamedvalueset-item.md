---
description: Метод Item объекта Свбемнамедвалуесет получает объект Свбемнамедвалуе из коллекции.
ms.assetid: ccebe65e-6032-43d5-9004-2247c3b96d6d
ms.tgt_platform: multiple
title: Метод Свбемнамедвалуесет. Item (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemNamedValueSet.Item
- ISWbemNamedValueSet.Item
- ISWbemNamedValueSet.Item
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 688c78aa644b7a5eab3fd6be9ae806ec254a7a50647dc9e87539e96049d6df04
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118992084"
---
# <a name="swbemnamedvaluesetitem-method"></a>Свбемнамедвалуесет. Item, метод

Метод **Item** объекта [**Свбемнамедвалуесет**](swbemnamedvalueset.md) получает объект [**свбемнамедвалуе**](swbemnamedvalue.md) из коллекции.

Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Синтаксис


```VB
objNamedValue = .Item( _
  ByVal strName, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*strName* \[ окне\]
</dt> <dd>

Обязательный. Имя извлекаемого значения.

</dd> <dt>

*ифлагс* \[ в необязательное\]
</dt> <dd>

Зарезервировано. Если указано, это значение должно быть равно нулю.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

В случае успешного выполнения возвращается запрошенный объект [**свбемнамедвалуе**](swbemnamedvalue.md) .

## <a name="error-codes"></a>Коды ошибок

После завершения метода **Item** объект **Err** может содержать один из кодов ошибок из следующего списка.

<dl> <dt>

**вбемеррфаилед** -2147749889 (0x80041001)
</dt> <dd>

Незаданная ошибка.

</dd> <dt>

**вбемерринвалидпараметер** -2147749896 (0x80041008)
</dt> <dd>

Указан недопустимый параметр, или не удалось выполнить синтаксический анализ пространства имен.

</dd> <dt>

**вбемерраутофмемори** -2147749894 (0x80041006)
</dt> <dd>

Недостаточно памяти для завершения операции.

</dd> <dt>

**вбемеррнотфаунд** -2147749890 (0x80041002)
</dt> <dd>

Запрашиваемый элемент не найден.

</dd> </dl>

## <a name="remarks"></a>Remarks

Примеры добавления и получения именованных значений см. в разделе [**свбемнамедвалуе. Value**](swbemnamedvalue-value.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Библиотека типов<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_СВБЕМНАМЕДВАЛУЕСЕТ CLSID<br/>                                                    |
| IID<br/>                      | IID \_ исвбемнамедвалуесет<br/>                                                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**свбемнамедвалуесет**](swbemnamedvalueset.md)
</dt> </dl>

 

 




