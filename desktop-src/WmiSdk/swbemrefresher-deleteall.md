---
description: Метод Свбемрефрешер. DeleteAll удаляет все элементы из коллекции в объекте Свбемрефрешер. Объект Свбемрефрешер.
ms.assetid: c6e462d3-52b3-40c0-9a9c-fa268415a5f0
ms.tgt_platform: multiple
title: Свбемрефрешер. DeleteAll, метод (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefresher.DeleteAll
- ISWbemRefresher.DeleteAll
- ISWbemRefresher.DeleteAll
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: ddeb1c5fc8e7fb1f9c5682a2da0d9a1d6f53ba5d
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105703461"
---
# <a name="swbemrefresherdeleteall-method"></a>Свбемрефрешер. DeleteAll, метод

Метод **свбемрефрешер. DeleteAll** удаляет все элементы из коллекции в объекте [**свбемрефрешер**](swbemrefresher.md) .

Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Синтаксис


```VB
SWbemRefresher.DeleteAll()
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Комментарии

В соответствующем [**свбемрефрешаблеитем**](swbemrefreshableitem.md) для каждого удаленного элемента свойство [**Обновитель**](swbemrefreshableitem-refresher.md) имеет значение **null**, которое указывает, что у него больше нет родительского обновления.

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

 

 




