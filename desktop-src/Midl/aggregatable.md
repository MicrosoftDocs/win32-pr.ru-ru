---
title: aggregatable - атрибут
description: Атрибут \ агрегированный \ указывает, что класс поддерживает агрегирование.
ms.assetid: 3b680692-fbf7-4aeb-b11a-c3a87ddaea67
keywords:
- статистически обрабатываемый атрибут MIDL
topic_type:
- apiref
api_name:
- aggregatable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5091815cf38060c30b82aa33fd05ad6be9d6c390
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104337084"
---
# <a name="aggregatable-attribute"></a>aggregatable - атрибут

**\[ Статистический \]** атрибут указывает, что класс поддерживает агрегирование.

``` syntax
[
   coclass-attribute-list,
   aggregatable
]
coclass coclass-name
{
   coclass-interface-list
}
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*Список атрибутов coclass* 
</dt> <dd>

Другие атрибуты, которые применяются к классу.

</dd> <dt>

*имя класса* 
</dt> <dd>

Имя класса.

</dd> <dt>

*coclass-интерфейс-список* 
</dt> <dd>

Список интерфейсов для класса.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Используйте **\[ \] статистический** атрибут в операторе [**coclass**](coclass.md) , чтобы пользователи могли понять, что класс поддерживает агрегирование. То есть класс позволяет предоставлять его интерфейсы классом контейнера, как если бы эти интерфейсы были собственными интерфейсами контейнера.

Представление типефлаг для этого атрибута — ТИПЕФЛАГ \_ фаггрегатабле.

## <a name="examples"></a>Примеры

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676),
    aggregatable
]
coclass Form
{
    [default] interface IForm;
    [default, source] interface IFormEvents;
}
```

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**кокласс**](coclass.md)
</dt> <dt>

[Создание библиотеки типов с помощью MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[Пример файла ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Синтаксис файла ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> </dl>

 

 