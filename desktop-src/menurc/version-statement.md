---
title: VERSION, инструкция
description: Определяет сведения о версии ресурса, который может использоваться инструментами, считывающими и записывающими файлы ресурсов.
ms.assetid: 3a33cff3-b8b3-43f4-b43a-ff1d1728cdc1
keywords:
- Меню инструкций версии и другие ресурсы
topic_type:
- apiref
api_name:
- VERSION
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 302ffcee38b287afff2697b9c5a5241fa406b55c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "103784047"
---
# <a name="version-statement"></a>VERSION, инструкция

Определяет сведения о версии ресурса, который может использоваться инструментами, считывающими и записывающими файлы ресурсов. Указанное значение *DWORD* отображается вместе с ресурсом в скомпилированном виде. RES — файл. Однако значение не сохраняется в исполняемом файле и не имеет значимости для системы.

Оператор **Version** появляется перед началом тела определения ресурса [**ускорителей**](accelerators-resource.md), [**диаложекс**](dialogex-resource.md), [**меню**](menu-resource.md), [**RCDATA**](rcdata-resource.md)или [**STRINGTABLE**](stringtable-resource.md) . Указанное значение применяется только к этому ресурсу.

``` syntax
VERSION dword
```

<dl> <dt>

<span id="dword"></span><span id="DWORD"></span>*DWORD*
</dt> <dd>

Определяемое пользователем значение **типа DWORD** .

</dd> </dl>

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Accelerator**](accelerators-resource.md)
</dt> <dt>

[**ПОКАЗАТЕЛИ**](characteristics-statement.md)
</dt> <dt>

[**ЯЗЫКЕ**](language-statement.md)
</dt> <dt>

[**МЕНЮ**](menu-resource.md)
</dt> <dt>

[**RCDATA**](rcdata-resource.md)
</dt> <dt>

[**STRINGTABLE**](stringtable-resource.md)
</dt> </dl>

 

 




