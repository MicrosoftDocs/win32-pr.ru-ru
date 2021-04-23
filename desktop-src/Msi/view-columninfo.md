---
description: Свойство ColumnInfo объекта View возвращает объект Record, содержащий запрошенные сведения о каждом столбце результирующего набора.
ms.assetid: 8cfa504c-a6f1-443e-9b3a-b230c4c39b64
title: Свойство View. ColumnInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- View.ColumnInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 38c016b15108446cc04114adc06ad12686d9932c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651823"
---
# <a name="viewcolumninfo-property"></a><span data-ttu-id="1a452-103">Свойство View. ColumnInfo</span><span class="sxs-lookup"><span data-stu-id="1a452-103">View.ColumnInfo property</span></span>

<span data-ttu-id="1a452-104">Свойство **ColumnInfo** объекта [**View**](view-object.md) возвращает объект [**Record**](record-object.md) , содержащий запрошенные сведения о каждом столбце результирующего набора.</span><span class="sxs-lookup"><span data-stu-id="1a452-104">The **ColumnInfo** property of the [**View**](view-object.md) object returns a [**Record**](record-object.md) object containing the requested information about each column in the result set.</span></span> <span data-ttu-id="1a452-105">Могут быть запрошены либо имена столбцов, либо определения столбцов.</span><span class="sxs-lookup"><span data-stu-id="1a452-105">Either the column names or the column definitions may be requested.</span></span> <span data-ttu-id="1a452-106">Константы, предоставленные в списке выбора, не имеют имен.</span><span class="sxs-lookup"><span data-stu-id="1a452-106">Constants supplied in the Select list do not have names.</span></span>

<span data-ttu-id="1a452-107">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="1a452-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a452-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1a452-108">Syntax</span></span>


```JScript
propVal = View.ColumnInfo
```



## <a name="property-value"></a><span data-ttu-id="1a452-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="1a452-109">Property value</span></span>

<span data-ttu-id="1a452-110">Необходимые сведения для каждого столбца.</span><span class="sxs-lookup"><span data-stu-id="1a452-110">Required information needed for each column.</span></span>



| <span data-ttu-id="1a452-111">Имя параметра</span><span class="sxs-lookup"><span data-stu-id="1a452-111">Parameter name</span></span>                                                                                                                                                                                                                                                          | <span data-ttu-id="1a452-112">Значение</span><span class="sxs-lookup"><span data-stu-id="1a452-112">Meaning</span></span>                                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <span id="msiColumnInfoNames"></span><span id="msicolumninfonames"></span><span id="MSICOLUMNINFONAMES"></span><dl> <span data-ttu-id="1a452-113"><dt>**мсиколумнинфонамес**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="1a452-113"><dt>**msiColumnInfoNames**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="1a452-114">Возвращает имена всех неконстантных столбцов в результирующем наборе.</span><span class="sxs-lookup"><span data-stu-id="1a452-114">Returns the names of all nonconstant columns in result set.</span></span><br/> |
| <span id="msiColumnInfoTypes"></span><span id="msicolumninfotypes"></span><span id="MSICOLUMNINFOTYPES"></span><dl> <span data-ttu-id="1a452-115"><dt>**мсиколумнинфотипес**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="1a452-115"><dt>**msiColumnInfoTypes**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="1a452-116">Возвращает типы всех неконстантных столбцов в результирующем наборе.</span><span class="sxs-lookup"><span data-stu-id="1a452-116">Returns the types of all nonconstant columns in result set.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="1a452-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1a452-117">Remarks</span></span>

<span data-ttu-id="1a452-118">Описания столбцов, возвращаемые свойством **ColumnInfo** , имеют формат, описанный в разделе [Формат определения столбца](column-definition-format.md).</span><span class="sxs-lookup"><span data-stu-id="1a452-118">The column descriptions returned by the **ColumnInfo** property are in the format described in [Column Definition Format](column-definition-format.md).</span></span> <span data-ttu-id="1a452-119">Каждый столбец описывается строкой в соответствующем поле записи.</span><span class="sxs-lookup"><span data-stu-id="1a452-119">Each column is described by a string in the corresponding record field.</span></span> <span data-ttu-id="1a452-120">Строка определения состоит из одной буквы, представляющей тип данных, а затем ширины столбца (в символах, если применимо или в других байтах).</span><span class="sxs-lookup"><span data-stu-id="1a452-120">The definition string consists of a single letter representing the data type followed by the width of the column (in characters when applicable, or else bytes).</span></span> <span data-ttu-id="1a452-121">Нулевая ширина означает неограниченную ширину (длинные текстовые поля и потоки).</span><span class="sxs-lookup"><span data-stu-id="1a452-121">A width of zero designates an unbounded width (long text fields and streams).</span></span> <span data-ttu-id="1a452-122">Прописная буква означает, что в столбце разрешены значения NULL.</span><span class="sxs-lookup"><span data-stu-id="1a452-122">An uppercase letter indicates that Null values are allowed in the column.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a452-123">Требования</span><span class="sxs-lookup"><span data-stu-id="1a452-123">Requirements</span></span>



| <span data-ttu-id="1a452-124">Требование</span><span class="sxs-lookup"><span data-stu-id="1a452-124">Requirement</span></span> | <span data-ttu-id="1a452-125">Значение</span><span class="sxs-lookup"><span data-stu-id="1a452-125">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a452-126">Версия</span><span class="sxs-lookup"><span data-stu-id="1a452-126">Version</span></span><br/> | <span data-ttu-id="1a452-127">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="1a452-127">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="1a452-128">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="1a452-128">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="1a452-129">установщик Windows в Windows Server 2003 или Windows XP</span><span class="sxs-lookup"><span data-stu-id="1a452-129">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="1a452-130">DLL</span><span class="sxs-lookup"><span data-stu-id="1a452-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="1a452-131"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1a452-131"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="1a452-132">IID</span><span class="sxs-lookup"><span data-stu-id="1a452-132">IID</span></span><br/>     | <span data-ttu-id="1a452-133">IID \_ IView определен как 000C109C-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="1a452-133">IID\_IView is defined as 000C109C-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                |



 

 




