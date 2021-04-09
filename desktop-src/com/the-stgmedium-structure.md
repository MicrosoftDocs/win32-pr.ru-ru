---
title: Структура СТГМЕДИУМ
description: Структура СТГМЕДИУМ
ms.assetid: ff1e1128-d228-45a6-a19d-2875b6c4e003
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86faf52ab93bab39b8413ea2eb6381da24b643b5
ms.sourcegitcommit: 89f99926f946dc6c5ea600fb7c41f6b19ceac516
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/21/2020
ms.locfileid: "104070838"
---
# <a name="the-stgmedium-structure"></a><span data-ttu-id="8df1a-103">Структура СТГМЕДИУМ</span><span class="sxs-lookup"><span data-stu-id="8df1a-103">The STGMEDIUM Structure</span></span>

<span data-ttu-id="8df1a-104">Точно так же, как структура [**форматетк**](/windows/win32/api/objidl/ns-objidl-formatetc) является расширением идентификатора формата буфера обмена Windows, структура [**стгмедиум**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) является улучшением глобального маркера памяти, используемого для перемещения данных.</span><span class="sxs-lookup"><span data-stu-id="8df1a-104">Just as the [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) structure is an enhancement of the Windows clipboard format identifier, so the [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) structure is an improvement of the global memory handle used to transfer the data.</span></span> <span data-ttu-id="8df1a-105">Структура **стгмедиум** включает член, **тимед**, указывающий используемый носитель, а также объединение, включающее в себя указатели и маркер для получения указанного среднего уровня в **тимед**.</span><span class="sxs-lookup"><span data-stu-id="8df1a-105">The **STGMEDIUM** structure includes a member, **tymed**, which indicates the medium to be used, and a union comprising pointers and a handle for getting whichever medium is specified in **tymed**.</span></span>

<span data-ttu-id="8df1a-106">Структура [**стгмедиум**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) позволяет как источникам данных, так и потребителям выбирать наиболее эффективный носитель Exchange на основе для отрисовки.</span><span class="sxs-lookup"><span data-stu-id="8df1a-106">The [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) structure enables both data sources and consumers to choose the most efficient exchange medium on a per-rendering basis.</span></span> <span data-ttu-id="8df1a-107">Если данные настолько велики, что они должны храниться на диске, источник данных может указывать на дисковый носитель в предпочтительном формате, а только использовать глобальную память в качестве резервной копии, если это единственный носитель, распознаваемый потребителем.</span><span class="sxs-lookup"><span data-stu-id="8df1a-107">If the data is so large that it should be kept on disk, the data source can indicate a disk-based medium in its preferred format, only using global memory as a backup if that's the only medium the consumer understands.</span></span> <span data-ttu-id="8df1a-108">Возможность использовать лучший носитель для Exchange, так как по умолчанию повышается общая производительность обмена данными между приложениями.</span><span class="sxs-lookup"><span data-stu-id="8df1a-108">Being able to use the best medium for exchanges as the default improves overall performance of data exchange between applications.</span></span> <span data-ttu-id="8df1a-109">Например, если часть данных, подлежащей передаче, уже находится на диске, исходное приложение может переместить или скопировать его в новое место назначения либо в том же приложении, либо в другом, не загружая данные в глобальную память.</span><span class="sxs-lookup"><span data-stu-id="8df1a-109">For example, if some of the data to be transferred is already on disk, the source application can move or copy it to a new destination, either in the same application or in some other, without having first to load the data into global memory.</span></span> <span data-ttu-id="8df1a-110">На стороне получателя данные не нужно записывать обратно на диск.</span><span class="sxs-lookup"><span data-stu-id="8df1a-110">At the receiving end, the consumer of the data does not have to write it back to disk.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8df1a-111">См. также</span><span class="sxs-lookup"><span data-stu-id="8df1a-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8df1a-112">Форматы данных и передачи мультимедиа</span><span class="sxs-lookup"><span data-stu-id="8df1a-112">Data Formats and Transfer Media</span></span>](data-formats-and-transfer-media.md)
</dt> </dl>

 

 




