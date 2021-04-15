---
title: Изменение атрибутов метаданных
description: Изменение атрибутов метаданных
ms.assetid: 96c979e2-c616-45e3-9c60-a24f03e29dc4
keywords:
- Windows Media Format SDK, изменение атрибутов метаданных
- Расширенный системный формат (ASF), изменение атрибутов метаданных
- ASF (Расширенный системный формат), изменение атрибутов метаданных
- метаданные, изменение атрибутов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a52990e5366da178e9ed5021af93a9f6403b80c4
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "104412562"
---
# <a name="editing-metadata-attributes"></a><span data-ttu-id="15567-107">Изменение атрибутов метаданных</span><span class="sxs-lookup"><span data-stu-id="15567-107">Editing Metadata Attributes</span></span>

<span data-ttu-id="15567-108">Изменение атрибутов метаданных очень похоже на установку новых.</span><span class="sxs-lookup"><span data-stu-id="15567-108">Editing metadata attributes is very similar to setting new ones.</span></span> <span data-ttu-id="15567-109">Вместо использования [**IWMHeaderInfo3:: аддаттрибуте**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addattribute)используйте [**IWMHeaderInfo3:: модифяттрибуте**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-modifyattribute).</span><span class="sxs-lookup"><span data-stu-id="15567-109">Instead of using [**IWMHeaderInfo3::AddAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addattribute), use [**IWMHeaderInfo3::ModifyAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-modifyattribute).</span></span> <span data-ttu-id="15567-110">**Модифяттрибуте** идентичен **аддаттрибуте** , за исключением того, что не указывается имя атрибута, а номер индекса является входным параметром, а не выходным.</span><span class="sxs-lookup"><span data-stu-id="15567-110">**ModifyAttribute** is identical to **AddAttribute** except that you do not specify an attribute name, and the index number is an input parameter instead of an output.</span></span>

<span data-ttu-id="15567-111">Можно использовать потоковый номер 0xFFFF, чтобы указать атрибут для изменения с помощью его глобального индекса.</span><span class="sxs-lookup"><span data-stu-id="15567-111">You can use stream number 0xFFFF to specify an attribute to modify using its global index.</span></span>

## <a name="related-topics"></a><span data-ttu-id="15567-112">См. также</span><span class="sxs-lookup"><span data-stu-id="15567-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="15567-113">**Работа с метаданными**</span><span class="sxs-lookup"><span data-stu-id="15567-113">**Working with Metadata**</span></span>](working-with-metadata.md)
</dt> </dl>

 

 




