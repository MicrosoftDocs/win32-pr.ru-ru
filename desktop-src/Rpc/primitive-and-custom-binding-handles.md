---
title: Простые и пользовательские дескрипторы привязки
description: Все дескрипторы, объявленные с \_ \_ типами дескрипторов привязки t или RPC \_ , являются примитивными дескрипторами привязки.
ms.assetid: 7a948aad-02fa-421d-b32c-f5dab071bd04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d496a9a54ba0ee7b9552326f7c4dc15792a72bce
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070505"
---
# <a name="primitive-and-custom-binding-handles"></a>Простые и пользовательские дескрипторы привязки

Все дескрипторы, объявленные с типами [**\_ \_ дескрипторов привязки**](rpc-binding-handle.md) [ \_ t](/windows/desktop/Midl/handle-t) или RPC, являются примитивными дескрипторами привязки. Можно расширить типы [**\_ \_ обработчиков привязки**](rpc-binding-handle.md) [ \_ t](/windows/desktop/Midl/handle-t) или RPC, чтобы они включали больше или больше информации, чем содержит тип простого обработчика. При этом создается пользовательский маркер привязки.

Чтобы сделать пользовательский маркер привязки для распределенного приложения, необходимо создать собственный тип данных и указать \[ атрибут [Handle](/windows/desktop/Midl/handle) в \] определении типа в IDL-файле. В конечном итоге, файлы заглушки сопоставляют пользовательские дескрипторы привязки с примитивными дескрипторами.

При создании собственного типа маркера привязки необходимо также предоставить подпрограммы BIND и Unbind, используемые клиентской заглушкой для отображения пользовательского маркера в виде примитивного маркера. Заглушка вызывает процедуры привязки и отмены привязки в начале и в конце каждого удаленного вызова процедуры. Подпрограммы BIND и Unbind должны соответствовать следующим прототипам функций.



| Прототип функции                     | Описание       |
|----------------------------------------|-------------------|
| Handle \_ -тип \_ привязки (*тип*)           | Подпрограммы привязки   |
| Unbind типа void \_ (*тип*, *Handle \_ t*) | Выполняется отмена привязки |



 

В следующем примере показано, как можно определить пользовательский маркер привязки в IDL-файле:

``` syntax
/* usrdef.idl */
[
  uuid(20B309B1-015C-101A-B308-02608C4C9B53),
  version(1.0),
  pointer_default(unique)
]
interface usrdef
{
  typedef struct _DATA_TYPE 
  {
      unsigned char * pszUuid;
      unsigned char * pszProtocolSequence;
      unsigned char * pszNetworkAddress;
      unsigned char * pszEndpoint;
      unsigned char * pszOptions;
  } DATA_TYPE;
 
  typedef [handle] DATA_TYPE * DATA_HANDLE_TYPE;
  void UsrdefProc([in] DATA_HANDLE_TYPE  hBinding,
                  [in, string] unsigned char *   pszString);
 
  void Shutdown([in] DATA_HANDLE_TYPE hBinding);
}
```

Если подпрограммы привязки обнаруживают ошибку, она должна вызвать исключение с помощью функции [**рпкраисиксцептион**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcraiseexception) . Клиентская заглушка будет очищена и позволить фильтру исключений в блок исключений, окружающий удаленный вызов процедур на стороне клиента. Если подпрограмма привязки просто возвращает **значение NULL**, клиентский код получает ошибку \_ " \_ Недопустимая привязка RPC S" \_ . Хотя это и может быть приемлемым в некоторых ситуациях, другие ситуации (например, не хватает памяти) не реагируют. Подпрограммы Unbind должны быть спроектированы так, чтобы не завершаться сбоем. Подпрограммы Unbind не должны вызывать исключения.

В клиентском приложении отображаются подпрограммы привязки и отмены привязки, определяемые программистом. В следующем примере подпрограммы привязки вызывают [**рпкбиндингфромстрингбиндинг**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) , чтобы преобразовать сведения о привязке строк в маркер привязки. Подпрограммы Unbind вызывают [**рпкбиндингфри**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfree) , чтобы освободить маркер привязки.

Имя определяемого программистом маркера привязки ( \_ тип маркера данных \_ ) отображается как часть имени функции. Он также используется в качестве типа параметра в параметрах функции.

``` syntax
/* The client stub calls this _bind routine at the */
/* beginning of each remote procedure call                */
 
RPC_BINDING_HANDLE __RPC_USER DATA_HANDLE_TYPE_bind(
    DATA_HANDLE_TYPE dh1)
{
    RPC_BINDING_HANDLE hBinding;
    RPC_STATUS status;
 
    unsigned char *pszStringBinding;
 
    status = RpcStringBindingCompose(
          dh1.pszUuid,
          dh1.pszProtocolSequence,
          dh1.pszNetworkAddress,
          dh1.pszEndpoint,
          dh1.pszOptions,
          &pszStringBinding);
          ...
 
    status = RpcBindingFromStringBinding(
          pszStringBinding,
          &hBinding);
          ...
 
    status = RpcStringFree(&pszStringBinding); 
    ...
 
    return(hBinding);
}
 
/* The client stub calls this _unbind routine */
/* after each remote procedure call.                            */
void __RPC_USER DATA_HANDLE_TYPE_unbind(
    DATA_HANDLE_TYPE dh1, 
    RPC_BINDING_HANDLE h1)
{
    RPC_STATUS status;
    status = RpcBindingFree(&h1); 
    ...
}
```

Как явные, так и неявные маркеры привязки могут быть простыми или пользовательскими дескрипторами. То есть, маркер может быть следующим:

-   Примитив и неявный
-   Пользовательские и неявные
-   Примитив и EXPLICIT
-   Custom и EXPLICIT

 

 