---
title: Сопоставление кода Visual Basic ADSI с кодом C++
description: Интерфейсы ADSI состоят из более чем 50 интерфейсов.
ms.assetid: 6316f504-265e-44d4-ba24-e6289065981b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c64a022569a95f38ec1da7a1cb7acf533eb04ca6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105654118"
---
# <a name="mapping-adsi-visual-basic-code-to-c-code"></a><span data-ttu-id="edf25-103">Сопоставление кода Visual Basic ADSI с кодом C++</span><span class="sxs-lookup"><span data-stu-id="edf25-103">Mapping ADSI Visual Basic Code to C++ Code</span></span>

<span data-ttu-id="edf25-104">Интерфейсы ADSI состоят из более чем 50 интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="edf25-104">ADSI consists of more than 50 interfaces.</span></span> <span data-ttu-id="edf25-105">Большинство операций с каталогами можно выполнить, используя только пять интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="edf25-105">Most directory operations can be completed using only five interfaces.</span></span> <span data-ttu-id="edf25-106">К ним относятся:</span><span class="sxs-lookup"><span data-stu-id="edf25-106">They are:</span></span>

-   [<span data-ttu-id="edf25-107">**иадсопендсобжект**</span><span class="sxs-lookup"><span data-stu-id="edf25-107">**IADsOpenDSObject**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsopendsobject)
-   [<span data-ttu-id="edf25-108">**IADs**</span><span class="sxs-lookup"><span data-stu-id="edf25-108">**IADs**</span></span>](/windows/desktop/api/Iads/nn-iads-iads)
-   [<span data-ttu-id="edf25-109">**иадсконтаинер**</span><span class="sxs-lookup"><span data-stu-id="edf25-109">**IADsContainer**</span></span>](/windows/desktop/api/Iads/nn-iads-iadscontainer)
-   [<span data-ttu-id="edf25-110">**идиректорйобжект**</span><span class="sxs-lookup"><span data-stu-id="edf25-110">**IDirectoryObject**</span></span>](/windows/desktop/api/Iads/nn-iads-idirectoryobject)
-   [<span data-ttu-id="edf25-111">**IDirectorySearch**</span><span class="sxs-lookup"><span data-stu-id="edf25-111">**IDirectorySearch**</span></span>](/windows/desktop/api/Iads/nn-iads-idirectorysearch)

<span data-ttu-id="edf25-112">В следующей таблице перечислены сопоставления из кода ADSI VB/VBS с кодом C++.</span><span class="sxs-lookup"><span data-stu-id="edf25-112">The following table lists mappings from ADSI VB/VBS code to C++ code.</span></span> <span data-ttu-id="edf25-113">Имейте в виду, что это не полный список.</span><span class="sxs-lookup"><span data-stu-id="edf25-113">Be aware that this is not a complete list.</span></span>



| <span data-ttu-id="edf25-114">Код VBS</span><span class="sxs-lookup"><span data-stu-id="edf25-114">VBS Code</span></span>                           | <span data-ttu-id="edf25-115">Код VC</span><span class="sxs-lookup"><span data-stu-id="edf25-115">VC Code</span></span>                                                               |
|------------------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="edf25-116">Set obj = GetObject ()</span><span class="sxs-lookup"><span data-stu-id="edf25-116">Set obj = GetObject()</span></span>              | <span data-ttu-id="edf25-117">HR = Адсжетобжект ()</span><span class="sxs-lookup"><span data-stu-id="edf25-117">hr = AdsGetObject()</span></span>                                                   |
| <span data-ttu-id="edf25-118">расширением. Установите obj. Получить obj. Источника</span><span class="sxs-lookup"><span data-stu-id="edf25-118">obj.Put obj.Get obj.Parent</span></span>         | <span data-ttu-id="edf25-119">IADs или Идиректорйобжект</span><span class="sxs-lookup"><span data-stu-id="edf25-119">IADs or IDirectoryObject</span></span>                                              |
| <span data-ttu-id="edf25-120">расширением. Создайте obj. Удалить obj. мовехере</span><span class="sxs-lookup"><span data-stu-id="edf25-120">obj.Create obj.Delete obj.MoveHere</span></span> | <span data-ttu-id="edf25-121">иадсконтаинер</span><span class="sxs-lookup"><span data-stu-id="edf25-121">IADsContainer</span></span>                                                         |
| <span data-ttu-id="edf25-122">Для каждого...</span><span class="sxs-lookup"><span data-stu-id="edf25-122">For each…</span></span> <span data-ttu-id="edf25-123">в...</span><span class="sxs-lookup"><span data-stu-id="edf25-123">in…</span></span>                      | <span data-ttu-id="edf25-124">Адсбуилденумератор () Адсенумератенекст ()</span><span class="sxs-lookup"><span data-stu-id="edf25-124">AdsBuildEnumerator() ADsEnumerateNext()</span></span>                               |
| <span data-ttu-id="edf25-125">Подключение, команда, набор записей</span><span class="sxs-lookup"><span data-stu-id="edf25-125">Connection, Command, RecordSet</span></span>     | <span data-ttu-id="edf25-126">IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="edf25-126">IDirectorySearch</span></span>                                                      |
| <span data-ttu-id="edf25-127">Дескриптор безопасности, ACL, ACE</span><span class="sxs-lookup"><span data-stu-id="edf25-127">Security descriptor, ACL, ACE</span></span>      | <span data-ttu-id="edf25-128">Иадссекуритидескриптор, Иадсакцессконтроллист, Иадсакцессконтролентри</span><span class="sxs-lookup"><span data-stu-id="edf25-128">IADsSecurityDescriptor, IADsAccessControlList, IADsAccessControlEntry</span></span> |



 

 

 




