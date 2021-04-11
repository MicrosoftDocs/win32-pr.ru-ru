---
title: /Pack, параметр
description: Параметр/Pack совпадает с вариантом/Zp.
ms.assetid: 381e3099-adb4-4219-bbb4-89c9e1dd3928
keywords:
- MIDL/Pack Switch
topic_type:
- apiref
api_name:
- /pack
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c807846148d81e0e59620046d9f24380fe647c11
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104069120"
---
# <a name="pack-switch"></a>/Pack, параметр

Параметр **/Pack** совпадает с вариантом [**/Zp**](-zp.md) .

``` syntax
midl /pack packing_level
```

## <a name="switch-options"></a>Параметры коммутатора

<dl> <dt>

*\_уровень упаковки* 
</dt> <dd>

Задает уровень упаковки для структур в целевой системе. Значение уровня упаковки может быть равно 1, 2, 4 или 8.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Параметр **/Pack** обозначает уровень упаковки для структур в целевой системе. Значение уровня упаковки соответствует значению параметра [**/Zp**](-zp.md) , используемому компилятором Microsoft C/C++ версии 7,0. Дополнительные сведения см. в документации по программированию для Microsoft C/C++.

Укажите тот же уровень упаковки при вызове компилятора MIDL и компилятора C. Уровень упаковки по умолчанию, используемый, если ни параметр [**/Zp**](-zp.md) , ни **/Pack** не задан как 8 в обеих средах сборки.

Обсуждение потенциальных опасностей при использовании нестандартных уровней упаковки см. в разделе справки [**/Zp**](-zp.md) .

## <a name="examples"></a>Примеры

**MIDL/Pack 2 filename. idl**

**MIDL/Pack 8 bar. idl**

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Общий синтаксис командной строки MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/env**](-env.md)
</dt> <dt>

[**/ZP**](-zp.md)
</dt> </dl>

 

 




