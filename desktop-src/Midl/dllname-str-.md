---
title: атрибут dllname (STR)
description: Атрибут \ dllname \ определяет имя библиотеки DLL, содержащей точки входа для модуля.
ms.assetid: dbf062ce-9dcc-4cc6-b7cd-cdc5945e399b
keywords:
- атрибут dllname (STR) MIDL
topic_type:
- apiref
api_name:
- dllname(str)
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7db6f70fb65822a63bd2bf0f9919ac1b9554a664d1ac7ec9775c611b5b4e7f73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067294"
---
# <a name="dllnamestr-attribute"></a>атрибут dllname (STR)

Атрибут **\[ dllname \]** определяет имя библиотеки DLL, содержащей точки входа для модуля.

``` syntax
[
    uuid(uuid-number), 
    dllname("filename")
    [, optional-attribute-list]
]
module modulename
{
    elementlist
};
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*UUID — номер* 
</dt> <dd>

Задает универсальный уникальный идентификационный номер для [**модуля**](module.md).

</dd> <dt>

*filename* 
</dt> <dd>

Указывает строку, завершающуюся НУЛЕМ, которая содержит полный путь к DLL-файлу.

</dd> <dt>

*список необязательных атрибутов* 
</dt> <dd>

Указывает список атрибутов интерфейса MIDL, отданных от нуля или более.

</dd> <dt>

*ModuleName* 
</dt> <dd>

Указывает имя, которое другие программные компоненты могут использовать для ссылки на модуль.

</dd> <dt>

*елементлист* 
</dt> <dd>

Указывает одну или несколько инструкций определения элемента модуля.

</dd> </dl>

## <a name="remarks"></a>Remarks

Атрибут **\[ dllname \]** является обязательным для модуля.

## <a name="examples"></a>Примеры

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676),
    helpstring("A meaningful comment"),   
    dllname("HANDY.DLL")
] 
module HandyStuff
{
    /* Module content definitions */
};
```

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**модуль**](module.md)
</dt> <dt>

[**операции**](entry.md)
</dt> <dt>

[Синтаксис файла ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Пример файла ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Создание библиотеки типов с помощью MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 