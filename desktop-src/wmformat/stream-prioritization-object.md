---
title: Объект определения приоритетов потоков
description: Объект определения приоритетов потоков
ms.assetid: cb0345ce-6847-435b-8cbb-f8b93856af9f
keywords:
- Пакет SDK для формата Windows Media, объекты определения приоритетов потоков
- Расширенный системный формат (ASF), объекты определения приоритетов потоков
- ASF (Расширенный системный формат), объекты определения приоритетов потоков
- объекты, объекты определения приоритетов потоков
- объекты определения приоритетов потоков
- потоки, объекты определения приоритетов потоков
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cce4189f64e85cca4e0d649dbc00409cf9d7c06
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "105719106"
---
# <a name="stream-prioritization-object"></a><span data-ttu-id="1bb72-109">Объект определения приоритетов потоков</span><span class="sxs-lookup"><span data-stu-id="1bb72-109">Stream Prioritization Object</span></span>

<span data-ttu-id="1bb72-110">Объект определения приоритетов потоков используется для указания порядка важности потоков в профиле.</span><span class="sxs-lookup"><span data-stu-id="1bb72-110">A stream prioritization object is used to specify an order of importance for the streams in a profile.</span></span> <span data-ttu-id="1bb72-111">Если полное воспроизведение невозможно из-за ограничений скорости, то первыми будут удалены потоки с наименьшим приоритетом.</span><span class="sxs-lookup"><span data-stu-id="1bb72-111">When full playback is not possible due to bit-rate limitations, the lowest priority streams will be the first to be dropped.</span></span>

<span data-ttu-id="1bb72-112">Объекты определения приоритетов потоков могут быть созданы для существующих данных определения приоритетов потоков в профиле или могут быть созданы пустыми, готовыми для получения новых данных.</span><span class="sxs-lookup"><span data-stu-id="1bb72-112">Stream prioritization objects can be created for existing stream prioritization data in a profile or can be created empty, ready to receive new data.</span></span> <span data-ttu-id="1bb72-113">Объекты определения приоритетов потоков не могут существовать независимо от объекта профиля.</span><span class="sxs-lookup"><span data-stu-id="1bb72-113">Stream prioritization objects cannot exist independently of a profile object.</span></span> <span data-ttu-id="1bb72-114">Чтобы сохранить содержимое объекта определения приоритетов потоков, необходимо вызвать метод [**IWMProfile3:: сетстреамприоритизатион**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-setstreamprioritization).</span><span class="sxs-lookup"><span data-stu-id="1bb72-114">To save the contents of a stream prioritization object, you must call [**IWMProfile3::SetStreamPrioritization**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-setstreamprioritization).</span></span> <span data-ttu-id="1bb72-115">Чтобы создать объект определения приоритетов потоков, используйте один из следующих методов.</span><span class="sxs-lookup"><span data-stu-id="1bb72-115">To create a stream prioritization object, use one of the following methods.</span></span>



| <span data-ttu-id="1bb72-116">Метод</span><span class="sxs-lookup"><span data-stu-id="1bb72-116">Method</span></span>                                                                                          | <span data-ttu-id="1bb72-117">Описание</span><span class="sxs-lookup"><span data-stu-id="1bb72-117">Description</span></span>                                                                  |
|-------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [<span data-ttu-id="1bb72-118">**IWMProfile3:: Креатеневстреамприоритизатион**</span><span class="sxs-lookup"><span data-stu-id="1bb72-118">**IWMProfile3::CreateNewStreamPrioritization**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-createnewstreamprioritization) | <span data-ttu-id="1bb72-119">Создает объект определения приоритетов потоков без каких-либо данных.</span><span class="sxs-lookup"><span data-stu-id="1bb72-119">Creates a stream prioritization object without any data.</span></span>                     |
| [<span data-ttu-id="1bb72-120">**IWMProfile3:: Жетстреамприоритизатион**</span><span class="sxs-lookup"><span data-stu-id="1bb72-120">**IWMProfile3::GetStreamPrioritization**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-getstreamprioritization)             | <span data-ttu-id="1bb72-121">Создает объект определения приоритетов потоков, заполненный данными из профиля.</span><span class="sxs-lookup"><span data-stu-id="1bb72-121">Creates a stream prioritization object populated with data from the profile.</span></span> |



 

<span data-ttu-id="1bb72-122">Оба метода в приведенной выше таблице устанавливают указатель на интерфейс **ивмстреамприоритизатион** .</span><span class="sxs-lookup"><span data-stu-id="1bb72-122">Both methods in the preceding table set a pointer to an **IWMStreamPrioritization** interface.</span></span> <span data-ttu-id="1bb72-123">Это единственный интерфейс, поддерживаемый объектом определения приоритетов потоков.</span><span class="sxs-lookup"><span data-stu-id="1bb72-123">This is the only interface supported by the stream prioritization object.</span></span>



| <span data-ttu-id="1bb72-124">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="1bb72-124">Interface</span></span>                                                  | <span data-ttu-id="1bb72-125">Описание</span><span class="sxs-lookup"><span data-stu-id="1bb72-125">Description</span></span>                                                          |
|------------------------------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="1bb72-126">**ивмстреамприоритизатион**</span><span class="sxs-lookup"><span data-stu-id="1bb72-126">**IWMStreamPrioritization**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamprioritization) | <span data-ttu-id="1bb72-127">Управляет списком потоков в объекте определения приоритетов потоков.</span><span class="sxs-lookup"><span data-stu-id="1bb72-127">Manages the list of streams within the stream prioritization object.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="1bb72-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1bb72-128">Remarks</span></span>

<span data-ttu-id="1bb72-129">Для данного профиля может существовать только одно определение приоритетов потоков.</span><span class="sxs-lookup"><span data-stu-id="1bb72-129">Only one stream prioritization can exist for a given profile.</span></span> <span data-ttu-id="1bb72-130">При создании нового приоритета потока для профиля, который уже содержит определение приоритетов потоков, старый объект будет удален.</span><span class="sxs-lookup"><span data-stu-id="1bb72-130">If you create a new stream prioritization for a profile that already contains a stream prioritization, the old one will be deleted.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1bb72-131">См. также</span><span class="sxs-lookup"><span data-stu-id="1bb72-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1bb72-132">**Объекты**</span><span class="sxs-lookup"><span data-stu-id="1bb72-132">**Objects**</span></span>](objects.md)
</dt> <dt>

[<span data-ttu-id="1bb72-133">**Объект Profile**</span><span class="sxs-lookup"><span data-stu-id="1bb72-133">**Profile Object**</span></span>](profile-object.md)
</dt> <dt>

[<span data-ttu-id="1bb72-134">**Использование определения приоритетов потоков**</span><span class="sxs-lookup"><span data-stu-id="1bb72-134">**Using Stream Prioritization**</span></span>](using-stream-prioritization.md)
</dt> </dl>

 

 




