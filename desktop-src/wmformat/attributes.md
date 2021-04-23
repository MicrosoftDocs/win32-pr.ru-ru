---
title: Атрибуты (пакет SDK для Windows Media Format 11)
description: Атрибуты
ms.assetid: 1e9392b4-4fff-41ad-9d80-23c1c7f9e9a4
keywords:
- Windows Media Format SDK, атрибуты
- Расширенный системный формат (ASF), атрибуты
- ASF (Расширенный системный формат), атрибуты
- атрибуты, сведения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c209558ed4803fee96e9b482302af1864cbf988b
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "104414561"
---
# <a name="attributes-windows-media-format-11-sdk"></a><span data-ttu-id="91a3c-107">Атрибуты (пакет SDK для Windows Media Format 11)</span><span class="sxs-lookup"><span data-stu-id="91a3c-107">Attributes (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="91a3c-108">Атрибут — это отдельный элемент метаданных.</span><span class="sxs-lookup"><span data-stu-id="91a3c-108">An attribute is an individual item of metadata.</span></span> <span data-ttu-id="91a3c-109">Большая часть атрибутов может быть задана приложением и записывается в заголовок файла ASF.</span><span class="sxs-lookup"><span data-stu-id="91a3c-109">Most of the attributes can be set by your application and are written to the header of an ASF file.</span></span>

<span data-ttu-id="91a3c-110">Некоторые предопределенные атрибуты являются запрограммированными атрибутами.</span><span class="sxs-lookup"><span data-stu-id="91a3c-110">Some of the predefined attributes are coded attributes.</span></span> <span data-ttu-id="91a3c-111">Эти атрибуты не хранятся в заголовке ASF-файла, но вычисляются объектами пакета SDK Windows Media Format при загрузке файла.</span><span class="sxs-lookup"><span data-stu-id="91a3c-111">These attributes are not stored in the header of an ASF file, but are computed by the objects of the Windows Media Format SDK when the file is loaded.</span></span> <span data-ttu-id="91a3c-112">Поскольку закодированные атрибуты всегда вычисляются, они по сути являются доступны только для чтения.</span><span class="sxs-lookup"><span data-stu-id="91a3c-112">Because coded attributes are always computed, they are inherently read-only.</span></span>

<span data-ttu-id="91a3c-113">Этот пакет SDK включает множество определений атрибутов, которые можно использовать.</span><span class="sxs-lookup"><span data-stu-id="91a3c-113">This SDK includes many attribute definitions that you can use.</span></span> <span data-ttu-id="91a3c-114">Вы также можете создавать собственные атрибуты для описания содержимого.</span><span class="sxs-lookup"><span data-stu-id="91a3c-114">You can also create attributes of your own to describe content.</span></span>

<span data-ttu-id="91a3c-115">В следующих разделах описываются предопределенные атрибуты.</span><span class="sxs-lookup"><span data-stu-id="91a3c-115">The following sections describe the predefined attributes.</span></span>



| <span data-ttu-id="91a3c-116">Section</span><span class="sxs-lookup"><span data-stu-id="91a3c-116">Section</span></span>                                                                | <span data-ttu-id="91a3c-117">Описание</span><span class="sxs-lookup"><span data-stu-id="91a3c-117">Description</span></span>                                                                                                                                                                                           |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="91a3c-118">Список атрибутов</span><span class="sxs-lookup"><span data-stu-id="91a3c-118">Attribute List</span></span>](attribute-list.md)                                   | <span data-ttu-id="91a3c-119">Предоставляет алфавитный список всех предопределенных атрибутов.</span><span class="sxs-lookup"><span data-stu-id="91a3c-119">Provides an alphabetical list of all of the predefined attributes.</span></span> <span data-ttu-id="91a3c-120">После списка каждый атрибут описан отдельно.</span><span class="sxs-lookup"><span data-stu-id="91a3c-120">After the list, each attribute is described individually.</span></span>                                                                          |
| [<span data-ttu-id="91a3c-121">Атрибуты с несколькими значениями</span><span class="sxs-lookup"><span data-stu-id="91a3c-121">Attributes with Multiple Values</span></span>](attributes-with-multiple-values.md) | <span data-ttu-id="91a3c-122">Список атрибутов, которые могут быть добавлены в файл несколько раз.</span><span class="sxs-lookup"><span data-stu-id="91a3c-122">Lists the attributes that can be added to a file more than once.</span></span>                                                                                                                                      |
| [<span data-ttu-id="91a3c-123">Атрибуты по типу</span><span class="sxs-lookup"><span data-stu-id="91a3c-123">Attributes By Type</span></span>](attributes-by-type.md)                           | <span data-ttu-id="91a3c-124">Содержит списки атрибутов, отсортированных по типу.</span><span class="sxs-lookup"><span data-stu-id="91a3c-124">Contains lists of attributes sorted by type.</span></span> <span data-ttu-id="91a3c-125">К ним относятся списки специальных атрибутов (таких как работа с цифровыми правами) и списки рекомендуемых атрибутов по типу содержимого.</span><span class="sxs-lookup"><span data-stu-id="91a3c-125">These include lists of special-purpose attributes (like those dealing with digital rights management) and lists of suggested attributes by content type.</span></span> |
| [<span data-ttu-id="91a3c-126">Поддержка тегов ID3</span><span class="sxs-lookup"><span data-stu-id="91a3c-126">ID3 Tag Support</span></span>](id3-tag-support.md)                                 | <span data-ttu-id="91a3c-127">Список атрибутов, совместимых с тегами ID3.</span><span class="sxs-lookup"><span data-stu-id="91a3c-127">Lists the attributes that are compatible with ID3 tags.</span></span>                                                                                                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="91a3c-128">См. также</span><span class="sxs-lookup"><span data-stu-id="91a3c-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="91a3c-129">**Ивмхеадеринфо:: Жетаттрибутебиндекс**</span><span class="sxs-lookup"><span data-stu-id="91a3c-129">**IWMHeaderInfo::GetAttributeByIndex**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getattributebyindex)
</dt> <dt>

[<span data-ttu-id="91a3c-130">**Ивмхеадеринфо:: Жетаттрибутебинаме**</span><span class="sxs-lookup"><span data-stu-id="91a3c-130">**IWMHeaderInfo::GetAttributeByName**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getattributebyname)
</dt> <dt>

[<span data-ttu-id="91a3c-131">**Ивмхеадеринфо:: SetAttribute**</span><span class="sxs-lookup"><span data-stu-id="91a3c-131">**IWMHeaderInfo::SetAttribute**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute)
</dt> <dt>

[<span data-ttu-id="91a3c-132">**Работа с метаданными**</span><span class="sxs-lookup"><span data-stu-id="91a3c-132">**Working with Metadata**</span></span>](working-with-metadata.md)
</dt> </dl>

 

 




