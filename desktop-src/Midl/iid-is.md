---
title: iid_is - атрибут
description: Атрибут \ IID = \_ \ указывает идентификатор IID COM-интерфейса, на который указывает указатель интерфейса.
ms.assetid: 7fb5eb87-15d8-4717-b79a-e8a81f2f7293
keywords:
- iid_is атрибута MIDL
topic_type:
- apiref
api_name:
- iid_is
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74553fdb1e3020d49eca7dfdd219354a4690056c45126b3af208395117ade991
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118383871"
---
# <a name="iid_is-attribute"></a>IID \_ является атрибутом

**\[ IID \_ — это \]** атрибут указателя, указывающий идентификатор IID COM-интерфейса, на который указывает указатель интерфейса.

``` syntax
[ iid_is(limited-expression) ]
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*ограниченное выражение* 
</dt> <dd>

Указывает выражение языка C. Компилятор MIDL поддерживает условные выражения, логические выражения, реляционные выражения и арифметические выражения. MIDL не разрешает вызовы функций в выражениях и не поддерживает операторы инкремента и декремента.

</dd> </dl>

## <a name="remarks"></a>Remarks

**\[ \_ IID \]** можно использовать в списках атрибутов для параметров функции, а также для элементов структуры или объединения. Заглушки используют IID для определения способа маршалирования указателя интерфейса. Это полезно для указателя интерфейса, который типизирован как параметр базового класса.

Файлы, использующие **\[ IID \_ \]** , должны быть скомпилированы с помощью компилятора MIDL в режиме по умолчанию, который не использует параметр [**/ОСФ**](-osf.md) .

## <a name="examples"></a>Примеры

``` syntax
HRESULT    CreateInstance( 
    [in] REFIID riid, 
    [out, iid_is(riid)] IUnknown ** ppvObject);
```

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**объектами**](object.md)
</dt> <dt>

[**uuid**](uuid.md)
</dt> </dl>

 

 




