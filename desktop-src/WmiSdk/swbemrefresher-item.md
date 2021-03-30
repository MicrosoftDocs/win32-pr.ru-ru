---
description: Метод Свбемрефрешер. Item возвращает указанный Свбемрефрешаблеитем из коллекции. Свбемрефрешаблеитем из коллекции.
ms.assetid: 8ae3dea5-0582-422e-9cd8-b6d91b41588a
ms.tgt_platform: multiple
title: Метод Свбемрефрешер. Item (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefresher.Item
- ISWbemRefresher.Item
- ISWbemRefresher.Item
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: cfdbb592e6358fb1f8c5f3d45bb7e6bb780641c3
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "104273254"
---
# <a name="swbemrefresheritem-method"></a>Свбемрефрешер. Item, метод

Метод **свбемрефрешер. Item** Возвращает указанный [**свбемрефрешаблеитем**](swbemrefreshableitem.md) из коллекции.

Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Синтаксис


```VB
objItem = .Item( _
  ByVal lIndex _
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*линдекс* 
</dt> <dd>

Значение индекса элемента в коллекции.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если вызов выполнен успешно, возвращается указанный объект [**свбемрефрешаблеитем**](swbemrefreshableitem.md) .

## <a name="error-codes"></a>Коды ошибок

Если у Обновитель нет элемента с указанным индексом, **вбемеррнотфаунд** создается.

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

 

 




