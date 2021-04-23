---
description: Свойство Плайстате извлекает текущее состояние объекта Мсвебдвд.
ms.assetid: ffe71c3f-f8c2-45cc-84bf-e937cfbbe7b9
title: Плайстате, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d8c699ce3f232f9afc14472f0308fa65adc6abb
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105682244"
---
# <a name="playstate-property"></a><span data-ttu-id="0bc5b-103">Плайстате, свойство</span><span class="sxs-lookup"><span data-stu-id="0bc5b-103">PlayState Property</span></span>

> [!Note]  
> <span data-ttu-id="0bc5b-104">Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="0bc5b-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="0bc5b-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="0bc5b-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="0bc5b-106">`PlayState`Свойство получает текущее состояние объекта **мсвебдвд** .</span><span class="sxs-lookup"><span data-stu-id="0bc5b-106">The `PlayState` property retrieves the current state of the **MSWebDVD** object.</span></span>

``` syntax
[ iState = ] MSWebDVD.PlayState
```

## <a name="return-value"></a><span data-ttu-id="0bc5b-107">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0bc5b-107">Return Value</span></span>

<span data-ttu-id="0bc5b-108">Возвращает целочисленное значение, представляющее текущее состояние навигатора DVD.</span><span class="sxs-lookup"><span data-stu-id="0bc5b-108">Returns an Integer value representing the current state of the DVD Navigator.</span></span>



| <span data-ttu-id="0bc5b-109">Код возврата</span><span class="sxs-lookup"><span data-stu-id="0bc5b-109">Return code</span></span> | <span data-ttu-id="0bc5b-110">Описание</span><span class="sxs-lookup"><span data-stu-id="0bc5b-110">Description</span></span>   |
|-------------|---------------|
| <span data-ttu-id="0bc5b-111">-2</span><span class="sxs-lookup"><span data-stu-id="0bc5b-111">-2</span></span>          | <span data-ttu-id="0bc5b-112">Не определено.</span><span class="sxs-lookup"><span data-stu-id="0bc5b-112">Undefined</span></span>     |
| <span data-ttu-id="0bc5b-113">-1</span><span class="sxs-lookup"><span data-stu-id="0bc5b-113">-1</span></span>          | <span data-ttu-id="0bc5b-114">Не инициализировано</span><span class="sxs-lookup"><span data-stu-id="0bc5b-114">Uninitialized</span></span> |
| <span data-ttu-id="0bc5b-115">0</span><span class="sxs-lookup"><span data-stu-id="0bc5b-115">0</span></span>           | <span data-ttu-id="0bc5b-116">Остановлена</span><span class="sxs-lookup"><span data-stu-id="0bc5b-116">Stopped</span></span>       |
| <span data-ttu-id="0bc5b-117">1</span><span class="sxs-lookup"><span data-stu-id="0bc5b-117">1</span></span>           | <span data-ttu-id="0bc5b-118">Пауза</span><span class="sxs-lookup"><span data-stu-id="0bc5b-118">Paused</span></span>        |
| <span data-ttu-id="0bc5b-119">2</span><span class="sxs-lookup"><span data-stu-id="0bc5b-119">2</span></span>           | <span data-ttu-id="0bc5b-120">Запущен</span><span class="sxs-lookup"><span data-stu-id="0bc5b-120">Running</span></span>       |



 

## <a name="remarks"></a><span data-ttu-id="0bc5b-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0bc5b-121">Remarks</span></span>

<span data-ttu-id="0bc5b-122">Это свойство доступно только для чтения и не имеет значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0bc5b-122">This property is read-only with no default value.</span></span>

<span data-ttu-id="0bc5b-123">Объект **мсвебдвд** управляет фильтром навигатора по DVD-навигатору DirectShow, который выполняет фактическую работу с навигацией по DVD.</span><span class="sxs-lookup"><span data-stu-id="0bc5b-123">The **MSWebDVD** object controls the DirectShow DVD Navigator filter, which does the actual work of DVD navigation.</span></span> <span data-ttu-id="0bc5b-124">На самом деле это состояние DVD-навигатора, на которое ссылается это свойство.</span><span class="sxs-lookup"><span data-stu-id="0bc5b-124">It is actually the state of the DVD Navigator that this property refers to.</span></span> <span data-ttu-id="0bc5b-125">Навигатор DVD может находиться в одном из нескольких состояний, как описано выше.</span><span class="sxs-lookup"><span data-stu-id="0bc5b-125">The DVD Navigator can be in one of several states, as described above.</span></span> <span data-ttu-id="0bc5b-126">`PlayState`Свойство может быть полезно в качестве диагностического средства, но в целом не должно быть причин для отслеживания состояния DVD-навигатора в приложении для работы со сценариями.</span><span class="sxs-lookup"><span data-stu-id="0bc5b-126">The `PlayState` property can be useful as a diagnostic tool, but generally there should be no reason for a scripting application to monitor the state of the DVD Navigator.</span></span>

 

 



