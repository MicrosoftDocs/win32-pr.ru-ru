---
title: Пользовательские метаданные
description: Пользовательские метаданные
ms.assetid: 86132163-da56-416a-9539-874d18972932
keywords:
- Windows Media Format SDK, пользовательские метаданные
- Расширенный системный формат (ASF), пользовательские метаданные
- ASF (Расширенный системный формат), пользовательские метаданные
- Windows Media Format SDK, интерфейс IWMHeaderInfo3
- Расширенный системный формат (ASF), интерфейс IWMHeaderInfo3
- ASF (Расширенный системный формат), интерфейс IWMHeaderInfo3
- метаданные, Настройка
- IWMHeaderInfo3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a795ab184e5bd6120278f61c0d3654679fd79c28
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/21/2020
ms.locfileid: "103789168"
---
# <a name="custom-metadata"></a><span data-ttu-id="f582d-111">Пользовательские метаданные</span><span class="sxs-lookup"><span data-stu-id="f582d-111">Custom Metadata</span></span>

<span data-ttu-id="f582d-112">Помимо множества поддерживаемых атрибутов, предоставляемых с помощью пакета SDK Windows Media Format, можно создавать атрибуты метаданных для собственных спецификаций.</span><span class="sxs-lookup"><span data-stu-id="f582d-112">In addition to the many supported attributes provided with the Windows Media Format SDK, you can create metadata attributes to your own specifications.</span></span> <span data-ttu-id="f582d-113">При создании пользовательских атрибутов метаданных следует использовать легко узнаваемое соглашение об именовании, чтобы избежать возможного конфликта с атрибутами, созданными другими пользователями.</span><span class="sxs-lookup"><span data-stu-id="f582d-113">When creating custom metadata attributes, you should use an easily identifiable naming convention to avoid possible conflict with attributes created by others.</span></span>

<span data-ttu-id="f582d-114">Рекомендуется использовать методы [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) для создания метаданных из-за дополнительной гибкости, предоставляемой методам [**ивмхеадеринфо**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo).</span><span class="sxs-lookup"><span data-stu-id="f582d-114">It is recommended that you use the methods of [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) to create your metadata because of the added flexibility they provide over the methods of [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f582d-115">См. также</span><span class="sxs-lookup"><span data-stu-id="f582d-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f582d-116">**Атрибуты**</span><span class="sxs-lookup"><span data-stu-id="f582d-116">**Attributes**</span></span>](attributes.md)
</dt> <dt>

[<span data-ttu-id="f582d-117">**Компоненты метаданных**</span><span class="sxs-lookup"><span data-stu-id="f582d-117">**Metadata Features**</span></span>](metadata-features.md)
</dt> <dt>

[<span data-ttu-id="f582d-118">**Работа с метаданными**</span><span class="sxs-lookup"><span data-stu-id="f582d-118">**Working with Metadata**</span></span>](working-with-metadata.md)
</dt> </dl>

 

 




