---
title: Связывание значков с категорией
description: Связывание значков с категорией
ms.assetid: 5e5c3c10-07cf-4a34-9822-97ec940b3117
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98c7a662ab3aaf578f037ff246207d03e4fcd688
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067501"
---
# <a name="associating-icons-with-a-category"></a><span data-ttu-id="89371-103">Связывание значков с категорией</span><span class="sxs-lookup"><span data-stu-id="89371-103">Associating Icons with a Category</span></span>

<span data-ttu-id="89371-104">Создание пользовательского интерфейса, позволяющего пользователю выбирать категории компонентов в категории, требует возможность отображать осмысленное изображение для определенной категории.</span><span class="sxs-lookup"><span data-stu-id="89371-104">Building a user interface that allows the user to select component categories within a category requires the ability to display a meaningful image for a particular category.</span></span> <span data-ttu-id="89371-105">Чтобы связать значок с категорией компонента, создайте ключ для идентификатора CATID категории и заполните этот ключ подразделом [дефаултикон](defaulticon.md) .</span><span class="sxs-lookup"><span data-stu-id="89371-105">To associate an icon with a component category, create a key for the category's CATID and populate that key with a [DefaultIcon](defaulticon.md) subkey.</span></span> <span data-ttu-id="89371-106">Запись реестра выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="89371-106">The registry entry is as follows:</span></span>

``` syntax
HKEY_CLASSES_ROOT\CLSID\{...catid...}\DefaultIcon = "c:\hello\icons.dll,1"
 
```

<span data-ttu-id="89371-107">Имя файла, на которое ссылается ключ Дефаултикон, может быть файлом EXE или DLL (библиотека DLL только для ресурсов).</span><span class="sxs-lookup"><span data-stu-id="89371-107">The filename referenced by the DefaultIcon key can be either an EXE or a DLL file (resource-only DLL).</span></span>

<span data-ttu-id="89371-108">Чтобы связать маленький значок панели элементов с категорией компонента, создайте ключ в **\_ \_ корневом \\ идентификаторе CLSID классов hKey** для идентификатора CATID категории и заполните этот ключ подключом [ToolBoxBitmap32](toolboxbitmap32.md) , как показано в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="89371-108">To associate a small 16x16 "toolbox bitmap" with a component category, create a key in **HKEY\_CLASSES\_ROOT\\CLSID** for the category's CATID and populate that key with a [ToolBoxBitmap32](toolboxbitmap32.md) subkey, as shown in the following example:</span></span>

``` syntax
HKEY_CLASSES_ROOT\CLSID\{...catid...}\ToolBoxBitmap32 = "c:\goodbye\mycomponent.dll,42"
 
```

<span data-ttu-id="89371-109">Имя файла, на которое ссылается ключ [ToolBoxBitmap32](toolboxbitmap32.md) , также может быть файлом EXE или DLL (библиотека DLL только для ресурсов).</span><span class="sxs-lookup"><span data-stu-id="89371-109">The filename referenced by the [ToolBoxBitmap32](toolboxbitmap32.md) key can also be an EXE or DLL file (resource-only DLL).</span></span>

## <a name="related-topics"></a><span data-ttu-id="89371-110">См. также</span><span class="sxs-lookup"><span data-stu-id="89371-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="89371-111">Категоризация по возможностям компонентов</span><span class="sxs-lookup"><span data-stu-id="89371-111">Categorizing by Component Capabilities</span></span>](categorizing-by-component-capabilities.md)
</dt> <dt>

[<span data-ttu-id="89371-112">Категоризация по возможностям контейнеров</span><span class="sxs-lookup"><span data-stu-id="89371-112">Categorizing by Container Capabilities</span></span>](categorizing-by-container-capabilities.md)
</dt> <dt>

[<span data-ttu-id="89371-113">Классы и ассоциации по умолчанию</span><span class="sxs-lookup"><span data-stu-id="89371-113">Default Classes and Associations</span></span>](default-classes-and-associations.md)
</dt> <dt>

[<span data-ttu-id="89371-114">Определение категорий компонентов</span><span class="sxs-lookup"><span data-stu-id="89371-114">Defining Component Categories</span></span>](defining-component-categories.md)
</dt> <dt>

[<span data-ttu-id="89371-115">**икатинформатион**</span><span class="sxs-lookup"><span data-stu-id="89371-115">**ICatInformation**</span></span>](/windows/desktop/api/ComCat/nn-comcat-icatinformation)
</dt> <dt>

[<span data-ttu-id="89371-116">**икатрегистер**</span><span class="sxs-lookup"><span data-stu-id="89371-116">**ICatRegister**</span></span>](/windows/desktop/api/ComCat/nn-comcat-icatregister)
</dt> <dt>

[<span data-ttu-id="89371-117">Диспетчер категорий компонентов</span><span class="sxs-lookup"><span data-stu-id="89371-117">The Component Categories Manager</span></span>](the-component-categories-manager.md)
</dt> </dl>

 

 




