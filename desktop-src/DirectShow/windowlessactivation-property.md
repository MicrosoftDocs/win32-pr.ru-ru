---
description: Свойство Виндовлессактиватион Инициализирует объект Мсвебдвд во время разработки для режима с оконным или безоконным режимом.
ms.assetid: 290a9459-154a-4ec7-a013-d696e6b27341
title: Виндовлессактиватион, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 427fdcb265d60200bfe8716cd1ece384861fbdf7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684391"
---
# <a name="windowlessactivation-property"></a><span data-ttu-id="02cd8-103">Виндовлессактиватион, свойство</span><span class="sxs-lookup"><span data-stu-id="02cd8-103">WindowlessActivation Property</span></span>

> [!Note]  
> <span data-ttu-id="02cd8-104">Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="02cd8-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="02cd8-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="02cd8-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="02cd8-106">`WindowlessActivation`Свойство Инициализирует объект **мсвебдвд** во время разработки для оконного или безоконного режима.</span><span class="sxs-lookup"><span data-stu-id="02cd8-106">The `WindowlessActivation` property initializes the **MSWebDVD** object at design time for either windowed or windowless mode.</span></span>

``` syntax
[ bWindowless = ] MSWebDVD.WindowlessActivation
```

## <a name="return-value"></a><span data-ttu-id="02cd8-107">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="02cd8-107">Return Value</span></span>

<span data-ttu-id="02cd8-108">Возвращает значение, указывающее, находится ли объект в оконном режиме в виде логического значения.</span><span class="sxs-lookup"><span data-stu-id="02cd8-108">Returns whether the object is in windowed mode as a Boolean.</span></span>

## <a name="remarks"></a><span data-ttu-id="02cd8-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="02cd8-109">Remarks</span></span>

<span data-ttu-id="02cd8-110">Это свойство доступно для чтения и записи со значением по умолчанию true.</span><span class="sxs-lookup"><span data-stu-id="02cd8-110">This property is read/write with a default value of true.</span></span> <span data-ttu-id="02cd8-111">Поэтому это свойство необходимо задавать, только если объект **мсвебдвд** выполняется в оконном контейнере.</span><span class="sxs-lookup"><span data-stu-id="02cd8-111">Therefore, you only need to set this property if you are running the **MSWebDVD** object in a windowed container.</span></span> <span data-ttu-id="02cd8-112">При его наличии на веб-странице в Microsoft® Internet Explorer, **мсвебдвд** всегда находится в режиме без окон, и вам не нужно задавать это свойство.</span><span class="sxs-lookup"><span data-stu-id="02cd8-112">When contained in a Web page in Microsoft® Internet Explorer, **MSWebDVD** is always in windowless mode, and you don't need to set this property.</span></span>

 

 



