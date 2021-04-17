---
title: Инкапсулированные объединения
description: Объединение, содержащее его discriminant в структуре в, является инкапсулированным объединением.
ms.assetid: d32c18b4-b2f6-4ce2-94fe-a495a3c15d14
keywords:
- типы данных MIDL, инкапсулированные объединения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4489a043ff3690ddb31a8acccf359dcd76940aa7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105681514"
---
# <a name="encapsulated-unions"></a>Инкапсулированные объединения

Объединение, содержащее его discriminant в структуре в, является инкапсулированным объединением. Инкапсулированное объединение обозначается наличием ключевого слова [**switch**](switch.md) . Этот тип объединения имеет имя, так как компилятор MIDL автоматически инкапсулирует объединение и его discriminant в структуре для передачи во время удаленного вызова процедуры.

Если отсутствует тег Union (тип U1 в приведенном \_ выше примере), компилятор создаст структуру с полем Union с именем *\_ Union с тегами*.

Для обеспечения взаимодействия между платформами все объединения должны быть одинаковыми для разных платформ.

Описание формы инкапсулированного объединения см. в разделе [**Union**](union.md).

## <a name="examples"></a>Примеры

``` syntax
typedef union _S1_TYPE switch (long l1) U1_TYPE 
{ 
    case 1024: 
        float f1; 
    case 2048: 
        double d2; 
} S1_TYPE; 
 
/* in generated header file */ 
typedef struct _S1_TYPE 
{ 
    long l1; 
    union 
    { 
        float f1; 
        double d2; 
    } U1_TYPE; 
} S1_TYPE;
```

Дополнительные сведения см. в разделе [базовые типы MIDL](midl-base-types.md), [**char**](char-idl.md), **\[** [**\_ маркер контекста**](context-handle.md) **\]** , [**перечисление**](enum.md), **\[** [**первый \_ —**](first-is.md) **\]** , **\[** [**Handle**](handle.md) **\]** , **\[** [**Ignore**](ignore.md) **\]** , [**int**](int.md), **\[** [**игнорировать**](ignore.md) **\]** , **\[** [**Last \_ —**](last-is.md) **\]** , **\[** [**length \_ —**](length-is.md) **\]** , **\[** [**Max \_ —**](max-is.md) **\]** , **\[** [**MS \_ Union**](ms-union-attrib.md) **\]** , [неинкапсулированные объединения](nonencapsulated-unions.md), **\[** [**ptr**](ptr.md) **\]** , **\[** [**ref**](ref.md) **\]** , **\[** [**размер \_ —**](size-is.md) **\]** , **\[** [**строка**](string.md) **\]** , [**Структура**](struct.md), [**переключатель**](switch.md), **\[** [**параметр \_ —**](switch-is.md) **\]** , **\[** [**\_ тип коммутатора**](switch-type.md), " **\]** **\[** [**передать \_ как**](transmit-as.md) **\]** [](union.md) **\[** [](unique.md) ", "объединить" и "уникальный"**\]**

 

 




