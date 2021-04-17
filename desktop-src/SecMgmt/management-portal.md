---
description: Используйте технологии управления безопасностью для создания систем управления информационной безопасностью, программного обеспечения для управления безопасностью, решений по управлению безопасностью и обеспечения управления безопасностью событий и управления безопасностью.
ms.assetid: c6626297-2e45-4073-b04d-8ed40866fe1a
title: Управление безопасностью
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fffeb33013029737db62d3db2b4c10448dac6a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684156"
---
# <a name="security-management"></a><span data-ttu-id="c1a3a-103">Управление безопасностью</span><span class="sxs-lookup"><span data-stu-id="c1a3a-103">Security Management</span></span>

## <a name="purpose"></a><span data-ttu-id="c1a3a-104">Назначение</span><span class="sxs-lookup"><span data-stu-id="c1a3a-104">Purpose</span></span>

<span data-ttu-id="c1a3a-105">Технологии управления безопасностью можно использовать для управления политикой [*локального центра безопасности*](/windows/desktop/SecGloss/l-gly) (LSA) и политикой [*фильтрации паролей*](/windows/desktop/SecGloss/p-gly) , выполнения запросов к возможностям программ из внешних источников и вложений служб, расширяющих функциональные возможности средства настройки безопасности.</span><span class="sxs-lookup"><span data-stu-id="c1a3a-105">The security management technologies can be used to manage [*Local Security Authority*](/windows/desktop/SecGloss/l-gly) (LSA) policy and [*password filter*](/windows/desktop/SecGloss/p-gly) policy, query the ability of programs from external sources, and service attachments that extend the functionality of the Security Configuration tool.</span></span>

<span data-ttu-id="c1a3a-106">Технологии управления безопасностью Майкрософт включают в себя API политики LSA, API фильтрации паролей, безопасный API и API вложений безопасности службы.</span><span class="sxs-lookup"><span data-stu-id="c1a3a-106">Microsoft security management technologies include the LSA Policy API, the Password Filter API, the Safer API, and the Service Security Attachments API.</span></span> <span data-ttu-id="c1a3a-107">Эти технологии позволяют разработчикам программного обеспечения создавать приложения, управляющие системами и приложениями.</span><span class="sxs-lookup"><span data-stu-id="c1a3a-107">These technologies enable software developers to create applications that manage systems and applications.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="c1a3a-108">Аудитория разработчиков</span><span class="sxs-lookup"><span data-stu-id="c1a3a-108">Developer audience</span></span>

<span data-ttu-id="c1a3a-109">API политики LSA, API фильтрации паролей, безопасный API и API вложений безопасности службы предназначены для использования разработчиками приложений, которые позволяют администраторам управлять системами и защищать их.</span><span class="sxs-lookup"><span data-stu-id="c1a3a-109">The LSA Policy API, the Password Filter API, the Safer API, and the Service Security Attachments API are intended for use by developers of applications that enable administrators to manage and secure their systems.</span></span> <span data-ttu-id="c1a3a-110">Разработчики должны быть знакомы с языками программирования C и C++, а также с программированием на основе Windows.</span><span class="sxs-lookup"><span data-stu-id="c1a3a-110">Developers should be familiar with the C and C++ programming languages and with Windows-based programming.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="c1a3a-111">Требования к среде выполнения</span><span class="sxs-lookup"><span data-stu-id="c1a3a-111">Run-time requirements</span></span>

<span data-ttu-id="c1a3a-112">Сведения о требованиях времени выполнения для определенного программного элемента см. в разделе "требования" на странице справочника по этому элементу.</span><span class="sxs-lookup"><span data-stu-id="c1a3a-112">For information about run-time requirements for a particular programming element, see the Requirements section of the reference page for that element.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="c1a3a-113">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="c1a3a-113">In this section</span></span>



| <span data-ttu-id="c1a3a-114">Раздел</span><span class="sxs-lookup"><span data-stu-id="c1a3a-114">Topic</span></span>                                                                | <span data-ttu-id="c1a3a-115">Описание</span><span class="sxs-lookup"><span data-stu-id="c1a3a-115">Description</span></span>                                                                                                                            |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c1a3a-116">Сведения об управлении безопасностью</span><span class="sxs-lookup"><span data-stu-id="c1a3a-116">About Security Management</span></span>](about-management.md)<br/>         | <span data-ttu-id="c1a3a-117">Обзор интерфейсов API управления безопасностью.</span><span class="sxs-lookup"><span data-stu-id="c1a3a-117">An overview of the security management APIs.</span></span><br/>                                                                                |
| [<span data-ttu-id="c1a3a-118">Использование управления безопасностью</span><span class="sxs-lookup"><span data-stu-id="c1a3a-118">Using Security Management</span></span>](using-management.md)<br/>         | <span data-ttu-id="c1a3a-119">Общие задачи управления безопасностью.</span><span class="sxs-lookup"><span data-stu-id="c1a3a-119">Common security management tasks.</span></span><br/>                                                                                           |
| [<span data-ttu-id="c1a3a-120">Справочник по управлению безопасностью</span><span class="sxs-lookup"><span data-stu-id="c1a3a-120">Security Management Reference</span></span>](management-reference.md)<br/> | <span data-ttu-id="c1a3a-121">Подробные сведения о функциях, структурах и других программных элементах, используемых для реализации управления безопасностью.</span><span class="sxs-lookup"><span data-stu-id="c1a3a-121">Detailed information about the functions, structures, and other programming elements used to implement security management.</span></span><br/> |



 

 

