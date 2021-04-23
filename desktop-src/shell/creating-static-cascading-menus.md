---
description: Начиная с Windows 7, каскадные меню создаются с помощью записи реестра подкоманд, записи реестра Екстендедсубкоммандскэй или интерфейса Иексплореркомманд.
title: Создание статических каскадных меню
ms.topic: article
ms.date: 05/31/2018
ms.assetid: E3A6F174-BE53-48EF-AE9B-A3F297E91B95
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: d812b4d3d2fb0754002cb37d72718e4fe861ce15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104567706"
---
# <a name="creating-static-cascading-menus"></a><span data-ttu-id="bd1d3-103">Создание статических каскадных меню</span><span class="sxs-lookup"><span data-stu-id="bd1d3-103">Creating Static Cascading Menus</span></span>

<span data-ttu-id="bd1d3-104">В Windows 7 и более поздних версиях реализация каскадного меню поддерживается с помощью параметров реестра.</span><span class="sxs-lookup"><span data-stu-id="bd1d3-104">In Windows 7 and later, cascading menu implementation is supported through registry settings.</span></span> <span data-ttu-id="bd1d3-105">До Windows 7 создание каскадных меню было возможно только через реализацию интерфейса [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) .</span><span class="sxs-lookup"><span data-stu-id="bd1d3-105">Prior to Windows 7, the creation of cascading menus was possible only through the implementation of the [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) interface.</span></span> <span data-ttu-id="bd1d3-106">В Windows 7 и более поздних версиях следует прибегнуть к решениям на основе кода объектной модели (COM) только в том случае, если статические методы недостаточны.</span><span class="sxs-lookup"><span data-stu-id="bd1d3-106">In Windows 7 and later, you should resort to Component Object Model (COM) code-based solutions only when the static methods are insufficient.</span></span>

<span data-ttu-id="bd1d3-107">На следующем снимке экрана приведен пример каскадного меню.</span><span class="sxs-lookup"><span data-stu-id="bd1d3-107">The following screen shot provides an example of a cascading menu.</span></span>

![снимок экрана, демонстрирующий Пример каскадного меню](images/file-assoc/filecascademenu2ndex.png)

<span data-ttu-id="bd1d3-109">В Windows 7 и более поздних версиях существует три способа создания каскадных меню, которые описаны в следующих разделах.</span><span class="sxs-lookup"><span data-stu-id="bd1d3-109">In Windows 7 and later, there are three ways to create cascading menus, which are described in the following sections.</span></span>

-   [<span data-ttu-id="bd1d3-110">Создание каскадных меню с помощью записи реестра "подкоманды"</span><span class="sxs-lookup"><span data-stu-id="bd1d3-110">How to Create Cascading Menus with the SubCommands Registry Entry</span></span>](how-to--create-cascading-menus-with-the-subcommands-registry-entry.md)
-   [<span data-ttu-id="bd1d3-111">Создание каскадных меню с помощью записи реестра Екстендедсубкоммандскэй</span><span class="sxs-lookup"><span data-stu-id="bd1d3-111">How to Create Cascading Menus with the ExtendedSubCommandsKey Registry Entry</span></span>](how-to-create-cascading-menus-with-the-extendedsubcommandskey-registry-entry.md)
-   [<span data-ttu-id="bd1d3-112">Создание каскадных меню с помощью интерфейса Иексплореркомманд</span><span class="sxs-lookup"><span data-stu-id="bd1d3-112">How to Create Cascading Menus with the IExplorerCommand Interface</span></span>](how-to-create-cascading-menus-with-the-iexplorercommand-interface.md)

 

 
