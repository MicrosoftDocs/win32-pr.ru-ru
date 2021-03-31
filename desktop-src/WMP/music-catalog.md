---
title: Каталог музыки
description: Каталог музыки
ms.assetid: d7ebf37f-00ae-4978-a63d-9d13741724f5
keywords:
- Интернет-магазины проигрывателя Windows Media, музыкальные каталоги
- Интернет-магазины, музыкальные каталоги
- Тип 1 Интернет-магазины, музыкальные каталоги
- Интернет-магазины проигрывателя Windows Media, компилятор каталогов
- Интернет-магазины, компилятор каталогов
- Тип 1 Интернет-магазины, компилятор каталога
- каталоги музыки
- компилятор каталога
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 479a74393ee4d853f591cb6d75eef8be741c9228
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "104069538"
---
# <a name="music-catalog"></a><span data-ttu-id="95f1c-111">Каталог музыки</span><span class="sxs-lookup"><span data-stu-id="95f1c-111">Music Catalog</span></span>

<span data-ttu-id="95f1c-112">Интернет-магазин типа 1 создает свой музыкальный каталог в виде набора файлов с разделителями-табуляциями (TSV).</span><span class="sxs-lookup"><span data-stu-id="95f1c-112">A type 1 online store creates its music catalog as a set of tab-separated-value (TSV) files.</span></span> <span data-ttu-id="95f1c-113">Затем Интернет-магазин использует [компилятор каталога](catalog-compiler-for-type-1-online-stores.md) Майкрософт для компиляции TSV-файлов в сжатый каталог, который может быть загружен проигрывателем Windows Media.</span><span class="sxs-lookup"><span data-stu-id="95f1c-113">Then the online store uses Microsoft's [catalog compiler](catalog-compiler-for-type-1-online-stores.md) to compile the TSV files into a compressed catalog that can be downloaded by Windows Media Player.</span></span> <span data-ttu-id="95f1c-114">Проигрыватель Windows Media может скачивать файлы полного каталога или файлы обновления каталога.</span><span class="sxs-lookup"><span data-stu-id="95f1c-114">Windows Media Player can download full catalog files or catalog update files.</span></span> <span data-ttu-id="95f1c-115">Обновления каталога содержат только сведения о каталоге, которые были изменены с момента последнего обновления каталога.</span><span class="sxs-lookup"><span data-stu-id="95f1c-115">Catalog updates contain only the catalog information that has changed since the last catalog update.</span></span> <span data-ttu-id="95f1c-116">Для определения необходимости загрузки полного каталога или обновления используется подключаемый модуль партнера по содержимому.</span><span class="sxs-lookup"><span data-stu-id="95f1c-116">It is up to the content partner plug-in to determine whether to download a full catalog or an update.</span></span> <span data-ttu-id="95f1c-117">В любом случае проигрыватель Windows Media применяет изменения к текущему каталогу при уведомлении от подключаемого модуля.</span><span class="sxs-lookup"><span data-stu-id="95f1c-117">In either case, Windows Media Player applies the changes to the current catalog upon notification from the plug-in.</span></span>

<span data-ttu-id="95f1c-118">Если в Интернет-магазине был подготовлен новый каталог, подключаемый модуль может уведомить игрока, вызвав [ивмпконтентпартнеркаллбакк:: notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-notify) и передав вмпкнневкаталогаваилабле в качестве значения параметра *типа* .</span><span class="sxs-lookup"><span data-stu-id="95f1c-118">If the online store has a new catalog prepared, the plug-in can notify the Player by calling [IWMPContentPartnerCallback::Notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-notify) and passing wmpcnNewCatalogAvailable as the value for the *type* parameter.</span></span>

<span data-ttu-id="95f1c-119">Когда проигрыватель Windows Media готов загрузить каталог или обновление, игрок вызывает [ивмпконтентпартнер:: жеткаталогурл](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcatalogurl).</span><span class="sxs-lookup"><span data-stu-id="95f1c-119">When Windows Media Player is ready to download a catalog or update, the Player calls [IWMPContentPartner::GetCatalogURL](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcatalogurl).</span></span> <span data-ttu-id="95f1c-120">Этот метод предоставляет подключаемому модулю сведения о текущем каталоге, такие как версия каталога и идентификатор локали.</span><span class="sxs-lookup"><span data-stu-id="95f1c-120">This method provides the plug-in with information about the current catalog, such as the catalog version and locale identifier.</span></span> <span data-ttu-id="95f1c-121">Подключаемый модуль отвечает, предоставляя универсальный указатель ресурсов (URL) правильного полного каталога или обновления, а также обновленный номер версии и дату окончания срока действия.</span><span class="sxs-lookup"><span data-stu-id="95f1c-121">The plug-in responds by supplying the uniform resource locator (URL) of the correct full catalog or update, as well as an updated version number and expiration date.</span></span> <span data-ttu-id="95f1c-122">Проигрыватель Windows Media будет периодически запрашивать обновления каталога на основе сведений, предоставленных подключаемым модулем в **жеткаталогурл**.</span><span class="sxs-lookup"><span data-stu-id="95f1c-122">Windows Media Player will periodically request catalog updates based upon the information provided by the plug-in in **GetCatalogURL**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="95f1c-123">См. также</span><span class="sxs-lookup"><span data-stu-id="95f1c-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="95f1c-124">**Сведения об Интернет-магазинах типа 1**</span><span class="sxs-lookup"><span data-stu-id="95f1c-124">**About Type 1 Online Stores**</span></span>](about-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="95f1c-125">**Компилятор каталога для Интернет-магазинов типа 1**</span><span class="sxs-lookup"><span data-stu-id="95f1c-125">**Catalog Compiler for Type 1 Online Stores**</span></span>](catalog-compiler-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="95f1c-126">**Интерфейс Ивмпконтентпартнер**</span><span class="sxs-lookup"><span data-stu-id="95f1c-126">**IWMPContentPartner Interface**</span></span>](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner)
</dt> </dl>

 

 




