---
title: Объект взаимного исключения
description: Объект взаимного исключения
ms.assetid: dd1f7865-e409-4bf9-9fa0-769a29eaed60
keywords:
- Пакет SDK для Windows Media Format, взаимоисключающие объекты
- Расширенный системный формат (ASF), взаимоисключающие объекты
- ASF (Расширенный системный формат), взаимоисключающие объекты
- объекты, взаимоисключающие объекты
- взаимное исключение, объекты
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8522b66f82bd88479b8c7b1d0d0b45bd038fdab3
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2020
ms.locfileid: "104133566"
---
# <a name="mutual-exclusion-object"></a><span data-ttu-id="bde79-108">Объект взаимного исключения</span><span class="sxs-lookup"><span data-stu-id="bde79-108">Mutual Exclusion Object</span></span>

<span data-ttu-id="bde79-109">Объект взаимного исключения используется для указания количества потоков, из которых может доставляться только один раз.</span><span class="sxs-lookup"><span data-stu-id="bde79-109">A mutual exclusion object is used to specify a number of streams, of which only one can be delivered at a time.</span></span> <span data-ttu-id="bde79-110">Это может быть использовано несколькими способами, например предоставление звукового потока на нескольких языках в качестве звуковой дорожки для одного видеопотока.</span><span class="sxs-lookup"><span data-stu-id="bde79-110">This can be used in several ways, such as providing an audio stream in several languages as the soundtrack for one video stream.</span></span>

<span data-ttu-id="bde79-111">Взаимное исключение является необязательной частью профиля.</span><span class="sxs-lookup"><span data-stu-id="bde79-111">Mutual exclusion is an optional part of a profile.</span></span> <span data-ttu-id="bde79-112">Взаимоисключающие объекты могут быть созданы для существующих взаимоисключающих сведений в профиле или могут быть созданы пустыми и готовы к получению новых данных.</span><span class="sxs-lookup"><span data-stu-id="bde79-112">Mutual exclusion objects can be created for existing mutual exclusion information in a profile or can be created empty, ready to receive new data.</span></span> <span data-ttu-id="bde79-113">Объекты взаимного исключения не могут существовать независимо от объекта профиля.</span><span class="sxs-lookup"><span data-stu-id="bde79-113">Mutual exclusion objects cannot exist independently of a profile object.</span></span> <span data-ttu-id="bde79-114">Чтобы сохранить содержимое взаимоисключающего объекта, необходимо вызвать метод [**ивмпрофиле:: аддмутуалексклусион**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addmutualexclusion).</span><span class="sxs-lookup"><span data-stu-id="bde79-114">To save the contents of a mutual exclusion object, you must call [**IWMProfile::AddMutualExclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addmutualexclusion).</span></span>

<span data-ttu-id="bde79-115">Чтобы создать объект взаимного исключения, используйте один из следующих методов.</span><span class="sxs-lookup"><span data-stu-id="bde79-115">To create a mutual exclusion object, use one of the following methods.</span></span>



| <span data-ttu-id="bde79-116">Метод</span><span class="sxs-lookup"><span data-stu-id="bde79-116">Method</span></span>                                                                              | <span data-ttu-id="bde79-117">Описание</span><span class="sxs-lookup"><span data-stu-id="bde79-117">Description</span></span>                                                                                                                                                 |
|-------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bde79-118">**Ивмпрофиле:: Креатеневмутуалексклусион**</span><span class="sxs-lookup"><span data-stu-id="bde79-118">**IWMProfile::CreateNewMutualExclusion**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewmutualexclusion) | <span data-ttu-id="bde79-119">Создает объект взаимного исключения без каких-либо данных.</span><span class="sxs-lookup"><span data-stu-id="bde79-119">Creates a mutual exclusion object without any data.</span></span>                                                                                                         |
| [<span data-ttu-id="bde79-120">**Ивмпрофиле:: Жетмутуалексклусион**</span><span class="sxs-lookup"><span data-stu-id="bde79-120">**IWMProfile::GetMutualExclusion**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getmutualexclusion)             | <span data-ttu-id="bde79-121">Создает объект взаимного исключения, заполненный данными из профиля.</span><span class="sxs-lookup"><span data-stu-id="bde79-121">Creates a mutual exclusion object populated with data from a profile.</span></span> <span data-ttu-id="bde79-122">Использует индекс взаимного исключения для обнаружения нужных взаимоисключающих сведений.</span><span class="sxs-lookup"><span data-stu-id="bde79-122">Uses the mutual exclusion index to identify the desired mutual exclusion information.</span></span> |



 

<span data-ttu-id="bde79-123">Оба метода в приведенной выше таблице устанавливают указатель на интерфейс **ивммутуалексклусион** .</span><span class="sxs-lookup"><span data-stu-id="bde79-123">Both methods in the preceding table set a pointer to an **IWMMutualExclusion** interface.</span></span> <span data-ttu-id="bde79-124">Интерфейс **ивмстреамлист** наследуется **ивммутуалексклусион** и никогда не должен обращаться к нему напрямую.</span><span class="sxs-lookup"><span data-stu-id="bde79-124">The **IWMStreamList** interface is inherited by **IWMMutualExclusion** and never needs to be accessed directly.</span></span> <span data-ttu-id="bde79-125">Другой интерфейс взаимоисключающего объекта можно получить, вызвав метод **QueryInterface** .</span><span class="sxs-lookup"><span data-stu-id="bde79-125">The other interface of the mutual exclusion object can be obtained by calling the **QueryInterface** method.</span></span>

<span data-ttu-id="bde79-126">Каждый объект взаимного исключения поддерживает следующие интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="bde79-126">The following interfaces are supported by every mutual exclusion object.</span></span>



| <span data-ttu-id="bde79-127">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="bde79-127">Interface</span></span>                                          | <span data-ttu-id="bde79-128">Описание</span><span class="sxs-lookup"><span data-stu-id="bde79-128">Description</span></span>                                                                                                                                            |
|----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bde79-129">**ивммутуалексклусион**</span><span class="sxs-lookup"><span data-stu-id="bde79-129">**IWMMutualExclusion**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion)   | <span data-ttu-id="bde79-130">Задает и получает тип используемого взаимоисключающего исключения.</span><span class="sxs-lookup"><span data-stu-id="bde79-130">Sets and retrieves the type of mutual exclusion to be used.</span></span>                                                                                            |
| [<span data-ttu-id="bde79-131">**IWMMutualExclusion2**</span><span class="sxs-lookup"><span data-stu-id="bde79-131">**IWMMutualExclusion2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion2) | <span data-ttu-id="bde79-132">Упорядочивает потоки по записям, которые можно использовать для создания сложных сценариев взаимного исключения.</span><span class="sxs-lookup"><span data-stu-id="bde79-132">Organizes streams into records, which can be used to create complex mutual exclusion scenarios.</span></span> <span data-ttu-id="bde79-133">Наследует все методы **ивммутуалексклусион**.</span><span class="sxs-lookup"><span data-stu-id="bde79-133">Inherits all of the methods of **IWMMutualExclusion**.</span></span> |
| [<span data-ttu-id="bde79-134">**ивмстреамлист**</span><span class="sxs-lookup"><span data-stu-id="bde79-134">**IWMStreamList**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamlist)             | <span data-ttu-id="bde79-135">Управляет списком взаимоисключающих потоков.</span><span class="sxs-lookup"><span data-stu-id="bde79-135">Manages the list of mutually exclusive streams.</span></span>                                                                                                        |



 

## <a name="related-topics"></a><span data-ttu-id="bde79-136">См. также</span><span class="sxs-lookup"><span data-stu-id="bde79-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bde79-137">**Взаимное исключение**</span><span class="sxs-lookup"><span data-stu-id="bde79-137">**Mutual Exclusion**</span></span>](mutual-exclusion.md)
</dt> <dt>

[<span data-ttu-id="bde79-138">**Объекты**</span><span class="sxs-lookup"><span data-stu-id="bde79-138">**Objects**</span></span>](objects.md)
</dt> <dt>

[<span data-ttu-id="bde79-139">**Объект диспетчера профилей**</span><span class="sxs-lookup"><span data-stu-id="bde79-139">**Profile Manager Object**</span></span>](profile-manager-object.md)
</dt> </dl>

 

 




