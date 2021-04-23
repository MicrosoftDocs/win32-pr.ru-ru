---
description: Поставщики услуг, поддерживающие абстракцию внештатных данных (OOB) для сокетов в стиле потока, должны соответствовать семантике в этом разделе.
ms.assetid: 83ed881f-8474-445e-8fb5-9635138a63dd
title: Данные по внештатному каналу в SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab9808fa301073bcbb06be23a9487c2a1fa4f14d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072739"
---
# <a name="out-of-band-data-in-the-spi"></a><span data-ttu-id="da367-103">Данные по внештатному каналу в SPI</span><span class="sxs-lookup"><span data-stu-id="da367-103">Out-of-Band Data in the SPI</span></span>

<span data-ttu-id="da367-104">Поставщики услуг, поддерживающие абстракцию внештатных данных (OOB) для сокетов в стиле потока, должны соответствовать семантике в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="da367-104">The service providers which support the out-of-band data (OOB) abstraction for the stream-style sockets must adhere to the semantics in this section.</span></span> <span data-ttu-id="da367-105">Мы будем описывать обработку данных OOB с помощью независимого от протокола способа.</span><span class="sxs-lookup"><span data-stu-id="da367-105">We will describe OOB data handling in a protocol-independent manner.</span></span> <span data-ttu-id="da367-106">Сведения о данных OOB, реализованных с помощью срочных данных в поставщиках услуг TCP/IP, см. в этом [приложении](winsock-annexes.md) .</span><span class="sxs-lookup"><span data-stu-id="da367-106">Please refer to the [Winsock Annexes](winsock-annexes.md) for a discussion of OOB data implemented using urgent data in TCP/IP service providers.</span></span> <span data-ttu-id="da367-107">В следующем примере использование [**вспрекв**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) также применяется к [**вспреквфром**](/previous-versions/windows/desktop/legacy/ms742287(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="da367-107">In the following, the use of [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) also applies to [**WSPRecvFrom**](/previous-versions/windows/desktop/legacy/ms742287(v=vs.85)).</span></span>

 

 
