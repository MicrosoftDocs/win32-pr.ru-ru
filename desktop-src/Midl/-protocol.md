---
title: /Протокол, параметр
description: Параметр/Протокол указывает, какой протокол связи поддерживается созданной заглушкой.
ms.assetid: b565b30c-72e5-442b-9588-324b9041524b
keywords:
- MIDL/протокол Switch
topic_type:
- apiref
api_name:
- /protocol
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9770fa94d010e21dcbd2a5574a0cffe29273a23
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104334659"
---
# <a name="protocol-switch"></a><span data-ttu-id="46dfa-104">/Протокол, параметр</span><span class="sxs-lookup"><span data-stu-id="46dfa-104">/protocol switch</span></span>

<span data-ttu-id="46dfa-105">Параметр **/протокол** указывает, какой протокол связи поддерживается созданной заглушкой.</span><span class="sxs-lookup"><span data-stu-id="46dfa-105">The **/protocol** switch specifies which wire protocol is supported by the generated stub.</span></span>

``` syntax
midl /protocol (dce | ndr64 | all)
```

## <a name="switch-options"></a><span data-ttu-id="46dfa-106">Параметры коммутатора</span><span class="sxs-lookup"><span data-stu-id="46dfa-106">Switch Options</span></span>

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="dce"></span><span id="DCE"></span>

<span data-ttu-id="46dfa-107"><span id="dce"></span><span id="DCE"></span>DCE \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="46dfa-107"><span id="dce"></span><span id="DCE"></span>\*\*\*\*dce\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="46dfa-108">Созданная заглушка поддерживает только протокол DCE.</span><span class="sxs-lookup"><span data-stu-id="46dfa-108">The generated stub supports DCE protocol only.</span></span>

</dd> <dt>

<span id="ndr64"></span><span id="NDR64"></span>

<span data-ttu-id="46dfa-109"><span id="ndr64"></span><span id="NDR64"></span>ndr64\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="46dfa-109"><span id="ndr64"></span><span id="NDR64"></span>\*\*\*\*ndr64\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="46dfa-110">Созданная заглушка поддерживает только протокол Microsoft NDR64.</span><span class="sxs-lookup"><span data-stu-id="46dfa-110">The generated stub supports Microsoft NDR64 protocol only.</span></span>

</dd> <dt>

<span id="all"></span><span id="ALL"></span>

<span data-ttu-id="46dfa-111"><span id="all"></span><span id="ALL"></span>все \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="46dfa-111"><span id="all"></span><span id="ALL"></span>\*\*\*\*all\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="46dfa-112">Созданная заглушка поддерживает все доступные протоколы для данной среды.</span><span class="sxs-lookup"><span data-stu-id="46dfa-112">The generated stub supports all available protocols for a given environment.</span></span>

</dd> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="46dfa-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="46dfa-113">Remarks</span></span>

<span data-ttu-id="46dfa-114">RPC маршалирует и расмаршалирует данные в соответствии с определенным протоколом передачи, который также называется синтаксисом перемещения, который определяет представление сети данных, например порядок, в котором выполняется маршалирование элементов данных, выравнивание данных по каналу, дополнительные сведения, включенные в данные, а также другие.</span><span class="sxs-lookup"><span data-stu-id="46dfa-114">RPC marshals and unmarshals data according to a strict wire protocol, also called transfer syntax, that defines data wire representation such as the order in which data members are marshaled, the alignment of data on the wire, additional information included with the data, among others.</span></span> <span data-ttu-id="46dfa-115">Microsoft RPC совместим с протоколом NDR использование DCE (представление данных сети).</span><span class="sxs-lookup"><span data-stu-id="46dfa-115">Microsoft RPC is compatible with OSF DCE's NDR (network data representation) protocol.</span></span> <span data-ttu-id="46dfa-116">В 64-разрядном выпуске Windows XP корпорация Майкрософт представляет экспериментальный протокол NDR64, оптимизированный для передачи 64-разрядных данных.</span><span class="sxs-lookup"><span data-stu-id="46dfa-116">In the 64-bit release of Windows XP, Microsoft introduces an experimental protocol NDR64 that is optimized for transferring 64-bit data.</span></span> <span data-ttu-id="46dfa-117">NDR64 не поддерживает обратную совместимость с протоколом DCE.</span><span class="sxs-lookup"><span data-stu-id="46dfa-117">NDR64 is not backward compatible with the DCE protocol.</span></span>

<span data-ttu-id="46dfa-118">Протокол **DCE** совместим с СИНТАКСИСОМ использование DCE для преобразования NDR.</span><span class="sxs-lookup"><span data-stu-id="46dfa-118">The **dce** protocol is compatible with OSF DCE's NDR transfer syntax.</span></span> <span data-ttu-id="46dfa-119">Этот протокол оптимизирован для передачи 32-разрядных данных.</span><span class="sxs-lookup"><span data-stu-id="46dfa-119">This protocol is optimized for transferring 32-bit data.</span></span>

<span data-ttu-id="46dfa-120">В настоящее время протокол **ndr64** поддерживается только при использовании в сочетании с параметром [**/Win64**](-win64.md) .</span><span class="sxs-lookup"><span data-stu-id="46dfa-120">The **ndr64** protocol is currently supported only when used in conjunction with the [**/win64**](-win64.md) switch.</span></span> <span data-ttu-id="46dfa-121">Если клиент ndr64 пытается подключиться к серверу только DCE (или наоборот), вызов отклоняется с помощью RPC S, не \_ \_ поддерживаемого через \_ \_ SYN.</span><span class="sxs-lookup"><span data-stu-id="46dfa-121">If a ndr64 only client tries to connect to a dce-only server, or vice versa, the call is rejected with RPC\_S\_UNSUPPORTED\_TRANS\_SYN.</span></span>

<span data-ttu-id="46dfa-122">Параметр **ALL** создает заглушку, которая может использовать любой доступный протокол.</span><span class="sxs-lookup"><span data-stu-id="46dfa-122">The **all** option creates a stub that may use any available protocol.</span></span> <span data-ttu-id="46dfa-123">Для 32-разрядных заглушек единственным доступным протоколом является DCE.</span><span class="sxs-lookup"><span data-stu-id="46dfa-123">For 32-bit stubs, the only protocol currently available is DCE.</span></span> <span data-ttu-id="46dfa-124">Для 64-разрядных заглушек, созданных с помощью параметра [**/Win64**](-win64.md) , доступны как устройства DCE, так и NDR64.</span><span class="sxs-lookup"><span data-stu-id="46dfa-124">For 64-bit stubs, created using the [**/win64**](-win64.md) switch, both DCE and NDR64 are available.</span></span>

## <a name="examples"></a><span data-ttu-id="46dfa-125">Примеры</span><span class="sxs-lookup"><span data-stu-id="46dfa-125">Examples</span></span>

<span data-ttu-id="46dfa-126">**MIDL/протокол все/Win64 filename. idl**</span><span class="sxs-lookup"><span data-stu-id="46dfa-126">**midl /protocol all /win64 filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="46dfa-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="46dfa-127">See also</span></span>

<dl> <dt>

[**/<system>**](-system-.md)
</dt> </dl>

 

 




