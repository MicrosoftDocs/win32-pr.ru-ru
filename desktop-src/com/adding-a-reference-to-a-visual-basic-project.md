---
title: Добавление ссылки на проект Visual Basic
description: Добавление ссылки на проект Visual Basic
ms.assetid: 635b1fe9-e592-42d7-a0ee-34fea205f412
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b29b99610464287f34e9c78e44319c16b4d47c5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329384"
---
# <a name="adding-a-reference-to-a-visual-basic-project"></a><span data-ttu-id="4b0ea-103">Добавление ссылки на проект Visual Basic</span><span class="sxs-lookup"><span data-stu-id="4b0ea-103">Adding a Reference to a Visual Basic Project</span></span>

<span data-ttu-id="4b0ea-104">В следующей процедуре описывается добавление ссылки на COM-объект в проект Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="4b0ea-104">The following procedure describes how to add a reference to a COM object to a Visual Basic project.</span></span> <span data-ttu-id="4b0ea-105">Приложение может использовать классы этого объекта.</span><span class="sxs-lookup"><span data-stu-id="4b0ea-105">Your application can then use the classes of that object.</span></span>

<span data-ttu-id="4b0ea-106">При добавлении объекта в качестве ссылки можно использовать только библиотеку типов, предоставленную элементом управления, или библиотеку типов "RAW".</span><span class="sxs-lookup"><span data-stu-id="4b0ea-106">When you add an object as a reference, you can only use the type library provided by the control, or the "raw" type library.</span></span> <span data-ttu-id="4b0ea-107">В отличие от этого, Добавление элемента управления в качестве компонента также предоставляет Visual Basic свойства и методы расширения, как если бы они были частью элемента управления.</span><span class="sxs-lookup"><span data-stu-id="4b0ea-107">In contrast, adding a control as a component also exposes the Visual Basic extender properties and methods as if they were part of the control.</span></span>

<span data-ttu-id="4b0ea-108">**Создание Visual Basic ссылки на компонент**</span><span class="sxs-lookup"><span data-stu-id="4b0ea-108">**To make a Visual Basic reference to a component**</span></span>

1.  <span data-ttu-id="4b0ea-109">В меню **Проект** выберите пункт **Ссылки**.</span><span class="sxs-lookup"><span data-stu-id="4b0ea-109">On the **Project** menu, click **References**.</span></span>
2.  <span data-ttu-id="4b0ea-110">Установите флажок рядом с компонентом, который нужно добавить.</span><span class="sxs-lookup"><span data-stu-id="4b0ea-110">Click to select the check box next to the component you want to add.</span></span> <span data-ttu-id="4b0ea-111">Если компонент отсутствует в списке, найдите DLL-или OCX-файл с помощью **кнопки Обзор**.</span><span class="sxs-lookup"><span data-stu-id="4b0ea-111">If the component is not listed, locate the .dll or .ocx file using **Browse**.</span></span>
3.  <span data-ttu-id="4b0ea-112">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="4b0ea-112">Click **OK**.</span></span>

<span data-ttu-id="4b0ea-113">Компонент теперь является частью проекта.</span><span class="sxs-lookup"><span data-stu-id="4b0ea-113">The component is now part of the project.</span></span> <span data-ttu-id="4b0ea-114">Приложение может создавать экземпляры классов с помощью ключевого слова **New** .</span><span class="sxs-lookup"><span data-stu-id="4b0ea-114">Your application can create class instances using the **New** keyword.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4b0ea-115">См. также</span><span class="sxs-lookup"><span data-stu-id="4b0ea-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4b0ea-116">Добавление компонента в проект Visual Basic</span><span class="sxs-lookup"><span data-stu-id="4b0ea-116">Adding a Component to a Visual Basic Project</span></span>](adding-a-component-to-a-visual-basic-project.md)
</dt> <dt>

[<span data-ttu-id="4b0ea-117">Перевод в Visual Basic</span><span class="sxs-lookup"><span data-stu-id="4b0ea-117">Translating to Visual Basic</span></span>](translating-to-visual-basic.md)
</dt> </dl>

 

 




