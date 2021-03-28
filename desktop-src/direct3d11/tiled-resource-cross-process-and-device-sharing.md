---
title: Мозаичная обработка ресурсов и совместное использование устройств
description: Пулы могут совместно использоваться разными процессами — точно так же как традиционные ресурсы.
ms.assetid: CADE009E-A71E-4ACA-A549-EFCE81F8EAD1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f69c88ec7e56a0ad3f67ca7d219352261af9d60
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104252879"
---
# <a name="tiled-resource-cross-process-and-device-sharing"></a><span data-ttu-id="842f8-103">Мозаичная обработка ресурсов и совместное использование устройств</span><span class="sxs-lookup"><span data-stu-id="842f8-103">Tiled resource cross process and device sharing</span></span>

<span data-ttu-id="842f8-104">Пулы могут совместно использоваться разными процессами — точно так же как традиционные ресурсы.</span><span class="sxs-lookup"><span data-stu-id="842f8-104">Tile pools can be shared with other processes just like traditional resources.</span></span> <span data-ttu-id="842f8-105">Мозаичные ресурсы, ссылающиеся на пулы плиток, нельзя совместно использовать на устройствах и процессах.</span><span class="sxs-lookup"><span data-stu-id="842f8-105">Tiled resources that reference tile pools can't be shared across devices and processes.</span></span> <span data-ttu-id="842f8-106">Но отдельные процессы могут создавать собственные мозаичные ресурсы, которые сопоставляются с пулами мозаичных элементов, которые являются общими для этих ресурсов.</span><span class="sxs-lookup"><span data-stu-id="842f8-106">But separate processes can create their own tiled resources that map to tile pools that are shared between those tiled resources.</span></span>

<span data-ttu-id="842f8-107">Размер общих пулов плиток изменить нельзя.</span><span class="sxs-lookup"><span data-stu-id="842f8-107">Shared tile pools can't be resized.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="842f8-108">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="842f8-108">In this section</span></span>



| <span data-ttu-id="842f8-109">Раздел</span><span class="sxs-lookup"><span data-stu-id="842f8-109">Topic</span></span>                                                                                                                   | <span data-ttu-id="842f8-110">Описание</span><span class="sxs-lookup"><span data-stu-id="842f8-110">Description</span></span>                                                                     |
|-------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [<span data-ttu-id="842f8-111">Форматы трафаретов не поддерживаются для мозаичных ресурсов</span><span class="sxs-lookup"><span data-stu-id="842f8-111">Stencil formats not supported with tiled resources</span></span>](stencil-formats-not-supported-with-tiled-resources.md)<br/> | <span data-ttu-id="842f8-112">Форматы, содержащие набор элементов, не поддерживаются для мозаичных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="842f8-112">Formats that contain stencil aren't supported with tiled resources.</span></span> <br/> |



 

## <a name="related-topics"></a><span data-ttu-id="842f8-113">См. также</span><span class="sxs-lookup"><span data-stu-id="842f8-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="842f8-114">Создание мозаичных ресурсов</span><span class="sxs-lookup"><span data-stu-id="842f8-114">Creating tiled resources</span></span>](creating-tiled-resources.md)
</dt> </dl>

 

 





