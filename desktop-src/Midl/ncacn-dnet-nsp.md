---
title: атрибут ncacn_dnet_nsp
description: '\_ \_ Ключевое слово нкакн днет NSP идентифицирует DECnet в качестве семейства протоколов для конечной точки. Это семейство протоколов устарело и не должно использоваться в новых приложениях.'
ms.assetid: 797251c1-c5d3-416b-8bc7-5b83bb7027e6
keywords:
- ncacn_dnet_nsp атрибута MIDL
topic_type:
- apiref
api_name:
- ncacn_dnet_nsp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6312aff15d3bdef85d1e37829d669ce1faa5fbb4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104133838"
---
# <a name="ncacn_dnet_nsp-attribute"></a><span data-ttu-id="5cb16-105">нкакн \_ днет \_ NSP, атрибут</span><span class="sxs-lookup"><span data-stu-id="5cb16-105">ncacn\_dnet\_nsp attribute</span></span>

<span data-ttu-id="5cb16-106">Ключевое слово **нкакн \_ днет \_ NSP** идентифицирует DECnet в качестве семейства протоколов для конечной точки.</span><span class="sxs-lookup"><span data-stu-id="5cb16-106">The **ncacn\_dnet\_nsp** keyword identifies DECnet as the protocol family for the endpoint.</span></span> <span data-ttu-id="5cb16-107">Это семейство протоколов устарело и не должно использоваться в новых приложениях.</span><span class="sxs-lookup"><span data-stu-id="5cb16-107">This protocol family is obsolete and should not be used in new applications.</span></span>

``` syntax
endpoint("ncacn_dnet_nsp:server-name[port-name]")
```

## <a name="parameters"></a><span data-ttu-id="5cb16-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="5cb16-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5cb16-109">*имя сервера*</span><span class="sxs-lookup"><span data-stu-id="5cb16-109">*server-name*</span></span> 
</dt> <dd>

<span data-ttu-id="5cb16-110">Указывает имя или адрес в Интернете для сервера или узла, компьютер.</span><span class="sxs-lookup"><span data-stu-id="5cb16-110">Specifies the name or internet address for the server, or host, computer.</span></span> <span data-ttu-id="5cb16-111">Имя является символьной строкой.</span><span class="sxs-lookup"><span data-stu-id="5cb16-111">The name is a character string.</span></span>

</dd> <dt>

<span data-ttu-id="5cb16-112">*имя порта*</span><span class="sxs-lookup"><span data-stu-id="5cb16-112">*port-name*</span></span> 
</dt> <dd>

<span data-ttu-id="5cb16-113">Указывает имя объекта или номер объекта DECnet.</span><span class="sxs-lookup"><span data-stu-id="5cb16-113">Specifies a DECnet object name or object number.</span></span> <span data-ttu-id="5cb16-114">Имя объекта может содержать до 16 символов.</span><span class="sxs-lookup"><span data-stu-id="5cb16-114">The object name can consist of up to 16 characters.</span></span> <span data-ttu-id="5cb16-115">Номера объектов могут начинаться с символа решетки ( \# ).</span><span class="sxs-lookup"><span data-stu-id="5cb16-115">Object numbers can be prefixed by the pound sign (\#).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5cb16-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5cb16-116">Remarks</span></span>

<span data-ttu-id="5cb16-117">Синтаксис строки транспортного порта DECnet, как и все строки портов, определяется независимо от спецификации IDL.</span><span class="sxs-lookup"><span data-stu-id="5cb16-117">The syntax of the DECnet transport port string, like all port strings, is defined independently of the IDL specification.</span></span> <span data-ttu-id="5cb16-118">Компилятор выполняет некоторую проверку синтаксиса, но не гарантирует, что указана правильная спецификация конечной точки.</span><span class="sxs-lookup"><span data-stu-id="5cb16-118">The compiler performs some syntax checking but does not guarantee that the endpoint specification is correct.</span></span> <span data-ttu-id="5cb16-119">Некоторые ошибки могут выводиться во время выполнения, а не во время компиляции.</span><span class="sxs-lookup"><span data-stu-id="5cb16-119">Some errors may be reported at run time rather than at compile time.</span></span>

> [!Note]  
> <span data-ttu-id="5cb16-120">Это семейство протоколов не поддерживается в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="5cb16-120">This protocol family is not supported in WindowsÂ XP.</span></span>

 

## <a name="examples"></a><span data-ttu-id="5cb16-121">Примеры</span><span class="sxs-lookup"><span data-stu-id="5cb16-121">Examples</span></span>

``` syntax
[   
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncacn_dnet_nsp:node[RPC0034501]") 
interface iface
{
    // Interface definition statements.
}

[
    uuid(12345678-1234-1234-1234-123456789ABC), 
    version(1.1), 
    endpoint("ncacn_dnet_nsp:node[#41]") 
] 
interface iface
{
    // Interface definition statements.
}
```

## <a name="see-also"></a><span data-ttu-id="5cb16-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5cb16-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5cb16-123">**endpoint**</span><span class="sxs-lookup"><span data-stu-id="5cb16-123">**endpoint**</span></span>](endpoint.md)
</dt> <dt>

[<span data-ttu-id="5cb16-124">**Строковая привязка**</span><span class="sxs-lookup"><span data-stu-id="5cb16-124">**string binding**</span></span>](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 