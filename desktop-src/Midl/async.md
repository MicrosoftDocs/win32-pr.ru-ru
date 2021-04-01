---
title: Атрибут async
description: Атрибут \ Async \ ACF определяет удаленный вызов процедуры в качестве асинхронной операции.
ms.assetid: 8002980a-94be-4d45-99d7-dfa4eae7f102
keywords:
- асинхронный атрибут MIDL
topic_type:
- apiref
api_name:
- async
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 562b157f26078c6f4d5b3cffe47417fa18fe608d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103987428"
---
# <a name="async-attribute"></a><span data-ttu-id="93a04-104">Атрибут async</span><span class="sxs-lookup"><span data-stu-id="93a04-104">async attribute</span></span>

<span data-ttu-id="93a04-105">Атрибут \[ **Async** \] ACF определяет удаленный вызов процедуры в качестве асинхронной операции.</span><span class="sxs-lookup"><span data-stu-id="93a04-105">The \[**async**\] ACF attribute defines a remote procedure call as an asynchronous operation.</span></span>

``` syntax
[async, opt-acf-attributes] function-name (param-list)
```

## <a name="parameters"></a><span data-ttu-id="93a04-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="93a04-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93a04-107">*OPT-ACF — атрибуты*</span><span class="sxs-lookup"><span data-stu-id="93a04-107">*opt-acf-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="93a04-108">Указывает необязательные атрибуты конфигурации приложения.</span><span class="sxs-lookup"><span data-stu-id="93a04-108">Specifies optional application configuration attributes.</span></span>

</dd> <dt>

<span data-ttu-id="93a04-109">*имя функции*</span><span class="sxs-lookup"><span data-stu-id="93a04-109">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="93a04-110">Указывает имя функции в IDL-файле.</span><span class="sxs-lookup"><span data-stu-id="93a04-110">Specifies the name of the function in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="93a04-111">*Param-List*</span><span class="sxs-lookup"><span data-stu-id="93a04-111">*param-list*</span></span> 
</dt> <dd>

<span data-ttu-id="93a04-112">Указывает необязательный список параметров.</span><span class="sxs-lookup"><span data-stu-id="93a04-112">Specifies an optional parameter list.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="93a04-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="93a04-113">Remarks</span></span>

<span data-ttu-id="93a04-114">Этот атрибут неприменим в интерфейсах COM.</span><span class="sxs-lookup"><span data-stu-id="93a04-114">This attribute is not applicable in COM interfaces.</span></span>

<span data-ttu-id="93a04-115">Чтобы объявить функцию RPC как асинхронную, сначала объявите функцию как часть определения интерфейса в IDL-файле.</span><span class="sxs-lookup"><span data-stu-id="93a04-115">To declare an RPC function as asynchronous, first declare the function as part of an interface definition in an IDL file.</span></span> <span data-ttu-id="93a04-116">Затем измените объявление функции в файле конфигурации приложения (ACF), применив \[  \] атрибут Async.</span><span class="sxs-lookup"><span data-stu-id="93a04-116">Then modify that function declaration, within the application configuration file (ACF), by applying the \[**async**\] attribute.</span></span> <span data-ttu-id="93a04-117">Обратите внимание, что в объявлении функции нет упоминания о асинхронном обработчике и что этот маркер привязки является первым параметром.</span><span class="sxs-lookup"><span data-stu-id="93a04-117">Note that the function declaration makes no mention of the asynchronous handle and that the binding handle is the first parameter.</span></span> <span data-ttu-id="93a04-118">Применение атрибута \[ **Async** \] в файле ACF создает соответствующий код, чтобы при вызове этой функции асинхронный сервер получал асинхронный обработчик перед другими параметрами.</span><span class="sxs-lookup"><span data-stu-id="93a04-118">Applying the \[**async**\] attribute in the ACF file generates the appropriate code so that when this function is called, the asynchronous server expects to receive an asynchronous handle before the other parameters.</span></span>

> [!Note]  
> <span data-ttu-id="93a04-119">Атрибут async нельзя использовать с параметром командной строки [**/ОСФ**](-osf.md) .</span><span class="sxs-lookup"><span data-stu-id="93a04-119">The async attribute cannot be used with the [**/osf**](-osf.md) command line switch.</span></span>

 

## <a name="examples"></a><span data-ttu-id="93a04-120">Примеры</span><span class="sxs-lookup"><span data-stu-id="93a04-120">Examples</span></span>

``` syntax
//file:Xasync.idl
interface AsyncIface 
{
    HRESULT MyAsyncFunc (
        handle_t hBinding,
        [in] int a,
        [in] int b,
        [out] int *c) ;
//other interface definitions
}
//end XAsync.idl

// file: Xasync.acf
interface AsyncIface
{
    [async] MyAsyncFunc () ;
    //any other ACF definitions
}
//end Xasync.acf
```

## <a name="see-also"></a><span data-ttu-id="93a04-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="93a04-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93a04-122">Файл конфигурации приложения (ACF)</span><span class="sxs-lookup"><span data-stu-id="93a04-122">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="93a04-123">Асинхронный RPC</span><span class="sxs-lookup"><span data-stu-id="93a04-123">Asynchronous RPC</span></span>](/windows/desktop/Rpc/asynchronous-rpc)
</dt> </dl>

 

 