---
description: Метод Екстрактфилесекс объекта Merge извлекает из модуля внедренный CAB-файл, а затем записывает эти файлы в целевой каталог.
ms.assetid: 8b063052-4f92-466a-9c52-bda26ed13d5c
title: Метод Merge. Екстрактфилесекс (Мержемод. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.ExtractFilesEx
- IMsmMerge.ExtractFilesEx
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: be6aa1001be0d3ecd6cbb9c4cd1d8c04b4649f10
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105652223"
---
# <a name="mergeextractfilesex-method"></a><span data-ttu-id="56486-103">Метод Merge. Екстрактфилесекс</span><span class="sxs-lookup"><span data-stu-id="56486-103">Merge.ExtractFilesEx method</span></span>

<span data-ttu-id="56486-104">Метод **екстрактфилесекс** объекта [**Merge**](merge-object.md) извлекает из модуля внедренный CAB-файл, а затем записывает эти файлы в целевой каталог.</span><span class="sxs-lookup"><span data-stu-id="56486-104">The **ExtractFilesEx** method of the [**Merge**](merge-object.md) object extracts the embedded .cab file from a module and then writes those files to the destination directory.</span></span>

## <a name="syntax"></a><span data-ttu-id="56486-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="56486-105">Syntax</span></span>


```JScript
Merge.ExtractFilesEx(
  Path,
  fLongFileNames,
  pFilePaths
)
```



## <a name="parameters"></a><span data-ttu-id="56486-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="56486-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56486-107">*Путь*</span><span class="sxs-lookup"><span data-stu-id="56486-107">*Path*</span></span> 
</dt> <dd>

<span data-ttu-id="56486-108">Полный каталог назначения.</span><span class="sxs-lookup"><span data-stu-id="56486-108">The fully qualified destination directory.</span></span>

</dd> <dt>

<span data-ttu-id="56486-109">*флонгфиленамес*</span><span class="sxs-lookup"><span data-stu-id="56486-109">*fLongFileNames*</span></span> 
</dt> <dd>

<span data-ttu-id="56486-110">Задайте, чтобы указать использование длинных имен файлов для сегментов пути и окончательных имен файлов.</span><span class="sxs-lookup"><span data-stu-id="56486-110">Set to specify using long file names for path segments and final file names.</span></span>

</dd> <dt>

<span data-ttu-id="56486-111">*пфилепасс*</span><span class="sxs-lookup"><span data-stu-id="56486-111">*pFilePaths*</span></span> 
</dt> <dd>

<span data-ttu-id="56486-112">Это список полных путей для файлов, которые были успешно извлечены.</span><span class="sxs-lookup"><span data-stu-id="56486-112">This is a list of fully qualified paths for the files that were successfully extracted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56486-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="56486-113">Return value</span></span>

<span data-ttu-id="56486-114">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="56486-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="56486-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="56486-115">Remarks</span></span>

<span data-ttu-id="56486-116">Все файлы в целевом каталоге с тем же именем перезаписываются.</span><span class="sxs-lookup"><span data-stu-id="56486-116">Any files in the destination directory with the same name are overwritten.</span></span> <span data-ttu-id="56486-117">Если путь еще не существует, он создается.</span><span class="sxs-lookup"><span data-stu-id="56486-117">The path is created if it does not already exist.</span></span>

### <a name="c"></a><span data-ttu-id="56486-118">C++</span><span class="sxs-lookup"><span data-stu-id="56486-118">C++</span></span>

<span data-ttu-id="56486-119">См. раздел Функция [**екстрактфилесекс**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-extractfilesex) .</span><span class="sxs-lookup"><span data-stu-id="56486-119">See [**ExtractFilesEx**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-extractfilesex) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="56486-120">Требования</span><span class="sxs-lookup"><span data-stu-id="56486-120">Requirements</span></span>



| <span data-ttu-id="56486-121">Требование</span><span class="sxs-lookup"><span data-stu-id="56486-121">Requirement</span></span> | <span data-ttu-id="56486-122">Значение</span><span class="sxs-lookup"><span data-stu-id="56486-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="56486-123">Версия</span><span class="sxs-lookup"><span data-stu-id="56486-123">Version</span></span><br/> | <span data-ttu-id="56486-124">Mergemod.dll 2,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="56486-124">Mergemod.dll 2.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="56486-125">Header</span><span class="sxs-lookup"><span data-stu-id="56486-125">Header</span></span><br/>  | <dl> <span data-ttu-id="56486-126"><dt>Мержемод. h</dt></span><span class="sxs-lookup"><span data-stu-id="56486-126"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="56486-127">DLL</span><span class="sxs-lookup"><span data-stu-id="56486-127">DLL</span></span><br/>     | <dl> <span data-ttu-id="56486-128"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="56486-128"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 




