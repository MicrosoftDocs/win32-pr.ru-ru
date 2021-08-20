---
description: Метод Свбемрефрешер. Refresh удаляет из Обновитель объект Свбемрефрешаблеитем с указанным индексом.
ms.assetid: db5ac740-e2b3-4667-b511-d750cb092e0f
ms.tgt_platform: multiple
title: Метод Свбемрефрешер. Remove (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefresher.Remove
- ISWbemRefresher.Remove
- ISWbemRefresher.Remove
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 6b262dde1338e05b24ac1c320e684d872e49fc63db48951145b4f4924326e0c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117921662"
---
# <a name="swbemrefresherremove-method"></a>Свбемрефрешер. Remove, метод

Метод **свбемрефрешер. Refresh** удаляет из Обновитель объект [**свбемрефрешаблеитем**](swbemrefreshableitem.md) с указанным индексом. Объект **свбемрефрешаблеитем** может представлять либо один объект, либо набор объектов.

Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Синтаксис


```VB
objRefresher = .Remove( _
  ByVal LIndex, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedvalueSet ] _
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*линдекс* 
</dt> <dd>

Индекс элемента в объекте [**свбемрефрешер**](swbemrefresher.md) .

</dd> <dt>

*ифлагс* \[ используемых\]
</dt> <dd>

Флаги должны быть установлены в T0 (ноль).

</dd> <dt>

*обжвбемнамедвалуесет* \[ используемых\]
</dt> <dd>

NULL.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не имеет возвращаемых значений.

## <a name="remarks"></a>Remarks

**Коды ошибок** Если у Обновитель нет элемента с указанным индексом, **вбемеррнотфаунд** создается.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Заголовок<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Библиотека типов<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_СВБЕМРЕФРЕШЕР CLSID<br/>                                                        |
| IID<br/>                      | IID \_ исвбемрефрешер<br/>                                                         |



## <a name="see-also"></a>См. также

<dl> <dt>

[**свбемрефрешер**](swbemrefresher.md)
</dt> </dl>

 

 




