---
title: /LCID, параметр
description: Параметр компилятора/LCID MIDL позволяет использовать международные символы во входных файлах, именах файлов и путях к каталогам.
ms.assetid: 2ab4ba67-4414-4889-8ed7-83f4888caf8b
keywords:
- MIDL/LCID Switch
topic_type:
- apiref
api_name:
- /lcid
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5ceff1f9a4ef2f6c95a8dac12ff689995efe4fdd3619cf48e11043967fec053
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118385517"
---
# <a name="lcid-switch"></a>/LCID, параметр

Параметр компилятора **/LCID** MIDL позволяет использовать международные символы во входных файлах, именах файлов и путях к каталогам.

``` syntax
midl /lcid localeID
```

## <a name="switch-options"></a>Параметры коммутатора

<dl> <dt>

*localeID* 
</dt> <dd>

указывает 32-разрядный идентификатор локали, используемый в Windows поддержки национальных языков. Код локали должен быть указан в десятичном формате.

</dd> </dl>

## <a name="remarks"></a>Remarks

Во входных файлах можно использовать локализованные комментарии, строки, хелпстрингс и идентификаторы. В частности, параметр **/LCID** обеспечивает полную поддержку DBCS для представления азиатских языков, таких как японский, китайский и корейский.

> [!Note]  
> Параметр **/LCID** доступен в MIDL версии 3.01.75 и более поздних.

 

## <a name="examples"></a>Примеры

**MIDL/LCID 1041 iface. idl**

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Общий синтаксис командной строки MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**намного**](lcid.md)
</dt> </dl>

 

 




