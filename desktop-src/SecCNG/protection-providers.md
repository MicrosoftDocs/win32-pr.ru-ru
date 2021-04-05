---
description: Начиная с Windows 8, корпорация Майкрософт приступила к распространению поставщиков, позволяющих безопасно обмениваться зашифрованными секретными данными и сообщениями на разных компьютерах.
ms.assetid: C2E62DD2-8316-407B-B879-2617873F8409
title: Поставщики защиты
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc2c262fcfbfa5ab0842f103849af3d67b20f8e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991621"
---
# <a name="protection-providers"></a><span data-ttu-id="2b18a-103">Поставщики защиты</span><span class="sxs-lookup"><span data-stu-id="2b18a-103">Protection Providers</span></span>

<span data-ttu-id="2b18a-104">Начиная с Windows 8, корпорация Майкрософт приступила к распространению поставщиков, позволяющих безопасно обмениваться зашифрованными секретными данными и сообщениями на разных компьютерах.</span><span class="sxs-lookup"><span data-stu-id="2b18a-104">Beginning with Windows 8, Microsoft began distributing the providers that enable you to securely share encrypted secrets and messages across computers.</span></span> <span data-ttu-id="2b18a-105">В настоящее время существует два поставщика защиты ключей.</span><span class="sxs-lookup"><span data-stu-id="2b18a-105">There are currently two key protection providers.</span></span> <span data-ttu-id="2b18a-106">Поставщик защиты ключей (Майкрософт) позволяет защищать содержимое в группе в Active Directoryном лесу.</span><span class="sxs-lookup"><span data-stu-id="2b18a-106">The Microsoft Key Protection provider allows you to protect content to a group in an Active Directory forest.</span></span> <span data-ttu-id="2b18a-107">Поставщик защиты ключей клиентов Майкрософт позволяет защищать содержимое с помощью набора учетных данных веб-служб.</span><span class="sxs-lookup"><span data-stu-id="2b18a-107">The Microsoft Client Key Protection provider allows you to protect content to a set of web credentials.</span></span>

<span data-ttu-id="2b18a-108">Правильный выбор предохранителя автоматически выбирается, когда функция [**нкрипткреатепротектиондескриптор**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptcreateprotectiondescriptor) анализирует строку правила дескриптора защиты, которую вы указали как входные данные.</span><span class="sxs-lookup"><span data-stu-id="2b18a-108">The correct protector to use is automatically chosen for you when the [**NCryptCreateProtectionDescriptor**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptcreateprotectiondescriptor) function parses the protection descriptor rule string your provide as input.</span></span> <span data-ttu-id="2b18a-109">Поставщик защиты ключей (Майкрософт) выбирается для строк правил, начинающихся с SID, SDDL и LOCAL.</span><span class="sxs-lookup"><span data-stu-id="2b18a-109">The Microsoft Key Protection provider is chosen for rule strings that begin with SID, SDDL, and LOCAL.</span></span> <span data-ttu-id="2b18a-110">Поставщик защиты ключей клиентов Майкрософт анализирует строки правил, которые начинаются с УЧЕТных данных веб.</span><span class="sxs-lookup"><span data-stu-id="2b18a-110">The Microsoft Client Key Protection provider parses rule strings that begin with WEBCREDENTIALS.</span></span> <span data-ttu-id="2b18a-111">Дополнительные сведения о строках правил см. в разделе [дескрипторы защиты](protection-descriptors.md).</span><span class="sxs-lookup"><span data-stu-id="2b18a-111">For more information about rule strings, see [Protection Descriptors](protection-descriptors.md).</span></span>

> [!Note]  
> <span data-ttu-id="2b18a-112">В настоящее время настраиваемые поставщики не разрешены. [CNG DPAPI](cng-dpapi.md)</span><span class="sxs-lookup"><span data-stu-id="2b18a-112">Custom providers are not currently allowed.[CNG DPAPI](cng-dpapi.md)</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="2b18a-113">См. также</span><span class="sxs-lookup"><span data-stu-id="2b18a-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2b18a-114">CNG DPAPI</span><span class="sxs-lookup"><span data-stu-id="2b18a-114">CNG DPAPI</span></span>](cng-dpapi.md)
</dt> <dt>

[<span data-ttu-id="2b18a-115">**нкрипткреатепротектиондескриптор**</span><span class="sxs-lookup"><span data-stu-id="2b18a-115">**NCryptCreateProtectionDescriptor**</span></span>](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptcreateprotectiondescriptor)
</dt> <dt>

[<span data-ttu-id="2b18a-116">Дескрипторы защиты</span><span class="sxs-lookup"><span data-stu-id="2b18a-116">Protection Descriptors</span></span>](protection-descriptors.md)
</dt> </dl>

 

 



