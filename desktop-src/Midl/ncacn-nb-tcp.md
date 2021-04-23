---
title: атрибут ncacn_nb_tcp
description: '\_ \_ Ключевое слово TCP нкакн NetBIOS используется для обнаружения TCP через NetBIOS в качестве семейства протоколов для конечной точки. Это семейство протоколов устарело и не должно использоваться в новых приложениях.'
ms.assetid: 3633842c-d1f5-46d9-866e-e54f31415ea5
keywords:
- ncacn_nb_tcp атрибута MIDL
topic_type:
- apiref
api_name:
- ncacn_nb_tcp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d59a544c592643cffcb282ba8a0f3fdab48c03fd
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104337292"
---
# <a name="ncacn_nb_tcp-attribute"></a><span data-ttu-id="bea83-105">\_ \_ атрибут TCP нкакн NetBIOS</span><span class="sxs-lookup"><span data-stu-id="bea83-105">ncacn\_nb\_tcp attribute</span></span>

<span data-ttu-id="bea83-106">Ключевое слово **\_ \_ TCP нкакн NetBIOS** используется для обнаружения TCP через NetBIOS в качестве семейства протоколов для конечной точки.</span><span class="sxs-lookup"><span data-stu-id="bea83-106">The **ncacn\_nb\_tcp** keyword is used to identify TCP over NetBIOS as the protocol family for the endpoint.</span></span> <span data-ttu-id="bea83-107">Это семейство протоколов устарело и не должно использоваться в новых приложениях.</span><span class="sxs-lookup"><span data-stu-id="bea83-107">This protocol family is obsolete and should not be used in new applications.</span></span>

``` syntax
endpoint("ncacn_nb_tcp:[port-name]")
```

## <a name="parameters"></a><span data-ttu-id="bea83-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="bea83-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bea83-109">*имя порта*</span><span class="sxs-lookup"><span data-stu-id="bea83-109">*port-name*</span></span> 
</dt> <dd>

<span data-ttu-id="bea83-110">Задает необязательное 8-разрядное значение в диапазоне от 1 до 254.</span><span class="sxs-lookup"><span data-stu-id="bea83-110">Specifies an optional 8-bit value ranging from 1 to 254.</span></span> <span data-ttu-id="bea83-111">Значения меньше 0x20 зарезервированы.</span><span class="sxs-lookup"><span data-stu-id="bea83-111">Values of less than 0x20 are reserved.</span></span> <span data-ttu-id="bea83-112">Если значение *имени порта* не указано, служба сопоставления конечных точек выбирает значение порта.</span><span class="sxs-lookup"><span data-stu-id="bea83-112">If the *port-name* value is not specified, the endpoint-mapping service selects the port value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bea83-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bea83-113">Remarks</span></span>

<span data-ttu-id="bea83-114">Синтаксис строки порта NetBIOS, как и все строки портов, определяется реализацией транспорта и не зависит от спецификации IDL.</span><span class="sxs-lookup"><span data-stu-id="bea83-114">The syntax of the NetBIOS port string, like all port strings, is defined by the transport implementation and is independent of the IDL specification.</span></span> <span data-ttu-id="bea83-115">Компилятор MIDL выполняет ограниченную проверку синтаксиса, но не гарантирует, что указана правильная спецификация конечной точки.</span><span class="sxs-lookup"><span data-stu-id="bea83-115">The MIDL compiler performs limited syntax checking but does not guarantee that the endpoint specification is correct.</span></span> <span data-ttu-id="bea83-116">Некоторые классы ошибок могут выводиться во время выполнения, а не во время компиляции.</span><span class="sxs-lookup"><span data-stu-id="bea83-116">Some classes of errors may be reported at run time rather than at compile time.</span></span>

> [!Note]  
> <span data-ttu-id="bea83-117">Это семейство протоколов не поддерживается в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="bea83-117">This protocol family is not supported in WindowsÂ XP.</span></span>

 

## <a name="examples"></a><span data-ttu-id="bea83-118">Примеры</span><span class="sxs-lookup"><span data-stu-id="bea83-118">Examples</span></span>

``` syntax
[
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncacn_nb_tcp:[100]") 
] 
interface iface
{
    // Interface definition statements.
}
```

## <a name="see-also"></a><span data-ttu-id="bea83-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bea83-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bea83-120">**endpoint**</span><span class="sxs-lookup"><span data-stu-id="bea83-120">**endpoint**</span></span>](endpoint.md)
</dt> <dt>

[<span data-ttu-id="bea83-121">Файл определения интерфейса (IDL)</span><span class="sxs-lookup"><span data-stu-id="bea83-121">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="bea83-122">**нкакн \_ IP \_ TCP**</span><span class="sxs-lookup"><span data-stu-id="bea83-122">**ncacn\_ip\_tcp**</span></span>](ncacn-ip-tcp.md)
</dt> <dt>

[<span data-ttu-id="bea83-123">**нкакн \_ имена \_ NetBIOS**</span><span class="sxs-lookup"><span data-stu-id="bea83-123">**ncacn\_nb\_nb**</span></span>](ncacn-nb-nb.md)
</dt> <dt>

[<span data-ttu-id="bea83-124">**нкакн \_ NP**</span><span class="sxs-lookup"><span data-stu-id="bea83-124">**ncacn\_np**</span></span>](ncacn-np.md)
</dt> <dt>

[<span data-ttu-id="bea83-125">**нкакн \_ SPX**</span><span class="sxs-lookup"><span data-stu-id="bea83-125">**ncacn\_spx**</span></span>](ncacn-spx.md)
</dt> <dt>

[<span data-ttu-id="bea83-126">**нкалрпк**</span><span class="sxs-lookup"><span data-stu-id="bea83-126">**ncalrpc**</span></span>](ncalrpc.md)
</dt> <dt>

[<span data-ttu-id="bea83-127">**Строковая привязка**</span><span class="sxs-lookup"><span data-stu-id="bea83-127">**string binding**</span></span>](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 