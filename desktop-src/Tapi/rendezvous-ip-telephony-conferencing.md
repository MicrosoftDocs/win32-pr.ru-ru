---
description: Встречные элементы управления TAPI 3 позволяют программисту создавать приложения, которые могут создавать и обнаруживать многоадресные IP-конференции мультимедиа.
ms.assetid: 4da2046c-00fd-46a8-805f-503729cfa531
title: Встречные конференции с IP-телефонией
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d1cbfc3a1e07fdc245af0ae6b93277c90083a75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264468"
---
# <a name="rendezvous-ip-telephony-conferencing"></a><span data-ttu-id="26dbc-103">Встречные конференции с IP-телефонией</span><span class="sxs-lookup"><span data-stu-id="26dbc-103">Rendezvous IP Telephony Conferencing</span></span>

<span data-ttu-id="26dbc-104">\[ В Windows Vista, Windows Server 2008 и последующих версиях операционной системы нельзя использовать встречные средства и элементы управления Конференц-телефонией и интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="26dbc-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="26dbc-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="26dbc-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="26dbc-106">Встречные элементы управления TAPI 3 позволяют программисту создавать приложения, которые могут создавать и обнаруживать многоадресные IP-конференции мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="26dbc-106">The TAPI 3 Rendezvous controls enable a programmer to create applications that can create and discover multimedia multicast IP conferences.</span></span>

<span data-ttu-id="26dbc-107">Ключевые компоненты встреч:</span><span class="sxs-lookup"><span data-stu-id="26dbc-107">The key components of Rendezvous:</span></span>

<span data-ttu-id="26dbc-108">[Элементы управления каталога](directory-controls.md) представляют собой абстракцию списков конференций на сервере ILS или NTDS.</span><span class="sxs-lookup"><span data-stu-id="26dbc-108">[Directory Controls](directory-controls.md) are an abstraction of conference listings on an ILS or NTDS server.</span></span>

<span data-ttu-id="26dbc-109">[Элементы управления "хранилище больших двоичных объектов](conference-blob-controls.md) " представляют сведения, относящиеся к Конференции, такие как время начала и окончания.</span><span class="sxs-lookup"><span data-stu-id="26dbc-109">[Conference Blob Controls](conference-blob-controls.md) represent conference-specific information such as start and stop time.</span></span> <span data-ttu-id="26dbc-110">Для протоколов. BLOB-объекты протокола SDP предоставляются специальными интерфейсами.</span><span class="sxs-lookup"><span data-stu-id="26dbc-110">Special interfaces are provided for SDP protocol blobs.</span></span> <span data-ttu-id="26dbc-111">Подробные сведения см. в RFC 2327 под названием «SDP: Протокол описания сеанса».</span><span class="sxs-lookup"><span data-stu-id="26dbc-111">For detailed information, see RFC 2327 entitled "SDP: Session Description Protocol."</span></span> <span data-ttu-id="26dbc-112">Текущую копию этого документа RFC можно найти с помощью поисковой системы в Интернете.</span><span class="sxs-lookup"><span data-stu-id="26dbc-112">A current copy of this RFC can be located using an Internet search engine.</span></span>

<span data-ttu-id="26dbc-113">[Многоадресные COM-интерфейсы](multicast-com-interfaces.md) — это оболочки COM для функций MADCAP, которые ранее известны как мдхкп.</span><span class="sxs-lookup"><span data-stu-id="26dbc-113">[Multicast COM Interfaces](multicast-com-interfaces.md) are COM wrappers for the MADCAP functions, formerly know as MDHCP.</span></span> <span data-ttu-id="26dbc-114">Эти интерфейсы позволяют приложению получать адреса многоадресной рассылки с сервера распределения адресов многоадресной рассылки.</span><span class="sxs-lookup"><span data-stu-id="26dbc-114">These interfaces allow an application to get multicast addresses from a multicast address allocation server.</span></span>

<span data-ttu-id="26dbc-115">Следующий материал содержит общие сведения и примеры использования встречных элементов управления для IP-телефонии и конференций.</span><span class="sxs-lookup"><span data-stu-id="26dbc-115">The following material provides a general overview and some usage examples of the Rendezvous controls for IP telephony and conferencing.</span></span>

 

 



