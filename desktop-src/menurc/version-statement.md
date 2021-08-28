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
ms.openlocfilehash: 2c95f2af63d5c7bdb499d371892d0c2fa6ddb875fda5daf5b19fd0d188a478fa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119776664"
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

## <a name="see-also"></a>См. также

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

 

 




