---
description: Свойство Субпиктуреон задает или получает текущее состояние подизображения (on или OFF).
ms.assetid: fa4500bc-48b4-41ed-8b88-0011a0e51c6f
title: Субпиктуреон, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83376793f20468bda88edd8897e8c956094c1a88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684395"
---
# <a name="subpictureon-property"></a><span data-ttu-id="60913-103">Субпиктуреон, свойство</span><span class="sxs-lookup"><span data-stu-id="60913-103">SubpictureOn Property</span></span>

> [!Note]  
> <span data-ttu-id="60913-104">Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="60913-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="60913-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="60913-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="60913-106">`SubpictureOn`Свойство задает или получает текущее состояние подизображения (on или OFF).</span><span class="sxs-lookup"><span data-stu-id="60913-106">The `SubpictureOn` property sets or retrieves the current subpicture state (on or off).</span></span>

``` syntax
[ bState = ] MSWebDVD.SubpictureOn
```

## <a name="return-value"></a><span data-ttu-id="60913-107">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="60913-107">Return Value</span></span>

<span data-ttu-id="60913-108">Возвращает логическое значение, указывающее, отображается ли подизображение.</span><span class="sxs-lookup"><span data-stu-id="60913-108">Returns a Boolean value indicating whether the subpicture is displayed.</span></span>

## <a name="remarks"></a><span data-ttu-id="60913-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="60913-109">Remarks</span></span>

<span data-ttu-id="60913-110">Это свойство не влияет на отображение скрытых субтитров.</span><span class="sxs-lookup"><span data-stu-id="60913-110">This property does not affect display of Closed Captions.</span></span> <span data-ttu-id="60913-111">Скрытые субтитры внедряются в поток видео.</span><span class="sxs-lookup"><span data-stu-id="60913-111">Closed Captions are embedded within the video stream.</span></span> <span data-ttu-id="60913-112">Подизображения DVD передаются в отдельном потоке.</span><span class="sxs-lookup"><span data-stu-id="60913-112">DVD subpictures are transported on a separate stream.</span></span>

<span data-ttu-id="60913-113">Когда поток субтитров изменяется с помощью [**куррентсубпиктурестреам**](currentsubpicturestream-property.md), `SubpictureOn` свойство переключается на **true**.</span><span class="sxs-lookup"><span data-stu-id="60913-113">When the subpicture stream is changed using [**CurrentSubpictureStream**](currentsubpicturestream-property.md), the `SubpictureOn` property toggles to **True**.</span></span>

<span data-ttu-id="60913-114">Это свойство доступно для чтения и записи со значением по умолчанию false.</span><span class="sxs-lookup"><span data-stu-id="60913-114">This property is read/write with a default value of false.</span></span>

 

 



