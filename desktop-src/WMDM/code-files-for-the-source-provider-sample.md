---
title: Файлы кода для примера поставщика источника
description: Файлы кода для примера поставщика источника
ms.assetid: bd6bfc98-a805-4e04-8a80-7af42ed3dbef
keywords:
- Диспетчер устройств Windows Media, примеры
- Диспетчер устройств, примеры
- Диспетчер устройств Windows Media, пример поставщика услуг
- Диспетчер устройств, пример поставщика услуг
- поставщики услуг, примеры
- Примеры, поставщики услуг
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64b8af4b34310ae183ce55b2e52d3dd346dc6665
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104132958"
---
# <a name="code-files-for-the-source-provider-sample"></a><span data-ttu-id="9f833-109">Файлы кода для примера поставщика источника</span><span class="sxs-lookup"><span data-stu-id="9f833-109">Code Files for the Source Provider Sample</span></span>

<span data-ttu-id="9f833-110">Пример проекта поставщика источника включает следующие файлы исходного кода со связанными заголовками:</span><span class="sxs-lookup"><span data-stu-id="9f833-110">The sample source provider project includes the following source code files, with associated headers:</span></span>



| <span data-ttu-id="9f833-111">Файл</span><span class="sxs-lookup"><span data-stu-id="9f833-111">File</span></span>                   | <span data-ttu-id="9f833-112">Описание</span><span class="sxs-lookup"><span data-stu-id="9f833-112">Description</span></span>                                                                                                                                                                                                     |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f833-113">хдсппч. cpp</span><span class="sxs-lookup"><span data-stu-id="9f833-113">hdsppch.cpp</span></span>            | <span data-ttu-id="9f833-114">Включает стандартные файлы ATL.</span><span class="sxs-lookup"><span data-stu-id="9f833-114">Includes standard ATL files.</span></span>                                                                                                                                                                                    |
| <span data-ttu-id="9f833-115">Key. c</span><span class="sxs-lookup"><span data-stu-id="9f833-115">key.c</span></span>                  | <span data-ttu-id="9f833-116">Содержит фиктивный ключ проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="9f833-116">Contains a dummy authentication key.</span></span>                                                                                                                                                                            |
| <span data-ttu-id="9f833-117">логхелп. cpp</span><span class="sxs-lookup"><span data-stu-id="9f833-117">loghelp.cpp</span></span>            | <span data-ttu-id="9f833-118">Содержит функции, которые заводят в журнал действия и ошибки с помощью класса **вмдмлогжер** , который реализован в WMDMLOG.dll системном файле.</span><span class="sxs-lookup"><span data-stu-id="9f833-118">Contains functions that log activity and errors by using the **WMDMLogger** class, which is implemented in the WMDMLOG.dll system file.</span></span>                                                                         |
| <span data-ttu-id="9f833-119">Мдсервицепровидер. cpp</span><span class="sxs-lookup"><span data-stu-id="9f833-119">MDServiceProvider.cpp</span></span>  | <span data-ttu-id="9f833-120">Реализует класс Кмдсервицепровидер, реализующий интерфейсы [**имдсервицепровидер**](/windows/desktop/api/mswmdm/nn-mswmdm-imdserviceprovider) и икомпонентаусентикате.</span><span class="sxs-lookup"><span data-stu-id="9f833-120">Implements a class, CMDServiceProvider, that implements the [**IMDServiceProvider**](/windows/desktop/api/mswmdm/nn-mswmdm-imdserviceprovider) and IComponentAuthenticate interfaces.</span></span>                                                             |
| <span data-ttu-id="9f833-121">МДСП. cpp</span><span class="sxs-lookup"><span data-stu-id="9f833-121">mdsp.cpp</span></span>               | <span data-ttu-id="9f833-122">Точка входа DLL и регистрационный код.</span><span class="sxs-lookup"><span data-stu-id="9f833-122">DLL entry point and registration code.</span></span>                                                                                                                                                                          |
| <span data-ttu-id="9f833-123">Мдспдевице. cpp</span><span class="sxs-lookup"><span data-stu-id="9f833-123">MDSPDevice.cpp</span></span>         | <span data-ttu-id="9f833-124">Реализует класс Кмдспдевице, реализующий интерфейсы [**IMDSPDevice2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice2), [**имдспдевицеконтрол**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevicecontrol)и **испеЦифипропертипажес** .</span><span class="sxs-lookup"><span data-stu-id="9f833-124">Implements a class, CMDSPDevice, that implements the [**IMDSPDevice2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice2), [**IMDSPDeviceControl**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevicecontrol), and **ISpecifyPropertyPages** interfaces.</span></span>                          |
| <span data-ttu-id="9f833-125">Мдспенумдевице. cpp</span><span class="sxs-lookup"><span data-stu-id="9f833-125">MDSPEnumDevice.cpp</span></span>     | <span data-ttu-id="9f833-126">Реализует класс Кмдспенумдевице, реализующий интерфейс [**имдспенумдевице**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspenumdevice) .</span><span class="sxs-lookup"><span data-stu-id="9f833-126">Implements a class, CMDSPEnumDevice, that implements the [**IMDSPEnumDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspenumdevice) interface.</span></span>                                                                                                  |
| <span data-ttu-id="9f833-127">Мдспенумстораже. cpp</span><span class="sxs-lookup"><span data-stu-id="9f833-127">MDSPEnumStorage.cpp</span></span>    | <span data-ttu-id="9f833-128">Реализует класс Кмдспенумстораже, реализующий интерфейс [**имдспенумстораже**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspenumstorage) .</span><span class="sxs-lookup"><span data-stu-id="9f833-128">Implements a class, CMDSPEnumStorage, that implements the [**IMDSPEnumStorage**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspenumstorage) interface.</span></span>                                                                                               |
| <span data-ttu-id="9f833-129">Мдспстораже. cpp</span><span class="sxs-lookup"><span data-stu-id="9f833-129">MDSPStorage.cpp</span></span>        | <span data-ttu-id="9f833-130">Реализует класс Кмдспстораже, реализующий интерфейсы [**IMDSPStorage2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage2), [**имдспобжектинфо**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobjectinfo)и [**имдспобжект**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobject) .</span><span class="sxs-lookup"><span data-stu-id="9f833-130">Implements a class, CMDSPStorage, that implements the [**IMDSPStorage2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage2), [**IMDSPObjectInfo**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobjectinfo), and [**IMDSPObject**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobject) interfaces.</span></span>                    |
| <span data-ttu-id="9f833-131">Мдспсторажеглобалс. cpp</span><span class="sxs-lookup"><span data-stu-id="9f833-131">MDSPStorageGlobals.cpp</span></span> | <span data-ttu-id="9f833-132">Реализует класс Кмдспсторажеглобалс, реализующий интерфейс [**имдспсторажеглобалс**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorageglobals) .</span><span class="sxs-lookup"><span data-stu-id="9f833-132">Implements a class, CMDSPStorageGlobals, that implements the [**IMDSPStorageGlobals**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorageglobals) interface.</span></span>                                                                                      |
| <span data-ttu-id="9f833-133">Мдспутил. cpp</span><span class="sxs-lookup"><span data-stu-id="9f833-133">MDSPutil.cpp</span></span>           | <span data-ttu-id="9f833-134">Содержит различные служебные функции для управления устройствами и файлами.</span><span class="sxs-lookup"><span data-stu-id="9f833-134">Contains various utility functions for device and file management.</span></span>                                                                                                                                              |
| <span data-ttu-id="9f833-135">заменяющий. cpp</span><span class="sxs-lookup"><span data-stu-id="9f833-135">proppage.cpp</span></span>           | <span data-ttu-id="9f833-136">Реализует класс Кпроппаже, наследующий классы ATL **ипропертипажеимпл** (для реализации ипропертипаже) и **CDialogImpl**, который наследует класс ATL CDialogImpl (для управления окнами и сообщениями).</span><span class="sxs-lookup"><span data-stu-id="9f833-136">Implements a class, CPropPage, that inherits the ATL classes **IPropertyPageImpl** (to implement IPropertyPage) and **CDialogImpl**, which inherits the ATL class CDialogImpl (to manage windows and messages).</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="9f833-137">См. также</span><span class="sxs-lookup"><span data-stu-id="9f833-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9f833-138">**Образец поставщика услуг**</span><span class="sxs-lookup"><span data-stu-id="9f833-138">**Sample Service Provider**</span></span>](sample-service-provider.md)
</dt> </dl>

 

 




