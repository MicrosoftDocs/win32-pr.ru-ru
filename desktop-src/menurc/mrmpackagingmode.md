---
title: Перечисление Мрмпаккагингмоде (Мрмресаурцеиндексер. h)
description: Определяет константы, которые определяют тип PRI-файлов, создаваемых Мрмкреатересаурцефиле и Мрмкреатересаурцефилеинмемори.
ms.assetid: 5695B67E-5446-4538-83D2-F8FF91A5080E
keywords:
- Меню перечисления Мрмпаккагингмоде и другие ресурсы
topic_type:
- apiref
api_name:
- MrmPackagingMode
api_location:
- MrmResourceIndexer.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eaca681dbcf9d171e279083abbb730895ff99333
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340740"
---
# <a name="mrmpackagingmode-enumeration"></a><span data-ttu-id="d46e2-104">Перечисление Мрмпаккагингмоде</span><span class="sxs-lookup"><span data-stu-id="d46e2-104">MrmPackagingMode enumeration</span></span>

<span data-ttu-id="d46e2-105">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="d46e2-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="d46e2-106">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="d46e2-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="d46e2-107">Определяет константы, которые определяют тип PRI-файлов, создаваемых [**мрмкреатересаурцефиле**](mrmcreateresourcefile.md) и [**мрмкреатересаурцефилеинмемори**](mrmcreateresourcefileinmemory.md).</span><span class="sxs-lookup"><span data-stu-id="d46e2-107">Defines constants that specify what kind of PRI file(s) should be created by [**MrmCreateResourceFile**](mrmcreateresourcefile.md) and [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md).</span></span> <span data-ttu-id="d46e2-108">Дополнительные сведения и пошаговые руководства по использованию этих API см. в разделе [пакетные API индексирования ресурсов (PRI) и пользовательские системы сборки](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="d46e2-108">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="d46e2-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d46e2-109">Syntax</span></span>


```C++
typedef enum _MrmPackagingMode { 
  MrmPackagingModeStandaloneFile  = 0,
  MrmPackagingModeAutoSplit       = 1,
  MrmPackagingModeResourcePack    = 2
} MrmPackagingMode;
```



## <a name="constants"></a><span data-ttu-id="d46e2-110">Константы</span><span class="sxs-lookup"><span data-stu-id="d46e2-110">Constants</span></span>

<dl> <dt>

<span data-ttu-id="d46e2-111"><span id="MrmPackagingModeStandaloneFile"></span><span id="mrmpackagingmodestandalonefile"></span><span id="MRMPACKAGINGMODESTANDALONEFILE"></span>**мрмпаккагингмодестандалонефиле**</span><span class="sxs-lookup"><span data-stu-id="d46e2-111"><span id="MrmPackagingModeStandaloneFile"></span><span id="mrmpackagingmodestandalonefile"></span><span id="MRMPACKAGINGMODESTANDALONEFILE"></span>**MrmPackagingModeStandaloneFile**</span></span>
</dt> <dd>

<span data-ttu-id="d46e2-112">Указывает, что должен быть создан один PRI-файл.</span><span class="sxs-lookup"><span data-stu-id="d46e2-112">Specifies that a single PRI file should be created.</span></span>

</dd> <dt>

<span data-ttu-id="d46e2-113"><span id="MrmPackagingModeAutoSplit"></span><span id="mrmpackagingmodeautosplit"></span><span id="MRMPACKAGINGMODEAUTOSPLIT"></span>**мрмпаккагингмодеаутосплит**</span><span class="sxs-lookup"><span data-stu-id="d46e2-113"><span id="MrmPackagingModeAutoSplit"></span><span id="mrmpackagingmodeautosplit"></span><span id="MRMPACKAGINGMODEAUTOSPLIT"></span>**MrmPackagingModeAutoSplit**</span></span>
</dt> <dd>

<span data-ttu-id="d46e2-114">Указывает, что необходимо создать несколько PRI файлов. Разделите автоматически всеми поддерживаемыми квалификаторами (в частности, языком и масштабом).</span><span class="sxs-lookup"><span data-stu-id="d46e2-114">Specifies that multiple PRI files should be created; split automatically by all supported qualifiers (specifically, language and scale).</span></span>

</dd> <dt>

<span data-ttu-id="d46e2-115"><span id="MrmPackagingModeResourcePack"></span><span id="mrmpackagingmoderesourcepack"></span><span id="MRMPACKAGINGMODERESOURCEPACK"></span>**мрмпаккагингмодересаурцепакк**</span><span class="sxs-lookup"><span data-stu-id="d46e2-115"><span id="MrmPackagingModeResourcePack"></span><span id="mrmpackagingmoderesourcepack"></span><span id="MRMPACKAGINGMODERESOURCEPACK"></span>**MrmPackagingModeResourcePack**</span></span>
</dt> <dd>

<span data-ttu-id="d46e2-116">Указывает, что должен быть создан вспомогательный PRI-файл надстройки.</span><span class="sxs-lookup"><span data-stu-id="d46e2-116">Specifies that an add-on satellite PRI file should be created.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d46e2-117">Требования</span><span class="sxs-lookup"><span data-stu-id="d46e2-117">Requirements</span></span>



| <span data-ttu-id="d46e2-118">Требование</span><span class="sxs-lookup"><span data-stu-id="d46e2-118">Requirement</span></span> | <span data-ttu-id="d46e2-119">Значение</span><span class="sxs-lookup"><span data-stu-id="d46e2-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d46e2-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d46e2-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d46e2-121">\[Только для настольных приложений Windows 10 версии 1803\]</span><span class="sxs-lookup"><span data-stu-id="d46e2-121">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="d46e2-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d46e2-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d46e2-123">\[Только классические приложения Windows Server\]</span><span class="sxs-lookup"><span data-stu-id="d46e2-123">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="d46e2-124">Header</span><span class="sxs-lookup"><span data-stu-id="d46e2-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d46e2-125"><dt>Мрмресаурцеиндексер. h</dt></span><span class="sxs-lookup"><span data-stu-id="d46e2-125"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d46e2-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d46e2-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d46e2-127">Интерфейсы API индексирования ресурсов пакета (PRI) и пользовательские системы сборки</span><span class="sxs-lookup"><span data-stu-id="d46e2-127">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

