---
title: Расширение ADSI службы BITS
description: Сервер BITS предоставляет следующие интерфейсы расширения ADSI для включения отправки BITS.
ms.assetid: 7937a86d-886b-4764-bfc1-2ffd64dbcbc1
keywords:
- БИТЫ расширения ADSI для службы BITS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34c045f8f7fff8e66251a94a9f704046674934ed
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105654207"
---
# <a name="bits-adsi-extension"></a><span data-ttu-id="d89a8-104">Расширение ADSI службы BITS</span><span class="sxs-lookup"><span data-stu-id="d89a8-104">BITS ADSI Extension</span></span>

<span data-ttu-id="d89a8-105">Сервер BITS предоставляет следующие интерфейсы расширения ADSI для включения отправки BITS.</span><span class="sxs-lookup"><span data-stu-id="d89a8-105">The BITS server provides the following ADSI extension interfaces to enable BITS uploads.</span></span>



| <span data-ttu-id="d89a8-106">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="d89a8-106">Interface</span></span>                                                        | <span data-ttu-id="d89a8-107">Описание</span><span class="sxs-lookup"><span data-stu-id="d89a8-107">Description</span></span>                                                                                                                                    |
|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d89a8-108">**ибитсекстенсионсетуп**</span><span class="sxs-lookup"><span data-stu-id="d89a8-108">**IBITSExtensionSetup**</span></span>](/windows/desktop/api/Bitscfg/nn-bitscfg-ibitsextensionsetup)               | <span data-ttu-id="d89a8-109">Используется для включения и отключения отправки BITS в виртуальный каталог.</span><span class="sxs-lookup"><span data-stu-id="d89a8-109">Use to enable and disable BITS uploads to a virtual directory.</span></span>                                                                                 |
| [<span data-ttu-id="d89a8-110">**ибитсекстенсионсетупфактори**</span><span class="sxs-lookup"><span data-stu-id="d89a8-110">**IBITSExtensionSetupFactory**</span></span>](/windows/desktop/api/Bitscfg/nn-bitscfg-ibitsextensionsetupfactory) | <span data-ttu-id="d89a8-111">Используется для получения указателя на интерфейс [**ибитсекстенсионсетуп**](/windows/desktop/api/Bitscfg/nn-bitscfg-ibitsextensionsetup) в программе установки, которая устанавливает сервер BITS.</span><span class="sxs-lookup"><span data-stu-id="d89a8-111">Use to retrieve a pointer to an [**IBITSExtensionSetup**](/windows/desktop/api/Bitscfg/nn-bitscfg-ibitsextensionsetup) interface in a setup program that installs the BITS server.</span></span> |



 

 

 




