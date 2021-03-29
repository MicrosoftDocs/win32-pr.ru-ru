---
title: атрибут ncacn_vns_spp
description: '\_ \_ Ключевое слово нкакн ВНС SPP идентифицирует Banyan VINEs SPP в качестве семейства протоколов для конечной точки. Это семейство протоколов устарело и не должно использоваться в новых приложениях.'
ms.assetid: a2aff0a6-2e7e-43e4-a180-f1ddd0456843
keywords:
- ncacn_vns_spp атрибута MIDL
topic_type:
- apiref
api_name:
- ncacn_vns_spp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84e72cd17ae65fbffc2cef280f15d12ba0ddbdbe
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103790710"
---
# <a name="ncacn_vns_spp-attribute"></a><span data-ttu-id="45d54-105">\_атрибут нкакн ВНС \_ SPP</span><span class="sxs-lookup"><span data-stu-id="45d54-105">ncacn\_vns\_spp attribute</span></span>

<span data-ttu-id="45d54-106">Ключевое слово **нкакн \_ ВНС \_ SPP** ИДЕНТИФИЦИРУЕТ Banyan Vines SPP в качестве семейства протоколов для конечной точки.</span><span class="sxs-lookup"><span data-stu-id="45d54-106">The **ncacn\_vns\_spp** keyword identifies Banyan Vines SPP as the protocol family for the endpoint.</span></span> <span data-ttu-id="45d54-107">Это семейство протоколов устарело и не должно использоваться в новых приложениях.</span><span class="sxs-lookup"><span data-stu-id="45d54-107">This protocol family is obsolete and should not be used in new applications.</span></span>

``` syntax
endpoint("ncacn_vns_spp:server-name[port-address]")
```

## <a name="parameters"></a><span data-ttu-id="45d54-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="45d54-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45d54-109">*имя сервера*</span><span class="sxs-lookup"><span data-stu-id="45d54-109">*server-name*</span></span> 
</dt> <dd>

<span data-ttu-id="45d54-110">Указывает Стритталк имя сервера.</span><span class="sxs-lookup"><span data-stu-id="45d54-110">Specifies the StreetTalk name of the server.</span></span> <span data-ttu-id="45d54-111">Имя имеет вид item@group @organization .</span><span class="sxs-lookup"><span data-stu-id="45d54-111">The name is of the form item@group@organization.</span></span> <span data-ttu-id="45d54-112">Элемент может иметь длину до 31 символа, а группа и организация могут содержать до 15 символов.</span><span class="sxs-lookup"><span data-stu-id="45d54-112">The item can be up to 31 characters long and the group and organization can be up to 15 characters.</span></span>

</dd> <dt>

<span data-ttu-id="45d54-113">*имя порта*</span><span class="sxs-lookup"><span data-stu-id="45d54-113">*port-name*</span></span> 
</dt> <dd>

<span data-ttu-id="45d54-114">Указывает порт Banyan Vines SPP.</span><span class="sxs-lookup"><span data-stu-id="45d54-114">Specifies a Banyan Vines SPP port.</span></span> <span data-ttu-id="45d54-115">Допустимый диапазон для статических конечных точек — 250 – 511.</span><span class="sxs-lookup"><span data-stu-id="45d54-115">The valid range for static endpoints is 250– 511.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="45d54-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="45d54-116">Remarks</span></span>

<span data-ttu-id="45d54-117">Чтобы использовать транспортный протокол **нкакн \_ ВНС \_ SPP** в распределенных приложениях под управлением Windows 2000, необходимо установить соответствующее клиентское программное обеспечение Banyan Enterprise.</span><span class="sxs-lookup"><span data-stu-id="45d54-117">In order to use the **ncacn\_vns\_spp** transport protocol in distributed applications running on Windows 2000, the appropriate Banyan Enterprise Client software must be installed.</span></span> <span data-ttu-id="45d54-118">После установки откройте **Панель управления**, выберите **Конфигурация и добавить**, а затем выберите **Service \| Banyan \| RPC Services for Banyan**.</span><span class="sxs-lookup"><span data-stu-id="45d54-118">After installation, open **Control Panel**, choose **Configuration and Add**, then select **Service \| Banyan \| RPC services for Banyan**.</span></span> <span data-ttu-id="45d54-119">Для поддержки 16-разрядных клиентов требуется соответствующее программное обеспечение Vines.</span><span class="sxs-lookup"><span data-stu-id="45d54-119">Support for 16-bit clients requires appropriate Vines software.</span></span> <span data-ttu-id="45d54-120">Дополнительные сведения о корпоративном клиенте Banyan и 16-разрядном программном обеспечении vines см. по адресу Banyan.</span><span class="sxs-lookup"><span data-stu-id="45d54-120">For more information about Banyan's Enterprise Client product and 16-bit Vines software, contact Banyan.</span></span>

<span data-ttu-id="45d54-121">Синтаксис строки транспортного порта Banyan Vines SPP, как и все строки портов, определяется независимо от спецификации IDL.</span><span class="sxs-lookup"><span data-stu-id="45d54-121">The syntax of the Banyan Vines SPP transport port string, like all port strings, is defined independently of the IDL specification.</span></span> <span data-ttu-id="45d54-122">Компилятор выполняет некоторую проверку синтаксиса, но не гарантирует, что указана правильная спецификация конечной точки.</span><span class="sxs-lookup"><span data-stu-id="45d54-122">The compiler performs some syntax checking but does not guarantee that the endpoint specification is correct.</span></span> <span data-ttu-id="45d54-123">Некоторые ошибки могут выводиться во время выполнения, а не во время компиляции.</span><span class="sxs-lookup"><span data-stu-id="45d54-123">Some errors may be reported at run time rather than at compile time.</span></span>

> [!Note]  
> <span data-ttu-id="45d54-124">Это семейство протоколов не поддерживается в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="45d54-124">This protocol family is not supported in Windows XP.</span></span>

 

## <a name="examples"></a><span data-ttu-id="45d54-125">Примеры</span><span class="sxs-lookup"><span data-stu-id="45d54-125">Examples</span></span>

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC), 
    version(1.1), 
    endpoint("ncacn_vns_spp:printer@sdkgrp@company[260]")
]
interface iface
{
    // Interface definition statements.
}
```

## <a name="see-also"></a><span data-ttu-id="45d54-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="45d54-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45d54-127">**endpoint**</span><span class="sxs-lookup"><span data-stu-id="45d54-127">**endpoint**</span></span>](endpoint.md)
</dt> <dt>

[<span data-ttu-id="45d54-128">Файл определения интерфейса (IDL)</span><span class="sxs-lookup"><span data-stu-id="45d54-128">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="45d54-129">**нкакн \_ в \_ DSP**</span><span class="sxs-lookup"><span data-stu-id="45d54-129">**ncacn\_at\_dsp**</span></span>](ncacn-at-dsp.md)
</dt> <dt>

[<span data-ttu-id="45d54-130">**нкакн \_ днет \_ NSP**</span><span class="sxs-lookup"><span data-stu-id="45d54-130">**ncacn\_dnet\_nsp**</span></span>](ncacn-dnet-nsp.md)
</dt> <dt>

[<span data-ttu-id="45d54-131">**нкакн \_ IP \_ TCP**</span><span class="sxs-lookup"><span data-stu-id="45d54-131">**ncacn\_ip\_tcp**</span></span>](ncacn-ip-tcp.md)
</dt> <dt>

[<span data-ttu-id="45d54-132">**нкакн \_ NetBIOS- \_ IPX**</span><span class="sxs-lookup"><span data-stu-id="45d54-132">**ncacn\_nb\_ipx**</span></span>](ncacn-nb-ipx.md)
</dt> <dt>

[<span data-ttu-id="45d54-133">**нкакн \_ SPX**</span><span class="sxs-lookup"><span data-stu-id="45d54-133">**ncacn\_spx**</span></span>](ncacn-spx.md)
</dt> <dt>

[<span data-ttu-id="45d54-134">**нкакн \_ имена \_ NetBIOS**</span><span class="sxs-lookup"><span data-stu-id="45d54-134">**ncacn\_nb\_nb**</span></span>](ncacn-nb-nb.md)
</dt> <dt>

[<span data-ttu-id="45d54-135">**нкакн \_ NetBIOS, \_ протокол TCP**</span><span class="sxs-lookup"><span data-stu-id="45d54-135">**ncacn\_nb\_tcp**</span></span>](ncacn-nb-tcp.md)
</dt> <dt>

[<span data-ttu-id="45d54-136">**нкакн \_ NP**</span><span class="sxs-lookup"><span data-stu-id="45d54-136">**ncacn\_np**</span></span>](ncacn-np.md)
</dt> <dt>

[<span data-ttu-id="45d54-137">**нкалрпк**</span><span class="sxs-lookup"><span data-stu-id="45d54-137">**ncalrpc**</span></span>](ncalrpc.md)
</dt> <dt>

[<span data-ttu-id="45d54-138">**нкадг \_ IPX**</span><span class="sxs-lookup"><span data-stu-id="45d54-138">**ncadg\_ipx**</span></span>](ncadg-ipx.md)
</dt> <dt>

[<span data-ttu-id="45d54-139">**нкадг \_ IP \_ UDP**</span><span class="sxs-lookup"><span data-stu-id="45d54-139">**ncadg\_ip\_udp**</span></span>](ncadg-ip-udp.md)
</dt> <dt>

[<span data-ttu-id="45d54-140">Строковая привязка</span><span class="sxs-lookup"><span data-stu-id="45d54-140">string binding</span></span>](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 