---
title: Получение свойств учета
description: Объект Account является одним из объектов в коллекции обработчиков запросов.
ms.assetid: eb5c8606-d3f0-4c33-9035-7b7b1369cb0d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9911397c1de3521ccb5a275405416d8b88c1fa6f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413241"
---
# <a name="obtaining-accounting-properties"></a><span data-ttu-id="e1f70-103">Получение свойств учета</span><span class="sxs-lookup"><span data-stu-id="e1f70-103">Obtaining Accounting Properties</span></span>

> [!Note]  
> <span data-ttu-id="e1f70-104">Служба проверки подлинности в Интернете (IAS) переименовала сервер политики сети (NPS), начиная с Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="e1f70-104">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.</span></span> <span data-ttu-id="e1f70-105">Содержимое этого раздела относится как к IAS, так и к NPS.</span><span class="sxs-lookup"><span data-stu-id="e1f70-105">The content of this topic applies to both IAS and NPS.</span></span> <span data-ttu-id="e1f70-106">По всему тексту NPS используется для ссылки на все версии службы, включая версии, изначально называемые IAS.</span><span class="sxs-lookup"><span data-stu-id="e1f70-106">Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</span></span>

 

<span data-ttu-id="e1f70-107">Объект Account является одним из объектов в коллекции обработчиков запросов.</span><span class="sxs-lookup"><span data-stu-id="e1f70-107">The accounting object is one of the objects in the Request Handlers collection.</span></span> <span data-ttu-id="e1f70-108">Значением перечисления для коллекции обработчиков запросов является **свойство \_ службы IAS \_ рекуессандлерс \_ Collection**.</span><span class="sxs-lookup"><span data-stu-id="e1f70-108">The enumeration value for the request handlers collection is **PROPERTY\_IAS\_REQUESTHANDLERS\_COLLECTION**.</span></span> <span data-ttu-id="e1f70-109">Имя обработчика для объекта учета — Microsoft Accounting.</span><span class="sxs-lookup"><span data-stu-id="e1f70-109">The name of the handler for the accounting object is "Microsoft Accounting".</span></span>

<span data-ttu-id="e1f70-110">Следующий Visual Basic код обращается к свойствам, доступным в обработчике объектов учета.</span><span class="sxs-lookup"><span data-stu-id="e1f70-110">The following Visual Basic code accesses the properties available from the accounting object handler.</span></span>


```VB
Set sdoRequestHandler = sdoCollRequestHandlers.Item("Microsoft Accounting")
vtTemp = sdoRequestHandler.GetProperty(PROPERTY_ACCOUNTING_LOG_ACCOUNTING)
vtTemp = sdoRequestHandler.GetProperty(PROPERTY_ACCOUNTING_LOG_ACCOUNTING_INTERIM)
vtTemp = sdoRequestHandler.GetProperty(PROPERTY_ACCOUNTING_LOG_AUTHENTICATION)
vtTemp = sdoRequestHandler.GetProperty(PROPERTY_ACCOUNTING_LOG_FILE_DIRECTORY)
vtTemp = sdoRequestHandler.GetProperty(PROPERTY_ACCOUNTING_LOG_IAS1_FORMAT)
vtTemp = sdoRequestHandler.GetProperty(PROPERTY_ACCOUNTING_LOG_OPEN_NEW_FREQUENCY)
vtTemp = sdoRequestHandler.GetProperty(PROPERTY_ACCOUNTING_LOG_OPEN_NEW_SIZE)
```



<span data-ttu-id="e1f70-111">Чтобы получить доступ к свойствам учета с помощью C++, сначала получите коллекцию обработчиков запросов.</span><span class="sxs-lookup"><span data-stu-id="e1f70-111">To access the accounting properties using C++, first obtain the request handlers collection.</span></span> <span data-ttu-id="e1f70-112">[Извлечение коллекции](/windows/desktop/Nps/sdo-retrieving-a-collection) содержит код C++, демонстрирующий получение коллекции.</span><span class="sxs-lookup"><span data-stu-id="e1f70-112">The [Retrieving a Collection](/windows/desktop/Nps/sdo-retrieving-a-collection) contains C++ code that demonstrates how to obtain a collection.</span></span> <span data-ttu-id="e1f70-113">Значением перечисления для коллекции обработчиков запросов является **свойство \_ службы IAS \_ рекуессандлерс \_ Collection**.</span><span class="sxs-lookup"><span data-stu-id="e1f70-113">The enumeration value for the request handlers collection is **PROPERTY\_IAS\_REQUESTHANDLERS\_COLLECTION**.</span></span> <span data-ttu-id="e1f70-114">(Значения, соответствующие различным коллекциям NPS, перечисляются типом перечисления [**иаспропертиес**](/windows/desktop/api/sdoias/ne-sdoias-iasproperties) .)</span><span class="sxs-lookup"><span data-stu-id="e1f70-114">(The values corresponding to the various NPS collections are enumerated by the [**IASPROPERTIES**](/windows/desktop/api/sdoias/ne-sdoias-iasproperties) enumeration type.)</span></span>

<span data-ttu-id="e1f70-115">Коллекция обработчиков запросов содержит объект с именем «Microsoft account».</span><span class="sxs-lookup"><span data-stu-id="e1f70-115">The request handlers collection contains an object named "Microsoft Accounting".</span></span> <span data-ttu-id="e1f70-116">Извлеките этот объект из коллекции.</span><span class="sxs-lookup"><span data-stu-id="e1f70-116">Retrieve this object from the collection.</span></span> <span data-ttu-id="e1f70-117">Раздел, в котором [извлекается объект из коллекции](/windows/desktop/Nps/sdo-retrieving-an-object-from-a-collection) , содержит код C++, демонстрирующий получение объекта из коллекции.</span><span class="sxs-lookup"><span data-stu-id="e1f70-117">The section [Retrieving an Object from a Collection](/windows/desktop/Nps/sdo-retrieving-an-object-from-a-collection) contains C++ code that demonstrates how to obtain an object from a collection.</span></span>

<span data-ttu-id="e1f70-118">Получив объект Microsoft account, получите интерфейс [**исдо**](/windows/desktop/api/sdoias/nn-sdoias-isdo) для объекта с помощью [**IUnknown:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)).</span><span class="sxs-lookup"><span data-stu-id="e1f70-118">Once you have the Microsoft Accounting object, obtain an [**ISdo**](/windows/desktop/api/sdoias/nn-sdoias-isdo) interface for the object using [**IUnknown::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)).</span></span> <span data-ttu-id="e1f70-119">В разделе [Получение ПОЛЬЗОВАТЕЛЬСКОГО SDO](/windows/desktop/Nps/sdo-retrieving-a-user-sdo) содержится код C++, демонстрирующий получение интерфейса **исдо** для объекта.</span><span class="sxs-lookup"><span data-stu-id="e1f70-119">The section [Retrieving a User SDO](/windows/desktop/Nps/sdo-retrieving-a-user-sdo) contains C++ code that demonstrates how obtain an **ISdo** interface for an object.</span></span> <span data-ttu-id="e1f70-120">Затем можно использовать метод [**исдо::**](/windows/desktop/api/sdoias/nf-sdoias-isdo-getproperty) GetObject для получения значений свойств для объекта Microsoft account.</span><span class="sxs-lookup"><span data-stu-id="e1f70-120">You can then use the [**ISdo::GetProperty**](/windows/desktop/api/sdoias/nf-sdoias-isdo-getproperty) method to obtain property values for the Microsoft Accounting object.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e1f70-121">См. также</span><span class="sxs-lookup"><span data-stu-id="e1f70-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e1f70-122">Получение коллекции</span><span class="sxs-lookup"><span data-stu-id="e1f70-122">Retrieving a Collection</span></span>](/windows/desktop/Nps/sdo-retrieving-a-collection)
</dt> <dt>

[<span data-ttu-id="e1f70-123">Получение объекта из коллекции</span><span class="sxs-lookup"><span data-stu-id="e1f70-123">Retrieving an Object from a Collection</span></span>](/windows/desktop/Nps/sdo-retrieving-an-object-from-a-collection)
</dt> <dt>

[<span data-ttu-id="e1f70-124">Получение SDO пользователя</span><span class="sxs-lookup"><span data-stu-id="e1f70-124">Retrieving a User SDO</span></span>](/windows/desktop/Nps/sdo-retrieving-a-user-sdo)
</dt> <dt>

[<span data-ttu-id="e1f70-125">**исдо**</span><span class="sxs-lookup"><span data-stu-id="e1f70-125">**ISdo**</span></span>](/windows/desktop/api/sdoias/nn-sdoias-isdo)
</dt> <dt>

<span data-ttu-id="e1f70-126">[**IUnknown:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span><span class="sxs-lookup"><span data-stu-id="e1f70-126">[**IUnknown::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span></span>
</dt> <dt>

[<span data-ttu-id="e1f70-127">**иаспропертиес**</span><span class="sxs-lookup"><span data-stu-id="e1f70-127">**IASPROPERTIES**</span></span>](/windows/desktop/api/sdoias/ne-sdoias-iasproperties)
</dt> </dl>

 

 