---
title: Управление схемой
description: Компонент поставщика в примере ADSI определяет классы схемы \ 0034; подразделение \ 0034; и \ 0034; Пользователь \ 0034; и управляют этими классами схемы следующим образом.
ms.assetid: c3e07846-a11e-46d4-9863-a89810896ad7
ms.tgt_platform: multiple
keywords:
- ADSI управления схемой
- ADSI управления схемой
- Управление схемами ADSI
- схемы, управление ADSI
- Управление схемой ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99d398f8eb056498977f886e836c0f97c95f0b9b
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104551896"
---
# <a name="schema-management"></a><span data-ttu-id="f6f97-108">Управление схемой</span><span class="sxs-lookup"><span data-stu-id="f6f97-108">Schema Management</span></span>

<span data-ttu-id="f6f97-109">Компонент "пример поставщика ADSI" определяет классы схемы "подразделение" и "пользователь", а также управляет этими классами схем следующим образом.</span><span class="sxs-lookup"><span data-stu-id="f6f97-109">The ADSI example provider component defines the schema classes "Organizational Unit" and "User" and manages these schema classes in the following way.</span></span>

<span data-ttu-id="f6f97-110">Класс схемы "подразделение" представлен объектом-контейнером ADs и может содержать другие "подразделения" и "Пользователи".</span><span class="sxs-lookup"><span data-stu-id="f6f97-110">The "Organizational Unit" schema class is represented by an ADs container object and can contain other "Organizational Units" and "Users".</span></span> <span data-ttu-id="f6f97-111">Объект контейнера поддерживает интерфейсы [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch), [**iAds**](/windows/desktop/api/Iads/nn-iads-iads)и [**иадсконтаинер**](/windows/desktop/api/Iads/nn-iads-iadscontainer).</span><span class="sxs-lookup"><span data-stu-id="f6f97-111">The container object supports the interfaces [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch), [**IADs**](/windows/desktop/api/Iads/nn-iads-iads), and [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer).</span></span> <span data-ttu-id="f6f97-112">Класс схемы User представлен универсальным Active Directory объектом и не содержит других типов объектов.</span><span class="sxs-lookup"><span data-stu-id="f6f97-112">The "User" schema class is represented by a generic Active Directory object and does not contain other types of objects.</span></span> <span data-ttu-id="f6f97-113">В примере компонента поставщика объект пользователя реализуется как универсальный объект Active Directory, который поддерживает интерфейсы **IUnknown**, **IDispatch** и **iAds**.</span><span class="sxs-lookup"><span data-stu-id="f6f97-113">In the example provider component, the User object is implemented as a generic Active Directory object that supports the interfaces **IUnknown**, **IDispatch**, and **IADs**.</span></span> <span data-ttu-id="f6f97-114">Имейте в виду, что объект User в данном случае не поддерживает интерфейс [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser) .</span><span class="sxs-lookup"><span data-stu-id="f6f97-114">Be aware that the User object, in this case, does not support the [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser) interface.</span></span>

<span data-ttu-id="f6f97-115">В примере компонента поставщика также должен быть реализован объект пространства имен ADs, который поддерживает интерфейсы [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), [**iAds**](/windows/desktop/api/Iads/nn-iads-iads), [**иадсконтаинер**](/windows/desktop/api/Iads/nn-iads-iadscontainer), [**иадсопендсобжект**](/windows/desktop/api/Iads/nn-iads-iadsopendsobject)и [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch).</span><span class="sxs-lookup"><span data-stu-id="f6f97-115">The example provider component must also implement the ADs namespace object, which supports the interfaces [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), [**IADs**](/windows/desktop/api/Iads/nn-iads-iads), [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer), [**IADsOpenDSObject**](/windows/desktop/api/Iads/nn-iads-iadsopendsobject), and [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch).</span></span>

<span data-ttu-id="f6f97-116">На следующем рисунке показаны сведения о схеме, представляющей два примера классов схемы компонентов поставщика.</span><span class="sxs-lookup"><span data-stu-id="f6f97-116">The following figure shows the details of the schema that represents the two example provider component schema classes.</span></span>

![Пример схемы компонента поставщика ADSI](images/dssmsch.png)

<span data-ttu-id="f6f97-118">Обратите внимание, что на предыдущем рисунке класс схемы "подразделение" определяет три свойства: "Description", "Хеадкаунтс" и "ID".</span><span class="sxs-lookup"><span data-stu-id="f6f97-118">Be aware that in the preceding figure the "Organizational Unit" schema class defines three properties: "Description," "Headcounts," and "ID."</span></span> <span data-ttu-id="f6f97-119">Класс схемы user определяет четыре свойства: "ID", "Name", "PhoneNumber" и "Title".</span><span class="sxs-lookup"><span data-stu-id="f6f97-119">The "User" schema class defines four properties: "ID," "Name," "PhoneNumber," and "Title."</span></span> <span data-ttu-id="f6f97-120">Свойство "ID" совместно используется обоими классами схемы.</span><span class="sxs-lookup"><span data-stu-id="f6f97-120">The "ID" property is shared by both schema classes.</span></span> <span data-ttu-id="f6f97-121">Каждое свойство определяется как объект синтаксиса "String" или "integer".</span><span class="sxs-lookup"><span data-stu-id="f6f97-121">Each property is defined by either the "String" or the "Integer" syntax object.</span></span>

> [!Note]  
> <span data-ttu-id="f6f97-122">Объекты синтаксиса не представлены в первом выпуске примера компонента поставщика.</span><span class="sxs-lookup"><span data-stu-id="f6f97-122">Syntax objects are not present in the first release of the example provider component.</span></span> <span data-ttu-id="f6f97-123">Однако в большинстве реализаций схемы Microsoft ADSI объекты синтаксиса включаются в объект контейнера схемы, точно так же, как класс схемы и объекты свойств.</span><span class="sxs-lookup"><span data-stu-id="f6f97-123">However, in most Microsoft ADSI schema implementations, the syntax objects are included in the schema container object, just as the schema class and property objects are.</span></span> <span data-ttu-id="f6f97-124">По этой причине они показаны здесь.</span><span class="sxs-lookup"><span data-stu-id="f6f97-124">For this reason, they are shown here.</span></span>

 

<span data-ttu-id="f6f97-125">Этот компонент поставщика предоставляет доступ к данным схемы клиентскому приложению ADSI в виде объектов класса ADs, объектов свойств ADs и объектов синтаксиса ADs, всех в объекте контейнера схемы, чтобы данные схемы можно было извлечь во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="f6f97-125">This provider component makes schema data accessible to the ADSI client application in the form of ADs class objects, ADs property objects, and ADs syntax objects, all within a schema class container object, so that schema data can be retrieved at run time.</span></span>

<span data-ttu-id="f6f97-126">Адспасс для объектов контейнера класса схемы, определенных для компонента примера поставщика, — это "Sample://Seattle/schema" и "Sample://Toronto/schema".</span><span class="sxs-lookup"><span data-stu-id="f6f97-126">The ADsPaths for the schema class container objects defined for the example provider component are "Sample://Seattle/schema" and "Sample://Toronto/schema".</span></span> <span data-ttu-id="f6f97-127">В этом примере содержимое схем идентично.</span><span class="sxs-lookup"><span data-stu-id="f6f97-127">In this example, the contents of the schemas are identical.</span></span>

 

 