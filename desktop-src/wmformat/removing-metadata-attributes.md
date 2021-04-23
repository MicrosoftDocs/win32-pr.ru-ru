---
title: Удаление атрибутов метаданных
description: Удаление атрибутов метаданных
ms.assetid: 44546091-406f-4ae6-914a-942d1b89e0e4
keywords:
- Windows Media Format SDK, удаление атрибутов метаданных
- Расширенный системный формат (ASF), удаление атрибутов метаданных
- ASF (Расширенный системный формат), удаление атрибутов метаданных
- метаданные, удаление атрибутов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25b10176452dcc78cc3eca898b61c350a157e568
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2020
ms.locfileid: "104412693"
---
# <a name="removing-metadata-attributes"></a><span data-ttu-id="563ea-107">Удаление атрибутов метаданных</span><span class="sxs-lookup"><span data-stu-id="563ea-107">Removing Metadata Attributes</span></span>

<span data-ttu-id="563ea-108">Атрибут метаданных можно удалить, передав его индекс и номер потока в метод [**IWMHeaderInfo3::D елетеаттрибуте**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-deleteattribute) .</span><span class="sxs-lookup"><span data-stu-id="563ea-108">You can remove a metadata attribute by passing its index and stream number to the [**IWMHeaderInfo3::DeleteAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-deleteattribute) method.</span></span> <span data-ttu-id="563ea-109">Порядок, в котором оставшиеся атрибуты индексируются после удаления атрибута, не изменяется. все оставшиеся атрибуты, для которых изначально было задано значение индекса больше, чем у удаляемого значения индекса, уменьшаются на один.</span><span class="sxs-lookup"><span data-stu-id="563ea-109">The order in which the remaining attributes are indexed after removing an attribute does not change; all remaining attributes that originally had an index value greater than the one removed have their index values reduced by one.</span></span> <span data-ttu-id="563ea-110">При удалении нескольких атрибутов сделайте это в порядке убывания по индексу, чтобы не вычислять коррекцию при индексировании.</span><span class="sxs-lookup"><span data-stu-id="563ea-110">When removing multiple attributes, do so in descending order by index to avoid having to calculate the adjustment in indexing.</span></span>

<span data-ttu-id="563ea-111">Для удобства удаления значений метод [**IWMHeaderInfo3:: жетаттрибутеиндицес**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributeindices) возвращает значения индекса в порядке убывания.</span><span class="sxs-lookup"><span data-stu-id="563ea-111">For convenience in removing values, the [**IWMHeaderInfo3::GetAttributeIndices**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributeindices) method returns the index values in descending order.</span></span>

> [!Note]  
> <span data-ttu-id="563ea-112">Значения индекса, полученные с помощью методов [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) , несовместимы со значениями индекса, полученными с помощью методов [**ивмхеадеринфо**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo).</span><span class="sxs-lookup"><span data-stu-id="563ea-112">Index values obtained by using the methods of [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) are not compatible with index values obtained by using the methods of [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo).</span></span> <span data-ttu-id="563ea-113">При использовании методов одного интерфейса для изменения атрибутов в файле следует предположить, что все значения индекса, ранее извлеченные из другого интерфейса, больше не являются допустимыми и должны быть получены снова.</span><span class="sxs-lookup"><span data-stu-id="563ea-113">If you use the methods of one interface to change attributes in a file, you should assume that any index values previously retrieved from the other interface are no longer valid and must be obtained again.</span></span> <span data-ttu-id="563ea-114">По возможности следует избегать использования методов **ивмхеадеринфо** .</span><span class="sxs-lookup"><span data-stu-id="563ea-114">You should avoid using the methods of **IWMHeaderInfo** if possible.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="563ea-115">См. также</span><span class="sxs-lookup"><span data-stu-id="563ea-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="563ea-116">**Работа с метаданными**</span><span class="sxs-lookup"><span data-stu-id="563ea-116">**Working with Metadata**</span></span>](working-with-metadata.md)
</dt> </dl>

 

 




