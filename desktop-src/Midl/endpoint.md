---
title: Атрибут конечной точки
description: Атрибут \ Endpoint \ указывает хорошо известный порт или порты (конечные точки связи), на которых серверы интерфейса ожидают вызовов.
ms.assetid: b88c5a97-b726-43de-b5b6-649cda60c320
keywords:
- Атрибут конечной точки MIDL
topic_type:
- apiref
api_name:
- endpoint
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4383df496a791859f7249766f0dbb59266d28e93
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103890485"
---
# <a name="endpoint-attribute"></a><span data-ttu-id="dff43-104">Атрибут конечной точки</span><span class="sxs-lookup"><span data-stu-id="dff43-104">endpoint attribute</span></span>

<span data-ttu-id="dff43-105">Атрибут **\[ Endpoint \]** указывает хорошо известный порт или порты (конечные точки связи), на которых серверы интерфейса ожидают вызовов.</span><span class="sxs-lookup"><span data-stu-id="dff43-105">The **\[endpoint\]** attribute specifies a well-known port or ports (communication endpoints) on which servers of the interface listen for calls.</span></span>

``` syntax
endpoint("protocol-sequence:[endpoint-port]" [ , ...] )
```

## <a name="parameters"></a><span data-ttu-id="dff43-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="dff43-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dff43-107">*протокол — последовательность*</span><span class="sxs-lookup"><span data-stu-id="dff43-107">*protocol-sequence*</span></span> 
</dt> <dd>

<span data-ttu-id="dff43-108">Указывает строку символов, представляющую допустимые комбинации протокола RPC (например, "нкакн"), транспортного протокола (например, "TCP") и сетевого протокола (например, "IP").</span><span class="sxs-lookup"><span data-stu-id="dff43-108">Specifies a character string that represents a valid combination of an RPC protocol (such as "ncacn"), a transport protocol (such as "tcp"), and a network protocol (such as "ip").</span></span> <span data-ttu-id="dff43-109">Список допустимых последовательностей протоколов см. в разделе [константы последовательности протоколов](/windows/desktop/Rpc/protocol-sequence-constants).</span><span class="sxs-lookup"><span data-stu-id="dff43-109">For a list of valid protocol sequences, see [Protocol Sequence Constants](/windows/desktop/Rpc/protocol-sequence-constants).</span></span>

</dd> <dt>

<span data-ttu-id="dff43-110">*Порт конечной точки*</span><span class="sxs-lookup"><span data-stu-id="dff43-110">*endpoint-port*</span></span> 
</dt> <dd>

<span data-ttu-id="dff43-111">Задает строку, которая представляет обозначение конечной точки для указанного семейства протоколов.</span><span class="sxs-lookup"><span data-stu-id="dff43-111">Specifies a string that represents the endpoint designation for the specified protocol family.</span></span> <span data-ttu-id="dff43-112">Синтаксис строки порта зависит от каждой последовательности протоколов.</span><span class="sxs-lookup"><span data-stu-id="dff43-112">The syntax of the port string is specific to each protocol sequence.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dff43-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dff43-113">Remarks</span></span>

<span data-ttu-id="dff43-114">Атрибут **\[ Endpoint \]** указывает семейство транспортов, например протокол TCP/IP, ориентированный на соединение по протоколу NetBIOS или именованный протокол, ориентированный на подключение.</span><span class="sxs-lookup"><span data-stu-id="dff43-114">The **\[endpoint\]** attribute specifies a transport family such as the TCP/IP connection-oriented protocol, a NetBIOS connection-oriented protocol, or the named-pipe connection-oriented protocol.</span></span> <span data-ttu-id="dff43-115">Использование атрибута **\[ Endpoint \]** согласуется с другими методами добавления конечной точки и не предоставляет дополнительные или специальные службы для конечной точки; он просто предоставляет ярлык для вызова API.</span><span class="sxs-lookup"><span data-stu-id="dff43-115">Use of the **\[endpoint\]** attribute is consistent with other methods for adding an endpoint, and does not provide additional or special services for the endpoint; it simply provides a shortcut for calling the API.</span></span>

> [!Note]  
> <span data-ttu-id="dff43-116">Указание конечной точки в. Определение интерфейса IDL не ограничивает доступ к интерфейсу для указанной конечной точки.</span><span class="sxs-lookup"><span data-stu-id="dff43-116">Specifying an endpoint in the .IDL interface definition does not restrict access to the interface to the specified endpoint.</span></span> <span data-ttu-id="dff43-117">Добавление конечной точки в. Определение интерфейса IDL позволяет вызывать интерфейс через любую конечную точку в этом процессе и позволяет использовать конечную точку для вызова других интерфейсов в этом процессе.</span><span class="sxs-lookup"><span data-stu-id="dff43-117">Adding an endpoint to the .IDL interface definition allows the interface to be called through any endpoint in that process, and allows the endpoint to be used to call other interfaces in that process.</span></span>

 

<span data-ttu-id="dff43-118">Значение *последовательности протоколов* определяет допустимые значения для *порта конечной точки*.</span><span class="sxs-lookup"><span data-stu-id="dff43-118">The *protocol-sequence* value determines the valid values for the *endpoint-port*.</span></span> <span data-ttu-id="dff43-119">Компилятор MIDL проверяет только общий синтаксис для записи *порта конечной точки* .</span><span class="sxs-lookup"><span data-stu-id="dff43-119">The MIDL compiler checks only general syntax for the *endpoint-port* entry.</span></span> <span data-ttu-id="dff43-120">Ошибки спецификации порта выводятся библиотеками времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="dff43-120">Port specification errors are reported by the run-time libraries.</span></span> <span data-ttu-id="dff43-121">Сведения о допустимых значениях для каждой последовательности протоколов см. в разделе [константы последовательности протоколов](/windows/desktop/Rpc/protocol-sequence-constants).</span><span class="sxs-lookup"><span data-stu-id="dff43-121">For information about the allowed values for each protocol sequence, see the [Protocol Sequence Constants](/windows/desktop/Rpc/protocol-sequence-constants).</span></span>

<span data-ttu-id="dff43-122">Следующие последовательности протоколов, заданные DCE, не поддерживаются компилятором MIDL, который предоставляется с Microsoft RPC: **нкакн \_ OSI \_ ДНК** и **нкадг \_ DDS**.</span><span class="sxs-lookup"><span data-stu-id="dff43-122">The following protocol sequences specified by DCE are not supported by the MIDL compiler provided with Microsoft RPC: **ncacn\_osi\_dna** and **ncadg\_dds**.</span></span>

<span data-ttu-id="dff43-123">Убедитесь, что в конечных точках правильно заключены символы обратной косой черты.</span><span class="sxs-lookup"><span data-stu-id="dff43-123">Make sure that you correctly quote backslash characters in endpoints.</span></span> <span data-ttu-id="dff43-124">Эта ошибка обычно возникает, когда конечная точка является именованным каналом.</span><span class="sxs-lookup"><span data-stu-id="dff43-124">This error commonly occurs when the endpoint is a named pipe.</span></span>

<span data-ttu-id="dff43-125">Сведения о конечной точке, указанные в IDL-файле, используются функциями [**рпксерверусепротсекиф**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseprotseqif) и [**РПКСЕРВЕРУСЕАЛЛПРОТСЕКСИФ**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseallprotseqsif)среды выполнения RPC.</span><span class="sxs-lookup"><span data-stu-id="dff43-125">Endpoint information specified in the IDL file is used by the RPC run-time functions [**RpcServerUseProtseqIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseprotseqif) and [**RpcServerUseAllProtseqsIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseallprotseqsif).</span></span>

## <a name="examples"></a><span data-ttu-id="dff43-126">Примеры</span><span class="sxs-lookup"><span data-stu-id="dff43-126">Examples</span></span>

``` syntax
endpoint("ncacn_np:[\\pipe\\rainier]") 

endpoint("ncacn_ip_tcp:[1044]", "ncacn_np:[\\pipe\\shasta]")
```

## <a name="see-also"></a><span data-ttu-id="dff43-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dff43-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dff43-128">Файл определения интерфейса (IDL)</span><span class="sxs-lookup"><span data-stu-id="dff43-128">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="dff43-129">**рпксерверусеаллпротсексиф**</span><span class="sxs-lookup"><span data-stu-id="dff43-129">**RpcServerUseAllProtseqsIf**</span></span>](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseallprotseqsif)
</dt> <dt>

[<span data-ttu-id="dff43-130">**рпксерверусепротсекиф**</span><span class="sxs-lookup"><span data-stu-id="dff43-130">**RpcServerUseProtseqIf**</span></span>](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseprotseqif)
</dt> </dl>

 

 