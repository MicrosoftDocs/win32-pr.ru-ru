---
title: API сервера DVC
description: Динамические API сервера виртуальных каналов (DVC) реализуются с помощью сервера подключение к удаленному рабочему столу (RDC) подключения.
ms.assetid: 9743ce32-9262-4af3-b013-668e834e279c
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3bc413cb6bc60f5b6a16f282fe3d4d1aa830272
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413534"
---
# <a name="dvc-server-apis"></a><span data-ttu-id="50716-103">API сервера DVC</span><span class="sxs-lookup"><span data-stu-id="50716-103">DVC Server APIs</span></span>

<span data-ttu-id="50716-104">Динамические API сервера виртуальных каналов (DVC) реализуются с помощью сервера подключение к удаленному рабочему столу (RDC) подключения.</span><span class="sxs-lookup"><span data-stu-id="50716-104">The dynamic virtual channel (DVC) server APIs are implemented by the Remote Desktop Connection (RDC) server of the connection.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="50716-105">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="50716-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="50716-106">**ивтссерверчаннел**</span><span class="sxs-lookup"><span data-stu-id="50716-106">**IWTSServerChannel**</span></span>](iwtsserverchannel.md)
</dt> <dd>

<span data-ttu-id="50716-107">Этот интерфейс не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="50716-107">This interface is not supported.</span></span>

</dd> <dt>

[<span data-ttu-id="50716-108">**ивтссерверчаннелманажер**</span><span class="sxs-lookup"><span data-stu-id="50716-108">**IWTSServerChannelManager**</span></span>](iwtsserverchannelmanager.md)
</dt> <dd>

<span data-ttu-id="50716-109">Этот интерфейс не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="50716-109">This interface is not supported.</span></span>

</dd> <dt>

[<span data-ttu-id="50716-110">**тприорити**</span><span class="sxs-lookup"><span data-stu-id="50716-110">**TPriority**</span></span>](tpriority.md)
</dt> <dd>

<span data-ttu-id="50716-111">Это перечисление не используется.</span><span class="sxs-lookup"><span data-stu-id="50716-111">This enumeration is not used.</span></span>

</dd> </dl>

## <a name="changes-in-behavior-for-other-server-apis"></a><span data-ttu-id="50716-112">Изменения в поведении для других серверных API</span><span class="sxs-lookup"><span data-stu-id="50716-112">Changes in Behavior for Other Server APIs</span></span>

-   <span data-ttu-id="50716-113">API сервера был расширен с помощью дополнительного вызова, который открывает динамический виртуальный канал (DVC).</span><span class="sxs-lookup"><span data-stu-id="50716-113">The server API has been extended with an additional call which opens a dynamic virtual channel (DVC).</span></span> <span data-ttu-id="50716-114">Дополнительный вызов выполняется с помощью функции [**втсвиртуалчаннелопенекс**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopenex) .</span><span class="sxs-lookup"><span data-stu-id="50716-114">The additional call is made using the [**WTSVirtualChannelOpenEx**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopenex) function.</span></span>
-   [<span data-ttu-id="50716-115">**втсвиртуалчаннелреад**</span><span class="sxs-lookup"><span data-stu-id="50716-115">**WTSVirtualChannelRead**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelread)

    <span data-ttu-id="50716-116">При использовании этого API с DVC всегда будет находиться в начале данных, считываемых с [**помощью \_ \_ заголовка канала PDU**](/windows/win32/api/pchannel/ns-pchannel-channel_pdu_header).</span><span class="sxs-lookup"><span data-stu-id="50716-116">When using this API with DVC, it will always prepend the data read with [**CHANNEL\_PDU\_HEADER**](/windows/win32/api/pchannel/ns-pchannel-channel_pdu_header).</span></span> <span data-ttu-id="50716-117">Это означает, что все считывание должно выполняться по крайней мере в блоке данных **\_ \_ длины канала PDU** , переданном в качестве входного буфера.</span><span class="sxs-lookup"><span data-stu-id="50716-117">This means that any read must be done with at least the **CHANNEL\_PDU\_LENGTH** data block passed as the input buffer.</span></span>

-   [<span data-ttu-id="50716-118">**ReadFile**</span><span class="sxs-lookup"><span data-stu-id="50716-118">**ReadFile**</span></span>](/windows/desktop/api/fileapi/nf-fileapi-readfile)

    <span data-ttu-id="50716-119">Если файловый обработчик для DVC извлекается путем вызова [**втсвиртуалчаннелкуери**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelquery) с параметром *втсвиртуалфилехандле*, будет применяться то же правило.</span><span class="sxs-lookup"><span data-stu-id="50716-119">If the file handle to the DVC is retrieved by calling [**WTSVirtualChannelQuery**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelquery) with parameter *WTSVirtualFileHandle*, the same rule will apply.</span></span> <span data-ttu-id="50716-120">Все операции чтения будут содержать [**\_ \_ заголовок PDU канала**](/windows/win32/api/pchannel/ns-pchannel-channel_pdu_header), а буфер чтения должен быть по крайней мере **размером \_ PDU \_ канала** .</span><span class="sxs-lookup"><span data-stu-id="50716-120">All reads will include the [**CHANNEL\_PDU\_HEADER**](/windows/win32/api/pchannel/ns-pchannel-channel_pdu_header), and the read buffer has to be at least **CHANNEL\_PDU\_LENGTH** size.</span></span>

 

 