---
description: Msitran.exe использует Мсидатабасеженератетрансформ, Мсикреатетрансформсуммаринфо и Мсидатабасеапплитрансформ для создания или применения файла преобразования. Это средство доступно только в компонентах Windows SDK для разработчиков установщик Windows.
ms.assetid: cfc7b907-78d7-4a78-bab4-ede9012d5a36
title: Msitran.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a69936155fb3880f43e0f7563bc6aabd59f53703
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674154"
---
# <a name="msitranexe"></a><span data-ttu-id="df6b5-103">Msitran.exe</span><span class="sxs-lookup"><span data-stu-id="df6b5-103">Msitran.exe</span></span>

<span data-ttu-id="df6b5-104">Msitran.exe использует [**мсидатабасеженератетрансформ**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegeneratetransforma), [**мсикреатетрансформсуммаринфо**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa)и [**мсидатабасеапплитрансформ**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseapplytransforma) для создания или применения файла преобразования.</span><span class="sxs-lookup"><span data-stu-id="df6b5-104">Msitran.exe uses [**MsiDatabaseGenerateTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegeneratetransforma), [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa), and [**MsiDatabaseApplyTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseapplytransforma) to generate or apply a transform file.</span></span>

<span data-ttu-id="df6b5-105">Это средство доступно только в [компонентах Windows SDK для разработчиков установщик Windows](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="df6b5-105">This tool is only available in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="df6b5-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="df6b5-106">Syntax</span></span>

<span data-ttu-id="df6b5-107">Для создания преобразования используйте следующий синтаксис.</span><span class="sxs-lookup"><span data-stu-id="df6b5-107">Use the following syntax to generate a transform.</span></span>

<span data-ttu-id="df6b5-108">**мситран-g** *{base DB} {ref DB} {имя файла преобразования} \[ {условия ошибок/условия проверки} \]*</span><span class="sxs-lookup"><span data-stu-id="df6b5-108">**msitran -g** *{base db}{ref db}{transform file name}\[{error conditions / validation conditions}\]*</span></span>

<span data-ttu-id="df6b5-109">Используйте следующий синтаксис для применения преобразования</span><span class="sxs-lookup"><span data-stu-id="df6b5-109">Use the following syntax to apply a transform</span></span>

<span data-ttu-id="df6b5-110">**мситран-a** *{Преобразование} {Database} \[ {условия ошибки} \]*</span><span class="sxs-lookup"><span data-stu-id="df6b5-110">**msitran -a** *{transform}{database}\[{error conditions}\]*</span></span>

## <a name="command-line-options"></a><span data-ttu-id="df6b5-111">Параметры командной строки</span><span class="sxs-lookup"><span data-stu-id="df6b5-111">Command Line Options</span></span>

<span data-ttu-id="df6b5-112">В Msitran.exe используются следующие параметры командной строки без учета регистра.</span><span class="sxs-lookup"><span data-stu-id="df6b5-112">Msitran.exe uses the following case-insensitive command line options.</span></span> <span data-ttu-id="df6b5-113">Вместо тире можно использовать разделитель с косой чертой.</span><span class="sxs-lookup"><span data-stu-id="df6b5-113">A slash delimiter may also be used in place of a dash.</span></span>



| <span data-ttu-id="df6b5-114">Параметр</span><span class="sxs-lookup"><span data-stu-id="df6b5-114">Option</span></span> | <span data-ttu-id="df6b5-115">Описание</span><span class="sxs-lookup"><span data-stu-id="df6b5-115">Description</span></span>            |
|--------|------------------------|
| <span data-ttu-id="df6b5-116">-g</span><span class="sxs-lookup"><span data-stu-id="df6b5-116">-g</span></span>     | <span data-ttu-id="df6b5-117">Создание преобразования.</span><span class="sxs-lookup"><span data-stu-id="df6b5-117">Transform generation.</span></span>  |
| <span data-ttu-id="df6b5-118">-a</span><span class="sxs-lookup"><span data-stu-id="df6b5-118">-a</span></span>     | <span data-ttu-id="df6b5-119">Преобразование приложения.</span><span class="sxs-lookup"><span data-stu-id="df6b5-119">Transform application.</span></span> |



 

<span data-ttu-id="df6b5-120">При применении преобразования могут быть подавлены следующие ошибки.</span><span class="sxs-lookup"><span data-stu-id="df6b5-120">The following errors may be suppressed when applying a transform.</span></span> <span data-ttu-id="df6b5-121">Чтобы отключить ошибку, включите соответствующий символ в аргумент {error conditions}.</span><span class="sxs-lookup"><span data-stu-id="df6b5-121">To suppress an error, include the appropriate character in the {error conditions} argument.</span></span> <span data-ttu-id="df6b5-122">Условия, заданные параметром-g, помещаются в сводные данные преобразования, но не используются при применении преобразования с параметром-a.</span><span class="sxs-lookup"><span data-stu-id="df6b5-122">Conditions specified with -g are placed in the summary information of the transform, but are not used when applying a transform with -a.</span></span> <span data-ttu-id="df6b5-123">Дополнительные сведения см. в разделе [**мсидатабасеапплитрансформ**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseapplytransforma).</span><span class="sxs-lookup"><span data-stu-id="df6b5-123">For information, see [**MsiDatabaseApplyTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseapplytransforma).</span></span>



| <span data-ttu-id="df6b5-124">Параметр</span><span class="sxs-lookup"><span data-stu-id="df6b5-124">Option</span></span> | <span data-ttu-id="df6b5-125">Подавленная ошибка</span><span class="sxs-lookup"><span data-stu-id="df6b5-125">Suppressed error</span></span>           |
|--------|----------------------------|
| <span data-ttu-id="df6b5-126">а</span><span class="sxs-lookup"><span data-stu-id="df6b5-126">a</span></span>      | <span data-ttu-id="df6b5-127">Добавить существующую строку.</span><span class="sxs-lookup"><span data-stu-id="df6b5-127">Add existing row.</span></span>          |
| <span data-ttu-id="df6b5-128">b</span><span class="sxs-lookup"><span data-stu-id="df6b5-128">b</span></span>      | <span data-ttu-id="df6b5-129">Удаление несуществующей строки.</span><span class="sxs-lookup"><span data-stu-id="df6b5-129">Delete non-existing row.</span></span>   |
| <span data-ttu-id="df6b5-130">c</span><span class="sxs-lookup"><span data-stu-id="df6b5-130">c</span></span>      | <span data-ttu-id="df6b5-131">Добавить существующую таблицу.</span><span class="sxs-lookup"><span data-stu-id="df6b5-131">Add existing table.</span></span>        |
| <span data-ttu-id="df6b5-132">d</span><span class="sxs-lookup"><span data-stu-id="df6b5-132">d</span></span>      | <span data-ttu-id="df6b5-133">Удаление несуществующей таблицы.</span><span class="sxs-lookup"><span data-stu-id="df6b5-133">Delete non-existing table.</span></span> |
| <span data-ttu-id="df6b5-134">й</span><span class="sxs-lookup"><span data-stu-id="df6b5-134">e</span></span>      | <span data-ttu-id="df6b5-135">Изменить существующую строку.</span><span class="sxs-lookup"><span data-stu-id="df6b5-135">Modify existing row.</span></span>       |
| <span data-ttu-id="df6b5-136">f</span><span class="sxs-lookup"><span data-stu-id="df6b5-136">f</span></span>      | <span data-ttu-id="df6b5-137">Изменить кодовую страницу.</span><span class="sxs-lookup"><span data-stu-id="df6b5-137">Change codepage.</span></span>           |



 

<span data-ttu-id="df6b5-138">Для указания, когда преобразование может быть применено к пакету, можно использовать следующие условия проверки.</span><span class="sxs-lookup"><span data-stu-id="df6b5-138">The following validation conditions may be used to indicate when a transform may be applied to a package.</span></span> <span data-ttu-id="df6b5-139">Эти условия могут быть указаны с помощью-g, но не от-a.</span><span class="sxs-lookup"><span data-stu-id="df6b5-139">These conditions may be specified with -g, but not -a.</span></span>



| <span data-ttu-id="df6b5-140">Параметр</span><span class="sxs-lookup"><span data-stu-id="df6b5-140">Option</span></span> | <span data-ttu-id="df6b5-141">Условие проверки</span><span class="sxs-lookup"><span data-stu-id="df6b5-141">Validation condition</span></span>                                  |
|--------|-------------------------------------------------------|
| <span data-ttu-id="df6b5-142">н</span><span class="sxs-lookup"><span data-stu-id="df6b5-142">g</span></span>      | <span data-ttu-id="df6b5-143">Проверьте код обновления.</span><span class="sxs-lookup"><span data-stu-id="df6b5-143">Check upgrade code.</span></span>                                   |
| <span data-ttu-id="df6b5-144">l</span><span class="sxs-lookup"><span data-stu-id="df6b5-144">l</span></span>      | <span data-ttu-id="df6b5-145">Проверить язык.</span><span class="sxs-lookup"><span data-stu-id="df6b5-145">Check language.</span></span>                                       |
| <span data-ttu-id="df6b5-146">p</span><span class="sxs-lookup"><span data-stu-id="df6b5-146">p</span></span>      | <span data-ttu-id="df6b5-147">Проверка платформы.</span><span class="sxs-lookup"><span data-stu-id="df6b5-147">Check platform.</span></span>                                       |
| <span data-ttu-id="df6b5-148">r</span><span class="sxs-lookup"><span data-stu-id="df6b5-148">r</span></span>      | <span data-ttu-id="df6b5-149">Проверьте продукт.</span><span class="sxs-lookup"><span data-stu-id="df6b5-149">Check product.</span></span>                                        |
| <span data-ttu-id="df6b5-150">s</span><span class="sxs-lookup"><span data-stu-id="df6b5-150">s</span></span>      | <span data-ttu-id="df6b5-151">Проверьте только основной номер версии.</span><span class="sxs-lookup"><span data-stu-id="df6b5-151">Check major version only.</span></span>                             |
| <span data-ttu-id="df6b5-152">t</span><span class="sxs-lookup"><span data-stu-id="df6b5-152">t</span></span>      | <span data-ttu-id="df6b5-153">Проверьте только основной и дополнительный версии.</span><span class="sxs-lookup"><span data-stu-id="df6b5-153">Check major and minor versions only.</span></span>                  |
| <span data-ttu-id="df6b5-154">u</span><span class="sxs-lookup"><span data-stu-id="df6b5-154">u</span></span>      | <span data-ttu-id="df6b5-155">Проверьте основные, дополнительные и обновленные версии.</span><span class="sxs-lookup"><span data-stu-id="df6b5-155">Check major, minor, and upgrade versions.</span></span>             |
| <span data-ttu-id="df6b5-156">v</span><span class="sxs-lookup"><span data-stu-id="df6b5-156">v</span></span>      | <span data-ttu-id="df6b5-157">Примененная версия базы данных < версия базовой базы данных.</span><span class="sxs-lookup"><span data-stu-id="df6b5-157">Applied database version < Base database version.</span></span>  |
| <span data-ttu-id="df6b5-158">w</span><span class="sxs-lookup"><span data-stu-id="df6b5-158">w</span></span>      | <span data-ttu-id="df6b5-159">Примененная версия базы данных <= базовая версия базы данных.</span><span class="sxs-lookup"><span data-stu-id="df6b5-159">Applied database version <= Base database version.</span></span> |
| <span data-ttu-id="df6b5-160">x</span><span class="sxs-lookup"><span data-stu-id="df6b5-160">x</span></span>      | <span data-ttu-id="df6b5-161">Примененная версия базы данных = базовая версия базы данных.</span><span class="sxs-lookup"><span data-stu-id="df6b5-161">Applied database version = Base database version.</span></span>     |
| <span data-ttu-id="df6b5-162">да</span><span class="sxs-lookup"><span data-stu-id="df6b5-162">y</span></span>      | <span data-ttu-id="df6b5-163">Примененная версия базы данных >= базовая версия базы данных.</span><span class="sxs-lookup"><span data-stu-id="df6b5-163">Applied database version >= Base database version.</span></span> |
| <span data-ttu-id="df6b5-164">z</span><span class="sxs-lookup"><span data-stu-id="df6b5-164">z</span></span>      | <span data-ttu-id="df6b5-165">Примененная версия базы данных > версия базовой базы данных.</span><span class="sxs-lookup"><span data-stu-id="df6b5-165">Applied database version > Base database version.</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="df6b5-166">См. также</span><span class="sxs-lookup"><span data-stu-id="df6b5-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="df6b5-167">Средства разработки установщик Windows</span><span class="sxs-lookup"><span data-stu-id="df6b5-167">Windows Installer Development Tools</span></span>](windows-installer-development-tools.md)
</dt> <dt>

[<span data-ttu-id="df6b5-168">Преобразования баз данных</span><span class="sxs-lookup"><span data-stu-id="df6b5-168">Database Transforms</span></span>](database-transforms.md)
</dt> <dt>

[<span data-ttu-id="df6b5-169">Пример преобразования настройки</span><span class="sxs-lookup"><span data-stu-id="df6b5-169">A Customization Transform Example</span></span>](a-customization-transform-example.md)
</dt> <dt>

[<span data-ttu-id="df6b5-170">Выпущенные версии, средства и распространяемые пакеты</span><span class="sxs-lookup"><span data-stu-id="df6b5-170">Released Versions, Tools, and Redistributables</span></span>](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



