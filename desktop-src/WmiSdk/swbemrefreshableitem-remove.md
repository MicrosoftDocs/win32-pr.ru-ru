---
description: Метод Свбемрефрешаблеитем. Remove удаляет объект Свбемрефрешаблеитем из родительского объекта Свбемрефрешер. Объект Свбемрефрешаблеитем из родительского объекта Свбемрефрешер.
ms.assetid: 8d3f5e22-c343-4191-a20a-6bca2ec9b01a
ms.tgt_platform: multiple
title: Метод Свбемрефрешаблеитем. Remove (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefreshableItem.Remove
- ISWbemRefreshableItem.Remove
- ISWbemRefreshableItem.Remove
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 028bff202108481ce498be02c6014141313f27cc
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105693840"
---
# <a name="swbemrefreshableitemremove-method"></a>Свбемрефрешаблеитем. Remove, метод

Метод **свбемрефрешаблеитем. Remove** удаляет объект [**свбемрефрешаблеитем**](swbemrefreshableitem.md) из родительского объекта [**свбемрефрешер**](swbemrefresher.md) .

Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Синтаксис


```VB
SWbemRefreshableItem.Remove( _
  [ ByVal lFlags ] _
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*лфлагс* \[ в необязательное\]
</dt> <dd>

Этот параметр должен иметь значение 0 (ноль).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

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
| CLSID<br/>                    | \_СВБЕМРЕФРЕШАБЛЕИТЕМ CLSID<br/>                                                  |
| IID<br/>                      | IID \_ исвбемрефрешаблеитем<br/>                                                   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**свбемрефрешаблеитем**](swbemrefreshableitem.md)
</dt> <dt>

[**свбемрефрешер**](swbemrefresher.md)
</dt> </dl>

 

 




