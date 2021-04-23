---
title: Константы ADSI
description: В следующей таблице перечислены константы, определенные и используемые в Active Directory интерфейсах служб (ADSI).
ms.assetid: facc00e8-2ecd-4428-bddd-cfa1ff1b8538
ms.tgt_platform: multiple
keywords:
- ADS_EXT_INITCREDENTIALS
- ADS_EXT_INITIALIZE_COMPLETE
- ADS_EXT_MAXEXTDISPID
- ADS_EXT_MINEXTDISPID
- ADS_VLV_RESPONSE
- DBPROPFLAGS_ADSISEARCH
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04cc4aaf5043f9fcd2a61dfa68124b6cb1a1a69b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773022"
---
# <a name="adsi-constants"></a><span data-ttu-id="a0707-109">Константы ADSI</span><span class="sxs-lookup"><span data-stu-id="a0707-109">ADSI Constants</span></span>

<span data-ttu-id="a0707-110">В следующей таблице перечислены константы, определенные и используемые в Active Directory интерфейсах служб (ADSI).</span><span class="sxs-lookup"><span data-stu-id="a0707-110">The following table lists constants defined and used in Active Directory Service Interfaces (ADSI).</span></span>



| <span data-ttu-id="a0707-111">Константа ADSI</span><span class="sxs-lookup"><span data-stu-id="a0707-111">ADSI constant</span></span>                      | <span data-ttu-id="a0707-112">Значение</span><span class="sxs-lookup"><span data-stu-id="a0707-112">Value</span></span>                                   | <span data-ttu-id="a0707-113">Описание</span><span class="sxs-lookup"><span data-stu-id="a0707-113">Description</span></span>                                                                                                                                                                                                      |
|------------------------------------|-----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0707-114">**Реклама \_ ext \_ иниткредентиалс**</span><span class="sxs-lookup"><span data-stu-id="a0707-114">**ADS\_EXT\_INITCREDENTIALS**</span></span>      | <span data-ttu-id="a0707-115">1</span><span class="sxs-lookup"><span data-stu-id="a0707-115">1</span></span>                                       | <span data-ttu-id="a0707-116">Управляющий код, указывающий, что пользовательские данные, передаваемые в метод [**иадсекстенсион:: оперирует**](/windows/desktop/api/Iads/nf-iads-iadsextension-operate) , содержат учетные данные пользователя.</span><span class="sxs-lookup"><span data-stu-id="a0707-116">A control code that indicates that the custom data supplied to the [**IADsExtension::Operate**](/windows/desktop/api/Iads/nf-iads-iadsextension-operate) method contains user credentials.</span></span>                                                     |
| <span data-ttu-id="a0707-117">**\_ \_ Инициализация ext AD \_ завершена**</span><span class="sxs-lookup"><span data-stu-id="a0707-117">**ADS\_EXT\_INITIALIZE\_COMPLETE**</span></span> | <span data-ttu-id="a0707-118">2</span><span class="sxs-lookup"><span data-stu-id="a0707-118">2</span></span>                                       | <span data-ttu-id="a0707-119">Управляющий код, используемый с [**иадсекстенсион:: работают**](/windows/desktop/api/Iads/nf-iads-iadsextension-operate) , чтобы указать, что расширения могут выполнять необходимую инициализацию в зависимости от возможностей, поддерживаемых родительским объектом.</span><span class="sxs-lookup"><span data-stu-id="a0707-119">A control code used with [**IADsExtension::Operate**](/windows/desktop/api/Iads/nf-iads-iadsextension-operate) to indicate that extensions can perform any necessary initialization, depending on the features supported by the parent object.</span></span> |
| <span data-ttu-id="a0707-120">**Реклама \_ ext \_ максекстдиспид**</span><span class="sxs-lookup"><span data-stu-id="a0707-120">**ADS\_EXT\_MAXEXTDISPID**</span></span>         | <span data-ttu-id="a0707-121">16777215</span><span class="sxs-lookup"><span data-stu-id="a0707-121">16777215</span></span>                                | <span data-ttu-id="a0707-122">Самый высокий идентификатор DISPID, который объект расширения может использовать для своих методов и свойств.</span><span class="sxs-lookup"><span data-stu-id="a0707-122">The highest DISPID an extension object can use for its methods and properties.</span></span>                                                                                                                                   |
| <span data-ttu-id="a0707-123">**Реклама \_ ext \_ минекстдиспид**</span><span class="sxs-lookup"><span data-stu-id="a0707-123">**ADS\_EXT\_MINEXTDISPID**</span></span>         | <span data-ttu-id="a0707-124">1</span><span class="sxs-lookup"><span data-stu-id="a0707-124">1</span></span>                                       | <span data-ttu-id="a0707-125">Самый низкий идентификатор DISPID, который объект расширения может использовать для своих методов и свойств.</span><span class="sxs-lookup"><span data-stu-id="a0707-125">The lowest DISPID an extension object can use for its methods and properties.</span></span>                                                                                                                                    |
| <span data-ttu-id="a0707-126">**\_ответ VLV \_ ADS**</span><span class="sxs-lookup"><span data-stu-id="a0707-126">**ADS\_VLV\_RESPONSE**</span></span>             | <span data-ttu-id="a0707-127">L "fc8cb04d-311d-406c-8cb9-1ae8b843b419"</span><span class="sxs-lookup"><span data-stu-id="a0707-127">L"fc8cb04d-311d-406c-8cb9-1ae8b843b419"</span></span> | <span data-ttu-id="a0707-128">Используется с методом [**IDirectorySearch:: DataColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn) для получения МЕТАДАННЫХ поиска VLV.</span><span class="sxs-lookup"><span data-stu-id="a0707-128">Used with the [**IDirectorySearch::GetColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn) method to retrieve VLV search metadata.</span></span> <span data-ttu-id="a0707-129">Дополнительные сведения см. [в разделе Поиск с помощью VLV](how-to-search-using-vlv.md).</span><span class="sxs-lookup"><span data-stu-id="a0707-129">For more information, see [How to Search Using VLV](how-to-search-using-vlv.md).</span></span>        |
| <span data-ttu-id="a0707-130">**DBPROPFLAGS \_ адсисеарч**</span><span class="sxs-lookup"><span data-stu-id="a0707-130">**DBPROPFLAGS\_ADSISEARCH**</span></span>        | <span data-ttu-id="a0707-131">0x0000C000</span><span class="sxs-lookup"><span data-stu-id="a0707-131">0x0000C000</span></span>                              | <span data-ttu-id="a0707-132">Используется для работы с поставщиком OLE DB.</span><span class="sxs-lookup"><span data-stu-id="a0707-132">Used to work with the OLE DB provider.</span></span>                                                                                                                                                                           |



 

 

 




