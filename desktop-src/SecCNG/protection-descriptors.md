---
description: Строка правила дескриптора защиты содержит последовательный список одного или нескольких предохранителей.
ms.assetid: FBFE2143-DC40-40F3-83CE-E6D8841F9C11
title: Дескрипторы защиты
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11814df2af5bd9abee4260f4aadab5bb74c77a9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264035"
---
# <a name="protection-descriptors"></a><span data-ttu-id="dc88b-103">Дескрипторы защиты</span><span class="sxs-lookup"><span data-stu-id="dc88b-103">Protection Descriptors</span></span>

<span data-ttu-id="dc88b-104">Строка правила дескриптора защиты содержит последовательный список одного или нескольких предохранителей.</span><span class="sxs-lookup"><span data-stu-id="dc88b-104">A protection descriptor rule string contains a sequential list of one or more protectors.</span></span> <span data-ttu-id="dc88b-105">Должен быть хотя бы один предохранитель.</span><span class="sxs-lookup"><span data-stu-id="dc88b-105">There must be at least one protector.</span></span> <span data-ttu-id="dc88b-106">Если имеется более одного, то предохранители должны быть разделены в строке с помощью **и** или **или**.</span><span class="sxs-lookup"><span data-stu-id="dc88b-106">If there is more than one, the protectors must be separated in the string by **AND** or **OR**.</span></span> <span data-ttu-id="dc88b-107">Эти значения должны быть прописными.</span><span class="sxs-lookup"><span data-stu-id="dc88b-107">These values must be capitalized.</span></span> <span data-ttu-id="dc88b-108">Следующий синтаксис показывает формат строки дескриптора защиты.</span><span class="sxs-lookup"><span data-stu-id="dc88b-108">The following syntax shows the string format of a protection descriptor.</span></span>


```C++
Descriptor = [ Protector-or
              *( OR-separator Protector-or ) ]

    Protector-or = Protector-and
              *( AND-separator Protector-and )

    OR-separator = "OR"
    AND-separator = "AND"

    Protector-and = providerName EQUALS providerAttributes

    providerName = descr

    providerAttribute = string | hexstring

      ; The following characters are to be escaped when they appear
      ; in the value to be encoded: ESC, one of <escaped>, leading
      ; SHARP or SPACE, trailing SPACE, and NULL.
      string =   [ ( leadchar / pair ) [ *( stringchar / pair )
         ( trailchar / pair ) ] ]

      leadchar = LUTF1 / UTFMB
      LUTF1 = %x01-1F / %x21 / %x24-2A / %x2D-3A / %x3D / %x3F-5B / %x5D-7F

      trailchar  = TUTF1 / UTFMB
      TUTF1 = %x01-1F / %x21 / %x23-2A / %x2D-3A / %x3D / %x3F-5B / %x5D-7F

      stringchar = SUTF1 / UTFMB
      SUTF1 = %x01-21 / %x23-2A / %x2D-3A / %x3D / %x3F-5B / %x5D-7F

      pair = ESC ( ESC / special / hexpair )
      special = escaped / SPACE / SHARP / EQUALS
      escaped = DQUOTE / PLUS / COMMA / SEMI / LANGLE / RANGLE
      hexstring = SHARP 1*hexpair
      hexpair = HEX HEX

      descr   = leadkeychar *keychar
      leadkeychar = ALPHA
      keychar = ALPHA / DIGIT / HYPHEN
      number  = DIGIT / ( LDIGIT 1*DIGIT )

      ALPHA   = %x41-5A / %x61-7A   ; "A"-"Z" / "a"-"z"
      DIGIT   = %x30 / LDIGIT       ; "0"-"9"
      LDIGIT  = %x31-39             ; "1"-"9"
      HEX     = DIGIT / %x41-46 / %x61-66 ; "0"-"9" / "A"-"F" / "a"-"f"

      NULL    = %x00 ; null (0)
      SPACE   = %x20 ; space (" ")
      DQUOTE  = %x22 ; quote (""")
      SHARP   = %x23 ; octothorpe (or sharp sign) ("#")
      DOLLAR  = %x24 ; dollar sign ("$")
      SQUOTE  = %x27 ; single quote ("'")
      LPAREN  = %x28 ; left paren ("(")
      RPAREN  = %x29 ; right paren (")")
      PLUS    = %x2B ; plus sign ("+")
      COMMA   = %x2C ; comma (",")
      HYPHEN  = %x2D ; hyphen ("-")
      DOT     = %x2E ; period (".")
      SEMI    = %x3B ; semicolon (";")
      LANGLE  = %x3C ; left angle bracket ("<")
      EQUALS  = %x3D ; equals sign ("=")
      RANGLE  = %x3E ; right angle bracket (">")
      ESC     = %x5C ; backslash ("\")
      USCORE  = %x5F ; underscore ("_")
      LCURLY  = %x7B ; left curly brace "{"
      RCURLY  = %x7D ; right curly brace "}"

      ; Any UTF-8 [RFC3629] encoded Unicode [Unicode] character
      UTF8    = UTF1 / UTFMB
      UTFMB   = UTF2 / UTF3 / UTF4
      UTF0    = %x80-BF
      UTF1    = %x00-7F
      UTF2    = %xC2-DF UTF0
      UTF3    = %xE0 %xA0-BF UTF0 / %xE1-EC 2(UTF0) /
                %xED %x80-9F UTF0 / %xEE-EF 2(UTF0)
      UTF4    = %xF0 %x90-BF 2(UTF0) / %xF1-F3 3(UTF0) /
                %xF4 %x80-8F 2(UTF0)

      OCTET   = %x00-FF ; Any octet (8-bit data unit)
```



<span data-ttu-id="dc88b-109">Дескрипторы защиты в настоящее время можно определить для следующих типов авторизации:</span><span class="sxs-lookup"><span data-stu-id="dc88b-109">Protection descriptors can currently be defined for the following types of authorization:</span></span>

-   <span data-ttu-id="dc88b-110">Группа в лесу Active Directory.</span><span class="sxs-lookup"><span data-stu-id="dc88b-110">A group in an Active Directory forest.</span></span>
-   <span data-ttu-id="dc88b-111">Набор учетных данных веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="dc88b-111">A set of web credentials.</span></span>
-   <span data-ttu-id="dc88b-112">Сертификат в хранилище сертификатов пользователя.</span><span class="sxs-lookup"><span data-stu-id="dc88b-112">A certificate in the user's certificate store.</span></span>

<span data-ttu-id="dc88b-113">Примеры строк правил дескриптора защиты для группы Active Directory включают следующее.</span><span class="sxs-lookup"><span data-stu-id="dc88b-113">Examples of protection descriptor rule strings for an Active Directory group include the following:</span></span>

-   <span data-ttu-id="dc88b-114">"SID = S-1-5-21-4392301 И SID = S-1-5-21-3101812"</span><span class="sxs-lookup"><span data-stu-id="dc88b-114">"SID=S-1-5-21-4392301 AND SID=S-1-5-21-3101812"</span></span>
-   <span data-ttu-id="dc88b-115">"SDDL = O:S-1-5-5-0-290724G: SYD: (A;; ККДК;;; S-1-5-5-0-290724) (A;;D C;;; WD) "</span><span class="sxs-lookup"><span data-stu-id="dc88b-115">"SDDL=O:S-1-5-5-0-290724G:SYD:(A;;CCDC;;;S-1-5-5-0-290724)(A;;DC;;;WD)"</span></span>
-   <span data-ttu-id="dc88b-116">"Локальный = пользователь"</span><span class="sxs-lookup"><span data-stu-id="dc88b-116">"LOCAL=user"</span></span>
-   <span data-ttu-id="dc88b-117">"Локальный = компьютер"</span><span class="sxs-lookup"><span data-stu-id="dc88b-117">"LOCAL=machine"</span></span>

<span data-ttu-id="dc88b-118">Примеры строк правил дескриптора защиты для набора веб-учетных данных включают следующее.</span><span class="sxs-lookup"><span data-stu-id="dc88b-118">Examples of protection descriptor rule strings for a set of web credentials include the following:</span></span>

-   <span data-ttu-id="dc88b-119">"CREDENTIALs = Мипассворднаме"</span><span class="sxs-lookup"><span data-stu-id="dc88b-119">"WEBCREDENTIALS=MyPasswordName"</span></span>
-   <span data-ttu-id="dc88b-120">"CREDENTIALs = Мипассворднаме, мивеб. com"</span><span class="sxs-lookup"><span data-stu-id="dc88b-120">"WEBCREDENTIALS=MyPasswordName,myweb.com"</span></span>

<span data-ttu-id="dc88b-121">Примеры строк правила дескриптора защиты для сертификата включают следующее.</span><span class="sxs-lookup"><span data-stu-id="dc88b-121">Examples of protection descriptor rule strings for a certificate include the following:</span></span>

-   <span data-ttu-id="dc88b-122">"CERTIFICATE = Хашид: \_ хэш SHA1 \_ для \_ сертификата"</span><span class="sxs-lookup"><span data-stu-id="dc88b-122">"CERTIFICATE=HashID:sha1\_hash\_of\_certificate"</span></span>
-   <span data-ttu-id="dc88b-123">"CERTIFICATE = Цертблоб: base64String"</span><span class="sxs-lookup"><span data-stu-id="dc88b-123">"CERTIFICATE=CertBlob:base64String"</span></span>

<span data-ttu-id="dc88b-124">Указанный вами дескриптор защиты автоматически определяет, какой поставщик защиты ключей используется.</span><span class="sxs-lookup"><span data-stu-id="dc88b-124">The protection descriptor you specify automatically determines which key protection provider is used.</span></span> <span data-ttu-id="dc88b-125">Дополнительные сведения см. в разделе [поставщики защиты](protection-providers.md).</span><span class="sxs-lookup"><span data-stu-id="dc88b-125">For more information, see [Protection Providers](protection-providers.md).</span></span>

<span data-ttu-id="dc88b-126">Обратите внимание, что левая часть знака равенства (=) должна быть равна **SID**, **SDDL**, **Local**, **Credential** или **Certificate**.</span><span class="sxs-lookup"><span data-stu-id="dc88b-126">Note that the left side of the equals sign (=) must be **SID**, **SDDL**, **LOCAL**, **WEBCREDENTIALS**, or **CERTIFICATE**.</span></span> <span data-ttu-id="dc88b-127">В значениях регистр не учитывается.</span><span class="sxs-lookup"><span data-stu-id="dc88b-127">These values are not case sensitive.</span></span>

<span data-ttu-id="dc88b-128">При вызове функции [**нкрипткреатепротектиондескриптор**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptcreateprotectiondescriptor) необходимо указать строку правила (или отображаемое имя, связанное со строкой правила).</span><span class="sxs-lookup"><span data-stu-id="dc88b-128">You must specify a rule string (or a display name associated with a rule string) when you call the [**NCryptCreateProtectionDescriptor**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptcreateprotectiondescriptor) function.</span></span> <span data-ttu-id="dc88b-129">Кроме того, так как строки правил дескриптора защиты достаточно громоздки для использования и запоминаются, можно связать отображаемое имя со строкой правила и зарегистрировать оба метода с помощью функции [**нкриптрегистерпротектиондескрипторнаме**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptregisterprotectiondescriptorname) .</span><span class="sxs-lookup"><span data-stu-id="dc88b-129">Alternatively, because protection descriptor rule strings are somewhat cumbersome to use and remember, you can associate a display name with the rule string and register both by using the [**NCryptRegisterProtectionDescriptorName**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptregisterprotectiondescriptorname) function.</span></span> <span data-ttu-id="dc88b-130">Затем можно использовать отображаемое имя в **нкрипткреатепротектиондескриптор**.</span><span class="sxs-lookup"><span data-stu-id="dc88b-130">Then you can use the display name in **NCryptCreateProtectionDescriptor**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dc88b-131">См. также</span><span class="sxs-lookup"><span data-stu-id="dc88b-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dc88b-132">CNG DPAPI</span><span class="sxs-lookup"><span data-stu-id="dc88b-132">CNG DPAPI</span></span>](cng-dpapi.md)
</dt> <dt>

[<span data-ttu-id="dc88b-133">Поставщики защиты</span><span class="sxs-lookup"><span data-stu-id="dc88b-133">Protection Providers</span></span>](protection-providers.md)
</dt> </dl>

 

 



