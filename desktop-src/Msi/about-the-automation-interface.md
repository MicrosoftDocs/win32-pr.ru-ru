---
description: Сначала необходимо создать объект установщика для загрузки поддержки автоматизации, необходимой для доступа к компонентам установщика через COM.
ms.assetid: 113ed443-a866-43d4-86bd-fc3b244f2edb
title: Об интерфейсе автоматизации
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 655a01a4daccb805bec4a858337c1dce48f0fb82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264211"
---
# <a name="about-the-automation-interface"></a><span data-ttu-id="acbc8-103">Об интерфейсе автоматизации</span><span class="sxs-lookup"><span data-stu-id="acbc8-103">About the Automation Interface</span></span>

<span data-ttu-id="acbc8-104">Сначала необходимо создать [**объект установщика**](installer-object.md) для загрузки поддержки автоматизации, необходимой для доступа к компонентам УСТАНОВЩИКА через COM.</span><span class="sxs-lookup"><span data-stu-id="acbc8-104">An [**Installer object**](installer-object.md) must be created initially to load the automation support required to access the installer components through COM.</span></span> <span data-ttu-id="acbc8-105">Этот объект предоставляет оболочки для создания объектов верхнего уровня и доступа к их методам.</span><span class="sxs-lookup"><span data-stu-id="acbc8-105">This object provides wrappers to create the top-level objects and access their methods.</span></span> <span data-ttu-id="acbc8-106">Эти оболочки просто предоставляют переводы параметров для предоставления функций установщика способом, согласованным с Microsoft Visual Basic без изменения поведения методов.</span><span class="sxs-lookup"><span data-stu-id="acbc8-106">These wrappers simply provide parameter translations to expose the installer functions in a manner consistent with Microsoft Visual Basic without changing the behavior of the methods.</span></span>

<span data-ttu-id="acbc8-107">Везде, где это возможно, пара методов Get и Set в C++ предоставляется Visual Basic как одно свойство.</span><span class="sxs-lookup"><span data-stu-id="acbc8-107">Whenever possible, a pair of Get and Set C++ methods are exposed to Visual Basic as a single property.</span></span> <span data-ttu-id="acbc8-108">В некоторых случаях методы C++, принимающие аргумент индекса, предоставляются как индексированное свойство.</span><span class="sxs-lookup"><span data-stu-id="acbc8-108">In some cases C++ methods taking an index argument are exposed as an indexed property.</span></span> <span data-ttu-id="acbc8-109">Многие методы C++ возвращают результат через параметр, так как возвращаемое значение используется для возврата ошибки.</span><span class="sxs-lookup"><span data-stu-id="acbc8-109">Many C++ methods return the result through a parameter because the return value is used for the error return.</span></span> <span data-ttu-id="acbc8-110">Однако в Visual Basic ошибки обрабатываются отдельным механизмом, и результат всегда передается в возвращаемое значение.</span><span class="sxs-lookup"><span data-stu-id="acbc8-110">However, in Visual Basic, errors are handled by a separate mechanism, and the result is always passed in the return value.</span></span>

<span data-ttu-id="acbc8-111">Сведения об использовании автоматизации и создании объекта установщика см. в разделе [Использование интерфейса автоматизации](using-the-automation-interface.md).</span><span class="sxs-lookup"><span data-stu-id="acbc8-111">For information about using automation and creating the Installer object, see [Using the Automation Interface](using-the-automation-interface.md).</span></span>

<span data-ttu-id="acbc8-112">Справочный материал по объектам установщик Windows см. в [справочнике по интерфейсу автоматизации](automation-interface-reference.md).</span><span class="sxs-lookup"><span data-stu-id="acbc8-112">For reference material for the Windows Installer objects, see [Automation Interface Reference](automation-interface-reference.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="acbc8-113">См. также</span><span class="sxs-lookup"><span data-stu-id="acbc8-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="acbc8-114">Примеры сценариев установщик Windows</span><span class="sxs-lookup"><span data-stu-id="acbc8-114">Windows Installer Scripting Examples</span></span>](windows-installer-scripting-examples.md)
</dt> </dl>

 

 



