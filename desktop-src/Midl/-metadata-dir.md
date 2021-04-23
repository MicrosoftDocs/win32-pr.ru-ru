---
title: параметр/metadata_dir (MIDLRT)
description: '\_Параметр dir/Метадата указывает один или несколько каталогов, содержащих файлы метаданных платформы.'
ms.assetid: 578b9d3f-3ee6-4978-9d2a-0c5aee561a30
keywords:
- /metadata_dir параметр MIDL
topic_type:
- apiref
api_name:
- /metadata_dir
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72781641323aa61ae75da256f84f8c1debfd6556
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679772"
---
# <a name="metadata_dir-switch-midlrt"></a><span data-ttu-id="68b5a-104">параметр/metadata_dir (MIDLRT)</span><span class="sxs-lookup"><span data-stu-id="68b5a-104">/metadata_dir switch (MIDLRT)</span></span>

<span data-ttu-id="68b5a-105">Параметр **\_ dir/Метадата** указывает один или несколько каталогов, содержащих файлы метаданных платформы.</span><span class="sxs-lookup"><span data-stu-id="68b5a-105">The **/metadata\_dir** switch specifies one or more directories that contain platform metadata files.</span></span>

``` syntax
midlrt /metadata_dir metadata_directory
```

## <a name="switch-options"></a><span data-ttu-id="68b5a-106">Параметры коммутатора</span><span class="sxs-lookup"><span data-stu-id="68b5a-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="68b5a-107">*\_Каталог метаданных*</span><span class="sxs-lookup"><span data-stu-id="68b5a-107">*metadata\_directory*</span></span> 
</dt> <dd>

<span data-ttu-id="68b5a-108">Указывает один или несколько каталогов, содержащих файлы метаданных платформы.</span><span class="sxs-lookup"><span data-stu-id="68b5a-108">Specifies one or more directories that contain platform metadata files.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="68b5a-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="68b5a-109">Remarks</span></span>

<span data-ttu-id="68b5a-110">Используйте этот параметр, чтобы указать расположение основного файла метаданных для Windows, который называется Windows. winmd.</span><span class="sxs-lookup"><span data-stu-id="68b5a-110">Use this switch to specify the location of the main metadata file for Windows, which is named windows.winmd.</span></span>

## <a name="examples"></a><span data-ttu-id="68b5a-111">Примеры</span><span class="sxs-lookup"><span data-stu-id="68b5a-111">Examples</span></span>

<span data-ttu-id="68b5a-112">**midlrt/Метадата \_ dir dir1 Dir2**</span><span class="sxs-lookup"><span data-stu-id="68b5a-112">**midlrt /metadata\_dir dir1 dir2**</span></span>

## <a name="requirements"></a><span data-ttu-id="68b5a-113">Требования</span><span class="sxs-lookup"><span data-stu-id="68b5a-113">Requirements</span></span>



| <span data-ttu-id="68b5a-114">Требование</span><span class="sxs-lookup"><span data-stu-id="68b5a-114">Requirement</span></span> | <span data-ttu-id="68b5a-115">Значение</span><span class="sxs-lookup"><span data-stu-id="68b5a-115">Value</span></span> |
|-------------------|--------------------------------|
| <span data-ttu-id="68b5a-116">Клиент</span><span class="sxs-lookup"><span data-stu-id="68b5a-116">Client</span></span><br/> | <span data-ttu-id="68b5a-117">Windows 8</span><span class="sxs-lookup"><span data-stu-id="68b5a-117">Windows 8</span></span><br/>           |
| <span data-ttu-id="68b5a-118">Сервер</span><span class="sxs-lookup"><span data-stu-id="68b5a-118">Server</span></span><br/> | <span data-ttu-id="68b5a-119">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="68b5a-119">Windows Server 2012</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="68b5a-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="68b5a-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68b5a-121">Общий синтаксис командной строки MIDL</span><span class="sxs-lookup"><span data-stu-id="68b5a-121">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> </dl>

 

 





