---
title: pointer_default - атрибут
description: Атрибут \ указатель \_ по умолчанию \ задает атрибут указателя по умолчанию для всех указателей, за исключением указателей верхнего уровня, которые отображаются в списках параметров.
ms.assetid: a6e83034-8adb-483d-8d1e-432a1aed22c6
keywords:
- pointer_default атрибута MIDL
topic_type:
- apiref
api_name:
- pointer_default
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08555358eb0abd42957d60527e18a4fd4f49165a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104069858"
---
# <a name="pointer_default-attribute"></a>\_атрибут указателя по умолчанию

Атрибут **\[ указателя \_ по \] умолчанию** задает атрибут указателя по умолчанию для всех указателей, за исключением указателей верхнего уровня, которые отображаются в списках параметров.

``` syntax
pointer_default ( ptr | ref | unique )
```

## <a name="parameters"></a>Параметры

Этот атрибут не имеет параметров.

## <a name="examples"></a>Примеры

``` syntax
[
    uuid(6B29FC40-CA47-1067-B31D-00DD010662DA), 
    version(3.3), 
    pointer_default(unique)
] 
interface dictionary 
{
    // Interface definition statements.
}
```

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**взаимодействия**](interface.md)
</dt> <dt>

[Атрибуты массива и Sized-Pointer](array-and-sized-pointer-attributes.md)
</dt> <dt>

[**массивы**](arrays-1.md)
</dt> <dt>

[Массивы и указатели](/windows/desktop/Rpc/arrays-and-pointers)
</dt> <dt>

[**ptr**](ptr.md)
</dt> <dt>

[**ref**](ref.md)
</dt> <dt>

[**однозначно**](unique.md)
</dt> <dt>

[Типы указателей по умолчанию](/windows/desktop/Rpc/default-pointer-types)
</dt> </dl>

 

 