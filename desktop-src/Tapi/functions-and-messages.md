---
description: Функция ФонедевспеЦифик и связанное с ней \_ сообщение девспеЦифик для телефона позволяют приложению получить доступ к функциям телефона для конкретного устройства, которые недоступны через общие службы телефонии для телефонов.
ms.assetid: b4c8d721-26e4-4895-9f09-0f67fe4d346b
title: Функции и сообщения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 292f85e2ea57ac11da8150d4d0a183c7c4fd2c88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998475"
---
# <a name="functions-and-messages"></a><span data-ttu-id="603e7-103">Функции и сообщения</span><span class="sxs-lookup"><span data-stu-id="603e7-103">Functions and Messages</span></span>

<span data-ttu-id="603e7-104">Функция [**фонедевспеЦифик**](/windows/desktop/api/Tapi/nf-tapi-phonedevspecific) и связанное с ней сообщение [**\_ девспеЦифик для телефона**](phone-devspecific.md) позволяют приложению получить доступ к функциям телефона для конкретного устройства, которые недоступны через общие службы телефонии для телефонов.</span><span class="sxs-lookup"><span data-stu-id="603e7-104">The [**phoneDevSpecific**](/windows/desktop/api/Tapi/nf-tapi-phonedevspecific) function and its associated [**PHONE\_DEVSPECIFIC**](phone-devspecific.md) message enable an application to access device-specific phone features that are unavailable through the common telephony services for phones.</span></span> <span data-ttu-id="603e7-105">Иными словами, **фонедевспеЦифик** — это функция экранирования для конкретного устройства, которая обеспечивает зависящие от поставщика расширения, а Phone \_ девспеЦифик — сообщение для конкретного устройства, которое отправляется в приложение.</span><span class="sxs-lookup"><span data-stu-id="603e7-105">In other words, **phoneDevSpecific** is the device-specific escape function that allows vendor-dependent extensions, and PHONE\_DEVSPECIFIC is the device-specific message that is sent to the application.</span></span>

<span data-ttu-id="603e7-106">Профиль параметров функции [**фонедевспеЦифик**](/windows/desktop/api/Tapi/nf-tapi-phonedevspecific) является универсальным в этой незначительной интерпретации параметров с помощью TAPI.</span><span class="sxs-lookup"><span data-stu-id="603e7-106">The parameter profile of the [**phoneDevSpecific**](/windows/desktop/api/Tapi/nf-tapi-phonedevspecific) function is generic in that little interpretation of the parameters is made by TAPI.</span></span> <span data-ttu-id="603e7-107">Вместо этого интерпретация параметров определяется поставщиком услуг и должна быть понята приложению, которое их использует.</span><span class="sxs-lookup"><span data-stu-id="603e7-107">Rather, the interpretation of the parameters is defined by the service provider and must be understood by an application that uses them.</span></span> <span data-ttu-id="603e7-108">Параметры просто передаются интерфейсом TAPI из приложения поставщику услуг.</span><span class="sxs-lookup"><span data-stu-id="603e7-108">The parameters are simply passed through by TAPI from the application to the service provider.</span></span> <span data-ttu-id="603e7-109">Приложение, которое использует расширения для конкретных устройств, обычно не работает с другими поставщиками служб, но приложения, написанные для общих телефонных служб телефонии, будут работать с расширенным поставщиком услуг.</span><span class="sxs-lookup"><span data-stu-id="603e7-109">An application that relies on device-specific extensions will usually not work with other service providers, but applications written to the common telephony phone services will work with the extended service provider.</span></span>

 

 



