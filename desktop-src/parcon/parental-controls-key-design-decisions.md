---
description: Родительские контрольные решения
ms.assetid: 0b41cf81-0770-4408-97a8-a178fae78d23
title: Родительские контрольные решения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39cb4be775a3380cb9fe7aa677362df31a2dc453
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081504"
---
# <a name="parental-controls-key-design-decisions"></a><span data-ttu-id="c84dd-103">Родительские контрольные решения</span><span class="sxs-lookup"><span data-stu-id="c84dd-103">Parental Controls Key Design Decisions</span></span>

<span data-ttu-id="c84dd-104">Основные решения по проектированию при разработке родительского контроля в Windows Vista:</span><span class="sxs-lookup"><span data-stu-id="c84dd-104">Major design decisions in the development of Windows Vista Parental Controls are:</span></span>

## <a name="essential-dependency-on-windows-vista-user-account-control-uac-feature"></a><span data-ttu-id="c84dd-105">Основная зависимость от функции контроля учетных записей пользователей Windows Vista (UAC)</span><span class="sxs-lookup"><span data-stu-id="c84dd-105">Essential Dependency on Windows Vista User Account Control (UAC) Feature</span></span>

<span data-ttu-id="c84dd-106">Основное решение для родительского контроля в Windows Vista заключается в том, чтобы использовать новую функцию контроля учетных записей (UAC) для реализации ограниченных идентификаторов учетных записей, особенно необходимых для ограничений в сети для контролируемых пользователей.</span><span class="sxs-lookup"><span data-stu-id="c84dd-106">A key decision for Windows Vista Parental Controls is to rely on the new User Account Control (UAC) feature to implement the reduced rights account identities especially needed for offline restrictions on controlled users.</span></span> <span data-ttu-id="c84dd-107">Дополнительные сведения о контроле учетных записей см. [в статье Windows Vista и Windows Server 2008 для разработчиков: требования к разработке приложений Windows Vista для контроля учетных записей пользователей (UAC)](/previous-versions/aa905330(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="c84dd-107">For more information about UAC, see [The Windows Vista and Windows Server 2008 Developer Story: Windows Vista Application Development Requirements for User Account Control (UAC)](/previous-versions/aa905330(v=msdn.10)).</span></span> <span data-ttu-id="c84dd-108">В целом, каждая учетная запись с правами администратора фактически имеет привилегии для выполнения родительской или роли защитника по просмотру данных журнала и настройке политик.</span><span class="sxs-lookup"><span data-stu-id="c84dd-108">In summary, every account with administrator rights effectively has privileges to perform the parent or guardian role of viewing log data and setting policies.</span></span> <span data-ttu-id="c84dd-109">Родительский контроль может быть установлен только для пользователей с правами обычного доступа (ранее именуемых учетными записями пользователей с наименьшими правами или ЛУАС), так как только они не могут изменять журналы и параметры с использованием списков управления доступом (ACL), настроенных только администраторам для записи.</span><span class="sxs-lookup"><span data-stu-id="c84dd-109">Parental controls may only be set on standard-rights users (formerly called Least-privileged User Accounts, or LUAs), as only they cannot alter logs and settings with Access Control Lists (ACLs) configured only for administrators to write.</span></span> <span data-ttu-id="c84dd-110">Другими словами:</span><span class="sxs-lookup"><span data-stu-id="c84dd-110">In other words:</span></span>

-   <span data-ttu-id="c84dd-111">Родительское или опекунное удостоверение неявно равно учетной записи, имеющей права администратора.</span><span class="sxs-lookup"><span data-stu-id="c84dd-111">A parent or guardian identity implicitly equals an account that has rights of an administrator.</span></span>
-   <span data-ttu-id="c84dd-112">Пользователи с родительским управлением должны быть стандартными пользователями.</span><span class="sxs-lookup"><span data-stu-id="c84dd-112">Parentally controlled users must be standard users.</span></span>

## <a name="nearly-all-settings-are-available-by-apis"></a><span data-ttu-id="c84dd-113">Почти все параметры доступны API-интерфейсам.</span><span class="sxs-lookup"><span data-stu-id="c84dd-113">Nearly All Settings Are Available by APIs</span></span>

<span data-ttu-id="c84dd-114">За исключением таких элементов, как определения системы оценок, параметры, доступные для манипуляции с пользовательским интерфейсом родительского контроля, также могут быть изменены предоставляемыми API.</span><span class="sxs-lookup"><span data-stu-id="c84dd-114">With the exception of items such as ratings system definitions, settings available for manipulation by the Parental Controls User Interface may also be modified by exposed APIs.</span></span> <span data-ttu-id="c84dd-115">Программам необходимо реализовать повышение прав для административных прав, чтобы изменить параметры, как указано выше для UAC.</span><span class="sxs-lookup"><span data-stu-id="c84dd-115">It is necessary for programs to implement elevation to administrative rights in order to alter settings, as noted above for UAC.</span></span>

## <a name="windows-vista-parental-controls-is-a-consumer-only-technology"></a><span data-ttu-id="c84dd-116">Родительский контроль в Windows Vista — это технология, предназначенная только для потребителей</span><span class="sxs-lookup"><span data-stu-id="c84dd-116">Windows Vista Parental Controls Is a Consumer-only Technology</span></span>

<span data-ttu-id="c84dd-117">Родительские элементы управления Windows Vista не предназначены для использования с учетными записями домена.</span><span class="sxs-lookup"><span data-stu-id="c84dd-117">Windows Vista Parental Controls are not intended to be used with domain accounts.</span></span> <span data-ttu-id="c84dd-118">В качестве потребительской технологии родительский контроль не развертывается в SKU Windows Vista для бизнеса.</span><span class="sxs-lookup"><span data-stu-id="c84dd-118">As a consumer technology, Parental Controls is not deployed in business SKUs of Windows Vista.</span></span> <span data-ttu-id="c84dd-119">Если компьютер присоединен к домену, ссылки на пользовательский интерфейс семейной безопасности будут подавляться.</span><span class="sxs-lookup"><span data-stu-id="c84dd-119">If a computer is joined to a domain, the Family Safety user interface links will be suppressed.</span></span>

<span data-ttu-id="c84dd-120">Будет предоставлен механизм для предоставления функциональных возможностей для присоединенного к домену варианта, но только учетные записи пользователей, не являющихся доменами, могут быть настроены с помощью родительского контроля.</span><span class="sxs-lookup"><span data-stu-id="c84dd-120">A mechanism will be provided to expose the functionality for the domain-joined case, but only non-domain user accounts may be configured with Parental Controls.</span></span>

 

 
