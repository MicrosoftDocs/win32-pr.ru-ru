---
description: В этом разделе описывается создание новых типов файлов и связывание приложения с типом файлов и другими хорошо определенными типами файлов.
ms.assetid: 055648cd-46ce-4e61-80b2-bcf1d1823e20
title: Типы файлов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d697c42626c6e1ab3e0b5cc0b88bd065523d53a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985532"
---
# <a name="file-types"></a><span data-ttu-id="1cd56-103">Типы файлов</span><span class="sxs-lookup"><span data-stu-id="1cd56-103">File Types</span></span>

<span data-ttu-id="1cd56-104">В этом разделе описывается создание новых типов файлов и связывание приложения с типом файлов и другими хорошо определенными типами файлов.</span><span class="sxs-lookup"><span data-stu-id="1cd56-104">This topic explains how to create new file types and how to associate your app with your file type and other well-defined file types.</span></span> <span data-ttu-id="1cd56-105">Файлы с общим расширением общего имени файла (doc, HTML и т. д.) имеют один и тот же *тип*.</span><span class="sxs-lookup"><span data-stu-id="1cd56-105">Files with a shared common file name extension (.doc, .html, and so on) are of the same *type*.</span></span> <span data-ttu-id="1cd56-106">Например, при создании нового текстового редактора можно использовать существующий txt-файл.</span><span class="sxs-lookup"><span data-stu-id="1cd56-106">For example, if you create a new text editor, then you can use the existing .txt file type.</span></span> <span data-ttu-id="1cd56-107">В других случаях может потребоваться создать новый тип файлов.</span><span class="sxs-lookup"><span data-stu-id="1cd56-107">In other cases, you might need to create a new file type.</span></span>

<span data-ttu-id="1cd56-108">Этот раздел организован следующим образом:</span><span class="sxs-lookup"><span data-stu-id="1cd56-108">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="1cd56-109">Открытые и закрытые типы файлов</span><span class="sxs-lookup"><span data-stu-id="1cd56-109">Public and Private File Types</span></span>](#public-and-private-file-types)
-   [<span data-ttu-id="1cd56-110">Регистрация типа файла</span><span class="sxs-lookup"><span data-stu-id="1cd56-110">Registering a File Type</span></span>](#registering-a-file-type)
    -   [<span data-ttu-id="1cd56-111">Задание дополнительных подразделов и атрибутов расширения типа файла</span><span class="sxs-lookup"><span data-stu-id="1cd56-111">Setting Optional Subkeys and File Type Extension Attributes</span></span>](#setting-optional-subkeys-and-file-type-extension-attributes)
    -   [<span data-ttu-id="1cd56-112">Удаление данных реестра во время удаления</span><span class="sxs-lookup"><span data-stu-id="1cd56-112">Deleting Registry Information During Uninstallation</span></span>](#deleting-registry-information-during-uninstallation)
-   [<span data-ttu-id="1cd56-113">Типы файлов, поддерживающие открытые метаданные</span><span class="sxs-lookup"><span data-stu-id="1cd56-113">File Types That Support Open Metadata</span></span>](#file-types-that-support-open-metadata)
-   [<span data-ttu-id="1cd56-114">См. также</span><span class="sxs-lookup"><span data-stu-id="1cd56-114">Related topics</span></span>](#related-topics)

<span data-ttu-id="1cd56-115">Дополнительные сведения можно найти в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="1cd56-115">Additional information can be found on the following topics:</span></span>

-   [<span data-ttu-id="1cd56-116">Выбор расширения типа файлов</span><span class="sxs-lookup"><span data-stu-id="1cd56-116">How To Choose a File Type Extension</span></span>](how-to-choose-a-file-type-extension.md)
-   [<span data-ttu-id="1cd56-117">Определение атрибутов типа файла</span><span class="sxs-lookup"><span data-stu-id="1cd56-117">How To Define File Type Attributes</span></span>](./how-to-define-file-type-attributes.md)
-   [<span data-ttu-id="1cd56-118">Включение приложения в диалоговое окно «Открыть с помощью»</span><span class="sxs-lookup"><span data-stu-id="1cd56-118">How To Include an Application on the Open with Dialog Box</span></span>](how-to-include-an-application-on-the-open-with-dialog-box.md)
-   [<span data-ttu-id="1cd56-119">Исключение приложения из диалогового окна "Открыть с помощью" для несвязанных типов файлов</span><span class="sxs-lookup"><span data-stu-id="1cd56-119">How To Exclude an Application from the Open with Dialog Box for Unassociated File Types</span></span>](how-to-exclude-an-application-from-the-open-with-dialog-box-for-unassociated-file-types.md)

## <a name="public-and-private-file-types"></a><span data-ttu-id="1cd56-120">Открытые и закрытые типы файлов</span><span class="sxs-lookup"><span data-stu-id="1cd56-120">Public and Private File Types</span></span>

<span data-ttu-id="1cd56-121">Типы общедоступных файлов также называются популярными или спорными типами, так как конкурирующие приложения могут быть связаны с этими типами файлов.</span><span class="sxs-lookup"><span data-stu-id="1cd56-121">Public file types are also known as popular or contentious types because competing applications might want to be associated with these file types.</span></span> <span data-ttu-id="1cd56-122">К общим типам файлов относятся следующие характеристики.</span><span class="sxs-lookup"><span data-stu-id="1cd56-122">Characteristics of public file types include:</span></span>

-   <span data-ttu-id="1cd56-123">Обычно они определяются стандартами стандартов и/или передаются в соответствии с их определением организациями в форматах обмена.</span><span class="sxs-lookup"><span data-stu-id="1cd56-123">They are typically defined by standards bodies, and/or are promoted by their defining organizations as interchange formats.</span></span>
-   <span data-ttu-id="1cd56-124">Они часто обмениваются данными между компьютерами и пользователями в различных целях.</span><span class="sxs-lookup"><span data-stu-id="1cd56-124">They are often exchanged between computers and users for diverse purposes.</span></span>
-   <span data-ttu-id="1cd56-125">Они должны поддерживаться на многих разных платформах.</span><span class="sxs-lookup"><span data-stu-id="1cd56-125">They need to be supported on many different platforms.</span></span>
-   <span data-ttu-id="1cd56-126">Приложения от нескольких поставщиков, скорее всего, будут работать с ними.</span><span class="sxs-lookup"><span data-stu-id="1cd56-126">Applications from multiple vendors are likely to handle them.</span></span>

<span data-ttu-id="1cd56-127">Некоторые примеры типов файлов, которые считаются открытыми, — это файлы изображений. PNG,. gif,. jpg и. bmp, а также типы аудио. wav,. mp3 и. au.</span><span class="sxs-lookup"><span data-stu-id="1cd56-127">Some examples of file types that are considered public are the image file types .png, .gif, .jpg, and .bmp, and the audio types .wav, .mp3, and .au.</span></span>

<span data-ttu-id="1cd56-128">В отличие от общедоступных типов файлов, закрытые или частные типы файлов обычно имеют формат, который реализуется и понимается только одним приложением или поставщиком.</span><span class="sxs-lookup"><span data-stu-id="1cd56-128">Unlike public file types, private or proprietary file types typically have a format that is implemented and understood by only one application or vendor.</span></span> <span data-ttu-id="1cd56-129">В результате типы частных файлов обычно не подвержены конфликтам между приложениями.</span><span class="sxs-lookup"><span data-stu-id="1cd56-129">As a result, private file types are typically not prone to conflicts between applications.</span></span> <span data-ttu-id="1cd56-130">Некоторые типы файлов могут запускаться как закрытые типы файлов, но в дальнейшем они становятся общедоступными типами файлов.</span><span class="sxs-lookup"><span data-stu-id="1cd56-130">Some file types can start as private file types but later become public file types.</span></span>

> [!Note]  
> <span data-ttu-id="1cd56-131">Windows не различает общедоступные и закрытые типы файлов.</span><span class="sxs-lookup"><span data-stu-id="1cd56-131">Windows does not differentiate between public and private file types.</span></span> <span data-ttu-id="1cd56-132">Это различие уместно только в принятии решений о выборе типа файлов для регистрации.</span><span class="sxs-lookup"><span data-stu-id="1cd56-132">The distinction is relevant only in making decisions about your choice of file type registration.</span></span>

 

## <a name="registering-a-file-type"></a><span data-ttu-id="1cd56-133">Регистрация типа файла</span><span class="sxs-lookup"><span data-stu-id="1cd56-133">Registering a File Type</span></span>

<span data-ttu-id="1cd56-134">Чтобы связать тип файла с существующим приложением, укажите идентификатор ProgID приложения в реестре.</span><span class="sxs-lookup"><span data-stu-id="1cd56-134">To associate the file type with an existing application, locate the application ProgID in the registry.</span></span> <span data-ttu-id="1cd56-135">Чтобы связать тип файла с новым приложением, определите идентификатор ProgID для приложения.</span><span class="sxs-lookup"><span data-stu-id="1cd56-135">To associate the file type with a new application, define a ProgID for your application.</span></span> <span data-ttu-id="1cd56-136">Дополнительные сведения об определении нового идентификатора ProgID см. в разделе [программные идентификаторы](fa-progids.md).</span><span class="sxs-lookup"><span data-stu-id="1cd56-136">For information about defining a new ProgID, see [Programmatic Identifiers](fa-progids.md).</span></span>

<span data-ttu-id="1cd56-137">Подразделы расширения имени файла имеют следующую общую форму: *расширение* = *ProgID*.</span><span class="sxs-lookup"><span data-stu-id="1cd56-137">File name extension subkeys have the following general form: *extension*=*ProgID*.</span></span> <span data-ttu-id="1cd56-138">Подразделы расширения имени файла хранятся в **\_ \_ корневом поддереве классов hKey** .</span><span class="sxs-lookup"><span data-stu-id="1cd56-138">File name extension subkeys are stored in the **HKEY\_CLASSES\_ROOT** subtree.</span></span>

<span data-ttu-id="1cd56-139">При создании подразделов типа файла в реестре важно включить в нее точку (.).</span><span class="sxs-lookup"><span data-stu-id="1cd56-139">It is important to include the leading period (.) when creating file type subkeys in the registry.</span></span> <span data-ttu-id="1cd56-140">Например, если нужен тип файла с коротким расширением. МИП и длинное расширение. МИП-File, открываемое с помощью приложения MyProgram, используйте следующий синтаксис:</span><span class="sxs-lookup"><span data-stu-id="1cd56-140">For example, if you want a file type with the short extension .myp and the long extension .myp-file to be opened with an application called MyProgram, use the following syntax:</span></span>

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = ApplicationVendor.MyProgram
   .myp-file
      (Default) = ApplicationVendor.MyProgram
   ApplicationVendor.MyProgram
      (Default) = MyProgram Application
```

<span data-ttu-id="1cd56-141">Как показано в предыдущем примере, при регистрации короткого расширения имени файла (. МИП) следует также создать подраздел для длинного расширения (. МИП-File).</span><span class="sxs-lookup"><span data-stu-id="1cd56-141">As demonstrated in the preceding example, if you also register a short file name extension (.myp), you should create a subkey for the long extension (.myp-file) as well.</span></span> <span data-ttu-id="1cd56-142">Дополнительные сведения см. в разделе [обработчики типов файлов](fa-file-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="1cd56-142">For more information, see [File Type Handlers](fa-file-extensions.md).</span></span>

### <a name="setting-optional-subkeys-and-file-type-extension-attributes"></a><span data-ttu-id="1cd56-143">Задание дополнительных подразделов и атрибутов расширения типа файла</span><span class="sxs-lookup"><span data-stu-id="1cd56-143">Setting Optional Subkeys and File Type Extension Attributes</span></span>

<span data-ttu-id="1cd56-144">Записи расширения типа файлов в реестре содержат несколько необязательных подразделов и атрибутов.</span><span class="sxs-lookup"><span data-stu-id="1cd56-144">File type extension entries in the registry have several optional subkeys and attributes.</span></span>

<span data-ttu-id="1cd56-145">В следующей таблице описаны записи расширения типа файлов, используемые для сопоставления файлов.</span><span class="sxs-lookup"><span data-stu-id="1cd56-145">The file type extension entries that are used by file associations are described in the following table.</span></span> <span data-ttu-id="1cd56-146">Все значения имеют тип **reg \_ SZ** .</span><span class="sxs-lookup"><span data-stu-id="1cd56-146">All values are of the **REG\_SZ** type.</span></span>



| <span data-ttu-id="1cd56-147">Запись реестра</span><span class="sxs-lookup"><span data-stu-id="1cd56-147">Registry entry</span></span>  | <span data-ttu-id="1cd56-148">Действие</span><span class="sxs-lookup"><span data-stu-id="1cd56-148">Action</span></span>                                                                                                                                                                                                                                                                                                                             |
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1cd56-149">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="1cd56-149">Default</span></span>         | <span data-ttu-id="1cd56-150">В качестве значения по умолчанию для подраздела расширения укажите идентификатор ProgID, с которым он связан.</span><span class="sxs-lookup"><span data-stu-id="1cd56-150">Set the default value of the extension subkey to the ProgID to which it is linked.</span></span>                                                                                                                                                                                                                                                 |
| <span data-ttu-id="1cd56-151">Тип содержимого</span><span class="sxs-lookup"><span data-stu-id="1cd56-151">Content Type</span></span>    | <span data-ttu-id="1cd56-152">Установите значение типа содержимого в тип содержимого MIME типа файла.</span><span class="sxs-lookup"><span data-stu-id="1cd56-152">Set the Content Type value to the file type's MIME content type.</span></span>                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="1cd56-153">OpenWithList</span><span class="sxs-lookup"><span data-stu-id="1cd56-153">OpenWithList</span></span>    | <span data-ttu-id="1cd56-154">Не используйте.</span><span class="sxs-lookup"><span data-stu-id="1cd56-154">Do not use.</span></span> <span data-ttu-id="1cd56-155">Этот подраздел содержит один или несколько подразделов приложения для приложений, которые отображаются в записи диалогового окна " **Открыть с помощью** " для типа файлов и предназначены только для EXE-приложений в операционных системах до Windows XP.</span><span class="sxs-lookup"><span data-stu-id="1cd56-155">This subkey contains one or more application subkeys for applications that appear in the **Open with** dialog box entry for the file type and is intended only for .exe applications on operating systems prior to Windows XP.</span></span> <span data-ttu-id="1cd56-156">Вместо этого используйте Опенвиспрогидс.</span><span class="sxs-lookup"><span data-stu-id="1cd56-156">Use OpenWithProgIds instead.</span></span>                                                            |
| <span data-ttu-id="1cd56-157">OpenWithProgIds</span><span class="sxs-lookup"><span data-stu-id="1cd56-157">OpenWithProgIds</span></span> | <span data-ttu-id="1cd56-158">Этот подраздел содержит список альтернативных идентификаторов ProgID для этого типа файлов.</span><span class="sxs-lookup"><span data-stu-id="1cd56-158">This subkey contains a list of alternate ProgIDs for this file type.</span></span> <span data-ttu-id="1cd56-159">Программы для этих идентификаторов ProgID отображаются в меню **Открыть с помощью** и доступны в виде приложений Магазина Windows по умолчанию для этого типа файлов.</span><span class="sxs-lookup"><span data-stu-id="1cd56-159">The programs for these ProgIDs appear in the **Open with** menu and are available as default Windows Store apps for the file type.</span></span> <span data-ttu-id="1cd56-160">Каждый раз, когда приложение принимает этот тип файла, изменяя значение по умолчанию, оно также должно добавлять запись в этот список.</span><span class="sxs-lookup"><span data-stu-id="1cd56-160">Whenever an application takes over this file type by changing the default value, it should also add an entry to this list.</span></span> |
| <span data-ttu-id="1cd56-161">PerceivedType</span><span class="sxs-lookup"><span data-stu-id="1cd56-161">PerceivedType</span></span>   | <span data-ttu-id="1cd56-162">Установите значение PerceivedType для PerceivedType, которому принадлежит файл, если он есть.</span><span class="sxs-lookup"><span data-stu-id="1cd56-162">Set the PerceivedType value to the PerceivedType to which the file belongs, if any.</span></span> <span data-ttu-id="1cd56-163">Эта строка не используется версиями Windows, выпущенными до Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="1cd56-163">This string is not used by Windows versions prior to Windows Vista.</span></span> <span data-ttu-id="1cd56-164">Дополнительные сведения см. в разделе [наблюдаемые типы и регистрация приложений](fa-perceivedtypes.md).</span><span class="sxs-lookup"><span data-stu-id="1cd56-164">For more information, see [Perceived Types and Application Registration](fa-perceivedtypes.md).</span></span>                                                                           |



 

<span data-ttu-id="1cd56-165">Ниже приведена общая форма подраздела расширения имени файла.</span><span class="sxs-lookup"><span data-stu-id="1cd56-165">The general form of a file name extension subkey is as follows.</span></span> <span data-ttu-id="1cd56-166">Все типы записей имеют тип **reg \_ SZ** .</span><span class="sxs-lookup"><span data-stu-id="1cd56-166">All entry types are of the **REG\_SZ** type.</span></span>

```
HKEY_CLASSES_ROOT
   .ext
      (Default) = ProgID.ext.1
      Content Type = MIME content type
      PerceivedType = PerceivedType
      OpenWithProgids
         ProgID2.ext.1
         ProgID3.ext.1
      ProgID.ext.1
         shellnew
```

<span data-ttu-id="1cd56-167">Ниже приведены важные моменты, связанные с типами файлов.</span><span class="sxs-lookup"><span data-stu-id="1cd56-167">Important considerations about file types include:</span></span>

-   <span data-ttu-id="1cd56-168">**\_ \_ Корневым** поддеревом классов hKey является представление, сформированное путем слияния **\_ \_** \\  \\ **классов** и программного обеспечения **\_ локального \_ компьютера** hKey \\  \\  .</span><span class="sxs-lookup"><span data-stu-id="1cd56-168">The **HKEY\_CLASSES\_ROOT** subtree is a view formed by merging **HKEY\_CURRENT\_USER**\\**Software**\\**Classes** and **HKEY\_LOCAL\_MACHINE**\\**Software**\\**Classes**</span></span>
-   <span data-ttu-id="1cd56-169">Как правило, **\_ \_ корневой класс hKey classes** предназначен для чтения, но не для написания.</span><span class="sxs-lookup"><span data-stu-id="1cd56-169">In general, **HKEY\_CLASSES\_ROOT** is intended to be read from but not written to.</span></span> <span data-ttu-id="1cd56-170">Дополнительные сведения см. в [ \_ \_ корневой статье о классах hKey](../sysinfo/hkey-classes-root-key.md) .</span><span class="sxs-lookup"><span data-stu-id="1cd56-170">For more information, see the [HKEY\_CLASSES\_ROOT](../sysinfo/hkey-classes-root-key.md) article.</span></span>
-   <span data-ttu-id="1cd56-171">Чтобы глобально зарегистрировать тип файла на определенном компьютере, создайте запись для этого типа файлов в подразделе классы программного обеспечения файла **hKey \_ локального \_ компьютера** \\  \\  .</span><span class="sxs-lookup"><span data-stu-id="1cd56-171">To register a file type globally on a particular computer, create an entry for the file type in the **HKEY\_LOCAL\_MACHINE**\\**Software**\\**Classes** subkey.</span></span>
-   <span data-ttu-id="1cd56-172">Чтобы регистрация типа файла стала видимой только для текущего пользователя, создайте запись для типа файла в подразделе «классы **\_ текущего \_ пользовательского** \\ **программного обеспечения**» раздела hKey \\  .</span><span class="sxs-lookup"><span data-stu-id="1cd56-172">To make a file type registration visible to the current user only, create an entry for the file type in the **HKEY\_CURRENT\_USER**\\**Software**\\**Classes** subkey.</span></span>
-   <span data-ttu-id="1cd56-173">Приложение может предоставить собственную реализацию глагола, например Open или Play, как показано в следующем примере реестра.</span><span class="sxs-lookup"><span data-stu-id="1cd56-173">An application can provide its own implementation of a verb, such as open or play, as shown in the following registry example.</span></span>

    ```
    HKEY_CLASSES_ROOT
       Applications
          ApplicationName.exe
             shell
                verb
    ```

    <span data-ttu-id="1cd56-174">Подразделы подраздела команды включают в себя командную строку и целевой метод перетаскивания: **Command** и **дроптаржет**.</span><span class="sxs-lookup"><span data-stu-id="1cd56-174">Subkeys of the verb subkey include the command line and the drop target method: **command** and **DropTarget**.</span></span>

-   <span data-ttu-id="1cd56-175">При создании или изменении сопоставления файлов важно уведомить систему, что вы внесли изменения.</span><span class="sxs-lookup"><span data-stu-id="1cd56-175">When you create or change a file association, it is important to notify the system that you have made a change.</span></span> <span data-ttu-id="1cd56-176">Для этого вызовите [**шчанженотифи**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) и укажите событие **шкне \_ ассокчанжед** .</span><span class="sxs-lookup"><span data-stu-id="1cd56-176">Do so by calling [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) and specifying the **SHCNE\_ASSOCCHANGED** event.</span></span> <span data-ttu-id="1cd56-177">Если не вызвать **шчанженотифи**, изменение может быть не распознано до тех пор, пока система не будет перезагружена.</span><span class="sxs-lookup"><span data-stu-id="1cd56-177">If you do not call **SHChangeNotify**, the change may not be recognized until after the system is rebooted.</span></span>
-   <span data-ttu-id="1cd56-178">Чтобы получить сведения о реестре, касающиеся сопоставления файлов, используйте интерфейс [**икуеряссоЦиатионс**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) .</span><span class="sxs-lookup"><span data-stu-id="1cd56-178">To retrieve registry information regarding a file association, use the [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) interface.</span></span> <span data-ttu-id="1cd56-179">Сценарий, демонстрирующий эту процедуру, см. в разделе [Пример сценария сопоставления файлов](fa-sample-scenarios.md).</span><span class="sxs-lookup"><span data-stu-id="1cd56-179">For a scenario that illustrates this procedure, see [File Association Sample Scenario](fa-sample-scenarios.md).</span></span>

> [!Note]  
> <span data-ttu-id="1cd56-180">Подразделы реестра " **пути приложений** " и " **приложения** " используются для регистрации и управления поведением системы от имени приложений.</span><span class="sxs-lookup"><span data-stu-id="1cd56-180">Both the **App Paths** and **Applications** registry subkeys are used to register and control the behavior of the system on behalf of applications.</span></span> <span data-ttu-id="1cd56-181">Более подробные сведения об этих функциях см. в разделе [Регистрация приложения](app-registration.md).</span><span class="sxs-lookup"><span data-stu-id="1cd56-181">For more detailed information about this functionality, see [Application Registration](app-registration.md).</span></span>

 

### <a name="deleting-registry-information-during-uninstallation"></a><span data-ttu-id="1cd56-182">Удаление данных реестра во время удаления</span><span class="sxs-lookup"><span data-stu-id="1cd56-182">Deleting Registry Information During Uninstallation</span></span>

<span data-ttu-id="1cd56-183">При удалении приложения идентификаторы ProgID и большинство других данных реестра, связанных с этим приложением, должны быть удалены в процессе удаления.</span><span class="sxs-lookup"><span data-stu-id="1cd56-183">When uninstalling an application, the ProgIDs and most other registry information associated with that application should be deleted as part of the uninstallation.</span></span> <span data-ttu-id="1cd56-184">Тем не менее, приложения, которые владеют типом файла (путем установки значения по умолчанию для подраздела **\_ \_ root** \\ *. extension* в файле типа файла с идентификатором ProgID приложения), не должны пытаться удалить это значение при удалении.</span><span class="sxs-lookup"><span data-stu-id="1cd56-184">However, applications that have taken ownership of a file type (by setting the Default value of the file type's **HKEY\_CLASSES\_ROOT**\\ *.extension* subkey to the ProgID of the application) should not attempt to remove that value when uninstalling.</span></span> <span data-ttu-id="1cd56-185">Если не вводить данные в качестве значения по умолчанию, это позволяет избежать трудностей определить, является ли другое приложение владельцем файла и перезаписало значение по умолчанию после установки исходного приложения.</span><span class="sxs-lookup"><span data-stu-id="1cd56-185">Leaving the data in place for the Default value avoids the difficulty of determining whether another application has taken ownership of the file type and overwritten the Default value after the original application was installed.</span></span> <span data-ttu-id="1cd56-186">Значение по умолчанию для Windows учитывается только в том случае, если найден зарегистрированный идентификатор ProgID.</span><span class="sxs-lookup"><span data-stu-id="1cd56-186">Windows respects the Default value only if the ProgID found there is a registered ProgID.</span></span> <span data-ttu-id="1cd56-187">Если идентификатор ProgID не зарегистрирован, он игнорируется.</span><span class="sxs-lookup"><span data-stu-id="1cd56-187">If the ProgID is unregistered, it is ignored.</span></span>

<span data-ttu-id="1cd56-188">Обратите внимание, что другие сведения о владении типами файлов хранятся в поддереве **hKey \_ Current \_ User**, а также используются только при регистрации приложения, на которое он ссылается.</span><span class="sxs-lookup"><span data-stu-id="1cd56-188">Note that other file-type ownership information is stored in the **HKEY\_CURRENT\_USER** subtree and also is used only when the application that it references is registered.</span></span> <span data-ttu-id="1cd56-189">Поэтому эти данные не нужно удалять при удалении приложения.</span><span class="sxs-lookup"><span data-stu-id="1cd56-189">Therefore, this data does not need to be removed when uninstalling an application.</span></span>

<span data-ttu-id="1cd56-190">В качестве примера ниже показано состояние реестра перед удалением приложения.</span><span class="sxs-lookup"><span data-stu-id="1cd56-190">As an example, the following shows the state of the registry before an application is uninstalled:</span></span>

```
HKEY_CLASSES_ROOT
   .mp3
      (Default) = YourProgID
   YourProgID
      shell
         open
            command
               (Default) = yourapp.exe %1
```

<span data-ttu-id="1cd56-191">Ниже показано состояние тех же записей реестра после удаления приложения.</span><span class="sxs-lookup"><span data-stu-id="1cd56-191">The following shows the state of those same registry entries after the application has been uninstalled.</span></span>

```
HKEY_CLASSES_ROOT
   .mp3
      (Default) = YourProgID
   YourProgID subkey removed
```

## <a name="file-types-that-support-open-metadata"></a><span data-ttu-id="1cd56-192">Типы файлов, поддерживающие открытые метаданные</span><span class="sxs-lookup"><span data-stu-id="1cd56-192">File Types That Support Open Metadata</span></span>

<span data-ttu-id="1cd56-193">В Windows 7 и более поздних версиях следующие типы файлов поддерживают открытые метаданные.</span><span class="sxs-lookup"><span data-stu-id="1cd56-193">In Windows 7 and later, the following file types support open metadata.</span></span>



| <span data-ttu-id="1cd56-194">Тип файла</span><span class="sxs-lookup"><span data-stu-id="1cd56-194">File type</span></span>                                                               | <span data-ttu-id="1cd56-195">Расширения имен файлов</span><span class="sxs-lookup"><span data-stu-id="1cd56-195">File name extensions</span></span>                                          |
|-------------------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="1cd56-196">Документы Office 2007</span><span class="sxs-lookup"><span data-stu-id="1cd56-196">Office 2007 Documents</span></span>                                                   | <span data-ttu-id="1cd56-197">DOCX, XLSX, PPTX</span><span class="sxs-lookup"><span data-stu-id="1cd56-197">.docx, .xlsx, .pptx</span></span>                                           |
| <span data-ttu-id="1cd56-198">Документы Office 97-2003</span><span class="sxs-lookup"><span data-stu-id="1cd56-198">Office 97-2003 Documents</span></span>                                                | <span data-ttu-id="1cd56-199">doc, XLS, PPT</span><span class="sxs-lookup"><span data-stu-id="1cd56-199">.doc, .xls, .ppt</span></span>                                              |
| <span data-ttu-id="1cd56-200">Сохраненные поисковые запросы</span><span class="sxs-lookup"><span data-stu-id="1cd56-200">Saved Search</span></span>                                                            | <span data-ttu-id="1cd56-201">. Search — MS</span><span class="sxs-lookup"><span data-stu-id="1cd56-201">.search-ms</span></span>                                                    |
| <span data-ttu-id="1cd56-202">Форматы на основе Windows Media (формат ASF)</span><span class="sxs-lookup"><span data-stu-id="1cd56-202">Windows Media-based formats (Advanced Streaming Format (ASF) container)</span></span> | <span data-ttu-id="1cd56-203">. WMV,. WMA</span><span class="sxs-lookup"><span data-stu-id="1cd56-203">.wmv, .wma</span></span>                                                    |
| <span data-ttu-id="1cd56-204">MP4 (обработчик свойств)</span><span class="sxs-lookup"><span data-stu-id="1cd56-204">MP4 (property handler)</span></span>                                                  | <span data-ttu-id="1cd56-205">MP4, M4A,. m4v,. MP4V,. M4P,. m4b,. 3GP,. 3GPP,. 3GP2,. mov</span><span class="sxs-lookup"><span data-stu-id="1cd56-205">.mp4, .m4a, .m4v, .mp4v, .m4p, .m4b, .3gp, .3gpp, .3gp2, .mov</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="1cd56-206">См. также</span><span class="sxs-lookup"><span data-stu-id="1cd56-206">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1cd56-207">Регистрация приложения</span><span class="sxs-lookup"><span data-stu-id="1cd56-207">Application Registration</span></span>](app-registration.md)
</dt> <dt>

[<span data-ttu-id="1cd56-208">Как работают сопоставления файлов</span><span class="sxs-lookup"><span data-stu-id="1cd56-208">How File Associations Work</span></span>](fa-how-work.md)
</dt> <dt>

[<span data-ttu-id="1cd56-209">Представление содержимого по типу или виду файла</span><span class="sxs-lookup"><span data-stu-id="1cd56-209">Content View By File Type or Kind</span></span>](prophand-content-view.md)
</dt> <dt>

[<span data-ttu-id="1cd56-210">Средство проверки типов файлов</span><span class="sxs-lookup"><span data-stu-id="1cd56-210">File Type Verifier</span></span>](file-type-verifier.md)
</dt> <dt>

[<span data-ttu-id="1cd56-211">Обработчики типов файлов</span><span class="sxs-lookup"><span data-stu-id="1cd56-211">File Type Handlers</span></span>](fa-file-extensions.md)
</dt> <dt>

[<span data-ttu-id="1cd56-212">Программные идентификаторы</span><span class="sxs-lookup"><span data-stu-id="1cd56-212">Programmatic Identifiers</span></span>](fa-progids.md)
</dt> <dt>

[<span data-ttu-id="1cd56-213">Наблюдаемые типы</span><span class="sxs-lookup"><span data-stu-id="1cd56-213">Perceived Types</span></span>](fa-perceivedtypes.md)
</dt> <dt>

[<span data-ttu-id="1cd56-214">Массивы ассоциаций</span><span class="sxs-lookup"><span data-stu-id="1cd56-214">Association Arrays</span></span>](fa-associationarray.md)
</dt> </dl>

 

 
