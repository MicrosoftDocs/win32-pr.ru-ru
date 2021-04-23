---
description: Свойство Фуллскринмоде задает или получает значение, указывающее, находится ли дисплей в полноэкранном режиме.
ms.assetid: e4682f50-080c-4f38-b2ca-ce4ca6b746d7
title: Фуллскринмоде, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a96b3c0ca8261eb934e95eb7235b51e76e8c7579
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104139355"
---
# <a name="fullscreenmode-property"></a><span data-ttu-id="42ae9-103">Фуллскринмоде, свойство</span><span class="sxs-lookup"><span data-stu-id="42ae9-103">FullScreenMode Property</span></span>

> [!Note]  
> <span data-ttu-id="42ae9-104">Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="42ae9-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="42ae9-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="42ae9-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="42ae9-106">`FullScreenMode`Свойство задает или получает значение, указывающее, находится ли дисплей в полноэкранном режиме.</span><span class="sxs-lookup"><span data-stu-id="42ae9-106">The `FullScreenMode` property sets or retrieves a value indicating whether the display is in full-screen mode.</span></span>

``` syntax
[ bFullScreen = ] MSWebDVD.FullScreenMode
```

## <a name="return-value"></a><span data-ttu-id="42ae9-107">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="42ae9-107">Return Value</span></span>

<span data-ttu-id="42ae9-108">Возвращает логическое значение, указывающее, следует ли включать или отключать полноэкранное воспроизведение.</span><span class="sxs-lookup"><span data-stu-id="42ae9-108">Returns a Boolean value indicating whether to enable or disable full-screen playback.</span></span>

## <a name="remarks"></a><span data-ttu-id="42ae9-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="42ae9-109">Remarks</span></span>

<span data-ttu-id="42ae9-110">Это свойство доступно для чтения и записи со значением по умолчанию false.</span><span class="sxs-lookup"><span data-stu-id="42ae9-110">This property is read/write with a default value of false.</span></span>



| <span data-ttu-id="42ae9-111">Значение</span><span class="sxs-lookup"><span data-stu-id="42ae9-111">Value</span></span> | <span data-ttu-id="42ae9-112">Описание</span><span class="sxs-lookup"><span data-stu-id="42ae9-112">Description</span></span>                                            |
|-------|--------------------------------------------------------|
| <span data-ttu-id="42ae9-113">true</span><span class="sxs-lookup"><span data-stu-id="42ae9-113">true</span></span>  | <span data-ttu-id="42ae9-114">Включить воспроизведение в полноэкранном режиме.</span><span class="sxs-lookup"><span data-stu-id="42ae9-114">Enable full-screen playback.</span></span> <span data-ttu-id="42ae9-115">Это значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="42ae9-115">This is the default value</span></span> |
| <span data-ttu-id="42ae9-116">false</span><span class="sxs-lookup"><span data-stu-id="42ae9-116">false</span></span> | <span data-ttu-id="42ae9-117">Отключить воспроизведение в полноэкранном режиме.</span><span class="sxs-lookup"><span data-stu-id="42ae9-117">Disable full-screen playback.</span></span>                          |



 

<span data-ttu-id="42ae9-118">Полноэкранный режим доступен, только если элемент управления Мсвебдвд работает в оконном режиме.</span><span class="sxs-lookup"><span data-stu-id="42ae9-118">Full screen mode is only available when the MSWebDVD control is running in windowed mode.</span></span>

 

 



