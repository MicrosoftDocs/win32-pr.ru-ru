---
description: 'Другим вариантом добавления команд в каскадное меню является Иексплореркомманд:: Енумсубкоммандс.'
ms.assetid: 010157F3-B950-4A57-B0AA-248B4990DA34
title: Создание каскадных меню с помощью интерфейса Иексплореркомманд
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5afb88a7ac04857ac64e79115a4e8984d325e47b
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/28/2021
ms.locfileid: "104559954"
---
# <a name="how-to-create-cascading-menus-with-the-iexplorercommand-interface"></a><span data-ttu-id="4092b-103">Создание каскадных меню с помощью интерфейса Иексплореркомманд</span><span class="sxs-lookup"><span data-stu-id="4092b-103">How to Create Cascading Menus with the IExplorerCommand Interface</span></span>

<span data-ttu-id="4092b-104">Другим вариантом добавления команд в каскадное меню является [**иексплореркомманд:: енумсубкоммандс**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-enumsubcommands).</span><span class="sxs-lookup"><span data-stu-id="4092b-104">Another option for adding verbs to a cascading menu is through [**IExplorerCommand::EnumSubCommands**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-enumsubcommands).</span></span> <span data-ttu-id="4092b-105">Этот метод позволяет источникам данных, которые предоставляют команды командного модуля через интерфейс [**иексплореркоммандпровидер**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider) , использовать эти команды в качестве команд в контекстном меню.</span><span class="sxs-lookup"><span data-stu-id="4092b-105">This method enables data sources that provide their command module commands through the [**IExplorerCommandProvider**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider) interface to use those commands as verbs on a shortcut menu.</span></span> <span data-ttu-id="4092b-106">В Windows 7 и более поздних версиях вы можете предоставить ту же реализацию команды с помощью интерфейса [**иексплореркомманд**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) , как и с помощью интерфейса [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) .</span><span class="sxs-lookup"><span data-stu-id="4092b-106">In Windows 7 and later, you can provide the same verb implementation using the [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) interface as you can with the [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) interface.</span></span>

## <a name="instructions"></a><span data-ttu-id="4092b-107">Инструкции</span><span class="sxs-lookup"><span data-stu-id="4092b-107">Instructions</span></span>


<span data-ttu-id="4092b-108">Следующие два снимка экрана иллюстрируют использование каскадных меню в папке **Devices** .</span><span class="sxs-lookup"><span data-stu-id="4092b-108">The following two screen shots illustrate the use of cascading menus in the **Devices** folder.</span></span>

![Снимок экрана, на котором показан пример каскадного меню в папке Devices.](images/file-assoc/filecascademenu.png)

![снимок экрана, показывающий пример каскадного меню в папке "устройства"](images/file-assoc/cascadedevices2.png)

## <a name="remarks"></a><span data-ttu-id="4092b-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="4092b-111">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="4092b-112">Так как [**иексплореркомманд**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) поддерживает только внутрипроцессный активацию, рекомендуется использовать их в качестве источников данных оболочки, которые должны совместно использовать реализацию команд и контекстных меню.</span><span class="sxs-lookup"><span data-stu-id="4092b-112">Because [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) supports in-process activation only, it is recommended for use by Shell data sources that need to share the implementation between commands and shortcut menus.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="4092b-113">См. также</span><span class="sxs-lookup"><span data-stu-id="4092b-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4092b-114">**иексплореркомманд**</span><span class="sxs-lookup"><span data-stu-id="4092b-114">**IExplorerCommand**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand)
</dt> <dt>

[<span data-ttu-id="4092b-115">**иексплореркоммандпровидер**</span><span class="sxs-lookup"><span data-stu-id="4092b-115">**IExplorerCommandProvider**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider)
</dt> <dt>

[<span data-ttu-id="4092b-116">**IContextMenu**</span><span class="sxs-lookup"><span data-stu-id="4092b-116">**IContextMenu**</span></span>](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu)
</dt> </dl>

 

 
