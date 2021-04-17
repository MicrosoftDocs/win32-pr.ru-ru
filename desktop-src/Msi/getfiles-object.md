---
description: Объект GetObject извлекает файлы, необходимые на определенном языке модуля. Требует выполнения определенных действий через объект MERGE, прежде чем все части этого интерфейса будут возвращать допустимые результаты.
ms.assetid: f3bf64ec-75f7-43a6-bbd8-a51508c57002
title: Объект GetObject (Мержемод. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFiles
- IMsmGetFiles
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 8a26bb072b0b4a1f048ded76fbd52ffc6d42de62
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105652207"
---
# <a name="getfiles-object"></a><span data-ttu-id="81f67-104">Файл GetObject</span><span class="sxs-lookup"><span data-stu-id="81f67-104">GetFiles object</span></span>

<span data-ttu-id="81f67-105">Объект **GetObject извлекает** файлы, необходимые на определенном языке модуля.</span><span class="sxs-lookup"><span data-stu-id="81f67-105">The **GetFiles** object retrieves the files needed in a particular language of the module.</span></span> <span data-ttu-id="81f67-106">Требует выполнения определенных действий через [объект Merge](merge-object.md) , прежде чем все части этого интерфейса будут возвращать допустимые результаты.</span><span class="sxs-lookup"><span data-stu-id="81f67-106">Requires certain actions be performed through the [Merge object](merge-object.md) before all parts of this interface returns valid results.</span></span>

## <a name="members"></a><span data-ttu-id="81f67-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="81f67-107">Members</span></span>

<span data-ttu-id="81f67-108">Объект **GetObject** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="81f67-108">The **GetFiles** object has these types of members:</span></span>

-   [<span data-ttu-id="81f67-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="81f67-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="81f67-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="81f67-110">Properties</span></span>

<span data-ttu-id="81f67-111">Объект **GetObject** имеет эти свойства.</span><span class="sxs-lookup"><span data-stu-id="81f67-111">The **GetFiles** object has these properties.</span></span>



| <span data-ttu-id="81f67-112">Свойство</span><span class="sxs-lookup"><span data-stu-id="81f67-112">Property</span></span>                                               | <span data-ttu-id="81f67-113">Описание</span><span class="sxs-lookup"><span data-stu-id="81f67-113">Description</span></span>                                                                                                                                                     |
|:-------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="81f67-114">**модулефилес**</span><span class="sxs-lookup"><span data-stu-id="81f67-114">**ModuleFiles**</span></span>](getfiles-modulefiles.md)<br/> | <span data-ttu-id="81f67-115">Свойство [**модулефилес**](getfiles-modulefiles.md) возвращает все первичные ключи [таблицы файлов](file-table.md) для текущего открытого модуля.</span><span class="sxs-lookup"><span data-stu-id="81f67-115">[**ModuleFiles**](getfiles-modulefiles.md) property returns all the primary keys of the [File table](file-table.md) for the currently open module.</span></span><br/> |



 

## <a name="c"></a><span data-ttu-id="81f67-116">C++</span><span class="sxs-lookup"><span data-stu-id="81f67-116">C++</span></span>

<span data-ttu-id="81f67-117">интерфейс **имсмжетфилес: IDispatch**</span><span class="sxs-lookup"><span data-stu-id="81f67-117">interface **IMsmGetFiles : IDispatch**</span></span>

## <a name="interface-id"></a><span data-ttu-id="81f67-118">Идентификатор интерфейса</span><span class="sxs-lookup"><span data-stu-id="81f67-118">Interface ID</span></span>



| <span data-ttu-id="81f67-119">Константа</span><span class="sxs-lookup"><span data-stu-id="81f67-119">Constant</span></span>              | <span data-ttu-id="81f67-120">Значение</span><span class="sxs-lookup"><span data-stu-id="81f67-120">Value</span></span>                                  |
|-----------------------|----------------------------------------|
| <span data-ttu-id="81f67-121">**IID \_ имсмжетфилес**</span><span class="sxs-lookup"><span data-stu-id="81f67-121">**IID\_IMsmGetFiles**</span></span> | <span data-ttu-id="81f67-122">{7041AE26-2D78-11D2-888A-00A0C981B015}</span><span class="sxs-lookup"><span data-stu-id="81f67-122">{7041AE26-2D78-11D2-888A-00A0C981B015}</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="81f67-123">Требования</span><span class="sxs-lookup"><span data-stu-id="81f67-123">Requirements</span></span>



| <span data-ttu-id="81f67-124">Требование</span><span class="sxs-lookup"><span data-stu-id="81f67-124">Requirement</span></span> | <span data-ttu-id="81f67-125">Значение</span><span class="sxs-lookup"><span data-stu-id="81f67-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="81f67-126">Версия</span><span class="sxs-lookup"><span data-stu-id="81f67-126">Version</span></span><br/> | <span data-ttu-id="81f67-127">Mergemod.dll 1,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="81f67-127">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="81f67-128">Header</span><span class="sxs-lookup"><span data-stu-id="81f67-128">Header</span></span><br/>  | <dl> <span data-ttu-id="81f67-129"><dt>Мержемод. h</dt></span><span class="sxs-lookup"><span data-stu-id="81f67-129"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="81f67-130">DLL</span><span class="sxs-lookup"><span data-stu-id="81f67-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="81f67-131"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="81f67-131"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 




