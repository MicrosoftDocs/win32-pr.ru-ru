---
description: Компонент можно скопировать из одного приложения COM+ в другое. После копирования компонента в другое приложение COM+ этот компонент можно настроить не так, как исходный компонент.
ms.assetid: 49dfd449-05eb-4442-989f-15bc1586d8c5
title: Копирование компонентов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2224c42e9891c67999934062a50cd2215da2adc4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538819"
---
# <a name="copying-components"></a><span data-ttu-id="a8da0-104">Копирование компонентов</span><span class="sxs-lookup"><span data-stu-id="a8da0-104">Copying Components</span></span>

<span data-ttu-id="a8da0-105">Компонент можно скопировать из одного приложения COM+ в другое.</span><span class="sxs-lookup"><span data-stu-id="a8da0-105">You can copy a component from one COM+ application to another.</span></span> <span data-ttu-id="a8da0-106">После копирования компонента в другое приложение COM+ этот компонент можно настроить не так, как исходный компонент.</span><span class="sxs-lookup"><span data-stu-id="a8da0-106">After you copy a component to another COM+ application, you can configure this component differently than the original component.</span></span>

<span data-ttu-id="a8da0-107">**Копирование компонента из одного приложения COM+ в другое**</span><span class="sxs-lookup"><span data-stu-id="a8da0-107">**To copy a component from one COM+ application to another**</span></span>

1.  <span data-ttu-id="a8da0-108">В области сведений средства администрирования "службы компонентов" щелкните правой кнопкой мыши компонент, который необходимо скопировать, и выберите команду **Копировать**.</span><span class="sxs-lookup"><span data-stu-id="a8da0-108">In the details pane of the Component Services administrative tool, right-click the component that you want to copy and then click **Copy**.</span></span>

2.  <span data-ttu-id="a8da0-109">В диалоговом окне **копирование компонента** в области **Выбор назначения** выберите приложение COM+, в которое будет скопирован компонент.</span><span class="sxs-lookup"><span data-stu-id="a8da0-109">In the **Copy Component** dialog box, in the **Please select a Destination** pane, select the COM+ application to which the component will be copied.</span></span>

3.  <span data-ttu-id="a8da0-110">Введите новый идентификатор ProgID для скопированного компонента.</span><span class="sxs-lookup"><span data-stu-id="a8da0-110">Enter the new ProgID for the copied component.</span></span>

    > [!Note]  
    > <span data-ttu-id="a8da0-111">Идентификатор ProgID для исходного компонента отображается для справки и не может быть изменен.</span><span class="sxs-lookup"><span data-stu-id="a8da0-111">The ProgID for the original component is displayed for reference and cannot be changed.</span></span>

     

4.  <span data-ttu-id="a8da0-112">Введите новый идентификатор CLSID для скопированного компонента.</span><span class="sxs-lookup"><span data-stu-id="a8da0-112">Enter the new CLSID for the copied component.</span></span> <span data-ttu-id="a8da0-113">COM+ отображает автоматически созданный CLSID.</span><span class="sxs-lookup"><span data-stu-id="a8da0-113">COM+ displays an automatically generated CLSID.</span></span> <span data-ttu-id="a8da0-114">В большинстве случаев это достаточно для уникальной идентификации скопированного компонента.</span><span class="sxs-lookup"><span data-stu-id="a8da0-114">In most cases, this will be sufficient to uniquely identify the copied component.</span></span> <span data-ttu-id="a8da0-115">Введите новый идентификатор CLSID, только если вы хотите изменить его, предоставленный COM+.</span><span class="sxs-lookup"><span data-stu-id="a8da0-115">Enter a new CLSID only if you want to change the one provided by COM+.</span></span>

5.  <span data-ttu-id="a8da0-116">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="a8da0-116">Click **OK**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a8da0-117">См. также</span><span class="sxs-lookup"><span data-stu-id="a8da0-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a8da0-118">Создание нового приложения COM+</span><span class="sxs-lookup"><span data-stu-id="a8da0-118">Creating a New COM+ Application</span></span>](creating-a-new-com--application.md)
</dt> <dt>

[<span data-ttu-id="a8da0-119">Удаление приложения COM+</span><span class="sxs-lookup"><span data-stu-id="a8da0-119">Deleting a COM+ Application</span></span>](deleting-a-com--application.md)
</dt> <dt>

[<span data-ttu-id="a8da0-120">Импорт компонентов</span><span class="sxs-lookup"><span data-stu-id="a8da0-120">Importing Components</span></span>](importing-components.md)
</dt> <dt>

[<span data-ttu-id="a8da0-121">Установка новых компонентов</span><span class="sxs-lookup"><span data-stu-id="a8da0-121">Installing New Components</span></span>](installing-new-components.md)
</dt> <dt>

[<span data-ttu-id="a8da0-122">Перемещение компонентов</span><span class="sxs-lookup"><span data-stu-id="a8da0-122">Moving Components</span></span>](moving-components.md)
</dt> <dt>

[<span data-ttu-id="a8da0-123">Удаление компонента из приложения COM+</span><span class="sxs-lookup"><span data-stu-id="a8da0-123">Removing a Component from a COM+ Application</span></span>](removing-a-component-from-a-com--application.md)
</dt> </dl>

 

 



