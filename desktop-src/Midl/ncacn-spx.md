---
title: атрибут ncacn_spx
description: '\_Ключевое слово нкакн SPX обозначает SPX в качестве семейства протоколов для конечной точки. Это семейство протоколов устарело и не должно использоваться в новых приложениях.'
ms.assetid: 45e93e25-e84d-4242-80b0-c4b61e80f716
keywords:
- ncacn_spx атрибута MIDL
topic_type:
- apiref
api_name:
- ncacn_spx
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09d27cc746df906ff6b1a3290e41d860c76dc362
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "105661723"
---
# <a name="ncacn_spx-attribute"></a><span data-ttu-id="abb92-105">\_атрибут нкакн SPX</span><span class="sxs-lookup"><span data-stu-id="abb92-105">ncacn\_spx attribute</span></span>

<span data-ttu-id="abb92-106">Ключевое слово **нкакн \_ SPX** обозначает SPX в качестве семейства протоколов для конечной точки.</span><span class="sxs-lookup"><span data-stu-id="abb92-106">The **ncacn\_spx** keyword identifies SPX as the protocol family for the endpoint.</span></span> <span data-ttu-id="abb92-107">Это семейство протоколов устарело и не должно использоваться в новых приложениях.</span><span class="sxs-lookup"><span data-stu-id="abb92-107">This protocol family is obsolete and should not be used in new applications.</span></span>

``` syntax
endpoint("ncacn_spx:link-address[port-name]")
```

## <a name="parameters"></a><span data-ttu-id="abb92-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="abb92-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="abb92-109">*адрес ссылки*</span><span class="sxs-lookup"><span data-stu-id="abb92-109">*link-address*</span></span> 
</dt> <dd>

<span data-ttu-id="abb92-110">Указывает сервер узла.</span><span class="sxs-lookup"><span data-stu-id="abb92-110">Specifies the host server.</span></span> <span data-ttu-id="abb92-111">Это может быть либо строка символов (имя сервера), либо 20-значное шестнадцатеричное число, состоящее из сетевого адреса сервера узла (8 цифр), сцепленного с адресом узла (12 цифр).</span><span class="sxs-lookup"><span data-stu-id="abb92-111">This may be either a character string (the server name), or a 20-digit hexadecimal number that consists of the host server's network address (8 digits) concatenated with the node address (12 digits).</span></span> <span data-ttu-id="abb92-112">Инструкции по получению сетевого адреса и адреса узла см. в разделе Примечания.</span><span class="sxs-lookup"><span data-stu-id="abb92-112">See Remarks for instructions on how to obtain the network address and node address.</span></span> <span data-ttu-id="abb92-113">Строка **null** указывает локальный компьютер.</span><span class="sxs-lookup"><span data-stu-id="abb92-113">A **NULL** string specifies the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="abb92-114">*имя порта*</span><span class="sxs-lookup"><span data-stu-id="abb92-114">*port-name*</span></span> 
</dt> <dd>

<span data-ttu-id="abb92-115">Указывает необязательное 16-разрядное число, представляющее адрес сокета.</span><span class="sxs-lookup"><span data-stu-id="abb92-115">Specifies an optional 16-bit number that represents the socket address.</span></span> <span data-ttu-id="abb92-116">Значения могут находиться в диапазоне от 1 до 65 535.</span><span class="sxs-lookup"><span data-stu-id="abb92-116">Values can range from 1 to 65,535.</span></span> <span data-ttu-id="abb92-117">Если значение не указано, служба сопоставления конечных точек выбирает допустимое значение *имени порта* .</span><span class="sxs-lookup"><span data-stu-id="abb92-117">When no value is specified, the endpoint-mapping service selects a valid *port-name* value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="abb92-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="abb92-118">Remarks</span></span>

<span data-ttu-id="abb92-119">При использовании транспортного **нкакн \_ SPX** имя сервера точно совпадает с именем 32-разрядного Windows.</span><span class="sxs-lookup"><span data-stu-id="abb92-119">When you use the **ncacn\_spx** transport, the server name is exactly the same as the 32-bit Windows name.</span></span> <span data-ttu-id="abb92-120">Однако поскольку имена распределяются по протоколам Novell, они должны соответствовать соглашениям об именовании Novell.</span><span class="sxs-lookup"><span data-stu-id="abb92-120">However, since the names are distributed using Novell protocols, they must conform to the Novell naming conventions.</span></span> <span data-ttu-id="abb92-121">Если имя сервера не является допустимым именем Novell, серверы не смогут создавать конечные точки с помощью транспорта **нкакн \_ SPX** .</span><span class="sxs-lookup"><span data-stu-id="abb92-121">If a server name is not a valid Novell name, servers will not be able to create endpoints with the **ncacn\_spx** transport.</span></span> <span data-ttu-id="abb92-122">Ниже приведен неполный список символов, запрещенных в именах серверов Novell.</span><span class="sxs-lookup"><span data-stu-id="abb92-122">The following is a partial list of characters prohibited in Novell server names:</span></span>

<span data-ttu-id="abb92-123">" \* + .</span><span class="sxs-lookup"><span data-stu-id="abb92-123">" \* + .</span></span> <span data-ttu-id="abb92-124">/ : ; < = >?</span><span class="sxs-lookup"><span data-stu-id="abb92-124">/ : ; < = > ?</span></span> <span data-ttu-id="abb92-125">\[ \] \\ \|</span><span class="sxs-lookup"><span data-stu-id="abb92-125">\[ \] \\ \|</span></span>

<span data-ttu-id="abb92-126">Транспорт **нкакн \_ SPX** не поддерживается версией NWLink, предоставляемой в MS Client 3,0.</span><span class="sxs-lookup"><span data-stu-id="abb92-126">The **ncacn\_spx** transport is not supported by the version of NWLink supplied with MS Client 3.0.</span></span>

<span data-ttu-id="abb92-127">в 16-разрядных клиентских приложениях Windows, использующих транспорт **нкакн \_ SPX** , требуется, чтобы файл Nwipxspx.dll был установлен для запуска в подсистеме WOW.</span><span class="sxs-lookup"><span data-stu-id="abb92-127">16-bit Windows client applications that use the **ncacn\_spx** transport require that the file Nwipxspx.dll be installed in order to run under the WOW subsystem.</span></span> <span data-ttu-id="abb92-128">Чтобы получить этот файл, обратитесь в Novell.</span><span class="sxs-lookup"><span data-stu-id="abb92-128">Contact Novell to obtain this file.</span></span>

> [!Note]  
> <span data-ttu-id="abb92-129">Чтобы получить адреса сети и узла, используйте служебную программу Novell **comпроверьте конфигурацию** или **ипксжетинтернетаддресс** API, определяемый Novell.</span><span class="sxs-lookup"><span data-stu-id="abb92-129">To obtain the network and node addresses, use Novell's **comcheck** utility, or the Novell-defined API **IPXGetInternetAddress**.</span></span> <span data-ttu-id="abb92-130">В Windows эти адреса также можно получить с помощью команды **ipxroute config** .</span><span class="sxs-lookup"><span data-stu-id="abb92-130">On Windows, you can also obtain these addresses with the **ipxroute config** command.</span></span>

 

<span data-ttu-id="abb92-131">Синтаксис строки транспортного порта SPX, как и все строки портов, определяется независимо от спецификации IDL.</span><span class="sxs-lookup"><span data-stu-id="abb92-131">The syntax of the SPX transport port string, like all port strings, is defined independently of the IDL specification.</span></span> <span data-ttu-id="abb92-132">Компилятор выполняет некоторую проверку синтаксиса, но не гарантирует, что указана правильная спецификация конечной точки.</span><span class="sxs-lookup"><span data-stu-id="abb92-132">The compiler performs some syntax checking but does not guarantee that the endpoint specification is correct.</span></span> <span data-ttu-id="abb92-133">Некоторые ошибки могут выводиться во время выполнения, а не во время компиляции.</span><span class="sxs-lookup"><span data-stu-id="abb92-133">Some errors may be reported at run time rather than at compile time.</span></span>

## <a name="examples"></a><span data-ttu-id="abb92-134">Примеры</span><span class="sxs-lookup"><span data-stu-id="abb92-134">Examples</span></span>

``` syntax
[
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncacn_spx:[1000]") 
] 
interface iface
{
    // Interface definition statements.
}
```

## <a name="see-also"></a><span data-ttu-id="abb92-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="abb92-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="abb92-136">**endpoint**</span><span class="sxs-lookup"><span data-stu-id="abb92-136">**endpoint**</span></span>](endpoint.md)
</dt> <dt>

[<span data-ttu-id="abb92-137">Файл определения интерфейса (IDL)</span><span class="sxs-lookup"><span data-stu-id="abb92-137">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="abb92-138">**нкакн \_ в \_ DSP**</span><span class="sxs-lookup"><span data-stu-id="abb92-138">**ncacn\_at\_dsp**</span></span>](ncacn-at-dsp.md)
</dt> <dt>

[<span data-ttu-id="abb92-139">**нкакн \_ днет \_ NSP**</span><span class="sxs-lookup"><span data-stu-id="abb92-139">**ncacn\_dnet\_nsp**</span></span>](ncacn-dnet-nsp.md)
</dt> <dt>

[<span data-ttu-id="abb92-140">**нкакн \_ IP \_ TCP**</span><span class="sxs-lookup"><span data-stu-id="abb92-140">**ncacn\_ip\_tcp**</span></span>](ncacn-ip-tcp.md)
</dt> <dt>

[<span data-ttu-id="abb92-141">**нкакн \_ NetBIOS- \_ IPX**</span><span class="sxs-lookup"><span data-stu-id="abb92-141">**ncacn\_nb\_ipx**</span></span>](ncacn-nb-ipx.md)
</dt> <dt>

[<span data-ttu-id="abb92-142">**нкакн \_ имена \_ NetBIOS**</span><span class="sxs-lookup"><span data-stu-id="abb92-142">**ncacn\_nb\_nb**</span></span>](ncacn-nb-nb.md)
</dt> <dt>

[<span data-ttu-id="abb92-143">**нкакн \_ NetBIOS, \_ протокол TCP**</span><span class="sxs-lookup"><span data-stu-id="abb92-143">**ncacn\_nb\_tcp**</span></span>](ncacn-nb-tcp.md)
</dt> <dt>

[<span data-ttu-id="abb92-144">**нкакн \_ NP**</span><span class="sxs-lookup"><span data-stu-id="abb92-144">**ncacn\_np**</span></span>](ncacn-np.md)
</dt> <dt>

[<span data-ttu-id="abb92-145">**нкакн \_ ВНС \_ SPP**</span><span class="sxs-lookup"><span data-stu-id="abb92-145">**ncacn\_vns\_spp**</span></span>](ncacn-vns-spp.md)
</dt> <dt>

[<span data-ttu-id="abb92-146">**нкалрпк**</span><span class="sxs-lookup"><span data-stu-id="abb92-146">**ncalrpc**</span></span>](ncalrpc.md)
</dt> <dt>

[<span data-ttu-id="abb92-147">**нкадг \_ IPX**</span><span class="sxs-lookup"><span data-stu-id="abb92-147">**ncadg\_ipx**</span></span>](ncadg-ipx.md)
</dt> <dt>

[<span data-ttu-id="abb92-148">**нкадг \_ IP \_ UDP**</span><span class="sxs-lookup"><span data-stu-id="abb92-148">**ncadg\_ip\_udp**</span></span>](ncadg-ip-udp.md)
</dt> <dt>

[<span data-ttu-id="abb92-149">Строковая привязка</span><span class="sxs-lookup"><span data-stu-id="abb92-149">string binding</span></span>](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 