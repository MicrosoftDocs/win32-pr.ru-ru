---
title: LANGUAGE, инструкция
description: Определяет язык для всех ресурсов вплоть до инструкции следующего языка или до конца файла.
ms.assetid: 175e27e2-903a-4aaf-89ef-532166b167e8
keywords:
- Меню инструкций языка и другие ресурсы
topic_type:
- apiref
api_name:
- LANGUAGE
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9563ba2ec00362a3b9caa3911a701919a81cae1e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104533167"
---
# <a name="language-statement"></a>LANGUAGE, инструкция

Определяет язык для всех ресурсов вплоть до инструкции следующего **языка** или до конца файла.

Если оператор **Language** появляется перед началом тела определения ресурса [**ускорителей**](accelerators-resource.md), [**диаложекс**](dialogex-resource.md), [**Menu**](menu-resource.md), [**RCDATA**](rcdata-resource.md)или [**STRINGTABLE**](stringtable-resource.md) , указанный язык применяется только к этому ресурсу.

``` syntax
LANGUAGE language, sublanguage
```

<dl> <dt>

<span id="language"></span><span id="LANGUAGE"></span>*языке*
</dt> <dd>

Идентификатор языка.

</dd> <dt>

<span id="sublanguage"></span><span id="SUBLANGUAGE"></span>*вариантом*
</dt> <dd>

Идентификатор языка.

</dd> </dl>

Дополнительные сведения см. в разделе [константы и строки идентификатора языка](/windows/desktop/Intl/language-identifier-constants-and-strings).

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Accelerator**](accelerators-resource.md)
</dt> <dt>

[**ПОКАЗАТЕЛИ**](characteristics-statement.md)
</dt> <dt>

[**МЕНЮ**](menu-resource.md)
</dt> <dt>

[**RCDATA**](rcdata-resource.md)
</dt> <dt>

[**STRINGTABLE**](stringtable-resource.md)
</dt> <dt>

[**Версия**](version-statement.md)
</dt> </dl>

 

 