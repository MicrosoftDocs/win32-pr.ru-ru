---
description: Описание использования функций политики LSA.
ms.assetid: 7f4b963d-3442-4c04-b3d4-f7c8eb1ed15b
title: Использование политики LSA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 240a59c9009b91d03c1e0904861f815773c95af2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272252"
---
# <a name="using-lsa-policy"></a><span data-ttu-id="abcbb-103">Использование политики LSA</span><span class="sxs-lookup"><span data-stu-id="abcbb-103">Using LSA Policy</span></span>

<span data-ttu-id="abcbb-104">В следующих разделах описывается использование функций политики LSA.</span><span class="sxs-lookup"><span data-stu-id="abcbb-104">The following topics describe how to use the LSA Policy functions.</span></span>

-   <span data-ttu-id="abcbb-105">[Использование строк LSA в Юникоде](using-lsa-unicode-strings.md) объясняет, как преобразовать строки в формат структуры, используемый некоторыми ФУНКЦИЯМИ политики LSA.</span><span class="sxs-lookup"><span data-stu-id="abcbb-105">[Using LSA Unicode Strings](using-lsa-unicode-strings.md) explains how to convert strings into the structure format used by some LSA Policy functions.</span></span>
-   <span data-ttu-id="abcbb-106">[Открытие обработчика объектов политики](opening-a-policy-object-handle.md) описывает, как открыть обработчик для объекта локальной [**политики**](policy-object.md) .</span><span class="sxs-lookup"><span data-stu-id="abcbb-106">[Opening a Policy Object Handle](opening-a-policy-object-handle.md) describes how to open a handle to the local [**Policy**](policy-object.md) object.</span></span> <span data-ttu-id="abcbb-107">Этот обработчик необходим для многих функций политики LSA в качестве входного параметра.</span><span class="sxs-lookup"><span data-stu-id="abcbb-107">This handle is required by many of the LSA Policy functions as an input parameter.</span></span>
-   <span data-ttu-id="abcbb-108">[Управление сведениями о политике](managing-policy-information.md) сведения о настройке и запросе сведений о глобальных политиках для локальной системы и домена.</span><span class="sxs-lookup"><span data-stu-id="abcbb-108">[Managing Policy Information](managing-policy-information.md) details how to set and query global policy information for the local system and the domain.</span></span>
-   <span data-ttu-id="abcbb-109">[Получение событий изменения политики](receiving-policy-change-events.md) описывает создание и регистрацию события для получения уведомлений при изменении сведений о политике.</span><span class="sxs-lookup"><span data-stu-id="abcbb-109">[Receiving Policy Change Events](receiving-policy-change-events.md) describes how to create and register an event to receive notifications when policy information changes.</span></span>
-   <span data-ttu-id="abcbb-110">[Управление разрешениями учетной записи](managing-account-permissions.md) объясняет создание, удаление и перечисление учетных записей, а также добавление и удаление привилегий для этих учетных записей.</span><span class="sxs-lookup"><span data-stu-id="abcbb-110">[Managing Account Permissions](managing-account-permissions.md) explains how to create, delete, and enumerate accounts and how to add and remove privileges for those accounts.</span></span>
-   <span data-ttu-id="abcbb-111">[Управление сведениями о доверенном домене](managing-trusted-domain-information.md) описывает создание, перечисление и удаление доверенных доменов, а так же задание и получение сведений о доверенном домене.</span><span class="sxs-lookup"><span data-stu-id="abcbb-111">[Managing Trusted Domain Information](managing-trusted-domain-information.md) describes how to create, enumerate, and delete trusted domains, and how to set and retrieve trusted domain information.</span></span>
-   <span data-ttu-id="abcbb-112">При [преобразовании между именами и идентификаторами безопасности](translating-between-names-and-sids.md) объясняется, как сопоставлять идентификаторы безопасности с именами учетных записей и наоборот.</span><span class="sxs-lookup"><span data-stu-id="abcbb-112">[Translating Between Names and SIDs](translating-between-names-and-sids.md) explains how to map SIDs to account names and vice versa.</span></span>
-   <span data-ttu-id="abcbb-113">[Сопоставление идентификаторов POSIX](mapping-posix-identifiers.md) описывает, как сопоставлять идентификаторы безопасности с 32-разрядными кодами POSIX.</span><span class="sxs-lookup"><span data-stu-id="abcbb-113">[Mapping Posix Identifiers](mapping-posix-identifiers.md) describes how to map SIDs to 32-bit Posix identifiers.</span></span>
-   <span data-ttu-id="abcbb-114">[Хранение конфиденциальных данных](storing-private-data.md) объясняет, как сохранять и извлекать закрытые строки данных.</span><span class="sxs-lookup"><span data-stu-id="abcbb-114">[Storing Private Data](storing-private-data.md) explains how to store and retrieve private data strings.</span></span>

<span data-ttu-id="abcbb-115">Сведения о том, как использовать LSA для входа и проверки подлинности пользователей, см. в разделе [LSA Authentication](/windows/desktop/SecAuthN/lsa-authentication).</span><span class="sxs-lookup"><span data-stu-id="abcbb-115">For information about how to use the LSA to logon and authenticate users, see [LSA Authentication](/windows/desktop/SecAuthN/lsa-authentication).</span></span>

 

 
