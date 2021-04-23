---
title: атрибут ncadg_ip_udp
description: '\_ \_ Ключевое слово нкадг IP UDP определяет версию датаграммы TCP/IP в качестве семейства протоколов для конечной точки. Это семейство протоколов устарело и не должно использоваться в новых приложениях.'
ms.assetid: c9133fcc-6dc2-49da-9c6f-5ce3c51090d5
keywords:
- ncadg_ip_udp атрибута MIDL
topic_type:
- apiref
api_name:
- ncadg_ip_udp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 173ccd0b81eb5fa7d84a6fa4d2821162b852303d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104133763"
---
# <a name="ncadg_ip_udp-attribute"></a><span data-ttu-id="6073c-105">\_атрибут IP \_ UDP нкадг</span><span class="sxs-lookup"><span data-stu-id="6073c-105">ncadg\_ip\_udp attribute</span></span>

<span data-ttu-id="6073c-106">Ключевое слово **нкадг \_ IP \_ UDP** определяет версию ДАТАГРАММы TCP/IP в качестве семейства протоколов для конечной точки.</span><span class="sxs-lookup"><span data-stu-id="6073c-106">The **ncadg\_ip\_udp** keyword identifies the datagram version of TCP/IP as the protocol family for the endpoint.</span></span> <span data-ttu-id="6073c-107">Это семейство протоколов устарело и не должно использоваться в новых приложениях.</span><span class="sxs-lookup"><span data-stu-id="6073c-107">This protocol family is obsolete and should not be used in new applications.</span></span>

``` syntax
endpoint("ncadg_ip_udp:server-name[port-name]")
```

## <a name="parameters"></a><span data-ttu-id="6073c-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="6073c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6073c-109">*имя сервера*</span><span class="sxs-lookup"><span data-stu-id="6073c-109">*server-name*</span></span> 
</dt> <dd>

<span data-ttu-id="6073c-110">Указывает имя или адрес в Интернете для сервера или узла, компьютер.</span><span class="sxs-lookup"><span data-stu-id="6073c-110">Specifies the name or internet address for the server, or host, computer.</span></span> <span data-ttu-id="6073c-111">Имя является символьной строкой и может быть полным доменным именем.</span><span class="sxs-lookup"><span data-stu-id="6073c-111">The name is a character string and may be a fully qualified domain name.</span></span> <span data-ttu-id="6073c-112">Интернет-адрес представляет собой стандартную нотацию Интернета.</span><span class="sxs-lookup"><span data-stu-id="6073c-112">The internet address is a common internet address notation.</span></span>

</dd> <dt>

<span data-ttu-id="6073c-113">*имя порта*</span><span class="sxs-lookup"><span data-stu-id="6073c-113">*port-name*</span></span> 
</dt> <dd>

<span data-ttu-id="6073c-114">Указывает необязательное 16-разрядное число.</span><span class="sxs-lookup"><span data-stu-id="6073c-114">Specifies an optional 16-bit number.</span></span> <span data-ttu-id="6073c-115">Значения менее 1024 обычно зарезервированы.</span><span class="sxs-lookup"><span data-stu-id="6073c-115">Values of less than 1024 are usually reserved.</span></span> <span data-ttu-id="6073c-116">Если значение не указано, служба сопоставления конечных точек выбирает допустимое значение *имени порта* .</span><span class="sxs-lookup"><span data-stu-id="6073c-116">If no value is specified, the endpoint-mapping service selects a valid *port-name* value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6073c-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6073c-117">Remarks</span></span>

<span data-ttu-id="6073c-118">К протоколам датаграмм, [**нкадг \_ IPX**](ncadg-ipx.md) и **нкадг \_ IP \_ UDP** применяются следующие ограничения.</span><span class="sxs-lookup"><span data-stu-id="6073c-118">The following restrictions apply to the datagram protocols, [**ncadg\_ipx**](ncadg-ipx.md) and **ncadg\_ip\_udp**:</span></span>

-   <span data-ttu-id="6073c-119">Они не поддерживают обратные вызовы.</span><span class="sxs-lookup"><span data-stu-id="6073c-119">They do not support callbacks.</span></span> <span data-ttu-id="6073c-120">Все функции, использующие **\[** атрибут [**обратного вызова**](callback.md) , завершатся **\]** ошибкой.</span><span class="sxs-lookup"><span data-stu-id="6073c-120">Any functions using the **\[**[**callback**](callback.md)**\]** attribute will fail.</span></span>
-   <span data-ttu-id="6073c-121">Они не поддерживают использование конструктора типа [**канала**](pipe.md) .</span><span class="sxs-lookup"><span data-stu-id="6073c-121">They do not support use of the [**pipe**](pipe.md) type constructor.</span></span>

<span data-ttu-id="6073c-122">Синтаксис строки порта транспорта TCP/IP, как и все строки портов, определяется независимо от спецификации IDL.</span><span class="sxs-lookup"><span data-stu-id="6073c-122">The syntax of the TCP/IP transport port string, like all port strings, is defined independently of the IDL specification.</span></span> <span data-ttu-id="6073c-123">Компилятор выполняет некоторую проверку синтаксиса, но не гарантирует, что указана правильная спецификация конечной точки.</span><span class="sxs-lookup"><span data-stu-id="6073c-123">The compiler performs some syntax checking but does not guarantee that the endpoint specification is correct.</span></span> <span data-ttu-id="6073c-124">Некоторые ошибки могут выводиться во время выполнения, а не во время компиляции.</span><span class="sxs-lookup"><span data-stu-id="6073c-124">Some errors may be reported at run time rather than at compile time.</span></span>

## <a name="examples"></a><span data-ttu-id="6073c-125">Примеры</span><span class="sxs-lookup"><span data-stu-id="6073c-125">Examples</span></span>

``` syntax
[
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncadg_ip_udp:rainier[1404]") 
]
interface iface1
{
    // Interface definition statements.
}

[
    uuid(87654321-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncadg_ip_udp:128.10.2.30[1404]") 
]
interface iface2
{
    // Interface definition statements.
}
```

## <a name="see-also"></a><span data-ttu-id="6073c-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6073c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6073c-127">**endpoint**</span><span class="sxs-lookup"><span data-stu-id="6073c-127">**endpoint**</span></span>](endpoint.md)
</dt> <dt>

[<span data-ttu-id="6073c-128">Файл определения интерфейса (IDL)</span><span class="sxs-lookup"><span data-stu-id="6073c-128">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="6073c-129">**нкакн \_ в \_ DSP**</span><span class="sxs-lookup"><span data-stu-id="6073c-129">**ncacn\_at\_dsp**</span></span>](ncacn-at-dsp.md)
</dt> <dt>

[<span data-ttu-id="6073c-130">**нкакн \_ днет \_ NSP**</span><span class="sxs-lookup"><span data-stu-id="6073c-130">**ncacn\_dnet\_nsp**</span></span>](ncacn-dnet-nsp.md)
</dt> <dt>

[<span data-ttu-id="6073c-131">**нкакн \_ IP \_ TCP**</span><span class="sxs-lookup"><span data-stu-id="6073c-131">**ncacn\_ip\_tcp**</span></span>](ncacn-ip-tcp.md)
</dt> <dt>

[<span data-ttu-id="6073c-132">**нкакн \_ NetBIOS- \_ IPX**</span><span class="sxs-lookup"><span data-stu-id="6073c-132">**ncacn\_nb\_ipx**</span></span>](ncacn-nb-ipx.md)
</dt> <dt>

[<span data-ttu-id="6073c-133">**нкакн \_ SPX**</span><span class="sxs-lookup"><span data-stu-id="6073c-133">**ncacn\_spx**</span></span>](ncacn-spx.md)
</dt> <dt>

[<span data-ttu-id="6073c-134">**нкакн \_ имена \_ NetBIOS**</span><span class="sxs-lookup"><span data-stu-id="6073c-134">**ncacn\_nb\_nb**</span></span>](ncacn-nb-nb.md)
</dt> <dt>

[<span data-ttu-id="6073c-135">**нкакн \_ NetBIOS, \_ протокол TCP**</span><span class="sxs-lookup"><span data-stu-id="6073c-135">**ncacn\_nb\_tcp**</span></span>](ncacn-nb-tcp.md)
</dt> <dt>

[<span data-ttu-id="6073c-136">**нкакн \_ NP**</span><span class="sxs-lookup"><span data-stu-id="6073c-136">**ncacn\_np**</span></span>](ncacn-np.md)
</dt> <dt>

[<span data-ttu-id="6073c-137">**нкакн \_ ВНС \_ SPP**</span><span class="sxs-lookup"><span data-stu-id="6073c-137">**ncacn\_vns\_spp**</span></span>](ncacn-vns-spp.md)
</dt> <dt>

[<span data-ttu-id="6073c-138">**нкалрпк**</span><span class="sxs-lookup"><span data-stu-id="6073c-138">**ncalrpc**</span></span>](ncalrpc.md)
</dt> <dt>

[<span data-ttu-id="6073c-139">**нкадг \_ IPX**</span><span class="sxs-lookup"><span data-stu-id="6073c-139">**ncadg\_ipx**</span></span>](ncadg-ipx.md)
</dt> <dt>

[<span data-ttu-id="6073c-140">Строковая привязка</span><span class="sxs-lookup"><span data-stu-id="6073c-140">String Binding</span></span>](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 