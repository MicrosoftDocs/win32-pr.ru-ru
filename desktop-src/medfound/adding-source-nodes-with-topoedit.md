---
description: Добавление исходных узлов с помощью Топоедит
ms.assetid: f42227eb-a988-4eaa-9c18-b3ac270cd7a2
title: Добавление исходных узлов с помощью Топоедит
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b12456e76f64d44d9c335dec1ea171c732e4040c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701617"
---
# <a name="adding-source-nodes-with-topoedit"></a><span data-ttu-id="3444d-103">Добавление исходных узлов с помощью Топоедит</span><span class="sxs-lookup"><span data-stu-id="3444d-103">Adding Source Nodes with TopoEdit</span></span>

<span data-ttu-id="3444d-104">Исходный узел представляет поток в файле мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="3444d-104">A source node represents a stream in a media file.</span></span> <span data-ttu-id="3444d-105">Чтобы создать исходный узел в Топоедит, укажите файл мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="3444d-105">To create a source node in TopoEdit, you specify a media file.</span></span> <span data-ttu-id="3444d-106">Топоедит перечисляет потоки в файле и создает соответствующие исходные узлы.</span><span class="sxs-lookup"><span data-stu-id="3444d-106">TopoEdit enumerates the streams in the file and creates the appropriate source nodes.</span></span>

<span data-ttu-id="3444d-107">Сведения о добавлении исходных узлов программным путем с помощью Media Foundation API-интерфейсов см. в разделе [Создание исходных узлов](creating-source-nodes.md).</span><span class="sxs-lookup"><span data-stu-id="3444d-107">For information about adding source nodes programmatically by using Media Foundation APIs, see [Creating Source Nodes](creating-source-nodes.md).</span></span>

## <a name="to-add-a-source-node-to-a-topology"></a><span data-ttu-id="3444d-108">Добавление исходного узла в топологию</span><span class="sxs-lookup"><span data-stu-id="3444d-108">To add a source node to a topology</span></span>

1.  <span data-ttu-id="3444d-109">В меню **топология** выберите команду **Добавить источник**.</span><span class="sxs-lookup"><span data-stu-id="3444d-109">On the **Topology** menu, click **Add Source**.</span></span>

    <span data-ttu-id="3444d-110">Откроется диалоговое окно **Выбор источника носителя** .</span><span class="sxs-lookup"><span data-stu-id="3444d-110">The **Select Media Source** dialog box opens.</span></span>

2.  <span data-ttu-id="3444d-111">Перейдите к папке, в которой находится файл мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="3444d-111">Navigate to the folder where the media file is located.</span></span>

3.  <span data-ttu-id="3444d-112">В поле **имя файла:** введите имя файла.</span><span class="sxs-lookup"><span data-stu-id="3444d-112">In the **File name:** field, enter the name of the file.</span></span>

4.  <span data-ttu-id="3444d-113">Нажмите кнопку **Открыть**.</span><span class="sxs-lookup"><span data-stu-id="3444d-113">Click **Open**.</span></span>

<span data-ttu-id="3444d-114">Топоедит создает исходные узлы для потоков.</span><span class="sxs-lookup"><span data-stu-id="3444d-114">TopoEdit creates source nodes for the streams.</span></span> <span data-ttu-id="3444d-115">На **панели топология** отображается исходный узел, содержащийся в сером поле, в котором отображается имя файла мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="3444d-115">The **Topology Pane** shows the source node contained in a grey box that shows the name of the media file.</span></span> <span data-ttu-id="3444d-116">Исходный узел показывает тип потока узла.</span><span class="sxs-lookup"><span data-stu-id="3444d-116">The source node shows the stream type of the node.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3444d-117">См. также</span><span class="sxs-lookup"><span data-stu-id="3444d-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3444d-118">Создание топологий с помощью Топоедит</span><span class="sxs-lookup"><span data-stu-id="3444d-118">Building Topologies by Using TopoEdit</span></span>](building-topologies-by-using-topoedit.md)
</dt> <dt>

[<span data-ttu-id="3444d-119">топоедит</span><span class="sxs-lookup"><span data-stu-id="3444d-119">TopoEdit</span></span>](topoedit.md)
</dt> </dl>

 

 



