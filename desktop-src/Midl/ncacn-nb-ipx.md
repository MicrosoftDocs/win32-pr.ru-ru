---
title: атрибут ncacn_nb_ipx
description: '\_ \_ Ключевое слово нкакн NetBIOS IPX определяет NetBIOS через IPX в качестве семейства протоколов для конечной точки. Это семейство протоколов устарело и не должно использоваться в новых приложениях.'
ms.assetid: 641471d4-eba4-4d4a-a3fe-1e40b3751e38
keywords:
- ncacn_nb_ipx атрибута MIDL
topic_type:
- apiref
api_name:
- ncacn_nb_ipx
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 156b5c460c4cc8638640e7eb3500ec9a7a9fa0b0
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "105650348"
---
# <a name="ncacn_nb_ipx-attribute"></a><span data-ttu-id="12dda-105">\_ \_ атрибут IPX нкакн NetBIOS</span><span class="sxs-lookup"><span data-stu-id="12dda-105">ncacn\_nb\_ipx attribute</span></span>

<span data-ttu-id="12dda-106">Ключевое слово **нкакн \_ NetBIOS \_ IPX** определяет NetBIOS через IPX в качестве семейства протоколов для конечной точки.</span><span class="sxs-lookup"><span data-stu-id="12dda-106">The **ncacn\_nb\_ipx** keyword identifies NetBIOS over IPX as the protocol family for the endpoint.</span></span> <span data-ttu-id="12dda-107">Это семейство протоколов устарело и не должно использоваться в новых приложениях.</span><span class="sxs-lookup"><span data-stu-id="12dda-107">This protocol family is obsolete and should not be used in new applications.</span></span>

``` syntax
endpoint("ncacn_nb_ipx:[port-name]")
```

## <a name="parameters"></a><span data-ttu-id="12dda-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="12dda-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12dda-109">*имя порта*</span><span class="sxs-lookup"><span data-stu-id="12dda-109">*port-name*</span></span> 
</dt> <dd>

<span data-ttu-id="12dda-110">Задает необязательное 8-разрядное значение в диапазоне от 1 до 254.</span><span class="sxs-lookup"><span data-stu-id="12dda-110">Specifies an optional 8-bit value ranging from 1 to 254.</span></span> <span data-ttu-id="12dda-111">Значения меньше 0x20 зарезервированы.</span><span class="sxs-lookup"><span data-stu-id="12dda-111">Values of less than 0x20 are reserved.</span></span> <span data-ttu-id="12dda-112">Если значение *имени порта* не указано, служба сопоставления конечных точек выбирает значение порта.</span><span class="sxs-lookup"><span data-stu-id="12dda-112">If the *port-name* value is not specified, the endpoint-mapping service selects the port value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="12dda-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="12dda-113">Remarks</span></span>

<span data-ttu-id="12dda-114">Синтаксис строки порта NetBIOS, как и все строки портов, определяется реализацией транспорта и не зависит от спецификации IDL.</span><span class="sxs-lookup"><span data-stu-id="12dda-114">The syntax of the NetBIOS port string, like all port strings, is defined by the transport implementation and is independent of the IDL specification.</span></span> <span data-ttu-id="12dda-115">Компилятор MIDL выполняет ограниченную проверку синтаксиса, но не гарантирует, что указана правильная спецификация конечной точки.</span><span class="sxs-lookup"><span data-stu-id="12dda-115">The MIDL compiler performs limited syntax checking but does not guarantee that the endpoint specification is correct.</span></span> <span data-ttu-id="12dda-116">Некоторые классы ошибок могут выводиться во время выполнения, а не во время компиляции.</span><span class="sxs-lookup"><span data-stu-id="12dda-116">Some classes of errors may be reported at run time rather than at compile time.</span></span>

> [!Note]  
> <span data-ttu-id="12dda-117">Это семейство протоколов не поддерживается в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="12dda-117">This protocol family is not supported in WindowsÂ XP.</span></span>

 

## <a name="examples"></a><span data-ttu-id="12dda-118">Примеры</span><span class="sxs-lookup"><span data-stu-id="12dda-118">Examples</span></span>

``` syntax
[
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncacn_nb_ipx:[100]") 
] 
interface iface
{
    // Interface definition statements.
}
```

## <a name="see-also"></a><span data-ttu-id="12dda-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="12dda-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12dda-120">**endpoint**</span><span class="sxs-lookup"><span data-stu-id="12dda-120">**endpoint**</span></span>](endpoint.md)
</dt> <dt>

[<span data-ttu-id="12dda-121">Файл определения интерфейса (IDL)</span><span class="sxs-lookup"><span data-stu-id="12dda-121">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="12dda-122">**нкакн \_ IP \_ TCP**</span><span class="sxs-lookup"><span data-stu-id="12dda-122">**ncacn\_ip\_tcp**</span></span>](ncacn-ip-tcp.md)
</dt> <dt>

[<span data-ttu-id="12dda-123">**нкакн \_ NetBIOS, \_ протокол TCP**</span><span class="sxs-lookup"><span data-stu-id="12dda-123">**ncacn\_nb\_tcp**</span></span>](ncacn-nb-tcp.md)
</dt> <dt>

[<span data-ttu-id="12dda-124">**нкакн \_ имена \_ NetBIOS**</span><span class="sxs-lookup"><span data-stu-id="12dda-124">**ncacn\_nb\_nb**</span></span>](ncacn-nb-nb.md)
</dt> <dt>

[<span data-ttu-id="12dda-125">**нкакн \_ в \_ DSP**</span><span class="sxs-lookup"><span data-stu-id="12dda-125">**ncacn\_at\_dsp**</span></span>](ncacn-at-dsp.md)
</dt> <dt>

[<span data-ttu-id="12dda-126">**нкакн \_ SPX**</span><span class="sxs-lookup"><span data-stu-id="12dda-126">**ncacn\_spx**</span></span>](ncacn-spx.md)
</dt> <dt>

[<span data-ttu-id="12dda-127">**нкакн \_ NP**</span><span class="sxs-lookup"><span data-stu-id="12dda-127">**ncacn\_np**</span></span>](ncacn-np.md)
</dt> <dt>

[<span data-ttu-id="12dda-128">**нкалрпк**</span><span class="sxs-lookup"><span data-stu-id="12dda-128">**ncalrpc**</span></span>](ncalrpc.md)
</dt> <dt>

[<span data-ttu-id="12dda-129">**нкадг \_ IP \_ UDP**</span><span class="sxs-lookup"><span data-stu-id="12dda-129">**ncadg\_ip\_udp**</span></span>](ncadg-ip-udp.md)
</dt> <dt>

[<span data-ttu-id="12dda-130">**нкадг \_ IPX**</span><span class="sxs-lookup"><span data-stu-id="12dda-130">**ncadg\_ipx**</span></span>](ncadg-ipx.md)
</dt> <dt>

[<span data-ttu-id="12dda-131">**Строковая привязка**</span><span class="sxs-lookup"><span data-stu-id="12dda-131">**string binding**</span></span>](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 