---
description: Метод Сетделайтиме задает время задержки для подсказки, связанной с объектом Мсвебдвд.
ms.assetid: bb1086e1-57e2-495a-9b7b-2d349a516e72
title: сетделайтиме
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c7653777be7e6603494d9ba04a671ed46d3d949
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104494193"
---
# <a name="setdelaytime"></a><span data-ttu-id="f4a1c-103">сетделайтиме</span><span class="sxs-lookup"><span data-stu-id="f4a1c-103">SetDelayTime</span></span>

> [!Note]  
> <span data-ttu-id="f4a1c-104">Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="f4a1c-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="f4a1c-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="f4a1c-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="f4a1c-106">`SetDelayTime`Метод задает время задержки для подсказки, связанной с объектом **мсвебдвд** .</span><span class="sxs-lookup"><span data-stu-id="f4a1c-106">The `SetDelayTime` method sets the delay time for the ToolTip associated with the **MSWebDVD** object.</span></span>

``` syntax
MSWebDVD.SetDelayTime(iDelayType, iNewVal)
```

## <a name="parameters"></a><span data-ttu-id="f4a1c-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="f4a1c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f4a1c-108"><span id="iDelayType"></span><span id="idelaytype"></span><span id="IDELAYTYPE"></span>*иделайтипе*</span><span class="sxs-lookup"><span data-stu-id="f4a1c-108"><span id="iDelayType"></span><span id="idelaytype"></span><span id="IDELAYTYPE"></span>*iDelayType*</span></span>
</dt> <dd>

<span data-ttu-id="f4a1c-109">Указывает тип задержки в виде целого числа.</span><span class="sxs-lookup"><span data-stu-id="f4a1c-109">Specifies the type of delay as an Integer.</span></span>



| <span data-ttu-id="f4a1c-110">Значение</span><span class="sxs-lookup"><span data-stu-id="f4a1c-110">Value</span></span> | <span data-ttu-id="f4a1c-111">Описание</span><span class="sxs-lookup"><span data-stu-id="f4a1c-111">Description</span></span>                                                                                                                                                                                                                                      |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4a1c-112">-1</span><span class="sxs-lookup"><span data-stu-id="f4a1c-112">-1</span></span>    | <span data-ttu-id="f4a1c-113">Чтобы сбросить время задержки аутопоп до значения по умолчанию, установите *иневвал* в значение-1.</span><span class="sxs-lookup"><span data-stu-id="f4a1c-113">To reset the autopop delay time to its default value, set *iNewVal* to -1.</span></span>                                                                                                                                                                       |
| <span data-ttu-id="f4a1c-114">0</span><span class="sxs-lookup"><span data-stu-id="f4a1c-114">0</span></span>     | <span data-ttu-id="f4a1c-115">Задайте время, в течение которого окно подсказки остается видимым, если указатель мыши находится в ограничивающем прямоугольнике инструмента.</span><span class="sxs-lookup"><span data-stu-id="f4a1c-115">Set the length of time a ToolTip window remains visible if the pointer is stationary within a tool's bounding rectangle.</span></span>                                                                                                                         |
| <span data-ttu-id="f4a1c-116">1</span><span class="sxs-lookup"><span data-stu-id="f4a1c-116">1</span></span>     | <span data-ttu-id="f4a1c-117">Задайте период времени, в течение которого указатель должен оставаться свободным внутри ограничивающего прямоугольника инструмента перед отображением окна подсказки.</span><span class="sxs-lookup"><span data-stu-id="f4a1c-117">Set the length of time a pointer must remain stationary within a tool's bounding rectangle before the ToolTip window appears.</span></span>                                                                                                                    |
| <span data-ttu-id="f4a1c-118">2</span><span class="sxs-lookup"><span data-stu-id="f4a1c-118">2</span></span>     | <span data-ttu-id="f4a1c-119">Задайте время, необходимое для отображения последующих окон всплывающей подсказки при переходе указателя с одного инструмента на другое.</span><span class="sxs-lookup"><span data-stu-id="f4a1c-119">Set the length of time it takes for subsequent ToolTip windows to appear as the pointer moves from one tool to another.</span></span>                                                                                                                          |
| <span data-ttu-id="f4a1c-120">3</span><span class="sxs-lookup"><span data-stu-id="f4a1c-120">3</span></span>     | <span data-ttu-id="f4a1c-121">Установите все времена задержки в пропорции по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f4a1c-121">Set all delay times to default proportions.</span></span> <span data-ttu-id="f4a1c-122">Аутопоп время в десять раз больше начального времени, а время перепоказа — одно-пятое начальное время.</span><span class="sxs-lookup"><span data-stu-id="f4a1c-122">The autopop time is ten times the initial time and the reshow time is one-fifth the initial time.</span></span> <span data-ttu-id="f4a1c-123">Если этот флаг установлен, используйте положительное значение Иневвал, чтобы указать начальное время в миллисекундах.</span><span class="sxs-lookup"><span data-stu-id="f4a1c-123">If this flag is set, use a positive value of iNewVal to specify the initial time, in milliseconds.</span></span> |



 

</dd> <dt>

<span data-ttu-id="f4a1c-124"><span id="iNewVal"></span><span id="inewval"></span><span id="INEWVAL"></span>*иневвал*</span><span class="sxs-lookup"><span data-stu-id="f4a1c-124"><span id="iNewVal"></span><span id="inewval"></span><span id="INEWVAL"></span>*iNewVal*</span></span>
</dt> <dd>

<span data-ttu-id="f4a1c-125">Указывает задержку в миллисекундах в виде целого числа.</span><span class="sxs-lookup"><span data-stu-id="f4a1c-125">Specifies the delay, in milliseconds, as an Integer.</span></span>



| <span data-ttu-id="f4a1c-126">Значение</span><span class="sxs-lookup"><span data-stu-id="f4a1c-126">Value</span></span>                    | <span data-ttu-id="f4a1c-127">Описание</span><span class="sxs-lookup"><span data-stu-id="f4a1c-127">Description</span></span>                                                   |
|--------------------------|---------------------------------------------------------------|
| <span data-ttu-id="f4a1c-128">-1</span><span class="sxs-lookup"><span data-stu-id="f4a1c-128">-1</span></span>                       | <span data-ttu-id="f4a1c-129">Устанавливает для задержки, указанной в *иделайтипе* , значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="f4a1c-129">Sets the delay specified in *iDelayType* to its default value</span></span> |
| <span data-ttu-id="f4a1c-130">любое другое отрицательное значение</span><span class="sxs-lookup"><span data-stu-id="f4a1c-130">any other negative value</span></span> | <span data-ttu-id="f4a1c-131">Задает для всех типов задержки значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f4a1c-131">Sets all delay types to their default value.</span></span>                  |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f4a1c-132">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f4a1c-132">Return Value</span></span>

<span data-ttu-id="f4a1c-133">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="f4a1c-133">No return value.</span></span>

 

 



