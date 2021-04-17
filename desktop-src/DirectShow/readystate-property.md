---
description: Свойство ReadyState извлекает значение свойства ReadyState объекта Мсвебдвд.
ms.assetid: e43b0fa4-4a5a-4492-a6a9-bf271f58e11b
title: Свойство ReadyState (ОЦидл. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- READYSTATE
api_type:
- HeaderDef
api_location:
- ocidl.h
ms.openlocfilehash: a52b20349c58e8bd44458266da6a0a33ea149c98
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675344"
---
# <a name="readystate-property"></a><span data-ttu-id="d8331-103">Свойство ReadyState</span><span class="sxs-lookup"><span data-stu-id="d8331-103">ReadyState Property</span></span>

> [!Note]  
> <span data-ttu-id="d8331-104">Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="d8331-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="d8331-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="d8331-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="d8331-106">`ReadyState`Свойство получает значение свойства readyState объекта **мсвебдвд** .</span><span class="sxs-lookup"><span data-stu-id="d8331-106">The `ReadyState` property retrieves the ReadyState of the **MSWebDVD** object.</span></span>

``` syntax
[ iReadyState = ] MSWebDVD.ReadyState
```

## <a name="return-value"></a><span data-ttu-id="d8331-107">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d8331-107">Return Value</span></span>

<span data-ttu-id="d8331-108">Возвращает целочисленное значение, представляющее параметр ReadyState элемента управления.</span><span class="sxs-lookup"><span data-stu-id="d8331-108">Returns an integer value representing the control's ReadyState.</span></span>



| <span data-ttu-id="d8331-109">Код возврата</span><span class="sxs-lookup"><span data-stu-id="d8331-109">Return code</span></span> | <span data-ttu-id="d8331-110">Описание</span><span class="sxs-lookup"><span data-stu-id="d8331-110">Description</span></span>                                               |
|-------------|-----------------------------------------------------------|
| <span data-ttu-id="d8331-111">0</span><span class="sxs-lookup"><span data-stu-id="d8331-111">0</span></span>           | <span data-ttu-id="d8331-112">Состояние инициализации по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d8331-112">Default initialization state.</span></span>                             |
| <span data-ttu-id="d8331-113">1</span><span class="sxs-lookup"><span data-stu-id="d8331-113">1</span></span>           | <span data-ttu-id="d8331-114">Объект загружает свойства.</span><span class="sxs-lookup"><span data-stu-id="d8331-114">Object is loading its properties.</span></span>                         |
| <span data-ttu-id="d8331-115">2</span><span class="sxs-lookup"><span data-stu-id="d8331-115">2</span></span>           | <span data-ttu-id="d8331-116">Объект инициализирован.</span><span class="sxs-lookup"><span data-stu-id="d8331-116">Object has been initialized.</span></span>                              |
| <span data-ttu-id="d8331-117">3</span><span class="sxs-lookup"><span data-stu-id="d8331-117">3</span></span>           | <span data-ttu-id="d8331-118">Объект является интерактивным, но не все его данные доступны.</span><span class="sxs-lookup"><span data-stu-id="d8331-118">Object is interactive, but not all its data is available.</span></span> |
| <span data-ttu-id="d8331-119">4</span><span class="sxs-lookup"><span data-stu-id="d8331-119">4</span></span>           | <span data-ttu-id="d8331-120">Объект получил все свои данные.</span><span class="sxs-lookup"><span data-stu-id="d8331-120">Object has received all its data.</span></span>                         |



 

## <a name="remarks"></a><span data-ttu-id="d8331-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d8331-121">Remarks</span></span>

<span data-ttu-id="d8331-122">Это свойство доступно только для чтения и не имеет значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d8331-122">This property is read-only with no default value.</span></span>

<span data-ttu-id="d8331-123">Любой объект, внедренный в веб-страницу, предоставляет `ReadyState` свойство.</span><span class="sxs-lookup"><span data-stu-id="d8331-123">Any object embedded in a Web page exposes the `ReadyState` property.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8331-124">Требования</span><span class="sxs-lookup"><span data-stu-id="d8331-124">Requirements</span></span>



| <span data-ttu-id="d8331-125">Требование</span><span class="sxs-lookup"><span data-stu-id="d8331-125">Requirement</span></span> | <span data-ttu-id="d8331-126">Значение</span><span class="sxs-lookup"><span data-stu-id="d8331-126">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d8331-127">Header</span><span class="sxs-lookup"><span data-stu-id="d8331-127">Header</span></span><br/> | <dl> <span data-ttu-id="d8331-128"><dt>ОЦидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="d8331-128"><dt>Ocidl.h</dt></span></span> </dl> |



 

 




