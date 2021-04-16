---
description: Список требований, принудительно применяемых средствами администрирования системы надежных паролей.
ms.assetid: a84f83b2-181b-4f65-82bd-bc7f0689aad3
title: Принудительное применение надежных паролей и Passfilt.dll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63b7be524511d52048e06ae83ab110384c3bf5c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540967"
---
# <a name="strong-password-enforcement-and-passfiltdll"></a><span data-ttu-id="54c06-103">Принудительное применение надежных паролей и Passfilt.dll</span><span class="sxs-lookup"><span data-stu-id="54c06-103">Strong Password Enforcement and Passfilt.dll</span></span>

<span data-ttu-id="54c06-104">Принудительное применение надежных паролей можно включить с помощью средств системного администрирования.</span><span class="sxs-lookup"><span data-stu-id="54c06-104">Strong password enforcement can be enabled by using the system administration tools.</span></span> <span data-ttu-id="54c06-105">Если политика системного администрирования включена, пароли должны удовлетворять следующим минимальным требованиям при их создании или изменении.</span><span class="sxs-lookup"><span data-stu-id="54c06-105">If the system administration policy is enabled, passwords must meet the following minimum requirements when they are created or changed:</span></span>

-   <span data-ttu-id="54c06-106">Пароли не могут содержать значение samAccountName (имя учетной записи) пользователя или полное значение displayName (полное имя).</span><span class="sxs-lookup"><span data-stu-id="54c06-106">Passwords may not contain the user's samAccountName (Account Name) value or entire displayName (Full Name value).</span></span> <span data-ttu-id="54c06-107">В обеих проверках регистр не учитывается.</span><span class="sxs-lookup"><span data-stu-id="54c06-107">Both checks are not case sensitive.</span></span>
-   <span data-ttu-id="54c06-108">Значение samAccountName проверяется целиком только для того, чтобы определить, является ли он частью пароля.</span><span class="sxs-lookup"><span data-stu-id="54c06-108">The samAccountName is checked in its entirety only to determine whether it is part of the password.</span></span> <span data-ttu-id="54c06-109">Если значение samAccountName меньше трех символов, эта проверка пропускается.</span><span class="sxs-lookup"><span data-stu-id="54c06-109">If the samAccountName is less than three characters long, this check is skipped.</span></span>
-   <span data-ttu-id="54c06-110">DisplayName анализируется для разделителей: запятые, точки, тире или дефисы, символы подчеркивания, пробелы, знаки фунта и табуляции.</span><span class="sxs-lookup"><span data-stu-id="54c06-110">The displayName is parsed for delimiters: commas, periods, dashes or hyphens, underscores, spaces, pound signs, and tabs.</span></span> <span data-ttu-id="54c06-111">Если какой-либо из этих разделителей найден, то раздел displayName разбивается, а все проанализированные разделы (токены) подтверждаются без включения в пароль.</span><span class="sxs-lookup"><span data-stu-id="54c06-111">If any of these delimiters are found, the displayName is split and all parsed sections (tokens) are confirmed to not be included in the password.</span></span> <span data-ttu-id="54c06-112">Маркеры, которые меньше трех символов, игнорируются, а подстроки токенов не проверяются.</span><span class="sxs-lookup"><span data-stu-id="54c06-112">Tokens that are less than three characters are ignored, and substrings of the tokens are not checked.</span></span> <span data-ttu-id="54c06-113">Например, имя "Эрин M. Хаженс" разбивается на три токена: "Эрин", "M" и "Хаженс".</span><span class="sxs-lookup"><span data-stu-id="54c06-113">For example, the name "Erin M. Hagens" is split into three tokens: "Erin", "M", and "Hagens".</span></span> <span data-ttu-id="54c06-114">Так как второй маркер состоит только из одного символа, он игнорируется.</span><span class="sxs-lookup"><span data-stu-id="54c06-114">Because the second token is only one character long, it is ignored.</span></span> <span data-ttu-id="54c06-115">Таким образом, этот пользователь не может иметь пароль, включающий "Эрин" или "хаженс" в качестве подстроки в любом месте пароля.</span><span class="sxs-lookup"><span data-stu-id="54c06-115">Therefore, this user could not have a password that included either "erin" or "hagens" as a substring anywhere in the password.</span></span>
-   <span data-ttu-id="54c06-116">Пароли должны содержать символы из трех из пяти следующих категорий.</span><span class="sxs-lookup"><span data-stu-id="54c06-116">Passwords must contain characters from three of the five following categories.</span></span>



| <span data-ttu-id="54c06-117">Категории символов</span><span class="sxs-lookup"><span data-stu-id="54c06-117">Character categories</span></span>                                                                                                                                                      | <span data-ttu-id="54c06-118">Примеры</span><span class="sxs-lookup"><span data-stu-id="54c06-118">Examples</span></span>                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="54c06-119">Прописные буквы в европейских языках (от A до Z, диакритические знаки, греческие и кириллические символы)</span><span class="sxs-lookup"><span data-stu-id="54c06-119">Uppercase letters of European languages (A through Z, with diacritic marks, Greek and Cyrillic characters)</span></span><br/>                                                     | <span data-ttu-id="54c06-120">A, B, C, Z</span><span class="sxs-lookup"><span data-stu-id="54c06-120">A, B, C,   Z</span></span><br/>                |
| <span data-ttu-id="54c06-121">Строчные буквы европейских языков (a – z, диез-s, диакритические знаки, греческие и кириллица)</span><span class="sxs-lookup"><span data-stu-id="54c06-121">Lowercase letters of European languages (a through z, sharp-s, with diacritic marks, Greek and Cyrillic characters)</span></span><br/>                                            | <span data-ttu-id="54c06-122">a, b, c, z</span><span class="sxs-lookup"><span data-stu-id="54c06-122">a, b, c,   z</span></span><br/>                |
| <span data-ttu-id="54c06-123">цифры (0-9)</span><span class="sxs-lookup"><span data-stu-id="54c06-123">Base 10 digits (0 through 9)</span></span><br/>                                                                                                                                   | <span data-ttu-id="54c06-124">0, 1, 2, 9</span><span class="sxs-lookup"><span data-stu-id="54c06-124">0, 1, 2,   9</span></span><br/>                |
| <span data-ttu-id="54c06-125">Символы, отличные от алфавитно-цифровых (специальные символы)</span><span class="sxs-lookup"><span data-stu-id="54c06-125">Non-alphanumeric characters (special characters)</span></span><br/>                                                                                                               | <span data-ttu-id="54c06-126">$,!,%, ^, () {} \[ \] ;: <>?</span><span class="sxs-lookup"><span data-stu-id="54c06-126">$,!,%,^,(){}\[\];:<>?</span></span><br/> |
| <span data-ttu-id="54c06-127">Любой символ Юникода, классифицированный как буквенный символ, но не являющийся прописной буквой или строчной буквой.</span><span class="sxs-lookup"><span data-stu-id="54c06-127">Any Unicode character that is categorized as an alphabetic character but is not uppercase or lowercase.</span></span> <span data-ttu-id="54c06-128">Сюда входят символы Юникода из азиатских языков.</span><span class="sxs-lookup"><span data-stu-id="54c06-128">This includes Unicode characters from Asian languages.</span></span><br/> |                                        |



 

<span data-ttu-id="54c06-129">**Включение принудительного применения надежных паролей**</span><span class="sxs-lookup"><span data-stu-id="54c06-129">**To enable strong password enforcement**</span></span>

1.  <span data-ttu-id="54c06-130">В консоли администрирования выберите **Локальная политика безопасности**.</span><span class="sxs-lookup"><span data-stu-id="54c06-130">From the administration console, locate **Local Security Policy**.</span></span>
2.  <span data-ttu-id="54c06-131">Выберите **Политика учетной записи**, а затем выберите **Политика паролей**.</span><span class="sxs-lookup"><span data-stu-id="54c06-131">Select **Account Policy**, and then select **Password Policy**.</span></span>
3.  <span data-ttu-id="54c06-132">Включение **паролей должно соответствовать параметру требования сложности** .</span><span class="sxs-lookup"><span data-stu-id="54c06-132">Enable the **Passwords must meet complexity requirements** setting.</span></span>

> [!Note]  
> <span data-ttu-id="54c06-133">Заданный символ может соответствовать только одной категории.</span><span class="sxs-lookup"><span data-stu-id="54c06-133">A given character can satisfy only one category.</span></span> <span data-ttu-id="54c06-134">Функция [жетстрингтипев](/windows/win32/api/stringapiset/nf-stringapiset-getstringtypew) используется для проверки, является ли каждый символ в пароле прописными, строчными или буквенно-цифровыми.</span><span class="sxs-lookup"><span data-stu-id="54c06-134">The [GetStringTypeW](/windows/win32/api/stringapiset/nf-stringapiset-getstringtypew) function is used to test whether each character in the password is uppercase, lowercase, or alphanumeric.</span></span>

 

 

