---
description: Свойство примеры CursorType задает или получает текущий тип курсора.
ms.assetid: f362e790-a7c7-4fb6-86f3-7cd25f78fe0e
title: Примеры CursorType, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c17ae74c471bebe6da2bcef4d22d7c247f4eda1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103894709"
---
# <a name="cursortype-property"></a><span data-ttu-id="2445b-103">Примеры CursorType, свойство</span><span class="sxs-lookup"><span data-stu-id="2445b-103">CursorType Property</span></span>

> [!Note]  
> <span data-ttu-id="2445b-104">Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="2445b-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="2445b-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="2445b-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="2445b-106">`CursorType`Свойство задает или получает текущий тип курсора.</span><span class="sxs-lookup"><span data-stu-id="2445b-106">The `CursorType` property sets or retrieves the current cursor type.</span></span>

``` syntax
[ iCursorType = ] MSWebDVD.CursorType
```

## <a name="return-value"></a><span data-ttu-id="2445b-107">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2445b-107">Return Value</span></span>

<span data-ttu-id="2445b-108">Возвращает целочисленное значение, представляющее тип курсора.</span><span class="sxs-lookup"><span data-stu-id="2445b-108">Returns an integer value representing the cursor type.</span></span>

## <a name="remarks"></a><span data-ttu-id="2445b-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2445b-109">Remarks</span></span>

<span data-ttu-id="2445b-110">Возможные значения этого свойства:</span><span class="sxs-lookup"><span data-stu-id="2445b-110">The possible values for this property are:</span></span>



| <span data-ttu-id="2445b-111">Значение</span><span class="sxs-lookup"><span data-stu-id="2445b-111">Value</span></span> | <span data-ttu-id="2445b-112">Описание</span><span class="sxs-lookup"><span data-stu-id="2445b-112">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="2445b-113">0</span><span class="sxs-lookup"><span data-stu-id="2445b-113">0</span></span>     | <span data-ttu-id="2445b-114">Стрелка</span><span class="sxs-lookup"><span data-stu-id="2445b-114">Arrow</span></span>       |
| <span data-ttu-id="2445b-115">1</span><span class="sxs-lookup"><span data-stu-id="2445b-115">1</span></span>     | <span data-ttu-id="2445b-116">Увеличить</span><span class="sxs-lookup"><span data-stu-id="2445b-116">Zoom In</span></span>     |
| <span data-ttu-id="2445b-117">2</span><span class="sxs-lookup"><span data-stu-id="2445b-117">2</span></span>     | <span data-ttu-id="2445b-118">Уменьшить</span><span class="sxs-lookup"><span data-stu-id="2445b-118">Zoom Out</span></span>    |
| <span data-ttu-id="2445b-119">3</span><span class="sxs-lookup"><span data-stu-id="2445b-119">3</span></span>     | <span data-ttu-id="2445b-120">Правый</span><span class="sxs-lookup"><span data-stu-id="2445b-120">Hand</span></span>        |
| <span data-ttu-id="2445b-121">-1</span><span class="sxs-lookup"><span data-stu-id="2445b-121">-1</span></span>    | <span data-ttu-id="2445b-122">Нет</span><span class="sxs-lookup"><span data-stu-id="2445b-122">None</span></span>        |



 

<span data-ttu-id="2445b-123">Это свойство доступно для чтения и записи и имеет нулевое значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2445b-123">This property is read/write with a default value of zero.</span></span> <span data-ttu-id="2445b-124">Когда изображение масштабируется, параметр `CursorType` " **рука** " (0x3) переводит приложение в режим перетаскивания, позволяя пользователю перемещать изображение в область экрана.</span><span class="sxs-lookup"><span data-stu-id="2445b-124">When the picture is zoomed in, setting `CursorType` to **Hand** (0x3) puts the application into drag mode, enabling the user to move the image inside the video display area.</span></span>

 

 



