---
description: Встречные элементы управления TAPI 3 предоставляют механизмы для объявления и обнаружения многокомпонентных мультимедийных IP-конференций. Ниже описывается набор компонентов и интерфейсов модели COM для реализации конференций.
ms.assetid: 0ca2edac-b507-497e-9e63-78a10466e2eb
title: О встречных конференциях IP-телефонии
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4bd06fb848088a42e34bd7b176358a7507e3d2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104562855"
---
# <a name="about-rendezvous-ip-telephony-conferencing"></a><span data-ttu-id="68c0d-104">О встречных конференциях IP-телефонии</span><span class="sxs-lookup"><span data-stu-id="68c0d-104">About Rendezvous IP Telephony Conferencing</span></span>

<span data-ttu-id="68c0d-105">\[ В Windows Vista, Windows Server 2008 и последующих версиях операционной системы нельзя использовать встречные средства и элементы управления Конференц-телефонией и интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="68c0d-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="68c0d-106">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="68c0d-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="68c0d-107">Встречные элементы управления TAPI 3 предоставляют механизмы для объявления и обнаружения многокомпонентных мультимедийных IP-конференций.</span><span class="sxs-lookup"><span data-stu-id="68c0d-107">The TAPI 3 Rendezvous controls provide mechanisms to advertise and discover multiparty multimedia IP conferences.</span></span> <span data-ttu-id="68c0d-108">Ниже описывается набор компонентов и интерфейсов модели COM для реализации конференций.</span><span class="sxs-lookup"><span data-stu-id="68c0d-108">The following describes a set of Component Object Model (COM) components and interfaces to implement conferencing.</span></span>

<span data-ttu-id="68c0d-109">COM — это базовая модель программирования для TAPI 3, и ее знакомство с этим документом предполагается.</span><span class="sxs-lookup"><span data-stu-id="68c0d-109">COM is the basic coding model for TAPI 3, and familiarity with it is assumed throughout this document.</span></span> <span data-ttu-id="68c0d-110">Для получения сведений об COM выполните поиск по пакету SDK для платформы.</span><span class="sxs-lookup"><span data-stu-id="68c0d-110">For information on COM, search the Platform Software Development Kit (SDK).</span></span>

## <a name="features"></a><span data-ttu-id="68c0d-111">Компоненты</span><span class="sxs-lookup"><span data-stu-id="68c0d-111">Features</span></span>

-   <span data-ttu-id="68c0d-112">Предоставляет абстракцию каталога конференций для управления объявлениями об мультимедийных конференциях</span><span class="sxs-lookup"><span data-stu-id="68c0d-112">Provides the abstraction of a conference directory for manipulating announcements of multimedia conferences</span></span>
-   <span data-ttu-id="68c0d-113">Обеспечивает безопасность с помощью проверки подлинности, шифрования и уровня контроля доступа (ACL) для каждого объявления.</span><span class="sxs-lookup"><span data-stu-id="68c0d-113">Provides security through authentication, encryption, and a per-announcement access control layer (ACL)</span></span>
-   <span data-ttu-id="68c0d-114">Предоставляет общую схему объявления конференции, позволяющую выполнять поиск по значениям атрибутов.</span><span class="sxs-lookup"><span data-stu-id="68c0d-114">Provides a common schema for a conference announcement, enabling searches by attribute values</span></span>
-   <span data-ttu-id="68c0d-115">Разрешает расширения через атрибут, обслуживаемый поставщиком (объект Conference BLOB) в схеме</span><span class="sxs-lookup"><span data-stu-id="68c0d-115">Allows extensions through a provider-maintained attribute (conference blob) in the schema</span></span>
-   <span data-ttu-id="68c0d-116">Предоставляет обертку COM для API распределения адресов многоадресной рассылки (MADCAP)</span><span class="sxs-lookup"><span data-stu-id="68c0d-116">Provides a COM wrapper for the multicast address allocation (MADCAP) API</span></span>

## <a name="architecture"></a><span data-ttu-id="68c0d-117">Архитектура</span><span class="sxs-lookup"><span data-stu-id="68c0d-117">Architecture</span></span>

<span data-ttu-id="68c0d-118">Следующие описания и схема иллюстрируют ключевые аспекты архитектуры системы.</span><span class="sxs-lookup"><span data-stu-id="68c0d-118">The following descriptions and diagram illustrate key aspects of the system architecture.</span></span>

-   <span data-ttu-id="68c0d-119">Клиент может управлять Конференцией, хранящейся на динамическом каталоге ILS или сервере NTDS, с помощью встречных элементов управления.</span><span class="sxs-lookup"><span data-stu-id="68c0d-119">The client can manipulate conferences stored on an ILS dynamic directory or NTDS server using Rendezvous controls.</span></span> <span data-ttu-id="68c0d-120">Протокол LDAP используется для взаимодействия с сервером ILS.</span><span class="sxs-lookup"><span data-stu-id="68c0d-120">The Lightweight Directory Access Protocol (LDAP) is used to communicate with an ILS server.</span></span>
-   <span data-ttu-id="68c0d-121">Встречные элементы управления предоставляют сдвоенные COM-интерфейсы для написания сценариев и программирования.</span><span class="sxs-lookup"><span data-stu-id="68c0d-121">The Rendezvous controls provide dual COM interfaces for scripting and programming.</span></span>
-   <span data-ttu-id="68c0d-122">Сервер SAP с прямым доступом к Интернету прослушивает объявления конференций в Интернете и заполняет динамические серверы ILS сведениями о Конференции.</span><span class="sxs-lookup"><span data-stu-id="68c0d-122">A Session Announcement Protocol (SAP) server with direct access to the Internet listens to conference announcements on the Internet and populates ILS dynamic servers with the conference information.</span></span> <span data-ttu-id="68c0d-123">Аналогичным образом также объявляется локально созданные конференции, область действия которых включает в себя Интернет.</span><span class="sxs-lookup"><span data-stu-id="68c0d-123">Similarly, it also announces the locally created conferences whose scope includes the Internet.</span></span> <span data-ttu-id="68c0d-124">(Сервер SAP не планируется для Microsoft Windows 2000.)</span><span class="sxs-lookup"><span data-stu-id="68c0d-124">(The SAP server is not planned for Microsoft Windows 2000.)</span></span>

![встречная архитектура системы](images/rend1.png)

 

 



