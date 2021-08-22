---
title: атрибут хелпстрингдлл
description: Атрибут \ хелпстрингдлл \ задает имя библиотеки DLL, используемой для поиска строки документа.
ms.assetid: 1b9b962c-c355-4428-b5ea-dc7fd48b50a9
keywords:
- атрибут хелпстрингдлл MIDL
topic_type:
- apiref
api_name:
- helpstringdll
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f773ed18e72f184305275ce238ddf0576c81447181a0b7fb420c30341935f5e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067254"
---
# <a name="helpstringdll-attribute"></a>атрибут хелпстрингдлл

Атрибут **\[ хелпстрингдлл \]** задает имя библиотеки DLL, используемой для поиска строки документа.

``` syntax
[
    helpstringdll(help-text-string)
    [, optional-attribute-list]
] 
library library-name
{ 
    library-definition-statements
};
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*Справка-текстовая строка* 
</dt> <dd>

Строка символов с нулевым нулем, указывающая полное имя файла DLL.

</dd> <dt>

*список необязательных атрибутов* 
</dt> <dd>

Другие атрибуты, применяемые к оператору Library в целом.

</dd> <dt>

*имя библиотеки* 
</dt> <dd>

Идентификатор, который программные компоненты будут использовать для обозначения этой [**библиотеки**](library.md).

</dd> <dt>

*Library-операторы определения* 
</dt> <dd>

Одна или несколько инструкций MIDL, которые определяют интерфейс [**библиотеки**](library.md).

</dd> </dl>

## <a name="remarks"></a>Remarks

Используйте атрибут **\[ хелпстрингдлл \]** в операторе Library, чтобы указать в виде символьной строки полное имя файла библиотеки динамической компоновки. Это позволяет пользователю просматривать описание библиотеки DLL с помощью средства просмотра объектов.

Используйте функции **GetDocumentation2** в интерфейсах **ITypeLib2** и **ITypeInfo2** , чтобы получить строку справки.

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Библиотечная**](library.md)
</dt> <dt>

[Синтаксис файла ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Пример файла ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Создание библиотеки типов с помощью MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 