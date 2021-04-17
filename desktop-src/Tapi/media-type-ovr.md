---
description: Тип носителя (или режим) устройства описывает тип данных, которые могут быть заменены, например интерактивный речевой ввод. Данное устройство может обрабатывать только один тип носителя или может работать с диапазоном типов.
ms.assetid: fccf85e9-3889-4ebc-b1bf-a60e27ab4586
title: Тип носителя
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 369954a4b0d1f78e12f6ea42bcc2ec61ca425012
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105674537"
---
# <a name="media-type"></a><span data-ttu-id="cc9e3-104">Тип носителя</span><span class="sxs-lookup"><span data-stu-id="cc9e3-104">Media Type</span></span>

<span data-ttu-id="cc9e3-105">*Тип носителя* (или режим) устройства описывает тип данных, которые могут быть заменены, например интерактивный речевой ввод.</span><span class="sxs-lookup"><span data-stu-id="cc9e3-105">The *media type* (or mode) of a device describes the type of information that can be exchanged, such as interactive voice.</span></span> <span data-ttu-id="cc9e3-106">Данное устройство может обрабатывать только один тип носителя или может работать с диапазоном типов.</span><span class="sxs-lookup"><span data-stu-id="cc9e3-106">A given device might be able to handle only one media type, or it might be able to deal with a range of types.</span></span>

<span data-ttu-id="cc9e3-107">Поставщики услуг предоставляют тип или типы носителей, поддерживаемые устройствами, которыми они управляют.</span><span class="sxs-lookup"><span data-stu-id="cc9e3-107">Service providers expose the media type or types supported by the devices they control.</span></span> <span data-ttu-id="cc9e3-108">Приложение запрашивает тип мультимедиа, а затем использует эти сведения для выбора подходящего адреса для инициации сеанса.</span><span class="sxs-lookup"><span data-stu-id="cc9e3-108">Applications query for media type and then use this information to select an appropriate address on which to initiate a session.</span></span> <span data-ttu-id="cc9e3-109">Ответ приложения на предложенный сеанс можно также запредикатировать на типе носителя.</span><span class="sxs-lookup"><span data-stu-id="cc9e3-109">Application response to a session offered may also be predicated on media type.</span></span>

<span data-ttu-id="cc9e3-110">Данный сеанс связи или вызов может затрагивать несколько типов носителей.</span><span class="sxs-lookup"><span data-stu-id="cc9e3-110">A given communications session, or call, can involve several media types.</span></span> <span data-ttu-id="cc9e3-111">Дополнительные сведения см. в разделе Тип носителя для сеанса.</span><span class="sxs-lookup"><span data-stu-id="cc9e3-111">For further information, see Media type for a session.</span></span>

<span data-ttu-id="cc9e3-112">**Интерфейс TAPI 2. x:** См. раздел [**линежетаддресскапс**](/windows/win32/api/tapi/nf-tapi-linegetaddresscaps), **Дваваилаблемедиамодес** member структуры [**Линеаддресскапс**](/windows/win32/api/tapi/ns-tapi-lineaddresscaps) , на который указывает *лпаддресскапс*, [линемедиамоде \_ константы](./linemediamode--constants.md).</span><span class="sxs-lookup"><span data-stu-id="cc9e3-112">**TAPI 2.x:** See [**lineGetAddressCaps**](/windows/win32/api/tapi/nf-tapi-linegetaddresscaps), **dwAvailableMediaModes** member of [**LINEADDRESSCAPS**](/windows/win32/api/tapi/ns-tapi-lineaddresscaps) structure pointed to by *lpAddressCaps*, [LINEMEDIAMODE\_ Constants](./linemediamode--constants.md).</span></span>

<span data-ttu-id="cc9e3-113">**Интерфейс TAPI 3. x:** См. раздел [**иттерминал:: Get \_ mediaType**](/windows/win32/api/tapi3if/nf-tapi3if-itterminal-get_mediatype), [ \_ константы тапимедиатипе](tapimediatype--constants.md).</span><span class="sxs-lookup"><span data-stu-id="cc9e3-113">**TAPI 3.x:** See [**ITTerminal::get\_MediaType**](/windows/win32/api/tapi3if/nf-tapi3if-itterminal-get_mediatype), [TAPIMEDIATYPE\_ Constants](tapimediatype--constants.md).</span></span>
