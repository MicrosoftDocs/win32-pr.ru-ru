---
description: Метод Екстрактфилес объекта Merge извлекает из модуля внедренный CAB-файл, а затем записывает эти файлы в целевой каталог.
ms.assetid: 846355d6-32f2-4b04-91dc-acd60445fbd9
title: Метод Merge. Екстрактфилес (Адвпуб. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.ExtractFiles
- IMsmMerge.ExtractFiles
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 3869dc37b841d386891eb70940054bd78805bf94
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665540"
---
# <a name="mergeextractfiles-method"></a><span data-ttu-id="7ae46-103">Метод Merge. Екстрактфилес</span><span class="sxs-lookup"><span data-stu-id="7ae46-103">Merge.ExtractFiles method</span></span>

<span data-ttu-id="7ae46-104">Метод **екстрактфилес** объекта [**Merge**](merge-object.md) извлекает из модуля внедренный CAB-файл, а затем записывает эти файлы в целевой каталог.</span><span class="sxs-lookup"><span data-stu-id="7ae46-104">The **ExtractFiles** method of the [**Merge**](merge-object.md) object extracts the embedded .cab file from a module and then writes those files to the destination directory.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ae46-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7ae46-105">Syntax</span></span>


```JScript
Merge.ExtractFiles(
  Path
)
```



## <a name="parameters"></a><span data-ttu-id="7ae46-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7ae46-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ae46-107">*Путь*</span><span class="sxs-lookup"><span data-stu-id="7ae46-107">*Path*</span></span> 
</dt> <dd>

<span data-ttu-id="7ae46-108">Полный каталог назначения.</span><span class="sxs-lookup"><span data-stu-id="7ae46-108">The fully qualified destination directory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ae46-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7ae46-109">Return value</span></span>

<span data-ttu-id="7ae46-110">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="7ae46-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7ae46-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7ae46-111">Remarks</span></span>

<span data-ttu-id="7ae46-112">Все файлы в целевом каталоге с тем же именем перезаписываются.</span><span class="sxs-lookup"><span data-stu-id="7ae46-112">Any files in the destination directory with the same name are overwritten.</span></span> <span data-ttu-id="7ae46-113">Если путь еще не существует, он создается.</span><span class="sxs-lookup"><span data-stu-id="7ae46-113">The path is created if it does not already exist.</span></span>

<span data-ttu-id="7ae46-114">**Екстрактфилес** всегда извлекает файлы, используя короткие имена файлов для пути.</span><span class="sxs-lookup"><span data-stu-id="7ae46-114">**ExtractFiles** always extracts files using short file names for the path.</span></span> <span data-ttu-id="7ae46-115">Чтобы использовать длинные имена файлов для пути, используйте [**метод екстрактфилесекс**](merge-extractfilesex.md).</span><span class="sxs-lookup"><span data-stu-id="7ae46-115">To use long file names for the path, use the [**ExtractFilesEx method**](merge-extractfilesex.md).</span></span>

### <a name="c"></a><span data-ttu-id="7ae46-116">C++</span><span class="sxs-lookup"><span data-stu-id="7ae46-116">C++</span></span>

<span data-ttu-id="7ae46-117">См. раздел Функция [**екстрактфилес**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-extractfiles) .</span><span class="sxs-lookup"><span data-stu-id="7ae46-117">See [**ExtractFiles**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-extractfiles) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ae46-118">Требования</span><span class="sxs-lookup"><span data-stu-id="7ae46-118">Requirements</span></span>



| <span data-ttu-id="7ae46-119">Требование</span><span class="sxs-lookup"><span data-stu-id="7ae46-119">Requirement</span></span> | <span data-ttu-id="7ae46-120">Значение</span><span class="sxs-lookup"><span data-stu-id="7ae46-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ae46-121">Версия</span><span class="sxs-lookup"><span data-stu-id="7ae46-121">Version</span></span><br/> | <span data-ttu-id="7ae46-122">Mergemod.dll 1,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="7ae46-122">Mergemod.dll 1.0 or later</span></span><br/>                                                                     |
| <span data-ttu-id="7ae46-123">Header</span><span class="sxs-lookup"><span data-stu-id="7ae46-123">Header</span></span><br/>  | <dl> <span data-ttu-id="7ae46-124"><dt>Адвпуб. h (включение Мержемод. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7ae46-124"><dt>Advpub.h (include Mergemod.h)</dt></span></span> </dl> |
| <span data-ttu-id="7ae46-125">DLL</span><span class="sxs-lookup"><span data-stu-id="7ae46-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="7ae46-126"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7ae46-126"><dt>Mergemod.dll</dt></span></span> </dl>                  |



 

 
