---
title: атрибут ncacn_ip_tcp
description: '\_ \_ Ключевое слово нкакн IP TCP определяет TCP/IP как семейство протоколов для конечной точки.'
ms.assetid: 8142c667-9a5f-4066-a36d-1bb5ce551d21
keywords:
- ncacn_ip_tcp атрибута MIDL
topic_type:
- apiref
api_name:
- ncacn_ip_tcp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1adb57951e862ebcdfa6889aae170bfdf5a14f96
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "105650349"
---
# <a name="ncacn_ip_tcp-attribute"></a><span data-ttu-id="b750d-104">нкакн \_ IP- \_ атрибут TCP</span><span class="sxs-lookup"><span data-stu-id="b750d-104">ncacn\_ip\_tcp attribute</span></span>

<span data-ttu-id="b750d-105">Ключевое слово **нкакн \_ IP \_ TCP** определяет TCP/IP как семейство протоколов для конечной точки.</span><span class="sxs-lookup"><span data-stu-id="b750d-105">The **ncacn\_ip\_tcp** keyword identifies TCP/IP as the protocol family for the endpoint.</span></span>

``` syntax
endpoint("ncacn_ip_tcp:server-name[port-name]")
```

## <a name="parameters"></a><span data-ttu-id="b750d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b750d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b750d-107">*имя сервера*</span><span class="sxs-lookup"><span data-stu-id="b750d-107">*server-name*</span></span> 
</dt> <dd>

<span data-ttu-id="b750d-108">Указывает имя или адрес в Интернете для сервера или узла, компьютер.</span><span class="sxs-lookup"><span data-stu-id="b750d-108">Specifies the name or Internet address for the server, or host, computer.</span></span> <span data-ttu-id="b750d-109">Имя является символьной строкой.</span><span class="sxs-lookup"><span data-stu-id="b750d-109">The name is a character string.</span></span> <span data-ttu-id="b750d-110">Интернет-адрес представляет собой стандартную нотацию Интернета.</span><span class="sxs-lookup"><span data-stu-id="b750d-110">The Internet address is a common Internet address notation.</span></span>

</dd> <dt>

<span data-ttu-id="b750d-111">*имя порта*</span><span class="sxs-lookup"><span data-stu-id="b750d-111">*port-name*</span></span> 
</dt> <dd>

<span data-ttu-id="b750d-112">Указывает необязательное 16-разрядное число.</span><span class="sxs-lookup"><span data-stu-id="b750d-112">Specifies an optional 16-bit number.</span></span> <span data-ttu-id="b750d-113">Значения менее 1024 обычно зарезервированы.</span><span class="sxs-lookup"><span data-stu-id="b750d-113">Values of less than 1024 are usually reserved.</span></span> <span data-ttu-id="b750d-114">Если значение не указано, служба сопоставления конечных точек выбирает допустимое значение *имени порта* .</span><span class="sxs-lookup"><span data-stu-id="b750d-114">If no value is specified, the endpoint-mapping service selects a valid *port-name* value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b750d-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b750d-115">Remarks</span></span>

<span data-ttu-id="b750d-116">Синтаксис строки порта транспорта TCP/IP, как и все строки портов, определяется независимо от спецификации IDL.</span><span class="sxs-lookup"><span data-stu-id="b750d-116">The syntax of the TCP/IP transport port string, like all port strings, is defined independently of the IDL specification.</span></span> <span data-ttu-id="b750d-117">Компилятор выполняет некоторую проверку синтаксиса, но не гарантирует, что указана правильная спецификация конечной точки.</span><span class="sxs-lookup"><span data-stu-id="b750d-117">The compiler performs some syntax checking but does not guarantee that the endpoint specification is correct.</span></span> <span data-ttu-id="b750d-118">Некоторые ошибки могут выводиться во время выполнения, а не во время компиляции.</span><span class="sxs-lookup"><span data-stu-id="b750d-118">Some errors may be reported at run time rather than at compile time.</span></span>

## <a name="examples"></a><span data-ttu-id="b750d-119">Примеры</span><span class="sxs-lookup"><span data-stu-id="b750d-119">Examples</span></span>

``` syntax
[   
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncacn_ip_tcp:rainier[1404]") 
]
interface iface
{
    // Interface definition statements.
}

 
endpoint("ncacn_ip_tcp:128.10.2.30[1404]")
```

## <a name="see-also"></a><span data-ttu-id="b750d-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b750d-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b750d-121">**endpoint**</span><span class="sxs-lookup"><span data-stu-id="b750d-121">**endpoint**</span></span>](endpoint.md)
</dt> <dt>

[<span data-ttu-id="b750d-122">Файл определения интерфейса (IDL)</span><span class="sxs-lookup"><span data-stu-id="b750d-122">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="b750d-123">**нкакн \_ NetBIOS, \_ протокол TCP**</span><span class="sxs-lookup"><span data-stu-id="b750d-123">**ncacn\_nb\_tcp**</span></span>](ncacn-nb-tcp.md)
</dt> <dt>

[<span data-ttu-id="b750d-124">**нкакн \_ NP**</span><span class="sxs-lookup"><span data-stu-id="b750d-124">**ncacn\_np**</span></span>](ncacn-np.md)
</dt> <dt>

[<span data-ttu-id="b750d-125">**нкакн \_ SPX**</span><span class="sxs-lookup"><span data-stu-id="b750d-125">**ncacn\_spx**</span></span>](ncacn-spx.md)
</dt> <dt>

[<span data-ttu-id="b750d-126">**нкалрпк**</span><span class="sxs-lookup"><span data-stu-id="b750d-126">**ncalrpc**</span></span>](ncalrpc.md)
</dt> <dt>

[<span data-ttu-id="b750d-127">**Строковая привязка**</span><span class="sxs-lookup"><span data-stu-id="b750d-127">**string binding**</span></span>](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 