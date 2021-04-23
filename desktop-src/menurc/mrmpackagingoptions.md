---
title: Перечисление Мрмпаккагингоптионс (Мрмресаурцеиндексер. h)
description: Определяет константы, указывающие параметры для PRI файла, созданного с помощью Мрмкреатересаурцефиле и Мрмкреатересаурцефилеинмемори.
ms.assetid: 11FADCB2-CE6F-449E-8A85-DA50B52B26D0
keywords:
- Меню перечисления Мрмпаккагингоптионс и другие ресурсы
topic_type:
- apiref
api_name:
- MrmPackagingOptions
api_location:
- MrmResourceIndexer.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9a8b2bee733fe17e91501fe295e5f80be159ec5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105710441"
---
# <a name="mrmpackagingoptions-enumeration"></a><span data-ttu-id="77330-104">Перечисление Мрмпаккагингоптионс</span><span class="sxs-lookup"><span data-stu-id="77330-104">MrmPackagingOptions enumeration</span></span>

<span data-ttu-id="77330-105">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="77330-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="77330-106">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="77330-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="77330-107">Определяет константы, указывающие параметры для PRI файла, созданного с помощью [**мрмкреатересаурцефиле**](mrmcreateresourcefile.md) и [**мрмкреатересаурцефилеинмемори**](mrmcreateresourcefileinmemory.md).</span><span class="sxs-lookup"><span data-stu-id="77330-107">Defines constants that specify options for the PRI file created by [**MrmCreateResourceFile**](mrmcreateresourcefile.md) and [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md).</span></span> <span data-ttu-id="77330-108">Дополнительные сведения и пошаговые руководства по использованию этих API см. в разделе [пакетные API индексирования ресурсов (PRI) и пользовательские системы сборки](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="77330-108">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="77330-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="77330-109">Syntax</span></span>


```C++
typedef enum _MrmPackagingOptions { 
  MrmPackagingOptionsNone                         = 0x00,
  MrmPackagingOptionsOmitSchemaFromResourcePacks  = 0x01,
  MrmPackagingOptionsSplitLanguageVariants        = 0x02
} MrmPackagingOptions;
```



## <a name="constants"></a><span data-ttu-id="77330-110">Константы</span><span class="sxs-lookup"><span data-stu-id="77330-110">Constants</span></span>

<dl> <dt>

<span data-ttu-id="77330-111"><span id="MrmPackagingOptionsNone"></span><span id="mrmpackagingoptionsnone"></span><span id="MRMPACKAGINGOPTIONSNONE"></span>**мрмпаккагингоптионсноне**</span><span class="sxs-lookup"><span data-stu-id="77330-111"><span id="MrmPackagingOptionsNone"></span><span id="mrmpackagingoptionsnone"></span><span id="MRMPACKAGINGOPTIONSNONE"></span>**MrmPackagingOptionsNone**</span></span>
</dt> <dd>

<span data-ttu-id="77330-112">Указывает, что параметры упаковки отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="77330-112">Specifies no packaging options.</span></span>

</dd> <dt>

<span data-ttu-id="77330-113"><span id="MrmPackagingOptionsOmitSchemaFromResourcePacks"></span><span id="mrmpackagingoptionsomitschemafromresourcepacks"></span><span id="MRMPACKAGINGOPTIONSOMITSCHEMAFROMRESOURCEPACKS"></span>**мрмпаккагингоптионсомитсчемафромресаурцепаккс**</span><span class="sxs-lookup"><span data-stu-id="77330-113"><span id="MrmPackagingOptionsOmitSchemaFromResourcePacks"></span><span id="mrmpackagingoptionsomitschemafromresourcepacks"></span><span id="MRMPACKAGINGOPTIONSOMITSCHEMAFROMRESOURCEPACKS"></span>**MrmPackagingOptionsOmitSchemaFromResourcePacks**</span></span>
</dt> <dd>

<span data-ttu-id="77330-114">Указывает, что необходимо создать пакет ресурсов без схемы.</span><span class="sxs-lookup"><span data-stu-id="77330-114">Specifies that a schema-free resource pack should be created.</span></span>

</dd> <dt>

<span data-ttu-id="77330-115"><span id="MrmPackagingOptionsSplitLanguageVariants"></span><span id="mrmpackagingoptionssplitlanguagevariants"></span><span id="MRMPACKAGINGOPTIONSSPLITLANGUAGEVARIANTS"></span>**мрмпаккагингоптионссплитлангуажевариантс**</span><span class="sxs-lookup"><span data-stu-id="77330-115"><span id="MrmPackagingOptionsSplitLanguageVariants"></span><span id="mrmpackagingoptionssplitlanguagevariants"></span><span id="MRMPACKAGINGOPTIONSSPLITLANGUAGEVARIANTS"></span>**MrmPackagingOptionsSplitLanguageVariants**</span></span>
</dt> <dd>

<span data-ttu-id="77330-116">Указывает, что PRI-файл должен автоматически разбиваться всеми поддерживаемыми квалификаторами (в частности, языком и масштабом).</span><span class="sxs-lookup"><span data-stu-id="77330-116">Specifies that the PRI file should be automatically split by all supported qualifiers (specifically, language and scale).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="77330-117">Требования</span><span class="sxs-lookup"><span data-stu-id="77330-117">Requirements</span></span>



| <span data-ttu-id="77330-118">Требование</span><span class="sxs-lookup"><span data-stu-id="77330-118">Requirement</span></span> | <span data-ttu-id="77330-119">Значение</span><span class="sxs-lookup"><span data-stu-id="77330-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="77330-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="77330-120">Minimum supported client</span></span><br/> | <span data-ttu-id="77330-121">\[Только для настольных приложений Windows 10 версии 1803\]</span><span class="sxs-lookup"><span data-stu-id="77330-121">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="77330-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="77330-122">Minimum supported server</span></span><br/> | <span data-ttu-id="77330-123">\[Только классические приложения Windows Server\]</span><span class="sxs-lookup"><span data-stu-id="77330-123">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="77330-124">Header</span><span class="sxs-lookup"><span data-stu-id="77330-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="77330-125"><dt>Мрмресаурцеиндексер. h</dt></span><span class="sxs-lookup"><span data-stu-id="77330-125"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77330-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="77330-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77330-127">Интерфейсы API индексирования ресурсов пакета (PRI) и пользовательские системы сборки</span><span class="sxs-lookup"><span data-stu-id="77330-127">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

