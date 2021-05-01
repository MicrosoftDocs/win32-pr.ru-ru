---
title: Измеряемая загрузка
description: Измеряемая загрузка
ms.assetid: D7ED02FA-6D0F-4753-AC07-BD7DCE55B3FD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d728a1980bc9a461e6383b1dea2bd7eb4aab461
ms.sourcegitcommit: f14de4414da072d5a761e946aedfde24d8b65102
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/30/2021
ms.locfileid: "108314345"
---
# <a name="measured-boot"></a><span data-ttu-id="a9e1f-103">Измеряемая загрузка</span><span class="sxs-lookup"><span data-stu-id="a9e1f-103">Measured Boot</span></span>

## <a name="platforms"></a><span data-ttu-id="a9e1f-104">Платформы</span><span class="sxs-lookup"><span data-stu-id="a9e1f-104">Platforms</span></span>

 <span data-ttu-id="a9e1f-105">**Клиенты** — Windows 8</span><span class="sxs-lookup"><span data-stu-id="a9e1f-105">**Clients** - Windows 8</span></span>  
<span data-ttu-id="a9e1f-106">**Серверы** — Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a9e1f-106">**Servers** - Windows Server 2012</span></span>  



## <a name="description"></a><span data-ttu-id="a9e1f-107">Описание</span><span class="sxs-lookup"><span data-stu-id="a9e1f-107">Description</span></span>

<span data-ttu-id="a9e1f-108">По мере того, как антивредоносное по стало более эффективным при обнаружении вредоносных программ во время выполнения, злоумышленники также становятся более эффективными при создании rootkit-программ, которые могут скрываться от обнаружения.</span><span class="sxs-lookup"><span data-stu-id="a9e1f-108">As antimalware (AM) software has become better and better at detecting runtime malware, attackers are also becoming better at creating rootkits that can hide from detection.</span></span> <span data-ttu-id="a9e1f-109">Обнаружение вредоносных программ, запускаемых на ранних этапах цикла загрузки, является сложной задачей, которая в большинстве случаев имеет более тщательного решения.</span><span class="sxs-lookup"><span data-stu-id="a9e1f-109">Detecting malware that starts early in the boot cycle is a challenge that most AM vendors address diligently.</span></span> <span data-ttu-id="a9e1f-110">Как правило, они создают системные атаки, которые не поддерживаются операционной системой узла, и фактически могут привести к нестабильной работе компьютера.</span><span class="sxs-lookup"><span data-stu-id="a9e1f-110">Typically, they create system hacks that are not supported by the host operating system and can actually result in placing the computer in an unstable state.</span></span> <span data-ttu-id="a9e1f-111">До этого момента Windows не предоставила хороший способ обнаружения и устранения угроз с ранним загрузкой.</span><span class="sxs-lookup"><span data-stu-id="a9e1f-111">Up to this point, Windows has not provided a good way for AM to detect and resolve these early boot threats.</span></span> <span data-ttu-id="a9e1f-112">В Windows 8 появилась новая функция под названием измеряемая Загрузка, которая измеряет каждый компонент, от микропрограммы до загрузочных драйверов, сохраняет эти измерения в доверенный платформенный модуль (TPM) (TPM) на компьютере, а затем делает доступным журнал, который можно проверить удаленно, чтобы проверить состояние загрузки клиента.</span><span class="sxs-lookup"><span data-stu-id="a9e1f-112">Windows 8 introduces a new feature called Measured Boot, which measures each component, from firmware up through the boot start drivers, stores those measurements in the Trusted Platform Module (TPM) on the machine, and then makes available a log that can be tested remotely to verify the boot state of the client.</span></span>

## <a name="manifestation"></a><span data-ttu-id="a9e1f-113">Проявление</span><span class="sxs-lookup"><span data-stu-id="a9e1f-113">Manifestation</span></span>

<span data-ttu-id="a9e1f-114">Измеряемая функция загрузки предоставляет программное обеспечение с надежным (устойчивым к подмене и искажением) журналом всех компонентов загрузки, запущенных до программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="a9e1f-114">The Measured Boot feature provides AM software with a trusted (resistant to spoofing and tampering) log of all boot components that started before AM software.</span></span> <span data-ttu-id="a9e1f-115">Программа по может использовать журнал, чтобы определить, являются ли компоненты, которые выполнялись до этого, надежными или заражены вредоносными программами.</span><span class="sxs-lookup"><span data-stu-id="a9e1f-115">AM software can use the log to determine whether components that ran before it are trustworthy or if they are infected with malware.</span></span> <span data-ttu-id="a9e1f-116">Программа AM на локальном компьютере может отправить журнал на удаленный сервер для ознакомления.</span><span class="sxs-lookup"><span data-stu-id="a9e1f-116">The AM software on the local machine can send the log to a remote server for evaluation.</span></span> <span data-ttu-id="a9e1f-117">Удаленный сервер может инициировать действия по исправлению либо путем взаимодействия с программным обеспечением на клиенте, либо посредством использования механизмов по внешнему каналу, если это уместно.</span><span class="sxs-lookup"><span data-stu-id="a9e1f-117">The remote server may initiate remediation actions either by interacting with software on the client or through out-of-band mechanisms, as appropriate.</span></span>

## <a name="mitigation"></a><span data-ttu-id="a9e1f-118">Меры по снижению риска</span><span class="sxs-lookup"><span data-stu-id="a9e1f-118">Mitigation</span></span>

<span data-ttu-id="a9e1f-119">В корпоративных сценариях системный администратор управляет использованием измеряемой информации о загрузке.</span><span class="sxs-lookup"><span data-stu-id="a9e1f-119">In enterprise scenarios, the system administrator has control of how Measured Boot info is used.</span></span> <span data-ttu-id="a9e1f-120">В сценариях конечных пользователей, например в интерактивных банковских операциях, потребитель должен принять участие в использовании измеряемой загрузки для конкретной службы.</span><span class="sxs-lookup"><span data-stu-id="a9e1f-120">In end-user scenarios for example, online banking), the consumer must opt in to use Measured Boot for the specific service.</span></span>

## <a name="solution"></a><span data-ttu-id="a9e1f-121">Решение</span><span class="sxs-lookup"><span data-stu-id="a9e1f-121">Solution</span></span>

<span data-ttu-id="a9e1f-122">Готовится технический документ с подробными сведениями об API и вызовах функций, которые должны быть сделаны для различных измеряемых сценариев загрузки.</span><span class="sxs-lookup"><span data-stu-id="a9e1f-122">A white paper is being prepared that details the APIs and function calls that must be made for various Measured Boot scenarios.</span></span>

 

 




