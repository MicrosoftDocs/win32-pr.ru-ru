---
description: Метод Clone объекта Свбемнамедвалуесет возвращает новый объект, который является клоном текущей коллекции.
ms.assetid: 0e7fab2e-8175-45e5-aa70-1109502e2b3f
ms.tgt_platform: multiple
title: Метод Свбемнамедвалуесет. Clone (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemNamedValueSet.Clone
- ISWbemNamedValueSet.Clone
- ISWbemNamedValueSet.Clone
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 17678d36a553c84c008f606c647d7ff1fa9dfadc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103814321"
---
# <a name="swbemnamedvaluesetclone-method"></a>Свбемнамедвалуесет. Clone, метод

Метод **clone** объекта [**свбемнамедвалуесет**](swbemnamedvalueset.md) возвращает новый объект, который является клоном текущей коллекции.

Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Синтаксис


```VB
objwbemNamedValueSet = .Clone( _
)
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

В случае успешного выполнения новый объект [**свбемнамедвалуесет**](swbemnamedvalueset.md) возвращает значение.

## <a name="error-codes"></a>Коды ошибок

После завершения метода **clone** объект **Err** может содержать один из кодов ошибок, приведенных ниже.

<dl> <dt>

**вбемеррфаилед** -2147749889 (0x80041001)
</dt> <dd>

Незаданная ошибка.

</dd> <dt>

**вбемерраутофмемори** -2147749894 (0x80041006)
</dt> <dd>

Недостаточно памяти для клонирования объекта.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Используйте этот метод для дублирования коллекции [**свбемнамедвалуесет**](swbemnamedvalueset.md) .

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

 

 




