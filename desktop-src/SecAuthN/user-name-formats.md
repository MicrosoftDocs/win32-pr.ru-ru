---
description: Когда приложение использует API управления учетными данными для запроса учетных данных, пользователь должен ввести данные, которые могут быть проверены либо операционной системой, либо приложением.
ms.assetid: 53ed2eb4-2c29-48fd-b7fa-0c27bf155758
title: Форматы имен пользователей
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1fb99a9e6064cd3883a8d71c1e76ca853d88661
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105651018"
---
# <a name="user-name-formats"></a><span data-ttu-id="007fd-103">Форматы имен пользователей</span><span class="sxs-lookup"><span data-stu-id="007fd-103">User Name Formats</span></span>

<span data-ttu-id="007fd-104">Когда приложение использует API управления учетными данными для запроса учетных данных, пользователь должен ввести данные, которые могут быть проверены либо операционной системой, либо приложением.</span><span class="sxs-lookup"><span data-stu-id="007fd-104">When an application uses the Credentials Management API to prompt for credentials, the user is expected to enter information that can be validated, either by the operating system or by the application.</span></span> <span data-ttu-id="007fd-105">Пользователь может указать сведения об учетных данных домена в одном из следующих форматов:</span><span class="sxs-lookup"><span data-stu-id="007fd-105">The user can specify domain credentials information in one of the following formats:</span></span>

-   [<span data-ttu-id="007fd-106">Имя участника-пользователя</span><span class="sxs-lookup"><span data-stu-id="007fd-106">User Principal Name</span></span>](#user-principal-name)
-   [<span data-ttu-id="007fd-107">Имя для входа нижнего уровня</span><span class="sxs-lookup"><span data-stu-id="007fd-107">Down-Level Logon Name</span></span>](#down-level-logon-name)

## <a name="user-principal-name"></a><span data-ttu-id="007fd-108">Имя участника-пользователя</span><span class="sxs-lookup"><span data-stu-id="007fd-108">User Principal Name</span></span>

<span data-ttu-id="007fd-109">Формат [*имени участника-пользователя*](../secgloss/u-gly.md) (UPN) используется для указания имени в формате Интернета, например <b>UserName@Example.Microsoft.com</b> .</span><span class="sxs-lookup"><span data-stu-id="007fd-109">[*User principal name*](../secgloss/u-gly.md) (UPN) format is used to specify an Internet-style name, such as <b>UserName@Example.Microsoft.com</b>.</span></span> <span data-ttu-id="007fd-110">В следующей таблице перечислены части имени участника-пользователя.</span><span class="sxs-lookup"><span data-stu-id="007fd-110">The following table summarizes the parts of a UPN.</span></span>



| <span data-ttu-id="007fd-111">Отделение</span><span class="sxs-lookup"><span data-stu-id="007fd-111">Part</span></span>                                                        | <span data-ttu-id="007fd-112">Пример</span><span class="sxs-lookup"><span data-stu-id="007fd-112">Example</span></span>                                |
|-------------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="007fd-113">Имя учетной записи пользователя.</span><span class="sxs-lookup"><span data-stu-id="007fd-113">User account name.</span></span> <span data-ttu-id="007fd-114">Также называется именем входа.</span><span class="sxs-lookup"><span data-stu-id="007fd-114">Also known as the logon name.</span></span><br/> | <span data-ttu-id="007fd-115">*UserName*</span><span class="sxs-lookup"><span data-stu-id="007fd-115">*UserName*</span></span><br/>                  |
| <span data-ttu-id="007fd-116">Двоеточи.</span><span class="sxs-lookup"><span data-stu-id="007fd-116">Separator.</span></span> <span data-ttu-id="007fd-117">Символьный литерал, символ @.</span><span class="sxs-lookup"><span data-stu-id="007fd-117">A character literal, the at sign (@).</span></span><br/> | @<br/>                           |
| <span data-ttu-id="007fd-118">Суффикс имени участника-пользователя.</span><span class="sxs-lookup"><span data-stu-id="007fd-118">UPN suffix.</span></span> <span data-ttu-id="007fd-119">Также называется доменным именем.</span><span class="sxs-lookup"><span data-stu-id="007fd-119">Also known as the domain name.</span></span><br/>       | <span data-ttu-id="007fd-120">*Example.Microsoft.com*</span><span class="sxs-lookup"><span data-stu-id="007fd-120">*Example.Microsoft.com*</span></span> <br/> |



 

<span data-ttu-id="007fd-121">Имя участника-пользователя может быть явно или явно определено.</span><span class="sxs-lookup"><span data-stu-id="007fd-121">A UPN can be implicitly or explicitly defined.</span></span> <span data-ttu-id="007fd-122">Неявное имя участника-пользователя имеет форму <b>UserName@DNSDomainName.com</b> .</span><span class="sxs-lookup"><span data-stu-id="007fd-122">An implicit UPN is of the form <b>UserName@DNSDomainName.com</b>.</span></span> <span data-ttu-id="007fd-123">Неявное имя участника-пользователя всегда связано с учетной записью пользователя, даже если явно не определено имя участника-пользователя.</span><span class="sxs-lookup"><span data-stu-id="007fd-123">An implicit UPN is always associated with the user's account, even if an explicit UPN is not defined.</span></span> <span data-ttu-id="007fd-124">Явное имя участника-пользователя — это форма <i><b>Name@Suffix</b></i> , где строки имени и суффикса явно определяются администратором.</span><span class="sxs-lookup"><span data-stu-id="007fd-124">An explicit UPN is of the form <i><b>Name@Suffix</b></i>, where both the name and suffix strings are explicitly defined by the administrator.</span></span>

## <a name="down-level-logon-name"></a><span data-ttu-id="007fd-125">Down-Level имя для входа</span><span class="sxs-lookup"><span data-stu-id="007fd-125">Down-Level Logon Name</span></span>

<span data-ttu-id="007fd-126">Формат имени входа нижнего уровня используется для указания домена и учетной записи пользователя в этом домене, например <i><b>домен \\ имя_пользователя</b></i>.</span><span class="sxs-lookup"><span data-stu-id="007fd-126">The down-level logon name format is used to specify a domain and a user account in that domain, for example, <i><b>DOMAIN\\UserName</b></i>.</span></span> <span data-ttu-id="007fd-127">В следующей таблице перечислены части имени входа нижнего уровня.</span><span class="sxs-lookup"><span data-stu-id="007fd-127">The following table summarizes the parts of a down-level logon name.</span></span>



| <span data-ttu-id="007fd-128">Отделение</span><span class="sxs-lookup"><span data-stu-id="007fd-128">Part</span></span>                                                           | <span data-ttu-id="007fd-129">Пример</span><span class="sxs-lookup"><span data-stu-id="007fd-129">Example</span></span>               |
|----------------------------------------------------------------|-----------------------|
| <span data-ttu-id="007fd-130">NetBIOS-имя домена.</span><span class="sxs-lookup"><span data-stu-id="007fd-130">NetBIOS domain name.</span></span><br/>                                | <span data-ttu-id="007fd-131">*DOMAIN*</span><span class="sxs-lookup"><span data-stu-id="007fd-131">*DOMAIN*</span></span><br/>   |
| <span data-ttu-id="007fd-132">Двоеточи.</span><span class="sxs-lookup"><span data-stu-id="007fd-132">Separator.</span></span> <span data-ttu-id="007fd-133">Символьный литерал, обратная косая черта ( \\ ).</span><span class="sxs-lookup"><span data-stu-id="007fd-133">A character literal, the backslash (\\).</span></span><br/> | **\\**<br/>     |
| <span data-ttu-id="007fd-134">Имя учетной записи пользователя.</span><span class="sxs-lookup"><span data-stu-id="007fd-134">User account name.</span></span> <span data-ttu-id="007fd-135">Также называется именем входа.</span><span class="sxs-lookup"><span data-stu-id="007fd-135">Also known as the logon name.</span></span><br/>    | <span data-ttu-id="007fd-136">*UserName*</span><span class="sxs-lookup"><span data-stu-id="007fd-136">*UserName*</span></span><br/> |



 

 

 
