---
description: Объект зависимости возвращает модуль, от которого зависит текущий модуль, который еще не был объединен с текущей базой данных установки.
ms.assetid: 3157f07d-99de-4628-9b03-eb86eb4896a4
title: Объект зависимости (Мержемод. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Dependency
- IMsmDependency
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 24b215b67d22d27639f3e002590e7d08dd54b0c6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651949"
---
# <a name="dependency-object"></a><span data-ttu-id="8b7dc-103">Объект зависимости</span><span class="sxs-lookup"><span data-stu-id="8b7dc-103">Dependency object</span></span>

<span data-ttu-id="8b7dc-104">Объект **зависимости** возвращает модуль, от которого зависит текущий модуль, который еще не был объединен с текущей базой данных установки.</span><span class="sxs-lookup"><span data-stu-id="8b7dc-104">The **Dependency** object returns a module that the current module is dependent upon and which has not yet been merged into the current installation database.</span></span>

## <a name="members"></a><span data-ttu-id="8b7dc-105">Элементы</span><span class="sxs-lookup"><span data-stu-id="8b7dc-105">Members</span></span>

<span data-ttu-id="8b7dc-106">Объект **зависимости** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="8b7dc-106">The **Dependency** object has these types of members:</span></span>

-   [<span data-ttu-id="8b7dc-107">Свойства</span><span class="sxs-lookup"><span data-stu-id="8b7dc-107">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8b7dc-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="8b7dc-108">Properties</span></span>

<span data-ttu-id="8b7dc-109">Объект **зависимости** имеет эти свойства.</span><span class="sxs-lookup"><span data-stu-id="8b7dc-109">The **Dependency** object has these properties.</span></span>



| <span data-ttu-id="8b7dc-110">Свойство</span><span class="sxs-lookup"><span data-stu-id="8b7dc-110">Property</span></span>                                           | <span data-ttu-id="8b7dc-111">Описание</span><span class="sxs-lookup"><span data-stu-id="8b7dc-111">Description</span></span>                                             |
|:---------------------------------------------------|:--------------------------------------------------------|
| [<span data-ttu-id="8b7dc-112">**Язык**</span><span class="sxs-lookup"><span data-stu-id="8b7dc-112">**Language**</span></span>](dependency-language.md)<br/> | <span data-ttu-id="8b7dc-113">Возвращает язык модуля.</span><span class="sxs-lookup"><span data-stu-id="8b7dc-113">Return the language of the module.</span></span><br/>           |
| [<span data-ttu-id="8b7dc-114">**Модуль**</span><span class="sxs-lookup"><span data-stu-id="8b7dc-114">**Module**</span></span>](dependency-module.md)<br/>     | <span data-ttu-id="8b7dc-115">Возвращает идентификатор модуля требуемого модуля.</span><span class="sxs-lookup"><span data-stu-id="8b7dc-115">Return the module ID of the required module.</span></span><br/> |
| [<span data-ttu-id="8b7dc-116">**Версия**</span><span class="sxs-lookup"><span data-stu-id="8b7dc-116">**Version**</span></span>](dependency-version.md)<br/>   | <span data-ttu-id="8b7dc-117">Возврат версии требуемого модуля.</span><span class="sxs-lookup"><span data-stu-id="8b7dc-117">Return the version of the required module.</span></span><br/>   |



 

## <a name="c"></a><span data-ttu-id="8b7dc-118">C++</span><span class="sxs-lookup"><span data-stu-id="8b7dc-118">C++</span></span>

<span data-ttu-id="8b7dc-119">интерфейс **имсмдепенденци: IDispatch**</span><span class="sxs-lookup"><span data-stu-id="8b7dc-119">interface **IMsmDependency : IDispatch**</span></span>

## <a name="interface-id"></a><span data-ttu-id="8b7dc-120">Идентификатор интерфейса</span><span class="sxs-lookup"><span data-stu-id="8b7dc-120">Interface ID</span></span>



| <span data-ttu-id="8b7dc-121">Константа</span><span class="sxs-lookup"><span data-stu-id="8b7dc-121">Constant</span></span>                | <span data-ttu-id="8b7dc-122">Значение</span><span class="sxs-lookup"><span data-stu-id="8b7dc-122">Value</span></span>                                  |
|-------------------------|----------------------------------------|
| <span data-ttu-id="8b7dc-123">**IID \_ имсмдепенденци**</span><span class="sxs-lookup"><span data-stu-id="8b7dc-123">**IID\_IMsmDependency**</span></span> | <span data-ttu-id="8b7dc-124">{0ADDA82D-2C26-11D2-AD65-00A0C9AF11A6}</span><span class="sxs-lookup"><span data-stu-id="8b7dc-124">{0ADDA82D-2C26-11D2-AD65-00A0C9AF11A6}</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="8b7dc-125">Требования</span><span class="sxs-lookup"><span data-stu-id="8b7dc-125">Requirements</span></span>



| <span data-ttu-id="8b7dc-126">Требование</span><span class="sxs-lookup"><span data-stu-id="8b7dc-126">Requirement</span></span> | <span data-ttu-id="8b7dc-127">Значение</span><span class="sxs-lookup"><span data-stu-id="8b7dc-127">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8b7dc-128">Версия</span><span class="sxs-lookup"><span data-stu-id="8b7dc-128">Version</span></span><br/> | <span data-ttu-id="8b7dc-129">Mergemod.dll 1,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="8b7dc-129">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="8b7dc-130">Header</span><span class="sxs-lookup"><span data-stu-id="8b7dc-130">Header</span></span><br/>  | <dl> <span data-ttu-id="8b7dc-131"><dt>Мержемод. h</dt></span><span class="sxs-lookup"><span data-stu-id="8b7dc-131"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="8b7dc-132">DLL</span><span class="sxs-lookup"><span data-stu-id="8b7dc-132">DLL</span></span><br/>     | <dl> <span data-ttu-id="8b7dc-133"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8b7dc-133"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 




