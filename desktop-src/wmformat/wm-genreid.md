---
title: WM/GenreID
description: Атрибут WM/GenreID содержит идентификатор жанра, соответствующий содержимому тега ТКОН в ID3v2.
ms.assetid: 2f2a87f7-ba2d-465a-a36b-a8f58b5dd2d0
keywords:
- Формат Windows Media WM/GenreID
topic_type:
- apiref
api_name:
- WM/GenreID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a3b25dffe69471f47eaf20124af48141835540f
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104411983"
---
# <a name="wmgenreid"></a><span data-ttu-id="3dc70-104">WM/GenreID</span><span class="sxs-lookup"><span data-stu-id="3dc70-104">WM/GenreID</span></span>

<span data-ttu-id="3dc70-105">Атрибут **WM/GenreID** содержит идентификатор жанра, соответствующий содержимому тега Ткон в ID3v2.</span><span class="sxs-lookup"><span data-stu-id="3dc70-105">The **WM/GenreID** attribute contains a genre identifier compliant with the contents of the TCON tag in ID3v2.</span></span> <span data-ttu-id="3dc70-106">Он должен содержать идентификатор жанра в круглых скобках, при необходимости за которым следует уточнение, описывающее жанр.</span><span class="sxs-lookup"><span data-stu-id="3dc70-106">This should contain the genre ID in parentheses, optionally followed by a refinement further describing the genre.</span></span> <span data-ttu-id="3dc70-107">Дополнительные сведения см. в спецификации ID3v2.</span><span class="sxs-lookup"><span data-stu-id="3dc70-107">For more information, refer to the ID3v2 specification.</span></span>

## <a name="global-constant"></a><span data-ttu-id="3dc70-108">Глобальная константа</span><span class="sxs-lookup"><span data-stu-id="3dc70-108">Global Constant</span></span>

<span data-ttu-id="3dc70-109">g \_ всзвмженреид</span><span class="sxs-lookup"><span data-stu-id="3dc70-109">g\_wszWMGenreID</span></span>

## <a name="data-type"></a><span data-ttu-id="3dc70-110">Тип данных</span><span class="sxs-lookup"><span data-stu-id="3dc70-110">Data Type</span></span>

<span data-ttu-id="3dc70-111">**\_Строка типа \_ ВМТ**</span><span class="sxs-lookup"><span data-stu-id="3dc70-111">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="3dc70-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3dc70-112">Remarks</span></span>

<span data-ttu-id="3dc70-113">Предпочтительным атрибутом для указания жанра является [**WM/жанр**](wm-genre.md).</span><span class="sxs-lookup"><span data-stu-id="3dc70-113">The preferred attribute for specifying a genre is [**WM/Genre**](wm-genre.md).</span></span> <span data-ttu-id="3dc70-114">Используйте его в качестве предпочтения к этому атрибуту.</span><span class="sxs-lookup"><span data-stu-id="3dc70-114">Use it in preference to this attribute.</span></span>

<span data-ttu-id="3dc70-115">Если изменить файл **WM/жанр** или **WM/GENREID** в файле MP3, то другой атрибут будет изменен на Match.</span><span class="sxs-lookup"><span data-stu-id="3dc70-115">If you change either **WM/Genre** or **WM/GenreID** in an MP3 file, the other attribute will be changed to match.</span></span>

### <a name="example"></a><span data-ttu-id="3dc70-116">Пример</span><span class="sxs-lookup"><span data-stu-id="3dc70-116">Example</span></span>



| <span data-ttu-id="3dc70-117">Тип файла</span><span class="sxs-lookup"><span data-stu-id="3dc70-117">File type</span></span> | <span data-ttu-id="3dc70-118">Пример значения</span><span class="sxs-lookup"><span data-stu-id="3dc70-118">Example value</span></span>   |
|-----------|-----------------|
| <span data-ttu-id="3dc70-119">звук;</span><span class="sxs-lookup"><span data-stu-id="3dc70-119">Audio</span></span>     | <span data-ttu-id="3dc70-120">"(4) еуродиско"</span><span class="sxs-lookup"><span data-stu-id="3dc70-120">"(4) Eurodisco"</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="3dc70-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3dc70-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3dc70-122">**Список атрибутов**</span><span class="sxs-lookup"><span data-stu-id="3dc70-122">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




