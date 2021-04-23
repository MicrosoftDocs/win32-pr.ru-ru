---
description: Метод Опенмодуле объекта Merge открывает модуль слияния установщик Windows в режиме только для чтения. Модуль необходимо открыть, прежде чем его можно будет объединить с базой данных установки.
ms.assetid: fc976899-2c39-4314-b2fb-417e0dfc53b9
title: Метод Merge. Опенмодуле (Мержемод. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.OpenModule
- IMsmMerge.OpenModule
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 9d83a9331c91817f70c49ecf74c7171c5e627be6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680121"
---
# <a name="mergeopenmodule-method"></a><span data-ttu-id="82a96-104">Метод Merge. Опенмодуле</span><span class="sxs-lookup"><span data-stu-id="82a96-104">Merge.OpenModule method</span></span>

<span data-ttu-id="82a96-105">Метод **опенмодуле** объекта [**Merge**](merge-object.md) открывает модуль слияния установщик Windows в режиме только для чтения.</span><span class="sxs-lookup"><span data-stu-id="82a96-105">The **OpenModule** method of the [**Merge**](merge-object.md) object opens a Windows Installer merge module in read-only mode.</span></span> <span data-ttu-id="82a96-106">Модуль необходимо открыть, прежде чем его можно будет объединить с базой данных установки.</span><span class="sxs-lookup"><span data-stu-id="82a96-106">A module must be opened before it can be merged with an installation database.</span></span>

## <a name="syntax"></a><span data-ttu-id="82a96-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="82a96-107">Syntax</span></span>


```JScript
Merge.OpenModule(
  FileName,
  Language
)
```



## <a name="parameters"></a><span data-ttu-id="82a96-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="82a96-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82a96-109">*FileName*</span><span class="sxs-lookup"><span data-stu-id="82a96-109">*FileName*</span></span> 
</dt> <dd>

<span data-ttu-id="82a96-110">Полное имя файла, указывающее на модуль слияния.</span><span class="sxs-lookup"><span data-stu-id="82a96-110">Fully qualified file name pointing to a merge module.</span></span>

</dd> <dt>

<span data-ttu-id="82a96-111">*Язык*</span><span class="sxs-lookup"><span data-stu-id="82a96-111">*Language*</span></span> 
</dt> <dd>

<span data-ttu-id="82a96-112">Допустимый идентификатор языка (LANGID).</span><span class="sxs-lookup"><span data-stu-id="82a96-112">A valid language identifier (LANGID).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82a96-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="82a96-113">Return value</span></span>

<span data-ttu-id="82a96-114">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="82a96-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="82a96-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="82a96-115">Remarks</span></span>

<span data-ttu-id="82a96-116">Эта функция открывает модуль слияния в режиме только для чтения и исключает другие программы из записи в модуль слияния, пока не будет вызван метод [**клосемодуле**](merge-closemodule.md) .</span><span class="sxs-lookup"><span data-stu-id="82a96-116">This function opens the merge module in read-only mode and excludes other programs from writing to the merge module until the [**CloseModule**](merge-closemodule.md) method is called.</span></span>

<span data-ttu-id="82a96-117">Установщик пытается открыть модуль на языке, указанном *языком*, или на более общем языке.</span><span class="sxs-lookup"><span data-stu-id="82a96-117">The installer attempts to open the module in the language specified by *Language*, or a more general language.</span></span> <span data-ttu-id="82a96-118">Например, если *язык* указан как 1033, то модуль с языком по умолчанию 1033, 9 или 0 можно открыть на языке по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="82a96-118">For example, if *Language* is specified as 1033, a module with a default language of 1033, 9, or 0 can be opened in its default language.</span></span> <span data-ttu-id="82a96-119">Значение параметра *Language* , равное 9, открывает модули с языком по умолчанию 9 или 0.</span><span class="sxs-lookup"><span data-stu-id="82a96-119">A *Language* value of 9 opens modules with a default language of 9 or 0.</span></span> <span data-ttu-id="82a96-120">Если язык по умолчанию модуля не соответствует указанным требованиям, предпринимается попытка преобразовать модуль в требуемый язык.</span><span class="sxs-lookup"><span data-stu-id="82a96-120">If the default language of the module does not meet the specified requirements, an attempt is made to transform the module to the requested language.</span></span> <span data-ttu-id="82a96-121">Если это не удается, модуль преобразуется в все более общие языки, не зависящие от языка.</span><span class="sxs-lookup"><span data-stu-id="82a96-121">If that fails, the module is transformed to increasingly general languages, all the way to language neutral.</span></span> <span data-ttu-id="82a96-122">Если ни одно из преобразований не выполнено, модуль не открывается.</span><span class="sxs-lookup"><span data-stu-id="82a96-122">If none of the transforms succeed, the module fails to open.</span></span> <span data-ttu-id="82a96-123">В этом случае в список ошибок типа Мсмеррорлангуажеунсуппортед добавляется ошибка.</span><span class="sxs-lookup"><span data-stu-id="82a96-123">In this case, an error is added to the error list of type msmErrorLanguageUnsupported.</span></span> <span data-ttu-id="82a96-124">Если при преобразовании модуля на нужный язык возникает ошибка, в список ошибок типа Мсмеррорлангуажефаилед добавляется ошибка.</span><span class="sxs-lookup"><span data-stu-id="82a96-124">If there is an error transforming the module to the desired language, an error is added to the error list of type msmErrorLanguageFailed.</span></span> <span data-ttu-id="82a96-125">Дополнительные сведения см. в описании свойства [**Type**](error-type.md) объекта [**Error**](error-object.md) .</span><span class="sxs-lookup"><span data-stu-id="82a96-125">For details, see the [**Type**](error-type.md) property of the [**Error**](error-object.md) object.</span></span> <span data-ttu-id="82a96-126">При открытии модуля слияния очищаются все ошибки, которые еще не были получены.</span><span class="sxs-lookup"><span data-stu-id="82a96-126">Opening a merge module clears any errors that have not already been retrieved.</span></span>

### <a name="c"></a><span data-ttu-id="82a96-127">C++</span><span class="sxs-lookup"><span data-stu-id="82a96-127">C++</span></span>

<span data-ttu-id="82a96-128">См. раздел Функция [**опенмодуле**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-openmodule) .</span><span class="sxs-lookup"><span data-stu-id="82a96-128">See [**OpenModule**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-openmodule) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="82a96-129">Требования</span><span class="sxs-lookup"><span data-stu-id="82a96-129">Requirements</span></span>



| <span data-ttu-id="82a96-130">Требование</span><span class="sxs-lookup"><span data-stu-id="82a96-130">Requirement</span></span> | <span data-ttu-id="82a96-131">Значение</span><span class="sxs-lookup"><span data-stu-id="82a96-131">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="82a96-132">Версия</span><span class="sxs-lookup"><span data-stu-id="82a96-132">Version</span></span><br/> | <span data-ttu-id="82a96-133">Mergemod.dll 1,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="82a96-133">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="82a96-134">Header</span><span class="sxs-lookup"><span data-stu-id="82a96-134">Header</span></span><br/>  | <dl> <span data-ttu-id="82a96-135"><dt>Мержемод. h</dt></span><span class="sxs-lookup"><span data-stu-id="82a96-135"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="82a96-136">DLL</span><span class="sxs-lookup"><span data-stu-id="82a96-136">DLL</span></span><br/>     | <dl> <span data-ttu-id="82a96-137"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="82a96-137"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 
