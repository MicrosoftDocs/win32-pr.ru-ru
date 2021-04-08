---
title: Выбор последовательности протокола
description: Последовательность протокола — это язык, используемый сетевой операционной системой для обмена данными между сетью и другими компьютерами.
ms.assetid: 9c788b9b-82c5-4a4b-86c6-e9a9df699da3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ac6b79f5f7a0829eea88eba77f2d022e8de2ca8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068426"
---
# <a name="selecting-a-protocol-sequence"></a><span data-ttu-id="7d703-103">Выбор последовательности протокола</span><span class="sxs-lookup"><span data-stu-id="7d703-103">Selecting a Protocol Sequence</span></span>

<span data-ttu-id="7d703-104">Последовательность протокола — это язык, используемый сетевой операционной системой для обмена данными между сетью и другими компьютерами.</span><span class="sxs-lookup"><span data-stu-id="7d703-104">A protocol sequence is the language that a network operating system uses to talk over the network to other computers.</span></span> <span data-ttu-id="7d703-105">В более конкретных условиях приложения RPC должны указывать строку, представляющую сочетание протокола RPC, транспортного протокола и сетевого протокола.</span><span class="sxs-lookup"><span data-stu-id="7d703-105">In more specific terms, RPC applications must specify a string that represents a combination of an RPC protocol, a transport protocol, and a network protocol.</span></span>

<span data-ttu-id="7d703-106">Microsoft RPC поддерживает три протокола RPC:</span><span class="sxs-lookup"><span data-stu-id="7d703-106">Microsoft RPC supports three RPC protocols:</span></span>

-   <span data-ttu-id="7d703-107">Сетевая вычислительная архитектура. Протокол, ориентированный на подключение (НКАКН)</span><span class="sxs-lookup"><span data-stu-id="7d703-107">Network Computing Architecture connection-oriented protocol (NCACN)</span></span>
-   <span data-ttu-id="7d703-108">Протокол датаграмм с архитектурой сетевой инфраструктуры (НКАДГ)</span><span class="sxs-lookup"><span data-stu-id="7d703-108">Network Computing Architecture datagram protocol (NCADG)</span></span>
-   <span data-ttu-id="7d703-109">Сетевая вычислительная архитектура локальный удаленный вызов процедур (НКАЛРПК)</span><span class="sxs-lookup"><span data-stu-id="7d703-109">Network Computing Architecture local remote procedure call (NCALRPC)</span></span>

<span data-ttu-id="7d703-110">Приложения RPC могут использовать протокол НКАЛРПК для вызова процедур, предлагаемых серверными программами, работающими на том же компьютере, на котором выполняется клиентская программа.</span><span class="sxs-lookup"><span data-stu-id="7d703-110">RPC applications can use the NCALRPC protocol to invoke procedures offered by server programs running on the same computer that the client program runs on.</span></span> <span data-ttu-id="7d703-111">Это, по крайней мере, самый эффективный метод вызова функциональных возможностей в другом процессе на том же компьютере.</span><span class="sxs-lookup"><span data-stu-id="7d703-111">This is, by far, the most efficient method for calling functionality in a different process on the same computer.</span></span>

<span data-ttu-id="7d703-112">Протоколы транспорта и сети, используемые приложением, зависят от того, какие протоколы поддерживает сеть.</span><span class="sxs-lookup"><span data-stu-id="7d703-112">The transport and network protocols that your application uses depend on which protocols the network supports.</span></span> <span data-ttu-id="7d703-113">Многие сети уже сегодня, включая Интернет, поддерживают TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="7d703-113">Many networks today, including the Internet, support TCP/IP.</span></span> <span data-ttu-id="7d703-114">Другими распространенными транспортными и сетевыми протоколами являются IPX/SPX, NetBIOS и AppleTalk DSP.</span><span class="sxs-lookup"><span data-stu-id="7d703-114">Other common transport and network protocols are IPX/SPX, NetBIOS, and AppleTalk DSP.</span></span> <span data-ttu-id="7d703-115">Microsoft RPC поддерживает эти и другие транспортные и сетевые протоколы.</span><span class="sxs-lookup"><span data-stu-id="7d703-115">Microsoft RPC supports these and other transport and network protocols.</span></span> <span data-ttu-id="7d703-116">Полный список см. в разделе [константы последовательности протоколов](protocol-sequence-constants.md).</span><span class="sxs-lookup"><span data-stu-id="7d703-116">For a complete list, see [Protocol Sequence Constants](protocol-sequence-constants.md).</span></span>

<span data-ttu-id="7d703-117">Если приложение использует автоматические дескрипторы привязки, указывать последовательность протокола не требуется.</span><span class="sxs-lookup"><span data-stu-id="7d703-117">When your application uses automatic binding handles, it does not need to specify the protocol sequence.</span></span> <span data-ttu-id="7d703-118">Если он использует неявные или явные дескрипторы, он должен получить или указать последовательность протокола.</span><span class="sxs-lookup"><span data-stu-id="7d703-118">If it uses implicit or explicit handles, it must obtain or specify the protocol sequence.</span></span> <span data-ttu-id="7d703-119">Каждая распределенная система должна проверить среду, в которой она будет развернута, чтобы определить, какая последовательность протоколов лучше всего подходит для этой среды.</span><span class="sxs-lookup"><span data-stu-id="7d703-119">Each distributed system must examine the environment in which it will be deployed to determine which protocol sequence is best suited for that environment.</span></span>

<span data-ttu-id="7d703-120">Не все последовательности протоколов имеют эквивалентные функции.</span><span class="sxs-lookup"><span data-stu-id="7d703-120">Not all protocol sequences have equivalent functionality.</span></span> <span data-ttu-id="7d703-121">Разработчики должны убедиться, что выбранная последовательность протокола поддерживает необходимые функции.</span><span class="sxs-lookup"><span data-stu-id="7d703-121">Developers should verify that the chosen protocol sequence supports the required features.</span></span> <span data-ttu-id="7d703-122">В общем случае рекомендуется **нкалрпк** для локальных подключений и **нкакн \_ IP \_ TCP** или **нкакн \_ http** для удаленных подключений. они работают во всех средах, имеют оптимальную производительность и поддерживают все необходимые, оптимальные возможности.</span><span class="sxs-lookup"><span data-stu-id="7d703-122">In general, **ncalrpc** for local communications and **ncacn\_ip\_tcp** or **ncacn\_http** for remote communications are recommended; they work in all environments, they have optimal performance, and they support all necessary, best-practice features.</span></span>

<span data-ttu-id="7d703-123">Клиенты также могут указать сведения о последовательности протоколов, получаемые от Active Directory, реестра, переменных среды, созданных и инициализированных программой установки, файлами конфигурации конкретного приложения или строками литералов в исходном коде программы.</span><span class="sxs-lookup"><span data-stu-id="7d703-123">Clients can also specify protocol sequence information that they obtain from Active Directory, the registry, environment variables created and initialized by the setup program, application-specific configuration files, or from literal strings in the program source code.</span></span>

<span data-ttu-id="7d703-124">После того, как клиентская программа имеет допустимую строку последовательности протокола, она может передать эту информацию функциям [**рпкстрингбиндингкомпосе**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose) и [**рпкбиндингфромстрингбиндинг**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) , чтобы создать маркер привязки.</span><span class="sxs-lookup"><span data-stu-id="7d703-124">After your client program has a valid protocol sequence string, it can pass that information to the [**RpcStringBindingCompose**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose) and [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) functions to create the binding handle.</span></span>

 

 




