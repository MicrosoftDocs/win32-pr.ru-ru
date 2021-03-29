---
description: Программисты используют технологии проверки подлинности для создания программного обеспечения управления паролями, проверки подлинности единого входа, надежной аутентификации, проверки подлинности пользователей и проверки личности
ms.assetid: 7863dbee-aa48-4024-886c-1056d7141e60
title: Проверка подлинности (аутентификация)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3989944068ade080b6b819dc34b77c914ed2e73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991453"
---
# <a name="authentication-authentication"></a><span data-ttu-id="c052a-103">Проверка подлинности (аутентификация)</span><span class="sxs-lookup"><span data-stu-id="c052a-103">Authentication (Authentication)</span></span>

## <a name="purpose"></a><span data-ttu-id="c052a-104">Назначение</span><span class="sxs-lookup"><span data-stu-id="c052a-104">Purpose</span></span>

<span data-ttu-id="c052a-105">Проверка подлинности — это процесс, с помощью которого система проверяет сведения о входе пользователя в систему.</span><span class="sxs-lookup"><span data-stu-id="c052a-105">Authentication is the process by which the system validates a user's logon information.</span></span> <span data-ttu-id="c052a-106">Имя пользователя и пароль сравниваются с разрешенным списком, и если система обнаруживает совпадение, доступ предоставляется к экстенту, указанному в списке разрешений для этого пользователя.</span><span class="sxs-lookup"><span data-stu-id="c052a-106">A user's name and password are compared to an authorized list, and if the system detects a match, access is granted to the extent specified in the permission list for that user.</span></span>

<span data-ttu-id="c052a-107">Технологии проверки подлинности Майкрософт включают проверку подлинности LSA, Управление учетными данными, проверку подлинности смарт-карты, поставщик сети, интерфейс поставщика поддержки безопасности (SSPI), Winlogon и GINA.</span><span class="sxs-lookup"><span data-stu-id="c052a-107">Microsoft authentication technologies include LSA Authentication, Credentials Management, Smart Card Authentication, Network Provider, Security Support Provider Interface (SSPI), Winlogon, and GINA.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="c052a-108">Аудитория разработчиков</span><span class="sxs-lookup"><span data-stu-id="c052a-108">Developer audience</span></span>

<span data-ttu-id="c052a-109">Технологии проверки подлинности Майкрософт предназначены для разработчиков приложений, основанных на операционных системах Windows Server, Windows Vista и Windows, которые выполняют проверку подлинности клиентов.</span><span class="sxs-lookup"><span data-stu-id="c052a-109">Microsoft authentication technologies are intended for use by developers of applications that are based on the Windows Server, Windows Vista, and Windows operating systems that authenticate clients.</span></span> <span data-ttu-id="c052a-110">Разработчики должны быть знакомы с программированием на основе Windows.</span><span class="sxs-lookup"><span data-stu-id="c052a-110">Developers should be familiar with Windows-based programming.</span></span> <span data-ttu-id="c052a-111">Хотя это и не является обязательным, рекомендуется понимание вопросов, связанных с проверкой подлинности или безопасностью.</span><span class="sxs-lookup"><span data-stu-id="c052a-111">Although not required, an understanding of authentication or security-related subjects is advised.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="c052a-112">Требования к среде выполнения</span><span class="sxs-lookup"><span data-stu-id="c052a-112">Run-time requirements</span></span>

<span data-ttu-id="c052a-113">Сведения о требованиях времени выполнения для определенного программного элемента см. в разделе "требования" на странице справочника по этому элементу.</span><span class="sxs-lookup"><span data-stu-id="c052a-113">For information about run-time requirements for a particular programming element, see the Requirements section of the reference page for that element.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="c052a-114">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="c052a-114">In this section</span></span>



| <span data-ttu-id="c052a-115">Раздел</span><span class="sxs-lookup"><span data-stu-id="c052a-115">Topic</span></span>                                                               | <span data-ttu-id="c052a-116">Описание</span><span class="sxs-lookup"><span data-stu-id="c052a-116">Description</span></span>                                                                                                                      |
|---------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c052a-117">О проверке подлинности</span><span class="sxs-lookup"><span data-stu-id="c052a-117">About Authentication</span></span>](about-authentication.md)<br/>         | <span data-ttu-id="c052a-118">Основные понятия проверки подлинности и высокоуровневое представление технологий проверки подлинности Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="c052a-118">Key authentication concepts and a high-level view of Microsoft authentication technologies.</span></span><br/>                           |
| [<span data-ttu-id="c052a-119">Использование проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="c052a-119">Using Authentication</span></span>](using-authentication.md)<br/>         | <span data-ttu-id="c052a-120">Процессы проверки подлинности, процедуры и примеры программ, использующих технологии проверки подлинности Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="c052a-120">Authentication processes, procedures, and examples of programs that use Microsoft authentication technologies.</span></span><br/>        |
| [<span data-ttu-id="c052a-121">Справочник по проверке подлинности</span><span class="sxs-lookup"><span data-stu-id="c052a-121">Authentication Reference</span></span>](authentication-reference.md)<br/> | <span data-ttu-id="c052a-122">Подробные сведения о функциях проверки подлинности, интерфейсах, объектах, структурах и других программных элементах.</span><span class="sxs-lookup"><span data-stu-id="c052a-122">Detailed information about authentication functions, interfaces, objects, structures, and other programming elements.</span></span><br/> |



 

 

 




