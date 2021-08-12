---
title: Ерроритем. Кустомурл
description: Свойство Кустомурл извлекает URL-адрес сайта, который отображает конкретные сведения об ошибке загрузки кодека.
ms.assetid: 51028f45-2ce6-4e57-86bd-d7c2d8fb3af8
keywords:
- ерроритем. кустомурл проигрыватель Windows Media
topic_type:
- apiref
api_name:
- ErrorItem.customUrl
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: acccf086fc9b620243667aadac50ec2f727ab6951b2770cd2c8b21d5ea41b683
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118577840"
---
# <a name="erroritemcustomurl"></a>Ерроритем. Кустомурл

Свойство **кустомурл** извлекает URL-адрес сайта, который отображает конкретные сведения об ошибке загрузки кодека.

``` syntax
player.error.item(
        index
        ).customURL
      
```

## <a name="possible-values"></a>Возможные значения

Это свойство является **строкой**, доступная только для чтения.

## <a name="remarks"></a>Remarks

**проигрыватель Windows Media 10 Mobile:** Это свойство всегда возвращает пустую строку.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | проигрыватель Windows Media версии 7,0 или более поздней.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Объект Ерроритем**](erroritem-object.md)
</dt> </dl>

 

 





