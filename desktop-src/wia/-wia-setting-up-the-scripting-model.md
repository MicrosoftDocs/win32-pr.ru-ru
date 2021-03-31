---
description: Чтобы использовать модель сценариев для получения образа Windows (WIA), необходимо, чтобы файл Wiascr.dll установлен и зарегистрирован на компьютере.
ms.assetid: 94b08833-9fbd-46cf-b6a3-71713cc6ac30
title: Настройка среды разработки модели сценариев
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f6b70d52e937e93f26f95926c5ec2319611b2e8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263126"
---
# <a name="setting-up-the-scripting-model-development-environment"></a><span data-ttu-id="59108-103">Настройка среды разработки модели сценариев</span><span class="sxs-lookup"><span data-stu-id="59108-103">Setting up the Scripting Model Development Environment</span></span>

<span data-ttu-id="59108-104">Чтобы использовать модель сценариев для получения образа Windows (WIA), необходимо, чтобы файл Wiascr.dll установлен и зарегистрирован на компьютере.</span><span class="sxs-lookup"><span data-stu-id="59108-104">To use the Windows Image Acquisition (WIA) scripting model, you must have the file Wiascr.dll installed and registered on the computer.</span></span>

> [!Note]  
> <span data-ttu-id="59108-105">Эта система сценариев была заменена на уровень автоматизации службы "получение образа Windows" (WIA).</span><span class="sxs-lookup"><span data-stu-id="59108-105">This scripting system has been replaced with Windows Image Acquisition (WIA) Automation Layer.</span></span> <span data-ttu-id="59108-106">См. раздел [уровень службы "получение образа Windows](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage)".</span><span class="sxs-lookup"><span data-stu-id="59108-106">See [Windows Image Acquisition Automation Layer](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage).</span></span>

 

<span data-ttu-id="59108-107">Скопируйте этот файл из пакета SDK для WIA в каталог *% WINDIR%*/system32 (например, c: \\ Windows \\ System32).</span><span class="sxs-lookup"><span data-stu-id="59108-107">Copy this file from the WIA SDK into the *%windir%*/System32 (for example, c:\\windows\\System32) directory.</span></span> <span data-ttu-id="59108-108">В командной строке перейдите в этот каталог и введите **regsvr32 Wiascr.dll**.</span><span class="sxs-lookup"><span data-stu-id="59108-108">At the command line, navigate to this directory, and type **regsvr32 Wiascr.dll**.</span></span>

<span data-ttu-id="59108-109">Это приводит к вводу необходимых сведений в системный реестр.</span><span class="sxs-lookup"><span data-stu-id="59108-109">This enters the necessary information in the system registry.</span></span>

<span data-ttu-id="59108-110">Теперь вы готовы использовать модель скриптов WIA.</span><span class="sxs-lookup"><span data-stu-id="59108-110">You are now ready to use the WIA scripting model.</span></span>

 

 
