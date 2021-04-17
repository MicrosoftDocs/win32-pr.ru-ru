---
description: Свойство Компоненткостс объекта Session возвращает объект Рекордлист, перечисляющий место на диске, необходимое для установки компонента.
ms.assetid: 9b1355f1-cc99-49d9-8187-07fba4804d1f
title: Свойство Session. Компоненткостс
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.ComponentCosts
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: a6ef4e3bfd441f5de61c0f3d69aea93d6cfd2ed8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675429"
---
# <a name="sessioncomponentcosts-property"></a><span data-ttu-id="17e7f-103">Свойство Session. Компоненткостс</span><span class="sxs-lookup"><span data-stu-id="17e7f-103">Session.ComponentCosts property</span></span>

<span data-ttu-id="17e7f-104">Свойство Компоненткостс объекта [**Session**](session-object.md) возвращает объект [**рекордлист**](recordlist-object.md) , перечисляющий место на диске, необходимое для установки компонента.</span><span class="sxs-lookup"><span data-stu-id="17e7f-104">The ComponentCosts property of the [**Session**](session-object.md) object returns a [**RecordList**](recordlist-object.md) object enumerating the disk space per drive required to install a component.</span></span> <span data-ttu-id="17e7f-105">Эти сведения используются в пользовательском интерфейсе для вывода места на диске, необходимого для всех дисков.</span><span class="sxs-lookup"><span data-stu-id="17e7f-105">This information is used by the user interface to display the disk space required for all drives.</span></span> <span data-ttu-id="17e7f-106">Объем возвращаемого места на диске составляет несколько 512 байт.</span><span class="sxs-lookup"><span data-stu-id="17e7f-106">The returned disk space costs are in multiples of 512 bytes.</span></span>

<span data-ttu-id="17e7f-107">Свойство Компоненткостс должно использоваться только после того, как установщик завершит [Расчет стоимости файлов](file-costing.md) и после [действия костфинализе](costfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="17e7f-107">The ComponentCosts property should only be used after the installer has completed [file costing](file-costing.md) and after the [CostFinalize action](costfinalize-action.md).</span></span>

<span data-ttu-id="17e7f-108">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="17e7f-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="17e7f-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="17e7f-109">Syntax</span></span>


```JScript
propVal = Session.ComponentCosts
```



## <a name="property-value"></a><span data-ttu-id="17e7f-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="17e7f-110">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="17e7f-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="17e7f-111">Remarks</span></span>

<span data-ttu-id="17e7f-112">Чтобы получить общую стоимость, добавьте затраты для всех компонентов, а также стоимость подсистемы установщика (компонент = "").</span><span class="sxs-lookup"><span data-stu-id="17e7f-112">To obtain the total cost, add the costs for all components plus the installer engine cost (Component = "").</span></span>

<span data-ttu-id="17e7f-113">Компоненткостс возвращает [**объект рекордлист**](recordlist-object.md).</span><span class="sxs-lookup"><span data-stu-id="17e7f-113">ComponentCosts returns a [**RecordList object**](recordlist-object.md).</span></span> <span data-ttu-id="17e7f-114">Каждая запись в возвращенном объекте Рекордлист имеет следующие поля:</span><span class="sxs-lookup"><span data-stu-id="17e7f-114">Each record in the returned RecordList object has the following fields:</span></span>



| <span data-ttu-id="17e7f-115">Поле</span><span class="sxs-lookup"><span data-stu-id="17e7f-115">Field</span></span> | <span data-ttu-id="17e7f-116">Описание</span><span class="sxs-lookup"><span data-stu-id="17e7f-116">Description</span></span>                                          |
|-------|------------------------------------------------------|
| <span data-ttu-id="17e7f-117">1</span><span class="sxs-lookup"><span data-stu-id="17e7f-117">1</span></span>     | <span data-ttu-id="17e7f-118">Имя тома или диска</span><span class="sxs-lookup"><span data-stu-id="17e7f-118">Volume/Drive name</span></span>                                    |
| <span data-ttu-id="17e7f-119">2</span><span class="sxs-lookup"><span data-stu-id="17e7f-119">2</span></span>     | <span data-ttu-id="17e7f-120">Окончательная стоимость места на диске (кратная 512 байт).</span><span class="sxs-lookup"><span data-stu-id="17e7f-120">Final disk space cost in multiples of 512 bytes.</span></span>     |
| <span data-ttu-id="17e7f-121">3</span><span class="sxs-lookup"><span data-stu-id="17e7f-121">3</span></span>     | <span data-ttu-id="17e7f-122">Затраты на временное место на диске, кратные 512 байт.</span><span class="sxs-lookup"><span data-stu-id="17e7f-122">Temporary disk space cost in multiples of 512 bytes.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="17e7f-123">Требования</span><span class="sxs-lookup"><span data-stu-id="17e7f-123">Requirements</span></span>



| <span data-ttu-id="17e7f-124">Требование</span><span class="sxs-lookup"><span data-stu-id="17e7f-124">Requirement</span></span> | <span data-ttu-id="17e7f-125">Значение</span><span class="sxs-lookup"><span data-stu-id="17e7f-125">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17e7f-126">Версия</span><span class="sxs-lookup"><span data-stu-id="17e7f-126">Version</span></span><br/> | <span data-ttu-id="17e7f-127">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="17e7f-127">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="17e7f-128">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="17e7f-128">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="17e7f-129">установщик Windows в Windows Server 2003 или Windows XP</span><span class="sxs-lookup"><span data-stu-id="17e7f-129">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="17e7f-130">DLL</span><span class="sxs-lookup"><span data-stu-id="17e7f-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="17e7f-131"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="17e7f-131"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="17e7f-132">IID</span><span class="sxs-lookup"><span data-stu-id="17e7f-132">IID</span></span><br/>     | <span data-ttu-id="17e7f-133">IID \_ ISession определяется как 000C109E-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="17e7f-133">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



 

 




