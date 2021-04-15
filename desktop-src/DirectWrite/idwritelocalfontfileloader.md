---
title: Интерфейс Идврителокалфонтфилелоадер
description: Встроенная реализация интерфейса Идвритефонтфилелоадер, которая работает с локальными файлами шрифтов и предоставляет сведения о файле локального шрифта из ключа ссылки на файл шрифта.
ms.assetid: acb777c8-24c6-452e-8f58-8fb2ad8c0b6c
keywords:
- Непосредственная запись интерфейса Идврителокалфонтфилелоадер
- Непосредственная запись интерфейса Идврителокалфонтфилелоадер, описание
topic_type:
- apiref
api_name:
- IDWriteLocalFontFileLoader
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c65f537dc2a4a96161a11d85ae0a4e1869a331e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668705"
---
# <a name="idwritelocalfontfileloader-interface"></a><span data-ttu-id="d9047-105">Интерфейс Идврителокалфонтфилелоадер</span><span class="sxs-lookup"><span data-stu-id="d9047-105">IDWriteLocalFontFileLoader interface</span></span>

<span data-ttu-id="d9047-106">Встроенная реализация интерфейса [**идвритефонтфилелоадер**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileloader) , которая работает с локальными файлами шрифтов и предоставляет сведения о файле локального шрифта из ключа ссылки на файл шрифта.</span><span class="sxs-lookup"><span data-stu-id="d9047-106">A built-in implementation of the [**IDWriteFontFileLoader**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileloader) interface, that operates on local font files and exposes local font file information from the font file reference key.</span></span> <span data-ttu-id="d9047-107">Ссылки на файлы шрифтов, созданные с помощью [**креатефонтфилереференце**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createfontfilereference) , используют этот загрузчик файлов шрифтов.</span><span class="sxs-lookup"><span data-stu-id="d9047-107">Font file references created using [**CreateFontFileReference**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createfontfilereference) use this font file loader.</span></span>

## <a name="members"></a><span data-ttu-id="d9047-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="d9047-108">Members</span></span>

<span data-ttu-id="d9047-109">Интерфейс **идврителокалфонтфилелоадер** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="d9047-109">The **IDWriteLocalFontFileLoader** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="d9047-110">**Идврителокалфонтфилелоадер** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="d9047-110">**IDWriteLocalFontFileLoader** also has these types of members:</span></span>

-   [<span data-ttu-id="d9047-111">Методы</span><span class="sxs-lookup"><span data-stu-id="d9047-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="d9047-112">Методы</span><span class="sxs-lookup"><span data-stu-id="d9047-112">Methods</span></span>

<span data-ttu-id="d9047-113">Интерфейс **идврителокалфонтфилелоадер** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="d9047-113">The **IDWriteLocalFontFileLoader** interface has these methods.</span></span>



| <span data-ttu-id="d9047-114">Метод</span><span class="sxs-lookup"><span data-stu-id="d9047-114">Method</span></span>                                                                                  | <span data-ttu-id="d9047-115">Описание</span><span class="sxs-lookup"><span data-stu-id="d9047-115">Description</span></span>                                                                               |
|:----------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d9047-116">**жетфилепасфромкэй**</span><span class="sxs-lookup"><span data-stu-id="d9047-116">**GetFilePathFromKey**</span></span>](idwritelocalfontfileloader-getfilepathfromkey.md)             | <span data-ttu-id="d9047-117">Получает абсолютный путь к файлу шрифта из ключа ссылки на файл шрифта.</span><span class="sxs-lookup"><span data-stu-id="d9047-117">Obtains the absolute font file path from the font file reference key.</span></span><br/>          |
| [<span data-ttu-id="d9047-118">**жетфилепасленгсфромкэй**</span><span class="sxs-lookup"><span data-stu-id="d9047-118">**GetFilePathLengthFromKey**</span></span>](idwritelocalfontfileloader-getfilepathlengthfromkey.md) | <span data-ttu-id="d9047-119">Получает длину абсолютного пути к файлу из ключа ссылки на файл шрифта.</span><span class="sxs-lookup"><span data-stu-id="d9047-119">Obtains the length of the absolute file path from the font file reference key.</span></span><br/> |
| [<span data-ttu-id="d9047-120">**жетластвритетимефромкэй**</span><span class="sxs-lookup"><span data-stu-id="d9047-120">**GetLastWriteTimeFromKey**</span></span>](idwritelocalfontfileloader-getlastwritetimefromkey.md)   | <span data-ttu-id="d9047-121">Получает время последней записи файла из ключа ссылки на файл шрифта.</span><span class="sxs-lookup"><span data-stu-id="d9047-121">Obtains the last write time of the file from the font file reference key.</span></span><br/>      |



 

## <a name="requirements"></a><span data-ttu-id="d9047-122">Требования</span><span class="sxs-lookup"><span data-stu-id="d9047-122">Requirements</span></span>



| <span data-ttu-id="d9047-123">Требование</span><span class="sxs-lookup"><span data-stu-id="d9047-123">Requirement</span></span> | <span data-ttu-id="d9047-124">Значение</span><span class="sxs-lookup"><span data-stu-id="d9047-124">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d9047-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d9047-125">Library</span></span><br/> | <dl> <span data-ttu-id="d9047-126"><dt>Дврите. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d9047-126"><dt>Dwrite.lib</dt></span></span> </dl> |
| <span data-ttu-id="d9047-127">DLL</span><span class="sxs-lookup"><span data-stu-id="d9047-127">DLL</span></span><br/>     | <dl> <span data-ttu-id="d9047-128"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d9047-128"><dt>Dwrite.dll</dt></span></span> </dl> |



 

