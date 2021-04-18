---
description: Создание приложений COM+
ms.assetid: 32828d4d-aa98-4e6a-b7de-2ec832024517
title: Создание приложений COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e42a4b7ad18dab3f7163f527626322e05671e7be
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701297"
---
# <a name="creating-com-applications"></a><span data-ttu-id="5ccfe-103">Создание приложений COM+</span><span class="sxs-lookup"><span data-stu-id="5ccfe-103">Creating COM+ Applications</span></span>

<span data-ttu-id="5ccfe-104">В этом разделе описывается, как создать новое (пустое) приложение COM+, а затем добавить компоненты в это приложение.</span><span class="sxs-lookup"><span data-stu-id="5ccfe-104">This section describes how to create a new (empty) COM+ application and then add components to that application.</span></span> <span data-ttu-id="5ccfe-105">Здесь также описывается, как добавлять компоненты COM в и удалять их из существующих приложений COM+, а также как перемещать и копировать компоненты из одного приложения COM+ в другое.</span><span class="sxs-lookup"><span data-stu-id="5ccfe-105">It also describes how to add COM components to, and remove them from, existing COM+ applications, and how to move and copy components from one COM+ application to another.</span></span>



| <span data-ttu-id="5ccfe-106">Раздел</span><span class="sxs-lookup"><span data-stu-id="5ccfe-106">Topic</span></span>                                                                                                       | <span data-ttu-id="5ccfe-107">Описание</span><span class="sxs-lookup"><span data-stu-id="5ccfe-107">Description</span></span>                                                                        |
|-------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="5ccfe-108">Создание нового приложения COM+</span><span class="sxs-lookup"><span data-stu-id="5ccfe-108">Creating a New COM+ Application</span></span>](creating-a-new-com--application.md)<br/>                           | <span data-ttu-id="5ccfe-109">Описывает создание нового приложения COM+.</span><span class="sxs-lookup"><span data-stu-id="5ccfe-109">Describes how to create a new COM+ application.</span></span><br/>                         |
| [<span data-ttu-id="5ccfe-110">Установка новых компонентов</span><span class="sxs-lookup"><span data-stu-id="5ccfe-110">Installing New Components</span></span>](installing-new-components.md)<br/>                                       | <span data-ttu-id="5ccfe-111">Описывает установку новых компонентов.</span><span class="sxs-lookup"><span data-stu-id="5ccfe-111">Describes how to install new components.</span></span><br/>                                |
| [<span data-ttu-id="5ccfe-112">Импорт компонентов</span><span class="sxs-lookup"><span data-stu-id="5ccfe-112">Importing Components</span></span>](importing-components.md)<br/>                                                 | <span data-ttu-id="5ccfe-113">Описывает, как импортировать компоненты.</span><span class="sxs-lookup"><span data-stu-id="5ccfe-113">Describes how to import components.</span></span><br/>                                     |
| [<span data-ttu-id="5ccfe-114">Удаление компонента из приложения COM+</span><span class="sxs-lookup"><span data-stu-id="5ccfe-114">Removing a Component from a COM+ Application</span></span>](removing-a-component-from-a-com--application.md)<br/> | <span data-ttu-id="5ccfe-115">Описывает, как удалить компонент из приложения COM+.</span><span class="sxs-lookup"><span data-stu-id="5ccfe-115">Describes how to delete a component from a COM+ application.</span></span><br/>            |
| [<span data-ttu-id="5ccfe-116">Перемещение компонентов</span><span class="sxs-lookup"><span data-stu-id="5ccfe-116">Moving Components</span></span>](moving-components.md)<br/>                                                       | <span data-ttu-id="5ccfe-117">Описывает, как переместить компонент из одного приложения COM+ в другое.</span><span class="sxs-lookup"><span data-stu-id="5ccfe-117">Describes how to move a component from one COM+ application to another.</span></span><br/> |
| [<span data-ttu-id="5ccfe-118">Копирование компонентов</span><span class="sxs-lookup"><span data-stu-id="5ccfe-118">Copying Components</span></span>](copying-components.md)<br/>                                                     | <span data-ttu-id="5ccfe-119">Описывает копирование компонента из одного приложения COM+ в другое.</span><span class="sxs-lookup"><span data-stu-id="5ccfe-119">Describes how to copy a component from one COM+ application to another.</span></span><br/> |
| [<span data-ttu-id="5ccfe-120">Удаление приложения COM+</span><span class="sxs-lookup"><span data-stu-id="5ccfe-120">Deleting a COM+ Application</span></span>](deleting-a-com--application.md)<br/>                                   | <span data-ttu-id="5ccfe-121">Описывает, как удалить приложение COM+.</span><span class="sxs-lookup"><span data-stu-id="5ccfe-121">Describes how to delete a COM+ application.</span></span><br/>                             |



 

<span data-ttu-id="5ccfe-122">Основные сведения о процедурах, описанных в этом разделе, см. в разделе [Общие сведения о приложении COM+](com--application-overview.md) и [развертывание приложений COM+](deploying-com--applications.md).</span><span class="sxs-lookup"><span data-stu-id="5ccfe-122">For conceptual information on the procedures described in this section, see [COM+ Application Overview](com--application-overview.md) and [Deploying COM+ Applications](deploying-com--applications.md).</span></span>

<span data-ttu-id="5ccfe-123">Практические сведения о задачах администрирования, связанных с экспортом и установкой приложений COM+, см. в разделе "Установка приложений COM+" раздела "Администрирование служб компонентов".</span><span class="sxs-lookup"><span data-stu-id="5ccfe-123">For procedural information on the administrative tasks involved in exporting and installing COM+ applications, see "Installing COM+ Applications" in the Component Services Administrator's Guide.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5ccfe-124">См. также</span><span class="sxs-lookup"><span data-stu-id="5ccfe-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5ccfe-125">Автоматизация администрирования COM+</span><span class="sxs-lookup"><span data-stu-id="5ccfe-125">Automating COM+ Administration</span></span>](automating-com--administration.md)
</dt> <dt>

[<span data-ttu-id="5ccfe-126">Настройка приложений COM+</span><span class="sxs-lookup"><span data-stu-id="5ccfe-126">Configuring COM+ Applications</span></span>](configuring-com--applications.md)
</dt> <dt>

[<span data-ttu-id="5ccfe-127">Преобразование пакетов MTS в приложения COM+</span><span class="sxs-lookup"><span data-stu-id="5ccfe-127">Conversion of MTS Packages to COM+ Applications</span></span>](conversion-of-mts-packages-to-com--applications.md)
</dt> </dl>

 

 




