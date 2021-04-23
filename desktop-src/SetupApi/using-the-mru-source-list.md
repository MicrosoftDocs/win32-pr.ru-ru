---
description: Функция Сетупсетсаурцелист будет открывать или создавать исходный список в системе пользователей.
ms.assetid: cda632cf-6c92-48fb-aef1-25b320affd3e
title: Использование списка источников MRU
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dbecb9e32a554d1818661b1fd7f6e782744c16e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991611"
---
# <a name="using-the-mru-source-list"></a><span data-ttu-id="f84a5-103">Использование списка источников MRU</span><span class="sxs-lookup"><span data-stu-id="f84a5-103">Using the MRU Source List</span></span>

<span data-ttu-id="f84a5-104">Функция [**сетупсетсаурцелист**](/windows/desktop/api/Setupapi/nf-setupapi-setupsetsourcelista) будет открывать или создавать исходный список в системе пользователя.</span><span class="sxs-lookup"><span data-stu-id="f84a5-104">The [**SetupSetSourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupsetsourcelista) function will open or create a source list on the user's system.</span></span> <span data-ttu-id="f84a5-105">Можно задать список пользователей, системный список, сочетание списков пользователей и систем, а также временный список источников MRU.</span><span class="sxs-lookup"><span data-stu-id="f84a5-105">You can specify to set the user list, the system list, a combination of the user and system lists, or a temporary list as the MRU source list.</span></span> <span data-ttu-id="f84a5-106">Если используется временный список, он будет единственным списком, доступным для приложения установки до тех пор, пока не будет вызван [**сетупканцелтемпорарисаурцелист**](/windows/desktop/api/Setupapi/nf-setupapi-setupcanceltemporarysourcelist) , или **сетупсетсаурцелист** будет вызван второй раз.</span><span class="sxs-lookup"><span data-stu-id="f84a5-106">If a temporary list is used, it will be the only list available to the setup application until [**SetupCancelTemporarySourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupcanceltemporarysourcelist) is called, or **SetupSetSourceList** is called a second time.</span></span>

<span data-ttu-id="f84a5-107">После задания списка можно запросить исходный список с помощью [**сетупкуерисаурцелист**](/windows/desktop/api/Setupapi/nf-setupapi-setupquerysourcelista) , чтобы получить массив исходных путей.</span><span class="sxs-lookup"><span data-stu-id="f84a5-107">After a list is set, you can query the source list by using [**SetupQuerySourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupquerysourcelista) to obtain an array of the source paths.</span></span> <span data-ttu-id="f84a5-108">Если массив исходного списка больше не нужен, необходимо вызвать функцию [**сетупфрисаурцелист**](/windows/desktop/api/Setupapi/nf-setupapi-setupfreesourcelista) , чтобы освободить ресурсы, выделенные [**сетупкуерисаурцелист**](/windows/desktop/api/Setupapi/nf-setupapi-setupquerysourcelista).</span><span class="sxs-lookup"><span data-stu-id="f84a5-108">When the source list array is no longer needed, you must call the [**SetupFreeSourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupfreesourcelista) function to free the resources allocated by [**SetupQuerySourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupquerysourcelista).</span></span>

<span data-ttu-id="f84a5-109">Чтобы добавить путь к исходному списку, который находится в системе пользователя или во временном списке, вызовите [**сетупаддтосаурцелист**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddtosourcelista).</span><span class="sxs-lookup"><span data-stu-id="f84a5-109">To add a path to a source list, either one that is resident on the user's system, or a temporary list, call [**SetupAddToSourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddtosourcelista).</span></span> <span data-ttu-id="f84a5-110">Если указанный исходный список не является временным, он остается в системе пользователя и доступен для последующих установок.</span><span class="sxs-lookup"><span data-stu-id="f84a5-110">If the source list specified is not temporary, that source will remain on the user's system and is accessible to subsequent installations.</span></span>

<span data-ttu-id="f84a5-111">Чтобы удалить путь из исходного пути, вызовите функцию [**сетупремовефромсаурцелист**](/windows/desktop/api/Setupapi/nf-setupapi-setupremovefromsourcelista) .</span><span class="sxs-lookup"><span data-stu-id="f84a5-111">To remove a path from the source path, call the [**SetupRemoveFromSourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupremovefromsourcelista) function.</span></span>

 

 



