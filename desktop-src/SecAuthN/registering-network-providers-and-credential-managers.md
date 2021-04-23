---
description: После создания поставщика сети или диспетчера учетных данных необходимо зарегистрировать его в системе.
ms.assetid: 4c58671d-d11d-4f32-866b-e278fc8e6114
title: Регистрация поставщиков сети и диспетчеров учетных данных
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de34c97b61f685c3e779bd487fbc2c5b21fa7af2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104264816"
---
# <a name="registering-network-providers-and-credential-managers"></a><span data-ttu-id="84ce2-103">Регистрация поставщиков сети и диспетчеров учетных данных</span><span class="sxs-lookup"><span data-stu-id="84ce2-103">Registering Network Providers and Credential Managers</span></span>

<span data-ttu-id="84ce2-104">После создания поставщика сети или диспетчера учетных данных необходимо зарегистрировать его в системе.</span><span class="sxs-lookup"><span data-stu-id="84ce2-104">After you have created your network provider or credential manager, you must register it with the system.</span></span> <span data-ttu-id="84ce2-105">Это необходимо, чтобы многопротокольный маршрутизатор знал, какие сетевые поставщики установлены.</span><span class="sxs-lookup"><span data-stu-id="84ce2-105">This is necessary so the MPR will know what network providers are installed.</span></span> <span data-ttu-id="84ce2-106">После запуска многопротокольного маршрутизатора он проверяет реестр и загружает найденные поставщики сетевых услуг или диспетчеров учетных данных.</span><span class="sxs-lookup"><span data-stu-id="84ce2-106">When the MPR starts, it checks the registry and loads any network providers or credential managers it finds.</span></span>

<span data-ttu-id="84ce2-107">Так как поставщики сетевых услуг и диспетчеры учетных данных связаны друг с друга, они регистрируются в тех же подразделах реестра.</span><span class="sxs-lookup"><span data-stu-id="84ce2-107">Because network providers and credential managers are related, they are registered in the same subkeys of the registry.</span></span> <span data-ttu-id="84ce2-108">Фактически, библиотеки DLL поставщика сетевых услуг также могут быть диспетчерами учетных данных.</span><span class="sxs-lookup"><span data-stu-id="84ce2-108">In fact, network provider DLLs can also be credential managers.</span></span>

<span data-ttu-id="84ce2-109">Подробные сведения о разделах реестра, которые следует создать для поставщика сети или диспетчера учетных данных, см. в разделе [разделы реестра для проверки подлинности](authentication-registry-keys.md).</span><span class="sxs-lookup"><span data-stu-id="84ce2-109">For detailed information about the registry keys you should create for your network provider or credential manager, see [Authentication Registry Keys](authentication-registry-keys.md).</span></span>

 

 



