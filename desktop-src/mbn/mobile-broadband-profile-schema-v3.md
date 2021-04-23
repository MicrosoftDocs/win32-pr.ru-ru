---
description: Схема профиля мобильного широкополосного подключения v3.
ms.assetid: f7a3598f-57dd-4178-896f-31b4d2f65e56
title: Схема профиля мобильного широкополосного подключения v3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea42c0c4b6384b85e5373d6537f52cf8c9499e8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897277"
---
# <a name="mobile-broadband-profile-schema-v3"></a><span data-ttu-id="4befa-103">Схема профиля мобильного широкополосного подключения v3</span><span class="sxs-lookup"><span data-stu-id="4befa-103">Mobile Broadband Profile Schema v3</span></span>

<span data-ttu-id="4befa-104">Схема профиля Windows 8Mobile широкополосной сети v3 доступна в пространстве имен `https://www.microsoft.com/networking/WWAN/profile/v3` .</span><span class="sxs-lookup"><span data-stu-id="4befa-104">The Windows 8Mobile Broadband Profile Schema v3 is available in the namespace `https://www.microsoft.com/networking/WWAN/profile/v3`.</span></span>

-   [<span data-ttu-id="4befa-105">Элементы схемы профиля Mobile широкополосной сети v3</span><span class="sxs-lookup"><span data-stu-id="4befa-105">Mobile Broadband Profile Schema v3 Elements</span></span>](mobile-broadband-profile-schema-v3-elements.md)

``` syntax
<xs:schema targetNamespace="https://www.microsoft.com/networking/WWAN/profile/v3" 
    xmlns="https://www.microsoft.com/networking/WWAN/profile/v3"  
    xmlns:xs="https://www.w3.org/2001/XMLSchema" 
    xmlns:WWAN_profile_v2="https://www.microsoft.com/networking/WWAN/profile/v2"  
    elementFormDefault="qualified"> 

    <xs:import namespace="https://www.microsoft.com/networking/WWAN/profile/v2" schemaLocation="WWAN_profile_v2.xsd"/> 

    <!-- Flag to indicate whether this is an additional PDP context profile, default is "false" --> 
    <xs:element name="IsAdditionalPdpContextProfile" type="xs:boolean"/> 
</xs:schema> 
```

 

 



