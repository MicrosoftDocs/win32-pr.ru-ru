---
title: /префикс, параметр
description: Параметр/префикс направляет компилятор MIDL к добавлению строк префикса в имена клиента и (или) имени подпрограммы заглушки сервера.
ms.assetid: 5530e972-08bf-4cca-9bb4-9631db824bdb
keywords:
- MIDL/префикс Switch
topic_type:
- apiref
api_name:
- /prefix
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79885a57f257fe2648a27fd67a014421b2c1c13a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104532738"
---
# <a name="prefix-switch"></a><span data-ttu-id="ddce3-104">/префикс, параметр</span><span class="sxs-lookup"><span data-stu-id="ddce3-104">/prefix switch</span></span>

<span data-ttu-id="ddce3-105">Параметр **/префикс** направляет компилятор MIDL к добавлению строк префикса в имена клиента и (или) имени подпрограммы заглушки сервера.</span><span class="sxs-lookup"><span data-stu-id="ddce3-105">The **/prefix** switch directs the MIDL compiler to add prefix strings to the client and/or server stub routine names.</span></span> <span data-ttu-id="ddce3-106">Это можно использовать для того, чтобы одна программа была как клиентом, так и сервером того же интерфейса, без возникновения конфликта имен клиентских и серверных подпрограмм.</span><span class="sxs-lookup"><span data-stu-id="ddce3-106">This can be used to allow a single program to be both a client and server of the same interface, without having the client- and server-side routine names conflict with each other.</span></span>

``` syntax
midl /prefix { client | cstub | server | sstub | switch | all }
```

## <a name="switch-options"></a><span data-ttu-id="ddce3-107">Параметры коммутатора</span><span class="sxs-lookup"><span data-stu-id="ddce3-107">Switch Options</span></span>

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="client"></span><span id="CLIENT"></span>

<span data-ttu-id="ddce3-108"><span id="client"></span><span id="CLIENT"></span>Клиент \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="ddce3-108"><span id="client"></span><span id="CLIENT"></span>\*\*\*\*client\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="ddce3-109">Затрагивает только имена подпрограмм клиентской заглушки.</span><span class="sxs-lookup"><span data-stu-id="ddce3-109">Affects only the client stub routine names.</span></span>

</dd> <dt>

<span id="cstub"></span><span id="CSTUB"></span>

<span data-ttu-id="ddce3-110"><span id="cstub"></span><span id="CSTUB"></span>кстуб \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="ddce3-110"><span id="cstub"></span><span id="CSTUB"></span>\*\*\*\*cstub\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="ddce3-111">То же, что и *клиент*.</span><span class="sxs-lookup"><span data-stu-id="ddce3-111">Same as *client*.</span></span> <span data-ttu-id="ddce3-112">Затрагивает только имена подпрограмм клиентской заглушки.</span><span class="sxs-lookup"><span data-stu-id="ddce3-112">Affects only the client stub routine names.</span></span>

</dd> <dt>

<span id="server"></span><span id="SERVER"></span>

<span data-ttu-id="ddce3-113"><span id="server"></span><span id="SERVER"></span>сервер \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="ddce3-113"><span id="server"></span><span id="SERVER"></span>\*\*\*\*server\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="ddce3-114">Затрагивает только имена подпрограмм, вызванных подпрограммой заглушки сервера.</span><span class="sxs-lookup"><span data-stu-id="ddce3-114">Affects only the routine names called by the server stub routine.</span></span>

</dd> <dt>

<span id="sstub"></span><span id="SSTUB"></span>

<span data-ttu-id="ddce3-115"><span id="sstub"></span><span id="SSTUB"></span>сстуб \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="ddce3-115"><span id="sstub"></span><span id="SSTUB"></span>\*\*\*\*sstub\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="ddce3-116">То же, что и *сервер*.</span><span class="sxs-lookup"><span data-stu-id="ddce3-116">Same as *server*.</span></span> <span data-ttu-id="ddce3-117">Затрагивает только имена подпрограмм, вызванных подпрограммой заглушки сервера.</span><span class="sxs-lookup"><span data-stu-id="ddce3-117">Affects only the routine names called by the server stub routine.</span></span>

</dd> <dt>

<span id="switch"></span><span id="SWITCH"></span>

<span data-ttu-id="ddce3-118"><span id="switch"></span><span id="SWITCH"></span>Switch \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="ddce3-118"><span id="switch"></span><span id="SWITCH"></span>\*\*\*\*switch\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="ddce3-119">Влияет на дополнительный прототип, добавленный в файл заголовка.</span><span class="sxs-lookup"><span data-stu-id="ddce3-119">Affects an extra prototype added to the header file.</span></span>

</dd> <dt>

<span id="all"></span><span id="ALL"></span>

<span data-ttu-id="ddce3-120"><span id="all"></span><span id="ALL"></span>все \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="ddce3-120"><span id="all"></span><span id="ALL"></span>\*\*\*\*all\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="ddce3-121">Влияет на имена клиентской и серверной подпрограммы-заглушки.</span><span class="sxs-lookup"><span data-stu-id="ddce3-121">Affects both the client and server stub routine names.</span></span>

</dd> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ddce3-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ddce3-122">Remarks</span></span>

<span data-ttu-id="ddce3-123">Если префикс для клиентских подпрограмм отличается от префикса для подпрограмм на стороне сервера, созданный файл заголовка будет содержать как клиентские, так и прототипы подпрограмм на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="ddce3-123">If the prefix for the client-side routines is different from the prefix for the server-side routines, the generated header file will have both client-side routine prototypes and server-side routine prototypes.</span></span>

<span data-ttu-id="ddce3-124">Параметр **/префикс** полезен, если один файл заголовка будет использоваться с заглушками из нескольких запусков компилятора MIDL.</span><span class="sxs-lookup"><span data-stu-id="ddce3-124">The **/prefix** switch is useful when a single header file will be used with stubs from multiple runs of the MIDL compiler.</span></span> <span data-ttu-id="ddce3-125">Это приводит к вызову дополнительных прототипов подпрограмм в файле заголовка.</span><span class="sxs-lookup"><span data-stu-id="ddce3-125">This forces additional routine prototypes in the header file.</span></span>

<span data-ttu-id="ddce3-126">Во всех случаях префиксы "клиент", "сервер" и "переключить" будут переопределять все.</span><span class="sxs-lookup"><span data-stu-id="ddce3-126">In all cases, the client, server, and switch prefixes will override an all prefix.</span></span>

## <a name="examples"></a><span data-ttu-id="ddce3-127">Примеры</span><span class="sxs-lookup"><span data-stu-id="ddce3-127">Examples</span></span>

<span data-ttu-id="ddce3-128">**MIDL/префикс клиент "c \_ " сервер "s \_ "**</span><span class="sxs-lookup"><span data-stu-id="ddce3-128">**midl /prefix client "c\_" server "s\_"**</span></span>

<span data-ttu-id="ddce3-129">**MIDL/префикс все «мууу \_ »**</span><span class="sxs-lookup"><span data-stu-id="ddce3-129">**midl /prefix all "moo\_"**</span></span>

<span data-ttu-id="ddce3-130">**MIDL/префикс Client "лай \_ "**</span><span class="sxs-lookup"><span data-stu-id="ddce3-130">**midl /prefix client "bark\_"**</span></span>

## <a name="see-also"></a><span data-ttu-id="ddce3-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ddce3-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ddce3-132">Общий синтаксис командной строки MIDL</span><span class="sxs-lookup"><span data-stu-id="ddce3-132">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> </dl>

 

 




