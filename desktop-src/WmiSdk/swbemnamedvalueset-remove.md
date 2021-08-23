---
description: Метод Remove объекта Свбемнамедвалуесет удаляет именованное значение из контекста.
ms.assetid: 8cb353fb-c6d7-41d9-a2d0-ff1ad37264e4
ms.tgt_platform: multiple
title: Метод Свбемнамедвалуесет. Remove (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemNamedValueSet.Remove
- ISWbemNamedValueSet.Remove
- ISWbemNamedValueSet.Remove
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 1c733f932588c5c0d7ccfe3c906f28244d37fee0c649451c05fb8f72742edef4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119611924"
---
# <a name="swbemnamedvaluesetremove-method"></a>Свбемнамедвалуесет. Remove, метод

Метод **Remove** объекта [**свбемнамедвалуесет**](swbemnamedvalueset.md) удаляет именованное значение из контекста.

Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Синтаксис


```VB
SWbemNamedValueSet.Remove( _
  ByVal strName, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*strName* \[ окне\]
</dt> <dd>

Обязательный. Имя удаляемого значения.

</dd> <dt>

*ифлагс* \[ в необязательное\]
</dt> <dd>

Зарезервировано. Если указано, это значение должно быть равно нулю.

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

**вбемерринвалидпараметер** -2147749896 (0x80041008)
</dt> <dd>

Указан недопустимый параметр, или не удалось выполнить синтаксический анализ пространства имен.

</dd> <dt>

**вбемеррнотфаунд** -2147749890 (0x80041002)
</dt> <dd>

Запрашиваемый элемент не найден.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Заголовок<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Библиотека типов<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_СВБЕМНАМЕДВАЛУЕСЕТ CLSID<br/>                                                    |
| IID<br/>                      | IID \_ исвбемнамедвалуесет<br/>                                                     |



## <a name="see-also"></a>См. также

<dl> <dt>

[**свбемнамедвалуесет**](swbemnamedvalueset.md)
</dt> </dl>

 

 




