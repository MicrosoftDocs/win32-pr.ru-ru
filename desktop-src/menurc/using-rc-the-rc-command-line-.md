---
title: Использование компилятора ресурсов (командная строка RC)
description: Чтобы запустить RC, используйте следующую команду.
ms.assetid: da087e15-ecb5-4d03-b534-be872cf7d8b6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c34e24fdf7b9b648a9baf9c6db8981f05d5434ef
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103987437"
---
# <a name="using-rc-the-rc-command-line"></a><span data-ttu-id="c8732-103">Использование компилятора ресурсов (командная строка RC)</span><span class="sxs-lookup"><span data-stu-id="c8732-103">Using RC (The RC Command Line)</span></span>

<span data-ttu-id="c8732-104">Чтобы запустить RC, используйте следующую команду.</span><span class="sxs-lookup"><span data-stu-id="c8732-104">To start RC, use the following command.</span></span>

<span data-ttu-id="c8732-105">**Версия-кандидат** \[ *Параметры* \] *файл скрипта*</span><span class="sxs-lookup"><span data-stu-id="c8732-105">**RC** \[*options*\] *script-file*</span></span>

<span data-ttu-id="c8732-106">Параметр *script-File* задает имя файла определения ресурса, содержащего имена, типы, файлы имен и описания ресурсов для компиляции.</span><span class="sxs-lookup"><span data-stu-id="c8732-106">The *script-file* parameter specifies the name of the resource-definition file that contains the names, types, filenames, and descriptions of the resources to be compiled.</span></span>

<span data-ttu-id="c8732-107">Версия-кандидат может создавать отдельные файлы ресурсов для приложений, которые имеют как независимые от языка, так и зависящие от языка ресурсы.</span><span class="sxs-lookup"><span data-stu-id="c8732-107">RC can generate separate resource files for applications that have both language-neutral and language-specific resources.</span></span> <span data-ttu-id="c8732-108">Разработчики могут использовать [файл конфигурации ресурсов](/windows/desktop/Intl/preparing-resources) или задать параметры командной строки, чтобы выбрать, какие типы ресурсов и элементы являются нелокализованными ресурсами файла, не [зависящего от языка (LN)](/windows/desktop/Intl/mui-resource-management) , а какие — локализуемые ресурсы файлов MUI, зависящих от языка.</span><span class="sxs-lookup"><span data-stu-id="c8732-108">Developers can use a [resource configuration file](/windows/desktop/Intl/preparing-resources) or set command-line options to select which resource types and items are non-localizable resources of the [language-neutral (LN) file](/windows/desktop/Intl/mui-resource-management) and which are localizable resources of language-specific MUI files.</span></span> <span data-ttu-id="c8732-109">Дополнительные сведения см. в разделе [многоязычный пользовательский интерфейс](/windows/desktop/Intl/multilingual-user-interface).</span><span class="sxs-lookup"><span data-stu-id="c8732-109">For more information, see the [Multilingual User Interface](/windows/desktop/Intl/multilingual-user-interface).</span></span>

<span data-ttu-id="c8732-110">Параметр *Options* может быть одним или несколькими из следующих параметров командной строки.</span><span class="sxs-lookup"><span data-stu-id="c8732-110">The *options* parameter can be one or more of the following command-line options.</span></span>

## <a name="options"></a><span data-ttu-id="c8732-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="c8732-111">Options</span></span>

<dl> <dt>

<span data-ttu-id="c8732-112"><span id="__"></span>**/?**</span><span class="sxs-lookup"><span data-stu-id="c8732-112"><span id="__"></span>**/?**</span></span>
</dt> <dd>

<span data-ttu-id="c8732-113">Отображает список параметров командной строки.</span><span class="sxs-lookup"><span data-stu-id="c8732-113">Displays a list of command-line options.</span></span>

</dd> <dt>

<span data-ttu-id="c8732-114"><span id="_c"></span><span id="_C"></span>**ключей**</span><span class="sxs-lookup"><span data-stu-id="c8732-114"><span id="_c"></span><span id="_C"></span>**/c**</span></span>
</dt> <dd>

<span data-ttu-id="c8732-115">Определяет кодовую страницу, используемую при преобразовании NLS.</span><span class="sxs-lookup"><span data-stu-id="c8732-115">Defines a code page used by NLS conversion.</span></span>

</dd> <dt>

<span data-ttu-id="c8732-116"><span id="_d"></span><span id="_D"></span>**/d**</span><span class="sxs-lookup"><span data-stu-id="c8732-116"><span id="_d"></span><span id="_D"></span>**/d**</span></span>
</dt> <dd>

<span data-ttu-id="c8732-117">Определяет символ для препроцессора, который можно протестировать с помощью директивы [**\# ifdef**](-ifdef.md) .</span><span class="sxs-lookup"><span data-stu-id="c8732-117">Defines a symbol for the preprocessor that you can test with the [**\#ifdef**](-ifdef.md) directive.</span></span>

</dd> <dt>

<span data-ttu-id="c8732-118"><span id="_fm_mresname"></span><span id="_FM_MRESNAME"></span>**/FM** *мреснаме*</span><span class="sxs-lookup"><span data-stu-id="c8732-118"><span id="_fm_mresname"></span><span id="_FM_MRESNAME"></span>**/fm** *mresname*</span></span>
</dt> <dd>

<span data-ttu-id="c8732-119">Версия-кандидат создает один язык, не зависящий от языка. RES-файл и один зависящий от языка язык (MUI). RES-файл с использованием *файла сценария*.</span><span class="sxs-lookup"><span data-stu-id="c8732-119">RC creates one language-neutral .RES file and one language-dependent (MUI) .RES file using *script-file*.</span></span> <span data-ttu-id="c8732-120">Этот параметр следует использовать вместе с параметром **/FO** *реснаме* .</span><span class="sxs-lookup"><span data-stu-id="c8732-120">This option must be used together with the **/fo** *resname* option.</span></span> <span data-ttu-id="c8732-121">Версия-кандидат — это имя, не зависящее от языка. RES-файл *реснаме. Res* и имена, зависящие от языка (MUI). RES файл *мреснаме. Res*.</span><span class="sxs-lookup"><span data-stu-id="c8732-121">RC names the language-neutral .RES file *resname.res* and names the language-dependent (MUI) .RES file *mresname.res*.</span></span>

<span data-ttu-id="c8732-122">**Windows Server 2003 и Windows XP/2000:** Этот параметр недоступен без использования функций [**лоадмуилибрари**](/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya) и [**фримуилибрари**](/windows/desktop/api/muiload/nf-muiload-freemuilibrary) в обновленной системе.</span><span class="sxs-lookup"><span data-stu-id="c8732-122">**Windows Server 2003 and Windows XP/2000:** This option is not available without also using the [**LoadMUILibrary**](/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya) and [**FreeMUILibrary**](/windows/desktop/api/muiload/nf-muiload-freemuilibrary) functions on an updated system.</span></span>

</dd> <dt>

<span data-ttu-id="c8732-123"><span id="_fo_resname"></span><span id="_FO_RESNAME"></span>**/FO** *реснаме*</span><span class="sxs-lookup"><span data-stu-id="c8732-123"><span id="_fo_resname"></span><span id="_FO_RESNAME"></span>**/fo** *resname*</span></span>
</dt> <dd>

<span data-ttu-id="c8732-124">Версия-кандидат создает. RES-файл с именем *реснаме* , использующий *файл сценария*.</span><span class="sxs-lookup"><span data-stu-id="c8732-124">RC creates a .RES file named *resname* using *script-file*.</span></span>

<span data-ttu-id="c8732-125">Если также задан параметр **/FM** *мреснаме* , версия-кандидат создает язык, не зависящий от языка. RES-файл и один зависящий от языка язык (MUI). RES — файл.</span><span class="sxs-lookup"><span data-stu-id="c8732-125">If the **/fm** *mresname* option is also set, RC creates one language-neutral .RES file and one language-dependent (MUI) .RES file.</span></span>

<span data-ttu-id="c8732-126">**Windows Server 2003 и Windows XP/2000:** Этот параметр недоступен без использования функций [**лоадмуилибрари**](/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya) и [**фримуилибрари**](/windows/desktop/api/muiload/nf-muiload-freemuilibrary) в обновленной системе.</span><span class="sxs-lookup"><span data-stu-id="c8732-126">**Windows Server 2003 and Windows XP/2000:** This option is not available without also using the [**LoadMUILibrary**](/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya) and [**FreeMUILibrary**](/windows/desktop/api/muiload/nf-muiload-freemuilibrary) functions on an updated system.</span></span>

</dd> <dt>

<span data-ttu-id="c8732-127"><span id="_g1"></span><span id="_G1"></span>**/G1**</span><span class="sxs-lookup"><span data-stu-id="c8732-127"><span id="_g1"></span><span id="_G1"></span>**/g1**</span></span>
</dt> <dd>

<span data-ttu-id="c8732-128">Если задано значение/G1, RC создает файл MUI, если единственный локализуемый ресурс, включаемый в файл MUI, является ресурсом версии.</span><span class="sxs-lookup"><span data-stu-id="c8732-128">If /g1, is set, RC generates a MUI file if the only localizable resource being included in the MUI file is a version resource.</span></span> <span data-ttu-id="c8732-129">Если параметр/G1 не задан, версия-кандидат не будет создавать файл MUI, если единственный локализуемый ресурс, включаемый в файл MUI, — это ресурс версии.</span><span class="sxs-lookup"><span data-stu-id="c8732-129">If /g1 is not set, RC will not generate a MUI file if the only localizable resource being included in the MUI file is a version resource.</span></span>

</dd> <dt>

<span data-ttu-id="c8732-130"><span id="_h"></span><span id="_H"></span>**/h**</span><span class="sxs-lookup"><span data-stu-id="c8732-130"><span id="_h"></span><span id="_H"></span>**/h**</span></span>
</dt> <dd>

<span data-ttu-id="c8732-131">Отображает список параметров командной строки.</span><span class="sxs-lookup"><span data-stu-id="c8732-131">Displays the list of command-line options.</span></span>

</dd> <dt>

<span data-ttu-id="c8732-132"><span id="_I"></span><span id="_i"></span>**/I**</span><span class="sxs-lookup"><span data-stu-id="c8732-132"><span id="_I"></span><span id="_i"></span>**/I**</span></span>
</dt> <dd>

<span data-ttu-id="c8732-133">Выполняет поиск в указанном каталоге перед поиском в каталогах, заданных переменной среды INCLUDE.</span><span class="sxs-lookup"><span data-stu-id="c8732-133">Searches the specified directory before searching the directories specified by the INCLUDE environment variable.</span></span>

</dd> <dt>

<span data-ttu-id="c8732-134"><span id="_j__loctype"></span><span id="_J__LOCTYPE"></span>**/j** *локтипе*</span><span class="sxs-lookup"><span data-stu-id="c8732-134"><span id="_j__loctype"></span><span id="_J__LOCTYPE"></span>**/j** *loctype*</span></span>
</dt> <dd>

<span data-ttu-id="c8732-135">Локализуемые типы ресурсов версия-кандидат помещает в языковой интерфейс, зависящий от языка (MUI). RES — файл.</span><span class="sxs-lookup"><span data-stu-id="c8732-135">Localizable resource types RC places into the language-dependent (MUI) .RES file.</span></span> <span data-ttu-id="c8732-136">Если также задан параметр **/q** , этот параметр не учитывается, и информация в файле конфигурации RC имеет приоритет.</span><span class="sxs-lookup"><span data-stu-id="c8732-136">If the **/q** option is also set, this option is ignored, and the information in the RC Configuration file takes precedence.</span></span>

<span data-ttu-id="c8732-137">**Windows Server 2003 и Windows XP/2000:** Этот параметр недоступен без использования функций [**лоадмуилибрари**](/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya) и [**фримуилибрари**](/windows/desktop/api/muiload/nf-muiload-freemuilibrary) в обновленной системе.</span><span class="sxs-lookup"><span data-stu-id="c8732-137">**Windows Server 2003 and Windows XP/2000:** This option is not available without also using the [**LoadMUILibrary**](/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya) and [**FreeMUILibrary**](/windows/desktop/api/muiload/nf-muiload-freemuilibrary) functions on an updated system.</span></span>

</dd> <dt>

<span data-ttu-id="c8732-138"><span id="_k_overtype"></span><span id="_K_OVERTYPE"></span>перетип **/k** </span><span class="sxs-lookup"><span data-stu-id="c8732-138"><span id="_k_overtype"></span><span id="_K_OVERTYPE"></span>**/k** *overtype*</span></span>
</dt> <dd>

<span data-ttu-id="c8732-139">Перекрывающиеся типы ресурсов, которые версия-кандидат помещает в как нейтральный к языку. RES и зависящие от языка (MUI). RES файлы.</span><span class="sxs-lookup"><span data-stu-id="c8732-139">Overlapping resource types that RC places into both the language-neutral .RES and the language-dependent (MUI).RES files.</span></span> <span data-ttu-id="c8732-140">Типы ресурсов, заданные параметром **/k** , должны быть подмножеством параметров, заданных параметром **/j** .</span><span class="sxs-lookup"><span data-stu-id="c8732-140">The resource types that are specified by the **/k** option must be a subset of those that are specified by the **/j** option.</span></span> <span data-ttu-id="c8732-141">Например? J2? J3? K3 указывает, что версия-кандидат ресурса размещает тип 3 в файлах, не зависящих от языка, и от языка (MUI).</span><span class="sxs-lookup"><span data-stu-id="c8732-141">For example, ?J2 ?J3 ?K3 specifies that RC places resource type 3 in both the language-neutral and language-dependent (MUI) files.</span></span> <span data-ttu-id="c8732-142">Если также задан параметр **/q** , этот параметр не учитывается, и информация в файле конфигурации RC имеет приоритет.</span><span class="sxs-lookup"><span data-stu-id="c8732-142">If the **/q** option is also set, this option is ignored, and the information in the RC Configuration file takes precedence.</span></span>

<span data-ttu-id="c8732-143">**Windows Server 2003 и Windows XP/2000:** Этот параметр недоступен без использования функций [**лоадмуилибрари**](/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya) и [**фримуилибрари**](/windows/desktop/api/muiload/nf-muiload-freemuilibrary) в обновленной системе.</span><span class="sxs-lookup"><span data-stu-id="c8732-143">**Windows Server 2003 and Windows XP/2000:** This option is not available without also using the [**LoadMUILibrary**](/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya) and [**FreeMUILibrary**](/windows/desktop/api/muiload/nf-muiload-freemuilibrary) functions on an updated system.</span></span>

</dd> <dt>

<span data-ttu-id="c8732-144"><span id="_l_langid"></span><span id="_L_LANGID"></span>**/l** *LangID*</span><span class="sxs-lookup"><span data-stu-id="c8732-144"><span id="_l_langid"></span><span id="_L_LANGID"></span>**/l** *langid*</span></span>
</dt> <dd>

<span data-ttu-id="c8732-145">Указывает язык по умолчанию для компиляции.</span><span class="sxs-lookup"><span data-stu-id="c8732-145">Specifies the default language for compilation.</span></span> <span data-ttu-id="c8732-146">Например, параметр-l409 эквивалентен включению следующей инструкции в начало файла скрипта ресурсов: `LANGUAGE LANG_ENGLISH,SUBLANG_ENGLISH_US`</span><span class="sxs-lookup"><span data-stu-id="c8732-146">For example, -l409 is equivalent to including the following statement at the top of the resource script file: `LANGUAGE LANG_ENGLISH,SUBLANG_ENGLISH_US`</span></span>

<span data-ttu-id="c8732-147">Дополнительные сведения см. в разделе [идентификаторы языков](/windows/desktop/Intl/language-identifiers).</span><span class="sxs-lookup"><span data-stu-id="c8732-147">For more information, see [Language Identifiers](/windows/desktop/Intl/language-identifiers).</span></span>

</dd> <dt>

<span data-ttu-id="c8732-148"><span id="_n"></span><span id="_N"></span>**параметра**</span><span class="sxs-lookup"><span data-stu-id="c8732-148"><span id="_n"></span><span id="_N"></span>**/n**</span></span>
</dt> <dd>

<span data-ttu-id="c8732-149">NULL завершает все строки в таблице строк.</span><span class="sxs-lookup"><span data-stu-id="c8732-149">Null terminates all strings in the string table.</span></span>

</dd> <dt>

<span data-ttu-id="c8732-150"><span id="_q_Mui.RCConfig"></span><span id="_q_mui.rcconfig"></span><span id="_Q_MUI.RCCONFIG"></span>**/Q** *MUI. ркконфиг*</span><span class="sxs-lookup"><span data-stu-id="c8732-150"><span id="_q_Mui.RCConfig"></span><span id="_q_mui.rcconfig"></span><span id="_Q_MUI.RCCONFIG"></span>**/q** *Mui.RCConfig*</span></span>
</dt> <dd>

<span data-ttu-id="c8732-151">RC-файл конфигурации, следующий за форматом файла конфигурации версии-КАНДИДАТа.</span><span class="sxs-lookup"><span data-stu-id="c8732-151">An RC configuration file that follows the RC Configuration File format.</span></span> <span data-ttu-id="c8732-152">Формат файла конфигурации RC позволяет компонентам самостоятельно описывать сведения о ресурсах, такие как управление версиями ресурсов, путь к файлам MUI, типы ресурсов и элементы.</span><span class="sxs-lookup"><span data-stu-id="c8732-152">The RC Configuration File format enables components to self-describe resource information such as resource versioning, MUI file path, resource types and items.</span></span> <span data-ttu-id="c8732-153">Этот файл указывает, какие ресурсы переходят в нейтральный язык. RES-файл и ресурсы, которые переходят в зависимости от языка (MUI). RES — файл.</span><span class="sxs-lookup"><span data-stu-id="c8732-153">This file specifies which resources go into the language-neutral .RES file and which resources go into the language-dependent (MUI) .RES file.</span></span> <span data-ttu-id="c8732-154">Этот параметр и сведения, указанные в файле конфигурации RC, переопределяют параметры командной строки **/j** и **/k**.</span><span class="sxs-lookup"><span data-stu-id="c8732-154">This option, and the information provided in the RC Configuration file, override the command line options **/j** and **/k**.</span></span>

<span data-ttu-id="c8732-155">**Windows Server 2003 и Windows XP/2000:** Этот параметр недоступен без использования функций [**лоадмуилибрари**](/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya) и [**фримуилибрари**](/windows/desktop/api/muiload/nf-muiload-freemuilibrary) в обновленной системе.</span><span class="sxs-lookup"><span data-stu-id="c8732-155">**Windows Server 2003 and Windows XP/2000:** This option is not available without also using the [**LoadMUILibrary**](/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya) and [**FreeMUILibrary**](/windows/desktop/api/muiload/nf-muiload-freemuilibrary) functions on an updated system.</span></span>

</dd> <dt>

<span data-ttu-id="c8732-156"><span id="_r"></span><span id="_R"></span>**/r**</span><span class="sxs-lookup"><span data-stu-id="c8732-156"><span id="_r"></span><span id="_R"></span>**/r**</span></span>
</dt> <dd>

<span data-ttu-id="c8732-157">Не обрабатывается.</span><span class="sxs-lookup"><span data-stu-id="c8732-157">Ignored.</span></span> <span data-ttu-id="c8732-158">Предоставляется для совместимости с существующими Makefile.</span><span class="sxs-lookup"><span data-stu-id="c8732-158">Provided for compatibility with existing makefiles.</span></span>

</dd> <dt>

<span data-ttu-id="c8732-159"><span id="_u"></span><span id="_U"></span>**/u**</span><span class="sxs-lookup"><span data-stu-id="c8732-159"><span id="_u"></span><span id="_U"></span>**/u**</span></span>
</dt> <dd>

<span data-ttu-id="c8732-160">Отменяет определение символа для препроцессора.</span><span class="sxs-lookup"><span data-stu-id="c8732-160">Undefines a symbol for the preprocessor.</span></span>

</dd> <dt>

<span data-ttu-id="c8732-161"><span id="_v"></span><span id="_V"></span>**/v**</span><span class="sxs-lookup"><span data-stu-id="c8732-161"><span id="_v"></span><span id="_V"></span>**/v**</span></span>
</dt> <dd>

<span data-ttu-id="c8732-162">Отображает сообщения, которые сообщают о ходе выполнения компилятора.</span><span class="sxs-lookup"><span data-stu-id="c8732-162">Displays messages that report on the progress of the compiler.</span></span>

</dd> <dt>

<span data-ttu-id="c8732-163"><span id="_x"></span><span id="_X"></span>**/x**</span><span class="sxs-lookup"><span data-stu-id="c8732-163"><span id="_x"></span><span id="_X"></span>**/x**</span></span>
</dt> <dd>

<span data-ttu-id="c8732-164">Предотвращает проверку версии-КАНДИДАТа переменной среды INCLUDE при поиске файлов заголовков или файлов ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c8732-164">Prevents RC from checking the INCLUDE environment variable when searching for header files or resource files.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c8732-165">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c8732-165">Remarks</span></span>

<span data-ttu-id="c8732-166">В параметрах регистр не учитывается, а вместо косой черты (/) можно использовать дефис (-).</span><span class="sxs-lookup"><span data-stu-id="c8732-166">Options are not case sensitive, and a hyphen (-) can be used in place of a slash mark (/).</span></span> <span data-ttu-id="c8732-167">Можно объединить однобуквенные параметры, если они не нуждаются в дополнительных параметрах.</span><span class="sxs-lookup"><span data-stu-id="c8732-167">You can combine single-letter options if they do not require any additional parameters.</span></span>

<span data-ttu-id="c8732-168">Версия-кандидат не будет создавать файл MUI в следующих случаях.</span><span class="sxs-lookup"><span data-stu-id="c8732-168">RC will not generate a MUI file in the following cases.</span></span>

-   <span data-ttu-id="c8732-169">В RC-файле не существует локализуемых ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c8732-169">No localizable resources exist in the .rc file.</span></span>
-   <span data-ttu-id="c8732-170">Единственный идентификатор языка ресурса, указанный в RC-файле, является нейтральным (0x0).</span><span class="sxs-lookup"><span data-stu-id="c8732-170">The only resource language id specified in the .rc file is neutral (0x0).</span></span>
-   <span data-ttu-id="c8732-171">RC-файл содержит ресурсы, указанные на нескольких языках.</span><span class="sxs-lookup"><span data-stu-id="c8732-171">The .rc file has resources that are specified in more than one language.</span></span> <span data-ttu-id="c8732-172">Исключением является то, что RC-файл содержит два языка, а один язык является нейтральным (0x0), RC создает файл MUI.</span><span class="sxs-lookup"><span data-stu-id="c8732-172">The exception is if the .rc file contains two languages, and one language is neutral (0x0), RC generates a MUI file.</span></span>

<span data-ttu-id="c8732-173">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="c8732-173">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="c8732-174">Определение имен для препроцессора</span><span class="sxs-lookup"><span data-stu-id="c8732-174">Defining Names for the Preprocessor</span></span>](defining-names-for-the-preprocessor.md)
-   [<span data-ttu-id="c8732-175">Переименование скомпилированного файла ресурсов</span><span class="sxs-lookup"><span data-stu-id="c8732-175">Renaming the Compiled Resource File</span></span>](renaming-the-compiled-resource-file.md)
-   [<span data-ttu-id="c8732-176">Поиск файлов</span><span class="sxs-lookup"><span data-stu-id="c8732-176">Searching for Files</span></span>](searching-for-files.md)
-   [<span data-ttu-id="c8732-177">Отображение сообщений о ходе выполнения</span><span class="sxs-lookup"><span data-stu-id="c8732-177">Displaying Progress Messages</span></span>](displaying-progress-messages.md)
-   [<span data-ttu-id="c8732-178">Диагностические сообщения RC</span><span class="sxs-lookup"><span data-stu-id="c8732-178">RC Diagnostic Messages</span></span>](rc-diagnostic-messages.md)

## <a name="related-topics"></a><span data-ttu-id="c8732-179">См. также</span><span class="sxs-lookup"><span data-stu-id="c8732-179">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c8732-180">Многоязыковой интерфейс пользователя</span><span class="sxs-lookup"><span data-stu-id="c8732-180">Multilingual User Interface</span></span>](/windows/desktop/Intl/multilingual-user-interface)
</dt> </dl>

 

 