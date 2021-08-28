---
title: cpp_opt Switch
description: Параметр/КПП \_ OPT указывает параметры для передачи препроцессору C/C++.
ms.assetid: f0059caa-aff3-4e96-95f8-a0014d6a6556
keywords:
- /cpp_opt параметр MIDL
topic_type:
- apiref
api_name:
- /cpp_opt
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c3b7845feb36cd09d96fc64cb7397e4daf001957f6ce7a6f5e797707caafd32
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105655"
---
# <a name="cpp_opt-switch"></a>/КПП \_ Неявное переключение

Параметр **/КПП \_ OPT** указывает параметры для передачи препроцессору C/C++.

``` syntax
midl /cpp_opt "C_preprocessor_option" file.idl
```

## <a name="switch-options"></a>Параметры коммутатора

<dl> <dt>

*\_Параметр препроцессора \_ C* 
</dt> <dd>

Задает параметр командной строки, связанный с вызываемым препроцессором. 

**Примечание**. для препроцессоров Microsoft C/C++ необходимо указать `/E` параметр в виде части строки *\_ \_ параметра препроцессора c* . 

Кавычки требуются, если используется более одного параметра и для пробелов.

</dd> </dl>

## <a name="remarks"></a>Remarks

Не используйте этот параметр, если нет конкретной причины для этого. Дополнительные сведения о предварительной обработке см. [в документации C-требования к препроцессору для MIDL](c-preprocessor-requirements-for-midl.md) .

Параметр **/КПП \_ OPT** можно использовать с параметром [**/КПП \_ cmd**](-cpp-cmd.md) или без него. Дополнительные сведения о создании командной строки препроцессора в любом случае см. в **/КПП \_ cmd** .

Параметр **/КПП \_ OPT** , если он указан, должен всегда включать `/E` в себя для правильной работы.

## <a name="examples"></a>Примеры

**MIDL/КПП \_ cmd d: \\ NT \\ tools \\ ia64 \\cl.exe/дфлаг = true/ИК: \\ Inc filename. idl**

**MIDL/КПП \_ cmd "микпп"/дфлаг = true/ИК: \\ Inc filename. idl**

**MIDL/КПП \_ OPT "/E/дфлаг = true/ИК: \\ Inc" имя_файла. idl**

**MIDL/КПП \_ cmd "CL"/КПП \_ OPT "/e/ДФЛАГ = true/ИК: \\ Inc" имя_файла. idl**

## <a name="see-also"></a>См. также

<dl> <dt>

[**/савепп**](-savepp.md)
</dt> <dt>

[**/КПП \_ cmd**](-cpp-cmd.md)
</dt> <dt>

[Общий синтаксис командной строки MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/но \_ cpp**](-no-cpp-nocpp.md)
</dt> <dt>

[Требования к препроцессору C-препроцессор для MIDL](c-preprocessor-requirements-for-midl.md)
</dt> </dl>

 

 




