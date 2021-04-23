---
description: AppContainer реализуется путем добавления новых сведений в маркер процесса, изменения Сеакцессчекк () таким образом, чтобы все устаревшие, неизмененные объекты списка управления доступом (ACL) блокировали запросы на доступ из процессов AppContainer по умолчанию и объекты повторного управления доступом, которые должны быть доступны для Аппконтаинерс.
ms.assetid: C70A2F8C-27CB-4298-AA31-8F5099616625
title: Реализация AppContainer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a6fc4c8d807d6a45f27f4f7a79d69ceb97edeb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912428"
---
# <a name="implementing-an-appcontainer"></a><span data-ttu-id="63f32-103">Реализация AppContainer</span><span class="sxs-lookup"><span data-stu-id="63f32-103">Implementing an AppContainer</span></span>

<span data-ttu-id="63f32-104">AppContainer реализуется путем добавления новых сведений в маркер процесса, изменения [**сеакцессчекк ()**](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-seaccesscheck) таким образом, чтобы все устаревшие, неизмененные объекты списка управления доступом (ACL) блокировали запросы на доступ из процессов AppContainer по умолчанию и объекты повторного управления доступом, которые должны быть доступны для аппконтаинерс.</span><span class="sxs-lookup"><span data-stu-id="63f32-104">An AppContainer is implemented by adding new information to the process token, changing [**SeAccessCheck()**](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-seaccesscheck) so that all legacy, unmodified access control list (ACL) objects block access requests from AppContainer processes by default, and re-ACL objects that should be available to AppContainers.</span></span>

## <a name="the-process"></a><span data-ttu-id="63f32-105">Процесс</span><span class="sxs-lookup"><span data-stu-id="63f32-105">The process</span></span>

<span data-ttu-id="63f32-106">Начните с добавления новых сведений для токена процесса.</span><span class="sxs-lookup"><span data-stu-id="63f32-106">Begin by adding new information for the process token.</span></span> <span data-ttu-id="63f32-107">Затем измените **сеакцессчекк ()** , чтобы все устаревшие, неизмененные списки управления доступом блокировали запросы на доступ из процессов AppContainer по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="63f32-107">Then change **SeAccessCheck()** so that all legacy, unmodified ACLs will block access requests from AppContainer processes by default.</span></span> <span data-ttu-id="63f32-108">Наконец, повторно изменяйте ресурсы ACL, которые должны быть доступны для Аппконтаинерс</span><span class="sxs-lookup"><span data-stu-id="63f32-108">Finally, re-ACL resources that should be available to AppContainers</span></span>

<span data-ttu-id="63f32-109">Идентификатор безопасности AppContainer — это постоянный уникальный идентификатор для appcontainer.</span><span class="sxs-lookup"><span data-stu-id="63f32-109">The AppContainer SID is a persistent unique identifier for the appcontainer.</span></span> <span data-ttu-id="63f32-110">Идентификаторы безопасности возможностей предоставляют доступ к группам ресурсов группам Аппконтаинерс.</span><span class="sxs-lookup"><span data-stu-id="63f32-110">Capability SIDs grant access to groups of resources to groups of AppContainers.</span></span> <span data-ttu-id="63f32-111">Аппконтаинернумбер — это временный **DWORD** , используемый для различения аппконтаинерс.</span><span class="sxs-lookup"><span data-stu-id="63f32-111">An AppContainerNumber is a transient **DWORD** used to distinguish between AppContainers.</span></span> <span data-ttu-id="63f32-112">Однако его не следует использовать в качестве удостоверения для AppContainer.</span><span class="sxs-lookup"><span data-stu-id="63f32-112">However, it should not be used as an identity for the AppContainer.</span></span>

<span data-ttu-id="63f32-113">Чтобы разрешить одному AppContainer доступ к ресурсу, добавьте его Аппконтаинерсид в список управления доступом для этого ресурса.</span><span class="sxs-lookup"><span data-stu-id="63f32-113">To allow a single AppContainer to access a resource, add its AppContainerSID to the ACL for that resource.</span></span>

<span data-ttu-id="63f32-114">Чтобы разрешить нескольким конкретным Аппконтаинерс доступ к ресурсу, добавьте все их Аппконтаинерсидс в список ACL для этого ресурса.</span><span class="sxs-lookup"><span data-stu-id="63f32-114">To allow several specific AppContainers to access a resource, add all of their AppContainerSIDs to the ACL for that resource.</span></span>

<span data-ttu-id="63f32-115">Чтобы управлять группами разрешений, создайте идентификатор безопасности (GUID) возможности и установите этот идентификатор безопасности для всех предоставляемых ресурсов.</span><span class="sxs-lookup"><span data-stu-id="63f32-115">To manage groups of permissions, create a Capability SID (a GUID) and put that Capability SID on all of the resources to be granted.</span></span> <span data-ttu-id="63f32-116">Затем добавьте идентификатор безопасности возможности в токен процесса.</span><span class="sxs-lookup"><span data-stu-id="63f32-116">Then add the Capability SID to your process token.</span></span>

<span data-ttu-id="63f32-117">Чтобы разрешить всем Аппконтаинерс доступ к ресурсу, добавьте идентификатор безопасности " **все пакеты приложений** " в список управления доступом для этого ресурса.</span><span class="sxs-lookup"><span data-stu-id="63f32-117">To allow all AppContainers to access a resource, add the **ALL APPLICATION PACKAGES** SID to the ACL for that resource.</span></span> <span data-ttu-id="63f32-118">Это действует как подстановочный знак.</span><span class="sxs-lookup"><span data-stu-id="63f32-118">This acts like a wildcard.</span></span>

<span data-ttu-id="63f32-119">Аппконтаинерсид и Капабилитисид поддерживают маски доступа в записях контроля доступа (ACE).</span><span class="sxs-lookup"><span data-stu-id="63f32-119">Both AppContainerSID and CapabilitySID support access masks in Access Control Entries (ACE).</span></span> <span data-ttu-id="63f32-120">Задайте соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="63f32-120">Set as appropriate.</span></span>

 

 
