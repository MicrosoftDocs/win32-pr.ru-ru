---
description: Можно разработать приложение, которое выполняет операции, для которых требуются права администратора, но выполняется как обычный пользователь.
ms.assetid: 78099b59-b09b-43c0-91f5-adb5c9e0e191
title: Разработка приложений, требующих прав администратора
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84d22687dad0a8914c5dcaebe8ea85a525529a34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105651010"
---
# <a name="developing-applications-that-require-administrator-privilege"></a><span data-ttu-id="b6581-103">Разработка приложений, требующих прав администратора</span><span class="sxs-lookup"><span data-stu-id="b6581-103">Developing Applications that Require Administrator Privilege</span></span>

<span data-ttu-id="b6581-104">Можно разработать приложение, которое выполняет операции, для которых требуются права администратора, но выполняется как обычный пользователь.</span><span class="sxs-lookup"><span data-stu-id="b6581-104">It is possible to develop an application that performs operations that require administrator privilege yet runs as a standard user.</span></span>

<span data-ttu-id="b6581-105">Это достигается несколькими моделями.</span><span class="sxs-lookup"><span data-stu-id="b6581-105">There are several models for accomplishing this.</span></span>



| <span data-ttu-id="b6581-106">Раздел</span><span class="sxs-lookup"><span data-stu-id="b6581-106">Topic</span></span>                                                                | <span data-ttu-id="b6581-107">Описание</span><span class="sxs-lookup"><span data-stu-id="b6581-107">Description</span></span>                                                                                                                                                                                          |
|----------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b6581-108">Модель задач с повышенными правами</span><span class="sxs-lookup"><span data-stu-id="b6581-108">Elevated Task Model</span></span>](elevated-task-model.md)                       | <span data-ttu-id="b6581-109">Приложение, выполняющееся в качестве обычного пользователя, выполняет операции, требующие прав администратора, запуская запланированную задачу.</span><span class="sxs-lookup"><span data-stu-id="b6581-109">An application running as a standard user performs operations that require administrator privilege by starting a scheduled task.</span></span>                                                                     |
| [<span data-ttu-id="b6581-110">Модель службы операционной системы</span><span class="sxs-lookup"><span data-stu-id="b6581-110">Operating System Service Model</span></span>](operating-system-service-model.md) | <span data-ttu-id="b6581-111">Приложение, работающее как обычный пользователь, взаимодействует со службой, работающей как **система** , с помощью [удаленного вызова процедур](/windows/desktop/Rpc/rpc-start-page) (RPC).</span><span class="sxs-lookup"><span data-stu-id="b6581-111">An application running as a standard user communicates with a service running as **SYSTEM** by using [Remote Procedure Call](/windows/desktop/Rpc/rpc-start-page) (RPC).</span></span>                                              |
| [<span data-ttu-id="b6581-112">Модель брокера администратора</span><span class="sxs-lookup"><span data-stu-id="b6581-112">Administrator Broker Model</span></span>](administrator-broker-model.md)         | <span data-ttu-id="b6581-113">Приложение делится на две программы.</span><span class="sxs-lookup"><span data-stu-id="b6581-113">The application is divided into two programs.</span></span> <span data-ttu-id="b6581-114">Одна из программ запускается от имени обычного пользователя, а другая запускается с правами администратора.</span><span class="sxs-lookup"><span data-stu-id="b6581-114">One of the programs runs as a standard user, and the other runs with administrator privilege.</span></span>                                                          |
| [<span data-ttu-id="b6581-115">Модель COM-объектов администратора</span><span class="sxs-lookup"><span data-stu-id="b6581-115">Administrator COM Object Model</span></span>](administrator-com-object-model.md) | <span data-ttu-id="b6581-116">Приложение, выполняющееся в качестве обычного пользователя, выполняет операции, требующие прав администратора, создавая объект [модели объектов](/windows/desktop/com/component-object-model--com--portal) с повышенными правами.</span><span class="sxs-lookup"><span data-stu-id="b6581-116">An application running as a standard user performs operations that require administrator privilege by creating an elevated [Component Object Model](/windows/desktop/com/component-object-model--com--portal) object.</span></span> |



 

 

 
