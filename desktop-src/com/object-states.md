---
title: Состояния объектов
description: Состояния объектов
ms.assetid: 8ebef6d6-7a2f-4b95-91ca-999646cde82d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 268b9bc9c69009850a5172259ab7a13c760d2c72
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105700491"
---
# <a name="object-states"></a><span data-ttu-id="b672e-103">Состояния объектов</span><span class="sxs-lookup"><span data-stu-id="b672e-103">Object States</span></span>

<span data-ttu-id="b672e-104">Составной объект существует в одном из трех состояний: passive, загружен или выполняется.</span><span class="sxs-lookup"><span data-stu-id="b672e-104">A compound object exists in one of three states: passive, loaded, or running.</span></span> <span data-ttu-id="b672e-105">Состояние объекта составного документа описывает связь между объектом в его контейнере и приложением, ответственным за его создание.</span><span class="sxs-lookup"><span data-stu-id="b672e-105">A compound-document object's state describes the relationship between the object in its container and the application responsible for its creation.</span></span> <span data-ttu-id="b672e-106">Эти состояния обобщены в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="b672e-106">The following table summarizes these states.</span></span>



| <span data-ttu-id="b672e-107">Состояние объекта</span><span class="sxs-lookup"><span data-stu-id="b672e-107">Object state</span></span>       | <span data-ttu-id="b672e-108">Описание</span><span class="sxs-lookup"><span data-stu-id="b672e-108">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                         |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b672e-109">Пассивно</span><span class="sxs-lookup"><span data-stu-id="b672e-109">Passive</span></span><br/> | <span data-ttu-id="b672e-110">Объект составного документа существует только в хранилище на диске или в базе данных.</span><span class="sxs-lookup"><span data-stu-id="b672e-110">The compound-document object exists only in storage, either on disk or in a database.</span></span> <span data-ttu-id="b672e-111">В этом состоянии объект недоступен для просмотра или редактирования.</span><span class="sxs-lookup"><span data-stu-id="b672e-111">In this state, the object is unavailable for viewing or editing.</span></span><br/>                                                                                                                                                                                                                                   |
| <span data-ttu-id="b672e-112">Загружен</span><span class="sxs-lookup"><span data-stu-id="b672e-112">Loaded</span></span><br/>  | <span data-ttu-id="b672e-113">Структуры данных объекта, созданные обработчиком объектов, находятся в памяти контейнера.</span><span class="sxs-lookup"><span data-stu-id="b672e-113">The object's data structures created by the object handler are in the container's memory.</span></span> <span data-ttu-id="b672e-114">Контейнер установил связь с обработчиком объектов, и для визуализации объекта доступны кэшированные данные представления.</span><span class="sxs-lookup"><span data-stu-id="b672e-114">The container has established communication with the object handler and there is cached presentation data available for rendering the object.</span></span> <span data-ttu-id="b672e-115">Вызовы обрабатываются обработчиком объектов.</span><span class="sxs-lookup"><span data-stu-id="b672e-115">Calls are processed by the object handler.</span></span> <span data-ttu-id="b672e-116">Это состояние, вызванное низкой нагрузкой, используется, когда пользователь просто просматривает или печатает объект.</span><span class="sxs-lookup"><span data-stu-id="b672e-116">This state, because of its low overhead, is used when a user is simply viewing or printing an object.</span></span><br/> |
| <span data-ttu-id="b672e-117">Запущен</span><span class="sxs-lookup"><span data-stu-id="b672e-117">Running</span></span><br/> | <span data-ttu-id="b672e-118">Объекты, управляющие удаленным взаимодействием, были созданы и запущено серверное приложение OLE.</span><span class="sxs-lookup"><span data-stu-id="b672e-118">The objects that control remoting have been created and the OLE server application is running.</span></span> <span data-ttu-id="b672e-119">Интерфейсы объекта доступны, и контейнер может получать уведомления об изменениях.</span><span class="sxs-lookup"><span data-stu-id="b672e-119">The object's interfaces are accessible, and the container can receive notification of changes.</span></span> <span data-ttu-id="b672e-120">В этом состоянии конечный пользователь может редактировать объект или иным образом манипулировать им.</span><span class="sxs-lookup"><span data-stu-id="b672e-120">In this state, an end user can edit or otherwise manipulate the object.</span></span><br/>                                                                                                                    |



 

<span data-ttu-id="b672e-121">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="b672e-121">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="b672e-122">Вход в загруженное состояние</span><span class="sxs-lookup"><span data-stu-id="b672e-122">Entering the Loaded State</span></span>](entering-the-loaded-state.md)
-   [<span data-ttu-id="b672e-123">Вход в состояние выполнения</span><span class="sxs-lookup"><span data-stu-id="b672e-123">Entering the Running State</span></span>](entering-the-running-state.md)
-   [<span data-ttu-id="b672e-124">Вход в пассивное состояние</span><span class="sxs-lookup"><span data-stu-id="b672e-124">Entering the Passive State</span></span>](entering-the-passive-state.md)

## <a name="related-topics"></a><span data-ttu-id="b672e-125">См. также</span><span class="sxs-lookup"><span data-stu-id="b672e-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b672e-126">Составные документы</span><span class="sxs-lookup"><span data-stu-id="b672e-126">Compound Documents</span></span>](compound-documents.md)
</dt> </dl>

 

 





