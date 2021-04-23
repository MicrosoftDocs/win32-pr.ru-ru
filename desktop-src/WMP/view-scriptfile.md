---
title: VIEW. scriptFile
description: Атрибут scriptFile указывает имена файлов сопутствующих файлов JScript.
ms.assetid: c285c467-5ba7-4f46-b316-977e833c3cdd
keywords:
- Просмотреть. scriptFile проигрыватель Windows Media
topic_type:
- apiref
api_name:
- VIEW.scriptFile
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac7f447f1934c2589b7ae52b3a24e2dcb2b1ef7b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648905"
---
# <a name="viewscriptfile"></a><span data-ttu-id="47a67-104">VIEW. scriptFile</span><span class="sxs-lookup"><span data-stu-id="47a67-104">VIEW.scriptFile</span></span>

<span data-ttu-id="47a67-105">Атрибут **scriptFile** указывает имена файлов сопутствующих файлов JScript.</span><span class="sxs-lookup"><span data-stu-id="47a67-105">The **scriptFile** attribute specifies the file names of accompanying JScript files.</span></span>

``` syntax
        elementID.scriptFile
```

## <a name="possible-values"></a><span data-ttu-id="47a67-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="47a67-106">Possible Values</span></span>

<span data-ttu-id="47a67-107">Этот атрибут является **строкой** только для записи и не имеет значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="47a67-107">This attribute is a write-only **String** with no default value.</span></span> <span data-ttu-id="47a67-108">Имена файлов нескольких файлов JScript разделяются точкой с запятой.</span><span class="sxs-lookup"><span data-stu-id="47a67-108">The file names of multiple JScript files are delimited with semicolons.</span></span> <span data-ttu-id="47a67-109">Не должны присутствовать начальные и следующие пробелы и точки с запятой.</span><span class="sxs-lookup"><span data-stu-id="47a67-109">Leading and following spaces and semicolons should not be present.</span></span>

## <a name="remarks"></a><span data-ttu-id="47a67-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="47a67-110">Remarks</span></span>

<span data-ttu-id="47a67-111">Код в указанных файлах может использоваться любым обработчиком событий в представлении.</span><span class="sxs-lookup"><span data-stu-id="47a67-111">The code in the specified files can be used by any event handler in the View.</span></span> <span data-ttu-id="47a67-112">Код, используемый обработчиками событий в нескольких представлениях, может быть помещен в файл с тем же именем, что и файл определения обложки, но с расширением. js, а не с расширением WMS.</span><span class="sxs-lookup"><span data-stu-id="47a67-112">Code that is used by event handlers in multiple Views can be placed in a file with the same name as the skin definition file but with a .js extension instead of a .wms extension.</span></span> <span data-ttu-id="47a67-113">Этот файл загружается автоматически, и его не нужно указывать в файле определения обложки.</span><span class="sxs-lookup"><span data-stu-id="47a67-113">This file is loaded automatically and need not be specified in the skin definition file.</span></span>

## <a name="examples"></a><span data-ttu-id="47a67-114">Примеры</span><span class="sxs-lookup"><span data-stu-id="47a67-114">Examples</span></span>


```C++
<VIEW id="theView" scriptFile="theScript.js">
</VIEW>

```



## <a name="requirements"></a><span data-ttu-id="47a67-115">Требования</span><span class="sxs-lookup"><span data-stu-id="47a67-115">Requirements</span></span>



| <span data-ttu-id="47a67-116">Требование</span><span class="sxs-lookup"><span data-stu-id="47a67-116">Requirement</span></span> | <span data-ttu-id="47a67-117">Значение</span><span class="sxs-lookup"><span data-stu-id="47a67-117">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="47a67-118">Версия</span><span class="sxs-lookup"><span data-stu-id="47a67-118">Version</span></span><br/> | <span data-ttu-id="47a67-119">Проигрыватель Windows Media версии 7,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="47a67-119">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="47a67-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="47a67-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47a67-121">**VIEW, элемент**</span><span class="sxs-lookup"><span data-stu-id="47a67-121">**VIEW Element**</span></span>](view-element.md)
</dt> </dl>

 

 





