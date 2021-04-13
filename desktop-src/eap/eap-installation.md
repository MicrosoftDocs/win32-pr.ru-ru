---
title: Установка EAP
description: Поставщики реализуют ЕАПС, также известные как протоколы проверки подлинности, в библиотеках динамической компоновки (DLL).
ms.assetid: af10b1e9-45c9-4640-ba79-fc9c23cc3c47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 619505a55108ebde0e14d7ff20c78394c6c90fad
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2019
ms.locfileid: "104412275"
---
# <a name="eap-installation"></a><span data-ttu-id="74279-103">Установка EAP</span><span class="sxs-lookup"><span data-stu-id="74279-103">EAP Installation</span></span>

<span data-ttu-id="74279-104">Поставщики реализуют ЕАПС, также известные как протоколы проверки подлинности, в библиотеках динамической компоновки (DLL).</span><span class="sxs-lookup"><span data-stu-id="74279-104">Vendors implement EAPs, also known as authentication protocols, in dynamic-link libraries (DLLs).</span></span> <span data-ttu-id="74279-105">Библиотека DLL для протокола проверки подлинности должна размещаться как на клиентской, так и на серверной компьютерах.</span><span class="sxs-lookup"><span data-stu-id="74279-105">A DLL for the authentication protocol must reside on both the client and server computers.</span></span> <span data-ttu-id="74279-106">Для простоты клиентские и серверные библиотеки DLL могут быть идентичными. Однако это не обязательно.</span><span class="sxs-lookup"><span data-stu-id="74279-106">For simplicity, the client and server DLLs may be identical; however, this is not a requirement.</span></span> <span data-ttu-id="74279-107">Кроме того, имейте в виду, что одна и та же библиотека DLL может поддерживать несколько протоколов проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="74279-107">Also, be aware that the same DLL may support more than one authentication protocol.</span></span>

<span data-ttu-id="74279-108">Поставщик должен предоставить программное обеспечение для установки и удаления библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="74279-108">The vendor should provide setup software to install and remove the DLL.</span></span> <span data-ttu-id="74279-109">Программа установки также должна создать соответствующие ключи и значения для протокола проверки подлинности в системном реестре и удалить их после удаления.</span><span class="sxs-lookup"><span data-stu-id="74279-109">The setup software should also create the appropriate keys and values for the authentication protocol in the system registry and remove them upon uninstall.</span></span>

<span data-ttu-id="74279-110">При установке каждой DLL-библиотеки EAP необходимо создать следующий раздел реестра.</span><span class="sxs-lookup"><span data-stu-id="74279-110">The installation of each EAP DLL should create the following registry key.</span></span>

<span data-ttu-id="74279-111">**HKey \_ Локальный \_ компьютер** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **RASMAN** \\ **PPP** \\ **EAP** \\ **&lt; еаптипеид &gt;**</span><span class="sxs-lookup"><span data-stu-id="74279-111">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Services**\\**Rasman**\\**PPP**\\**EAP**\\**&lt;eaptypeid&gt;**</span></span>

<span data-ttu-id="74279-112">В предыдущем пути **&lt; еаптипеид &gt;** — это идентификатор протокола проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="74279-112">In the preceding path, **&lt;eaptypeid&gt;** is the ID of the authentication protocol.</span></span> <span data-ttu-id="74279-113">Поставщик должен получить этот идентификатор из центра "назначенные номера Интернета (IANA)".</span><span class="sxs-lookup"><span data-stu-id="74279-113">The vendor must obtain this ID from the Internet Assigned Numbers Authority (IANA).</span></span>

<span data-ttu-id="74279-114">Дополнительные сведения и описание поддерживаемых значений для этого ключа см. в разделе [значения реестра протокола проверки подлинности](authentication-protocol-registry-values.md).</span><span class="sxs-lookup"><span data-stu-id="74279-114">For more information and a description of the supported values for this key, see [Authentication Protocol Registry Values](authentication-protocol-registry-values.md).</span></span>

 

 




