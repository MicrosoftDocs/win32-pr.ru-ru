---
description: Допустимый функциональный дескриптор безопасности содержит сведения о безопасности в двоичном формате.
ms.assetid: 8f802652-b2bf-45cf-8186-1ac31eef1fe1
title: Строки дескрипторов безопасности
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bb875bee4d35267b578193ca7cd08420722400a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154747"
---
# <a name="security-descriptor-strings"></a><span data-ttu-id="c5a82-103">Строки дескрипторов безопасности</span><span class="sxs-lookup"><span data-stu-id="c5a82-103">Security Descriptor Strings</span></span>

<span data-ttu-id="c5a82-104">Допустимый функциональный [*дескриптор безопасности*](/windows/desktop/SecGloss/s-gly) содержит сведения о безопасности в двоичном формате.</span><span class="sxs-lookup"><span data-stu-id="c5a82-104">A valid functional [*security descriptor*](/windows/desktop/SecGloss/s-gly) contains security information in binary format.</span></span> <span data-ttu-id="c5a82-105">Windows API предоставляет функции для преобразования двоичных дескрипторов безопасности в текстовые строки и из них.</span><span class="sxs-lookup"><span data-stu-id="c5a82-105">The Windows API provides functions for converting binary security descriptors to and from text strings.</span></span> <span data-ttu-id="c5a82-106">Дескрипторы безопасности в строковом формате не работают, но они могут быть полезны для хранения или переноса сведений о дескрипторах безопасности.</span><span class="sxs-lookup"><span data-stu-id="c5a82-106">Security descriptors in string format are not functional, but they can be useful for storing or transporting security descriptor information.</span></span>

<span data-ttu-id="c5a82-107">Чтобы преобразовать дескриптор безопасности в строковый формат, вызовите функцию [**конвертсекуритидескриптортострингсекуритидескриптор**](/windows/desktop/api/Sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) .</span><span class="sxs-lookup"><span data-stu-id="c5a82-107">To convert a security descriptor to a string format, call the [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) function.</span></span> <span data-ttu-id="c5a82-108">Чтобы преобразовать дескриптор безопасности строкового формата обратно в допустимый функциональный дескриптор безопасности, вызовите функцию [**конвертстрингсекуритидескриптортосекуритидескриптор**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) .</span><span class="sxs-lookup"><span data-stu-id="c5a82-108">To convert a string-format security descriptor back to a valid functional security descriptor, call the [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) function.</span></span>

<span data-ttu-id="c5a82-109">Дополнительные сведения см. в разделе [язык определения дескрипторов безопасности](security-descriptor-definition-language.md).</span><span class="sxs-lookup"><span data-stu-id="c5a82-109">For more information, see [Security Descriptor Definition Language](security-descriptor-definition-language.md).</span></span>

 

 
