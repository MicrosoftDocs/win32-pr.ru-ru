---
title: Советы и рекомендации в отношении тестовых случаев для игр в Windows XP, Windows Vista, Windows 7 и Windows 8
description: В этой статье содержатся тестовые случаи для игр для Windows.
ms.assetid: bbe84d3f-e7ff-f14f-ec25-ae1c980749fe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b13a4934c539579e49c9b00c60f3603bd64c711
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120279"
---
# <a name="games-for-windows-test-cases-best-practices-for-games-on-windows-xp-windows-vista-windows-7-and-windows-8"></a><span data-ttu-id="987a3-103">Игры для тестовых случаев Windows: рекомендации по играм в Windows XP, Windows Vista, Windows 7 и Windows 8</span><span class="sxs-lookup"><span data-stu-id="987a3-103">Games for Windows Test Cases: Best Practices for Games on Windows XP, Windows Vista, Windows 7, and Windows 8</span></span>

<span data-ttu-id="987a3-104">В этой статье содержатся тестовые случаи для игр для Windows.</span><span class="sxs-lookup"><span data-stu-id="987a3-104">This article provides test cases for games for Windows.</span></span>

## <a name="how-to-use-this-article"></a><span data-ttu-id="987a3-105">Применение данной статьи</span><span class="sxs-lookup"><span data-stu-id="987a3-105">How to Use This Article</span></span>

<span data-ttu-id="987a3-106">Эта статья состоит из трех основных разделов:</span><span class="sxs-lookup"><span data-stu-id="987a3-106">There are three main sections to this article:</span></span>

<dl> <dt>

<span data-ttu-id="987a3-107"><span id="Test_Requirements"></span><span id="test_requirements"></span><span id="TEST_REQUIREMENTS"></span>**Требования к тестированию**</span><span class="sxs-lookup"><span data-stu-id="987a3-107"><span id="Test_Requirements"></span><span id="test_requirements"></span><span id="TEST_REQUIREMENTS"></span>**Test Requirements**</span></span>
</dt> <dd>

<span data-ttu-id="987a3-108">Каждое требование к тестированию в этом документе состоит из четырех основных разделов: заголовка и таблицы с тремя важными разделами (левый столбец, правый верхний, правый нижний).</span><span class="sxs-lookup"><span data-stu-id="987a3-108">Each test requirement in this document has four main sections: a title and a table with three notable sections (left column, right top, right bottom).</span></span>

<dl> <dt>

<span data-ttu-id="987a3-109"><span id="Title"></span><span id="title"></span><span id="TITLE"></span>Титуль</span><span class="sxs-lookup"><span data-stu-id="987a3-109"><span id="Title"></span><span id="title"></span><span id="TITLE"></span>Title</span></span>
</dt> <dd>

<span data-ttu-id="987a3-110">Имя тестового случая.</span><span class="sxs-lookup"><span data-stu-id="987a3-110">Name of the test case.</span></span>

</dd> <dt>

<span data-ttu-id="987a3-111"><span id="Box__far_left_column"></span><span id="box__far_left_column"></span><span id="BOX__FAR_LEFT_COLUMN"></span>Box, столбец дальнего левого края</span><span class="sxs-lookup"><span data-stu-id="987a3-111"><span id="Box__far_left_column"></span><span id="box__far_left_column"></span><span id="BOX__FAR_LEFT_COLUMN"></span>Box, far left column</span></span>
</dt> <dd>

<span data-ttu-id="987a3-112">Имена операционных систем, к которым применяется тестовый случай.</span><span class="sxs-lookup"><span data-stu-id="987a3-112">Names of the operating systems to which the test case applies.</span></span>

</dd> <dt>

<span data-ttu-id="987a3-113"><span id="Box__right_top"></span><span id="box__right_top"></span><span id="BOX__RIGHT_TOP"></span>Box, справа сверху</span><span class="sxs-lookup"><span data-stu-id="987a3-113"><span id="Box__right_top"></span><span id="box__right_top"></span><span id="BOX__RIGHT_TOP"></span>Box, right top</span></span>
</dt> <dd>

<span data-ttu-id="987a3-114">Краткая сводка тестового случая.</span><span class="sxs-lookup"><span data-stu-id="987a3-114">Brief summary of the test case.</span></span>

</dd> <dt>

<span data-ttu-id="987a3-115"><span id="Box__right_bottom"></span><span id="box__right_bottom"></span><span id="BOX__RIGHT_BOTTOM"></span>Box, справа снизу</span><span class="sxs-lookup"><span data-stu-id="987a3-115"><span id="Box__right_bottom"></span><span id="box__right_bottom"></span><span id="BOX__RIGHT_BOTTOM"></span>Box, right bottom</span></span>
</dt> <dd>

<span data-ttu-id="987a3-116">Сведения о фактическом тестовом случае.</span><span class="sxs-lookup"><span data-stu-id="987a3-116">Details of the actual test case.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="987a3-117"><span id="Sample_Test_Script"></span><span id="sample_test_script"></span><span id="SAMPLE_TEST_SCRIPT"></span>**Пример скрипта теста**</span><span class="sxs-lookup"><span data-stu-id="987a3-117"><span id="Sample_Test_Script"></span><span id="sample_test_script"></span><span id="SAMPLE_TEST_SCRIPT"></span>**Sample Test Script**</span></span>
</dt> <dd>

<span data-ttu-id="987a3-118">В этом разделе приведен пример последовательности, в которой будет следовать типичный тестовый проход при использовании тестовых требований в качестве руководств.</span><span class="sxs-lookup"><span data-stu-id="987a3-118">This section is a sample of the sequence that a typical test pass would follow if using the test requirements as a guide.</span></span>

</dd> <dt>

<span data-ttu-id="987a3-119"><span id="Test_Tool_Notes"></span><span id="test_tool_notes"></span><span id="TEST_TOOL_NOTES"></span>**Заметки к средству тестирования**</span><span class="sxs-lookup"><span data-stu-id="987a3-119"><span id="Test_Tool_Notes"></span><span id="test_tool_notes"></span><span id="TEST_TOOL_NOTES"></span>**Test Tool Notes**</span></span>
</dt> <dd>

<span data-ttu-id="987a3-120">В этом разделе содержатся подробные примечания к каждому из средств тестирования, используемых для проверки условий пройденного или неудачи в требованиях к тестированию.</span><span class="sxs-lookup"><span data-stu-id="987a3-120">This section contains detailed notes on each of the test tools used to verify pass or fail conditions in the test requirements.</span></span>

</dd> </dl>

## <a name="test-requirements"></a><span data-ttu-id="987a3-121">Требования к тестированию</span><span class="sxs-lookup"><span data-stu-id="987a3-121">Test Requirements</span></span>

### <a name="1-game-requirements"></a><span data-ttu-id="987a3-122">1. требования к игре</span><span class="sxs-lookup"><span data-stu-id="987a3-122">1. Game Requirements</span></span>

### <a name="11-windows-games-explorer"></a><span data-ttu-id="987a3-123">1,1 Обозреватель игр Windows</span><span class="sxs-lookup"><span data-stu-id="987a3-123">1.1 Windows Games Explorer</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="987a3-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="987a3-124">Windows 7</span></span><br/> <span data-ttu-id="987a3-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="987a3-125">Windows Vista</span></span><br/></td>
<td><span data-ttu-id="987a3-126">Игра должна быть видна в обозревателе игр в Windows Vista и Windows 7.</span><span class="sxs-lookup"><span data-stu-id="987a3-126">The game must be visible within the Games Explorer on Windows Vista and Windows 7.</span></span> <span data-ttu-id="987a3-127">Если этот флажок установлен, игра также должна отображать правильные метаданные.</span><span class="sxs-lookup"><span data-stu-id="987a3-127">When selected, the game must also display correct metadata.</span></span> <span data-ttu-id="987a3-128">Установка не должна создавать ярлыки для запуска игры на рабочем столе, в меню "Пуск" или в любом другом расположении.</span><span class="sxs-lookup"><span data-stu-id="987a3-128">The installation must not create a shortcut to launch the game on the desktop, in the Start menu, or in any other location.</span></span> <span data-ttu-id="987a3-129">Не следует создавать задачи и ярлыки для удаления.</span><span class="sxs-lookup"><span data-stu-id="987a3-129">Tasks and shortcuts for removal must not be created.</span></span></td>
</tr>
<tr class="even">

<td><ol>
<li><span data-ttu-id="987a3-130">После установки игры откройте Обозреватель игр.</span><span class="sxs-lookup"><span data-stu-id="987a3-130">After installing the game, open Games Explorer.</span></span></li>
<li><span data-ttu-id="987a3-131">Убедитесь, что значок игры отображается в обозревателе игр.</span><span class="sxs-lookup"><span data-stu-id="987a3-131">Verify that the game icon displays in Games Explorer.</span></span></li>
<li><span data-ttu-id="987a3-132">Щелкните правой кнопкой мыши значок и проверьте каждую задачу поддержки, определяемую приложением &.</span><span class="sxs-lookup"><span data-stu-id="987a3-132">Right-click the icon and test each application-defined play & support task.</span></span></li>
<li><span data-ttu-id="987a3-133">Щелкните значок и убедитесь, что метаданные (издатель, разработчик, жанр, Дата выпуска, версия) внизу отображаются и указаны правильно.</span><span class="sxs-lookup"><span data-stu-id="987a3-133">Click the icon and verify that the metadata (publisher, developer, genre, release date, version) at the bottom displays and is correct.</span></span></li>
<li><span data-ttu-id="987a3-134">Убедитесь, что значок игры отображает сведения индекса производительности Windows (WEI) в обозревателе игр.</span><span class="sxs-lookup"><span data-stu-id="987a3-134">Verify that the game icon displays Windows Experience Index (WEI) information in Games Explorer.</span></span></li>
<li><span data-ttu-id="987a3-135">Убедитесь, что гиперссылки на игры для метаданных работают правильно в обозревателе игр.</span><span class="sxs-lookup"><span data-stu-id="987a3-135">Verify that game hyperlinks for metadata work correctly in Games Explorer.</span></span> <span data-ttu-id="987a3-136">(Если гиперссылки не отображаются, это может быть знак того, что exe-файл не подписан; см. <a href="#23-sign-files">раздел 2,3</a>.)</span><span class="sxs-lookup"><span data-stu-id="987a3-136">(If hyperlinks don't show up, then this is a possible sign that the exe isn't signed; see <a href="#23-sign-files">section 2.3</a>.)</span></span></li>
<li><span data-ttu-id="987a3-137">Убедитесь, что игра отображает точную оценку родительского контроля в обозревателе игр.</span><span class="sxs-lookup"><span data-stu-id="987a3-137">Verify that the game displays accurate parental control rating in Games Explorer.</span></span> <span data-ttu-id="987a3-138">(Если он говорит о неклассифицированности, убедитесь, что это игра без оценки; в противном случае это признак того, что exe-файл не подписан; см. <a href="#23-sign-files">раздел 2,3</a>.)</span><span class="sxs-lookup"><span data-stu-id="987a3-138">(If it says unrated, then verify that this is an unrated game; otherwise, this is an indicator that the exe isn't signed; see <a href="#23-sign-files">section 2.3</a>.)</span></span></li>
<li><span data-ttu-id="987a3-139">Убедитесь, что в игре не размещаются ярлыки запуска на рабочем столе пользователя.</span><span class="sxs-lookup"><span data-stu-id="987a3-139">Verify that the game does not place launch shortcuts on user desktop.</span></span></li>
<li><span data-ttu-id="987a3-140">Нажмите кнопку Пуск — > все программы.</span><span class="sxs-lookup"><span data-stu-id="987a3-140">Click Start -> All Programs.</span></span></li>
<li><span data-ttu-id="987a3-141">Убедитесь, что игра не помещает ярлыки запуска в меню "Пуск".</span><span class="sxs-lookup"><span data-stu-id="987a3-141">Verify that the game does not place launch shortcuts in the Start Menu.</span></span></li>
<li><span data-ttu-id="987a3-142">Убедитесь, что в меню "Пуск" за пределами панели управления не размещаются ярлыки для удаления.</span><span class="sxs-lookup"><span data-stu-id="987a3-142">Verify that the game does not place uninstall shortcuts in Start Menu outside of Control Panel.</span></span></li>
<li><span data-ttu-id="987a3-143">Если игра распространяется в цифровом формате, убедитесь, что поставщик услуг отображается в обозревателе игр Windows.</span><span class="sxs-lookup"><span data-stu-id="987a3-143">If the game is distributed digitally, verify that the service provider appears in Windows Games Explorer.</span></span></li>
</ol>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="12-windows-family-safety--parental-controls"></a><span data-ttu-id="987a3-144">1,2. Управление безопасностью и родительским контролем семейства Windows</span><span class="sxs-lookup"><span data-stu-id="987a3-144">1.2 Windows Family Safety / Parental Controls</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="987a3-145">Windows 7</span><span class="sxs-lookup"><span data-stu-id="987a3-145">Windows 7</span></span><br/> <span data-ttu-id="987a3-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="987a3-146">Windows Vista</span></span><br/></td>
<td><span data-ttu-id="987a3-147">Игра должна выполняться в контексте &quot; обычного пользователя &quot; .</span><span class="sxs-lookup"><span data-stu-id="987a3-147">Game must execute within the context of a &quot;Standard User&quot;.</span></span> <span data-ttu-id="987a3-148">Родительский контроль должен быть способен блокировать игру.</span><span class="sxs-lookup"><span data-stu-id="987a3-148">Parental Controls must be able to block the game.</span></span> <span data-ttu-id="987a3-149">Убедитесь, что в ГДФ есть имена EXE.</span><span class="sxs-lookup"><span data-stu-id="987a3-149">Verify that the GDF has EXE names.</span></span></td>
</tr>
<tr class="even">

<td><ol>
<li><span data-ttu-id="987a3-150">Создайте учетную запись обычного пользователя в Windows Vista или Windows 7 с именем Тоби.</span><span class="sxs-lookup"><span data-stu-id="987a3-150">Create a Standard User account in Windows Vista or Windows 7 called Toby.</span></span> <span data-ttu-id="987a3-151">Пуск-> панель управления — > добавить или удалить учетные записи пользователей — > создать учетную запись</span><span class="sxs-lookup"><span data-stu-id="987a3-151">Start -> Control Panel -> Add or Remove User Accounts -> Create New Account</span></span></li>
<li><span data-ttu-id="987a3-152">Мария, от учетной записи администратора, настроить родительский контроль для игры.</span><span class="sxs-lookup"><span data-stu-id="987a3-152">As Jane, from Administrator account set up Parental Controls for the game.</span></span> <span data-ttu-id="987a3-153">Пуск-> панель управления — > настроить родительские элементы управления для любого пользователя > Тоби</span><span class="sxs-lookup"><span data-stu-id="987a3-153">Start -> Control Panel -> Set Up Parental Controls for Any User -> Toby</span></span>
<ol>
<li><span data-ttu-id="987a3-154">Убедитесь, что игра запускается с помощью значка Обозреватель игр.</span><span class="sxs-lookup"><span data-stu-id="987a3-154">Verify that the game launches from the Games Explorer icon.</span></span></li>
<li><span data-ttu-id="987a3-155">Убедитесь, что в игре отображается Точная оценка родительского контроля под названием игры на панели управления родительского элемента управления.</span><span class="sxs-lookup"><span data-stu-id="987a3-155">Verify that the game displays accurate Parental Control Rating below the game title in the Parental Controls Control Panel.</span></span></li>
<li><span data-ttu-id="987a3-156">Прежде чем применять родительский контроль, убедитесь, что игра не запрашивает учетные данные администратора при запуске.</span><span class="sxs-lookup"><span data-stu-id="987a3-156">Before applying Parental Controls, verify that the game does not prompt for Administrator Credentials on launch.</span></span></li>
<li><span data-ttu-id="987a3-157">Установите для родительского контроля значение &quot; вкл &quot; .</span><span class="sxs-lookup"><span data-stu-id="987a3-157">Set Parental Controls to &quot;On&quot;.</span></span></li>
<li><span data-ttu-id="987a3-158">В разделе "Параметры Windows" щелкните "игры".</span><span class="sxs-lookup"><span data-stu-id="987a3-158">In the Windows Settings section, click Games.</span></span></li>
<li><span data-ttu-id="987a3-159">Нажмите кнопку ОК (теперь параметр должен быть &quot; AO/все игры &quot; ).</span><span class="sxs-lookup"><span data-stu-id="987a3-159">Click OK (setting should now be &quot;AO / all games&quot;).</span></span></li>
<li><span data-ttu-id="987a3-160">Убедитесь, что игра выполняется с этими параметрами в качестве пользователя Джейн.</span><span class="sxs-lookup"><span data-stu-id="987a3-160">Verify that the game runs with these settings as User Jane.</span></span></li>
<li><span data-ttu-id="987a3-161">Выйдите как Мария и войдите в систему как Тоби.</span><span class="sxs-lookup"><span data-stu-id="987a3-161">Log off as Jane and log on as Toby.</span></span></li>
<li><span data-ttu-id="987a3-162">Убедитесь, что игра выполняется с этими параметрами в качестве пользователя Тоби.</span><span class="sxs-lookup"><span data-stu-id="987a3-162">Verify that the game runs with these settings as User Toby.</span></span></li>
<li><span data-ttu-id="987a3-163">Выйдите из системы как Тоби и войдите в систему как Джейн.</span><span class="sxs-lookup"><span data-stu-id="987a3-163">Log off as Toby and log on as Jane.</span></span></li>
<li><span data-ttu-id="987a3-164">Вернитесь к предыдущему экрану и выберите &quot; задать рейтинги игр &quot; .</span><span class="sxs-lookup"><span data-stu-id="987a3-164">Go back to the previous screen and select &quot;Set Game Ratings&quot;.</span></span></li>
<li><p><span data-ttu-id="987a3-165">Выберите оценку ниже рейтинга ЕСРБ игры.</span><span class="sxs-lookup"><span data-stu-id="987a3-165">Select a rating lower than the game's ESRB Rating.</span></span></p>
<blockquote>
[!Note]<br />
<span data-ttu-id="987a3-166">Если игра не оценивается, пропустите этот шаг и перейдите к следующей части этого теста.</span><span class="sxs-lookup"><span data-stu-id="987a3-166">If the game is not rated, then skip this step and move onto the next part of this test.</span></span> <span data-ttu-id="987a3-167">Может потребоваться выбрать другую систему оценки для поиска рейтинга игры в зависимости от языкового стандарта тестируемого SKU.</span><span class="sxs-lookup"><span data-stu-id="987a3-167">It may be necessary to choose a different rating system to find a game rating, depending on the language locale of the SKU being tested.</span></span>
</blockquote>
<p><br/></p></li>
<li><span data-ttu-id="987a3-168">Выйдите как Мария и войдите в систему как Тоби.</span><span class="sxs-lookup"><span data-stu-id="987a3-168">Log off as Jane and log on as Toby.</span></span></li>
<li><span data-ttu-id="987a3-169">Убедитесь, что игра не запускается для пользователя Тоби, когда ЕСРБ заблокирована пользователем Джейн.</span><span class="sxs-lookup"><span data-stu-id="987a3-169">Verify that the game does not launch for User Toby when ESRB is blocked by User Jane.</span></span></li>
<li><span data-ttu-id="987a3-170">Выйдите из системы как Тоби и войдите в систему как Джейн.</span><span class="sxs-lookup"><span data-stu-id="987a3-170">Log off as Toby and log on as Jane.</span></span></li>
<li><span data-ttu-id="987a3-171">Если вы изменили ранее, восстановите параметры ЕСРБ.</span><span class="sxs-lookup"><span data-stu-id="987a3-171">If changed previously, restore the ESRB settings.</span></span></li>
<li><span data-ttu-id="987a3-172">Если параметры ЕСРБ отсутствуют, установите флажок &quot; блокировать или разрешить конкретные игры &quot; и выберите игру по имени.</span><span class="sxs-lookup"><span data-stu-id="987a3-172">If there are no ESRB settings, then select &quot;Block or Allow Specific Games&quot; and select the game by name.</span></span></li>
<li><span data-ttu-id="987a3-173">Выйдите как Мария и войдите в систему как Тоби.</span><span class="sxs-lookup"><span data-stu-id="987a3-173">Log off as Jane and log on as Toby.</span></span></li>
<li><span data-ttu-id="987a3-174">Убедитесь, что игра не запускается для пользователя Тоби, когда имя EXE/Name заблокировано пользователем Джейн.</span><span class="sxs-lookup"><span data-stu-id="987a3-174">Verify that the game does not launch for User Toby when EXE/Name is blocked by User Jane.</span></span></li>
<li><span data-ttu-id="987a3-175">Выйдите как Тоби и вернемся как Мария.</span><span class="sxs-lookup"><span data-stu-id="987a3-175">Log off as Toby and back on as Jane.</span></span></li>
<li><span data-ttu-id="987a3-176">Как Джейн, откройте пользовательские элементы управления — > ограничения приложений.</span><span class="sxs-lookup"><span data-stu-id="987a3-176">As Jane, open User Controls -> Application Restrictions.</span></span></li>
<li><span data-ttu-id="987a3-177">Щелкните &quot; Тоби может использовать только разрешенные программы &quot; и нажмите кнопку ОК (т. е. разрешить отсутствие исполняемых EXE-файлы).</span><span class="sxs-lookup"><span data-stu-id="987a3-177">Click &quot;Toby can only use the programs I allow&quot; and click OK (that is, allow no exes).</span></span></li>
<li><span data-ttu-id="987a3-178">Переход к пользовательским элементам управления | Элементы управления играми и позволяют конкретной игре использовать оценку ЕСРБ.</span><span class="sxs-lookup"><span data-stu-id="987a3-178">Go to User Controls | Games Controls and allow the specific game using the ESRB rating.</span></span></li>
<li><span data-ttu-id="987a3-179">Выйдите в систему как Мария и войдите в систему как Тоби и попытайтесь воспроизвести игру.</span><span class="sxs-lookup"><span data-stu-id="987a3-179">Log off as Jane, and log on as Toby and try to play the game.</span></span></li>
<li><span data-ttu-id="987a3-180">Убедитесь, что игра не заблокирована и Тоби может воспроизвести ее, если не &quot; задан параметр Разрешить отсутствие исполняемых &quot; данных.</span><span class="sxs-lookup"><span data-stu-id="987a3-180">Verify that the game is NOT blocked and that Toby can play it when &quot;allow no exes&quot; is set.</span></span></li>
</ol></li>
</ol>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="13-windows-vista-rich-saved-games"></a><span data-ttu-id="987a3-181">1,3. полнофункциональные сохраненные игры Windows Vista</span><span class="sxs-lookup"><span data-stu-id="987a3-181">1.3 Windows Vista Rich Saved Games</span></span>

<span data-ttu-id="987a3-182">Это требование было снято с учета.</span><span class="sxs-lookup"><span data-stu-id="987a3-182">This requirement has been retired.</span></span>

### <a name="14-xbox-360-common-controller-for-windows-conditional-requirement"></a><span data-ttu-id="987a3-183">1,4. Общий контроллер Xbox 360 для \[ условного требования Windows\]</span><span class="sxs-lookup"><span data-stu-id="987a3-183">1.4 Xbox 360 Common Controller for Windows \[Conditional Requirement\]</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="987a3-184">Windows 7</span><span class="sxs-lookup"><span data-stu-id="987a3-184">Windows 7</span></span><br/> <span data-ttu-id="987a3-185">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="987a3-185">Windows Vista</span></span><br/> <span data-ttu-id="987a3-186">Windows XP</span><span class="sxs-lookup"><span data-stu-id="987a3-186">Windows XP</span></span><br/></td>
<td><span data-ttu-id="987a3-187">Игры, поддерживающие контроллеры игровых устройств, должны поддерживать контроллер Xbox 360 для Windows с помощью API Ксинпут.</span><span class="sxs-lookup"><span data-stu-id="987a3-187">Games that support gamepad controllers must support the Xbox 360 Controller for Windows using the XInput API.</span></span> <span data-ttu-id="987a3-188">Все ссылки на общие триггеры контроллера и кнопки должны использовать имена Xbox 360.</span><span class="sxs-lookup"><span data-stu-id="987a3-188">All references to common controller triggers and buttons must use the Xbox 360 names.</span></span></td>
</tr>
<tr class="even">

<td><ol>
<li><span data-ttu-id="987a3-189">Запустите игру.</span><span class="sxs-lookup"><span data-stu-id="987a3-189">Launch the game.</span></span></li>
<li><span data-ttu-id="987a3-190">Перейдите в раздел параметры контроллера.</span><span class="sxs-lookup"><span data-stu-id="987a3-190">Go into the controller options.</span></span> **</li>
<li><span data-ttu-id="987a3-191">Убедитесь, что игра распознает контроллер Xbox 360 для Windows в качестве устройства ввода.</span><span class="sxs-lookup"><span data-stu-id="987a3-191">Verify that the game recognizes Xbox 360 Controller for Windows as an input device.</span></span></li>
<li><span data-ttu-id="987a3-192">Воспроизведите игру и убедитесь, что игра и система меню являются управляемыми с помощью контроллера Xbox 360 для Windows.</span><span class="sxs-lookup"><span data-stu-id="987a3-192">Play the game and verify that the game and menu system are controllable with Xbox 360 Controller for Windows.</span></span></li>
<li><span data-ttu-id="987a3-193">Убедитесь, что контроллер Xbox 360 для Windows ведет себя в соответствии с принятыми стандартами.</span><span class="sxs-lookup"><span data-stu-id="987a3-193">Verify that the Xbox 360 Controller for Windows behaves according to accepted standards.</span></span> <span data-ttu-id="987a3-194">(Б для возврата, A для принятия, запуск в меню "игра", "Пауза" или "принять" и т. д.)</span><span class="sxs-lookup"><span data-stu-id="987a3-194">(B for back, A for accept, Start for in game menu/pause or accept, etc.)</span></span></li>
<li><span data-ttu-id="987a3-195">Убедитесь, что игра относится к кнопкам контроллера и триггерам, использующим имена Xbox 360.</span><span class="sxs-lookup"><span data-stu-id="987a3-195">Verify that the game refers to the controller buttons and triggers using Xbox 360 names.</span></span></li>
</ol>
<br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="987a3-196">Если игра не поддерживает игровой контроллер и/или поддерживает только клавиатуру и мышь, пропустите этот тестовый случай.</span><span class="sxs-lookup"><span data-stu-id="987a3-196">If the game does not support a game controller and/or only supports keyboard/mouse, then skip this test case.</span></span>
</blockquote>
<br/> <span data-ttu-id="987a3-197">\* \* Параметры контроллера могут находиться за пределами игры.</span><span class="sxs-lookup"><span data-stu-id="987a3-197">\*\* Settings for the controller might be located outside of the game.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

### <a name="15-multiple-aspect-ratios-and-resolutions"></a><span data-ttu-id="987a3-198">1,5. множественные пропорции и разрешения</span><span class="sxs-lookup"><span data-stu-id="987a3-198">1.5 Multiple Aspect Ratios and Resolutions</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="987a3-199">Windows 7</span><span class="sxs-lookup"><span data-stu-id="987a3-199">Windows 7</span></span><br/> <span data-ttu-id="987a3-200">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="987a3-200">Windows Vista</span></span><br/> <span data-ttu-id="987a3-201">Windows XP</span><span class="sxs-lookup"><span data-stu-id="987a3-201">Windows XP</span></span><br/></td>
<td><span data-ttu-id="987a3-202">Игра должна поддерживать по крайней мере следующие пропорции и связанные с ними разрешения экрана:</span><span class="sxs-lookup"><span data-stu-id="987a3-202">The game must support at least the following aspect ratios and associated screen resolutions:</span></span> <br/>
<ul>
<li><span data-ttu-id="987a3-203">4:3 &quot; Обычная &quot; (800 600 или 1024 768)</span><span class="sxs-lookup"><span data-stu-id="987a3-203">4:3 &quot;normal&quot; (800 600 or 1024 768)</span></span></li>
<li><span data-ttu-id="987a3-204">&quot;широкоэкранный дисплей 16:9 &quot; (1280 720)</span><span class="sxs-lookup"><span data-stu-id="987a3-204">16:9 &quot;widescreen&quot; (1280 720)</span></span></li>
<li><span data-ttu-id="987a3-205">&quot;широкоэкранный дисплей 16:10 &quot; (1152 720, 1680 1050 или 800 480)</span><span class="sxs-lookup"><span data-stu-id="987a3-205">16:10 &quot;widescreen&quot; (1152 720, 1680 1050, or 800 480)</span></span></li>
</ul></td>
</tr>
<tr class="even">

<td><span data-ttu-id="987a3-206">Поиск параметров видео для игры (это может быть в нашей игре).</span><span class="sxs-lookup"><span data-stu-id="987a3-206">Locate the Video Options for the game (this may be in our out of game).</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="987a3-207">Следующие тесты должны выполняться на широкоформатном мониторе.</span><span class="sxs-lookup"><span data-stu-id="987a3-207">The following tests must be done on a widescreen monitor.</span></span>
</blockquote>
<br/>
<ol>
<li><span data-ttu-id="987a3-208">В разделе Разрешение видео выберите 800 600 или 1024 768.</span><span class="sxs-lookup"><span data-stu-id="987a3-208">In the video resolution section, select 800 600 or 1024 768.</span></span></li>
<li><span data-ttu-id="987a3-209">Убедитесь, что игра выполняется с разрешением пропорции 4:3.</span><span class="sxs-lookup"><span data-stu-id="987a3-209">Verify that the game runs at a 4:3 Aspect Ratio resolution.</span></span></li>
<li><span data-ttu-id="987a3-210">В разделе Разрешение видео выберите 1280 720.</span><span class="sxs-lookup"><span data-stu-id="987a3-210">In the video resolution section, select 1280 720.</span></span></li>
<li><span data-ttu-id="987a3-211">Убедитесь, что игра выполняется с разрешением пропорции 16:9.</span><span class="sxs-lookup"><span data-stu-id="987a3-211">Verify that the game runs at a 16:9 Aspect Ratio resolution.</span></span></li>
<li><span data-ttu-id="987a3-212">В разделе Разрешение видео выберите 1680 1050, 800 480 или 1152 720.</span><span class="sxs-lookup"><span data-stu-id="987a3-212">In the video resolution section, select 1680 1050, 800 480, or 1152 720.</span></span></li>
<li><span data-ttu-id="987a3-213">Убедитесь, что игра выполняется с разрешением пропорции 16:10.</span><span class="sxs-lookup"><span data-stu-id="987a3-213">Verify that the game runs at a 16:10 Aspect Ratio resolution.</span></span></li>
<li><span data-ttu-id="987a3-214">Убедитесь, что игра не растягивает изображение и, в свою очередь, представляет более широкую область представления.</span><span class="sxs-lookup"><span data-stu-id="987a3-214">Verify that the game does not stretch the picture and in turn presents a wider area of view.</span></span></li>
<li><span data-ttu-id="987a3-215">Убедитесь, что игра запрашивает пользователя при внесении изменений в разрешение.</span><span class="sxs-lookup"><span data-stu-id="987a3-215">Verify that the game prompts the user when a change is made to the resolution.</span></span></li>
<li><span data-ttu-id="987a3-216">Если пользователь не принимает условия в течение 15 секунд, убедитесь, что на экране возвращен предыдущий параметр.</span><span class="sxs-lookup"><span data-stu-id="987a3-216">If the user does not accept within 15 seconds, verify that the display reverts to the previous setting.</span></span></li>
<li><span data-ttu-id="987a3-217">Убедитесь, что игра не добавляет черные полосы слева и справа от области игры.</span><span class="sxs-lookup"><span data-stu-id="987a3-217">Verify that the game does not add black bars to the left and right of the game play area.</span></span> <span data-ttu-id="987a3-218">(В этом случае площадь игры будет по-прежнему соотношение 4:3 в середине экрана.)</span><span class="sxs-lookup"><span data-stu-id="987a3-218">(In this case, you will see the game area still in a 4:3 ratio in the middle of the screen.)</span></span></li>
</ol>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="16-windows-media-center"></a><span data-ttu-id="987a3-219">1,6 Windows Media Center</span><span class="sxs-lookup"><span data-stu-id="987a3-219">1.6 Windows Media Center</span></span>

<span data-ttu-id="987a3-220">Это требование было снято с учета.</span><span class="sxs-lookup"><span data-stu-id="987a3-220">This requirement has been retired.</span></span>

### <a name="17-direct3d-conditional-requirement"></a><span data-ttu-id="987a3-221">1,7. \[ условное требование Direct3D\]</span><span class="sxs-lookup"><span data-stu-id="987a3-221">1.7 Direct3D \[Conditional Requirement\]</span></span>



| <span data-ttu-id="987a3-222">ОС</span><span class="sxs-lookup"><span data-stu-id="987a3-222">OS</span></span>                                                                    | <span data-ttu-id="987a3-223">Требование</span><span class="sxs-lookup"><span data-stu-id="987a3-223">Requirement</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="987a3-224">Windows 7</span><span class="sxs-lookup"><span data-stu-id="987a3-224">Windows 7</span></span><br/> <span data-ttu-id="987a3-225">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="987a3-225">Windows Vista</span></span><br/> <span data-ttu-id="987a3-226">Windows XP</span><span class="sxs-lookup"><span data-stu-id="987a3-226">Windows XP</span></span><br/> | <span data-ttu-id="987a3-227">Если в игре используется Direct3D, минимальная поддерживаемая версия должна быть Direct3D 9, а Direct3D — значением по умолчанию для любого параметра конфигурации дисплея.</span><span class="sxs-lookup"><span data-stu-id="987a3-227">If the game uses Direct3D, the minimum version supported must be Direct3D 9, and Direct3D must be the default for any display configuration option.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|     <dl> <span data-ttu-id="987a3-228"><dt><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>Вручную</dt></span><span class="sxs-lookup"><span data-stu-id="987a3-228"><dt><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>Manual</dt></span></span> <dd> <span data-ttu-id="987a3-229">Запустите игру.</span><span class="sxs-lookup"><span data-stu-id="987a3-229">Launch the game.</span></span> <span data-ttu-id="987a3-230">В параметрах видео проверьте наличие параметров рендеринга, D3D и OpenGL.</span><span class="sxs-lookup"><span data-stu-id="987a3-230">In the video options, check to see if there are render options, D3D and/or OpenGL.</span></span> <span data-ttu-id="987a3-231">Если они есть, убедитесь, что параметры визуализации игры по умолчанию имеют значение Direct3D.</span><span class="sxs-lookup"><span data-stu-id="987a3-231">If there are, verify that the game render options default to Direct3D.</span></span> <span data-ttu-id="987a3-232">Если не удается проверить, что D3D9 является используемой версией DirectX, перейдите к автоматическому тесту.</span><span class="sxs-lookup"><span data-stu-id="987a3-232">If you are unable to verify that D3D9 is the version of DirectX that is being used, then proceed to Automated Test.</span></span> <br/> </dd> <span data-ttu-id="987a3-233"><dt><span id="Automated_Test"></span><span id="automated_test"></span><span id="AUTOMATED_TEST"></span>Автоматический тест</dt></span><span class="sxs-lookup"><span data-stu-id="987a3-233"><dt><span id="Automated_Test"></span><span id="automated_test"></span><span id="AUTOMATED_TEST"></span>Automated Test</dt></span></span> <dd> <span data-ttu-id="987a3-234">Использование средства: Depends.exe</span><span class="sxs-lookup"><span data-stu-id="987a3-234">Use tool: Depends.exe</span></span> <br/> </dd> </dl> |



 

### <a name="18-enable-high-dpi-aware"></a><span data-ttu-id="987a3-235">1,8. Включение поддержки высокого DPI</span><span class="sxs-lookup"><span data-stu-id="987a3-235">1.8 Enable High-DPI Aware</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="987a3-236">Windows 7</span><span class="sxs-lookup"><span data-stu-id="987a3-236">Windows 7</span></span><br/> <span data-ttu-id="987a3-237">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="987a3-237">Windows Vista</span></span><br/></td>
<td><span data-ttu-id="987a3-238">Игры и их установщики должны работать правильно без визуальных проблем при включенном масштабировании DPI.</span><span class="sxs-lookup"><span data-stu-id="987a3-238">Games and their installers must run correctly without visual problems when DPI scaling is enabled.</span></span></td>
</tr>
<tr class="even">

<td><dl> <span data-ttu-id="987a3-239"><dt><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>Вручную</dt> </span><span class="sxs-lookup"><span data-stu-id="987a3-239"><dt><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>Manual</dt> </span></span><dd>
<ol>
<li><span data-ttu-id="987a3-240">Установите для системы значение DPI 150%:</span><span class="sxs-lookup"><span data-stu-id="987a3-240">Set the system to DPI 150%:</span></span> <br/> <span data-ttu-id="987a3-241">Windows Vista: панель управления: персонализация, Настройка размера шрифта (DPI), пользовательское разрешение на дюйм.</span><span class="sxs-lookup"><span data-stu-id="987a3-241">Windows Vista: Control Panel: Personalization, Adjust font size (DPI), Custom DPI.</span></span> <span data-ttu-id="987a3-242">Задайте значение 150%.</span><span class="sxs-lookup"><span data-stu-id="987a3-242">Set to 150%.</span></span><br/> <span data-ttu-id="987a3-243">Windows 7: панель управления: отображение, для которой установлено значение больше 150%.</span><span class="sxs-lookup"><span data-stu-id="987a3-243">Windows 7: Control Panel: Display, Set to Larger - 150%.</span></span><br/></li>
<li><span data-ttu-id="987a3-244">Запустите процесс установки и игру, чтобы убедиться в отсутствии проблем с обрезанными экранами или диалоговыми окнами.</span><span class="sxs-lookup"><span data-stu-id="987a3-244">Run the installation process and game to verify there are no problems with clipped screens or dialog boxes.</span></span></li>
</ol>
</dd> <span data-ttu-id="987a3-245"><dt><span id="Automated_Test"></span><span id="automated_test"></span><span id="AUTOMATED_TEST"></span>Автоматический тест</dt> </span><span class="sxs-lookup"><span data-stu-id="987a3-245"><dt><span id="Automated_Test"></span><span id="automated_test"></span><span id="AUTOMATED_TEST"></span>Automated Test</dt> </span></span><dd> <span data-ttu-id="987a3-246">Убедитесь, что элемент <dpiAware>true</dpiAware> содержится во внедренном манифесте.</span><span class="sxs-lookup"><span data-stu-id="987a3-246">Verify that element <dpiAware>true</dpiAware> is contained in the embedded manifest.</span></span><br/> <span data-ttu-id="987a3-247">Использование средства: Mt.exe</span><span class="sxs-lookup"><span data-stu-id="987a3-247">Use tool: Mt.exe</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



 

### <a name="2-security-and-compatibility"></a><span data-ttu-id="987a3-248">2. безопасность и совместимость</span><span class="sxs-lookup"><span data-stu-id="987a3-248">2. Security and Compatibility</span></span>

### <a name="21-follow-user-account-control-guidelines"></a><span data-ttu-id="987a3-249">2,1 Следуйте рекомендациям по контролю учетных записей пользователей</span><span class="sxs-lookup"><span data-stu-id="987a3-249">2.1 Follow User Account Control Guidelines</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="987a3-250">Windows 7</span><span class="sxs-lookup"><span data-stu-id="987a3-250">Windows 7</span></span><br/> <span data-ttu-id="987a3-251">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="987a3-251">Windows Vista</span></span><br/></td>
<td><span data-ttu-id="987a3-252">Каждый исполняемый файл (расширение .EXE), включенный в приложение, должен иметь встроенный манифест, определяющий его уровень выполнения:</span><span class="sxs-lookup"><span data-stu-id="987a3-252">Every executable file (.EXE extension) included with an application must have an embedded manifest that defines its execution level:</span></span>
<pre class="syntax" data-space="preserve"><code><requestedExecutionLevel level=&quot;asInvoker|highestAvailable|requireAdministrator&quot; 
              uiAccess=&quot;true|false&quot;/></code></pre>
<br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="987a3-253">Для игр и игровых установщиков параметру uiAccess всегда следует присвоить значение &quot; false &quot; .</span><span class="sxs-lookup"><span data-stu-id="987a3-253">For games and game installers, uiAccess should always be set to &quot;false&quot;.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">

<td><ol>
<li><span data-ttu-id="987a3-254">Убедитесь, что исполняемые файлы игры содержат манифесты.</span><span class="sxs-lookup"><span data-stu-id="987a3-254">Verify game executable files contain manifests.</span></span></li>
<li><span data-ttu-id="987a3-255">Убедитесь, что файл манифеста исполняемого файла игры requestedExecutionLevel имеет параметр &quot; asInvoker &quot; .</span><span class="sxs-lookup"><span data-stu-id="987a3-255">Verify game executable file manifest requestedExecutionLevel is &quot;AsInvoker&quot;.</span></span></li>
</ol>
<span data-ttu-id="987a3-256">Использование средства: Mt.exe</span><span class="sxs-lookup"><span data-stu-id="987a3-256">Use tool: Mt.exe</span></span> <br/></td>
</tr>
</tbody>
</table>



 

### <a name="22-support-x64-versions-of-windows"></a><span data-ttu-id="987a3-257">2,2 Поддержка 64-разрядных версий Windows</span><span class="sxs-lookup"><span data-stu-id="987a3-257">2.2 Support x64 Versions of Windows</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="987a3-258">Windows 7</span><span class="sxs-lookup"><span data-stu-id="987a3-258">Windows 7</span></span><br/> <span data-ttu-id="987a3-259">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="987a3-259">Windows Vista</span></span><br/></td>
<td><span data-ttu-id="987a3-260">Для обеспечения совместимости с 64-разрядными версиями Windows:</span><span class="sxs-lookup"><span data-stu-id="987a3-260">To maintain compatibility with x64 versions of Windows:</span></span> <br/>
<ul>
<li><span data-ttu-id="987a3-261">Установщики titles и Title не должны содержать 16-разрядный код или использовать любой 16-разрядный компонент.</span><span class="sxs-lookup"><span data-stu-id="987a3-261">Titles and title installers must not contain any 16-bit code or rely on any 16-bit component.</span></span></li>
<li><span data-ttu-id="987a3-262">Если игра зависит от драйверов режима ядра для работы, должны быть доступны версии x64 этих драйверов.</span><span class="sxs-lookup"><span data-stu-id="987a3-262">If the game is dependent on kernel-mode drivers for operation, x64 versions of these drivers must be available.</span></span> <span data-ttu-id="987a3-263">Программа установки игр должна обнаружить и установить правильные драйверы и компоненты для 64-разрядных выпусков Windows.</span><span class="sxs-lookup"><span data-stu-id="987a3-263">The game setup must detect and install the proper drivers and components for 64-bit editions of Windows.</span></span></li>
</ul>
<blockquote>
[!Note]<br />
<span data-ttu-id="987a3-264">Поддержка 64-разрядного выпуска Windows XP Professional является необязательной.</span><span class="sxs-lookup"><span data-stu-id="987a3-264">Support for the 64-bit Edition of Windows XP Professional is optional.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">

<td><span data-ttu-id="987a3-265">Ручной тест</span><span class="sxs-lookup"><span data-stu-id="987a3-265">Manual Test</span></span><br/>
<ol>
<li><span data-ttu-id="987a3-266">Запустите игру на 64-разрядных выпусках Windows.</span><span class="sxs-lookup"><span data-stu-id="987a3-266">Run the game on 64-bit editions of Windows.</span></span> <span data-ttu-id="987a3-267">Убедитесь, что процесс установки игры выполняется как обычно в 64-разрядных выпусках Windows Vista или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="987a3-267">Verify that the game installation process runs normally on 64-bit editions of Windows Vista or Windows 7.</span></span></li>
<li><span data-ttu-id="987a3-268">Убедитесь, что игра не обнаружила ошибку в результате 16-разрядных исполняемых файлов в 64-разрядных выпусках Windows Vista или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="987a3-268">Verify that the game does not encounter an error as a result of 16-bit executables on 64-bit editions of Windows Vista or Windows 7.</span></span> <span data-ttu-id="987a3-269">В окне ошибки будет упомянуто 16-разрядное приложение.</span><span class="sxs-lookup"><span data-stu-id="987a3-269">The error will mention the 16-bit application in the error window.</span></span></li>
<li><span data-ttu-id="987a3-270">Если у игры есть собственный 64-разрядный исполняемый файл, используйте его.</span><span class="sxs-lookup"><span data-stu-id="987a3-270">If the game has a native 64-bit executable, then use that as well.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="23-sign-files"></a><span data-ttu-id="987a3-271">2,3. входные файлы</span><span class="sxs-lookup"><span data-stu-id="987a3-271">2.3 Sign Files</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="987a3-272">Windows 7</span><span class="sxs-lookup"><span data-stu-id="987a3-272">Windows 7</span></span><br/> <span data-ttu-id="987a3-273">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="987a3-273">Windows Vista</span></span><br/> <span data-ttu-id="987a3-274">Windows XP</span><span class="sxs-lookup"><span data-stu-id="987a3-274">Windows XP</span></span><br/></td>
<td><span data-ttu-id="987a3-275">Все файлы исполняемого кода (например, расширения .exe и .dll) должны быть подписаны с помощью сертификата Authenticode.</span><span class="sxs-lookup"><span data-stu-id="987a3-275">All executable code files (for example, .exe and .dll extensions) must be signed with an Authenticode certificate.</span></span> <br/> <span data-ttu-id="987a3-276">Если используется установщик Windows, файлы пакета установщика (.msi файлы) должны быть подписаны.</span><span class="sxs-lookup"><span data-stu-id="987a3-276">If you are using Windows Installer, the installer's package files (.msi files) must be signed.</span></span> <br/></td>
</tr>
<tr class="even">

<td><span data-ttu-id="987a3-277">Ручной тест</span><span class="sxs-lookup"><span data-stu-id="987a3-277">Manual Test</span></span><br/>
<ol>
<li><span data-ttu-id="987a3-278">Перейдите в каталог игры.</span><span class="sxs-lookup"><span data-stu-id="987a3-278">Navigate to the game directory.</span></span></li>
<li><span data-ttu-id="987a3-279">Нахождение всех файлов .exe и .dll.</span><span class="sxs-lookup"><span data-stu-id="987a3-279">Locate all of the .exe and .dll files.</span></span></li>
<li><span data-ttu-id="987a3-280">Щелкните правой кнопкой мыши свойства каждого файла.</span><span class="sxs-lookup"><span data-stu-id="987a3-280">Right-click Properties on each file.</span></span></li>
<li><span data-ttu-id="987a3-281">Убедитесь, что исполняемые файлы игры содержат цифровую подпись.</span><span class="sxs-lookup"><span data-stu-id="987a3-281">Verify that the game executable files contain a digital signature.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="24-sign-drivers"></a><span data-ttu-id="987a3-282">2,4. подписывать драйверы</span><span class="sxs-lookup"><span data-stu-id="987a3-282">2.4 Sign Drivers</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="987a3-283">Windows 7</span><span class="sxs-lookup"><span data-stu-id="987a3-283">Windows 7</span></span><br/> <span data-ttu-id="987a3-284">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="987a3-284">Windows Vista</span></span><br/> <span data-ttu-id="987a3-285">Windows XP</span><span class="sxs-lookup"><span data-stu-id="987a3-285">Windows XP</span></span><br/></td>
<td><span data-ttu-id="987a3-286">Любой драйвер режима ядра, установленный игрой, должен быть подписан открытым действительным сертификатом Authenticode.</span><span class="sxs-lookup"><span data-stu-id="987a3-286">Any kernel-mode driver that is installed by the game must be signed with a publicly valid Authenticode certificate.</span></span> <br/> <span data-ttu-id="987a3-287">Любой драйвер аппаратного устройства в режиме ядра, установленный игрой, должен иметь подпись Майкрософт, полученную с помощью программы WHQL или подписи надежности драйвера (DRS).</span><span class="sxs-lookup"><span data-stu-id="987a3-287">Any kernel-mode hardware device driver that is installed by the game must have a Microsoft signature obtained through the Windows Hardware Quality Labs (WHQL) or Driver Reliability Signature (DRS) program.</span></span> <br/></td>
</tr>
<tr class="even">

<td><span data-ttu-id="987a3-288">Ручной тест</span><span class="sxs-lookup"><span data-stu-id="987a3-288">Manual Test</span></span><br/>
<ol>
<li><span data-ttu-id="987a3-289">Установите игру.</span><span class="sxs-lookup"><span data-stu-id="987a3-289">Install the game.</span></span></li>
<li><span data-ttu-id="987a3-290">Убедитесь, что в процессе установки игры не отображаются диалоговые окна неподписанного драйвера.</span><span class="sxs-lookup"><span data-stu-id="987a3-290">Verify that the game install process does not display unsigned driver dialog(s).</span></span></li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="25-perform-version-checking-properly"></a><span data-ttu-id="987a3-291">2,5. Проверка версии выполнена правильно</span><span class="sxs-lookup"><span data-stu-id="987a3-291">2.5 Perform Version Checking Properly</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="987a3-292">Windows 7</span><span class="sxs-lookup"><span data-stu-id="987a3-292">Windows 7</span></span><br/> <span data-ttu-id="987a3-293">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="987a3-293">Windows Vista</span></span><br/> <span data-ttu-id="987a3-294">Windows XP</span><span class="sxs-lookup"><span data-stu-id="987a3-294">Windows XP</span></span><br/></td>
<td><span data-ttu-id="987a3-295">Игры не должны работать в будущих операционных системах, как указано в изменениях номера версии Windows, если лицензионное соглашение не запрещает использовать в будущих операционных системах.</span><span class="sxs-lookup"><span data-stu-id="987a3-295">Games must not fail to run on future operating systems as indicated by changes in the Windows version number, unless the End User License Agreement prohibits use on future operating systems.</span></span> <span data-ttu-id="987a3-296">Если предполагается, что игра завершится ошибкой, она должна правильно сделать это, отображая сообщение для пользователя.</span><span class="sxs-lookup"><span data-stu-id="987a3-296">If the game is supposed to fail, it must do so gracefully by displaying a message to the user.</span></span></td>
</tr>
<tr class="even">

<td><dl> <span data-ttu-id="987a3-297"><dt><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>Вручную</dt> </span><span class="sxs-lookup"><span data-stu-id="987a3-297"><dt><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>Manual</dt> </span></span><dd>
<ol>
<li><span data-ttu-id="987a3-298">Установите игру в Windows XP, в 32-разрядных выпусках Windows Vista и Windows 7, а также в 64-разрядных выпусках Windows Vista и Windows 7.</span><span class="sxs-lookup"><span data-stu-id="987a3-298">Install the game on Windows XP, on 32-bit editions of Windows Vista and Windows 7, and on 64-bit editions of Windows Vista and Windows 7.</span></span></li>
<li><span data-ttu-id="987a3-299">Убедитесь, что в процессе установки игры не обнаружена ошибка, относящаяся к версии ОС.</span><span class="sxs-lookup"><span data-stu-id="987a3-299">Verify that the game installation process does not encounter an error regarding OS version.</span></span></li>
</ol>
</dd> <span data-ttu-id="987a3-300"><dt><span id="Automated_Test"></span><span id="automated_test"></span><span id="AUTOMATED_TEST"></span>Автоматический тест</dt> </span><span class="sxs-lookup"><span data-stu-id="987a3-300"><dt><span id="Automated_Test"></span><span id="automated_test"></span><span id="AUTOMATED_TEST"></span>Automated Test</dt> </span></span><dd> <span data-ttu-id="987a3-301">Использование средства: средство проверки приложений</span><span class="sxs-lookup"><span data-stu-id="987a3-301">Use tool: Application Verifier</span></span><br/>
<ol>
<li><span data-ttu-id="987a3-302">Запустите средство проверки приложений.</span><span class="sxs-lookup"><span data-stu-id="987a3-302">Launch Application Verifier.</span></span></li>
<li><span data-ttu-id="987a3-303">Включите проверку совместимости: Хигхверсионлие после выбора INSTALL.EXE.</span><span class="sxs-lookup"><span data-stu-id="987a3-303">Enable the Compatibility:HighVersionLie test after selecting the INSTALL.EXE.</span></span></li>
<li><span data-ttu-id="987a3-304">Установите игру и убедитесь, что она не блокирует установку на основе версии ОС.</span><span class="sxs-lookup"><span data-stu-id="987a3-304">Install the game and ensure that it does not block installation based on the OS version.</span></span></li>
<li><span data-ttu-id="987a3-305">Включите проверку совместимости: Хигхверсионлие после выбора GAME.EXE.</span><span class="sxs-lookup"><span data-stu-id="987a3-305">Enable the Compatibility:HighVersionLie test after selecting the GAME.EXE.</span></span></li>
<li><span data-ttu-id="987a3-306">Запустите игру и убедитесь, что она не блокирует выполнение на основе версии ОС.</span><span class="sxs-lookup"><span data-stu-id="987a3-306">Run the game and ensure it does not block execution based on the OS version.</span></span></li>
</ol>
</dd> </dl></td>
</tr>
</tbody>
</table>



 

### <a name="26-support-concurrent-user-sessions"></a><span data-ttu-id="987a3-307">2,6 Поддержка параллельных сеансов пользователей</span><span class="sxs-lookup"><span data-stu-id="987a3-307">2.6 Support Concurrent User Sessions</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="987a3-308">Windows 7</span><span class="sxs-lookup"><span data-stu-id="987a3-308">Windows 7</span></span><br/> <span data-ttu-id="987a3-309">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="987a3-309">Windows Vista</span></span><br/> <span data-ttu-id="987a3-310">Windows XP</span><span class="sxs-lookup"><span data-stu-id="987a3-310">Windows XP</span></span><br/></td>
<td><span data-ttu-id="987a3-311">Игры должны поддерживать стандартные многозадачные сценарии Windows.</span><span class="sxs-lookup"><span data-stu-id="987a3-311">Games must support standard Windows multitasking scenarios.</span></span></td>
</tr>
<tr class="even">

<td><span data-ttu-id="987a3-312">Создайте учетную запись обычного пользователя в Windows Vista или Windows 7 с именем Тоби.</span><span class="sxs-lookup"><span data-stu-id="987a3-312">Create a Standard User account in Windows Vista or Windows 7 called Toby.</span></span> <span data-ttu-id="987a3-313">Пуск-> панель управления — > добавить или удалить учетные записи пользователей — > создать учетную запись</span><span class="sxs-lookup"><span data-stu-id="987a3-313">Start -> Control Panel -> Add or Remove User Accounts -> Create New Account</span></span> <br/>
<ol>
<li><span data-ttu-id="987a3-314">Запустите игру от имени пользователя Джейн.</span><span class="sxs-lookup"><span data-stu-id="987a3-314">Launch the game as User Jane.</span></span></li>
<li><span data-ttu-id="987a3-315">ALT + TAB вернуться к рабочему столу.</span><span class="sxs-lookup"><span data-stu-id="987a3-315">ALT+TAB back to the desktop.</span></span></li>
<li><span data-ttu-id="987a3-316">Убедитесь, что игра правильно ALT + Табуляция на рабочем столе Windows.</span><span class="sxs-lookup"><span data-stu-id="987a3-316">Verify that the game properly ALT+TABs to the Windows desktop.</span></span></li>
<li><span data-ttu-id="987a3-317">Нажмите кнопку Пуск-> [стрелка вправо от блокировки]-> параметр пользователь.</span><span class="sxs-lookup"><span data-stu-id="987a3-317">Click Start -> [arrow to the right of Lock] -> Switch User.</span></span></li>
<li><span data-ttu-id="987a3-318">Войдите в систему как пользователь Тоби.</span><span class="sxs-lookup"><span data-stu-id="987a3-318">Log on as User Toby.</span></span></li>
<li><span data-ttu-id="987a3-319">Убедитесь, что игра запускается как пользователь Тоби, но по-прежнему выполняется от имени пользователя Джейн.</span><span class="sxs-lookup"><span data-stu-id="987a3-319">Verify that the game launches as User Toby while still running as User Jane.</span></span></li>
<li><span data-ttu-id="987a3-320">Убедитесь, что игра не сталкивается с ошибками для пользователя Тоби или Джейн пользователя во время процесса переключения пользователя.</span><span class="sxs-lookup"><span data-stu-id="987a3-320">Verify that the game does not encounter errors for User Toby or User Jane during User Switch process.</span></span></li>
<li><span data-ttu-id="987a3-321">Если вы можете запустить другой сеанс игры, убедитесь, что вы не можете слышать звук из исходного сеанса игры.</span><span class="sxs-lookup"><span data-stu-id="987a3-321">If you can launch another game session, verify that you cannot hear audio from the original game session.</span></span></li>
<li><span data-ttu-id="987a3-322">Закройте игру и вернитесь к исходному пользователю и игре.</span><span class="sxs-lookup"><span data-stu-id="987a3-322">Close the game and switch back to the original user and game.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="27-support-long-names"></a><span data-ttu-id="987a3-323">2,7. Поддержка длинных имен</span><span class="sxs-lookup"><span data-stu-id="987a3-323">2.7 Support Long Names</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="987a3-324">Windows 7</span><span class="sxs-lookup"><span data-stu-id="987a3-324">Windows 7</span></span><br/> <span data-ttu-id="987a3-325">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="987a3-325">Windows Vista</span></span><br/> <span data-ttu-id="987a3-326">Windows XP</span><span class="sxs-lookup"><span data-stu-id="987a3-326">Windows XP</span></span><br/></td>
<td><span data-ttu-id="987a3-327">Если игра поддерживает сохранение файлов, она должна иметь возможность сохранять файлы с длинными именами и путями.</span><span class="sxs-lookup"><span data-stu-id="987a3-327">If a game supports saving files, it must be able to save files that have long names and paths.</span></span> <span data-ttu-id="987a3-328">Игра должна правильно работать с специальными символами файловой системы, например \/: \*?</span><span class="sxs-lookup"><span data-stu-id="987a3-328">The game must properly handle special file system characters, such as \ / : \* ?</span></span> <span data-ttu-id="987a3-329">&quot; < или > в любых пользовательских полях ввода, используемых для создания имен файлов или путей.</span><span class="sxs-lookup"><span data-stu-id="987a3-329">&quot; < or > in any user input fields used to create file names or paths.</span></span></td>
</tr>
<tr class="even">

<td><ol>
<li><span data-ttu-id="987a3-330">Запустите игру.</span><span class="sxs-lookup"><span data-stu-id="987a3-330">Launch the game.</span></span></li>
<li><span data-ttu-id="987a3-331">Начать новую игру.</span><span class="sxs-lookup"><span data-stu-id="987a3-331">Start a new game.</span></span></li>
<li><span data-ttu-id="987a3-332">Сохраните игру.</span><span class="sxs-lookup"><span data-stu-id="987a3-332">Save the game.</span></span> <span data-ttu-id="987a3-333">В процессе сохранения убедитесь, что игра сохраняется с помощью команды Сохранить имя: Моя первая игра.</span><span class="sxs-lookup"><span data-stu-id="987a3-333">During the save process, verify that the game saves using the save name: My First Save Game.</span></span></li>
<li><span data-ttu-id="987a3-334">Вернитесь в главное меню.</span><span class="sxs-lookup"><span data-stu-id="987a3-334">Exit back to the main menu.</span></span></li>
<li><span data-ttu-id="987a3-335">Попытка загрузить только что сохраненную игру.</span><span class="sxs-lookup"><span data-stu-id="987a3-335">Attempt to load the newly saved game.</span></span></li>
<li><span data-ttu-id="987a3-336">Убедитесь, что игра не сталкивается с ошибками при обработке неподдерживаемых символов файловой системы, например \/: \*?</span><span class="sxs-lookup"><span data-stu-id="987a3-336">Verify that the game does not encounter errors when handling unsupported file system characters, such as \ / : \* ?</span></span> <span data-ttu-id="987a3-337">&quot; < или > если игра разрешена, назовите сохраненную игру.</span><span class="sxs-lookup"><span data-stu-id="987a3-337">&quot; < or > If the game allows you, name the saved game.</span></span></li>
<li><span data-ttu-id="987a3-338">Если пользователю разрешено наименовать свой профиль или символ или сохранить игры, убедитесь, что игра не сталкивается с ошибками при использовании длинных имен файлов.</span><span class="sxs-lookup"><span data-stu-id="987a3-338">If the user is allowed to name their profile and/or character or save games, verify that the game does not encounter errors when using long file names here as well.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="3-installation"></a><span data-ttu-id="987a3-339">3. Установка</span><span class="sxs-lookup"><span data-stu-id="987a3-339">3. Installation</span></span>

### <a name="31-easy-install"></a><span data-ttu-id="987a3-340">3,1 простая установка</span><span class="sxs-lookup"><span data-stu-id="987a3-340">3.1 Easy Install</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="987a3-341">Windows 7</span><span class="sxs-lookup"><span data-stu-id="987a3-341">Windows 7</span></span><br/> <span data-ttu-id="987a3-342">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="987a3-342">Windows Vista</span></span><br/> <span data-ttu-id="987a3-343">Windows XP</span><span class="sxs-lookup"><span data-stu-id="987a3-343">Windows XP</span></span><br/></td>
<td><span data-ttu-id="987a3-344">Игры с традиционной установкой должны предоставлять упрощенный путь в пользовательском интерфейсе установки.</span><span class="sxs-lookup"><span data-stu-id="987a3-344">Games with a traditional installation must provide a simplified path in their setup user interface.</span></span></td>
</tr>
<tr class="even">

<td><ol>
<li><span data-ttu-id="987a3-345">Вставьте диск игры.</span><span class="sxs-lookup"><span data-stu-id="987a3-345">Insert the game disc.</span></span></li>
<li><span data-ttu-id="987a3-346">Убедитесь, что игра не отображает более одного End-User лицензионного соглашения (EULA).</span><span class="sxs-lookup"><span data-stu-id="987a3-346">Verify that the game does not display more than one End-User License Agreement (EULA).</span></span></li>
<li><span data-ttu-id="987a3-347">Если игра поддерживает пользовательский или расширенный вариант установки, убедитесь, что этот параметр доступен в процессе установки.</span><span class="sxs-lookup"><span data-stu-id="987a3-347">If the game supports a custom or advanced installation option, verify that this option is accessible during the installation process.</span></span></li>
<li><span data-ttu-id="987a3-348">Убедитесь, что параметр установки по умолчанию обходит все входные данные пользователя для процесса установки (Выбор папки установки, выбор компонентов и т. д.).</span><span class="sxs-lookup"><span data-stu-id="987a3-348">Verify that the Default installation option bypasses all user input selections for the installation process (selection of installation folder, components selection, and so on).</span></span></li>
<li><span data-ttu-id="987a3-349">Убедитесь, что процесс установки игры не запрашивает установку компонентов ОС (Установка DirectX, среды выполнения Visual C и т. д.).</span><span class="sxs-lookup"><span data-stu-id="987a3-349">Verify that the game installation process does not prompt for OS component setup (DirectX setup, Visual C Runtimes, and so on).</span></span></li>
<li><span data-ttu-id="987a3-350">Убедитесь, что процесс установки игры не запрашивает взаимодействие с брандмауэром.</span><span class="sxs-lookup"><span data-stu-id="987a3-350">Verify that the game installation process does not prompt for firewall interaction.</span></span></li>
<li><span data-ttu-id="987a3-351">Убедитесь, что игра автоматически запускается, или что в конце процесса установки имеется меню запуска.</span><span class="sxs-lookup"><span data-stu-id="987a3-351">Verify that the game automatically runs or that a launcher menu is present at the end of the install process.</span></span></li>
<li><span data-ttu-id="987a3-352">Убедитесь, что процесс удаления игры удаляет все установленные, нераспространенные файлы компонентов ОС и очищает все параметры.</span><span class="sxs-lookup"><span data-stu-id="987a3-352">Verify that the game uninstallation process removes all installed, non-redistributed OS component files and clears all settings.</span></span> <span data-ttu-id="987a3-353">Очистка всех параметров и данных на уровне пользователя (например, сохраненные игры) не требуется.</span><span class="sxs-lookup"><span data-stu-id="987a3-353">Cleaning up all per-user settings and data (such as saved games) is not required.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="32-support-user-account-control-for-installation"></a><span data-ttu-id="987a3-354">3,2. Поддержка контроля учетных записей пользователей для установки</span><span class="sxs-lookup"><span data-stu-id="987a3-354">3.2 Support User Account Control for Installation</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="987a3-355">Windows 7</span><span class="sxs-lookup"><span data-stu-id="987a3-355">Windows 7</span></span><br/> <span data-ttu-id="987a3-356">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="987a3-356">Windows Vista</span></span><br/></td>
<td><span data-ttu-id="987a3-357">Установщик игры не должен считать, что он работает в том же контексте, что и пользователь.</span><span class="sxs-lookup"><span data-stu-id="987a3-357">The game installer must not assume it is running in the same context as the user.</span></span> <span data-ttu-id="987a3-358">Таким образом, игры должны выполнять задачи для каждого пользователя при первом запуске отдельно от установки.</span><span class="sxs-lookup"><span data-stu-id="987a3-358">Games must therefore perform per-user tasks on first-run separately from the installation.</span></span></td>
</tr>
<tr class="even">

<td><ol>
<li><span data-ttu-id="987a3-359">Убедитесь, что вы можете установить игру в качестве пользователя Джейн.</span><span class="sxs-lookup"><span data-stu-id="987a3-359">Verify that you can install the game as User Jane.</span></span> <span data-ttu-id="987a3-360">(Это потребует повышенных прав в процессе установки или установки.)</span><span class="sxs-lookup"><span data-stu-id="987a3-360">(This will require elevated rights during the setup/installation process.)</span></span></li>
<li><span data-ttu-id="987a3-361">Убедитесь, что в процессе установки игры пользователь Джейн запрашивает повышение прав через учетные данные администратора.</span><span class="sxs-lookup"><span data-stu-id="987a3-361">Verify that the game installation process prompts User Jane to elevate through Administrator Credentials.</span></span> <span data-ttu-id="987a3-362">(При попытке установки пользователь получит запрос на повышение прав.)</span><span class="sxs-lookup"><span data-stu-id="987a3-362">(The prompt to elevate will come up when the user attempts to install.)</span></span></li>
<li><span data-ttu-id="987a3-363">Выберите автоматический запуск игры в конце установки, если это еще не сделано, или запустите его из появившегося меню.</span><span class="sxs-lookup"><span data-stu-id="987a3-363">Opt to Autorun the game at the end of installation, if it does not already do so, or launch it from the menu that appears.</span></span></li>
<li><span data-ttu-id="987a3-364">После игры Создайте новый профиль, воспроизведите и сохраните игру.</span><span class="sxs-lookup"><span data-stu-id="987a3-364">Once in-game, create a new profile, play and save a game.</span></span></li>
<li><span data-ttu-id="987a3-365">Выйдите из игры.</span><span class="sxs-lookup"><span data-stu-id="987a3-365">Exit the game.</span></span></li>
<li><span data-ttu-id="987a3-366">Перезапустите игру и убедитесь, что учетная запись пользователя Джейн может получить доступ к профилям пользователей и сохраненным играм.</span><span class="sxs-lookup"><span data-stu-id="987a3-366">Restart the game and verify that User Profiles and Saved Games can be accessed by the User Jane account.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="33-install-to-correct-folders"></a><span data-ttu-id="987a3-367">3,3. Установка для исправления папок</span><span class="sxs-lookup"><span data-stu-id="987a3-367">3.3 Install to Correct Folders</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="987a3-368">Windows 7</span><span class="sxs-lookup"><span data-stu-id="987a3-368">Windows 7</span></span><br/> <span data-ttu-id="987a3-369">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="987a3-369">Windows Vista</span></span><br/> <span data-ttu-id="987a3-370">Windows XP</span><span class="sxs-lookup"><span data-stu-id="987a3-370">Windows XP</span></span><br/></td>
<td><span data-ttu-id="987a3-371">По умолчанию игры должны быть установлены в папку Program Files.</span><span class="sxs-lookup"><span data-stu-id="987a3-371">Games must be installed to the Program Files folder by default.</span></span> <span data-ttu-id="987a3-372">Пользовательские данные должны быть записаны при первом запуске, а не во время установки.</span><span class="sxs-lookup"><span data-stu-id="987a3-372">User data must be written at first run and not during the installation.</span></span></td>
</tr>
<tr class="even">

<td><ol>
<li><span data-ttu-id="987a3-373">Установите игру, используя тип установки по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="987a3-373">Install the game using the Default install type.</span></span></li>
<li><span data-ttu-id="987a3-374">Убедитесь, что игра установлена в Program Files.</span><span class="sxs-lookup"><span data-stu-id="987a3-374">Verify that the game was installed to Program Files.</span></span></li>
</ol>
<blockquote>
[!Note]<br />
<span data-ttu-id="987a3-375">Если проверка не пройдена, убедитесь, что игра должна быть установлена для всех пользователей.</span><span class="sxs-lookup"><span data-stu-id="987a3-375">If this test fails, verify that the game is intended to install for All Users.</span></span> <span data-ttu-id="987a3-376">Если да, это не является ошибкой.</span><span class="sxs-lookup"><span data-stu-id="987a3-376">If so, this is a failure.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="34-install-windows-resources-properly"></a><span data-ttu-id="987a3-377">3,4. Установка ресурсов Windows надлежащим образом</span><span class="sxs-lookup"><span data-stu-id="987a3-377">3.4 Install Windows Resources Properly</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="987a3-378">Windows 7</span><span class="sxs-lookup"><span data-stu-id="987a3-378">Windows 7</span></span><br/> <span data-ttu-id="987a3-379">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="987a3-379">Windows Vista</span></span><br/> <span data-ttu-id="987a3-380">Windows XP</span><span class="sxs-lookup"><span data-stu-id="987a3-380">Windows XP</span></span><br/></td>
<td><span data-ttu-id="987a3-381">Приложения не должны пытаться установить файлы или ключи реестра, защищенные защита ресурсов Windows (WRP).</span><span class="sxs-lookup"><span data-stu-id="987a3-381">Applications must not attempt to install files or registry keys that are protected by Windows Resource Protection (WRP).</span></span></td>
</tr>
<tr class="even">

<td><ul>
<li><span data-ttu-id="987a3-382">Убедитесь, что в процессе установки не отображаются диалоговые окна защита ресурсов Windows WRP.</span><span class="sxs-lookup"><span data-stu-id="987a3-382">Verify that no Windows Resource Protection WRP dialog boxes appear during the installation process.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

### <a name="35-avoid-reboots-during-installation"></a><span data-ttu-id="987a3-383">3,5. Предотвращение перезагрузки во время установки</span><span class="sxs-lookup"><span data-stu-id="987a3-383">3.5 Avoid Reboots During Installation</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="987a3-384">Windows 7</span><span class="sxs-lookup"><span data-stu-id="987a3-384">Windows 7</span></span><br/> <span data-ttu-id="987a3-385">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="987a3-385">Windows Vista</span></span><br/> <span data-ttu-id="987a3-386">Windows XP</span><span class="sxs-lookup"><span data-stu-id="987a3-386">Windows XP</span></span><br/></td>
<td><span data-ttu-id="987a3-387">Установщик игр не предполагает, что установка компонентов Windows из пакетов распространения требует перезагрузки, если только перезагрузка не указана в результате возврата или документации Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="987a3-387">The game installer should not assume that installation of Windows components from redistribution packages requires a reboot, unless the reboot is indicated by a return result or by Microsoft documentation.</span></span></td>
</tr>
<tr class="even">

<td><ol>
<li><span data-ttu-id="987a3-388">Установите игру.</span><span class="sxs-lookup"><span data-stu-id="987a3-388">Install the game.</span></span></li>
<li><span data-ttu-id="987a3-389">Убедитесь, что игра не требует перезагрузки системы после установки.</span><span class="sxs-lookup"><span data-stu-id="987a3-389">Verify that the game does not require the system to be rebooted after installation.</span></span></li>
</ol>
<blockquote>
[!Note]<br />
<span data-ttu-id="987a3-390">Если РАСПРОСТРАНЯЕМый пакет обновления системы Microsoft требует перезагрузки, выполните следующие действия. Завершите установку игры, удалите игру и повторно установите игру.</span><span class="sxs-lookup"><span data-stu-id="987a3-390">If a Microsoft system update REDIST requires a reboot, then do the following: Complete the game installation, uninstall the game, and reinstall the game a second time.</span></span> <span data-ttu-id="987a3-391">В ходе этой второй установки не требуется перезагружать компьютер в процессе установки игры.</span><span class="sxs-lookup"><span data-stu-id="987a3-391">The game installation process should not require a reboot on this second installation.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="36-use-file-versioning-correctly"></a><span data-ttu-id="987a3-392">3,6. правильное использование управления версиями файлов</span><span class="sxs-lookup"><span data-stu-id="987a3-392">3.6 Use File Versioning Correctly</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="987a3-393">Windows 7</span><span class="sxs-lookup"><span data-stu-id="987a3-393">Windows 7</span></span><br/> <span data-ttu-id="987a3-394">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="987a3-394">Windows Vista</span></span><br/> <span data-ttu-id="987a3-395">Windows XP</span><span class="sxs-lookup"><span data-stu-id="987a3-395">Windows XP</span></span><br/></td>
<td><span data-ttu-id="987a3-396">Программа установки игр должна правильно проверить, чтобы убедиться, что установлены последние версии файлов.</span><span class="sxs-lookup"><span data-stu-id="987a3-396">The game installation program must properly check to ensure that the latest file versions are installed.</span></span> <span data-ttu-id="987a3-397">При установке игры никогда не следует регрессию файлов, которые не создаются или которые являются общими для приложений, которые не создаются.</span><span class="sxs-lookup"><span data-stu-id="987a3-397">Installing a game must never regress any files that you do not produce or that are shared by applications that you do not produce.</span></span></td>
</tr>
<tr class="even">

<td><ol>
<li><span data-ttu-id="987a3-398">Перед установкой игры Создайте предварительно установленный моментальный снимок System32.</span><span class="sxs-lookup"><span data-stu-id="987a3-398">Prior to installing the game, create a pre-install snapshot of System32.</span></span><br/>
<ol>
<li><span data-ttu-id="987a3-399">Создайте каталог с именем G4Wtest.</span><span class="sxs-lookup"><span data-stu-id="987a3-399">Make a directory called G4Wtest.</span></span></li>
<li><span data-ttu-id="987a3-400">Откройте окно командной строки (Start-> Run-> cmd).</span><span class="sxs-lookup"><span data-stu-id="987a3-400">Bring up a command Window (Start -> Run -> cmd).</span></span></li>
<li><span data-ttu-id="987a3-401">Перейдите по адресу c:\Windows\System32.</span><span class="sxs-lookup"><span data-stu-id="987a3-401">Navigate to c:\windows\system32.</span></span></li>
<li><span data-ttu-id="987a3-402">Введите dir/o:-g/o:-d >> c:\G4Wtest\pregame.txt.</span><span class="sxs-lookup"><span data-stu-id="987a3-402">Type dir /o:-g /o:-d >> c:\G4Wtest\pregame.txt.</span></span></li>
</ol></li>
<li><span data-ttu-id="987a3-403">Создайте моментальный снимок после установки System32.</span><span class="sxs-lookup"><span data-stu-id="987a3-403">Create a post-install snapshot of System32.</span></span> <br/>
<ol>
<li><span data-ttu-id="987a3-404">Откройте окно командной строки (Start-> Run-> cmd).</span><span class="sxs-lookup"><span data-stu-id="987a3-404">Bring up a command Window (Start -> Run -> cmd).</span></span></li>
<li><span data-ttu-id="987a3-405">Перейдите по адресу c:\Windows\System32.</span><span class="sxs-lookup"><span data-stu-id="987a3-405">Navigate to c:\windows\system32.</span></span></li>
<li><span data-ttu-id="987a3-406">Введите dir/o:-g/o:-d >> c:\G4Wtest\postgame.txt.</span><span class="sxs-lookup"><span data-stu-id="987a3-406">Type dir /o:-g /o:-d >> c:\G4Wtest\postgame.txt.</span></span></li>
<li><span data-ttu-id="987a3-407">Убедитесь, что игра не выполняет регрессию файлов версий файлов, которые не были воспроизведены игрой (... файлов, перечисленных в двух документах, путем сравнения pregame.txt с postgame.txt).</span><span class="sxs-lookup"><span data-stu-id="987a3-407">Verify that the game does not regress any file versions of files that the game did not produce (...of the files listed in the two documents by comparing pregame.txt to postgame.txt).</span></span></li>
</ol></li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="37-support-autorun-conditional-requirement"></a><span data-ttu-id="987a3-408">3,7 поддержка \[ условного требования автозапуска\]</span><span class="sxs-lookup"><span data-stu-id="987a3-408">3.7 Support Autorun \[Conditional Requirement\]</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="987a3-409">Windows 7</span><span class="sxs-lookup"><span data-stu-id="987a3-409">Windows 7</span></span><br/> <span data-ttu-id="987a3-410">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="987a3-410">Windows Vista</span></span><br/> <span data-ttu-id="987a3-411">Windows XP</span><span class="sxs-lookup"><span data-stu-id="987a3-411">Windows XP</span></span><br/></td>
<td><span data-ttu-id="987a3-412">Для игр, распространяемых на компакт-диске, DVD-диске или другом съемном носителе, поддерживающем автозапуск, при первой вставке диска приложение должно автоматически запуститься или предложить пользователю установить игру.</span><span class="sxs-lookup"><span data-stu-id="987a3-412">For games distributed on CD, DVD, or other removable media that support Autorun, when the disc is inserted for the first time, the application must automatically run or prompt the user to install the game.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="987a3-413">Программы автозапуска, написанные для использования в версиях Windows до Windows Vista, не должны использовать среду выполнения .NET, так как эта технология не входит в состав Windows XP и более ранних версий Windows.</span><span class="sxs-lookup"><span data-stu-id="987a3-413">Autorun programs that were written for use on versions of Windows prior to Windows Vista should not use the .NET runtime, because this technology is not included with Windows XP or older versions of Windows.</span></span>
</blockquote>
<br/> <span data-ttu-id="987a3-414">Дополнительные сведения см. в статье <a href="/windows/win32/DxTechArts/games-for-windows-technical-requirements-1-1-0006">технические требования для Windows</a> 3,7, поддержка автозапуска.</span><span class="sxs-lookup"><span data-stu-id="987a3-414">For further guidance, please refer to <a href="/windows/win32/DxTechArts/games-for-windows-technical-requirements-1-1-0006">Games for Windows Technical Requirements</a> 3.7, Support Autorun.</span></span> <br/></td>
</tr>
<tr class="even">

<td><ol>
<li><span data-ttu-id="987a3-415">Вставьте игровой диск или носитель.</span><span class="sxs-lookup"><span data-stu-id="987a3-415">Insert the game disc or media.</span></span></li>
<li><span data-ttu-id="987a3-416">Убедитесь, что диалоговое окно «Установка и запуск» автоматически появляется.</span><span class="sxs-lookup"><span data-stu-id="987a3-416">Verify that the install / run dialog box comes up automatically.</span></span></li>
<li><span data-ttu-id="987a3-417">Windows Vista или Windows 7. Убедитесь, что программа автозапуска игр не запрашивает у пользователя, который будет повышать права, с помощью учетных данных администратора.</span><span class="sxs-lookup"><span data-stu-id="987a3-417">Windows Vista or Windows 7: Verify that the game Autorun program itself does not prompt User Jane to elevate through Administrator Credentials.</span></span></li>
<li><span data-ttu-id="987a3-418">Убедитесь, что исполняемому файлу автозапуска не требуются готовые компоненты Redist, такие как .NET 3,5, C Run-Time librarys и т. д.</span><span class="sxs-lookup"><span data-stu-id="987a3-418">Verify that the Autorun executable doesn't need out-of-box REDIST components, such as .NET 3.5, C Run-Time libraries, and so on.</span></span></li>
<li><span data-ttu-id="987a3-419">Убедитесь, что повторная вставка диска в дисковод после установки не приводит к повторному запуску установки.</span><span class="sxs-lookup"><span data-stu-id="987a3-419">Verify that re-inserting the disc in the drive after installation does not cause installation to automatically begin again.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="4-reliability"></a><span data-ttu-id="987a3-420">4. надежность</span><span class="sxs-lookup"><span data-stu-id="987a3-420">4. Reliability</span></span>

### <a name="41-eliminate-unnecessary-reboots"></a><span data-ttu-id="987a3-421">4,1. Устраните ненужные перезагрузки</span><span class="sxs-lookup"><span data-stu-id="987a3-421">4.1 Eliminate Unnecessary Reboots</span></span>



| <span data-ttu-id="987a3-422">ОС</span><span class="sxs-lookup"><span data-stu-id="987a3-422">OS</span></span>                                              | <span data-ttu-id="987a3-423">Требование</span><span class="sxs-lookup"><span data-stu-id="987a3-423">Requirement</span></span>                                                                                                                                                                   |
|-----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="987a3-424">Windows 7</span><span class="sxs-lookup"><span data-stu-id="987a3-424">Windows 7</span></span><br/> <span data-ttu-id="987a3-425">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="987a3-425">Windows Vista</span></span><br/> | <span data-ttu-id="987a3-426">Все установщики приложений должны воспользоваться преимуществами API диспетчера перезапуска, чтобы избежать перезагрузки системы (см. [требование 3,5](#35-avoid-reboots-during-installation)).</span><span class="sxs-lookup"><span data-stu-id="987a3-426">All application installers must take advantage of the Restart Manager APIs to avoid system reboots (see [requirement 3.5](#35-avoid-reboots-during-installation)).</span></span> |



 

### <a name="42-eliminate-application-verifier-failures"></a><span data-ttu-id="987a3-427">4,2 Устранение сбоев средство проверки приложений</span><span class="sxs-lookup"><span data-stu-id="987a3-427">4.2 Eliminate Application Verifier Failures</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="987a3-428">Windows 7</span><span class="sxs-lookup"><span data-stu-id="987a3-428">Windows 7</span></span><br/> <span data-ttu-id="987a3-429">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="987a3-429">Windows Vista</span></span><br/> <span data-ttu-id="987a3-430">Windows XP</span><span class="sxs-lookup"><span data-stu-id="987a3-430">Windows XP</span></span><br/></td>
<td><span data-ttu-id="987a3-431">Игра не должна создавать ошибки, выполняемые в Microsoft средство проверки приложений (AppVerifier) версии 4,0 или более поздней, в следующих тестах:</span><span class="sxs-lookup"><span data-stu-id="987a3-431">The game must generate no failures running under Microsoft Application Verifier (AppVerifier), version 4.0 or later, in the following tests:</span></span> <br/>
<ul>
<li><span data-ttu-id="987a3-432">Основные сведения: дескрипторы, кучи, блокировки, память, TLS</span><span class="sxs-lookup"><span data-stu-id="987a3-432">Basics: Handles, Heaps, Locks, Memory, TLS</span></span></li>
<li><span data-ttu-id="987a3-433">Прочее: Данжераусапис, Диртистаккс</span><span class="sxs-lookup"><span data-stu-id="987a3-433">Miscellaneous: DangerousAPIs, DirtyStacks</span></span></li>
</ul></td>
</tr>
<tr class="even">

<td><span data-ttu-id="987a3-434">Использование средства: AppVerifier 4,0 (или более поздней версии)</span><span class="sxs-lookup"><span data-stu-id="987a3-434">Use Tool: AppVerifier 4.0 (or later)</span></span><br/>
<ol>
<li><span data-ttu-id="987a3-435">Установите AppVerifier.</span><span class="sxs-lookup"><span data-stu-id="987a3-435">Install AppVerifier.</span></span></li>
<li><span data-ttu-id="987a3-436">Запустите AppVerifier и выберите файл-> добавить приложение.</span><span class="sxs-lookup"><span data-stu-id="987a3-436">Launch AppVerifier and select File -> Add Application.</span></span></li>
<li><span data-ttu-id="987a3-437">Укажите исполняемый файл игры, выберите его и нажмите кнопку &quot; открыть &quot; .</span><span class="sxs-lookup"><span data-stu-id="987a3-437">Locate the game executable, select it, and click the &quot;Open&quot; button.</span></span></li>
<li><span data-ttu-id="987a3-438">В &quot; разделе приложения &quot; выберите исполняемый файл игры.</span><span class="sxs-lookup"><span data-stu-id="987a3-438">In the &quot;Applications&quot; section, select the game executable.</span></span></li>
<li><span data-ttu-id="987a3-439">В &quot; разделе тесты &quot; выберите тесты, перечисленные выше в разделе категории &quot; основные &quot; и &quot; Прочие &quot; (снимите флажки ThreadPool и тимеролловер) и убедитесь, что все остальные тесты не выбраны.</span><span class="sxs-lookup"><span data-stu-id="987a3-439">In the &quot;Tests&quot; section, select the tests listed above under the categories &quot;Basics&quot; and &quot;Miscellaneous&quot; (uncheck ThreadPool and TimeRollOver), and ensure all other tests are not selected.</span></span></li>
<li><span data-ttu-id="987a3-440">Запустите игру.</span><span class="sxs-lookup"><span data-stu-id="987a3-440">Launch the game.</span></span></li>
<li><span data-ttu-id="987a3-441">Убедитесь, что игра не создает ошибок при выполнении в средство проверки приложений.</span><span class="sxs-lookup"><span data-stu-id="987a3-441">Verify that the game does not generate failures when run under Application Verifier.</span></span></li>
</ol>
<blockquote>
[!Note]<br />
<span data-ttu-id="987a3-442">Для некоторых тестов требуется полный запуск отладчика.</span><span class="sxs-lookup"><span data-stu-id="987a3-442">Some tests require a debugger to be fully run.</span></span> <span data-ttu-id="987a3-443">Для этого может потребоваться незащищенная версия выпускаемого файла игры, так как технология борьбы-Памятка по/борьба с пиратством может помешать Аппверифер.</span><span class="sxs-lookup"><span data-stu-id="987a3-443">This may require an unprotected release version of the game executable, since anti-cheat/anti-piracy technology may interfere with AppVerifer.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="43-support-windows-error-reporting"></a><span data-ttu-id="987a3-444">отчеты об ошибках Windows поддержки 4,3</span><span class="sxs-lookup"><span data-stu-id="987a3-444">4.3 Support Windows Error Reporting</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="987a3-445">Windows 7</span><span class="sxs-lookup"><span data-stu-id="987a3-445">Windows 7</span></span><br/> <span data-ttu-id="987a3-446">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="987a3-446">Windows Vista</span></span><br/> <span data-ttu-id="987a3-447">Windows XP</span><span class="sxs-lookup"><span data-stu-id="987a3-447">Windows XP</span></span><br/></td>
<td><span data-ttu-id="987a3-448">Игры должны обрабатывать только известные и ожидаемые исключения, а отчеты об ошибках Windows не должны быть отключены.</span><span class="sxs-lookup"><span data-stu-id="987a3-448">Games must handle only exceptions that are known and expected, and Windows Error Reporting must not be disabled.</span></span> <span data-ttu-id="987a3-449">Если ошибка (например, нарушение прав доступа) внедряется в игру, она должна разрешить отчеты об ошибках Windows сообщить о сбое.</span><span class="sxs-lookup"><span data-stu-id="987a3-449">If a fault (such as an Access Violation) is injected into a game, it must allow Windows Error Reporting to report the crash.</span></span></td>
</tr>
<tr class="even">

<td><span data-ttu-id="987a3-450">Использование средства: средство захвата потоков</span><span class="sxs-lookup"><span data-stu-id="987a3-450">Use Tool: Thread Hijacker</span></span> <br/>
<ul>
<li><span data-ttu-id="987a3-451">Если во время тестирования происходит сбой приложения, убедитесь, что игра отображается отчеты об ошибках Windows должным образом и собирает данные о сбое.</span><span class="sxs-lookup"><span data-stu-id="987a3-451">If the application crashes while testing, verify that the game displays Windows Error Reporting properly and collects crash data.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="987a3-452">Windows 7</span><span class="sxs-lookup"><span data-stu-id="987a3-452">Windows 7</span></span><br/> <span data-ttu-id="987a3-453">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="987a3-453">Windows Vista</span></span><br/> <span data-ttu-id="987a3-454">Windows XP</span><span class="sxs-lookup"><span data-stu-id="987a3-454">Windows XP</span></span><br/></td>
<td><span data-ttu-id="987a3-455">Все исполняемые файлы (например, файлы .exe или .dll) должны содержать точное название продукта, название компании и версию файла.</span><span class="sxs-lookup"><span data-stu-id="987a3-455">All executable files (for example, .exe or .dll files) must contain an accurate Product Name, Company Name, and File Version.</span></span></td>
</tr>
<tr class="even">

<td><dl> <span data-ttu-id="987a3-456"><dt><span id="Manual_test_"></span><span id="manual_test_"></span><span id="MANUAL_TEST_"></span>Ручной тест:</dt> </span><span class="sxs-lookup"><span data-stu-id="987a3-456"><dt><span id="Manual_test_"></span><span id="manual_test_"></span><span id="MANUAL_TEST_"></span>Manual test:</dt> </span></span><dd>
<ol>
<li><span data-ttu-id="987a3-457">Щелкните правой кнопкой мыши исполняемые файлы игры на установочном носителе, а также на жестком диске компьютера.</span><span class="sxs-lookup"><span data-stu-id="987a3-457">Right-click the game's executable file(s) on both the installation media and those installed to the computer hard drive.</span></span></li>
<li><span data-ttu-id="987a3-458">Выберите "Свойства".</span><span class="sxs-lookup"><span data-stu-id="987a3-458">Select Properties.</span></span></li>
<li><span data-ttu-id="987a3-459">Windows XP: перейдите на вкладку <strong>версия</strong> . Убедитесь, что поля Название продукта, название организации и версия файла заполнены правильно.</span><span class="sxs-lookup"><span data-stu-id="987a3-459">Windows XP: Click the <strong>Version</strong> tab. Verify that the Product Name, Company Name, and File Version fields are properly populated.</span></span></li>
<li><span data-ttu-id="987a3-460">Windows Vista или Windows 7: перейдите на вкладку <strong>сведения</strong> . Убедитесь, что поля Название продукта и версия файла заполнены должным образом.</span><span class="sxs-lookup"><span data-stu-id="987a3-460">Windows Vista or Windows 7: Click the <strong>Details</strong> tab. Verify that the Product name and File Version fields are properly populated.</span></span> <span data-ttu-id="987a3-461">Название организации не отображается на странице свойств Windows Vista или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="987a3-461">Company Name is not visible in the Windows Vista or Windows 7 properties page.</span></span></li>
</ol>
</dd> <span data-ttu-id="987a3-462"><dt><span id="Automated_test_"></span><span id="automated_test_"></span><span id="AUTOMATED_TEST_"></span>Автоматический тест:</dt> </span><span class="sxs-lookup"><span data-stu-id="987a3-462"><dt><span id="Automated_test_"></span><span id="automated_test_"></span><span id="AUTOMATED_TEST_"></span>Automated test:</dt> </span></span><dd>
<ul>
<li><span data-ttu-id="987a3-463">Используйте инструмент Microsoft Games для тестирования Windows; см. <a href="#64-microsoft-games-for-windows-test-tool">раздел 6,4</a>.</span><span class="sxs-lookup"><span data-stu-id="987a3-463">Use the Microsoft Games for Windows Test Tool; see <a href="#64-microsoft-games-for-windows-test-tool">section 6.4</a>.</span></span></li>
</ul>
</dd> </dl></td>
</tr>
</tbody>
</table>



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="987a3-464">Windows 7</span><span class="sxs-lookup"><span data-stu-id="987a3-464">Windows 7</span></span><br/> <span data-ttu-id="987a3-465">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="987a3-465">Windows Vista</span></span><br/> <span data-ttu-id="987a3-466">Windows XP</span><span class="sxs-lookup"><span data-stu-id="987a3-466">Windows XP</span></span><br/></td>
<td><span data-ttu-id="987a3-467">Нормальное завершение игры не должно приводить к ошибке неизвестного исключения.</span><span class="sxs-lookup"><span data-stu-id="987a3-467">Normal exit of the game must not result in an unknown exception fault.</span></span></td>
</tr>
<tr class="even">

<td><ul>
<li><span data-ttu-id="987a3-468">После воспроизведения игры в течение обычного игрового сеанса убедитесь, что игра не создает ошибок при выходе.</span><span class="sxs-lookup"><span data-stu-id="987a3-468">After playing the game for a normal gaming session, verify that the game does not generate errors on exit.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="5-sample-test-script"></a><span data-ttu-id="987a3-469">5. пример скрипта теста</span><span class="sxs-lookup"><span data-stu-id="987a3-469">5. Sample Test Script</span></span>

<span data-ttu-id="987a3-470">Это пример типичного тестового прохода с использованием предыдущих тестовых требований в качестве инструкции.</span><span class="sxs-lookup"><span data-stu-id="987a3-470">This is an example of a typical test pass using the preceding test requirements as a guide.</span></span>

### <a name="51-tools"></a><span data-ttu-id="987a3-471">средства 5,1</span><span class="sxs-lookup"><span data-stu-id="987a3-471">5.1 Tools</span></span>

-   <span data-ttu-id="987a3-472">32-разрядный выпуск Windows Vista с пакетом обновления 1 (SP1) и (или) Windows 7 на ЦП AMD</span><span class="sxs-lookup"><span data-stu-id="987a3-472">32-bit edition of Windows Vista SP1 and/or Windows 7 on an AMD CPU</span></span>
-   <span data-ttu-id="987a3-473">32-разрядный выпуск Windows Vista с пакетом обновления 1 (SP1) и (или) Windows 7 на ЦП Intel</span><span class="sxs-lookup"><span data-stu-id="987a3-473">32-bit edition of Windows Vista SP1 and/or Windows 7 on an Intel CPU</span></span>
-   <span data-ttu-id="987a3-474">64-разрядный выпуск Windows Vista с пакетом обновления 1 (SP1) и (или) Windows 7 на ЦП AMD</span><span class="sxs-lookup"><span data-stu-id="987a3-474">64-bit edition of Windows Vista SP1 and/or Windows 7 on an AMD CPU</span></span>
-   <span data-ttu-id="987a3-475">64-разрядный выпуск Windows Vista с пакетом обновления 1 (SP1) и (или) Windows 7 на ЦП Intel</span><span class="sxs-lookup"><span data-stu-id="987a3-475">64-bit edition of Windows Vista SP1 and/or Windows 7 on an Intel CPU</span></span>
-   <span data-ttu-id="987a3-476">32-разрядный выпуск Windows XP с пакетом обновления 2 (SP2) на ЦП AMD</span><span class="sxs-lookup"><span data-stu-id="987a3-476">32-bit edition Windows XP SP2 on an AMD CPU</span></span>
-   <span data-ttu-id="987a3-477">32-разрядный выпуск Windows XP с пакетом обновления 2 (SP2) на ЦП Intel</span><span class="sxs-lookup"><span data-stu-id="987a3-477">32-bit edition Windows XP SP2 on an Intel CPU</span></span>
-   <span data-ttu-id="987a3-478">Широкий экранный монитор, поддерживающий 1680 1050</span><span class="sxs-lookup"><span data-stu-id="987a3-478">Wide Screen Monitor that supports 1680 1050</span></span>
-   <span data-ttu-id="987a3-479">Контроллер Xbox 360 для Windows</span><span class="sxs-lookup"><span data-stu-id="987a3-479">Xbox 360 Controller for Windows</span></span>

### <a name="52-pre-install"></a><span data-ttu-id="987a3-480">5,2. Предварительная установка</span><span class="sxs-lookup"><span data-stu-id="987a3-480">5.2 Pre-Install</span></span>

1.  <span data-ttu-id="987a3-481">Windows Vista и Windows 7: создание двух стандартных пользователей: Джейн и Тоби</span><span class="sxs-lookup"><span data-stu-id="987a3-481">Windows Vista and Windows 7: Create two Standard Users: Jane and Toby</span></span>
2.  <span data-ttu-id="987a3-482">Windows Vista и Windows 7: Убедитесь, что включен контроль учетных записей пользователей.</span><span class="sxs-lookup"><span data-stu-id="987a3-482">Windows Vista and Windows 7: Ensure User Account Control is enabled</span></span>
3.  <span data-ttu-id="987a3-483">Создание предварительной установки моментального снимка system32</span><span class="sxs-lookup"><span data-stu-id="987a3-483">Create a pre-install snapshot of System32</span></span>

    1.  <span data-ttu-id="987a3-484">Создание каталога с именем G4Wtest</span><span class="sxs-lookup"><span data-stu-id="987a3-484">Make a directory called G4Wtest</span></span>
    2.  <span data-ttu-id="987a3-485">Вывести окно командной строки (Start-> Run-> cmd)</span><span class="sxs-lookup"><span data-stu-id="987a3-485">Bring up a command Window (Start -> Run -> cmd)</span></span>
    3.  <span data-ttu-id="987a3-486">Перейдите по адресу c: \\ Windows \\ system32</span><span class="sxs-lookup"><span data-stu-id="987a3-486">Navigate to c:\\windows\\system32</span></span>
    4.  <span data-ttu-id="987a3-487">Введите dir/o:-g/o:-d >> c: \\ G4Wtest \\pregame.txt</span><span class="sxs-lookup"><span data-stu-id="987a3-487">Type dir /o:-g /o:-d >> c:\\G4Wtest\\pregame.txt</span></span>

4.  <span data-ttu-id="987a3-488">Windows Vista и Windows 7: задано значение 150% DPI \[ 1,8\]</span><span class="sxs-lookup"><span data-stu-id="987a3-488">Windows Vista and Windows 7: Set to 150% DPI \[1.8\]</span></span>
5.  <span data-ttu-id="987a3-489">Перейти к [установке](#3-installation)</span><span class="sxs-lookup"><span data-stu-id="987a3-489">Proceed to [Install](#3-installation)</span></span>

### <a name="53-install"></a><span data-ttu-id="987a3-490">5,3 Установка</span><span class="sxs-lookup"><span data-stu-id="987a3-490">5.3 Install</span></span>

1.  <span data-ttu-id="987a3-491">Вход от имени пользователя Джейн</span><span class="sxs-lookup"><span data-stu-id="987a3-491">Log on as User Jane</span></span>
2.  <span data-ttu-id="987a3-492">Вставьте игровой диск в дисковод компакт-или DVD-дисков, убедитесь, что диалоговое окно "Установка и запуск" автоматически появляется в \[ 3,7\]</span><span class="sxs-lookup"><span data-stu-id="987a3-492">Insert the game disc into the CD/DVD drive, verify that the install / run dialog box comes up automatically \[3.7\]</span></span>
3.  <span data-ttu-id="987a3-493">Убедитесь, что в процессе установки игры пользователь Джейн попросит у пользователя повысить права учетных данных администратора \[ 3,2\]</span><span class="sxs-lookup"><span data-stu-id="987a3-493">Verify that the game installation process prompts User Jane to elevate Administrator Credentials \[3.2\]</span></span>
4.  <span data-ttu-id="987a3-494">Убедитесь, что программа автозапуска игры не запрашивает у пользователя, который должен повысить свою подлинность, учетные данные администратора \[ 3,7\]</span><span class="sxs-lookup"><span data-stu-id="987a3-494">Verify that the game Autorun program itself does not prompt User Jane to elevate through Administrator Credentials \[3.7\]</span></span>
5.  <span data-ttu-id="987a3-495">Убедитесь, что игра не отображает более одного End-User лицензионного соглашения (EULA) \[ 3,1\]</span><span class="sxs-lookup"><span data-stu-id="987a3-495">Verify that the game does not display more than one End-User License Agreement (EULA) \[3.1\]</span></span>
6.  <span data-ttu-id="987a3-496">Убедитесь, что в игре отображаются параметры установки по умолчанию, простой и пользовательский/расширенный, \[ 3,1\]</span><span class="sxs-lookup"><span data-stu-id="987a3-496">Verify that the game displays Default/Easy and Custom/Advanced installation options \[3.1\]</span></span>
7.  <span data-ttu-id="987a3-497">Убедитесь, что параметр установки по умолчанию (простота) обходит все параметры ввода данных пользователя для процесса установки (Выбор папки установки, выбор компонентов и т. д.) \[ . 3,1\]</span><span class="sxs-lookup"><span data-stu-id="987a3-497">Verify that the Default/Easy installation option bypasses all user input selections for the install process (selection of installation folder, components selection, and so on.) \[3.1\]</span></span>
8.  <span data-ttu-id="987a3-498">Убедитесь, что процесс установки игры не запрашивает установку компонентов ОС (программа установки DirectX, библиотеки Run-Time C и т. д.) \[ . 3,1\]</span><span class="sxs-lookup"><span data-stu-id="987a3-498">Verify that the game installation process does not prompt for OS component setup (DirectX setup, C Run-Time libraries, and so on.) \[3.1\]</span></span>
9.  <span data-ttu-id="987a3-499">Убедитесь, что в процессе установки игры не запрашивается взаимодействие с брандмауэром \[ 3,1\]</span><span class="sxs-lookup"><span data-stu-id="987a3-499">Verify that the game installation process does not prompt for firewall interaction \[3.1\]</span></span>
10. <span data-ttu-id="987a3-500">Убедитесь, что в процессе установки игры не обнаружена ошибка, относящаяся к ОС версии \[ 2,5 \] \[ 4,2\]</span><span class="sxs-lookup"><span data-stu-id="987a3-500">Verify that the game installation process does not encounter an error regarding OS Version \[2.5\] \[4.2\]</span></span>
11. <span data-ttu-id="987a3-501">Убедитесь, что в процессе установки игры не отображаются диалоговые окна неподписанного драйвера (s) \[ 2,4\]</span><span class="sxs-lookup"><span data-stu-id="987a3-501">Verify that the game installation process does not display unsigned driver dialog(s) \[2.4\]</span></span>
12. <span data-ttu-id="987a3-502">Убедитесь, что в процессе установки 3,4 не появляются диалоговые окна защита ресурсов Windows (WRP). \[\]</span><span class="sxs-lookup"><span data-stu-id="987a3-502">Verify that no Windows Resource Protection (WRP) dialogs appear during the install process \[3.4\]</span></span>
13. <span data-ttu-id="987a3-503">Убедитесь, что повторная вставка диска в дисковод после установки не приводит к повторному запуску установки.</span><span class="sxs-lookup"><span data-stu-id="987a3-503">Verify that re-inserting the disc in the drive after installation does not cause installation to automatically begin again</span></span>
14. <span data-ttu-id="987a3-504">Убедитесь, что игра не требует перезагрузки системы после установки \[ 3,5.\]</span><span class="sxs-lookup"><span data-stu-id="987a3-504">Verify that the game does not require the system to be rebooted after installation \[3.5\]</span></span>
15. <span data-ttu-id="987a3-505">Убедитесь, что вы можете установить игру как пользователь Джейн \[ 3,2.\]</span><span class="sxs-lookup"><span data-stu-id="987a3-505">Verify that you can install the game as User Jane \[3.2\]</span></span>
16. <span data-ttu-id="987a3-506">Убедитесь, что игра автоматически запускается, или что в конце процесса установки имеется меню запуска \[ 3,1\]</span><span class="sxs-lookup"><span data-stu-id="987a3-506">Verify that the game automatically runs or that a launcher menu is present at the end of the installation process \[3.1\]</span></span>
17. <span data-ttu-id="987a3-507">Если игра не запускается после установки, переходите к [исполнению](#55-runtime)</span><span class="sxs-lookup"><span data-stu-id="987a3-507">If the game does auto-run after installation, skip to [Runtime](#55-runtime)</span></span>
18. <span data-ttu-id="987a3-508">Если игра находится в меню запуска или не удалось удалить, см. раздел [после установки](#54-post-install) .</span><span class="sxs-lookup"><span data-stu-id="987a3-508">If the game left a launch menu up, or failed to uninstall see section [Post-Install](#54-post-install)</span></span>

### <a name="54-post-install"></a><span data-ttu-id="987a3-509">5,4 после установки</span><span class="sxs-lookup"><span data-stu-id="987a3-509">5.4 Post-Install</span></span>

1.  <span data-ttu-id="987a3-510">Убедитесь, что игра не размещает ярлыки запуска на рабочем столе пользователя \[ 1,1\]</span><span class="sxs-lookup"><span data-stu-id="987a3-510">Verify that the game does not place launch shortcuts on user desktop \[1.1\]</span></span>
2.  <span data-ttu-id="987a3-511">Убедитесь, что игра не помещает ярлыки запуска в меню "Пуск" \[ 1,1\]</span><span class="sxs-lookup"><span data-stu-id="987a3-511">Verify that the game does not place launch shortcuts in the Start Menu \[1.1\]</span></span>
3.  <span data-ttu-id="987a3-512">Убедитесь, что значок игры отображается в обозревателе игр Windows \[ 1,1\]</span><span class="sxs-lookup"><span data-stu-id="987a3-512">Verify that the game icon displays in Windows Games Explorer \[1.1\]</span></span>
4.  <span data-ttu-id="987a3-513">Убедитесь, что в нижней части отображаются метаданные (издатель, разработчик, жанр, Дата выпуска, версия) и это правильный \[ 1,1.\]</span><span class="sxs-lookup"><span data-stu-id="987a3-513">Verify that the metadata (publisher, developer, genre, release date, version) at the bottom displays and is correct \[1.1\]</span></span>
5.  <span data-ttu-id="987a3-514">Убедитесь, что значок игры отображает сведения индекса производительности Windows (WEI) в обозревателе игр Windows \[ 1,1\]</span><span class="sxs-lookup"><span data-stu-id="987a3-514">Verify that the game icon displays Windows Experience Index (WEI) information in Windows Games Explorer \[1.1\]</span></span>
6.  <span data-ttu-id="987a3-515">Убедитесь, что гиперссылки на игры для метаданных работают правильно в обозревателе игр Windows \[ 1,1\]</span><span class="sxs-lookup"><span data-stu-id="987a3-515">Verify that game hyperlinks for metadata work correctly in Windows Games Explorer \[1.1\]</span></span>
7.  <span data-ttu-id="987a3-516">Убедитесь, что игра отображает точную оценку родительского контроля в обозревателе игр Windows \[ 1,1\]</span><span class="sxs-lookup"><span data-stu-id="987a3-516">Verify that the game displays accurate parental control rating in Windows Games Explorer \[1.1\]</span></span>
8.  <span data-ttu-id="987a3-517">Создание снимка после установки system32</span><span class="sxs-lookup"><span data-stu-id="987a3-517">Create a post-install snapshot of System32</span></span>

    1.  <span data-ttu-id="987a3-518">Вывести окно командной строки (Start-> Run-> cmd)</span><span class="sxs-lookup"><span data-stu-id="987a3-518">Bring up a command Window (Start -> Run -> cmd)</span></span>
    2.  <span data-ttu-id="987a3-519">Перейдите по адресу c: \\ Windows \\ system32</span><span class="sxs-lookup"><span data-stu-id="987a3-519">Navigate to c:\\windows\\system32</span></span>
    3.  <span data-ttu-id="987a3-520">Введите dir/o:-g/o:-d >> c: \\ G4Wtest \\postgame.txt</span><span class="sxs-lookup"><span data-stu-id="987a3-520">Type dir /o:-g /o:-d >> c:\\G4Wtest\\postgame.txt</span></span>
    4.  <span data-ttu-id="987a3-521">Убедитесь, что игра не проверит наличие файлов версий файлов, перечисленных в двух документах, сравнив pregame.txt с postgame.txt \[ 3,6.\]</span><span class="sxs-lookup"><span data-stu-id="987a3-521">Verify that the game does not regress any file versions of files listed in the two documents by comparing pregame.txt to postgame.txt \[3.6\]</span></span>

9.  <span data-ttu-id="987a3-522">Перейти к [исполнению](#55-runtime)</span><span class="sxs-lookup"><span data-stu-id="987a3-522">Proceed to [Runtime](#55-runtime)</span></span>

### <a name="55-runtime"></a><span data-ttu-id="987a3-523">среда выполнения 5,5</span><span class="sxs-lookup"><span data-stu-id="987a3-523">5.5 Runtime</span></span>

1.  <span data-ttu-id="987a3-524">Среда выполнения 1. Если имеется меню запуска, запустите игру отсюда.</span><span class="sxs-lookup"><span data-stu-id="987a3-524">RUNTIME 1: If the launch menu is present, launch the game from there.</span></span> <span data-ttu-id="987a3-525">Если игра запускалась или была запущена из меню средства запуска игр после установки, выполните следующие действия. Если нет, перейдите к ИСПОЛНЕНию 2:</span><span class="sxs-lookup"><span data-stu-id="987a3-525">If the game auto-ran or was launched from the game launcher menu after install, perform the following; if not, skip to RUNTIME 2:</span></span>

    1.  <span data-ttu-id="987a3-526">Создание профиля (если игра разрешена)</span><span class="sxs-lookup"><span data-stu-id="987a3-526">Create a profile (if the game allows)</span></span>
    2.  <span data-ttu-id="987a3-527">Начать новую игру</span><span class="sxs-lookup"><span data-stu-id="987a3-527">Start a new game</span></span>
    3.  <span data-ttu-id="987a3-528">Сохранить игру</span><span class="sxs-lookup"><span data-stu-id="987a3-528">Save the game</span></span>
    4.  <span data-ttu-id="987a3-529">Выйти из игры</span><span class="sxs-lookup"><span data-stu-id="987a3-529">Exit the game</span></span>
    5.  <span data-ttu-id="987a3-530">Запуск игры из обозревателя игр</span><span class="sxs-lookup"><span data-stu-id="987a3-530">Launch the game from Games Explorer</span></span>
    6.  <span data-ttu-id="987a3-531">Убедитесь, что игра запускается из обозревателя игр значок \[ 1,2\]</span><span class="sxs-lookup"><span data-stu-id="987a3-531">Verify that the game launches from the Games Explorer icon \[1.2\]</span></span>
    7.  <span data-ttu-id="987a3-532">Убедитесь, что игра не запрашивает учетные данные администратора при запуске \[ 1,2\]</span><span class="sxs-lookup"><span data-stu-id="987a3-532">Verify that the game does not prompt for Administrator Credentials on launch \[1.2\]</span></span>
    8.  <span data-ttu-id="987a3-533">Убедитесь, что к профилям пользователей и сохранению игр можно получить доступ с помощью учетной записи пользователя Джейн \[ 3,2.\]</span><span class="sxs-lookup"><span data-stu-id="987a3-533">Verify that User Profiles and Save Games can be accessed by User Jane account \[3.2\]</span></span>
    9.  <span data-ttu-id="987a3-534">Перейти к ИСПОЛНЕНию 3</span><span class="sxs-lookup"><span data-stu-id="987a3-534">Proceed to RUNTIME 3</span></span>

2.  <span data-ttu-id="987a3-535">Среда выполнения 2. Если игра не выполнялась в автоматическом режиме или не отображает запуск из меню средства запуска игры, это происходит из-за ошибки \[ 3,1, \] однако тестирование может продолжаться в обычном режиме:</span><span class="sxs-lookup"><span data-stu-id="987a3-535">RUNTIME 2: If the game did not auto-run or display a launch from the game launcher menu, this is a failure of \[3.1\]; however, testing can continue normally:</span></span>

    1.  <span data-ttu-id="987a3-536">Запуск игры из обозревателя игр</span><span class="sxs-lookup"><span data-stu-id="987a3-536">Launch the game from Games Explorer</span></span>
    2.  <span data-ttu-id="987a3-537">Убедитесь, что игра запускается из обозревателя игр значок \[ 1,2\]</span><span class="sxs-lookup"><span data-stu-id="987a3-537">Verify that the game launches from the Games Explorer icon \[1.2\]</span></span>
    3.  <span data-ttu-id="987a3-538">Убедитесь, что игра не запрашивает учетные данные администратора при запуске \[ 1,2\]</span><span class="sxs-lookup"><span data-stu-id="987a3-538">Verify that the game does not prompt for Administrator Credentials on launch \[1.2\]</span></span>
    4.  <span data-ttu-id="987a3-539">Перейти к ИСПОЛНЕНию 3</span><span class="sxs-lookup"><span data-stu-id="987a3-539">Proceed to RUNTIME 3</span></span>

3.  <span data-ttu-id="987a3-540">Среда выполнения 3. Если игра поддерживает игровой планшет, убедитесь, что игра распознает контроллер Xbox 360 для Windows как устройство ввода \[ 1,4\]</span><span class="sxs-lookup"><span data-stu-id="987a3-540">RUNTIME 3: If the game supports a game pad, verify that the game recognizes Xbox 360 Controller for Windows as an input device \[1.4\]</span></span>

    1.  <span data-ttu-id="987a3-541">При необходимости включите контроллер с помощью меню Параметры.</span><span class="sxs-lookup"><span data-stu-id="987a3-541">If needed, enable the controller via the options menu</span></span>
    2.  <span data-ttu-id="987a3-542">Убедитесь, что игра относится к кнопкам контроллера и триггерам, использующим имена Xbox 360.</span><span class="sxs-lookup"><span data-stu-id="987a3-542">Verify that the game refers to the controller buttons and triggers using Xbox 360 names</span></span>
    3.  <span data-ttu-id="987a3-543">Убедитесь, что игра и система меню могут быть управляемыми с помощью контроллера Xbox 360 для Windows.</span><span class="sxs-lookup"><span data-stu-id="987a3-543">Verify that the game and menu system are controllable with the Xbox 360 Controller for Windows</span></span>
    4.  <span data-ttu-id="987a3-544">Убедитесь, что контроллер Xbox 360 для Windows ведет себя в соответствии с принятыми стандартами.</span><span class="sxs-lookup"><span data-stu-id="987a3-544">Verify that the Xbox 360 Controller for Windows behaves according to accepted standards</span></span>

4.  <span data-ttu-id="987a3-545">Установите для видео значение \[ 1,5 \] :</span><span class="sxs-lookup"><span data-stu-id="987a3-545">Set the video to \[1.5\]:</span></span>

    1.  <span data-ttu-id="987a3-546">Убедитесь, что игра выполняется с разрешением пропорции 4:3 (800 600 или 1024 768).</span><span class="sxs-lookup"><span data-stu-id="987a3-546">Verify that the game runs at a 4:3 Aspect Ratio resolution (800 600 or 1024 768)</span></span>
    2.  <span data-ttu-id="987a3-547">Убедитесь, что игра выполняется с разрешением пропорции 16:9 (1280 720).</span><span class="sxs-lookup"><span data-stu-id="987a3-547">Verify that the game runs at a 16:9 Aspect Ratio resolution (1280 720)</span></span>
    3.  <span data-ttu-id="987a3-548">Убедитесь, что игра выполняется с разрешением пропорции 16:10 (1680 1050, 800 480 или 1152 720).</span><span class="sxs-lookup"><span data-stu-id="987a3-548">Verify that the game runs at a 16:10 Aspect Ratio resolution (1680 1050, 800 480, or 1152 720)</span></span>
    4.  <span data-ttu-id="987a3-549">Убедитесь, что игра запрашивает пользователя при изменении разрешения.</span><span class="sxs-lookup"><span data-stu-id="987a3-549">Verify that the game prompts the user when a change is made to the resolution</span></span>
    5.  <span data-ttu-id="987a3-550">Убедитесь, что отображение возвращается к предыдущему параметру, если не принято в течение 15 секунд.</span><span class="sxs-lookup"><span data-stu-id="987a3-550">Verify that the display reverts to the previous setting if you do not accept within 15 seconds</span></span>
    6.  <span data-ttu-id="987a3-551">Убедитесь, что игра не растягивает изображение и, в свою очередь, представляет более широкую область зрения</span><span class="sxs-lookup"><span data-stu-id="987a3-551">Verify that the game does not stretch the picture and in turn presents a wider area of view</span></span>
    7.  <span data-ttu-id="987a3-552">Убедитесь, что игра не добавляет черные полосы слева и справа от области игры.</span><span class="sxs-lookup"><span data-stu-id="987a3-552">Verify that the game does not add black bars to the left and right of the game play area</span></span>

5.  <span data-ttu-id="987a3-553">Если в параметрах видео есть значение, убедитесь, что параметры визуализации игры по умолчанию имеют значение Direct3D \[ 1,7 \] ; в противном случае перейдите к [автоматическим тестам](#58-automated-tests) .</span><span class="sxs-lookup"><span data-stu-id="987a3-553">If available in the video settings, verify that the game render options default to Direct3D \[1.7\]; otherwise, proceed to [Automated Tests](#58-automated-tests)</span></span>
6.  <span data-ttu-id="987a3-554">При появлении запроса или если параметр доступен, создайте профиль пользователя.</span><span class="sxs-lookup"><span data-stu-id="987a3-554">If prompted or if the option is available, create a user profile.</span></span> <span data-ttu-id="987a3-555">Убедитесь, что игра не сталкивается с ошибками при использовании длинных имен файлов \[ 2,7\]</span><span class="sxs-lookup"><span data-stu-id="987a3-555">Verify that the game does not encounter errors when using long file names \[2.7\]</span></span>
7.  <span data-ttu-id="987a3-556">Запустите новую игру, создайте игру Save и убедитесь, что игра не сталкивается с ошибками при обработке неподдерживаемых символов файловой системы \[ 2,7\]</span><span class="sxs-lookup"><span data-stu-id="987a3-556">Start a new game, create a game save, and verify that the game does not encounter errors when handling unsupported file system characters \[2.7\]</span></span>
8.  <span data-ttu-id="987a3-557">Убедитесь, что игра правильно ALT + Табуляция на рабочем столе Windows \[ 2,6\]</span><span class="sxs-lookup"><span data-stu-id="987a3-557">Verify that the game properly ALT+TABs to the Windows desktop \[2.6\]</span></span>

    1.  <span data-ttu-id="987a3-558">Переключитесь на пользователей с запущенной игрой, нажав кнопку Пуск-> Сменить пользователя.</span><span class="sxs-lookup"><span data-stu-id="987a3-558">Switch users with the game running by clicking Start -> Switch User</span></span>
    2.  <span data-ttu-id="987a3-559">Вход в систему как Тоби</span><span class="sxs-lookup"><span data-stu-id="987a3-559">Log on as Toby</span></span>
    3.  <span data-ttu-id="987a3-560">Убедитесь, что игра запускается как пользователь Тоби, но по-прежнему выполняется от имени пользователя Джейн \[ 2,6.\]</span><span class="sxs-lookup"><span data-stu-id="987a3-560">Verify that the game launches as User Toby while still running as User Jane \[2.6\]</span></span>
    4.  <span data-ttu-id="987a3-561">Убедитесь, что игра не сталкивается с ошибками для пользователя Тоби или Джейн пользователя во время процесса переключения пользователя \[ 2,6\]</span><span class="sxs-lookup"><span data-stu-id="987a3-561">Verify that the game does not encounter errors for User Toby or User Jane during User Switch process \[2.6\]</span></span>
    5.  <span data-ttu-id="987a3-562">Убедитесь, что вы не слышите звук из исходного сеанса игры \[ 2,6\]</span><span class="sxs-lookup"><span data-stu-id="987a3-562">Verify that you cannot hear audio from the original game session \[2.6\]</span></span>
    6.  <span data-ttu-id="987a3-563">Выйти из игры</span><span class="sxs-lookup"><span data-stu-id="987a3-563">Exit the game</span></span>
    7.  <span data-ttu-id="987a3-564">Выход из Тоби</span><span class="sxs-lookup"><span data-stu-id="987a3-564">Log off Toby</span></span>
    8.  <span data-ttu-id="987a3-565">Переключитесь обратно на исходного пользователя, где запущена игра</span><span class="sxs-lookup"><span data-stu-id="987a3-565">Switch back to the original user where the game is running</span></span>
    9.  <span data-ttu-id="987a3-566">ALT + TAB вернуться в игру</span><span class="sxs-lookup"><span data-stu-id="987a3-566">ALT+TAB back into the game</span></span>

9.  <span data-ttu-id="987a3-567">Выйти из игры</span><span class="sxs-lookup"><span data-stu-id="987a3-567">Exit the game</span></span>
10. <span data-ttu-id="987a3-568">Перейти к выполнению [после выполнения](#56-post-runtime)</span><span class="sxs-lookup"><span data-stu-id="987a3-568">Proceed to [Post-Runtime](#56-post-runtime)</span></span>

### <a name="56-post-runtime"></a><span data-ttu-id="987a3-569">5,6 после выполнения</span><span class="sxs-lookup"><span data-stu-id="987a3-569">5.6 Post-Runtime</span></span>

1.  <span data-ttu-id="987a3-570">Убедитесь, что игра не создает ошибки при выходе из программы \[ 4,3\]</span><span class="sxs-lookup"><span data-stu-id="987a3-570">Verify that the game does not generate errors on exit \[4.3\]</span></span>
2.  <span data-ttu-id="987a3-571">Убедитесь, что игра установлена в Program Files \[ 3,3\]</span><span class="sxs-lookup"><span data-stu-id="987a3-571">Verify that the game installed to Program Files \[3.3\]</span></span>
3.  <span data-ttu-id="987a3-572">Перейти к [родительским элементам управления](/windows)</span><span class="sxs-lookup"><span data-stu-id="987a3-572">Proceed to [Parental Controls](/windows)</span></span>

### <a name="57-parental-controls"></a><span data-ttu-id="987a3-573">5,7 родительский контроль</span><span class="sxs-lookup"><span data-stu-id="987a3-573">5.7 Parental Controls</span></span>

1.  <span data-ttu-id="987a3-574">Открытие родительского элемента управления в панели управления</span><span class="sxs-lookup"><span data-stu-id="987a3-574">Open Parental Controls in Control Panel</span></span>
2.  <span data-ttu-id="987a3-575">Убедитесь, что в игре отображается Точная оценка родительского контроля под названием игры в панели управления родительского контроля \[ 1,2\]</span><span class="sxs-lookup"><span data-stu-id="987a3-575">Verify that the game displays accurate Parental Control Rating below the game title in Parental Controls Control Panel \[1.2\]</span></span>
3.  <span data-ttu-id="987a3-576">См. тестовый случай \[ 1,2 \] для следующих тестов:</span><span class="sxs-lookup"><span data-stu-id="987a3-576">See Test Case \[1.2\] for the following tests:</span></span>

    1.  <span data-ttu-id="987a3-577">После настройки родительского контроля на "вкл." убедитесь, что игра выполняется с этими параметрами в качестве пользователя Джейн \[ 1,2\]</span><span class="sxs-lookup"><span data-stu-id="987a3-577">After setting Parental Controls to "On", verify that the game runs with these settings as User Jane \[1.2\]</span></span>
    2.  <span data-ttu-id="987a3-578">Выйдите из системы и войдите в систему как Тоби</span><span class="sxs-lookup"><span data-stu-id="987a3-578">Log off and log on as Toby</span></span>
    3.  <span data-ttu-id="987a3-579">Убедитесь, что игра выполняется с этими параметрами в качестве пользователя Тоби \[ 1,2.\]</span><span class="sxs-lookup"><span data-stu-id="987a3-579">Verify that the game runs with these settings as User Toby \[1.2\]</span></span>
    4.  <span data-ttu-id="987a3-580">Выйдите из системы и войдите в систему как Джейн</span><span class="sxs-lookup"><span data-stu-id="987a3-580">Log off and log on as Jane</span></span>
    5.  <span data-ttu-id="987a3-581">В разделе "родительский контроль" запрещайте пользователям Тоби просматривать игры на одном уровне ЕСРБ выше и выше в игре, которую вы только что установили.</span><span class="sxs-lookup"><span data-stu-id="987a3-581">In the Parental Control section, block User Toby from seeing games one ESRB level up and higher from the game that you just installed</span></span>

        <span data-ttu-id="987a3-582">Пример. Если игра имеет оценку E, настройте ее так, чтобы Тоби мог играть только игры с оценкой C</span><span class="sxs-lookup"><span data-stu-id="987a3-582">Example: If the game is rated E, set it so Toby can only play games that are rated C</span></span>

    6.  <span data-ttu-id="987a3-583">Убедитесь, что игра выполняется с этими параметрами в качестве пользователя Джейн \[ 1,2.\]</span><span class="sxs-lookup"><span data-stu-id="987a3-583">Verify that the game runs with these settings as User Jane \[1.2\]</span></span>
    7.  <span data-ttu-id="987a3-584">Выйдите из системы и войдите в систему как пользователь Тоби</span><span class="sxs-lookup"><span data-stu-id="987a3-584">Log off and log on as user Toby</span></span>
    8.  <span data-ttu-id="987a3-585">Убедитесь, что игра не запускается на пользователе Тоби, когда ЕСРБ заблокирован пользователем Джейн 1,2. \[\]</span><span class="sxs-lookup"><span data-stu-id="987a3-585">Verify that the game does not launch on User Toby when ESRB is blocked by User Jane \[1.2\]</span></span>
    9.  <span data-ttu-id="987a3-586">Выйдите из системы как пользователь Тоби и снова в качестве пользователя Джейн</span><span class="sxs-lookup"><span data-stu-id="987a3-586">Log off as user Toby and back on as user Jane</span></span>
    10. <span data-ttu-id="987a3-587">Если вы изменили ранее, восстановите параметры ЕСРБ.</span><span class="sxs-lookup"><span data-stu-id="987a3-587">If changed previously, restore the ESRB settings</span></span>
    11. <span data-ttu-id="987a3-588">Если параметры ЕСРБ отсутствуют, выберите "блокировать или разрешить определенные игры" и выберите игру по имени.</span><span class="sxs-lookup"><span data-stu-id="987a3-588">If there are no ESRB settings, then select "Block or Allow Specific Games" and select the game by name</span></span>
    12. <span data-ttu-id="987a3-589">Выйдите от имени Джейн и Тоби</span><span class="sxs-lookup"><span data-stu-id="987a3-589">Log off as Jane and on as Toby</span></span>
    13. <span data-ttu-id="987a3-590">Убедитесь, что игра не запускается на пользователе Тоби, когда имя EXE-файла заблокировано пользователем Джейн \[ 1,2.\]</span><span class="sxs-lookup"><span data-stu-id="987a3-590">Verify that the game does not launch on User Toby when EXE/Name is blocked by User Jane \[1.2\]</span></span>
    14. <span data-ttu-id="987a3-591">Выйдите как Тоби и снова в виде Джейн</span><span class="sxs-lookup"><span data-stu-id="987a3-591">Log off as Toby and back on as Jane</span></span>
    15. <span data-ttu-id="987a3-592">Как Джейн, откройте пользовательский элемент управления — ограничения для приложений ></span><span class="sxs-lookup"><span data-stu-id="987a3-592">As Jane, open User Controls -> Application Restrictions</span></span>
    16. <span data-ttu-id="987a3-593">Щелкните "Тоби может использовать только разрешенные программы" и нажмите кнопку "ОК" (т. е. разрешить без exe-файлы).</span><span class="sxs-lookup"><span data-stu-id="987a3-593">Click "Toby can only use the programs I allow", and then click OK (i.e. allow no exes)</span></span>
    17. <span data-ttu-id="987a3-594">Установите флажок снять все и нажмите кнопку ОК.</span><span class="sxs-lookup"><span data-stu-id="987a3-594">Click the Uncheck All box, and then click OK</span></span>
    18. <span data-ttu-id="987a3-595">Переход к элементу user controls \| Controls Games и разрешение конкретной игры с ОЦЕНКОЙ есрб</span><span class="sxs-lookup"><span data-stu-id="987a3-595">Go to User Controls \| Games Controls and allow the specific game using the ESRB rating</span></span>
    19. <span data-ttu-id="987a3-596">Выйдите как Мария и войдите в систему как Тоби и попытайтесь воспроизвести игру.</span><span class="sxs-lookup"><span data-stu-id="987a3-596">Log off as Jane and log on as Toby and try to play the game</span></span>
    20. <span data-ttu-id="987a3-597">Убедитесь, что игра не заблокирована и Тоби может воспроизвести ее, если параметр "разрешить без exe" установлен в значение \[ 1,2\]</span><span class="sxs-lookup"><span data-stu-id="987a3-597">Verify that the game is NOT blocked and that Toby can play it when "allow no exes" is set \[1.2\]</span></span>
    21. <span data-ttu-id="987a3-598">Выйдите из системы как пользователь Тоби и снова в качестве пользователя Джейн</span><span class="sxs-lookup"><span data-stu-id="987a3-598">Log off as user Toby and back on as user Jane</span></span>
    22. <span data-ttu-id="987a3-599">Перейдите в раздел Родительский контроль на панели управления и удалите ограничения.</span><span class="sxs-lookup"><span data-stu-id="987a3-599">Go to Parental Controls in Control Panel and remove the restrictions</span></span>
    23. <span data-ttu-id="987a3-600">Убедитесь, что оба пользователя теперь могут играть игру</span><span class="sxs-lookup"><span data-stu-id="987a3-600">Verify that both users can now play the game</span></span>

4.  <span data-ttu-id="987a3-601">Перейти к [автоматическим тестам](#58-automated-tests)</span><span class="sxs-lookup"><span data-stu-id="987a3-601">Proceed to [Automated Tests](#58-automated-tests)</span></span>

### <a name="58-automated-tests"></a><span data-ttu-id="987a3-602">5,8 автоматические тесты</span><span class="sxs-lookup"><span data-stu-id="987a3-602">5.8 Automated Tests</span></span>

1.  <span data-ttu-id="987a3-603">Убедитесь, что игра не создает ошибки при запуске в разделе средство проверки приложений — см. документацию по средству тестирования фирменной символики \[ 4,2\]</span><span class="sxs-lookup"><span data-stu-id="987a3-603">Verify that the game does not generate failures when run under Application Verifier - See Branding Test Tool Documentation \[4.2\]</span></span>
2.  <span data-ttu-id="987a3-604">Убедитесь, что исполняемые файлы игры содержат манифесты — см. документацию по средству тестирования для фирменной символики \[ 2,1\]</span><span class="sxs-lookup"><span data-stu-id="987a3-604">Verify that the game executable files contain manifests - see Branding Test Tool Documentation \[2.1\]</span></span>
3.  <span data-ttu-id="987a3-605">Убедитесь, что файл манифеста исполняемого файла игры requestedExecutionLevel имеет значение "AsInvoker" — см. документацию по средству тестирования фирменной символики \[ 2,1\]</span><span class="sxs-lookup"><span data-stu-id="987a3-605">Verify that the game executable file manifest requestedExecutionLevel is "AsInvoker" - see Branding Test Tool Documentation \[2.1\]</span></span>
4.  <span data-ttu-id="987a3-606">Перейти к [другим тестам](#59-other-tests)</span><span class="sxs-lookup"><span data-stu-id="987a3-606">Proceed to [Other Tests](#59-other-tests)</span></span>

### <a name="59-other-tests"></a><span data-ttu-id="987a3-607">5,9 другие тесты</span><span class="sxs-lookup"><span data-stu-id="987a3-607">5.9 Other Tests</span></span>

1.  <span data-ttu-id="987a3-608">Убедитесь, что исполняемые файлы игры содержат цифровую подпись \[ 2,3\]</span><span class="sxs-lookup"><span data-stu-id="987a3-608">Verify that the game executable files contain a digital signature \[2.3\]</span></span>
2.  <span data-ttu-id="987a3-609">Убедитесь, что процесс установки игры выполняется как обычно в 64-разрядных выпусках Windows Vista и (или) Windows 7 \[ 2,3\]</span><span class="sxs-lookup"><span data-stu-id="987a3-609">Verify that the game installation process runs normally on 64-bit editions of Windows Vista and/or Windows 7 \[2.3\]</span></span>
3.  <span data-ttu-id="987a3-610">Убедитесь, что игра не обнаружила ошибку в результате 16-разрядных исполняемых файлов в 64-разрядных выпусках Windows Vista и (или) Windows 7 \[ 2,3\]</span><span class="sxs-lookup"><span data-stu-id="987a3-610">Verify that the game does not encounter an error as a result of 16-bit executables on 64-bit editions of Windows Vista and/or Windows 7 \[2.3\]</span></span>
4.  <span data-ttu-id="987a3-611">Принудительно завершить работу приложения во время тестирования и убедиться, что игра правильно отображается отчеты об ошибках Windows и собирает данные о сбое \[ 4,3\]</span><span class="sxs-lookup"><span data-stu-id="987a3-611">Force the application to crash while testing, and verify that the game displays Windows Error Reporting properly and collects crash data \[4.3\]</span></span>
5.  <span data-ttu-id="987a3-612">Обеспечение правильных сводок файлов \[ 4,3\]</span><span class="sxs-lookup"><span data-stu-id="987a3-612">Ensure proper file summaries \[4.3\]</span></span>

    1.  <span data-ttu-id="987a3-613">Нажмите кнопку Пуск — > компьютер.</span><span class="sxs-lookup"><span data-stu-id="987a3-613">Click Start -> Computer</span></span>
    2.  <span data-ttu-id="987a3-614">Переход к каталогу игр</span><span class="sxs-lookup"><span data-stu-id="987a3-614">Navigate to the game directory</span></span>
    3.  <span data-ttu-id="987a3-615">В окне поиска введите \*.dll</span><span class="sxs-lookup"><span data-stu-id="987a3-615">In the search window, type \*.dll</span></span>
    4.  <span data-ttu-id="987a3-616">Для каждого файла щелкните правой кнопкой мыши файл и выберите пункт Свойства.</span><span class="sxs-lookup"><span data-stu-id="987a3-616">For each file: Right-click the file and click Properties</span></span>

        -   <span data-ttu-id="987a3-617">В Windows XP: перейдите на вкладку версия. Убедитесь, что поля Название продукта, название организации и версия файла заполнены правильно.</span><span class="sxs-lookup"><span data-stu-id="987a3-617">In Windows XP: Click the Version tab. Verify that the Product Name, Company Name, and File Version fields are properly populated.</span></span> <span data-ttu-id="987a3-618">\[4.3\]</span><span class="sxs-lookup"><span data-stu-id="987a3-618">\[4.3\]</span></span>
        -   <span data-ttu-id="987a3-619">В Windows Vista и Windows 7: перейдите на вкладку сведения. Убедитесь, что поля Название продукта и версия файла заполнены должным образом.</span><span class="sxs-lookup"><span data-stu-id="987a3-619">In Windows Vista and Windows 7: Click the Details tab. Verify that the Product name and File Version fields are properly populated.</span></span> <span data-ttu-id="987a3-620">Название компании не отображается на странице свойств Windows Vista или Windows 7 \[ 4,3\]</span><span class="sxs-lookup"><span data-stu-id="987a3-620">Company Name is not visible in the Windows Vista or Windows 7 properties page \[4.3\]</span></span>

    5.  <span data-ttu-id="987a3-621">Повторите эту проверку для файлов .exe</span><span class="sxs-lookup"><span data-stu-id="987a3-621">Repeat this check for .exe files</span></span>

6.  <span data-ttu-id="987a3-622">Запустите игру.</span><span class="sxs-lookup"><span data-stu-id="987a3-622">Launch the game.</span></span>

    1.  <span data-ttu-id="987a3-623">Нажмите клавиши CTRL + ALT + DEL.</span><span class="sxs-lookup"><span data-stu-id="987a3-623">Press CTRL+ALT+DEL</span></span>
    2.  <span data-ttu-id="987a3-624">Щелкните стрелку "Параметры завершения работы".</span><span class="sxs-lookup"><span data-stu-id="987a3-624">Click the "Shutdown Options" arrow</span></span>
    3.  <span data-ttu-id="987a3-625">Нажмите кнопку Перезапустить.</span><span class="sxs-lookup"><span data-stu-id="987a3-625">Click Restart</span></span>
    4.  <span data-ttu-id="987a3-626">Проверка игры не блокирует завершение работы \[ 3,1\]</span><span class="sxs-lookup"><span data-stu-id="987a3-626">Verify game does not block shutdown \[3.1\]</span></span>

7.  <span data-ttu-id="987a3-627">Перейти к [удалению](#510-uninstall)</span><span class="sxs-lookup"><span data-stu-id="987a3-627">Proceed to [Uninstall](#510-uninstall)</span></span>

### <a name="510-uninstall"></a><span data-ttu-id="987a3-628">Удаление 5,10</span><span class="sxs-lookup"><span data-stu-id="987a3-628">5.10 Uninstall</span></span>

-   <span data-ttu-id="987a3-629">Убедитесь, что процесс удаления игры удаляет все установленные, нераспространенные файлы компонентов операционной системы и очищает все параметры \[ 3,1.\]</span><span class="sxs-lookup"><span data-stu-id="987a3-629">Verify that the game uninstallation process removes all installed, non-redistributed operating system component files and clears all settings \[3.1\]</span></span>

    -   <span data-ttu-id="987a3-630">Убедитесь, что в Windows Vista или Windows 7 единственный способ удаления программы \[ 1,1\]</span><span class="sxs-lookup"><span data-stu-id="987a3-630">Verify in Windows Vista or Windows 7 that Control Panel is the only way to remove the program \[1.1\]</span></span>

## <a name="test-tool-notes"></a><span data-ttu-id="987a3-631">Заметки к средству тестирования</span><span class="sxs-lookup"><span data-stu-id="987a3-631">Test Tool Notes</span></span>

<span data-ttu-id="987a3-632">Это примечания для каждого из средств тестирования, перечисленных в приведенных выше тестовых требованиях.</span><span class="sxs-lookup"><span data-stu-id="987a3-632">These are notes for each of the test tools listed in the above test requirements.</span></span>

### <a name="61-appverifier-40-or-higher"></a><span data-ttu-id="987a3-633">6,1 AppVerifier 4,0 (или более поздней версии)</span><span class="sxs-lookup"><span data-stu-id="987a3-633">6.1 Appverifier 4.0 (or higher)</span></span>

<span data-ttu-id="987a3-634">**Тестовый случай: 2,5, 4,2**</span><span class="sxs-lookup"><span data-stu-id="987a3-634">**Test Case: 2.5, 4.2**</span></span>

> [!Note]  
> <span data-ttu-id="987a3-635">Некоторые приложения не работают с AppVerifier, так как защита от копирования.</span><span class="sxs-lookup"><span data-stu-id="987a3-635">Some applications fail to run with AppVerifier running, because of copy protection.</span></span> <span data-ttu-id="987a3-636">Это можно разрешить, выполнив с незащищенной версией выпуска исполняемого файла игры.</span><span class="sxs-lookup"><span data-stu-id="987a3-636">This can be resolved by running with an unprotected release version of the game executable.</span></span>

 

1.  <span data-ttu-id="987a3-637">Установка AppVerifier 4,0 (или более поздней версии) на компьютере под управлением Windows XP</span><span class="sxs-lookup"><span data-stu-id="987a3-637">Install AppVerifier 4.0 (or higher) on a computer running Windows XP</span></span>
2.  <span data-ttu-id="987a3-638">Запустите AppVerifier и выберите файл — > добавить приложение.</span><span class="sxs-lookup"><span data-stu-id="987a3-638">Launch AppVerifier and click File -> Add Application</span></span>
3.  <span data-ttu-id="987a3-639">Перейдите к исполняемому файлу игры, выберите его и нажмите кнопку Открыть.</span><span class="sxs-lookup"><span data-stu-id="987a3-639">Locate the game executable, select it and click Open</span></span>
4.  <span data-ttu-id="987a3-640">В разделе "приложения" выберите исполняемый файл игры</span><span class="sxs-lookup"><span data-stu-id="987a3-640">In the "Applications" section, select the game executable</span></span>
5.  <span data-ttu-id="987a3-641">В разделе "Основные сведения" выберите следующие тесты:</span><span class="sxs-lookup"><span data-stu-id="987a3-641">Select the following tests in the "Basics" section:</span></span>

    -   <span data-ttu-id="987a3-642">Маркеры</span><span class="sxs-lookup"><span data-stu-id="987a3-642">Handles</span></span>
    -   <span data-ttu-id="987a3-643">Кучи</span><span class="sxs-lookup"><span data-stu-id="987a3-643">Heaps</span></span>
    -   <span data-ttu-id="987a3-644">Блокировки</span><span class="sxs-lookup"><span data-stu-id="987a3-644">Locks</span></span>
    -   <span data-ttu-id="987a3-645">Память</span><span class="sxs-lookup"><span data-stu-id="987a3-645">Memory</span></span>
    -   <span data-ttu-id="987a3-646">TLS</span><span class="sxs-lookup"><span data-stu-id="987a3-646">TLS</span></span>

6.  <span data-ttu-id="987a3-647">В разделе "Прочие" выберите следующие тесты:</span><span class="sxs-lookup"><span data-stu-id="987a3-647">Select the following tests in the "Miscellaneous" section:</span></span>

    -   <span data-ttu-id="987a3-648">данжераусапис</span><span class="sxs-lookup"><span data-stu-id="987a3-648">DangerousAPIs</span></span>
    -   <span data-ttu-id="987a3-649">диртистаккс</span><span class="sxs-lookup"><span data-stu-id="987a3-649">DirtyStacks</span></span>

7.  <span data-ttu-id="987a3-650">Убедитесь, что все остальные тесты не выбраны</span><span class="sxs-lookup"><span data-stu-id="987a3-650">Ensure all other tests are not selected</span></span>
8.  <span data-ttu-id="987a3-651">Запустить игру</span><span class="sxs-lookup"><span data-stu-id="987a3-651">Launch the game</span></span>
9.  <span data-ttu-id="987a3-652">Играть в игру</span><span class="sxs-lookup"><span data-stu-id="987a3-652">Play the game</span></span>
10. <span data-ttu-id="987a3-653">Закрыть игру</span><span class="sxs-lookup"><span data-stu-id="987a3-653">Close the game</span></span>
11. <span data-ttu-id="987a3-654">В AppVerifier выберите View-> журналы.</span><span class="sxs-lookup"><span data-stu-id="987a3-654">In AppVerifier select View -> Logs</span></span>
12. <span data-ttu-id="987a3-655">В разделе "приложения" выберите файл .exe приложения.</span><span class="sxs-lookup"><span data-stu-id="987a3-655">In the "Applications" section select the app .exe file</span></span>
13. <span data-ttu-id="987a3-656">В разделе "журналы" выберите файл журнала и просмотрите количество ошибок.</span><span class="sxs-lookup"><span data-stu-id="987a3-656">In the "Logs" section, select the log file and observe the error count.</span></span> <span data-ttu-id="987a3-657">Если ошибок нет, завершите тесты AppVerifier.</span><span class="sxs-lookup"><span data-stu-id="987a3-657">If there are no errors, then end AppVerifier tests.</span></span> <span data-ttu-id="987a3-658">При наличии ошибок нажмите кнопку "Просмотр"</span><span class="sxs-lookup"><span data-stu-id="987a3-658">If there are errors, click the View button</span></span>
14. <span data-ttu-id="987a3-659">Поиск в документе (CTRL + F) для уровня серьезности = "ошибка"</span><span class="sxs-lookup"><span data-stu-id="987a3-659">Search the document (CTRL+F) for Severity="Error</span></span>
15. <span data-ttu-id="987a3-660">Создание ошибок на основе Имя_слоя = части сбоя</span><span class="sxs-lookup"><span data-stu-id="987a3-660">Create bugs based on the LayerName= portion of the failure</span></span>

### <a name="62-manifest-test---mtexe"></a><span data-ttu-id="987a3-661">Тест манифеста 6,2 — mt.exe</span><span class="sxs-lookup"><span data-stu-id="987a3-661">6.2 Manifest Test - mt.exe</span></span>

<span data-ttu-id="987a3-662">**Тестовый случай: 1,8, 2,1**</span><span class="sxs-lookup"><span data-stu-id="987a3-662">**Test Case: 1.8, 2.1**</span></span>

<span data-ttu-id="987a3-663">Это средство запускается из командной строки, в которой находится MT.exe.</span><span class="sxs-lookup"><span data-stu-id="987a3-663">This tool is run from a command prompt where MT.exe is located.</span></span>

<span data-ttu-id="987a3-664">Пример.</span><span class="sxs-lookup"><span data-stu-id="987a3-664">Example:</span></span>

``` syntax
mt.exe -inputresource:"c:\yourdir\YourGame.exe";#1 -out:yourgame.manifest
```

1.  <span data-ttu-id="987a3-665">Нажмите кнопку Пуск-> Run-> Type cmd и нажмите кнопку ОК.</span><span class="sxs-lookup"><span data-stu-id="987a3-665">Click Start -> Run -> type cmd and click the OK button</span></span>
2.  <span data-ttu-id="987a3-666">Запустите средство mt.exe, чтобы создать файл манифеста для каждого файла .exe, который устанавливается вместе с игрой.</span><span class="sxs-lookup"><span data-stu-id="987a3-666">Run the mt.exe tool to generate a .manifest file for each .exe file that installs with the game</span></span>
3.  <span data-ttu-id="987a3-667">Открытие созданного файла. manifest</span><span class="sxs-lookup"><span data-stu-id="987a3-667">Open the generated .manifest file</span></span>
4.  <span data-ttu-id="987a3-668">Убедитесь, что каждый файл .exe содержит следующее (запрошено:</span><span class="sxs-lookup"><span data-stu-id="987a3-668">Ensure that each .exe file contains the following (requested:</span></span>

    ``` syntax
    <description>Example Game Name</description>
    <trustInfo xmlns="urn:schemas-microsoft-com:asm.v2">
      <security>
        <requestedPrivileges>
          <requestedExecutionLevel level="asInvoker"></requestedExecutionLevel>
        </requestedPrivileges>
      </security>
    </trustInfo>
      <asmv3:windowsSettings xmlns=http://schemas.microsoft.com/SMI/2005/WindowsSettings>
        <dpiAware>true<dpiAware>
      </asmv3:windowsSettings>
    </asmv3:application>
    ```

> [!Note]  
> <span data-ttu-id="987a3-669">Запрошенный уровень выполнения должен присутствовать для каждого файла, а Дпиаваре должен присутствовать по крайней мере для исполняемого файла Game.</span><span class="sxs-lookup"><span data-stu-id="987a3-669">Requested execution level should be present for every file, and dpiAware should be present for at least the game s executable file.</span></span>

 

### <a name="63-thread-hijacker---threadhijackerexe"></a><span data-ttu-id="987a3-670">6,3. захват потока — threadhijacker.exe</span><span class="sxs-lookup"><span data-stu-id="987a3-670">6.3 Thread Hijacker - threadhijacker.exe</span></span>

<span data-ttu-id="987a3-671">Это средство запускается из командной строки, в которой находится threadhijacker.exe.</span><span class="sxs-lookup"><span data-stu-id="987a3-671">This tool is run from a command prompt where threadhijacker.exe is located.</span></span>

<span data-ttu-id="987a3-672">Пример.</span><span class="sxs-lookup"><span data-stu-id="987a3-672">Example:</span></span>

``` syntax
threadhijacker.exe /process:str
```

<span data-ttu-id="987a3-673">Где str — имя \_ \_program.exe</span><span class="sxs-lookup"><span data-stu-id="987a3-673">Where str is the name\_of\_program.exe</span></span>

1.  <span data-ttu-id="987a3-674">Откройте диспетчер задач, перейдите на вкладку процессы и укажите имя исполняемого файла игры.</span><span class="sxs-lookup"><span data-stu-id="987a3-674">Bring up Task Manager, click the Processes tab, and locate the name of the game executable.</span></span>
2.  <span data-ttu-id="987a3-675">Открытие командной строки в режиме администратора</span><span class="sxs-lookup"><span data-stu-id="987a3-675">Open a command prompt in Admin mode</span></span>
3.  <span data-ttu-id="987a3-676">Перейдите в каталог, где threadhijacker.exe</span><span class="sxs-lookup"><span data-stu-id="987a3-676">Navigate to the directory where threadhijacker.exe is</span></span>
4.  <span data-ttu-id="987a3-677">Введите: **threadhijacker.exe/Process:** str, где str — это имя исполняемого файла, который вы хотите использовать.</span><span class="sxs-lookup"><span data-stu-id="987a3-677">Type: **threadhijacker.exe /process:** str, where str is the name of the executable that you want to hit</span></span>

### <a name="64-microsoft-games-for-windows-test-tool"></a><span data-ttu-id="987a3-678">6,4. игры Майкрософт для инструмента тестирования Windows</span><span class="sxs-lookup"><span data-stu-id="987a3-678">6.4 Microsoft Games for Windows Test Tool</span></span>

<span data-ttu-id="987a3-679">Это средство находится в пакете SDK для DirectX.</span><span class="sxs-lookup"><span data-stu-id="987a3-679">This tool is located in the DirectX SDK.</span></span> <span data-ttu-id="987a3-680">После установки пакета SDK на компьютере установщик средств тестирования для игр можно разместить на тестовом компьютере и установить.</span><span class="sxs-lookup"><span data-stu-id="987a3-680">Once the SDK is installed on a computer, the installer for the Games for Windows Test Tool can be placed on the test computer and installed.</span></span>

<span data-ttu-id="987a3-681">На компьютере разработчика, на котором установлен пакет SDK для DirectX, откройте раздел Игры Microsoft Games для средства тестирования Windows.</span><span class="sxs-lookup"><span data-stu-id="987a3-681">Locate the Microsoft Games for Windows Test Tool installer on the development computer where the DirectX SDK is installed.</span></span> <span data-ttu-id="987a3-682">По умолчанию он размещается в следующем расположении:</span><span class="sxs-lookup"><span data-stu-id="987a3-682">By default, it is placed in the following location:</span></span>

``` syntax
%SystemDrive%\Program Files (x86)\Microsoft DirectX SDK (Date)\Utilities\bin\x86\Microsoft Games for Windows Test Tools\
```

1.  <span data-ttu-id="987a3-683">Скопируйте установщик (MicrosoftGFWTestTool.msi и setup.exe) на тестовый компьютер.</span><span class="sxs-lookup"><span data-stu-id="987a3-683">Copy the installer (MicrosoftGFWTestTool.msi / setup.exe) to the test computer.</span></span>
2.  <span data-ttu-id="987a3-684">Запустите установщик.</span><span class="sxs-lookup"><span data-stu-id="987a3-684">Run the installer.</span></span>
3.  <span data-ttu-id="987a3-685">Запустите средство тестирования игр Microsoft для Windows.</span><span class="sxs-lookup"><span data-stu-id="987a3-685">Launch the Microsoft Games for Windows Test Tool.</span></span>
4.  <span data-ttu-id="987a3-686">В поле **список проектов** замените **создать проект** именем вашего заголовка и щелкните **создать**.</span><span class="sxs-lookup"><span data-stu-id="987a3-686">In the **Project List** field replace **Create New Project** with your title name and click **Create New**.</span></span>

    <span data-ttu-id="987a3-687">Дождитесь завершения базового плана.</span><span class="sxs-lookup"><span data-stu-id="987a3-687">Wait for the Baseline to complete.</span></span>

5.  <span data-ttu-id="987a3-688">Введите любые сведения, которые могут присутствовать в разделе " **сведения об игре** ", и щелкните **Обновить сведения об игре**.</span><span class="sxs-lookup"><span data-stu-id="987a3-688">Fill in any information that you may have in the **Game Information** section, and click **Update Game Information**.</span></span>
6.  <span data-ttu-id="987a3-689">Перейдите на вкладку **тестовые случаи** .</span><span class="sxs-lookup"><span data-stu-id="987a3-689">Click on **Test Cases** tab.</span></span>
7.  <span data-ttu-id="987a3-690">Начиная с верхней части, пройдите по тестовым случаям, выбрав пункт **пропустить** или **завершить с ошибкой** .</span><span class="sxs-lookup"><span data-stu-id="987a3-690">Starting at the top, proceed through the test cases, clicking **Pass** or **Fail** as appropriate.</span></span>

    <span data-ttu-id="987a3-691">Дополнительные сведения о включении ошибки в отчет см. в подразделе «написание ошибки» далее в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="987a3-691">See "Writing a Bug", later in this section, for details on including a bug in the report.</span></span>

8.  <span data-ttu-id="987a3-692">Вернитесь на вкладку **проекты** после просмотра отчета (путем проверки вкладок **отчет** и **изменение ошибки** ).</span><span class="sxs-lookup"><span data-stu-id="987a3-692">Return to the **Projects** tab after reviewing the report (by checking the **Report** and **Bug Edit** tabs).</span></span>
9.  <span data-ttu-id="987a3-693">Нажмите кнопку **компилировать отчет**.</span><span class="sxs-lookup"><span data-stu-id="987a3-693">Click **Compile Report**.</span></span>

    <span data-ttu-id="987a3-694">После завершения компиляции отчета откроется окно.</span><span class="sxs-lookup"><span data-stu-id="987a3-694">A window will open when the report is finished compiling.</span></span> <span data-ttu-id="987a3-695">Здесь можно найти .ZIP имена файлов *имя_проекта* \_report.zip.</span><span class="sxs-lookup"><span data-stu-id="987a3-695">Here you will find a .ZIP file names *ProjectName*\_report.zip.</span></span> <span data-ttu-id="987a3-696">Этот файл содержит все журналы и результаты, собранные во время тестового прохода.</span><span class="sxs-lookup"><span data-stu-id="987a3-696">This file contains all of the logs and results collected during the test pass.</span></span>

### <a name="writing-a-bug"></a><span data-ttu-id="987a3-697">Запись ошибки</span><span class="sxs-lookup"><span data-stu-id="987a3-697">Writing a Bug</span></span>

<span data-ttu-id="987a3-698">Существует два способа написания отчета об ошибке: можно пройти по тестовым случаям и нажать кнопку **завершить** , если заголовок не прошел тестовый случай, либо щелкнуть вкладку **изменение ошибки** и вручную добавить отчет об ошибке.</span><span class="sxs-lookup"><span data-stu-id="987a3-698">There are two ways to write a bug report: you can go through the test cases and click **Fail** when the title fails a test case, or you can click the **Bug Edit** tab and manually add a bug report.</span></span>

### <a name="clicking-fail-on-a-test-case"></a><span data-ttu-id="987a3-699">Нажатие кнопки "сбой" в тестовом случае</span><span class="sxs-lookup"><span data-stu-id="987a3-699">Clicking Fail on a test case</span></span>

1.  <span data-ttu-id="987a3-700">При нажатии кнопки **сбой** в тестовом случае в раскрывающемся списке **тип проблемы** будет автоматически задан тип тестового случая.</span><span class="sxs-lookup"><span data-stu-id="987a3-700">When you click **Fail** on a test case, the **Issue Type** drop-down list will automatically be set to the test case type.</span></span>
2.  <span data-ttu-id="987a3-701">Добавьте краткое описание в поле **Title (название** ), которое кратко описывает эту ошибку.</span><span class="sxs-lookup"><span data-stu-id="987a3-701">Add a short description to the **Title** field that briefly describes the issue.</span></span>
3.  <span data-ttu-id="987a3-702">Добавьте подробное описание проблемы в поле **наблюдаемое поведение** .</span><span class="sxs-lookup"><span data-stu-id="987a3-702">Add a detailed description of the issue to the **Observed Behavior** field.</span></span>
4.  <span data-ttu-id="987a3-703">При необходимости добавьте ожидаемое значение в поле **ожидаемое поведение** (в отличие от описания проблемы).</span><span class="sxs-lookup"><span data-stu-id="987a3-703">As appropriate, add what was expected (as opposed to a description of the issue) to the **Expected Behavior** field.</span></span>
5.  <span data-ttu-id="987a3-704">Добавьте подробное описание того, как воспроизвести ошибку в поле **шаги** воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="987a3-704">Add a detailed description of how to reproduce the issue to the **Repro-Steps** field.</span></span>
6.  <span data-ttu-id="987a3-705">По завершении нажмите кнопку **сохранить** .</span><span class="sxs-lookup"><span data-stu-id="987a3-705">When done, click the **Save** button.</span></span>

### <a name="manually-adding-a-bug"></a><span data-ttu-id="987a3-706">Добавление ошибки вручную</span><span class="sxs-lookup"><span data-stu-id="987a3-706">Manually Adding a Bug</span></span>

<span data-ttu-id="987a3-707">Этот процесс аналогичен нажатию кнопки **завершить**, за исключением автоматического заполнения раскрывающегося списка.</span><span class="sxs-lookup"><span data-stu-id="987a3-707">This process is the same as clicking **Fail**, with the exception of the auto-populated drop-down list.</span></span> <span data-ttu-id="987a3-708">В этом случае выберите подходящий тип сбоя ТКР или выберите **\* \* проблему \* \* , не** относящуюся к TR, для ошибок, которые выходят за пределы диапазона TR, но по-прежнему должны быть зарегистрированы.</span><span class="sxs-lookup"><span data-stu-id="987a3-708">In this case, either select the appropriate TCR failure type or select **\*\* Non-TR Issue \*\*** for bugs that fall outside of the TR range but should still be reported.</span></span>

## <a name="resources"></a><span data-ttu-id="987a3-709">Ресурсы</span><span class="sxs-lookup"><span data-stu-id="987a3-709">Resources</span></span>

<dl> <dt>

<span data-ttu-id="987a3-710"><span id="Games_for_Windows__Technical_Requirements"></span><span id="games_for_windows__technical_requirements"></span><span id="GAMES_FOR_WINDOWS__TECHNICAL_REQUIREMENTS"></span>Игры для Windows: технические требования</span><span class="sxs-lookup"><span data-stu-id="987a3-710"><span id="Games_for_Windows__Technical_Requirements"></span><span id="games_for_windows__technical_requirements"></span><span id="GAMES_FOR_WINDOWS__TECHNICAL_REQUIREMENTS"></span>Games for Windows: Technical Requirements</span></span>
</dt> <dd>

[<span data-ttu-id="987a3-711">Игры для технических требований Windows: рекомендации по работе с играми в Windows XP, Windows Vista и Windows 7</span><span class="sxs-lookup"><span data-stu-id="987a3-711">Games for Windows Technical Requirements: Best Practices for Games on Windows XP, Windows Vista, and Windows 7</span></span>](./games-for-windows-technical-requirements-1-1-0006.md)

</dd> <dt>

<span data-ttu-id="987a3-712"><span id="Windows_SDK"></span><span id="windows_sdk"></span><span id="WINDOWS_SDK"></span>Windows SDK</span><span class="sxs-lookup"><span data-stu-id="987a3-712"><span id="Windows_SDK"></span><span id="windows_sdk"></span><span id="WINDOWS_SDK"></span>Windows SDK</span></span>
</dt> <dd>

[<span data-ttu-id="987a3-713">Пакеты SDK для Windows</span><span class="sxs-lookup"><span data-stu-id="987a3-713">Windows SDKs</span></span>](https://msdn.microsoft.com/bb980924.aspx)

</dd> <dt>

<span data-ttu-id="987a3-714"><span id="User_Account_Control_Guidelines"></span><span id="user_account_control_guidelines"></span><span id="USER_ACCOUNT_CONTROL_GUIDELINES"></span>Рекомендации по контролю учетных записей пользователей</span><span class="sxs-lookup"><span data-stu-id="987a3-714"><span id="User_Account_Control_Guidelines"></span><span id="user_account_control_guidelines"></span><span id="USER_ACCOUNT_CONTROL_GUIDELINES"></span>User Account Control Guidelines</span></span>
</dt> <dd>

<span data-ttu-id="987a3-715">[Требования к разработке приложений Windows Vista для обеспечения совместимости управления учетными записями пользователей](/previous-versions/dotnet/articles/bb530410(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="987a3-715">[Windows Vista Application Development Requirements for User Account Control Compatibility](/previous-versions/dotnet/articles/bb530410(v=msdn.10))</span></span>

</dd> <dt>

<span data-ttu-id="987a3-716"><span id="Windows_Installer_Information"></span><span id="windows_installer_information"></span><span id="WINDOWS_INSTALLER_INFORMATION"></span>Сведения о установщик Windows</span><span class="sxs-lookup"><span data-stu-id="987a3-716"><span id="Windows_Installer_Information"></span><span id="windows_installer_information"></span><span id="WINDOWS_INSTALLER_INFORMATION"></span>Windows Installer Information</span></span>
</dt> <dd>

[<span data-ttu-id="987a3-717">Установщик Windows</span><span class="sxs-lookup"><span data-stu-id="987a3-717">Windows Installer</span></span>](../msi/windows-installer-portal.md)

</dd> <dt>

<span data-ttu-id="987a3-718"><span id="WinQual_Developer_Portal__"></span><span id="winqual_developer_portal__"></span><span id="WINQUAL_DEVELOPER_PORTAL__"></span>Портал разработчика Винкуал</span><span class="sxs-lookup"><span data-stu-id="987a3-718"><span id="WinQual_Developer_Portal__"></span><span id="winqual_developer_portal__"></span><span id="WINQUAL_DEVELOPER_PORTAL__"></span>WinQual Developer Portal</span></span> 
</dt> <dd>

[<span data-ttu-id="987a3-719">Веб-службы Windows Quality Services (Винкуал)</span><span class="sxs-lookup"><span data-stu-id="987a3-719">Windows Quality Online Services (Winqual)</span></span>](/windows-hardware/drivers/dashboard/winqual-submission-tool--winqualexe-)

</dd> <dt>

<span data-ttu-id="987a3-720"><span id="DirectX_Developer_Portal"></span><span id="directx_developer_portal"></span><span id="DIRECTX_DEVELOPER_PORTAL"></span>Портал разработчика DirectX</span><span class="sxs-lookup"><span data-stu-id="987a3-720"><span id="DirectX_Developer_Portal"></span><span id="directx_developer_portal"></span><span id="DIRECTX_DEVELOPER_PORTAL"></span>DirectX Developer Portal</span></span>
</dt> <dd>

<span data-ttu-id="987a3-721">[Центр разработчиков DirectX](/previous-versions/windows/apps/hh452744(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="987a3-721">[DirectX Developer Center](/previous-versions/windows/apps/hh452744(v=win.10))</span></span>

</dd> <dt>

<span data-ttu-id="987a3-722"><span id="Games_for_Windows_and_DirectX_SDK_Blog"></span><span id="games_for_windows_and_directx_sdk_blog"></span><span id="GAMES_FOR_WINDOWS_AND_DIRECTX_SDK_BLOG"></span>Блог о играх для Windows и DirectX SDK</span><span class="sxs-lookup"><span data-stu-id="987a3-722"><span id="Games_for_Windows_and_DirectX_SDK_Blog"></span><span id="games_for_windows_and_directx_sdk_blog"></span><span id="GAMES_FOR_WINDOWS_AND_DIRECTX_SDK_BLOG"></span>Games for Windows and DirectX SDK Blog</span></span>
</dt> <dd>

[<span data-ttu-id="987a3-723">Записи блога, посвященные играм для Windows и DirectX SDK</span><span class="sxs-lookup"><span data-stu-id="987a3-723">Games for Windows and the DirectX SDK</span></span>](https://walbourn.github.io/)

</dd> <dt>

<span data-ttu-id="987a3-724"><span id="Additional_DirectX_Articles"></span><span id="additional_directx_articles"></span><span id="ADDITIONAL_DIRECTX_ARTICLES"></span>Дополнительные статьи по DirectX</span><span class="sxs-lookup"><span data-stu-id="987a3-724"><span id="Additional_DirectX_Articles"></span><span id="additional_directx_articles"></span><span id="ADDITIONAL_DIRECTX_ARTICLES"></span>Additional DirectX Articles</span></span>
</dt> <dd>

[<span data-ttu-id="987a3-725">Технические статьи по DirectX</span><span class="sxs-lookup"><span data-stu-id="987a3-725">DirectX Technical Articles</span></span>](./dx9-technical-articles.md)

</dd> </dl>

 

