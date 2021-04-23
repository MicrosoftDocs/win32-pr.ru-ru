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
# <a name="primitive-and-custom-binding-handles"></a><span data-ttu-id="b3db4-103">Простые и пользовательские дескрипторы привязки</span><span class="sxs-lookup"><span data-stu-id="b3db4-103">Primitive and Custom Binding Handles</span></span>

<span data-ttu-id="b3db4-104">Все дескрипторы, объявленные с типами [**\_ \_ дескрипторов привязки**](rpc-binding-handle.md) [ \_ t](/windows/desktop/Midl/handle-t) или RPC, являются примитивными дескрипторами привязки.</span><span class="sxs-lookup"><span data-stu-id="b3db4-104">All handles declared with the [handle\_t](/windows/desktop/Midl/handle-t) or [**RPC\_BINDING\_HANDLE**](rpc-binding-handle.md) types are primitive binding handles.</span></span> <span data-ttu-id="b3db4-105">Можно расширить типы [**\_ \_ обработчиков привязки**](rpc-binding-handle.md) [ \_ t](/windows/desktop/Midl/handle-t) или RPC, чтобы они включали больше или больше информации, чем содержит тип простого обработчика.</span><span class="sxs-lookup"><span data-stu-id="b3db4-105">You can extend the [handle\_t](/windows/desktop/Midl/handle-t) or [**RPC\_BINDING\_HANDLE**](rpc-binding-handle.md) types to include more or different information than the primitive handle type contains.</span></span> <span data-ttu-id="b3db4-106">При этом создается пользовательский маркер привязки.</span><span class="sxs-lookup"><span data-stu-id="b3db4-106">When you do, you create a custom binding handle.</span></span>

<span data-ttu-id="b3db4-107">Чтобы сделать пользовательский маркер привязки для распределенного приложения, необходимо создать собственный тип данных и указать \[ атрибут [Handle](/windows/desktop/Midl/handle) в \] определении типа в IDL-файле.</span><span class="sxs-lookup"><span data-stu-id="b3db4-107">To make a custom binding handle for your distributed application, you will need to create your own data type and specify the \[ [handle](/windows/desktop/Midl/handle)\] attribute on a type definition in your IDL file.</span></span> <span data-ttu-id="b3db4-108">В конечном итоге, файлы заглушки сопоставляют пользовательские дескрипторы привязки с примитивными дескрипторами.</span><span class="sxs-lookup"><span data-stu-id="b3db4-108">Ultimately, the stub files map custom binding handles to primitive handles.</span></span>

<span data-ttu-id="b3db4-109">При создании собственного типа маркера привязки необходимо также предоставить подпрограммы BIND и Unbind, используемые клиентской заглушкой для отображения пользовательского маркера в виде примитивного маркера.</span><span class="sxs-lookup"><span data-stu-id="b3db4-109">If you do create your own binding handle type, you must also supply bind and unbind routines that the client stub uses to map a custom handle to a primitive handle.</span></span> <span data-ttu-id="b3db4-110">Заглушка вызывает процедуры привязки и отмены привязки в начале и в конце каждого удаленного вызова процедуры.</span><span class="sxs-lookup"><span data-stu-id="b3db4-110">The stub calls your bind and unbind routines at the beginning and end of each remote procedure call.</span></span> <span data-ttu-id="b3db4-111">Подпрограммы BIND и Unbind должны соответствовать следующим прототипам функций.</span><span class="sxs-lookup"><span data-stu-id="b3db4-111">The bind and unbind routines must conform to the following function prototypes.</span></span>



| <span data-ttu-id="b3db4-112">Прототип функции</span><span class="sxs-lookup"><span data-stu-id="b3db4-112">Function prototype</span></span>                     | <span data-ttu-id="b3db4-113">Описание</span><span class="sxs-lookup"><span data-stu-id="b3db4-113">Description</span></span>       |
|----------------------------------------|-------------------|
| <span data-ttu-id="b3db4-114">Handle \_ -тип \_ привязки (*тип*)</span><span class="sxs-lookup"><span data-stu-id="b3db4-114">handle\_t type\_bind(*type*)</span></span>           | <span data-ttu-id="b3db4-115">Подпрограммы привязки</span><span class="sxs-lookup"><span data-stu-id="b3db4-115">Binding routine</span></span>   |
| <span data-ttu-id="b3db4-116">Unbind типа void \_ (*тип*, *Handle \_ t*)</span><span class="sxs-lookup"><span data-stu-id="b3db4-116">void type\_unbind(*type*, *handle\_t*)</span></span> | <span data-ttu-id="b3db4-117">Выполняется отмена привязки</span><span class="sxs-lookup"><span data-stu-id="b3db4-117">Unbinding routine</span></span> |



 

<span data-ttu-id="b3db4-118">В следующем примере показано, как можно определить пользовательский маркер привязки в IDL-файле:</span><span class="sxs-lookup"><span data-stu-id="b3db4-118">The following example shows how a custom binding handle can be defined in the IDL file:</span></span>

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

<span data-ttu-id="b3db4-119">Если подпрограммы привязки обнаруживают ошибку, она должна вызвать исключение с помощью функции [**рпкраисиксцептион**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcraiseexception) .</span><span class="sxs-lookup"><span data-stu-id="b3db4-119">If the bind routine encounters an error, it should raise an exception using the [**RpcRaiseException**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcraiseexception) function.</span></span> <span data-ttu-id="b3db4-120">Клиентская заглушка будет очищена и позволить фильтру исключений в блок исключений, окружающий удаленный вызов процедур на стороне клиента.</span><span class="sxs-lookup"><span data-stu-id="b3db4-120">The client stub will then clean up, and let the exception filter through to the exception block surrounding the remote procedure call on the client side.</span></span> <span data-ttu-id="b3db4-121">Если подпрограмма привязки просто возвращает **значение NULL**, клиентский код получает ошибку \_ " \_ Недопустимая привязка RPC S" \_ .</span><span class="sxs-lookup"><span data-stu-id="b3db4-121">If the bind routine simply returns **NULL**, the client code gets error RPC\_S\_INVALID\_BINDING.</span></span> <span data-ttu-id="b3db4-122">Хотя это и может быть приемлемым в некоторых ситуациях, другие ситуации (например, не хватает памяти) не реагируют.</span><span class="sxs-lookup"><span data-stu-id="b3db4-122">While this might be acceptable in certain situations, other situations (such as being out of memory) do not respond well.</span></span> <span data-ttu-id="b3db4-123">Подпрограммы Unbind должны быть спроектированы так, чтобы не завершаться сбоем.</span><span class="sxs-lookup"><span data-stu-id="b3db4-123">The unbind routine should be designed so that it does not fail.</span></span> <span data-ttu-id="b3db4-124">Подпрограммы Unbind не должны вызывать исключения.</span><span class="sxs-lookup"><span data-stu-id="b3db4-124">The unbind routine should not raise exceptions.</span></span>

<span data-ttu-id="b3db4-125">В клиентском приложении отображаются подпрограммы привязки и отмены привязки, определяемые программистом.</span><span class="sxs-lookup"><span data-stu-id="b3db4-125">The programmer-defined bind and unbind routines appear in the client application.</span></span> <span data-ttu-id="b3db4-126">В следующем примере подпрограммы привязки вызывают [**рпкбиндингфромстрингбиндинг**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) , чтобы преобразовать сведения о привязке строк в маркер привязки.</span><span class="sxs-lookup"><span data-stu-id="b3db4-126">In the following example, the bind routine calls [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) to convert the string-binding information to a binding handle.</span></span> <span data-ttu-id="b3db4-127">Подпрограммы Unbind вызывают [**рпкбиндингфри**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfree) , чтобы освободить маркер привязки.</span><span class="sxs-lookup"><span data-stu-id="b3db4-127">The unbind routine calls [**RpcBindingFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfree) to free the binding handle.</span></span>

<span data-ttu-id="b3db4-128">Имя определяемого программистом маркера привязки ( \_ тип маркера данных \_ ) отображается как часть имени функции.</span><span class="sxs-lookup"><span data-stu-id="b3db4-128">The name of the programmer-defined binding handle, DATA\_HANDLE\_TYPE, appears as part of the name of the functions.</span></span> <span data-ttu-id="b3db4-129">Он также используется в качестве типа параметра в параметрах функции.</span><span class="sxs-lookup"><span data-stu-id="b3db4-129">It is also used as the parameter type in the function parameters.</span></span>

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

<span data-ttu-id="b3db4-130">Как явные, так и неявные маркеры привязки могут быть простыми или пользовательскими дескрипторами.</span><span class="sxs-lookup"><span data-stu-id="b3db4-130">Both implicit and explicit binding handles can either be primitive or custom handles.</span></span> <span data-ttu-id="b3db4-131">То есть, маркер может быть следующим:</span><span class="sxs-lookup"><span data-stu-id="b3db4-131">That is, a handle may be:</span></span>

-   <span data-ttu-id="b3db4-132">Примитив и неявный</span><span class="sxs-lookup"><span data-stu-id="b3db4-132">Primitive and implicit</span></span>
-   <span data-ttu-id="b3db4-133">Пользовательские и неявные</span><span class="sxs-lookup"><span data-stu-id="b3db4-133">Custom and implicit</span></span>
-   <span data-ttu-id="b3db4-134">Примитив и EXPLICIT</span><span class="sxs-lookup"><span data-stu-id="b3db4-134">Primitive and explicit</span></span>
-   <span data-ttu-id="b3db4-135">Custom и EXPLICIT</span><span class="sxs-lookup"><span data-stu-id="b3db4-135">Custom and explicit</span></span>

 

 