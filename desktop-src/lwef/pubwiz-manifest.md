---
title: Использование манифеста перемещения
description: Мастер веб-публикаций и мастер заказа отпечатков через Интернет используют манифест передачи для передачи сведений о передаче данных между клиентским компьютером и узлом сервера.
ms.assetid: b7bb541c-3bf4-4aab-ac70-c006517e772e
keywords:
- Мастер веб-публикаций, перенесите манифест
- Мастер заказа принтера в сети, перенесите манифест
- Перенесите манифест
- manifest
- Window. external, перенесите манифест
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20fa7b3a35a6f06e2939b6c25f82d12c2b98a7f7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103890625"
---
# <a name="using-the-transfer-manifest"></a><span data-ttu-id="04adb-108">Использование манифеста перемещения</span><span class="sxs-lookup"><span data-stu-id="04adb-108">Using the Transfer Manifest</span></span>

<span data-ttu-id="04adb-109">Мастер веб-публикаций и мастер заказа отпечатков через Интернет используют манифест передачи для передачи сведений о передаче данных между клиентским компьютером и узлом сервера.</span><span class="sxs-lookup"><span data-stu-id="04adb-109">The Web Publishing Wizard and Online Print Ordering Wizard use the transfer manifest to communicate details of data transfer between the client computer and the server site.</span></span>

## <a name="the-purpose-of-the-transfer-manifest"></a><span data-ttu-id="04adb-110">Назначение манифеста перемещения</span><span class="sxs-lookup"><span data-stu-id="04adb-110">The Purpose of the Transfer Manifest</span></span>

<span data-ttu-id="04adb-111">Манифест перемещения описывает файлы, участвующие в переносе, включая такие сведения, как конечная иерархия и метаданные файла.</span><span class="sxs-lookup"><span data-stu-id="04adb-111">The transfer manifest describes files involved in the transfer, including details such as the destination hierarchy and the file's metadata.</span></span> <span data-ttu-id="04adb-112">Сценарий на стороне сервера может изменить манифест, удалив из списка недопустимые файлы и добавив сведения о том, как и где следует передавать файлы.</span><span class="sxs-lookup"><span data-stu-id="04adb-112">Server-side script can modify the manifest by removing inappropriate files from the list and adding information about how and where the files should be transferred.</span></span>

<span data-ttu-id="04adb-113">Манифест предоставляется как **окно свойств. external. свойство ("трансферманифест")**, документ XML модель DOM (DOM).</span><span class="sxs-lookup"><span data-stu-id="04adb-113">The manifest is exposed as the property **window.external.Property("TransferManifest")**, an XML Document Object Model (DOM) document.</span></span> <span data-ttu-id="04adb-114">Дополнительные сведения об XML DOM см. в документации MSDN по [IXMLDOMDocument/DOMDocument](/previous-versions/windows/desktop/ms756987(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="04adb-114">For more information on the XML DOM, see the MSDN documentation for [IXMLDOMDocument/DOMDocument](/previous-versions/windows/desktop/ms756987(v=vs.85)).</span></span>

<span data-ttu-id="04adb-115">Ниже приведена организация верхнего уровня манифеста перемещения.</span><span class="sxs-lookup"><span data-stu-id="04adb-115">The top-level organization of the transfer manifest is as follows:</span></span>


```
<transfermanifest>
    <filelist/>
    <folderlist/>
    <uploadinfo/>
</transfermanifest>
```



<span data-ttu-id="04adb-116">Страница HTML на стороне сервера может использовать узлы в манифесте для получения определенных сведений о копируемых файлах, а затем соответствующим образом изменить пользовательский интерфейс службы.</span><span class="sxs-lookup"><span data-stu-id="04adb-116">The server-side HTML page can use the nodes in the manifest to obtain certain information about the files to be copied and then modify the service's UI accordingly.</span></span> <span data-ttu-id="04adb-117">Например, сайт печати фотографий может использовать информацию для показа эскизов выбранных изображений, в то время как сайт хранилища может использовать эти сведения для обеспечения достаточного объема дискового пространства для этого пользователя.</span><span class="sxs-lookup"><span data-stu-id="04adb-117">For instance, a photo printing site might use the information to display thumbnails of the chosen images, while a storage site might use the information to ensure that sufficient storage space is available for that user.</span></span> <span data-ttu-id="04adb-118">Полные сведения об узлах и атрибутах манифеста см. в статье о [перенесите схему манифеста](/windows/desktop/shell/interfaces).</span><span class="sxs-lookup"><span data-stu-id="04adb-118">For complete information on the transfer manifest nodes and attributes, see [Transfer Manifest Schema](/windows/desktop/shell/interfaces).</span></span>

<span data-ttu-id="04adb-119">Схема манифеста перемещения записывается в виде открытой модели, чтобы элементы, не определенные в схеме, могли отображаться в манифесте перемещения.</span><span class="sxs-lookup"><span data-stu-id="04adb-119">The transfer manifest schema is written as an open model so that elements not specifically defined in the schema may appear in the transfer manifest.</span></span> <span data-ttu-id="04adb-120">Таким образом, сайт поставщика может добавлять собственные элементы для собственного использования без нарушения допустимости манифеста.</span><span class="sxs-lookup"><span data-stu-id="04adb-120">Therefore, a provider site might add proprietary elements for its own use without disturbing the validity of the manifest.</span></span> <span data-ttu-id="04adb-121">Схема также определяется таким образом, чтобы порядок элементов не был ограничен.</span><span class="sxs-lookup"><span data-stu-id="04adb-121">The schema is also defined so that the order of elements is not restricted.</span></span>

> [!Note]  
> <span data-ttu-id="04adb-122">Манифест создается повторно каждый раз при выборе нового поставщика, чтобы поставщик получил возможность хранить сведения о сайте в манифесте.</span><span class="sxs-lookup"><span data-stu-id="04adb-122">The manifest is re-created each time a new provider is chosen so that the provider has a chance to store site information in the manifest.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="04adb-123">См. также</span><span class="sxs-lookup"><span data-stu-id="04adb-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="04adb-124">Схема перемещения манифеста</span><span class="sxs-lookup"><span data-stu-id="04adb-124">Transfer Manifest Schema</span></span>](/windows/desktop/shell/interfaces)
</dt> </dl>

 

 