---
title: параметр/align
description: Ключ/align функционально аналогичен параметру MIDL/ZP и распознается компилятором MIDL исключительно для обеспечения обратной совместимости с MkTypLib.
ms.assetid: 7f303c49-a6b5-4e3c-95e5-5c49e338c766
keywords:
- параметр/align MIDL
topic_type:
- apiref
api_name:
- /align
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 187607b783678d3045224daec021eabf436fa8ba1884128789f44b06ac4365ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067654"
---
# <a name="align-switch"></a>параметр/align

Ключ **/align** функционально аналогичен параметру MIDL [**/Zp**](-zp.md) и распознается компилятором MIDL исключительно для обеспечения обратной совместимости с MkTypLib.

> [!Note]  
> Средство Mktyplib.exe устарело. Вместо этого используйте компилятор MIDL.

 

``` syntax
midl /align:alignment
```

## <a name="switch-options"></a>Параметры коммутатора

<dl> <dt>

*Выравнивание* 
</dt> <dd>

Задает выравнивание для типов в библиотеке. Значение *выравнивания* может быть равно 1, 2, 4 или 8. Значение 1 указывает на естественное выравнивание; *n* обозначает выравнивание по байту *n*. Если параметр **/align** не задан, по умолчанию используется значение 8.

</dd> </dl>

## <a name="remarks"></a>Remarks

При создании нового файла makefile используйте параметр [**/Zp**](-zp.md) .

Значение выравнивания соответствует значению параметра [**/Zp**](-zp.md) , используемому компилятором Microsoft C/C++. Обязательно укажите одинаковое выравнивание при вызове компилятора C, как при вызове компилятора MIDL.

Дополнительные сведения см. в документации по программированию для Microsoft C/C++. Обсуждение потенциальных опасностей при использовании нестандартных уровней упаковки см. в разделе справки [**/Zp**](-zp.md) .

## <a name="examples"></a>Примеры

**MIDL/align: 4 filename. idl**

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Общий синтаксис командной строки MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/ZP**](-zp.md)
</dt> </dl>

 

 




