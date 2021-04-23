---
title: Выбор времени создания объектов со специальными возможностями
description: Разработчики сервера могут создавать все объекты, доступные в контейнере, при создании контейнера, а также динамически создавать объекты со специальными возможностями.
ms.assetid: 26c8bb4b-19ec-4fd5-b758-30cb6a513818
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 987b40527c178c40101288b0192c38d9a9b06040
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068266"
---
# <a name="choosing-when-to-create-accessible-objects"></a><span data-ttu-id="719f9-103">Выбор времени создания объектов со специальными возможностями</span><span class="sxs-lookup"><span data-stu-id="719f9-103">Choosing When to Create Accessible Objects</span></span>

<span data-ttu-id="719f9-104">Разработчики сервера могут создавать все объекты, доступные в контейнере, при создании контейнера, а также динамически создавать объекты со специальными возможностями.</span><span class="sxs-lookup"><span data-stu-id="719f9-104">Server developers can create all the accessible objects within a container when the container is created, or they can create the accessible objects dynamically.</span></span>

<span data-ttu-id="719f9-105">Например, представьте себе диалоговое окно с несколькими пользовательскими элементами управления.</span><span class="sxs-lookup"><span data-stu-id="719f9-105">For example, imagine a dialog box with several custom controls.</span></span> <span data-ttu-id="719f9-106">Сервер создает объекты со специальными возможностями для всех пользовательских элементов управления при отображении диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="719f9-106">A server creates accessible objects for all of the custom controls when the dialog box is displayed.</span></span> <span data-ttu-id="719f9-107">Однако если один из элементов управления является пользовательским полем со списком, сервер ждет, пока пользователь не выберет его, чтобы создать специальные объекты для элементов, содержащихся в поле со списком.</span><span class="sxs-lookup"><span data-stu-id="719f9-107">However, if one of the controls is a custom combo box, the server waits until a user selects it to create accessible objects for the items that the combo box contains.</span></span>

<span data-ttu-id="719f9-108">Если родительский объект создает объекты со специальными возможностями динамически, приложения используют меньше памяти, чем если бы все доступные объекты были созданы заранее.</span><span class="sxs-lookup"><span data-stu-id="719f9-108">By having the parent create accessible objects dynamically, applications use less memory than if all the possible accessible objects were created ahead of time.</span></span>

 

 




