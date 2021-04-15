---
description: Интерфейс Иамтимелинетракк предоставляет методы для управления объектами Track в службах редактирования DirectShow (DES). Запись содержит список источников, отображаемых в окончательном выводе.
ms.assetid: 42ac88f2-1361-413a-a9b0-95f5c32a7c3c
title: Интерфейс Иамтимелинетракк (Кедит. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 71003694d33b33980fb262f06f6b2e7aa55a70d1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689450"
---
# <a name="iamtimelinetrack-interface"></a><span data-ttu-id="bce66-103">Интерфейс Иамтимелинетракк</span><span class="sxs-lookup"><span data-stu-id="bce66-103">IAMTimelineTrack interface</span></span>

> [!Note]  
> <span data-ttu-id="bce66-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="bce66-104">\[Deprecated.</span></span> <span data-ttu-id="bce66-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="bce66-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="bce66-106">`IAMTimelineTrack`Интерфейс предоставляет методы для управления объектами *Track* в [службах редактирования DirectShow](directshow-editing-services.md) (DES).</span><span class="sxs-lookup"><span data-stu-id="bce66-106">The `IAMTimelineTrack` interface provides methods for manipulating *track* objects in [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span>

<span data-ttu-id="bce66-107">Запись содержит список источников, отображаемых в окончательном выводе.</span><span class="sxs-lookup"><span data-stu-id="bce66-107">A track contains a list of sources that are rendered in the final output.</span></span> <span data-ttu-id="bce66-108">Источники внутри одной и той же записи могут не перекрываться.</span><span class="sxs-lookup"><span data-stu-id="bce66-108">Sources within the same track may not overlap.</span></span> <span data-ttu-id="bce66-109">Видеодорожки могут иметь и эффекты, и переходы.</span><span class="sxs-lookup"><span data-stu-id="bce66-109">Video tracks can have both effects and transitions.</span></span> <span data-ttu-id="bce66-110">Подсистема подготовки отчетов применяет эффекты перед применением переходов.</span><span class="sxs-lookup"><span data-stu-id="bce66-110">The render engine applies effects before it applies transitions.</span></span> <span data-ttu-id="bce66-111">Звуковые дорожки могут иметь эффекты, но не переходы.</span><span class="sxs-lookup"><span data-stu-id="bce66-111">Audio tracks can have effects, but not transitions.</span></span> <span data-ttu-id="bce66-112">Дополнительные сведения см. [в разделе Модель временной шкалы](the-timeline-model.md).</span><span class="sxs-lookup"><span data-stu-id="bce66-112">For more information, see [The Timeline Model](the-timeline-model.md).</span></span>

<span data-ttu-id="bce66-113">Чтобы создать объект Track, вызовите [**иамтимелине:: креатимптиноде**](iamtimeline-createemptynode.md) со значением \_ Track основного типа временной шкалы \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="bce66-113">To create a track object, call [**IAMTimeline::CreateEmptyNode**](iamtimeline-createemptynode.md) with the value TIMELINE\_MAJOR\_TYPE\_TRACK.</span></span> <span data-ttu-id="bce66-114">Вы можете запросить возвращенный указатель **иамтимелинеобж** для `IAMTimelineTrack` интерфейса.</span><span class="sxs-lookup"><span data-stu-id="bce66-114">You can query the returned **IAMTimelineObj** pointer for the `IAMTimelineTrack` interface.</span></span>

## <a name="members"></a><span data-ttu-id="bce66-115">Элементы</span><span class="sxs-lookup"><span data-stu-id="bce66-115">Members</span></span>

<span data-ttu-id="bce66-116">Интерфейс **иамтимелинетракк** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="bce66-116">The **IAMTimelineTrack** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="bce66-117">**Иамтимелинетракк** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="bce66-117">**IAMTimelineTrack** also has these types of members:</span></span>

-   [<span data-ttu-id="bce66-118">Методы</span><span class="sxs-lookup"><span data-stu-id="bce66-118">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="bce66-119">Методы</span><span class="sxs-lookup"><span data-stu-id="bce66-119">Methods</span></span>

<span data-ttu-id="bce66-120">Интерфейс **иамтимелинетракк** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="bce66-120">The **IAMTimelineTrack** interface has these methods.</span></span>



| <span data-ttu-id="bce66-121">Метод</span><span class="sxs-lookup"><span data-stu-id="bce66-121">Method</span></span>                                                          | <span data-ttu-id="bce66-122">Описание</span><span class="sxs-lookup"><span data-stu-id="bce66-122">Description</span></span>                                                                                                                                          |
|:----------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bce66-123">**арэйаубланк**</span><span class="sxs-lookup"><span data-stu-id="bce66-123">**AreYouBlank**</span></span>](iamtimelinetrack-areyoublank.md)             | <span data-ttu-id="bce66-124">Определяет, пуста ли запись (не содержит исходных объектов).</span><span class="sxs-lookup"><span data-stu-id="bce66-124">Determines whether the track is blank (contains no source objects).</span></span><br/>                                                                       |
| [<span data-ttu-id="bce66-125">**жетнекстсрк**</span><span class="sxs-lookup"><span data-stu-id="bce66-125">**GetNextSrc**</span></span>](iamtimelinetrack-getnextsrc.md)               | <span data-ttu-id="bce66-126">Поиск следующего источника, отображаемого в указанное время или более поздней версии, в дорожке.</span><span class="sxs-lookup"><span data-stu-id="bce66-126">Searches the track for the next source that appears at the specified time or later.</span></span><br/>                                                       |
| [<span data-ttu-id="bce66-127">**GetNextSrc2**</span><span class="sxs-lookup"><span data-stu-id="bce66-127">**GetNextSrc2**</span></span>](iamtimelinetrack-getnextsrc2.md)             | <span data-ttu-id="bce66-128">Выполняет поиск следующего источника, который отображается в указанное время или более поздней версии, с заданным в качестве значения [**рефтиме**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="bce66-128">Searches the track for the next source that appears at the specified time or later, with the given as a [**REFTIME**](reftime.md) value.</span></span><br/> |
| [<span data-ttu-id="bce66-129">**жетнекстсрцекс**</span><span class="sxs-lookup"><span data-stu-id="bce66-129">**GetNextSrcEx**</span></span>](iamtimelinetrack-getnextsrcex.md)           | <span data-ttu-id="bce66-130">Извлекает следующий источник после указанного источника.</span><span class="sxs-lookup"><span data-stu-id="bce66-130">Retrieves the next source after the specified source.</span></span><br/>                                                                                     |
| [<span data-ttu-id="bce66-131">**жетсаурцескаунт**</span><span class="sxs-lookup"><span data-stu-id="bce66-131">**GetSourcesCount**</span></span>](iamtimelinetrack-getsourcescount.md)     | <span data-ttu-id="bce66-132">Возвращает количество источников в дорожке.</span><span class="sxs-lookup"><span data-stu-id="bce66-132">Retrieves the number of sources in the track.</span></span><br/>                                                                                             |
| [<span data-ttu-id="bce66-133">**жетсркаттиме**</span><span class="sxs-lookup"><span data-stu-id="bce66-133">**GetSrcAtTime**</span></span>](iamtimelinetrack-getsrcattime.md)           | <span data-ttu-id="bce66-134">Извлекает исходный объект, ближайший к указанному времени, в соответствии с указанными условиями границ.</span><span class="sxs-lookup"><span data-stu-id="bce66-134">Retrieves the source object nearest to the specified time, according to the specified boundary conditions.</span></span><br/>                                |
| [<span data-ttu-id="bce66-135">**GetSrcAtTime2**</span><span class="sxs-lookup"><span data-stu-id="bce66-135">**GetSrcAtTime2**</span></span>](iamtimelinetrack-getsrcattime2.md)         | <span data-ttu-id="bce66-136">Получает исходный объект, ближайший к указанному времени, заданный как значение [**рефтиме**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="bce66-136">Retrieves the source object nearest to the specified time, given as a [**REFTIME**](reftime.md) value.</span></span><br/>                                   |
| [<span data-ttu-id="bce66-137">**инсертспаце**</span><span class="sxs-lookup"><span data-stu-id="bce66-137">**InsertSpace**</span></span>](iamtimelinetrack-insertspace.md)             | <span data-ttu-id="bce66-138">Разделяет все объекты, существующие в указанное время, и вставляет между ними пробелы.</span><span class="sxs-lookup"><span data-stu-id="bce66-138">Splits any objects that exist at the specified time and inserts space between them.</span></span><br/>                                                       |
| [<span data-ttu-id="bce66-139">**InsertSpace2**</span><span class="sxs-lookup"><span data-stu-id="bce66-139">**InsertSpace2**</span></span>](iamtimelinetrack-insertspace2.md)           | <span data-ttu-id="bce66-140">Разделяет все объекты, существующие в указанное время, и вставляет пробел между ними, используя значения [**рефтиме**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="bce66-140">Splits any objects that exist at the specified time and inserts space between them, using [**REFTIME**](reftime.md) values.</span></span><br/>              |
| [<span data-ttu-id="bce66-141">**мовиверисингби**</span><span class="sxs-lookup"><span data-stu-id="bce66-141">**MoveEverythingBy**</span></span>](iamtimelinetrack-moveeverythingby.md)   | <span data-ttu-id="bce66-142">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="bce66-142">Not supported.</span></span><br/>                                                                                                                            |
| [<span data-ttu-id="bce66-143">**MoveEverythingBy2**</span><span class="sxs-lookup"><span data-stu-id="bce66-143">**MoveEverythingBy2**</span></span>](iamtimelinetrack-moveeverythingby2.md) | <span data-ttu-id="bce66-144">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="bce66-144">Not supported.</span></span><br/>                                                                                                                            |
| [<span data-ttu-id="bce66-145">**сркадд**</span><span class="sxs-lookup"><span data-stu-id="bce66-145">**SrcAdd**</span></span>](iamtimelinetrack-srcadd.md)                       | <span data-ttu-id="bce66-146">Добавляет источник к дорожке.</span><span class="sxs-lookup"><span data-stu-id="bce66-146">Adds a source to the track.</span></span><br/>                                                                                                               |
| [<span data-ttu-id="bce66-147">**зеробетвин**</span><span class="sxs-lookup"><span data-stu-id="bce66-147">**ZeroBetween**</span></span>](iamtimelinetrack-zerobetween.md)             | <span data-ttu-id="bce66-148">Удаляет все, начиная с курса, в указанное время.</span><span class="sxs-lookup"><span data-stu-id="bce66-148">Removes everything from the track between the specified times.</span></span><br/>                                                                            |
| [<span data-ttu-id="bce66-149">**ZeroBetween2**</span><span class="sxs-lookup"><span data-stu-id="bce66-149">**ZeroBetween2**</span></span>](iamtimelinetrack-zerobetween2.md)           | <span data-ttu-id="bce66-150">Удаляет все, начиная с курса, с указанного времени в виде значений [**рефтиме**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="bce66-150">Removes everything from the track between the specified times, given as [**REFTIME**](reftime.md) values.</span></span><br/>                                |



 

## <a name="remarks"></a><span data-ttu-id="bce66-151">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bce66-151">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="bce66-152">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="bce66-152">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="bce66-153">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="bce66-153">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="bce66-154">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="bce66-154">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="bce66-155">Требования</span><span class="sxs-lookup"><span data-stu-id="bce66-155">Requirements</span></span>



| <span data-ttu-id="bce66-156">Требование</span><span class="sxs-lookup"><span data-stu-id="bce66-156">Requirement</span></span> | <span data-ttu-id="bce66-157">Значение</span><span class="sxs-lookup"><span data-stu-id="bce66-157">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bce66-158">Header</span><span class="sxs-lookup"><span data-stu-id="bce66-158">Header</span></span><br/>  | <dl> <span data-ttu-id="bce66-159"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="bce66-159"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="bce66-160">Библиотека</span><span class="sxs-lookup"><span data-stu-id="bce66-160">Library</span></span><br/> | <dl> <span data-ttu-id="bce66-161"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bce66-161"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 
