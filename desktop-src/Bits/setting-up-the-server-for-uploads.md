---
title: Настройка сервера для отправки
description: Чтобы передать файлы на сервер с помощью службы BITS, на сервере должны быть установлены службы IIS и серверное расширение BITS ISAPI. Требования к службам IIS см. в разделе требования IIS к отправке BITS.
ms.assetid: 2f3a2f99-b9de-41da-897f-a4d9c6d5e8c0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c2ef81019f4c69157c267cd2438188f440299a4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104252813"
---
# <a name="setting-up-the-server-for-uploads"></a><span data-ttu-id="36580-104">Настройка сервера для отправки</span><span class="sxs-lookup"><span data-stu-id="36580-104">Setting Up the Server for Uploads</span></span>

<span data-ttu-id="36580-105">Чтобы передать файлы на сервер с помощью службы BITS, на сервере должны быть установлены службы IIS и серверное расширение BITS ISAPI.</span><span class="sxs-lookup"><span data-stu-id="36580-105">To upload files to a server using BITS, the server must have IIS and the BITS server extension ISAPI installed.</span></span> <span data-ttu-id="36580-106">Требования к службам IIS см. в разделе [требования IIS к отправке BITS](iis-requirements-for-bits-uploads.md).</span><span class="sxs-lookup"><span data-stu-id="36580-106">For IIS requirements, see [IIS Requirements for BITS Uploads](iis-requirements-for-bits-uploads.md).</span></span>

<span data-ttu-id="36580-107">Сведения о настройке виртуального каталога IIS, используемого BITS для отправки, см. в следующих разделах.</span><span class="sxs-lookup"><span data-stu-id="36580-107">For information on configuring the IIS virtual directory that BITS uses for uploads, see the following topics.</span></span>

-   [<span data-ttu-id="36580-108">Настройка разрешений для виртуальных каталогов</span><span class="sxs-lookup"><span data-stu-id="36580-108">Setting Permissions on Virtual Directories</span></span>](setting-permissions-on-virtual-directories.md)
-   [<span data-ttu-id="36580-109">Написание сценария для настройки виртуального каталога</span><span class="sxs-lookup"><span data-stu-id="36580-109">Writing a Script to Configure the Virtual Directory</span></span>](writing-a-script-to-configure-the-virtual-directory.md)
-   [<span data-ttu-id="36580-110">Использование пользовательского интерфейса IIS для настройки виртуального каталога</span><span class="sxs-lookup"><span data-stu-id="36580-110">Using the IIS UI to Configure the Virtual Directory</span></span>](using-the-iis-ui-to-configure-the-virtual-directory.md)
-   [<span data-ttu-id="36580-111">Предотвращение нескольких отправок</span><span class="sxs-lookup"><span data-stu-id="36580-111">Preventing Multiple Uploads</span></span>](preventing-multiple-uploads.md)
-   [<span data-ttu-id="36580-112">Отправка рекомендаций</span><span class="sxs-lookup"><span data-stu-id="36580-112">Upload Best Practices</span></span>](upload-best-practices.md)

> [!Note]  
> <span data-ttu-id="36580-113">Некоторые установки IIS включают компонент фильтрации UrlScan.</span><span class="sxs-lookup"><span data-stu-id="36580-113">Some IIS installations include the UrlScan filtering component.</span></span> <span data-ttu-id="36580-114">Если средство UrlScan включено, администратор должен добавить команду "POST BITS \_ " в список разрешенных HTTP-команд URLScan.</span><span class="sxs-lookup"><span data-stu-id="36580-114">If UrlScan is enabled, the administrator must add the "BITS\_POST" verb to UrlScan's list of allowed HTTP verbs.</span></span> <span data-ttu-id="36580-115">В противном случае отправка клиента BITS завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="36580-115">Otherwise, BITS client uploads will fail.</span></span> <span data-ttu-id="36580-116">Дополнительные сведения о включении команд в UrlScan см. в документации по UrlScan.</span><span class="sxs-lookup"><span data-stu-id="36580-116">For further details on enabling verbs in UrlScan, see the UrlScan documentation.</span></span>

 

 

 




