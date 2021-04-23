---
description: Перед реализацией кода, защищающего пароли, лучше проанализировать конкретную среду, чтобы злоумышленники могли попытаться проникнуть защиту программного обеспечения.
ms.assetid: 4ebf7185-0179-4754-80da-63b0002c883f
title: Оценка угроз паролей
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d48a79d44bda9714083c5dd1085e9d09497e7341
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664571"
---
# <a name="password-threat-assessment"></a><span data-ttu-id="aae17-103">Оценка угроз паролей</span><span class="sxs-lookup"><span data-stu-id="aae17-103">Password Threat Assessment</span></span>

<span data-ttu-id="aae17-104">Перед реализацией кода, защищающего пароли, лучше проанализировать конкретную среду, чтобы злоумышленники могли попытаться проникнуть защиту программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="aae17-104">Before implementing code that protects passwords, it is best to analyze your particular environment for ways that an attacker might try to penetrate software defenses.</span></span>

<span data-ttu-id="aae17-105">Начните с анализа архитектуры сети или системы.</span><span class="sxs-lookup"><span data-stu-id="aae17-105">Start by analyzing your network or system architecture.</span></span> <span data-ttu-id="aae17-106">Ниже приводится несколько примеров.</span><span class="sxs-lookup"><span data-stu-id="aae17-106">Here are some examples:</span></span>

-   <span data-ttu-id="aae17-107">Число паролей, которые должны быть защищены.</span><span class="sxs-lookup"><span data-stu-id="aae17-107">The number of passwords that must be protected.</span></span> <span data-ttu-id="aae17-108">Требуется ли пароль для входа на локальный компьютер?</span><span class="sxs-lookup"><span data-stu-id="aae17-108">Is a password required to log on to the local computer?</span></span> <span data-ttu-id="aae17-109">Используется ли тот же пароль для входа в сеть?</span><span class="sxs-lookup"><span data-stu-id="aae17-109">Is the same password used to log on to the network?</span></span> <span data-ttu-id="aae17-110">Распространяются ли пароли на несколько серверов в сети?</span><span class="sxs-lookup"><span data-stu-id="aae17-110">Are passwords propagated to more than one server on the network?</span></span> <span data-ttu-id="aae17-111">Сколько паролей должно соответствовать?</span><span class="sxs-lookup"><span data-stu-id="aae17-111">How many passwords must be accommodated?</span></span>
-   <span data-ttu-id="aae17-112">Тип сети (если есть), которая будет использоваться.</span><span class="sxs-lookup"><span data-stu-id="aae17-112">The kind of network (if any) that will be used.</span></span> <span data-ttu-id="aae17-113">Используется ли сеть, реализованная с помощью корпоративной системы каталогов (например, LDAP) и используемая ли архитектура паролей?</span><span class="sxs-lookup"><span data-stu-id="aae17-113">Is the network implemented using a corporate directory system (such as LDAP), and is its password architecture used?</span></span> <span data-ttu-id="aae17-114">Все ли объекты хранят незашифрованные пароли?</span><span class="sxs-lookup"><span data-stu-id="aae17-114">Are any objects storing unencrypted passwords?</span></span>
-   <span data-ttu-id="aae17-115">Открытая и закрытая сеть.</span><span class="sxs-lookup"><span data-stu-id="aae17-115">Open versus closed network.</span></span> <span data-ttu-id="aae17-116">Является ли сеть автономной или она открыта снаружи?</span><span class="sxs-lookup"><span data-stu-id="aae17-116">Is the network self-contained or is it open to the outside?</span></span> <span data-ttu-id="aae17-117">Если да, защищен ли он брандмауэром?</span><span class="sxs-lookup"><span data-stu-id="aae17-117">If so, is it protected by a firewall?</span></span>
-   <span data-ttu-id="aae17-118">Удаленный доступ.</span><span class="sxs-lookup"><span data-stu-id="aae17-118">Remote access.</span></span> <span data-ttu-id="aae17-119">Будут ли пользователи получать доступ к сети из удаленного расположения?</span><span class="sxs-lookup"><span data-stu-id="aae17-119">Will users need to access the network from a remote location?</span></span>

<span data-ttu-id="aae17-120">После анализа архитектуры системы или сети можно начать анализировать, как злоумышленник может попытаться атаковать ее.</span><span class="sxs-lookup"><span data-stu-id="aae17-120">After you have analyzed your system or network architecture, then you can start to analyze how an attacker might try to attack it.</span></span> <span data-ttu-id="aae17-121">Ниже приведены некоторые возможности.</span><span class="sxs-lookup"><span data-stu-id="aae17-121">Here are some possibilities:</span></span>

-   <span data-ttu-id="aae17-122">Чтение незашифрованного пароля из реестра компьютера.</span><span class="sxs-lookup"><span data-stu-id="aae17-122">Read an unencrypted password from a computer's registry.</span></span>
-   <span data-ttu-id="aae17-123">Считывает незашифрованный пароль, жестко заданный в программном обеспечении.</span><span class="sxs-lookup"><span data-stu-id="aae17-123">Read an unencrypted password that is hard-coded in the software.</span></span>
-   <span data-ttu-id="aae17-124">Чтение незашифрованного пароля с переопределенной кодовой страницы компьютера.</span><span class="sxs-lookup"><span data-stu-id="aae17-124">Read an unencrypted password from a computer's swapped-out code page.</span></span>
-   <span data-ttu-id="aae17-125">Чтение пароля из журнала событий программы.</span><span class="sxs-lookup"><span data-stu-id="aae17-125">Read a password from a program's event log.</span></span>
-   <span data-ttu-id="aae17-126">Чтение пароля из расширенной схемы службы каталогов Microsoft Active Directory, которая содержит объекты, содержащие пароль в виде открытого текста.</span><span class="sxs-lookup"><span data-stu-id="aae17-126">Read a password from an extended Microsoft Active Directory directory service schema that has objects that contain a plaintext password.</span></span>
-   <span data-ttu-id="aae17-127">Запустите отладчик в программе, для которой требуется пароль.</span><span class="sxs-lookup"><span data-stu-id="aae17-127">Run a debugger on a program that requires a password.</span></span>
-   <span data-ttu-id="aae17-128">Подобрать пароль.</span><span class="sxs-lookup"><span data-stu-id="aae17-128">Guess a password.</span></span> <span data-ttu-id="aae17-129">Можно использовать любой из нескольких методов.</span><span class="sxs-lookup"><span data-stu-id="aae17-129">Any of several techniques might be used.</span></span> <span data-ttu-id="aae17-130">Например, злоумышленник может знать некоторые персональные сведения о пользователе и попытаться угадать пароль из этой информации (например, имя супруга, партнера или ребенка).</span><span class="sxs-lookup"><span data-stu-id="aae17-130">For example, the attacker might know some personal information about a user and try to guess a password from that information (for example, the name of a spouse/partner or child).</span></span> <span data-ttu-id="aae17-131">Или же можно попытаться выполнить метод подбора, где будут выполняться все комбинации букв, цифр и знаков препинания (возможно, только если используются короткие пароли).</span><span class="sxs-lookup"><span data-stu-id="aae17-131">Or, a brute-force method might be tried, where all combinations of letters, numbers, and punctuation are tried (only feasible where short passwords are used).</span></span>

<span data-ttu-id="aae17-132">Сравнение возможных методологий атаки с архитектурой системы или сети, скорее всего, приведет к угрозам безопасности.</span><span class="sxs-lookup"><span data-stu-id="aae17-132">Comparing the possible attack methodologies with system or network architecture will likely reveal security risks.</span></span> <span data-ttu-id="aae17-133">На этом этапе можно установить фактор риска для каждого риска, а факторы риска можно использовать для рассмотрения исправлений.</span><span class="sxs-lookup"><span data-stu-id="aae17-133">At that point, a risk factor can be established for each risk, and the risk factors can be used to triage fixes.</span></span>

 

 



