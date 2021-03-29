---
title: N (RPC)
description: Слова, начинающиеся с N в глоссарии удаленного вызова процедур (RPC).
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: b004002f-ae52-4ae8-a570-19241bfcee51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 547012dcbd9b1044c09d3f039b0a72946cb65bef
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "104414481"
---
# <a name="n-rpc"></a><span data-ttu-id="84edb-103">N (RPC)</span><span class="sxs-lookup"><span data-stu-id="84edb-103">N (RPC)</span></span>

<span data-ttu-id="84edb-104">[A](a-glos.md) [B](b-glos.md) [C](c-glos.md) [D](d-glos.md) [E](e-glos.md) [F](f-glos.md) G р [. J](i-glos.md) K [L](l-glos.md) [M](m-glos.md) N [O](o-glos.md) [P](p-glos.md) [Q](q.md) [R](r-glos.md) [S](s-glos.md) [T](t-glos.md) [U](u-glos.md) [V](v-glos.md) [W](w-glos.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="84edb-104">[A](a-glos.md) [B](b-glos.md) [C](c-glos.md) [D](d-glos.md) [E](e-glos.md) [F](f-glos.md) G H [I](i-glos.md) J K [L](l-glos.md) [M](m-glos.md) N [O](o-glos.md) [P](p-glos.md) [Q](q.md) [R](r-glos.md) [S](s-glos.md) [T](t-glos.md) [U](u-glos.md) [V](v-glos.md) [W](w-glos.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="84edb-105"><span id="_rpc_name_service_glos"></span><span id="_RPC_NAME_SERVICE_GLOS"></span>**Служба имен**</span><span class="sxs-lookup"><span data-stu-id="84edb-105"><span id="_rpc_name_service_glos"></span><span id="_RPC_NAME_SERVICE_GLOS"></span>**name service**</span></span>
</dt> <dd>

<span data-ttu-id="84edb-106">Служба, которая сопоставляет имена с объектами и сохраняет пары "имя-объект" в базе данных.</span><span class="sxs-lookup"><span data-stu-id="84edb-106">Service that maps names to objects and stores the name/object pairs in a database.</span></span> <span data-ttu-id="84edb-107">Например, служба имен RPC сопоставляет логическое имя с [*маркером привязки*](b-glos.md) , чтобы клиентские приложения могли ссылаться на это логическое имя, а не на последовательность протокола и сетевой адрес.</span><span class="sxs-lookup"><span data-stu-id="84edb-107">For example, the RPC name service maps a logical name to a [*binding handle*](b-glos.md) so client applications can refer to that logical name, rather than a protocol sequence and network address.</span></span> <span data-ttu-id="84edb-108">См. также служба имен — демон интерфейса ([нсид)](/windows), Служба каталогов клиента ([*CD)*](c-glos.md), [*указатель*](l-glos.md).</span><span class="sxs-lookup"><span data-stu-id="84edb-108">See also name service–interface daemon ([nsid)](/windows), Client Directory Service ([*CDS)*](c-glos.md), [*Locator*](l-glos.md).</span></span>

</dd> <dt>

<span data-ttu-id="84edb-109"><span id="_rpc_nca_glos"></span><span id="_RPC_NCA_GLOS"></span>**Архитектура сетевых вычислений (NCA)**</span><span class="sxs-lookup"><span data-stu-id="84edb-109"><span id="_rpc_nca_glos"></span><span id="_RPC_NCA_GLOS"></span>**Network Computing Architecture (NCA)**</span></span>
</dt> <dd>

<span data-ttu-id="84edb-110">Набор рекомендаций по распределенным вычислениям.</span><span class="sxs-lookup"><span data-stu-id="84edb-110">Collection of guidelines for distributed computing.</span></span> <span data-ttu-id="84edb-111">Протоколы связи RPC следуют этим рекомендациям.</span><span class="sxs-lookup"><span data-stu-id="84edb-111">The RPC communication protocols follow these guidelines.</span></span>

</dd> <dt>

<span data-ttu-id="84edb-112"><span id="_rpc_nsi_glos"></span><span id="_RPC_NSI_GLOS"></span>**Независимо от службы имен (NSI)**</span><span class="sxs-lookup"><span data-stu-id="84edb-112"><span id="_rpc_nsi_glos"></span><span id="_RPC_NSI_GLOS"></span>**Name Service Independent (NSI)**</span></span>
</dt> <dd>

<span data-ttu-id="84edb-113">Стандартный интерфейс для функций API, позволяющий распределенному приложению получать доступ к элементам базы данных службы имен RPC с помощью различных поставщиков услуг имени, таких как служба каталогов ячеек использование-DCE или указатель Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="84edb-113">Standard for API functions that allows a distributed application to access RPC name-service database elements through various name-service providers, such as OSF-DCE Cell Directory Service or Microsoft Locator.</span></span> <span data-ttu-id="84edb-114">См. также [: Демон интерфейса](/windows) (нсид).</span><span class="sxs-lookup"><span data-stu-id="84edb-114">See also [–interface daemon](/windows) (nsid).</span></span>

</dd> <dt>

<span data-ttu-id="84edb-115"><span id="_rpc_nsid_glos"></span><span id="_RPC_NSID_GLOS"></span>**Служба имен — управляющая программа-интерфейс (нсид)**</span><span class="sxs-lookup"><span data-stu-id="84edb-115"><span id="_rpc_nsid_glos"></span><span id="_RPC_NSID_GLOS"></span>**name service–interface daemon (nsid)**</span></span>
</dt> <dd>

<span data-ttu-id="84edb-116">Служба, которая предоставляет интерфейс между [*локатором*](l-glos.md) Майкрософт и базами данных службы каталогов использование-DCE для функций службы имен RPC.</span><span class="sxs-lookup"><span data-stu-id="84edb-116">Service that provides an interface between Microsoft [*Locator*](l-glos.md) and the OSF-DCE Cell Directory Service name service databases for RPC name-service functions.</span></span>

</dd> <dt>

<span data-ttu-id="84edb-117"><span id="_rpc_named_pipe_glos"></span><span id="_RPC_NAMED_PIPE_GLOS"></span>**именованный канал**</span><span class="sxs-lookup"><span data-stu-id="84edb-117"><span id="_rpc_named_pipe_glos"></span><span id="_RPC_NAMED_PIPE_GLOS"></span>**named pipe**</span></span>
</dt> <dd>

<span data-ttu-id="84edb-118">Протокол, ориентированный на подключение, основанный на блоках сообщений сервера (SMB) и [NetBIOS](/windows), который используется для обмена данными между серверным процессом и одним или несколькими клиентскими процессами.</span><span class="sxs-lookup"><span data-stu-id="84edb-118">Connection-oriented protocol, based on Server Message Blocks (SMBs) and [NetBIOS](/windows), used for communication between a server process and one or more client processes.</span></span>

</dd> <dt>

<span data-ttu-id="84edb-119"><span id="_rpc_netbeui_glos"></span><span id="_RPC_NETBEUI_GLOS"></span>**Расширенный пользовательский интерфейс NetBIOS (NetBEUI)**</span><span class="sxs-lookup"><span data-stu-id="84edb-119"><span id="_rpc_netbeui_glos"></span><span id="_RPC_NETBEUI_GLOS"></span>**NetBIOS Extended User Interface (NetBEUI)**</span></span>
</dt> <dd>

<span data-ttu-id="84edb-120">Собственный транспортный протокол и драйвер сетевого устройства LAN Manager.</span><span class="sxs-lookup"><span data-stu-id="84edb-120">LAN Manager native transport protocol and network device driver.</span></span> <span data-ttu-id="84edb-121">См. также [NetBIOS](/windows).</span><span class="sxs-lookup"><span data-stu-id="84edb-121">See also [NetBIOS](/windows).</span></span>

</dd> <dt>

<span data-ttu-id="84edb-122"><span id="_rpc_netbios_glos"></span><span id="_RPC_NETBIOS_GLOS"></span>**Сетевая базовая система ввода-вывода (NetBIOS)**</span><span class="sxs-lookup"><span data-stu-id="84edb-122"><span id="_rpc_netbios_glos"></span><span id="_RPC_NETBIOS_GLOS"></span>**Network Basic Input/Output System (NetBIOS)**</span></span>
</dt> <dd>

<span data-ttu-id="84edb-123">Программный интерфейс между операционной системой Microsoft MS-DOS, шиной ввода-вывода и локальной сетью.</span><span class="sxs-lookup"><span data-stu-id="84edb-123">Software interface between the Microsoft MS-DOS operating system, the I/O bus, and a local area network.</span></span>

</dd> <dt>

<span data-ttu-id="84edb-124"><span id="_rpc_ndr_glos"></span><span id="_RPC_NDR_GLOS"></span>**Представление данных сети (NDR)**</span><span class="sxs-lookup"><span data-stu-id="84edb-124"><span id="_rpc_ndr_glos"></span><span id="_RPC_NDR_GLOS"></span>**Network Data Representation (NDR)**</span></span>
</dt> <dd>

<span data-ttu-id="84edb-125">Стандартный формат, используемый при передаче по сети, не зависящий от формата типа данных на любой конкретной архитектуре компьютера.</span><span class="sxs-lookup"><span data-stu-id="84edb-125">Standard format used during network transmission that is independent of the data-type format on any particular computer architecture.</span></span> <span data-ttu-id="84edb-126">Передаваемые данные содержат сведения, указывающие его формат NDR.</span><span class="sxs-lookup"><span data-stu-id="84edb-126">Transmitted data includes information that specifies its NDR format.</span></span>

</dd> <dt>

<span data-ttu-id="84edb-127"><span id="_rpc_network_address_glos"></span><span id="_RPC_NETWORK_ADDRESS_GLOS"></span>**сетевой адрес**</span><span class="sxs-lookup"><span data-stu-id="84edb-127"><span id="_rpc_network_address_glos"></span><span id="_RPC_NETWORK_ADDRESS_GLOS"></span>**network address**</span></span>
</dt> <dd>

<span data-ttu-id="84edb-128">Адрес, определяющий сервер в сети.</span><span class="sxs-lookup"><span data-stu-id="84edb-128">Address that identifies a server on a network.</span></span>

</dd> <dt>

<span data-ttu-id="84edb-129"><span id="_rpc_nonencapsulated_union_glos"></span><span id="_RPC_NONENCAPSULATED_UNION_GLOS"></span>**неинкапсулированное объединение**</span><span class="sxs-lookup"><span data-stu-id="84edb-129"><span id="_rpc_nonencapsulated_union_glos"></span><span id="_RPC_NONENCAPSULATED_UNION_GLOS"></span>**nonencapsulated union**</span></span>
</dt> <dd>

<span data-ttu-id="84edb-130">[*Размеченное объединение*](d-glos.md) , которое является менее ограничивающим, чем инкапсулированное объединение в том, что discriminant и объединение не тесно связаны.</span><span class="sxs-lookup"><span data-stu-id="84edb-130">[*Discriminated union*](d-glos.md) that is less restrictive than an encapsulated union in that the discriminant and the union are not tightly bound.</span></span> <span data-ttu-id="84edb-131">Если объединение является параметром, discriminant является другим параметром. Если объединение является полем структуры, discriminant является еще одним полем структуры.</span><span class="sxs-lookup"><span data-stu-id="84edb-131">If the union is a parameter, the discriminant is another parameter; if the union is a structure field, the discriminant is another structure field.</span></span> <span data-ttu-id="84edb-132">Параметр ключевых слов IDL \[ [**\_ имеет значение**](/windows/desktop/Midl/switch-is) \] и \[ [**\_ Тип переключателя**](/windows/desktop/Midl/switch-type) , \] который определяет discriminant и его тип.</span><span class="sxs-lookup"><span data-stu-id="84edb-132">The IDL keywords \[[**switch\_is**](/windows/desktop/Midl/switch-is)\] and \[[**switch\_type**](/windows/desktop/Midl/switch-type)\] identify the discriminant and its type.</span></span> <span data-ttu-id="84edb-133">См. также [*инкапсулированное объединение*](e-glos.md).</span><span class="sxs-lookup"><span data-stu-id="84edb-133">See also [*encapsulated union*](e-glos.md).</span></span>

</dd> <dt>

<span data-ttu-id="84edb-134"><span id="_rpc_nonidempotent_glos"></span><span id="_RPC_NONIDEMPOTENT_GLOS"></span>**нонидемпотент**</span><span class="sxs-lookup"><span data-stu-id="84edb-134"><span id="_rpc_nonidempotent_glos"></span><span id="_RPC_NONIDEMPOTENT_GLOS"></span>**nonidempotent**</span></span>
</dt> <dd>

<span data-ttu-id="84edb-135">Индикатор того, что удаленный вызов процедур не может быть выполнен несколько раз, так как он возвращает другое значение или изменяет состояние.</span><span class="sxs-lookup"><span data-stu-id="84edb-135">Indicator that a remote procedure call cannot be executed more than once because it will return a different value or change a state.</span></span>

</dd> </dl>

 

 
