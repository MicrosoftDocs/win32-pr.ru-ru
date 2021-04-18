---
description: Класс устройств NDIS состоит из устройств, которые могут быть связаны с драйверами NDIS для управления доступом к носителю (MAC) для поддержки сетевых подключений. Доступ к этим устройствам осуществляется с помощью функций.
ms.assetid: 98cdd929-0bd7-4509-b2f5-4edd8d6a8080
title: адаптер
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a0be1a69f98f9a4ff8cdc2f8ea173b208c0011d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673381"
---
# <a name="ndis"></a><span data-ttu-id="4cc4d-104">адаптер</span><span class="sxs-lookup"><span data-stu-id="4cc4d-104">ndis</span></span>

<span data-ttu-id="4cc4d-105">Класс устройств NDIS состоит из устройств, которые могут быть связаны с драйверами NDIS для управления доступом к носителю (MAC) для поддержки сетевых подключений.</span><span class="sxs-lookup"><span data-stu-id="4cc4d-105">The ndis device class consists of devices that can be associated with network driver interface specification (NDIS) media access control (MAC) drivers to support network communications.</span></span> <span data-ttu-id="4cc4d-106">Доступ к этим устройствам осуществляется с помощью функций.</span><span class="sxs-lookup"><span data-stu-id="4cc4d-106">You access these devices by using functions.</span></span>

<span data-ttu-id="4cc4d-107">Функции [**линежетид**](/windows/desktop/api/Tapi/nf-tapi-linegetid) и [**фонежетид**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) заполняют структуру [**Варстринг**](/windows/desktop/api/Tapi/ns-tapi-varstring) , устанавливая элемент **двстрингформат** в \_ двоичное значение STRINGFORMAT и добавляя следующие дополнительные члены:</span><span class="sxs-lookup"><span data-stu-id="4cc4d-107">The [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) and [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) functions fill a [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) structure, setting the **dwStringFormat** member to the STRINGFORMAT\_BINARY value and appending these additional members:</span></span>

``` syntax
HANDLE  hDevice;          // NDIS connection identifier
CHAR    szDeviceType[1];  // name of device 
```

<span data-ttu-id="4cc4d-108">Член **хдевице** — это идентификатор для передачи компьютеру Mac, например асинхронный MAC-адрес для удаленного доступа к сети, чтобы связать сетевое подключение с вызовом или модемом.</span><span class="sxs-lookup"><span data-stu-id="4cc4d-108">The **hDevice** member is the identifier to pass to a MAC, such as the asynchronous MAC for dial-up networking, to associate a network connection with the call/modem connection.</span></span> <span data-ttu-id="4cc4d-109">Элемент **сздевицетипе** является строкой, завершающейся нулем, с указанием имени устройства, связанного с идентификатором.</span><span class="sxs-lookup"><span data-stu-id="4cc4d-109">The **szDeviceType** member is a null-terminated string specifying the name of the device associated with the identifier.</span></span>

 

 



