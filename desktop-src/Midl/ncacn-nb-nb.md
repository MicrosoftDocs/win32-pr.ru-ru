---
title: атрибут ncacn_nb_nb
description: '\_ \_ Ключевое слово нкакн NetBIOS-имен NetBIOS определяет NetBEUI через NetBIOS в качестве семейства протоколов для конечной точки. Это семейство протоколов устарело и не должно использоваться в новых приложениях.'
ms.assetid: 8bab2784-44ba-4356-85c1-5bd17e75d6a8
keywords:
- ncacn_nb_nb атрибута MIDL
topic_type:
- apiref
api_name:
- ncacn_nb_nb
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c562bb0acd546fd2c8f92a92074e599c8a505dc9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "105661725"
---
# <a name="ncacn_nb_nb-attribute"></a><span data-ttu-id="c58d9-105">\_ \_ атрибут NetBIOS нкакн</span><span class="sxs-lookup"><span data-stu-id="c58d9-105">ncacn\_nb\_nb attribute</span></span>

<span data-ttu-id="c58d9-106">Ключевое слово **нкакн \_ NetBIOS \_** -имен NetBIOS определяет NetBEUI через NetBIOS в качестве семейства протоколов для конечной точки.</span><span class="sxs-lookup"><span data-stu-id="c58d9-106">The **ncacn\_nb\_nb** keyword identifies NetBEUI over NetBIOS as the protocol family for the endpoint.</span></span> <span data-ttu-id="c58d9-107">Это семейство протоколов устарело и не должно использоваться в новых приложениях.</span><span class="sxs-lookup"><span data-stu-id="c58d9-107">This protocol family is obsolete and should not be used in new applications.</span></span>

``` syntax
endpoint("ncacn_nb_nb:[port-name]")
```

## <a name="parameters"></a><span data-ttu-id="c58d9-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="c58d9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c58d9-109">*имя порта*</span><span class="sxs-lookup"><span data-stu-id="c58d9-109">*port-name*</span></span> 
</dt> <dd>

<span data-ttu-id="c58d9-110">Задает необязательное 8-разрядное значение в диапазоне от 1 до 255.</span><span class="sxs-lookup"><span data-stu-id="c58d9-110">Specifies an optional 8-bit value ranging from 1 to 255.</span></span> <span data-ttu-id="c58d9-111">Значения меньше 0x20 зарезервированы.</span><span class="sxs-lookup"><span data-stu-id="c58d9-111">Values of less than 0x20 are reserved.</span></span> <span data-ttu-id="c58d9-112">Если значение *имени порта* не указано, служба сопоставления конечных точек выбирает значение порта.</span><span class="sxs-lookup"><span data-stu-id="c58d9-112">If the *port-name* value is not specified, the endpoint-mapping service selects the port value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c58d9-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c58d9-113">Remarks</span></span>

<span data-ttu-id="c58d9-114">Синтаксис строки порта NetBIOS, как и все строки портов, определяется реализацией транспорта и не зависит от спецификации IDL.</span><span class="sxs-lookup"><span data-stu-id="c58d9-114">The syntax of the NetBIOS port string, like all port strings, is defined by the transport implementation and is independent of the IDL specification.</span></span> <span data-ttu-id="c58d9-115">Компилятор MIDL выполняет ограниченную проверку синтаксиса, но не гарантирует, что указана правильная спецификация конечной точки.</span><span class="sxs-lookup"><span data-stu-id="c58d9-115">The MIDL compiler performs limited syntax checking but does not guarantee that the endpoint specification is correct.</span></span> <span data-ttu-id="c58d9-116">Некоторые классы ошибок могут выводиться во время выполнения, а не во время компиляции.</span><span class="sxs-lookup"><span data-stu-id="c58d9-116">Some classes of errors may be reported at run time rather than at compile time.</span></span>

> [!Note]  
> <span data-ttu-id="c58d9-117">Это семейство протоколов не поддерживается в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="c58d9-117">This protocol family is not supported in WindowsÂ XP.</span></span>

 

## <a name="examples"></a><span data-ttu-id="c58d9-118">Примеры</span><span class="sxs-lookup"><span data-stu-id="c58d9-118">Examples</span></span>

``` syntax
[
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncacn_nb_nb:[100]") 
] 
interface iface
{
    // Interface definition statements.
}
```

## <a name="see-also"></a><span data-ttu-id="c58d9-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c58d9-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c58d9-120">**endpoint**</span><span class="sxs-lookup"><span data-stu-id="c58d9-120">**endpoint**</span></span>](endpoint.md)
</dt> <dt>

[<span data-ttu-id="c58d9-121">Файл определения интерфейса (IDL)</span><span class="sxs-lookup"><span data-stu-id="c58d9-121">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="c58d9-122">**нкакн \_ IP \_ TCP**</span><span class="sxs-lookup"><span data-stu-id="c58d9-122">**ncacn\_ip\_tcp**</span></span>](ncacn-ip-tcp.md)
</dt> <dt>

[<span data-ttu-id="c58d9-123">**нкакн \_ NetBIOS, \_ протокол TCP**</span><span class="sxs-lookup"><span data-stu-id="c58d9-123">**ncacn\_nb\_tcp**</span></span>](ncacn-nb-tcp.md)
</dt> <dt>

[<span data-ttu-id="c58d9-124">**нкакн \_ NP**</span><span class="sxs-lookup"><span data-stu-id="c58d9-124">**ncacn\_np**</span></span>](ncacn-np.md)
</dt> <dt>

[<span data-ttu-id="c58d9-125">**нкакн \_ SPX**</span><span class="sxs-lookup"><span data-stu-id="c58d9-125">**ncacn\_spx**</span></span>](ncacn-spx.md)
</dt> <dt>

[<span data-ttu-id="c58d9-126">**нкалрпк**</span><span class="sxs-lookup"><span data-stu-id="c58d9-126">**ncalrpc**</span></span>](ncalrpc.md)
</dt> <dt>

[<span data-ttu-id="c58d9-127">**Строковая привязка**</span><span class="sxs-lookup"><span data-stu-id="c58d9-127">**string binding**</span></span>](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 