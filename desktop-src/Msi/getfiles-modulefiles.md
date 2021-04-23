---
description: Свойство Модулефилес объекта GetObject возвращает все первичные ключи таблицы файлов для текущего открытого модуля.
ms.assetid: e1c8049c-b271-4def-abde-89ea99393574
title: Свойство файла. Модулефилес (Мержемод. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFiles.ModuleFiles
- IMsmGetFiles.get_ModuleFiles
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: d13d624f2cfb24bfa6946ca6c45fe799602f55b3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669321"
---
# <a name="getfilesmodulefiles-property"></a><span data-ttu-id="5ffc4-103">Файл Модулефилес.</span><span class="sxs-lookup"><span data-stu-id="5ffc4-103">GetFiles.ModuleFiles property</span></span>

<span data-ttu-id="5ffc4-104">Свойство **модулефилес** [**объекта GetObject возвращает**](getfiles-object.md) все первичные ключи [таблицы файлов](file-table.md) для текущего открытого модуля.</span><span class="sxs-lookup"><span data-stu-id="5ffc4-104">**ModuleFiles** property of the [**GetFiles**](getfiles-object.md) object returns all the primary keys of the [File table](file-table.md) for the currently open module.</span></span> <span data-ttu-id="5ffc4-105">Первичные ключи возвращаются в виде коллекции строк.</span><span class="sxs-lookup"><span data-stu-id="5ffc4-105">The primary keys are returned as a collection of strings.</span></span> <span data-ttu-id="5ffc4-106">Модуль должен быть открыт путем вызова метода [**опенмодуле**](merge-openmodule.md) [объекта Merge](merge-object.md) перед вызовом **модулефилес**.</span><span class="sxs-lookup"><span data-stu-id="5ffc4-106">The module must be opened by a call to the [**OpenModule**](merge-openmodule.md) method of the [Merge object](merge-object.md) before calling **ModuleFiles**.</span></span>

<span data-ttu-id="5ffc4-107">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="5ffc4-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ffc4-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5ffc4-108">Syntax</span></span>


```JScript
propVal = GetFiles.ModuleFiles
```



## <a name="property-value"></a><span data-ttu-id="5ffc4-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="5ffc4-109">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="5ffc4-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5ffc4-110">Remarks</span></span>

<span data-ttu-id="5ffc4-111">Обратите внимание, что порядок файлов, перечисленных в коллекции, может не находиться в той же последовательности, которая указана в таблице File.</span><span class="sxs-lookup"><span data-stu-id="5ffc4-111">Note that order of the files listed in the collection may not be in the same sequence as listed in the File table.</span></span>

<span data-ttu-id="5ffc4-112">Если модуль не имеет таблицы файлов или не содержит файлов на определенном языке, Модулефилес возвращает пустую коллекцию строк.</span><span class="sxs-lookup"><span data-stu-id="5ffc4-112">If the module has no File table, or contains no files in the particular language, ModuleFiles returns an empty collection of strings.</span></span>

### <a name="c"></a><span data-ttu-id="5ffc4-113">C++</span><span class="sxs-lookup"><span data-stu-id="5ffc4-113">C++</span></span>

<span data-ttu-id="5ffc4-114">См. раздел [**Получение функции \_ модулефилес**](/windows/win32/api/mergemod/nf-mergemod-imsmgetfiles-get_modulefiles) .</span><span class="sxs-lookup"><span data-stu-id="5ffc4-114">See [**get\_ModuleFiles**](/windows/win32/api/mergemod/nf-mergemod-imsmgetfiles-get_modulefiles) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ffc4-115">Требования</span><span class="sxs-lookup"><span data-stu-id="5ffc4-115">Requirements</span></span>



| <span data-ttu-id="5ffc4-116">Требование</span><span class="sxs-lookup"><span data-stu-id="5ffc4-116">Requirement</span></span> | <span data-ttu-id="5ffc4-117">Значение</span><span class="sxs-lookup"><span data-stu-id="5ffc4-117">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5ffc4-118">Версия</span><span class="sxs-lookup"><span data-stu-id="5ffc4-118">Version</span></span><br/> | <span data-ttu-id="5ffc4-119">Mergemod.dll 1,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="5ffc4-119">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="5ffc4-120">Header</span><span class="sxs-lookup"><span data-stu-id="5ffc4-120">Header</span></span><br/>  | <dl> <span data-ttu-id="5ffc4-121"><dt>Мержемод. h</dt></span><span class="sxs-lookup"><span data-stu-id="5ffc4-121"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="5ffc4-122">DLL</span><span class="sxs-lookup"><span data-stu-id="5ffc4-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="5ffc4-123"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5ffc4-123"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 
