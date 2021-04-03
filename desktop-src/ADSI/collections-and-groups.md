---
title: Коллекции и группы
description: ADSI использует объекты коллекции для представления любого произвольного набора элементов в службе каталогов, которые могут быть представлены с использованием одного и того же типа данных.
ms.assetid: 03257cc9-f354-4e1c-8880-936a7acac3ef
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, использование коллекций и групп
- коллекции ADSI
- группы ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9f0f4d699d8dde0c3d70c7449dfe146212b2b30
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "103987870"
---
# <a name="collections-and-groups"></a><span data-ttu-id="1bcea-106">Коллекции и группы</span><span class="sxs-lookup"><span data-stu-id="1bcea-106">Collections and Groups</span></span>

<span data-ttu-id="1bcea-107">ADSI использует объекты коллекции для представления любого произвольного набора элементов в службе каталогов, которые могут быть представлены с использованием одного и того же типа данных.</span><span class="sxs-lookup"><span data-stu-id="1bcea-107">ADSI uses collection objects to represent any arbitrary set of items in a directory service that can be represented using the same data type.</span></span> <span data-ttu-id="1bcea-108">Объекты коллекции определяются как набор значений **типа Variant** , представляющих любые допустимые типы данных автоматизации.</span><span class="sxs-lookup"><span data-stu-id="1bcea-108">Collection objects are defined as a set of **VARIANT** values, representing any of the valid Automation data types.</span></span> <span data-ttu-id="1bcea-109">Объекты коллекции могут представлять как постоянные данные, такие как списки управления доступом, так и временные сведения, например задания печати в очереди печати.</span><span class="sxs-lookup"><span data-stu-id="1bcea-109">Collection objects can represent both persistent information such as access-control lists and volatile information such as print jobs in a print queue.</span></span>

<span data-ttu-id="1bcea-110">Стандартным соглашением COM для перечисления содержимого объекта коллекции (или контейнера) является создание объекта перечислителя, поддерживающего [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant), который содержит методы для пошагового выполнения списка объектов коллекции.</span><span class="sxs-lookup"><span data-stu-id="1bcea-110">The standard COM convention for listing the contents of a collection (or container) object is to create an enumerator object that supports [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant), which has methods to step through the list of collection objects.</span></span> <span data-ttu-id="1bcea-111">Интерфейсы в ADSI, которые предоставляют метод **Get \_ \_ NewEnum** (Обратите внимание на два символа подчеркивания), — это [**иадсконтаинер**](/windows/desktop/api/Iads/nn-iads-iadscontainer), [**иадсмемберс**](/windows/desktop/api/Iads/nn-iads-iadsmembers) и [**иадсколлектион**](/windows/desktop/api/Iads/nn-iads-iadscollection).</span><span class="sxs-lookup"><span data-stu-id="1bcea-111">The interfaces in ADSI that supply the **get\_\_NewEnum** method (note the two underscores) are [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer), [**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers) and [**IADsCollection**](/windows/desktop/api/Iads/nn-iads-iadscollection).</span></span> <span data-ttu-id="1bcea-112">ADSI также предоставляет вспомогательные функции [**адсбуилденумератор**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildenumerator) и [**Адсенумератенекст**](/windows/desktop/api/Adshlp/nf-adshlp-adsenumeratenext) для программ C и C++, чтобы упростить перечисление.</span><span class="sxs-lookup"><span data-stu-id="1bcea-112">ADSI also supplies the helper functions [**ADsBuildEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildenumerator) and [**ADsEnumerateNext**](/windows/desktop/api/Adshlp/nf-adshlp-adsenumeratenext) for C and C++ programs to simplify enumeration.</span></span> <span data-ttu-id="1bcea-113">Клиенты автоматизации используют перечисление неявно при вызове **Next** в цикле **for** .</span><span class="sxs-lookup"><span data-stu-id="1bcea-113">Automation clients use enumeration implicitly when they call **Next** in a **For** loop.</span></span>

<span data-ttu-id="1bcea-114">Группы представляют собой просто коллекции объектов, поддерживающих интерфейс [**иадсмемберс**](/windows/desktop/api/Iads/nn-iads-iadsmembers) .</span><span class="sxs-lookup"><span data-stu-id="1bcea-114">Groups are simply collections of objects supporting the [**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers) interface.</span></span>

 

 