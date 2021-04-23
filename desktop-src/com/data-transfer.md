---
title: Передача данных
description: Передача данных
ms.assetid: 26b16438-f940-4086-869e-74021ed00b1e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37dee268b99f205e0093288f6980c8425220a45b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104532450"
---
# <a name="data-transfer"></a><span data-ttu-id="38121-103">Передача данных</span><span class="sxs-lookup"><span data-stu-id="38121-103">Data Transfer</span></span>

<span data-ttu-id="38121-104">Модель COM предоставляет стандартный механизм передачи данных между приложениями.</span><span class="sxs-lookup"><span data-stu-id="38121-104">The Component Object Model (COM) provides a standard mechanism for transferring data between applications.</span></span> <span data-ttu-id="38121-105">Этот механизм является *объектом данных*, который представляет собой любой COM-объект, реализующий интерфейс [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) .</span><span class="sxs-lookup"><span data-stu-id="38121-105">This mechanism is the *data object*, which is simply any COM object that implements the [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) interface.</span></span> <span data-ttu-id="38121-106">Некоторые объекты данных, например фрагмент текста, скопированного в буфер обмена, имеют интерфейс **IDataObject** в качестве единственного интерфейса.</span><span class="sxs-lookup"><span data-stu-id="38121-106">Some data objects, such as a piece of text copied to the clipboard, have **IDataObject** as their sole interface.</span></span> <span data-ttu-id="38121-107">Другие, такие как объекты составного документа, предоставляют несколько интерфейсов, для которых в качестве интерфейса **IDataObject** используется только один.</span><span class="sxs-lookup"><span data-stu-id="38121-107">Others, such as compound document objects, expose several interfaces, of which **IDataObject** is simply one.</span></span> <span data-ttu-id="38121-108">Объекты данных являются фундаментальными для работы с составными документами, хотя они также имеют широкое приложение вне этой технологии OLE.</span><span class="sxs-lookup"><span data-stu-id="38121-108">Data objects are fundamental to the working of compound documents, although they also have widespread application outside that OLE technology.</span></span>

<span data-ttu-id="38121-109">Благодаря обмену указателями на объект данных поставщики и потребители данных могут управлять передачей данных единообразно, независимо от формата данных, типа носителя, используемого для передачи данных, или целевого устройства, на котором они должны быть подготовлены для просмотра.</span><span class="sxs-lookup"><span data-stu-id="38121-109">By exchanging pointers to a data object, providers and consumers of data can manage data transfers in a uniform manner, regardless of the format of the data, the type of medium used to transfer the data, or the target device on which it is to be rendered.</span></span> <span data-ttu-id="38121-110">В приложение можно включить поддержку для базовых передач буфера обмена, перетаскивания передачи и передачи составных документов OLE с помощью одной реализации интерфейса [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject).</span><span class="sxs-lookup"><span data-stu-id="38121-110">You can include support in your application for basic clipboard transfers, drag and drop transfers, and OLE compound document transfers with a single implementation of [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject).</span></span> <span data-ttu-id="38121-111">После этого объем кода, необходимый для размещения специальной семантики каждого протокола, является минимальным.</span><span class="sxs-lookup"><span data-stu-id="38121-111">Having done that, the amount of code required to accommodate the special semantics of each protocol is minimal.</span></span>

<span data-ttu-id="38121-112">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="38121-112">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="38121-113">Интерфейсы Передача данных</span><span class="sxs-lookup"><span data-stu-id="38121-113">Data Transfer Interfaces</span></span>](data-transfer-interfaces.md)
-   [<span data-ttu-id="38121-114">Форматы данных и передачи мультимедиа</span><span class="sxs-lookup"><span data-stu-id="38121-114">Data Formats and Transfer Media</span></span>](data-formats-and-transfer-media.md)
-   [<span data-ttu-id="38121-115">Перетаскивание</span><span class="sxs-lookup"><span data-stu-id="38121-115">Drag and Drop</span></span>](drag-and-drop.md)

## <a name="related-topics"></a><span data-ttu-id="38121-116">См. также</span><span class="sxs-lookup"><span data-stu-id="38121-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="38121-117">Составные документы</span><span class="sxs-lookup"><span data-stu-id="38121-117">Compound Documents</span></span>](compound-documents.md)
</dt> </dl>

 

 




