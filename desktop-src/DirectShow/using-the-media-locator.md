---
description: Использование указателя мультимедиа
ms.assetid: 07840a37-7065-41e8-aee5-855c9f89fb77
title: Использование указателя мультимедиа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fce934b06d92c0bec66d9260a485516d3acaf5a9
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "103999859"
---
# <a name="using-the-media-locator"></a><span data-ttu-id="6858b-103">Использование указателя мультимедиа</span><span class="sxs-lookup"><span data-stu-id="6858b-103">Using the Media Locator</span></span>

<span data-ttu-id="6858b-104">\[Этот API не поддерживается и может быть изменен или недоступен в будущем.\]</span><span class="sxs-lookup"><span data-stu-id="6858b-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="6858b-105">Указатель мультимедиа — это вспомогательный объект, который проверяет имена файлов и ищет недостающие файлы в локальных или сетевых каталогах.</span><span class="sxs-lookup"><span data-stu-id="6858b-105">The media locator is a helper object that verifies file names and searches for missing files on local or network directories.</span></span> <span data-ttu-id="6858b-106">Средство обнаружения мультимедиа сохраняет кэш путей к каталогам, в которых файлы успешно найдены в прошлых поисках.</span><span class="sxs-lookup"><span data-stu-id="6858b-106">The media detector keeps a cache of directory paths where it has successfully found files in past searches.</span></span> <span data-ttu-id="6858b-107">Чтобы найти файл, он выполняет поиск в каталогах в кэше.</span><span class="sxs-lookup"><span data-stu-id="6858b-107">To locate a file, it searches the directories in its cache.</span></span> <span data-ttu-id="6858b-108">В этом случае средство обнаружения мультимедиа может отобразить диалоговое окно открытия файла для того, чтобы пользователь мог выбрать файл вручную.</span><span class="sxs-lookup"><span data-stu-id="6858b-108">Failing that, the media detector can display an Open File dialog for the user to locate a file manually.</span></span> <span data-ttu-id="6858b-109">Предполагая, что пользователь найдет файл, указатель носителя добавляет новый каталог в свой кэш.</span><span class="sxs-lookup"><span data-stu-id="6858b-109">Assuming the user locates the file, the media locator adds the new directory to its cache.</span></span> <span data-ttu-id="6858b-110">Указатель мультимедиа предоставляет интерфейс [**имедиалокатор**](imedialocator.md) .</span><span class="sxs-lookup"><span data-stu-id="6858b-110">The media locator exposes the [**IMediaLocator**](imedialocator.md) interface.</span></span>

<span data-ttu-id="6858b-111">Как правило, приложение не создает экземпляр указателя мультимедиа напрямую.</span><span class="sxs-lookup"><span data-stu-id="6858b-111">Typically, your application does not directly create an instance of the media locator.</span></span> <span data-ttu-id="6858b-112">Вместо этого временная шкала и подсистема визуализации предоставляют следующие методы проверки имен файлов с помощью средства обнаружения мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="6858b-112">Instead, the timeline and the render engine provide the following methods for validating file names using the media detector.</span></span>

-   <span data-ttu-id="6858b-113">Чтобы проверить имена файлов на временной шкале, вызовите метод [**иамтимелине:: валидатесаурценамес**](iamtimeline-validatesourcenames.md).</span><span class="sxs-lookup"><span data-stu-id="6858b-113">To validate file names in the timeline, call [**IAMTimeline::ValidateSourceNames**](iamtimeline-validatesourcenames.md).</span></span> <span data-ttu-id="6858b-114">При необходимости этот метод также обновляет исходные объекты с использованием правильных имен файлов.</span><span class="sxs-lookup"><span data-stu-id="6858b-114">Optionally, this method also updates the source objects with the correct file names.</span></span>
-   <span data-ttu-id="6858b-115">Чтобы проверить имена файлов при подготовке проекта к просмотру, вызовите метод [**ирендеренгине:: сетсаурценамевалидатион**](irenderengine-setsourcenamevalidation.md).</span><span class="sxs-lookup"><span data-stu-id="6858b-115">To validate file names when the project is rendered, call [**IRenderEngine::SetSourceNameValidation**](irenderengine-setsourcenamevalidation.md).</span></span>

<span data-ttu-id="6858b-116">Оба метода принимают флаги, управляющие поведением указателя мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="6858b-116">Both methods take flags that control the behavior of the media locator.</span></span> <span data-ttu-id="6858b-117">Например, можно ограничить поиск локальными каталогами.</span><span class="sxs-lookup"><span data-stu-id="6858b-117">For example, you can restrict the search to local directories.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6858b-118">См. также</span><span class="sxs-lookup"><span data-stu-id="6858b-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6858b-119">Работа с источниками</span><span class="sxs-lookup"><span data-stu-id="6858b-119">Working with Sources</span></span>](working-with-sources.md)
</dt> </dl>

 

 



