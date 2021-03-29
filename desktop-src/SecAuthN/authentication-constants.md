---
description: Список констант, используемых для API проверки подлинности Майкрософт.
ms.assetid: 3e5b7fd8-01bf-4090-b68f-006b7e2228a9
title: Константы проверки подлинности (проверка подлинности)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d671f356f11ccaf1f5aece1dc1168d3106d578c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105647553"
---
# <a name="authentication-constants-authentication"></a><span data-ttu-id="10934-103">Константы проверки подлинности (проверка подлинности)</span><span class="sxs-lookup"><span data-stu-id="10934-103">Authentication Constants (Authentication)</span></span>

## <a name="credentials-management-constants"></a><span data-ttu-id="10934-104">Константы управления учетными данными</span><span class="sxs-lookup"><span data-stu-id="10934-104">Credentials Management Constants</span></span>

<span data-ttu-id="10934-105">Для указания максимального размера строки в управлении учетными данными используются следующие константы.</span><span class="sxs-lookup"><span data-stu-id="10934-105">Credentials Management uses the following constants to specify maximum string sizes.</span></span>



| <span data-ttu-id="10934-106">Константа</span><span class="sxs-lookup"><span data-stu-id="10934-106">Constant</span></span>                                        | <span data-ttu-id="10934-107">Описание</span><span class="sxs-lookup"><span data-stu-id="10934-107">Description</span></span>                                                                                                                   |
|-------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10934-108">\_Максимальная \_ Длина сообщения \_ CREDUI</span><span class="sxs-lookup"><span data-stu-id="10934-108">CREDUI\_MAX\_MESSAGE\_LENGTH</span></span><br/>         | <span data-ttu-id="10934-109">Максимальное число символов для элемента **псзмессажетекст** структуры [**CREDUI \_ info**](/windows/desktop/api/WinCred/ns-wincred-credui_infoa) .</span><span class="sxs-lookup"><span data-stu-id="10934-109">Maximum number of characters for the **pszMessageText** member of a [**CREDUI\_INFO**](/windows/desktop/api/WinCred/ns-wincred-credui_infoa) structure.</span></span><br/> |
| <span data-ttu-id="10934-110">\_Максимальная \_ Длина заголовка \_ CREDUI</span><span class="sxs-lookup"><span data-stu-id="10934-110">CREDUI\_MAX\_CAPTION\_LENGTH</span></span><br/>         | <span data-ttu-id="10934-111">Максимальное число символов для элемента **псзкаптионтекст** структуры [**CREDUI \_ info**](/windows/desktop/api/WinCred/ns-wincred-credui_infoa) .</span><span class="sxs-lookup"><span data-stu-id="10934-111">Maximum number of characters for the **pszCaptionText** member of a [**CREDUI\_INFO**](/windows/desktop/api/WinCred/ns-wincred-credui_infoa) structure.</span></span><br/> |
| <span data-ttu-id="10934-112">\_Максимальная \_ Общая \_ ЦЕЛЕВая \_ Длина CREDUI</span><span class="sxs-lookup"><span data-stu-id="10934-112">CREDUI\_MAX\_GENERIC\_TARGET\_LENGTH</span></span><br/> | <span data-ttu-id="10934-113">Максимальное число символов в строке, которое указывает целевое имя.</span><span class="sxs-lookup"><span data-stu-id="10934-113">Maximum number of characters in a string that specifies a target name.</span></span><br/>                                             |
| <span data-ttu-id="10934-114">\_Максимальная \_ \_ Длина целевого объекта \_ домена CREDUI</span><span class="sxs-lookup"><span data-stu-id="10934-114">CREDUI\_MAX\_DOMAIN\_TARGET\_LENGTH</span></span><br/>  | <span data-ttu-id="10934-115">Максимальное число символов в строке, которое указывает доменное имя.</span><span class="sxs-lookup"><span data-stu-id="10934-115">Maximum number of characters in a string that specifies a domain name.</span></span><br/>                                             |
| <span data-ttu-id="10934-116">CREDUI \_ Максимальная \_ Длина имени пользователя \_</span><span class="sxs-lookup"><span data-stu-id="10934-116">CREDUI\_MAX\_USERNAME\_LENGTH</span></span><br/>        | <span data-ttu-id="10934-117">Максимальное число символов в строке, которое указывает имя учетной записи пользователя.</span><span class="sxs-lookup"><span data-stu-id="10934-117">Maximum number of characters in a string that specifies a user account name.</span></span><br/>                                       |
| <span data-ttu-id="10934-118">\_Максимальная \_ Длина пароля \_ CREDUI</span><span class="sxs-lookup"><span data-stu-id="10934-118">CREDUI\_MAX\_PASSWORD\_LENGTH</span></span><br/>        | <span data-ttu-id="10934-119">Максимальное число символов в строке, которое указывает пароль.</span><span class="sxs-lookup"><span data-stu-id="10934-119">Maximum number of characters in a string that specifies a password.</span></span><br/>                                                |



 

## <a name="gina-defined-values"></a><span data-ttu-id="10934-120">Определенные в GINA значения</span><span class="sxs-lookup"><span data-stu-id="10934-120">Gina Defined Values</span></span>

<span data-ttu-id="10934-121">Функции интерфейса [*GINA*](/windows/desktop/SecGloss/g-gly) и функции поддержки [*Winlogon*](/windows/desktop/SecGloss/w-gly) используют следующие определенные значения.</span><span class="sxs-lookup"><span data-stu-id="10934-121">[*GINA*](/windows/desktop/SecGloss/g-gly) interface functions and [*Winlogon*](/windows/desktop/SecGloss/w-gly) support functions use the following defined values.</span></span>

> [!Note]  
> <span data-ttu-id="10934-122">Библиотеки DLL GINA не учитываются в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="10934-122">GINA DLLs are ignored in Windows Vista.</span></span>

 



| <span data-ttu-id="10934-123">Значение</span><span class="sxs-lookup"><span data-stu-id="10934-123">Value</span></span>                                                              | <span data-ttu-id="10934-124">Описание</span><span class="sxs-lookup"><span data-stu-id="10934-124">Description</span></span>                                                                                                                          |
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="10934-125">**\_параметр входа \_ влкс \_ xxx**</span><span class="sxs-lookup"><span data-stu-id="10934-125">**WLX\_LOGON\_OPTION\_XXX**</span></span>](wlx-logon-option-xxx.md)<br/> | <span data-ttu-id="10934-126">Содержит стандартные параметры входа в систему.</span><span class="sxs-lookup"><span data-stu-id="10934-126">Contains predefined logon options.</span></span> <span data-ttu-id="10934-127">Он используется параметром *двоптионс* параметра [**влкслогжедаутсас**](/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedoutsas).</span><span class="sxs-lookup"><span data-stu-id="10934-127">It is used by the *dwOptions* parameter of [**WlxLoggedOutSAS**](/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedoutsas).</span></span><br/> |
| [<span data-ttu-id="10934-128">**\_тип SAS \_ влкс \_ xxx**</span><span class="sxs-lookup"><span data-stu-id="10934-128">**WLX\_SAS\_TYPE\_XXX**</span></span>](wlx-sas-type-xxx.md)<br/>         | <span data-ttu-id="10934-129">Определяет конкретный тип SAS.</span><span class="sxs-lookup"><span data-stu-id="10934-129">Defines a specific SAS type.</span></span><br/>                                                                                              |



 

 

