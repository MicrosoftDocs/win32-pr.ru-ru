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
ms.openlocfilehash: 9504b81ce83a91695765e75e74de374437c188d4
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "103999940"
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

## <a name="remarks"></a>Комментарии

**Коды ошибок** Если у Обновитель нет элемента с указанным индексом, **вбемеррнотфаунд** создается.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Библиотека типов<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_СВБЕМРЕФРЕШЕР CLSID<br/>                                                        |
| IID<br/>                      | IID \_ исвбемрефрешер<br/>                                                         |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**свбемрефрешер**](swbemrefresher.md)
</dt> </dl>

 

 




