---
title: атрибут force_allocate
description: Атрибут ACF \ принудительное \_ выделение \ принудительное выделение параметра указателя с помощью \_ пользовательского выделения MIDL \_ вместо оптимизации выделения.
ms.assetid: 40e3a7d9-7e4f-4e3d-8c82-fb6ef567f293
keywords:
- force_allocate атрибута MIDL
topic_type:
- apiref
api_name:
- force_allocate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f73d0386d786e4d3004c78b1acccda7e9be8fc16
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104487584"
---
# <a name="force_allocate-attribute"></a>принудительное \_ выделение атрибута

При принудительном выделении атрибут ACF принудительно выделяется \[ **\_** \] параметр указателя с помощью функции [**\_ \_ выделения пользователя MIDL**](midl-user-allocate-1.md) вместо оптимизации выделения.

``` syntax
[ [function-attribute-list <>] ] type-specifier <> [pointer- <>declarator <>] function-name <>( [ force_allocate [ , parameter-attribute-list <> ] ] type-specifier <> [declarator <>] , ...);
```

## <a name="parameters"></a>Параметры

Этот атрибут не имеет параметров.

## <a name="remarks"></a>Комментарии

RPC пытается сокращать выделение памяти на сервере, указывая указатели на внутренние буферы памяти. Такой подход может вызвать проблемы в приложениях, которые пытаются напрямую вызвать непосредственный [**\_ пользователь \_ MIDL**](midl-user-free-1.md) для указателей, предоставленных RPC, так как не удается освободить указатель, который был оптимизирован. Пометка параметра **\[ принудительным \_ выделением \]** позволит предотвратить эту оптимизацию для всех указателей, производных от него.

Другим распространенным применением **\[ принудительного \_ выделения \]** является обеспечение выравнивания памяти, на которую указывает, если приложению требуется выравнивание, превышающее размер памяти, на которую указывает. Например, приложения часто передают данные в универсальном массиве байтов вместо фактического типа, но байт гарантированно выравнивается только по 1, что может вызвать проблемы для приложений, которые предполагают более крупное выравнивание. Пометив параметр **\[ принудительным \_ выделением \]**, приложение может гарантировать, что вся память, на которую указывает, будет иметь выравнивание, равное значению, гарантированному [**\_ \_ выделять пользователем MIDL**](midl-user-allocate-1.md).

## <a name="examples"></a>Примеры

``` syntax
/* IDL file */
void Func1([in, out, string] char **ppstr);
void Func2([in] long s, [in, size_is(s)] byte *pData);

/* ACF file */

/* e.g. The application wishes to call midl_user_free on *ppstr and supply a new pointer */
Func1([force_allocate] pstr);

/* e.g. pData really points to a structure that needs an alignment greater than 1 */
Func2([force_allocate] pData);
```

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Предотвращение скрытия информации](/windows/desktop/WinProg64/avoiding-information-hiding)
</dt> <dt>

[Проектирование интерфейсов, совместимых с 64-bit](/windows/desktop/WinProg64/designing-64-bit-compatible-interfaces)
</dt> <dt>

[**\_пользовательское \_ выделение MIDL**](midl-user-allocate-1.md)
</dt> <dt>

[**\_бесплатный пользователь \_ MIDL**](midl-user-free-1.md)
</dt> <dt>

[**allocate**](allocate.md)
</dt> </dl>

 

 