---
description: На следующей схеме показаны основные объекты, участвующие в элементах управления "хранилище больших двоичных объектов" в TAPI 3. Показанные интерфейсы связаны со ссылками на соответствующие страницы.
ms.assetid: 535bbb33-01cb-4484-b216-4808e47e4db5
title: Элементы управления BLOB-объектами конференций
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bacf13567abd46f56c399cefa732be97b081cfd3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542991"
---
# <a name="conference-blob-controls"></a><span data-ttu-id="e17cf-104">Элементы управления BLOB-объектами конференций</span><span class="sxs-lookup"><span data-stu-id="e17cf-104">Conference Blob Controls</span></span>

<span data-ttu-id="e17cf-105">\[ В Windows Vista, Windows Server 2008 и последующих версиях операционной системы нельзя использовать встречные средства и элементы управления Конференц-телефонией и интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="e17cf-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="e17cf-106">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="e17cf-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="e17cf-107">На следующей схеме показаны основные объекты, участвующие в элементах управления "хранилище больших двоичных объектов" в TAPI 3.</span><span class="sxs-lookup"><span data-stu-id="e17cf-107">The following diagram illustrates the main objects involved in TAPI 3 conference blob controls.</span></span> <span data-ttu-id="e17cf-108">Показанные интерфейсы связаны со ссылками на соответствующие страницы.</span><span class="sxs-lookup"><span data-stu-id="e17cf-108">Interfaces shown are hyperlinked into the relevant reference pages.</span></span>

![элементы управления и интерфейсы для конференций больших двоичных объектов](images/rendblob.png)

<span data-ttu-id="e17cf-110">Объект Conference BLOB содержит сведения об объекте Conference, относящиеся к конкретному поставщику.</span><span class="sxs-lookup"><span data-stu-id="e17cf-110">The conference blob contains provider-specific information on a conference object.</span></span> <span data-ttu-id="e17cf-111">Указатель на большой двоичный объект интерфейса [**итконференцеблоб**](itconferenceblob.md) получается путем выполнения QueryInterface на [**итдиректорйобжектконференце**](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectconference).</span><span class="sxs-lookup"><span data-stu-id="e17cf-111">A pointer to the [**ITConferenceBlob**](itconferenceblob.md) interface blob is obtained by doing a QueryInterface on [**ITDirectoryObjectConference**](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectconference).</span></span> <span data-ttu-id="e17cf-112">Интерфейс **итконференцеблоб** предоставляет методы для базовой обработки универсального большого двоичного объекта для конференций.</span><span class="sxs-lookup"><span data-stu-id="e17cf-112">The **ITConferenceBlob** interface provides methods for basic manipulation of a generic conference blob.</span></span> <span data-ttu-id="e17cf-113">Приложение, использующее односторонние объекты для конференций без SDP, должно реализовать собственные методы для обработки подробностей.</span><span class="sxs-lookup"><span data-stu-id="e17cf-113">An application using non-SDP conference blobs must implement its own methods for detail manipulation.</span></span>

<span data-ttu-id="e17cf-114">Встречно предоставляет интерфейс [**итсдп**](itsdp.md) для манипулирования объектами конференций SDP.</span><span class="sxs-lookup"><span data-stu-id="e17cf-114">Rendezvous provides the [**ITSdp**](itsdp.md) interface for manipulating SDP conference blobs.</span></span> <span data-ttu-id="e17cf-115">SDP — это протокол для описания сеансов мультимедиа и связанных с ними сведений о расписании.</span><span class="sxs-lookup"><span data-stu-id="e17cf-115">The SDP is a protocol for describing multimedia sessions and their related scheduling information.</span></span> <span data-ttu-id="e17cf-116">Дополнительные сведения о протоколе SDP см. в описании Internet Engineering Task Force (IETF) RFC 2327 с названием "SDP: сеанс описания сеанса".</span><span class="sxs-lookup"><span data-stu-id="e17cf-116">For additional information on the SDP protocol, locate Internet Engineering Task Force (IETF) RFC 2327 entitled "SDP: Session Description Protocol."</span></span> <span data-ttu-id="e17cf-117">Если для данного большого двоичного объекта конференции существует интерфейс **итсдп** , можно получить указатель на него, выполнив **QueryInterface** на [**итконференцеблоб**](itconferenceblob.md).</span><span class="sxs-lookup"><span data-stu-id="e17cf-117">If the **ITSDP** interface exists for a given conference blob, you can obtain a pointer to it by doing a **QueryInterface** on [**ITConferenceBlob**](itconferenceblob.md).</span></span>

<span data-ttu-id="e17cf-118">Для одностраничных BLOB-объектов SDP интерфейсы [**иттимеколлектион**](ittimecollection.md), [**иттиме**](ittime.md), [**итмедиаколлектион**](itmediacollection.md)и [**итмедиа**](itmedia.md) позволяют подробно управлять временем конференции SDP и характеристиками мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="e17cf-118">For SDP conference blobs, the [**ITTimeCollection**](ittimecollection.md), [**ITTime**](ittime.md), [**ITMediaCollection**](itmediacollection.md), and [**ITMedia**](itmedia.md) interfaces allow detailed control of SDP conference time and media characteristics.</span></span>

 

 



