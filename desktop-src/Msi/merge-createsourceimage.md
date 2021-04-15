---
description: Метод Креатесаурцеимаже объекта merge позволяет клиенту извлечь файлы из модуля в исходное изображение на диске после слияния, принимая во внимание изменения в модуле, которые могли быть сделаны во время настройки модуля.
ms.assetid: c3e3465a-d5a7-4fcc-b26a-5a8c763c23d9
title: Метод Merge. Креатесаурцеимаже (Мержемод. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.CreateSourceImage
- IMsmMerge.CreateSourceImage
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: e8d9365a69ff6f33c2989e9102bac7c9c22166aa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665541"
---
# <a name="mergecreatesourceimage-method"></a><span data-ttu-id="38303-103">Метод Merge. Креатесаурцеимаже</span><span class="sxs-lookup"><span data-stu-id="38303-103">Merge.CreateSourceImage method</span></span>

<span data-ttu-id="38303-104">Метод **креатесаурцеимаже** объекта [**Merge**](merge-object.md) позволяет клиенту извлечь файлы из модуля в исходное изображение на диске после слияния, принимая во внимание изменения в модуле, которые могли быть сделаны во время настройки модуля.</span><span class="sxs-lookup"><span data-stu-id="38303-104">The **CreateSourceImage** method of the [**Merge**](merge-object.md) object allows the client to extract the files from a module to a source image on disk after a merge, taking into account changes to the module that might have been made during module configuration.</span></span> <span data-ttu-id="38303-105">Список извлекаемых файлов берется из таблицы файлов модуля во время процесса слияния.</span><span class="sxs-lookup"><span data-stu-id="38303-105">The list of files to be extracted is taken from the file table of the module during the merge process.</span></span> <span data-ttu-id="38303-106">Список файлов состоит из каждого файла, успешно скопированного из таблицы файлов модуля в целевую базу данных.</span><span class="sxs-lookup"><span data-stu-id="38303-106">The list of files consists of every file successfully copied from the file table of the module to the target database.</span></span> <span data-ttu-id="38303-107">Записи файловой таблицы, которые не были скопированы из-за конфликтов первичного ключа с существующими строками в базе данных, не являются частью этого списка.</span><span class="sxs-lookup"><span data-stu-id="38303-107">File table entries that were not copied due to primary key conflicts with existing rows in the database are not a part of this list.</span></span> <span data-ttu-id="38303-108">Во время создания образа каталог для каждого из этих файлов берется из открытой базы данных (после слияния).</span><span class="sxs-lookup"><span data-stu-id="38303-108">At image creation time, the directory for each of these files comes from the open (post-merge) database.</span></span> <span data-ttu-id="38303-109">Путь, указанный в параметре *path* , является корнем исходного образа для установки.</span><span class="sxs-lookup"><span data-stu-id="38303-109">The path specified in the *Path* parameter is the root of the source image for the install.</span></span> <span data-ttu-id="38303-110">*флонгфиленамес* определяет, используются ли длинные имена файлов для сегментов пути и конечных имен файлов.</span><span class="sxs-lookup"><span data-stu-id="38303-110">*fLongFileNames* determines whether or not long file names are used for both path segments and final file names.</span></span> <span data-ttu-id="38303-111">Функция завершается ошибкой, если база данных не открыта, модуль не открыт или слияние не выполнялось.</span><span class="sxs-lookup"><span data-stu-id="38303-111">The function fails if no database is open, no module is open, or no merge has been performed.</span></span>

## <a name="syntax"></a><span data-ttu-id="38303-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="38303-112">Syntax</span></span>


```JScript
Merge.CreateSourceImage(
  Path,
  fLongFileNames,
  pFilePaths
)
```



## <a name="parameters"></a><span data-ttu-id="38303-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="38303-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38303-114">*Путь*</span><span class="sxs-lookup"><span data-stu-id="38303-114">*Path*</span></span> 
</dt> <dd>

<span data-ttu-id="38303-115">Путь к корню исходного образа для установки.</span><span class="sxs-lookup"><span data-stu-id="38303-115">The path of the root of the source image for the install.</span></span>

</dd> <dt>

<span data-ttu-id="38303-116">*флонгфиленамес*</span><span class="sxs-lookup"><span data-stu-id="38303-116">*fLongFileNames*</span></span> 
</dt> <dd>

<span data-ttu-id="38303-117">*флонгфиленамес* определяет, используются ли длинные имена файлов для сегментов пути и конечных имен файлов.</span><span class="sxs-lookup"><span data-stu-id="38303-117">*fLongFileNames* determines whether or not long file names are used for both path segments and final file names.</span></span>

</dd> <dt>

<span data-ttu-id="38303-118">*пфилепасс*</span><span class="sxs-lookup"><span data-stu-id="38303-118">*pFilePaths*</span></span> 
</dt> <dd>

<span data-ttu-id="38303-119">Это список полных путей для файлов, которые были успешно извлечены.</span><span class="sxs-lookup"><span data-stu-id="38303-119">This is a list of fully qualified paths for the files that were successfully extracted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38303-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="38303-120">Return value</span></span>

<span data-ttu-id="38303-121">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="38303-121">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="38303-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="38303-122">Remarks</span></span>

<span data-ttu-id="38303-123">Все файлы в целевом каталоге с тем же именем перезаписываются.</span><span class="sxs-lookup"><span data-stu-id="38303-123">Any files in the destination directory with the same name are overwritten.</span></span> <span data-ttu-id="38303-124">Если путь еще не существует, он создается.</span><span class="sxs-lookup"><span data-stu-id="38303-124">The path is created if it does not already exist.</span></span>

### <a name="c"></a><span data-ttu-id="38303-125">C++</span><span class="sxs-lookup"><span data-stu-id="38303-125">C++</span></span>

<span data-ttu-id="38303-126">См. раздел Функция [**креатесаурцеимаже**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-createsourceimage) .</span><span class="sxs-lookup"><span data-stu-id="38303-126">See [**CreateSourceImage**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-createsourceimage) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="38303-127">Требования</span><span class="sxs-lookup"><span data-stu-id="38303-127">Requirements</span></span>



| <span data-ttu-id="38303-128">Требование</span><span class="sxs-lookup"><span data-stu-id="38303-128">Requirement</span></span> | <span data-ttu-id="38303-129">Значение</span><span class="sxs-lookup"><span data-stu-id="38303-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="38303-130">Версия</span><span class="sxs-lookup"><span data-stu-id="38303-130">Version</span></span><br/> | <span data-ttu-id="38303-131">Mergemod.dll 2,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="38303-131">Mergemod.dll 2.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="38303-132">Header</span><span class="sxs-lookup"><span data-stu-id="38303-132">Header</span></span><br/>  | <dl> <span data-ttu-id="38303-133"><dt>Мержемод. h</dt></span><span class="sxs-lookup"><span data-stu-id="38303-133"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="38303-134">DLL</span><span class="sxs-lookup"><span data-stu-id="38303-134">DLL</span></span><br/>     | <dl> <span data-ttu-id="38303-135"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="38303-135"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 




