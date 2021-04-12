---
title: Публикация с помощью & разрешения регистрации сокетов Windows
description: Службы сокетов Windows могут использовать API регистрации и разрешения (РНР) для публикации служб и поиска служб, опубликованных с помощью РНР.
ms.assetid: 95c16d0b-abbc-4407-ac31-d7de0b25bd74
ms.tgt_platform: multiple
keywords:
- Регистрация и разрешение Windows Sockets AD, публикация
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e722d83447bd97e3964a9a0cc85df45ffd27faba
ms.sourcegitcommit: 460af18ea55f4b12d47d5b8d4b883896e21adf00
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/04/2019
ms.locfileid: "104487208"
---
# <a name="publishing-with-windows-sockets-registration--resolution"></a><span data-ttu-id="03a83-104">Публикация с помощью & разрешения регистрации сокетов Windows</span><span class="sxs-lookup"><span data-stu-id="03a83-104">Publishing with Windows Sockets Registration & Resolution</span></span>

<span data-ttu-id="03a83-105">Службы сокетов Windows могут использовать API регистрации и разрешения (РНР) для публикации служб и поиска служб, опубликованных с помощью РНР.</span><span class="sxs-lookup"><span data-stu-id="03a83-105">Windows Sockets services can use the Registration and Resolution (RnR) APIs to publish services and look up services published with RnR.</span></span> <span data-ttu-id="03a83-106">Публикация РНР выполняется в два этапа.</span><span class="sxs-lookup"><span data-stu-id="03a83-106">RnR publication occurs in two steps.</span></span> <span data-ttu-id="03a83-107">На первом шаге устанавливается класс службы, связывающий идентификатор GUID с именем службы.</span><span class="sxs-lookup"><span data-stu-id="03a83-107">The first step installs a service class that associates a GUID with a name for the service.</span></span> <span data-ttu-id="03a83-108">Класс службы может содержать зависящие от службы данные конфигурации.</span><span class="sxs-lookup"><span data-stu-id="03a83-108">The service class can hold service-specific configuration data.</span></span> <span data-ttu-id="03a83-109">Затем службы могут публиковать себя как экземпляры класса службы.</span><span class="sxs-lookup"><span data-stu-id="03a83-109">Services can then publish themselves as instances of the service class.</span></span> <span data-ttu-id="03a83-110">При публикации клиенты могут запрашивать службу каталогов для экземпляров заданного класса с помощью интерфейсов API РНР и выбирать экземпляр для привязки.</span><span class="sxs-lookup"><span data-stu-id="03a83-110">When published, clients can query the directory service for instances of a given class using the RnR APIs and select an instance to bind to.</span></span> <span data-ttu-id="03a83-111">Если класс больше не требуется, его можно удалить.</span><span class="sxs-lookup"><span data-stu-id="03a83-111">When a class is no longer required, it can be removed.</span></span>

 

 




