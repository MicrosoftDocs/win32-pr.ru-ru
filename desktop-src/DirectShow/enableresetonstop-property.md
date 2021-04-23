---
description: Свойство Енаблересетонстоп задает или получает значение, которое определяет, как будет возобновляться воспроизведение, когда граф фильтра выполняет переход из остановленного состояния.
ms.assetid: ff2e2756-e3f3-4ddb-b99d-5fa65ec67f6b
title: Енаблересетонстоп, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9449d8dd3e2e5ab0e1f008cba3e4cb2aabaa78c8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103806136"
---
# <a name="enableresetonstop-property"></a><span data-ttu-id="abf0a-103">Енаблересетонстоп, свойство</span><span class="sxs-lookup"><span data-stu-id="abf0a-103">EnableResetOnStop Property</span></span>

> [!Note]  
> <span data-ttu-id="abf0a-104">Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="abf0a-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="abf0a-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="abf0a-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="abf0a-106">`EnableResetOnStop`Свойство задает или получает значение, определяющее, как возобновляется воспроизведение, когда граф фильтра выполняет переход из остановленного состояния.</span><span class="sxs-lookup"><span data-stu-id="abf0a-106">The `EnableResetOnStop` property sets or retrieves a value that determines how play will resume when the filter graph makes a transition from a stopped state.</span></span>

``` syntax
[ bEnableReset = ] MSWebDVD.EnableResetOnStop
```

## <a name="return-value"></a><span data-ttu-id="abf0a-107">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="abf0a-107">Return Value</span></span>

<span data-ttu-id="abf0a-108">Возвращает логическое значение, указывающее, где будет начато воспроизведение объекта Мсвебдвд после остановки графа фильтра.</span><span class="sxs-lookup"><span data-stu-id="abf0a-108">Returns a Boolean value indicating where the MSWebDVD object will start playing again after the filter graph is stopped.</span></span>

## <a name="remarks"></a><span data-ttu-id="abf0a-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="abf0a-109">Remarks</span></span>

<span data-ttu-id="abf0a-110">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="abf0a-110">This property is read/write.</span></span>

<span data-ttu-id="abf0a-111">Возможные значения этого свойства: со значением по умолчанию true.</span><span class="sxs-lookup"><span data-stu-id="abf0a-111">The possible values of this property are: with a default value of true.</span></span>



| <span data-ttu-id="abf0a-112">Значение</span><span class="sxs-lookup"><span data-stu-id="abf0a-112">Value</span></span> | <span data-ttu-id="abf0a-113">Описание</span><span class="sxs-lookup"><span data-stu-id="abf0a-113">Description</span></span>                                                                                       |
|-------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="abf0a-114">true</span><span class="sxs-lookup"><span data-stu-id="abf0a-114">true</span></span>  | <span data-ttu-id="abf0a-115">DVD-навигатор будет сброшен и начнет играть с начала диска. Это значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="abf0a-115">DVD Navigator will reset and start play from the beginning of the disc. This is the default value</span></span> |
| <span data-ttu-id="abf0a-116">false</span><span class="sxs-lookup"><span data-stu-id="abf0a-116">false</span></span> | <span data-ttu-id="abf0a-117">Воспроизведение DVD-навигатора продолжится с того места, на котором она была прервана.</span><span class="sxs-lookup"><span data-stu-id="abf0a-117">DVD Navigator will resume play where it left off.</span></span>                                                 |



 

 

 



