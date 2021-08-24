---
description: Метод Add объекта Свбемнамедвалуесет добавляет объект Свбемнамедвалуе в коллекцию. Если элемент уже существует в коллекции с тем же именем, новый элемент заменяет его.
ms.assetid: 471b23f5-6c53-40e2-a2a9-0798044c9dfb
ms.tgt_platform: multiple
title: Метод Свбемнамедвалуесет. Add (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemNamedValueSet.Add
- ISWbemNamedValueSet.Add
- ISWbemNamedValueSet.Add
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: a7a911dcfa6371421fd4033524400d0c818e814d3bd52f90b677ac7c9fcf1b60
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119612124"
---
# <a name="swbemnamedvaluesetadd-method"></a>Свбемнамедвалуесет. Add, метод

Метод **Add** объекта [**Свбемнамедвалуесет**](swbemnamedvalueset.md) добавляет объект [**свбемнамедвалуе**](swbemnamedvalue.md) в коллекцию. Если элемент уже существует в коллекции с тем же именем, новый элемент заменяет его.

Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Синтаксис


```VB
objNamedValue = .Add( _
  ByVal strName, _
  ByVal varVal, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*strName* \[ окне\]
</dt> <dd>

Обязательный. Имя нового значения.

</dd> <dt>

*варвал* \[ окне\]
</dt> <dd>

Обязательный. Вариант, представляющий новое значение.

</dd> <dt>

*ифлагс* \[ в необязательное\]
</dt> <dd>

Зарезервированные значения и должны быть равны нулю, если они заданы.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

В случае успешного выполнения этот метод возвращает недавно измененный или вновь созданный объект [**свбемнамедвалуе**](swbemnamedvalue.md) .

## <a name="remarks"></a>Remarks

Примеры добавления и получения именованных значений см. в разделе [**свбемнамедвалуе. Value**](swbemnamedvalue-value.md).

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

 

 




