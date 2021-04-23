---
description: Чтобы добавить компоненты в папку Components приложения COM+, можно либо использовать мастер установки компонента COM+, либо перетащить DLL-файлы, содержащие компоненты, из проводника Windows и удалить их в приложении.
ms.assetid: 3cb0c24d-cd52-42ac-8b07-d8774698b90c
title: Установка новых компонентов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 434bdb59c0a0e9c786bb3460a0cb1cbb6a1f50dd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072484"
---
# <a name="installing-new-components"></a><span data-ttu-id="b4669-103">Установка новых компонентов</span><span class="sxs-lookup"><span data-stu-id="b4669-103">Installing New Components</span></span>

<span data-ttu-id="b4669-104">Чтобы добавить компоненты в папку **Components** приложения COM+, можно либо использовать мастер установки компонента COM+, либо перетащить DLL-файлы, содержащие компоненты, из проводника Windows и удалить их в приложении.</span><span class="sxs-lookup"><span data-stu-id="b4669-104">To add components to the **Components** folder of a COM+ application, you can either use the COM+ Component Install Wizard or drag .dll files that contain the components from the Windows Explorer and drop them in the application.</span></span>

<span data-ttu-id="b4669-105">При использовании мастера установки компонента COM+ можно либо установить новый компонент, который регистрирует компонент на компьютере, либо импортировать уже зарегистрированные компоненты.</span><span class="sxs-lookup"><span data-stu-id="b4669-105">If you use the COM+ Component Install Wizard, you can either install a new component, which registers the component on the computer, or import components that have already been registered.</span></span> <span data-ttu-id="b4669-106">Компоненты можно добавлять в пустые приложения или существующие приложения.</span><span class="sxs-lookup"><span data-stu-id="b4669-106">Components can be added to empty applications or existing applications.</span></span>

<span data-ttu-id="b4669-107">**Добавление компонента в приложение COM+**</span><span class="sxs-lookup"><span data-stu-id="b4669-107">**To add a component to a COM+ application**</span></span>

1.  <span data-ttu-id="b4669-108">В дереве консоли средства администрирования "службы компонентов" выберите компьютер, на котором размещено приложение COM+.</span><span class="sxs-lookup"><span data-stu-id="b4669-108">In the console tree of the Component Services administrative tool, select the computer hosting the COM+ application.</span></span>

2.  <span data-ttu-id="b4669-109">Откройте папку **приложения COM+** для этого компьютера и выберите приложение, в котором необходимо установить компоненты.</span><span class="sxs-lookup"><span data-stu-id="b4669-109">Open the **COM+ Applications** folder for that computer, and select the application in which you want to install the component(s).</span></span>

3.  <span data-ttu-id="b4669-110">Откройте папку приложение и выберите **компоненты**.</span><span class="sxs-lookup"><span data-stu-id="b4669-110">Open the application folder and select **Components**.</span></span>

4.  <span data-ttu-id="b4669-111">В меню **действие** наведите указатель на пункт **создать** и выберите пункт **компонент**.</span><span class="sxs-lookup"><span data-stu-id="b4669-111">On the **Action** menu, point to **New**, and then click **Component**.</span></span> <span data-ttu-id="b4669-112">Можно также щелкнуть правой кнопкой мыши папку **компоненты** , наведите указатель на пункт **создать** и выберите пункт **компонент**.</span><span class="sxs-lookup"><span data-stu-id="b4669-112">You can also right-click the **Components** folder, point to **New**, and then click **Component**.</span></span>

5.  <span data-ttu-id="b4669-113">На странице **приветствия** мастера установки приложения COM+ нажмите кнопку **Далее**, а затем в диалоговом окне **Импорт или установка компонента** нажмите кнопку **установить новые компоненты** .</span><span class="sxs-lookup"><span data-stu-id="b4669-113">On the **Welcome** page of the COM+ Application Install Wizard, click **Next**, and then in the **Import or Install a Component** dialog box, click **Install new components** .</span></span>

6.  <span data-ttu-id="b4669-114">В диалоговом окне **Установка новых компонентов** нажмите кнопку **Добавить** , чтобы выбрать компонент, который нужно добавить.</span><span class="sxs-lookup"><span data-stu-id="b4669-114">In the **Install new components** dialog box, click **Add** to browse for the component you want to add.</span></span>

7.  <span data-ttu-id="b4669-115">В диалоговом окне **Выбор файлов для установки** введите имя файла компонента для установки или выберите имя файла из отображаемого списка.</span><span class="sxs-lookup"><span data-stu-id="b4669-115">In the **Select files to install** dialog box, type the filename of the component to install or select a filename from the displayed list.</span></span> <span data-ttu-id="b4669-116">Нажмите кнопку **Открыть**.</span><span class="sxs-lookup"><span data-stu-id="b4669-116">Click **Open**.</span></span>

    <span data-ttu-id="b4669-117">После добавления файлов в диалоговом окне **Установка новых компонентов** отображаются добавленные файлы и связанные с ними компоненты.</span><span class="sxs-lookup"><span data-stu-id="b4669-117">After you add the files, the **Install new components** dialog box displays the files you have added and their associated components.</span></span> <span data-ttu-id="b4669-118">Если установить флажок **сведения** , будут отображаться дополнительные сведения о содержимом файлов и найденных компонентах.</span><span class="sxs-lookup"><span data-stu-id="b4669-118">If you select the **Details** check box, you will see more information about file contents and the components that were found.</span></span>

    > [!Note]  
    > <span data-ttu-id="b4669-119">Ненастроенные COM-компоненты должны иметь библиотеку типов.</span><span class="sxs-lookup"><span data-stu-id="b4669-119">Unconfigured COM components must have a type library.</span></span> <span data-ttu-id="b4669-120">Если COM+ не удается найти библиотеку типов вашего компонента, компонент не появится в списке.</span><span class="sxs-lookup"><span data-stu-id="b4669-120">If COM+ cannot find your component's type library, your component will not appear in the list.</span></span> <span data-ttu-id="b4669-121">Можно также удалить файл из списка **файлов для установки** , выбрав его и нажав кнопку **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="b4669-121">You can also remove a file from the **Files to install** list by selecting it and clicking **Remove**.</span></span>

     

8.  <span data-ttu-id="b4669-122">Нажмите кнопку **Далее**, а затем кнопку **Готово** , чтобы установить компонент.</span><span class="sxs-lookup"><span data-stu-id="b4669-122">Click **Next**, and then click **Finish** to install the component.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b4669-123">См. также</span><span class="sxs-lookup"><span data-stu-id="b4669-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b4669-124">Копирование компонентов</span><span class="sxs-lookup"><span data-stu-id="b4669-124">Copying Components</span></span>](copying-components.md)
</dt> <dt>

[<span data-ttu-id="b4669-125">Создание нового приложения COM+</span><span class="sxs-lookup"><span data-stu-id="b4669-125">Creating a New COM+ Application</span></span>](creating-a-new-com--application.md)
</dt> <dt>

[<span data-ttu-id="b4669-126">Удаление приложения COM+</span><span class="sxs-lookup"><span data-stu-id="b4669-126">Deleting a COM+ Application</span></span>](deleting-a-com--application.md)
</dt> <dt>

[<span data-ttu-id="b4669-127">Импорт компонентов</span><span class="sxs-lookup"><span data-stu-id="b4669-127">Importing Components</span></span>](importing-components.md)
</dt> <dt>

[<span data-ttu-id="b4669-128">Перемещение компонентов</span><span class="sxs-lookup"><span data-stu-id="b4669-128">Moving Components</span></span>](moving-components.md)
</dt> <dt>

[<span data-ttu-id="b4669-129">Удаление компонента из приложения COM+</span><span class="sxs-lookup"><span data-stu-id="b4669-129">Removing a Component from a COM+ Application</span></span>](removing-a-component-from-a-com--application.md)
</dt> </dl>

 

 



