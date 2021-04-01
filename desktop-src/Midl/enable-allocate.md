---
title: атрибут enable_allocate
description: Атрибут \ Enable \_ allocate \ ACF указывает, что код заглушки сервера должен включать среду управления памятью заглушки.
ms.assetid: 3a232a82-f114-4d8c-8b71-cf8860c77db3
keywords:
- enable_allocate атрибута MIDL
topic_type:
- apiref
api_name:
- enable_allocate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f43e8c10592fcf99ea294327c400c579ce45bf6b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104133739"
---
# <a name="enable_allocate-attribute"></a>включить \_ атрибут выделения

Атрибут **\[ включить \_ выделение \]** ACF указывает, что код заглушки сервера должен включать среду управления памятью заглушки.

> [!Note]  
> Атрибут **\[ включения \_ выделения \]** устарел и больше не поддерживается.

 

``` syntax
[
    enable_allocate
  [ , optional-attribute-list]
]
interface interface-name
{
    . . .
};
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*список необязательных атрибутов* 
</dt> <dd>

Задает список из нуля или нескольких дополнительных атрибутов MIDL.

</dd> <dt>

*имя интерфейса* 
</dt> <dd>

Имя интерфейса, к которому будет применен атрибут **\[ Enable \_ аллкоате \]** .

</dd> </dl>

## <a name="remarks"></a>Комментарии

В режиме по умолчанию заглушка сервера включает среду памяти, только если используется атрибут **\[ включения \_ выделения \]** . Для выделения памяти с помощью [**рпксмаллокате**](/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmallocate)необходимо включить среду управления памятью. В режиме **Использование** (при компиляции с использованием параметра [**/ОСФ**](-osf.md) ) заглушка включает эту среду автоматически или по запросу, когда используется атрибут **\[ включения \_ выделения \]** .

Заглушка на стороне клиента может быть чувствительна к среде управления памятью **RPCSS** . Если конфиденциальная клиентская заглушка выполняется при отключенном пакете **RPCSS** , вызывается распределитель и освобождение пользователей по умолчанию (например, [MIDL, \_ \_ выделяющий](/windows/desktop/Rpc/the-midl-user-allocate-function)пользователя /  [MIDL, \_ \_ свободно](/windows/desktop/Rpc/the-midl-user-free-function)). Если этот параметр включен, пакет **RPCSS** использует пару распределителя и дераспределения из пакета. В режиме по умолчанию клиент учитывается только в том случае, если используется атрибут **\[ включения \_ выделения \]** . Как правило, заглушка на стороне клиента работает в отключенной среде. В режиме **Использование** (при компиляции с использованием параметра [**/ОСФ**](-osf.md) ) клиент всегда чувствителен к среде управления памятью **RPCSS** и, следовательно, атрибут **\[ включения \_ выделения \]** не влияет на заглушки клиента.

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Файл конфигурации приложения (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[\_пользовательское \_ выделение MIDL](/windows/desktop/Rpc/the-midl-user-allocate-function)
</dt> <dt>

[\_бесплатный пользователь \_ MIDL](/windows/desktop/Rpc/the-midl-user-free-function)
</dt> <dt>

[**/осф**](-osf.md)
</dt> <dt>

[рпксмдисаблеаллокате](/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmdisableallocate)
</dt> <dt>

[рпксменаблеаллокате](/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmenableallocate)
</dt> <dt>

[рпксмфри](/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmfree)
</dt> </dl>

 

 