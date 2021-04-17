---
description: Свойство зависимостей только для чтения объекта Merge Возвращает коллекцию объектов зависимостей, которая перечисляет набор неудовлетворенных зависимостей для текущей базы данных.
ms.assetid: d7081ffe-3d9e-486e-84b6-b45e92fff5f0
title: Свойство MERGE. Dependencies (Мержемод. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.Dependencies
- IMsmMerge.get_Dependencies
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 4c92d24ac2172b0d14de8e0609a407f2a0808494
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651874"
---
# <a name="mergedependencies-property"></a><span data-ttu-id="0f5ab-103">Merge. DEPENDENCIES, свойство</span><span class="sxs-lookup"><span data-stu-id="0f5ab-103">Merge.Dependencies property</span></span>

<span data-ttu-id="0f5ab-104">Свойство **зависимостей** только для чтения объекта [**Merge**](merge-object.md) Возвращает коллекцию объектов [**зависимостей**](dependency-object.md) , которая перечисляет набор неудовлетворенных зависимостей для текущей базы данных.</span><span class="sxs-lookup"><span data-stu-id="0f5ab-104">The read-only **Dependencies** property of the [**Merge**](merge-object.md) object returns a collection of [**Dependency**](dependency-object.md) objects that enumerates a set of unsatisfied dependencies for the current database.</span></span>

<span data-ttu-id="0f5ab-105">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="0f5ab-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f5ab-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0f5ab-106">Syntax</span></span>


```JScript
propVal = Merge.Dependencies
```



## <a name="property-value"></a><span data-ttu-id="0f5ab-107">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="0f5ab-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="0f5ab-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0f5ab-108">Remarks</span></span>

<span data-ttu-id="0f5ab-109">Для получения сведений о зависимостях не требуется открывать модуль.</span><span class="sxs-lookup"><span data-stu-id="0f5ab-109">A module does not need to be open to retrieve dependency information.</span></span>

### <a name="c"></a><span data-ttu-id="0f5ab-110">C++</span><span class="sxs-lookup"><span data-stu-id="0f5ab-110">C++</span></span>

<span data-ttu-id="0f5ab-111">См. раздел [**Получение \_ зависимостей**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-get_dependencies) .</span><span class="sxs-lookup"><span data-stu-id="0f5ab-111">See [**get\_Dependencies**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-get_dependencies) Function.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f5ab-112">Требования</span><span class="sxs-lookup"><span data-stu-id="0f5ab-112">Requirements</span></span>



| <span data-ttu-id="0f5ab-113">Требование</span><span class="sxs-lookup"><span data-stu-id="0f5ab-113">Requirement</span></span> | <span data-ttu-id="0f5ab-114">Значение</span><span class="sxs-lookup"><span data-stu-id="0f5ab-114">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0f5ab-115">Версия</span><span class="sxs-lookup"><span data-stu-id="0f5ab-115">Version</span></span><br/> | <span data-ttu-id="0f5ab-116">Mergemod.dll 1,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="0f5ab-116">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="0f5ab-117">Header</span><span class="sxs-lookup"><span data-stu-id="0f5ab-117">Header</span></span><br/>  | <dl> <span data-ttu-id="0f5ab-118"><dt>Мержемод. h</dt></span><span class="sxs-lookup"><span data-stu-id="0f5ab-118"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="0f5ab-119">DLL</span><span class="sxs-lookup"><span data-stu-id="0f5ab-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="0f5ab-120"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0f5ab-120"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 
