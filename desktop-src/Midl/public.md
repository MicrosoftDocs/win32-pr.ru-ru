---
title: public - атрибут
description: Атрибут \ Public \ включает псевдоним, объявленный с ключевым словом typedef в библиотеке типов.
ms.assetid: d4e90165-8b0d-47bb-998d-e515226be935
keywords:
- Открытый атрибут MIDL
topic_type:
- apiref
api_name:
- public
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8451ddf77b5074dbea609bfed144340dc877c00
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "105650329"
---
# <a name="public-attribute"></a>public - атрибут

**\[ Открытый \]** атрибут включает псевдоним, объявленный с ключевым словом [**typedef**](typedef.md) в библиотеке типов.

``` syntax
typedef [public] data-type identifier;
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*тип данных* 
</dt> <dd>

Тип данных, для которого идентификатор будет псевдонимом.

</dd> <dt>

*identifier* 
</dt> <dd>

Другое имя, по которому *тип данных* будет известен в программном обеспечении.

</dd> </dl>

## <a name="remarks"></a>Комментарии

По умолчанию псевдоним, объявленный с [**typedef**](typedef.md) и не имеющий других атрибутов, рассматривается как **\# Определение** и не включается в библиотеку типов. Использование атрибута **\[ Public \]** гарантирует, что псевдоним станет частью библиотеки типов.

> [!Note]  
> Компилятор MIDL требует явного применения атрибута **\[ Public \]** к каждому определению typedef, которое требуется сделать открытым.

 

## <a name="examples"></a>Примеры

``` syntax
typedef [public] long MEMBERID;
```

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Создание библиотеки типов с помощью MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[Пример файла ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[**взаимодействия**](interface.md)
</dt> <dt>

[Синтаксис файла ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**определение**](typedef.md)
</dt> </dl>

 

 