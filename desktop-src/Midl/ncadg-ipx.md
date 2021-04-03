---
title: атрибут ncadg_ipx
description: '\_Ключевое слово нкадг IPX определяет IPX как семейство протоколов для конечной точки. Это семейство протоколов устарело и не должно использоваться в новых приложениях.'
ms.assetid: 6b136eb9-4e18-43ff-993b-a2ad005273f1
keywords:
- ncadg_ipx атрибута MIDL
topic_type:
- apiref
api_name:
- ncadg_ipx
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1fa206902ae80e5218e1d5249da8a8fb1b9dfc04
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103790183"
---
# <a name="ncadg_ipx-attribute"></a><span data-ttu-id="a59ac-105">\_атрибут нкадг IPX</span><span class="sxs-lookup"><span data-stu-id="a59ac-105">ncadg\_ipx attribute</span></span>

<span data-ttu-id="a59ac-106">Ключевое слово **нкадг \_ IPX** определяет IPX как семейство протоколов для конечной точки.</span><span class="sxs-lookup"><span data-stu-id="a59ac-106">The **ncadg\_ipx** keyword identifies IPX as the protocol family for the endpoint.</span></span> <span data-ttu-id="a59ac-107">Это семейство протоколов устарело и не должно использоваться в новых приложениях.</span><span class="sxs-lookup"><span data-stu-id="a59ac-107">This protocol family is obsolete and should not be used in new applications.</span></span>

``` syntax
endpoint("ncadg_ipx:link-address[port-name]")
```

## <a name="parameters"></a><span data-ttu-id="a59ac-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="a59ac-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a59ac-109">*адрес ссылки*</span><span class="sxs-lookup"><span data-stu-id="a59ac-109">*link-address*</span></span> 
</dt> <dd>

<span data-ttu-id="a59ac-110">Указывает сервер узла.</span><span class="sxs-lookup"><span data-stu-id="a59ac-110">Specifies the host server.</span></span> <span data-ttu-id="a59ac-111">Это может быть либо строка символов (имя сервера), либо 20-значное шестнадцатеричное число, состоящее из сетевого адреса сервера узла (8 цифр), сцепленного с адресом узла (12 цифр).</span><span class="sxs-lookup"><span data-stu-id="a59ac-111">This may be either a character string (the server name), or a 20-digit hexadecimal number that consists of the host server's network address (8 digits) concatenated with the node address (12 digits).</span></span> <span data-ttu-id="a59ac-112">Инструкции по получению сетевого адреса и адреса узла см. в разделе Примечания.</span><span class="sxs-lookup"><span data-stu-id="a59ac-112">See Remarks for instructions on how to obtain the network address and node address.</span></span> <span data-ttu-id="a59ac-113">Строка **null** указывает локальный компьютер.</span><span class="sxs-lookup"><span data-stu-id="a59ac-113">A **NULL** string specifies the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="a59ac-114">*имя порта*</span><span class="sxs-lookup"><span data-stu-id="a59ac-114">*port-name*</span></span> 
</dt> <dd>

<span data-ttu-id="a59ac-115">Указывает необязательное 16-разрядное число, представляющее адрес сокета.</span><span class="sxs-lookup"><span data-stu-id="a59ac-115">Specifies an optional 16-bit number that represents the socket address.</span></span> <span data-ttu-id="a59ac-116">Значения могут находиться в диапазоне от 1 до 65535.</span><span class="sxs-lookup"><span data-stu-id="a59ac-116">Values can range from 1 to 65535.</span></span> <span data-ttu-id="a59ac-117">Если значение не указано, служба сопоставления конечных точек выбирает допустимое значение *имени порта* .</span><span class="sxs-lookup"><span data-stu-id="a59ac-117">When no value is specified, the endpoint-mapping service selects a valid *port-name* value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a59ac-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a59ac-118">Remarks</span></span>

<span data-ttu-id="a59ac-119">К протоколам датаграмм, **нкадг \_ IPX** и [**нкадг \_ IP \_ UDP**](ncadg-ip-udp.md)применяются следующие ограничения.</span><span class="sxs-lookup"><span data-stu-id="a59ac-119">The following restrictions apply to the datagram protocols, **ncadg\_ipx** and [**ncadg\_ip\_udp**](ncadg-ip-udp.md):</span></span>

-   <span data-ttu-id="a59ac-120">Они не поддерживают обратные вызовы.</span><span class="sxs-lookup"><span data-stu-id="a59ac-120">They do not support callbacks.</span></span> <span data-ttu-id="a59ac-121">Все функции, использующие **\[** атрибут [**обратного вызова**](callback.md) , завершатся **\]** ошибкой.</span><span class="sxs-lookup"><span data-stu-id="a59ac-121">Any functions using the **\[**[**callback**](callback.md)**\]** attribute will fail.</span></span>
-   <span data-ttu-id="a59ac-122">Они не поддерживают использование конструктора типа [**канала**](pipe.md) .</span><span class="sxs-lookup"><span data-stu-id="a59ac-122">They do not support use of the [**pipe**](pipe.md) type constructor.</span></span>

<span data-ttu-id="a59ac-123">При использовании транспорта **\_ IPX нкадг** имя сервера совпадает с именем 32-разрядного сервера Windows Server.</span><span class="sxs-lookup"><span data-stu-id="a59ac-123">When using the **ncadg\_ipx** transport, the server name is exactly the same as the 32-bit Windows server name.</span></span> <span data-ttu-id="a59ac-124">Однако поскольку имена распределяются по протоколам Novell, они должны соответствовать соглашениям об именовании Novell.</span><span class="sxs-lookup"><span data-stu-id="a59ac-124">However, since the names are distributed using Novell protocols, they must conform to the Novell naming conventions.</span></span> <span data-ttu-id="a59ac-125">Если имя сервера не является допустимым именем Novell, то серверы не смогут создавать конечные точки с помощью транспорта **нкадг \_ IPX** .</span><span class="sxs-lookup"><span data-stu-id="a59ac-125">If a server name is not a valid Novell name, servers will not be able to create endpoints with the **ncadg\_ipx** transport.</span></span> <span data-ttu-id="a59ac-126">Ниже приведен неполный список символов, запрещенных в именах серверов Novell.</span><span class="sxs-lookup"><span data-stu-id="a59ac-126">The following is a partial list of characters prohibited in Novell server names:</span></span>

<span data-ttu-id="a59ac-127">" \* + .</span><span class="sxs-lookup"><span data-stu-id="a59ac-127">" \* + .</span></span> <span data-ttu-id="a59ac-128">/ : ; < = >?</span><span class="sxs-lookup"><span data-stu-id="a59ac-128">/ : ; < = > ?</span></span> <span data-ttu-id="a59ac-129">\[ \] \\ \|</span><span class="sxs-lookup"><span data-stu-id="a59ac-129">\[ \] \\ \|</span></span>

<span data-ttu-id="a59ac-130">Транспорт **нкадг \_ IPX** поддерживается версией NWLink, предоставляемой с MS Client 3,0.</span><span class="sxs-lookup"><span data-stu-id="a59ac-130">The **ncadg\_ipx** transport is supported by the version of NWLink supplied with MS Client 3.0.</span></span>

<span data-ttu-id="a59ac-131">в 16-разрядных клиентских приложениях Windows, использующих транспорт **нкадг \_ IPX** , требуется, чтобы файл Nwipxspx.dll был установлен для запуска в подсистеме WOW.</span><span class="sxs-lookup"><span data-stu-id="a59ac-131">16-bit Windows client applications that use the **ncadg\_ipx** transport require that the file Nwipxspx.dll be installed in order to run under the WOW subsystem.</span></span> <span data-ttu-id="a59ac-132">Чтобы получить этот файл, обратитесь в Novell.</span><span class="sxs-lookup"><span data-stu-id="a59ac-132">Contact Novell to obtain this file.</span></span>

<span data-ttu-id="a59ac-133">Чтобы получить адреса сети и узла, используйте служебную программу Novell **comпроверьте конфигурацию** или **ипксжетинтернетаддресс** API, определяемый Novell.</span><span class="sxs-lookup"><span data-stu-id="a59ac-133">To obtain the network and node addresses, use Novell's **comcheck** utility, or the Novell-defined API **IPXGetInternetAddress**.</span></span> <span data-ttu-id="a59ac-134">В Windows эти адреса также можно получить с помощью команды **ipxroute config** .</span><span class="sxs-lookup"><span data-stu-id="a59ac-134">On Windows, you can also obtain these addresses with the **ipxroute config** command.</span></span>

<span data-ttu-id="a59ac-135">Синтаксис строки порта транспорта TCP/IP, как и все строки портов, определяется независимо от спецификации IDL.</span><span class="sxs-lookup"><span data-stu-id="a59ac-135">The syntax of the TCP/IP transport port string, like all port strings, is defined independently of the IDL specification.</span></span> <span data-ttu-id="a59ac-136">Компилятор выполняет некоторую проверку синтаксиса, но не гарантирует, что указана правильная спецификация конечной точки.</span><span class="sxs-lookup"><span data-stu-id="a59ac-136">The compiler performs some syntax checking but does not guarantee that the endpoint specification is correct.</span></span> <span data-ttu-id="a59ac-137">Некоторые ошибки могут выводиться во время выполнения, а не во время компиляции.</span><span class="sxs-lookup"><span data-stu-id="a59ac-137">Some errors may be reported at run time rather than at compile time.</span></span>

> [!Note]  
> <span data-ttu-id="a59ac-138">Это семейство протоколов не поддерживается в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a59ac-138">This protocol family is not supported in WindowsÂ XP.</span></span>

 

## <a name="examples"></a><span data-ttu-id="a59ac-139">Примеры</span><span class="sxs-lookup"><span data-stu-id="a59ac-139">Examples</span></span>

``` syntax
[
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncadg_ipx:[1000]") 
]
interface iface
{
    // Interface definition statements.
}
```

## <a name="see-also"></a><span data-ttu-id="a59ac-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a59ac-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a59ac-141">**endpoint**</span><span class="sxs-lookup"><span data-stu-id="a59ac-141">**endpoint**</span></span>](endpoint.md)
</dt> <dt>

[<span data-ttu-id="a59ac-142">Файл определения интерфейса (IDL)</span><span class="sxs-lookup"><span data-stu-id="a59ac-142">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="a59ac-143">**нкакн \_ в \_ DSP**</span><span class="sxs-lookup"><span data-stu-id="a59ac-143">**ncacn\_at\_dsp**</span></span>](ncacn-at-dsp.md)
</dt> <dt>

[<span data-ttu-id="a59ac-144">**нкакн \_ днет \_ NSP**</span><span class="sxs-lookup"><span data-stu-id="a59ac-144">**ncacn\_dnet\_nsp**</span></span>](ncacn-dnet-nsp.md)
</dt> <dt>

[<span data-ttu-id="a59ac-145">**нкакн \_ IP \_ TCP**</span><span class="sxs-lookup"><span data-stu-id="a59ac-145">**ncacn\_ip\_tcp**</span></span>](ncacn-ip-tcp.md)
</dt> <dt>

[<span data-ttu-id="a59ac-146">**нкакн \_ NetBIOS- \_ IPX**</span><span class="sxs-lookup"><span data-stu-id="a59ac-146">**ncacn\_nb\_ipx**</span></span>](ncacn-nb-ipx.md)
</dt> <dt>

[<span data-ttu-id="a59ac-147">**нкакн \_ SPX**</span><span class="sxs-lookup"><span data-stu-id="a59ac-147">**ncacn\_spx**</span></span>](ncacn-spx.md)
</dt> <dt>

[<span data-ttu-id="a59ac-148">**нкакн \_ имена \_ NetBIOS**</span><span class="sxs-lookup"><span data-stu-id="a59ac-148">**ncacn\_nb\_nb**</span></span>](ncacn-nb-nb.md)
</dt> <dt>

[<span data-ttu-id="a59ac-149">**нкакн \_ NetBIOS, \_ протокол TCP**</span><span class="sxs-lookup"><span data-stu-id="a59ac-149">**ncacn\_nb\_tcp**</span></span>](ncacn-nb-tcp.md)
</dt> <dt>

[<span data-ttu-id="a59ac-150">**нкакн \_ NP**</span><span class="sxs-lookup"><span data-stu-id="a59ac-150">**ncacn\_np**</span></span>](ncacn-np.md)
</dt> <dt>

[<span data-ttu-id="a59ac-151">**нкакн \_ ВНС \_ SPP**</span><span class="sxs-lookup"><span data-stu-id="a59ac-151">**ncacn\_vns\_spp**</span></span>](ncacn-vns-spp.md)
</dt> <dt>

[<span data-ttu-id="a59ac-152">**нкалрпк**</span><span class="sxs-lookup"><span data-stu-id="a59ac-152">**ncalrpc**</span></span>](ncalrpc.md)
</dt> <dt>

[<span data-ttu-id="a59ac-153">**нкадг \_ IP \_ UDP**</span><span class="sxs-lookup"><span data-stu-id="a59ac-153">**ncadg\_ip\_udp**</span></span>](ncadg-ip-udp.md)
</dt> <dt>

[<span data-ttu-id="a59ac-154">Строковая привязка</span><span class="sxs-lookup"><span data-stu-id="a59ac-154">string binding</span></span>](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 