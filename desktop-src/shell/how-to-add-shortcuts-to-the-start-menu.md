---
description: Чтобы добавить элемент в подменю программы, выполните следующие действия.
ms.assetid: F8793C33-2281-4E4A-9659-4189E1C8279A
title: Добавление ярлыков в меню "Пуск"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77ee942e07c48ed7addf07160412008bfb5b9322
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156475"
---
# <a name="how-to-add-shortcuts-to-the-start-menu"></a><span data-ttu-id="8b2c4-103">Добавление ярлыков в меню "Пуск"</span><span class="sxs-lookup"><span data-stu-id="8b2c4-103">How to Add Shortcuts to the Start Menu</span></span>

<span data-ttu-id="8b2c4-104">Чтобы добавить элемент в подменю **программы** , выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="8b2c4-104">To add an item to the **Programs** submenu, follow these steps.</span></span>

## <a name="instructions"></a><span data-ttu-id="8b2c4-105">Инструкции</span><span class="sxs-lookup"><span data-stu-id="8b2c4-105">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="8b2c4-106">Шаг 1.</span><span class="sxs-lookup"><span data-stu-id="8b2c4-106">Step 1:</span></span>

<span data-ttu-id="8b2c4-107">Создайте [ссылку на оболочку](./links.md) с помощью интерфейса [**ишелллинк**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) .</span><span class="sxs-lookup"><span data-stu-id="8b2c4-107">Create a [shell link](./links.md) by using the [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) interface.</span></span>

### <a name="step-2"></a><span data-ttu-id="8b2c4-108">Шаг 2.</span><span class="sxs-lookup"><span data-stu-id="8b2c4-108">Step 2:</span></span>

<span data-ttu-id="8b2c4-109">Получите расположение папки Programs с помощью функции [**шжеткновнфолдерпас**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) , передав [**\_ программы FOLDERID**](knownfolderid.md).</span><span class="sxs-lookup"><span data-stu-id="8b2c4-109">Obtain the location of the Programs folder by using the [**SHGetKnownFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) function, passing [**FOLDERID\_Programs**](knownfolderid.md).</span></span>

### <a name="step-3"></a><span data-ttu-id="8b2c4-110">Шаг 3.</span><span class="sxs-lookup"><span data-stu-id="8b2c4-110">Step 3:</span></span>

<span data-ttu-id="8b2c4-111">Добавьте ссылку оболочки в папку программы.</span><span class="sxs-lookup"><span data-stu-id="8b2c4-111">Add the Shell link to the Programs folder.</span></span> <span data-ttu-id="8b2c4-112">Можно также создать папку в папке Programs и добавить ссылку в эту папку.</span><span class="sxs-lookup"><span data-stu-id="8b2c4-112">You can also create a folder in the Programs folder and add the link to that folder.</span></span>

 

 
