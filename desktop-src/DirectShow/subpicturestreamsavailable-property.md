---
description: Свойство Субпиктурестреамсаваилабле извлекает количество потоков субтитров, доступных в текущем заголовке.
ms.assetid: 6a6d9d15-2f56-47fc-a7bb-2cf33f384f41
title: Субпиктурестреамсаваилабле, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e34f780a726966580a72d87b6f7900bb73c1a85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684394"
---
# <a name="subpicturestreamsavailable-property"></a><span data-ttu-id="bb928-103">Субпиктурестреамсаваилабле, свойство</span><span class="sxs-lookup"><span data-stu-id="bb928-103">SubpictureStreamsAvailable Property</span></span>

> [!Note]  
> <span data-ttu-id="bb928-104">Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="bb928-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="bb928-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="bb928-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="bb928-106">`SubpictureStreamsAvailable`Свойство получает количество потоков субтитров, доступных в текущем заголовке.</span><span class="sxs-lookup"><span data-stu-id="bb928-106">The `SubpictureStreamsAvailable` property retrieves the number of subpicture streams available in the current title.</span></span>

``` syntax
[ iStreams = ] MSWebDVD.SubpictureStreamsAvailable
```

## <a name="return-value"></a><span data-ttu-id="bb928-107">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bb928-107">Return Value</span></span>

<span data-ttu-id="bb928-108">Возвращает количество доступных потоков в виде целого числа.</span><span class="sxs-lookup"><span data-stu-id="bb928-108">Returns the number of available streams as an Integer.</span></span>

## <a name="remarks"></a><span data-ttu-id="bb928-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bb928-109">Remarks</span></span>

<span data-ttu-id="bb928-110">Это свойство доступно только для чтения и не имеет значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="bb928-110">This property is read-only with no default value.</span></span> <span data-ttu-id="bb928-111">Чтобы запросить каждый поток для своего атрибута языка, сначала вызовите этот метод, чтобы получить верхнюю границу.</span><span class="sxs-lookup"><span data-stu-id="bb928-111">To query each stream for its language attribute, first call this method to get the upper bound.</span></span>

<span data-ttu-id="bb928-112">Нумерация потоков отсчитывается от нуля.</span><span class="sxs-lookup"><span data-stu-id="bb928-112">Stream numbering is zero-based.</span></span>

 

 



