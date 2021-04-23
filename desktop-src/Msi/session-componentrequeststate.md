---
description: Свойство Компонентрекуестстате объекта Session получает или запрашивает изменение в состоянии действия строки в таблице Component.
ms.assetid: d0b50c25-dca6-4bdf-8ee9-490e436fcc5b
title: Свойство Session. Компонентрекуестстате
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.ComponentRequestState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 17ec77c5498a808e0d7ac0f2881057979d7db0c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675724"
---
# <a name="sessioncomponentrequeststate-property"></a><span data-ttu-id="5984f-103">Свойство Session. Компонентрекуестстате</span><span class="sxs-lookup"><span data-stu-id="5984f-103">Session.ComponentRequestState property</span></span>

<span data-ttu-id="5984f-104">Свойство **компонентрекуестстате** объекта [**Session**](session-object.md) получает или запрашивает изменение в состоянии действия строки в [таблице Component](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="5984f-104">The **ComponentRequestState** property of the [**Session**](session-object.md) object obtains or requests a change in the Action state of a row in the [Component table](component-table.md).</span></span>

<span data-ttu-id="5984f-105">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="5984f-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="5984f-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5984f-106">Syntax</span></span>


```JScript
propVal = Session.ComponentRequestState
```



## <a name="property-value"></a><span data-ttu-id="5984f-107">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="5984f-107">Property value</span></span>

<span data-ttu-id="5984f-108">Обязательное строковое имя элемента компонента, первичный ключ таблицы Component.</span><span class="sxs-lookup"><span data-stu-id="5984f-108">Required string name of the component item, primary key of the Component table.</span></span>

## <a name="remarks"></a><span data-ttu-id="5984f-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5984f-109">Remarks</span></span>



| <span data-ttu-id="5984f-110">Состояние выбора</span><span class="sxs-lookup"><span data-stu-id="5984f-110">Selection state</span></span>        | <span data-ttu-id="5984f-111">Значение</span><span class="sxs-lookup"><span data-stu-id="5984f-111">Value</span></span> | <span data-ttu-id="5984f-112">Описание</span><span class="sxs-lookup"><span data-stu-id="5984f-112">Description</span></span>                                                    |
|------------------------|-------|----------------------------------------------------------------|
| <span data-ttu-id="5984f-113">NULL</span><span class="sxs-lookup"><span data-stu-id="5984f-113">Null</span></span>                   | <span data-ttu-id="5984f-114">NULL</span><span class="sxs-lookup"><span data-stu-id="5984f-114">Null</span></span>  | <span data-ttu-id="5984f-115">Запрашивает, что действие для этого элемента не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5984f-115">Requests that no action be taken for this item.</span></span>                |
| <span data-ttu-id="5984f-116">мсиинсталлстатеабсент</span><span class="sxs-lookup"><span data-stu-id="5984f-116">msiInstallStateAbsent</span></span>  | <span data-ttu-id="5984f-117">2</span><span class="sxs-lookup"><span data-stu-id="5984f-117">2</span></span>     | <span data-ttu-id="5984f-118">Элемент будет удален.</span><span class="sxs-lookup"><span data-stu-id="5984f-118">Item is to be removed.</span></span>                                         |
| <span data-ttu-id="5984f-119">мсиинсталлстателокал</span><span class="sxs-lookup"><span data-stu-id="5984f-119">msiInstallStateLocal</span></span>   | <span data-ttu-id="5984f-120">3</span><span class="sxs-lookup"><span data-stu-id="5984f-120">3</span></span>     | <span data-ttu-id="5984f-121">Элемент должен быть установлен локально.</span><span class="sxs-lookup"><span data-stu-id="5984f-121">Item is to be installed locally.</span></span>                               |
| <span data-ttu-id="5984f-122">мсиинсталлстатесаурце</span><span class="sxs-lookup"><span data-stu-id="5984f-122">msiInstallStateSource</span></span>  | <span data-ttu-id="5984f-123">4</span><span class="sxs-lookup"><span data-stu-id="5984f-123">4</span></span>     | <span data-ttu-id="5984f-124">Элемент должен быть установлен и запущен с исходного носителя.</span><span class="sxs-lookup"><span data-stu-id="5984f-124">Item is to be installed and run from the source media.</span></span>         |
| <span data-ttu-id="5984f-125">мсиинсталлстатедефаулт</span><span class="sxs-lookup"><span data-stu-id="5984f-125">msiInstallStateDefault</span></span> | <span data-ttu-id="5984f-126">5</span><span class="sxs-lookup"><span data-stu-id="5984f-126">5</span></span>     | <span data-ttu-id="5984f-127">При установке элемент будет переустановлен в том же состоянии.</span><span class="sxs-lookup"><span data-stu-id="5984f-127">If installed, the item is to be reinstalled in the same state.</span></span> |



 

<span data-ttu-id="5984f-128">Если свойство завершается неудачно, можно получить расширенные сведения об ошибке с помощью метода [**ластерроррекорд**](installer-lasterrorrecord.md) .</span><span class="sxs-lookup"><span data-stu-id="5984f-128">If the property fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="5984f-129">Требования</span><span class="sxs-lookup"><span data-stu-id="5984f-129">Requirements</span></span>



| <span data-ttu-id="5984f-130">Требование</span><span class="sxs-lookup"><span data-stu-id="5984f-130">Requirement</span></span> | <span data-ttu-id="5984f-131">Значение</span><span class="sxs-lookup"><span data-stu-id="5984f-131">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5984f-132">Версия</span><span class="sxs-lookup"><span data-stu-id="5984f-132">Version</span></span><br/> | <span data-ttu-id="5984f-133">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="5984f-133">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="5984f-134">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="5984f-134">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="5984f-135">установщик Windows в Windows Server 2003 или Windows XP</span><span class="sxs-lookup"><span data-stu-id="5984f-135">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="5984f-136">DLL</span><span class="sxs-lookup"><span data-stu-id="5984f-136">DLL</span></span><br/>     | <dl> <span data-ttu-id="5984f-137"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5984f-137"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="5984f-138">IID</span><span class="sxs-lookup"><span data-stu-id="5984f-138">IID</span></span><br/>     | <span data-ttu-id="5984f-139">IID \_ ISession определяется как 000C109E-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="5984f-139">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



 

 




