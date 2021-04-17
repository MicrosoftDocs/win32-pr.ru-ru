---
description: Свойство CurrentDomain извлекает DVD-домен, в котором находится объект Мсвебдвд.
ms.assetid: 9d545438-9a3d-4c57-a3df-5e75af2e4d1b
title: CurrentDomain, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ead6d61cd622fceac2a4d133a0297892992e763a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104495150"
---
# <a name="currentdomain-property"></a><span data-ttu-id="6818c-103">CurrentDomain, свойство</span><span class="sxs-lookup"><span data-stu-id="6818c-103">CurrentDomain Property</span></span>

> [!Note]  
> <span data-ttu-id="6818c-104">Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="6818c-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="6818c-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="6818c-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="6818c-106">`CurrentDomain`Свойство получает DVD-домен, в котором находится объект мсвебдвд.</span><span class="sxs-lookup"><span data-stu-id="6818c-106">The `CurrentDomain` property retrieves the DVD domain that the MSWebDVD object is in.</span></span>

``` syntax
[ iDomain = ] MSWebDVD.CurrentDomain
```

## <a name="return-value"></a><span data-ttu-id="6818c-107">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6818c-107">Return Value</span></span>

<span data-ttu-id="6818c-108">Возвращает целочисленное значение, представляющее текущий домен.</span><span class="sxs-lookup"><span data-stu-id="6818c-108">Returns an integer value representing the current domain.</span></span>

## <a name="remarks"></a><span data-ttu-id="6818c-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6818c-109">Remarks</span></span>

<span data-ttu-id="6818c-110">Возможные значения свойства:</span><span class="sxs-lookup"><span data-stu-id="6818c-110">The possible values of the property are:</span></span>



| <span data-ttu-id="6818c-111">Значение</span><span class="sxs-lookup"><span data-stu-id="6818c-111">Value</span></span> | <span data-ttu-id="6818c-112">Описание</span><span class="sxs-lookup"><span data-stu-id="6818c-112">Description</span></span>          |
|-------|----------------------|
| <span data-ttu-id="6818c-113">1</span><span class="sxs-lookup"><span data-stu-id="6818c-113">1</span></span>     | <span data-ttu-id="6818c-114">Первое воспроизведение</span><span class="sxs-lookup"><span data-stu-id="6818c-114">First play</span></span>           |
| <span data-ttu-id="6818c-115">2</span><span class="sxs-lookup"><span data-stu-id="6818c-115">2</span></span>     | <span data-ttu-id="6818c-116">Меню менеджера видео</span><span class="sxs-lookup"><span data-stu-id="6818c-116">Video Manager Menu</span></span>   |
| <span data-ttu-id="6818c-117">3</span><span class="sxs-lookup"><span data-stu-id="6818c-117">3</span></span>     | <span data-ttu-id="6818c-118">Меню набора заголовков видео</span><span class="sxs-lookup"><span data-stu-id="6818c-118">Video Title Set Menu</span></span> |
| <span data-ttu-id="6818c-119">4</span><span class="sxs-lookup"><span data-stu-id="6818c-119">4</span></span>     | <span data-ttu-id="6818c-120">Заголовок</span><span class="sxs-lookup"><span data-stu-id="6818c-120">Title</span></span>                |
| <span data-ttu-id="6818c-121">5</span><span class="sxs-lookup"><span data-stu-id="6818c-121">5</span></span>     | <span data-ttu-id="6818c-122">Stop</span><span class="sxs-lookup"><span data-stu-id="6818c-122">Stop</span></span>                 |



 

<span data-ttu-id="6818c-123">Вызовите этот метод, чтобы убедиться, что Навигатор DVD находится в допустимом домене для метода, который вы собираетесь вызвать.</span><span class="sxs-lookup"><span data-stu-id="6818c-123">Call this method to ensure that the DVD Navigator is in a valid domain for the method you are about to call.</span></span> <span data-ttu-id="6818c-124">Например, перед вызовом [**плайтитле**](playtitle-method.md)проверьте свойство, `CurrentDomain` чтобы убедиться, что Навигатор DVD не находится в домене с остановкой или первым воспроизведением.</span><span class="sxs-lookup"><span data-stu-id="6818c-124">For example, before calling [**PlayTitle**](playtitle-method.md), check the `CurrentDomain` property to make sure that the DVD Navigator is not in the Stop or First Play domain.</span></span>

 

 



