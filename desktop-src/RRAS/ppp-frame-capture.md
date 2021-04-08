---
title: Запись драйвера для захвата кадров PPP
description: В этом документе объясняется, как разработать драйвер, который может записывать кадры PPP в Windows Vista перед их сжатием или шифрованием в пути отправки или после распаковки или расшифровки в пути получения.
ms.assetid: 1b3fe1b8-2b11-4aed-98e1-464b8c0821ec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d592596674cd64af5122303afefcfc81026dad27
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/20/2020
ms.locfileid: "104069619"
---
# <a name="writing-a-driver-to-capture-ppp-frames"></a><span data-ttu-id="e6749-103">Запись драйвера для захвата кадров PPP</span><span class="sxs-lookup"><span data-stu-id="e6749-103">Writing a Driver to Capture PPP Frames</span></span>

<span data-ttu-id="e6749-104">При отправке кадров протокол PPP (PPP) через туннель PPTP с включенным шифрованием или через туннель протокола второго уровня (L2TP), использующий протокол IPSec для шифрования, стандартная служебная программа записи кадров PPP может записывать только кадры PPP, имеющие поле удостоверения зашифрованного протокола.</span><span class="sxs-lookup"><span data-stu-id="e6749-104">When Point-to-Point Protocol (PPP) frames are sent through a Point-to-Point Tunneling Protocol (PPTP) tunnel with encryption turned on, or through a Layer 2 Tunneling Protocol (L2TP) tunnel that uses IPSec for encryption, the typical PPP frame capture utility can only capture PPP frames that have an encrypted protocol identity field.</span></span> <span data-ttu-id="e6749-105">В этом документе объясняется, как разработать драйвер, который может записывать кадры PPP в Windows Vista перед их сжатием или шифрованием в пути отправки или после распаковки или расшифровки в пути получения.</span><span class="sxs-lookup"><span data-stu-id="e6749-105">This document explains how to develop a driver that can capture PPP frames in Windows Vista before they are compressed/encrypted in the send path or after they are decompressed/decrypted in the receive path.</span></span>

1.  <span data-ttu-id="e6749-106">Напишите драйвер протокола NDIS.</span><span class="sxs-lookup"><span data-stu-id="e6749-106">Write an NDIS protocol driver.</span></span> <span data-ttu-id="e6749-107">Дополнительные сведения см. в разделе [драйверы протокола ndis 6,0](https://msdn.microsoft.com/library/ms795570.aspx) или [драйверы протокола ndis (NDIS 5,1)](https://msdn.microsoft.com/library/ms801145.aspx).</span><span class="sxs-lookup"><span data-stu-id="e6749-107">For details, see [NDIS 6.0 Protocol Drivers](https://msdn.microsoft.com/library/ms795570.aspx) or [NDIS Protocol Drivers (NDIS 5.1)](https://msdn.microsoft.com/library/ms801145.aspx).</span></span>
2.  <span data-ttu-id="e6749-108">Установите драйвер с удостоверением "MS \_ Netmon".</span><span class="sxs-lookup"><span data-stu-id="e6749-108">Install the driver with a hardware identity of "ms\_netmon".</span></span> <span data-ttu-id="e6749-109">Подробные инструкции по установке драйвера с указанным удостоверением оборудования см. в [разделе "модели INF](https://msdn.microsoft.com/library/ms794357.aspx)".</span><span class="sxs-lookup"><span data-stu-id="e6749-109">For detailed instructions on how to install the driver with a specific hardware identity, see [INF Models Section](https://msdn.microsoft.com/library/ms794357.aspx).</span></span>
    > [!Note]  
    > <span data-ttu-id="e6749-110">Каждый компьютер с Windows Vista допускает установку только одной сущности драйвера с удостоверением "MS \_ Netmon".</span><span class="sxs-lookup"><span data-stu-id="e6749-110">Each Windows Vista machine permits the installation of only one driver entity that has the "ms\_netmon" hardware identity.</span></span> <span data-ttu-id="e6749-111">Чтобы установить другой драйвер с этим удостоверением, необходимо удалить первый драйвер.</span><span class="sxs-lookup"><span data-stu-id="e6749-111">To install another driver with this identity, the first driver must be uninstalled.</span></span> <span data-ttu-id="e6749-112">Драйвер, установленный без использования удостоверения оборудования "MS \_ Netmon", не может выполнить привязку, необходимую для записи кадров PPP.</span><span class="sxs-lookup"><span data-stu-id="e6749-112">A driver that is installed without using the "ms\_netmon" hardware identity cannot perform the binding needed to capture PPP frames.</span></span>

     

3.  <span data-ttu-id="e6749-113">Драйвер протокола должен указать "ндисванбх" в качестве интерфейса привязки для захвата кадров PPP.</span><span class="sxs-lookup"><span data-stu-id="e6749-113">The protocol driver should specify "ndiswanbh" as the binding interface for capturing PPP frames.</span></span> <span data-ttu-id="e6749-114">Подробные инструкции см. в разделе [Указание интерфейсов привязки](https://msdn.microsoft.com/library/aa937923.aspx).</span><span class="sxs-lookup"><span data-stu-id="e6749-114">For detailed instructions, see [Specifying Binding Interfaces](https://msdn.microsoft.com/library/aa937923.aspx).</span></span>
4.  <span data-ttu-id="e6749-115">Реализация [протоколбиндадаптер](https://msdn.microsoft.com/library/ms797311.aspx) в драйвере должна поддерживать "ндисмедиумван" как часть среднего массива, чтобы он мог открыть ребро мини-порта ндисванбх с помощью функции [ндисопенадаптер](https://msdn.microsoft.com/library/ms804862.aspx) .</span><span class="sxs-lookup"><span data-stu-id="e6749-115">The [ProtocolBindAdapter](https://msdn.microsoft.com/library/ms797311.aspx) implementation in the driver should support "NdisMediumWan" as a part of the medium array, so that it can open the ndiswanbh miniport edge using the [NdisOpenAdapter](https://msdn.microsoft.com/library/ms804862.aspx) function.</span></span>
5.  <span data-ttu-id="e6749-116">Если функция [протоколопенадаптеркомплете](https://msdn.microsoft.com/library/ms797287.aspx) вызывается со статусом состояние \_ NDIS \_ успешно, драйвер протокола должен установить идентификатор объекта OID для [ \_ \_ текущего \_ \_ фильтра пакетов](https://msdn.microsoft.com/library/bb314089.aspx) с [ \_ \_ \_ неизбирательными](https://msdn.microsoft.com/library/bb314089.aspx) флагами NDIS и [ \_ типом пакета NDIS для \_ \_ \_ локальной](https://msdn.microsoft.com/library/bb314089.aspx) привязки.</span><span class="sxs-lookup"><span data-stu-id="e6749-116">If the [ProtocolOpenAdapterComplete](https://msdn.microsoft.com/library/ms797287.aspx) function is called with status NDIS\_STATUS\_SUCCESS, the protocol driver should set the [OID\_GEN\_CURRENT\_PACKET\_FILTER](https://msdn.microsoft.com/library/bb314089.aspx) OID with the flags [NDIS\_PACKET\_TYPE\_PROMISCUOUS](https://msdn.microsoft.com/library/bb314089.aspx) and [NDIS\_PACKET\_TYPE\_ALL\_LOCAL](https://msdn.microsoft.com/library/bb314089.aspx) over this binding.</span></span> <span data-ttu-id="e6749-117">После этого драйвер протокола получит расшифрованные кадры PPP из уровня кадрирования PPP в своей функции [протоколрецеиве](https://msdn.microsoft.com/library/ms797274.aspx) .</span><span class="sxs-lookup"><span data-stu-id="e6749-117">Once this is done, the protocol driver will receive the decrypted PPP frames from the PPP framing layer in its [ProtocolReceive](https://msdn.microsoft.com/library/ms797274.aspx) function.</span></span>

> [!Note]  
> <span data-ttu-id="e6749-118">Эта информация относится только к драйверам на компьютере с Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e6749-118">This information only applies to drivers on a Windows Vista machine.</span></span>

 

 

 




