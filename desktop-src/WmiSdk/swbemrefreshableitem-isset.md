---
description: Свойство Свбемрефрешаблеитем. Иссет является логическим значением, указывающим, представляет ли объект Свбемрефрешаблеитем один объект или набор объектов. Объект Свбемрефрешаблеитем представляет отдельный объект или набор объектов.
ms.assetid: 4be5d27c-9020-4150-84ce-f9efc55be947
ms.tgt_platform: multiple
title: Свойство Свбемрефрешаблеитем. Иссет (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefreshableItem.IsSet
- ISWbemRefreshableItem.IsSet
- ISWbemRefreshableItem.get_IsSet
- ISWbemRefreshableItem.put_IsSet
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 055c776c1beffe1550033d61b54256d7b2e983ca70ac13f1b9fc899920910d4c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118312923"
---
# <a name="swbemrefreshableitemisset-property"></a>Свбемрефрешаблеитем. Иссет, свойство

Свойство **свбемрефрешаблеитем. Иссет** является логическим значением, указывающим, представляет ли объект [**свбемрефрешаблеитем**](swbemrefreshableitem.md) один объект или набор объектов.

Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```VB
SWbemRefreshableItem.IsSet As Boolean
```



## <a name="property-value"></a>Значение свойства

## <a name="remarks"></a>Remarks

Если **свбемрефрешаблеитем. Иссет** имеет **значение true**, то элемент представляет объект [**SWbemObjectSet**](swbemobjectset.md) , а свойство [**объекта**](swbemrefreshableitem-object.md) будет иметь **значение NULL**. Если **значение равно false**, элемент представляет объект [**SWbemObject**](swbemobject.md) , а свойство **объекта** имеет **значение NULL**.

## <a name="requirements"></a>Requirements (Требования)



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

[**свбемрефрешаблеитем**](swbemrefresher.md)
</dt> </dl>

 

 




