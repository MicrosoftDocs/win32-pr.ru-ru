---
description: Метод Render инициализирует граф фильтра DVD.
ms.assetid: 910f1e3f-b3bb-498b-93da-3a974a3117e8
title: Метод Render
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 677abab1c669642c1e51e0041c98949d923147c7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105672997"
---
# <a name="render-method"></a><span data-ttu-id="67bbf-103">Метод Render</span><span class="sxs-lookup"><span data-stu-id="67bbf-103">Render Method</span></span>

> [!Note]  
> <span data-ttu-id="67bbf-104">Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="67bbf-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="67bbf-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="67bbf-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="67bbf-106">`Render`Метод инициализирует граф фильтра DVD.</span><span class="sxs-lookup"><span data-stu-id="67bbf-106">The `Render` method initializes the DVD filter graph.</span></span>

``` syntax
MSWebDVD.Render(iRender = 0)
```

## <a name="parameters"></a><span data-ttu-id="67bbf-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="67bbf-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67bbf-108"><span id="iRender"></span><span id="irender"></span><span id="IRENDER"></span>*ирендер*</span><span class="sxs-lookup"><span data-stu-id="67bbf-108"><span id="iRender"></span><span id="irender"></span><span id="IRENDER"></span>*iRender*</span></span>
</dt> <dd>

<span data-ttu-id="67bbf-109">Задает целочисленное значение, указывающее, будет ли граф фильтра уничтожен и перестроен.</span><span class="sxs-lookup"><span data-stu-id="67bbf-109">Specifies an integer value indicating whether the filter graph will be destroyed and rebuilt.</span></span>



| <span data-ttu-id="67bbf-110">Значение</span><span class="sxs-lookup"><span data-stu-id="67bbf-110">Value</span></span> | <span data-ttu-id="67bbf-111">Описание</span><span class="sxs-lookup"><span data-stu-id="67bbf-111">Description</span></span>                                                                                         |
|-------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67bbf-112">0</span><span class="sxs-lookup"><span data-stu-id="67bbf-112">0</span></span>     | <span data-ttu-id="67bbf-113">Граф фильтра не будет уничтожен и перестроен, если он уже существует.</span><span class="sxs-lookup"><span data-stu-id="67bbf-113">The filter graph will not be destroyed and rebuilt if it already exists.</span></span> <span data-ttu-id="67bbf-114">Это значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="67bbf-114">This is the default value.</span></span> |
| <span data-ttu-id="67bbf-115">1</span><span class="sxs-lookup"><span data-stu-id="67bbf-115">1</span></span>     | <span data-ttu-id="67bbf-116">Граф фильтра будет уничтожен и перестроен, если он уже существует.</span><span class="sxs-lookup"><span data-stu-id="67bbf-116">The filter graph will be destroyed and rebuilt if it already exists.</span></span>                                |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="67bbf-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="67bbf-117">Return Value</span></span>

<span data-ttu-id="67bbf-118">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="67bbf-118">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="67bbf-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="67bbf-119">Remarks</span></span>

<span data-ttu-id="67bbf-120">`Render`Метод позволяет объекту **мсвебдвд** полностью инициализировать базовый граф фильтра DirectShow при запуске.</span><span class="sxs-lookup"><span data-stu-id="67bbf-120">The `Render` method enables the **MSWebDVD** object to fully initialize the underlying DirectShow filter graph on startup.</span></span> <span data-ttu-id="67bbf-121">Это устраняет незначительную задержку, которая в противном случае возникает, когда пользователь выдает первую команду для воспроизведения диска или вывода меню.</span><span class="sxs-lookup"><span data-stu-id="67bbf-121">This eliminates the slight delay that otherwise occurs when the user issues the first command to play a disc or show a menu.</span></span> <span data-ttu-id="67bbf-122">Не существует случая, в котором необходимо `Render` вызвать метод перед вызовом любого другого метода.</span><span class="sxs-lookup"><span data-stu-id="67bbf-122">There is no case in which `Render` needs to be called before calling any other method.</span></span> <span data-ttu-id="67bbf-123">Например, если приложение вызывает [**плайтитле**](playtitle-method.md) до инициализации графа фильтра, объект **мсвебдвд** автоматически вызывается `Render` перед попыткой воспроизведения диска.</span><span class="sxs-lookup"><span data-stu-id="67bbf-123">For example, if the application calls [**PlayTitle**](playtitle-method.md) before the filter graph has been initialized, the **MSWebDVD** object calls `Render` automatically before attempting to play the disc.</span></span>

 

 



