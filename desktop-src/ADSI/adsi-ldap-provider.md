---
title: Поставщик LDAP ADSI
description: Поставщик LDAP ADSI реализует набор объектов ADSI, поддерживающих различные интерфейсы ADSI. Чтобы получить доступ к поставщику LDAP, выполните привязку к любому из объектов LDAP ADSI с помощью LDAP ADsPath.
ms.assetid: 3c13ea2f-fe40-4fd4-8540-422f277e07c1
ms.tgt_platform: multiple
keywords:
- Поставщик LDAP ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8edbca53708a46c2f788c328a78bd2488973486
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103887596"
---
# <a name="adsi-ldap-provider"></a><span data-ttu-id="b133b-105">Поставщик LDAP ADSI</span><span class="sxs-lookup"><span data-stu-id="b133b-105">ADSI LDAP Provider</span></span>

<span data-ttu-id="b133b-106">Поставщик LDAP ADSI реализует набор объектов ADSI, поддерживающих различные интерфейсы ADSI.</span><span class="sxs-lookup"><span data-stu-id="b133b-106">The ADSI LDAP Provider implements a set of ADSI objects that support various ADSI interfaces.</span></span> <span data-ttu-id="b133b-107">Чтобы получить доступ к поставщику LDAP, выполните привязку к любому из объектов LDAP ADSI с помощью LDAP ADsPath.</span><span class="sxs-lookup"><span data-stu-id="b133b-107">To access the LDAP provider, bind to any of the ADSI LDAP objects, using the LDAP ADsPath.</span></span>

<span data-ttu-id="b133b-108">Для работы с поставщиком необходимо установить на клиентском компьютере Adsldp.dll, Adsldpc.dll, Adsmsext.dll и Activeds.dll.</span><span class="sxs-lookup"><span data-stu-id="b133b-108">You must have Adsldp.dll, Adsldpc.dll, Adsmsext.dll, and Activeds.dll installed on your client computer to work with the provider.</span></span>

> [!Note]  
> <span data-ttu-id="b133b-109">Поставщик LDAP по умолчанию (ADSI) не может считаться полностью потокобезопасным.</span><span class="sxs-lookup"><span data-stu-id="b133b-109">The default ADSI LDAP provider cannot be assumed to be completely thread-safe.</span></span> <span data-ttu-id="b133b-110">Модули записи многопоточных приложений должны правильно координировать доступ между потоками посредством правильного использования объектов синхронизации, таких как семафоры, мьютексы, критические разделы и т. д.</span><span class="sxs-lookup"><span data-stu-id="b133b-110">Writers of multithreaded applications should properly coordinate access between threads through the proper use of synchronization objects such as semaphores, mutexes, critical sections, and so on.</span></span>

 

 

 




