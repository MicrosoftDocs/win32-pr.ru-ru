---
title: Управление устройством
description: После обнаружения устройств их можно контролировать.
ms.assetid: 6d0efb80-d6f5-4b36-a184-19f06afeb2a7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ff91339c67b67de5d3e90eda0ce64ebcc68b9e2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103889020"
---
# <a name="controlling-a-device"></a><span data-ttu-id="79cd5-103">Управление устройством</span><span class="sxs-lookup"><span data-stu-id="79cd5-103">Controlling a Device</span></span>

<span data-ttu-id="79cd5-104">После обнаружения устройств их можно контролировать.</span><span class="sxs-lookup"><span data-stu-id="79cd5-104">Once you have discovered devices, you can control them.</span></span>

<span data-ttu-id="79cd5-105">**Просмотр свойств устройства**</span><span class="sxs-lookup"><span data-stu-id="79cd5-105">**To view device properties**</span></span>

1.  <span data-ttu-id="79cd5-106">Выберите устройство в списке **найденные устройства** .</span><span class="sxs-lookup"><span data-stu-id="79cd5-106">Select a device from the **Devices Found** list.</span></span>
2.  <span data-ttu-id="79cd5-107">Щелкните **Свойства устройства**.</span><span class="sxs-lookup"><span data-stu-id="79cd5-107">Click **Device Properties**.</span></span> <span data-ttu-id="79cd5-108">Откроется окно **Свойства устройства** с запрошенными сведениями.</span><span class="sxs-lookup"><span data-stu-id="79cd5-108">The **Device Properties** window appears with the requested information.</span></span>

> [!Note]  
> <span data-ttu-id="79cd5-109">Функция **просмотра представления** недоступна в примере кода C++.</span><span class="sxs-lookup"><span data-stu-id="79cd5-109">The **View Presentation** functionality is not available in the C++ sample code.</span></span>

 

<span data-ttu-id="79cd5-110">**Просмотр страницы презентации устройства**</span><span class="sxs-lookup"><span data-stu-id="79cd5-110">**To view a device's presentation page**</span></span>

1.  <span data-ttu-id="79cd5-111">Выберите устройство в списке **найденные устройства** .</span><span class="sxs-lookup"><span data-stu-id="79cd5-111">Select a device from the **Devices Found** list.</span></span>
2.  <span data-ttu-id="79cd5-112">Нажмите кнопку **Просмотреть презентацию**.</span><span class="sxs-lookup"><span data-stu-id="79cd5-112">Click **View Presentation**.</span></span> <span data-ttu-id="79cd5-113">Откроется окно Internet Explorer с запрошенной страницей презентации.</span><span class="sxs-lookup"><span data-stu-id="79cd5-113">An Internet Explorer window appears with the requested presentation page.</span></span>

> [!Note]  
> <span data-ttu-id="79cd5-114">Функция **View Service DESC.** функциональная возможность недоступна в примере кода C++.</span><span class="sxs-lookup"><span data-stu-id="79cd5-114">The **View Service Desc.** functionality is not available in the C++ sample code.</span></span>

 

<span data-ttu-id="79cd5-115">**Просмотр описания службы**</span><span class="sxs-lookup"><span data-stu-id="79cd5-115">**To view a service description**</span></span>

1.  <span data-ttu-id="79cd5-116">URL-адрес описания службы можно ввести в поле **Service DESC. Поле URL-адреса** .</span><span class="sxs-lookup"><span data-stu-id="79cd5-116">You can enter the URL to the service description in the **Service Desc. URL** field.</span></span>

    ![URL-адрес описания службы](images/ucp-url.png)

2.  <span data-ttu-id="79cd5-118">Щелкните **View Service DESC.** Откроется окно **средства просмотра описания службы** .</span><span class="sxs-lookup"><span data-stu-id="79cd5-118">Click **View Service Desc.** The **Service Description Viewer** window is displayed.</span></span> <span data-ttu-id="79cd5-119">Затем можно просмотреть описание службы с помощью древовидного представления.</span><span class="sxs-lookup"><span data-stu-id="79cd5-119">You can then browse the service description using the tree view.</span></span> <span data-ttu-id="79cd5-120">Эта функция недоступна в примере кода C++.</span><span class="sxs-lookup"><span data-stu-id="79cd5-120">This functionality is not available in the C++ sample code.</span></span>

    ![окно средства просмотра описания службы](images/ucp-serv.png)

    <span data-ttu-id="79cd5-122">В окне средства просмотра описания служб можно использовать пять команд.</span><span class="sxs-lookup"><span data-stu-id="79cd5-122">There are five commands you can use in the Service Description Viewer window.</span></span>



| <span data-ttu-id="79cd5-123">Кнопка</span><span class="sxs-lookup"><span data-stu-id="79cd5-123">Button</span></span>                 | <span data-ttu-id="79cd5-124">Выполненное действие</span><span class="sxs-lookup"><span data-stu-id="79cd5-124">Action Performed</span></span>                                                                                                                                                                      |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="79cd5-125">Go</span><span class="sxs-lookup"><span data-stu-id="79cd5-125">Go</span></span>                     | <span data-ttu-id="79cd5-126">Загружает файл, показанный в **службе DESC. Поле URL-адреса** .</span><span class="sxs-lookup"><span data-stu-id="79cd5-126">Loads the file shown in the **Service Desc. URL** field.</span></span>                                                                                                                              |
| <span data-ttu-id="79cd5-127">Задание действия</span><span class="sxs-lookup"><span data-stu-id="79cd5-127">Set Action</span></span>             | <span data-ttu-id="79cd5-128">Выберите имя действия в дереве описания службы и щелкните **задать действие**.</span><span class="sxs-lookup"><span data-stu-id="79cd5-128">Select an action name in the service description tree and click **Set Action**.</span></span> <span data-ttu-id="79cd5-129">Имя действия указывается в поле действие при **вызове** основного **универсального окна управления служебной программой** .</span><span class="sxs-lookup"><span data-stu-id="79cd5-129">The action name is entered into the **Invoke Action** field of the main **Generic UCP** window.</span></span>       |
| <span data-ttu-id="79cd5-130">Установка значения переменной</span><span class="sxs-lookup"><span data-stu-id="79cd5-130">Set Variable</span></span>           | <span data-ttu-id="79cd5-131">Выберите имя переменной в дереве описания службы и нажмите кнопку **задать переменную**.</span><span class="sxs-lookup"><span data-stu-id="79cd5-131">Select a variable name in the service description tree and click **Set Variable**.</span></span> <span data-ttu-id="79cd5-132">Имя переменной задается в поле **переменная запроса** основного **универсального окна управления служебной программой (UCP** ).</span><span class="sxs-lookup"><span data-stu-id="79cd5-132">The variable name is entered into the **Query Variable** field of the main **Generic UCP** window.</span></span> |
| <span data-ttu-id="79cd5-133">Заполнить список переменных</span><span class="sxs-lookup"><span data-stu-id="79cd5-133">Populate Variable List</span></span> | <span data-ttu-id="79cd5-134">Загружает все имена переменных службы в список **переменных запроса** основного **универсального окна управления служебной программой (UCP** ).</span><span class="sxs-lookup"><span data-stu-id="79cd5-134">Loads all the service's variable names into the **Query Variable** list of the main **Generic UCP** window.</span></span>                                                                           |
| <span data-ttu-id="79cd5-135">Заполнение списка действий</span><span class="sxs-lookup"><span data-stu-id="79cd5-135">Populate Action List</span></span>   | <span data-ttu-id="79cd5-136">Загружает все имена действий службы в список **действий Invoke** основного **универсального окна управления служебной программой** .</span><span class="sxs-lookup"><span data-stu-id="79cd5-136">Loads all the service's action names into the **Invoke Action** list of the main **Generic UCP** window.</span></span>                                                                              |



 

<span data-ttu-id="79cd5-137">**Управление устройством**</span><span class="sxs-lookup"><span data-stu-id="79cd5-137">**To control a device**</span></span>

1.  <span data-ttu-id="79cd5-138">В списке **обнаруженные устройства** выберите устройство, которое требуется контролировать.</span><span class="sxs-lookup"><span data-stu-id="79cd5-138">From the **Devices Found** list, select the device you want to control.</span></span>
2.  <span data-ttu-id="79cd5-139">В списке **выберите службу** выберите службу, которую нужно вызвать, или переменную состояния, к которой необходимо выполнить запрос.</span><span class="sxs-lookup"><span data-stu-id="79cd5-139">From the **Choose Service** list, select the service you want to invoke or state variable you want to query.</span></span>

    ![окно управления устройствами](images/ucp-contr.png)

    > [!Note]  
    > <span data-ttu-id="79cd5-141">Содержимое **списка служб** основано на устройстве, выбранном в списке **найденные устройства** .</span><span class="sxs-lookup"><span data-stu-id="79cd5-141">The contents of the **Service List** is based on the device selected in the **Devices Found** list.</span></span>

     

3.  <span data-ttu-id="79cd5-142">Если вы хотите узнать значение переменной состояния для выбранной службы, введите имя переменной в поле " **переменная запроса** " для параметра "служба".</span><span class="sxs-lookup"><span data-stu-id="79cd5-142">If you want to find out the value of a state variable for the selected service, enter the variable name in the **Query Variable** field for service.</span></span> <span data-ttu-id="79cd5-143">Нажмите кнопку **Запрос**.</span><span class="sxs-lookup"><span data-stu-id="79cd5-143">Click **Query**.</span></span> <span data-ttu-id="79cd5-144">Результаты отображаются в поле **значение состояния запроса/аргументы исходящих действий** .</span><span class="sxs-lookup"><span data-stu-id="79cd5-144">The results are shown in the **Query State Value/Action Out Arguments** field.</span></span>
4.  <span data-ttu-id="79cd5-145">Если вы хотите вызвать действие для службы, введите имя действия в поле **Действие вызова** и любые аргументы в поле **аргументы действия** .</span><span class="sxs-lookup"><span data-stu-id="79cd5-145">If you want to invoke an action for a service, enter the action name in the **Invoke Action** field, and any arguments in the **Action Arguments** field.</span></span> <span data-ttu-id="79cd5-146">Нажмите кнопку **вызвать**.</span><span class="sxs-lookup"><span data-stu-id="79cd5-146">Click **Invoke**.</span></span> <span data-ttu-id="79cd5-147">Результаты отображаются в поле **значение состояния запроса или аргументы исходящих действий** (при наличии).</span><span class="sxs-lookup"><span data-stu-id="79cd5-147">The results are shown in the **Query State Value/Action Out Arguments** field, if any.</span></span>

    <span data-ttu-id="79cd5-148">Возвращаемое значение, если таковое имеется, содержится в первом аргументе out.</span><span class="sxs-lookup"><span data-stu-id="79cd5-148">The return value, if any, is contained in the first out argument.</span></span>

    > [!Note]  
    > <span data-ttu-id="79cd5-149">Если для действия существует несколько аргументов, разделите их пробелами.</span><span class="sxs-lookup"><span data-stu-id="79cd5-149">If there are multiple arguments for an action, separate them with spaces.</span></span>

     

5.  <span data-ttu-id="79cd5-150">Просмотрите сведения о событиях в поле **события** для выбранной службы.</span><span class="sxs-lookup"><span data-stu-id="79cd5-150">View eventing information in the **Events** field for the selected service.</span></span>

 

 




