---
description: Подобъекты
ms.assetid: 03cbd590-b573-4a98-9ab7-fe548800cfcb
title: Подобъекты
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad8b427a315231577f1608a168629bc8b77d2cc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911700"
---
# <a name="subobjects"></a><span data-ttu-id="90c84-103">Подобъекты</span><span class="sxs-lookup"><span data-stu-id="90c84-103">Subobjects</span></span>

<span data-ttu-id="90c84-104">\[Этот API не поддерживается и может быть изменен или недоступен в будущем.\]</span><span class="sxs-lookup"><span data-stu-id="90c84-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="90c84-105">Источники, эффекты и переходы имеют внутренние указатели на другие COM-объекты, называемые *подобъектами*.</span><span class="sxs-lookup"><span data-stu-id="90c84-105">Sources, effects, and transitions have internal pointers to other COM objects, called *subobjects*.</span></span> <span data-ttu-id="90c84-106">Подобъект выполняет фактическую работу объекта.</span><span class="sxs-lookup"><span data-stu-id="90c84-106">The subobject performs the actual work of the object.</span></span> <span data-ttu-id="90c84-107">Подобъект источника — это компонент, который создает видео-или звуковые данные.</span><span class="sxs-lookup"><span data-stu-id="90c84-107">The subobject of a source is the component that creates the video or audio data.</span></span> <span data-ttu-id="90c84-108">Подобъект действия или перехода является компонентом, который преобразует данные. Например, в видеоролике он создает визуальный эффекты в видеопотоке.</span><span class="sxs-lookup"><span data-stu-id="90c84-108">The subobject of an effect or transition is the component that transforms the data; for example, in a video effect, it creates the visual effect in the video stream.</span></span>

<span data-ttu-id="90c84-109">Тип подобъекта зависит от типа объекта:</span><span class="sxs-lookup"><span data-stu-id="90c84-109">The type of subobject depends on the type of object:</span></span>

-   <span data-ttu-id="90c84-110">Источник: любой фильтр источника DirectShow или фильтр синтаксического анализатора, который поддерживает поиск и создает формат, поддерживаемый DES.</span><span class="sxs-lookup"><span data-stu-id="90c84-110">Source: Any DirectShow source filter or parser filter that supports seeking and produces a format that DES supports.</span></span> <span data-ttu-id="90c84-111">Это может быть сжатый формат, если существуют фильтры DirectShow для декодирования.</span><span class="sxs-lookup"><span data-stu-id="90c84-111">It can be a compressed format if DirectShow filters exist to decode it.</span></span>
-   <span data-ttu-id="90c84-112">Действие: для видео — любой из двух входных одноэлементных данных Microsoft® DirectX® Transform.</span><span class="sxs-lookup"><span data-stu-id="90c84-112">Effect: For video, any 2-D one-input Microsoft® DirectX® Transform object.</span></span> <span data-ttu-id="90c84-113">Для звука — любой фильтр для звуковых эффектов DirectShow.</span><span class="sxs-lookup"><span data-stu-id="90c84-113">For audio, any DirectShow audio effect filter.</span></span>
-   <span data-ttu-id="90c84-114">Переход: для видео — любой двухмерный входной объект преобразования DirectX с двумя D.</span><span class="sxs-lookup"><span data-stu-id="90c84-114">Transition: For video, any 2-D two-input DirectX Transform object.</span></span> <span data-ttu-id="90c84-115">Звук не поддерживает переходы.</span><span class="sxs-lookup"><span data-stu-id="90c84-115">Audio does not support transitions.</span></span>

<span data-ttu-id="90c84-116">Группы, композиции и дорожки не имеют подобъектов.</span><span class="sxs-lookup"><span data-stu-id="90c84-116">Groups, compositions, and tracks do not have subobjects.</span></span>

<span data-ttu-id="90c84-117">Приложение не устанавливает указатель на подобъект напрямую.</span><span class="sxs-lookup"><span data-stu-id="90c84-117">The application does not directly set the subobject pointer.</span></span> <span data-ttu-id="90c84-118">Для эффектов и переходов приложение вызывает метод [**иамтимелинеобж:: сетсубобжектгуид**](iamtimelineobj-setsubobjectguid.md) , чтобы указать идентификатор GUID подобъекта.</span><span class="sxs-lookup"><span data-stu-id="90c84-118">For effects and transitions, the application calls the [**IAMTimelineObj::SetSubObjectGUID**](iamtimelineobj-setsubobjectguid.md) method to specify the GUID of the subobject.</span></span> <span data-ttu-id="90c84-119">Для исходных объектов приложение обычно вызывает метод [**иамтимелинесрк:: сетмедианаме**](iamtimelinesrc-setmedianame.md) , чтобы указать имя исходного файла.</span><span class="sxs-lookup"><span data-stu-id="90c84-119">For source objects, an application typically calls the [**IAMTimelineSrc::SetMediaName**](iamtimelinesrc-setmedianame.md) to specify the name of a source file.</span></span> <span data-ttu-id="90c84-120">Однако метод **сетсубобжектгуид** можно также использовать для исходных объектов, чтобы указать идентификатор класса (CLSID) фильтра.</span><span class="sxs-lookup"><span data-stu-id="90c84-120">However, the **SetSubObjectGUID** method can also be used for source objects, to specify the class identifier (CLSID) of a filter.</span></span>

<span data-ttu-id="90c84-121">Дополнительные сведения см. в разделе [Работа с источниками](working-with-sources.md) и [Работа с эффектами и переходами](working-with-effects-and-transitions.md).</span><span class="sxs-lookup"><span data-stu-id="90c84-121">For more information, see [Working with Sources](working-with-sources.md) and [Working with Effects and Transitions](working-with-effects-and-transitions.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="90c84-122">См. также</span><span class="sxs-lookup"><span data-stu-id="90c84-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="90c84-123">Общие сведения о компонентах временной шкалы</span><span class="sxs-lookup"><span data-stu-id="90c84-123">Overview of the Timeline Components</span></span>](overview-of-the-timeline-components.md)
</dt> </dl>

 

 



