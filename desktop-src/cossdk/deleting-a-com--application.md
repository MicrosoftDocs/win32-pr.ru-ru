---
description: Поскольку существующие приложения устарели или больше не используются, их может потребоваться удалить.
ms.assetid: 5cce94c9-8eff-40b9-946d-a57749da073d
title: Удаление приложения COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da685e5a7ae7590fcc247caa765d49dc34d076e9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423398"
---
# <a name="deleting-a-com-application"></a><span data-ttu-id="d2e09-103">Удаление приложения COM+</span><span class="sxs-lookup"><span data-stu-id="d2e09-103">Deleting a COM+ Application</span></span>

<span data-ttu-id="d2e09-104">Поскольку существующие приложения устарели или больше не используются, их может потребоваться удалить.</span><span class="sxs-lookup"><span data-stu-id="d2e09-104">As existing applications become dated or are no longer being used, you may need to remove them.</span></span>

<span data-ttu-id="d2e09-105">**Удаление приложения COM+**</span><span class="sxs-lookup"><span data-stu-id="d2e09-105">**To delete a COM+ application**</span></span>

1.  <span data-ttu-id="d2e09-106">В дереве консоли средства администрирования "службы компонентов" выберите компьютер, для которого необходимо удалить приложение.</span><span class="sxs-lookup"><span data-stu-id="d2e09-106">In the console tree of the Component Services administrative tool, select the computer for which you want to delete an application.</span></span>

2.  <span data-ttu-id="d2e09-107">Откройте папку **приложения COM+** для указанного компьютера, чтобы отобразить все приложения.</span><span class="sxs-lookup"><span data-stu-id="d2e09-107">Open the **COM+ Applications** folder for the specified computer to display all the applications.</span></span>

3.  <span data-ttu-id="d2e09-108">Выберите приложение, которое нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="d2e09-108">Select the application you want to remove.</span></span>

4.  <span data-ttu-id="d2e09-109">Если вы выбрали серверное приложение, завершите работу приложения.</span><span class="sxs-lookup"><span data-stu-id="d2e09-109">If you selected a server application, shut down the application.</span></span> <span data-ttu-id="d2e09-110">Можно завершить работу приложения, выбрав его в средстве администрирования "службы компонентов", щелкнув правой кнопкой мыши и выбрав пункт **Завершение работы**.</span><span class="sxs-lookup"><span data-stu-id="d2e09-110">You can shut down an application by selecting it in the Component Services administrative tool, right-clicking, and then clicking **Shut down**.</span></span> <span data-ttu-id="d2e09-111">Если вы выбрали приложение библиотеки, убедитесь, что все процессы, использующие это приложение библиотеки, закрыты.</span><span class="sxs-lookup"><span data-stu-id="d2e09-111">If you selected a library application, make sure that all processes currently using this library application are shut down.</span></span>

5.  <span data-ttu-id="d2e09-112">В меню **действие** выберите команду **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="d2e09-112">On the **Action** menu, click **Delete**.</span></span> <span data-ttu-id="d2e09-113">Можно также щелкнуть правой кнопкой мыши имя приложения и выбрать команду **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="d2e09-113">You can also right-click the application name and then click **Delete**.</span></span> <span data-ttu-id="d2e09-114">Можно также удалить приложение, выбрав его в средстве администрирования "службы компонентов" и нажав клавишу **Delete** . также можно выбрать приложение, щелкнуть его правой кнопкой мыши и выбрать команду **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="d2e09-114">You can also delete an application by selecting it in the Component Services administrative tool and pressing the **Delete** key, or you can select the application, right-click, and then click **Delete**.</span></span>

6.  <span data-ttu-id="d2e09-115">Нажмите кнопку **Да** при появлении запроса на подтверждение действия.</span><span class="sxs-lookup"><span data-stu-id="d2e09-115">Click **Yes** when prompted to confirm your action.</span></span>

<span data-ttu-id="d2e09-116">Кроме того, если серверное приложение или прокси приложения установлены на компьютере с помощью установщик Windows (как описано в разделе "Установка приложений COM+" в разделе "Администрирование служб компонентов"), его можно удалить с помощью программы установки и удаления программ на панели управления Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="d2e09-116">In addition, if a server application or application proxy has been installed on a computer using Windows Installer (as described in "Installing COM+ Applications" in the Component Services Administration Guide), you can delete it through the Add/Remove Programs utility in the Microsoft Windows Control Panel.</span></span> <span data-ttu-id="d2e09-117">Или можно удалить установленное серверное приложение или прокси приложения с помощью установщик Windows командной строки:</span><span class="sxs-lookup"><span data-stu-id="d2e09-117">Or you can delete an installed server application or application proxy by using the Windows Installer command line syntax:</span></span>

<span data-ttu-id="d2e09-118">**msiexec-x** *\_ имя приложения \* \* *. msi**</span><span class="sxs-lookup"><span data-stu-id="d2e09-118">**msiexec -x** *application\_name\*\*\*.msi*\*</span></span>

<span data-ttu-id="d2e09-119">Эти методы особенно полезны для удаления приложений COM+ на клиентских компьютерах, на которых не выполняется средство администрирования "службы компонентов".</span><span class="sxs-lookup"><span data-stu-id="d2e09-119">These methods are especially useful for deleting COM+ applications on client machines that are not running the Component Services administrative tool.</span></span>

<span data-ttu-id="d2e09-120">При удалении приложения также удаляются все компоненты, содержащиеся в приложении.</span><span class="sxs-lookup"><span data-stu-id="d2e09-120">Deleting the application also deletes any components contained in the application.</span></span> <span data-ttu-id="d2e09-121">Если эти компоненты зависят от дополнительных ресурсов (подключения к базе данных, файлы данных или текстовых файлов, Конфигурация виртуальных корневых компонентов IIS и т. д.), эти ресурсы необходимо удалить с помощью механизмов, отличных от средства администрирования служб компонентов.</span><span class="sxs-lookup"><span data-stu-id="d2e09-121">If these components depend on additional resources (database connections, data or text files, IIS virtual root configuration, and so on), these resources must be removed through mechanisms other than the Component Services administrative tool.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d2e09-122">См. также</span><span class="sxs-lookup"><span data-stu-id="d2e09-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d2e09-123">Копирование компонентов</span><span class="sxs-lookup"><span data-stu-id="d2e09-123">Copying Components</span></span>](copying-components.md)
</dt> <dt>

[<span data-ttu-id="d2e09-124">Создание нового приложения COM+</span><span class="sxs-lookup"><span data-stu-id="d2e09-124">Creating a New COM+ Application</span></span>](creating-a-new-com--application.md)
</dt> <dt>

[<span data-ttu-id="d2e09-125">Импорт компонентов</span><span class="sxs-lookup"><span data-stu-id="d2e09-125">Importing Components</span></span>](importing-components.md)
</dt> <dt>

[<span data-ttu-id="d2e09-126">Установка новых компонентов</span><span class="sxs-lookup"><span data-stu-id="d2e09-126">Installing New Components</span></span>](installing-new-components.md)
</dt> <dt>

[<span data-ttu-id="d2e09-127">Перемещение компонентов</span><span class="sxs-lookup"><span data-stu-id="d2e09-127">Moving Components</span></span>](moving-components.md)
</dt> <dt>

[<span data-ttu-id="d2e09-128">Удаление компонента из приложения COM+</span><span class="sxs-lookup"><span data-stu-id="d2e09-128">Removing a Component from a COM+ Application</span></span>](removing-a-component-from-a-com--application.md)
</dt> </dl>

 

 



