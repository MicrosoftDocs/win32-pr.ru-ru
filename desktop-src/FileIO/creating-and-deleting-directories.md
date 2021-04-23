---
description: Приложение может программно создавать и удалять каталоги.
ms.assetid: 52d1d8a8-e5a7-44f5-9bf2-2a496ef79d32
title: Создание и удаление каталогов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 140547594271e13bc78bfa78336f167f228879a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155299"
---
# <a name="creating-and-deleting-directories"></a><span data-ttu-id="e67a1-103">Создание и удаление каталогов</span><span class="sxs-lookup"><span data-stu-id="e67a1-103">Creating and Deleting Directories</span></span>

<span data-ttu-id="e67a1-104">Приложение может программно создавать и удалять каталоги.</span><span class="sxs-lookup"><span data-stu-id="e67a1-104">An application can programmatically create and delete directories.</span></span>

<span data-ttu-id="e67a1-105">Чтобы создать новый каталог, используйте функцию [**CreateDirectory**](/windows/desktop/api/FileAPI/nf-fileapi-createdirectorya), [**креатедиректорекс**](/windows/desktop/api/WinBase/nf-winbase-createdirectoryexa)или [**креатедиректоритрансактед**](/windows/desktop/api/WinBase/nf-winbase-createdirectorytransacteda) .</span><span class="sxs-lookup"><span data-stu-id="e67a1-105">To create a new directory, use the [**CreateDirectory**](/windows/desktop/api/FileAPI/nf-fileapi-createdirectorya), [**CreateDirectoryEx**](/windows/desktop/api/WinBase/nf-winbase-createdirectoryexa), or [**CreateDirectoryTransacted**](/windows/desktop/api/WinBase/nf-winbase-createdirectorytransacteda) function.</span></span> <span data-ttu-id="e67a1-106">Каталогу присваивается имя, указанное при его создании.</span><span class="sxs-lookup"><span data-stu-id="e67a1-106">A directory is given the name specified when it is created.</span></span> <span data-ttu-id="e67a1-107">Соглашения об именовании каталога следуют правилам именования файлов.</span><span class="sxs-lookup"><span data-stu-id="e67a1-107">The conventions for naming a directory follow the conventions for naming a file.</span></span> <span data-ttu-id="e67a1-108">Описание этих соглашений см. [в разделе Присвоение имени файлу](naming-a-file.md).</span><span class="sxs-lookup"><span data-stu-id="e67a1-108">For a description of these conventions, see [Naming a File](naming-a-file.md).</span></span>

<span data-ttu-id="e67a1-109">Чтобы удалить существующий каталог, используйте функцию [**ремоведиректори**](/windows/desktop/api/FileAPI/nf-fileapi-removedirectorya) или [**ремоведиректоритрансактед**](/windows/desktop/api/WinBase/nf-winbase-removedirectorytransacteda) .</span><span class="sxs-lookup"><span data-stu-id="e67a1-109">To delete an existing directory, use the [**RemoveDirectory**](/windows/desktop/api/FileAPI/nf-fileapi-removedirectorya) or [**RemoveDirectoryTransacted**](/windows/desktop/api/WinBase/nf-winbase-removedirectorytransacteda) function.</span></span> <span data-ttu-id="e67a1-110">Перед удалением каталога необходимо убедиться, что каталог пуст и у вас есть права на удаление для каталога.</span><span class="sxs-lookup"><span data-stu-id="e67a1-110">Before removing a directory, you must ensure that the directory is empty and that you have the delete access privilege for the directory.</span></span> <span data-ttu-id="e67a1-111">Чтобы выполнить Последнее действие, вызовите функцию [**жетсекуритинфо**](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) .</span><span class="sxs-lookup"><span data-stu-id="e67a1-111">To do the latter, call the [**GetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) function.</span></span>

 

 
