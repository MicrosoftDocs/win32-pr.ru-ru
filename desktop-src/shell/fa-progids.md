---
description: Оболочка использует подраздел реестра программного идентификатора (ProgID), чтобы связать тип файла с приложением и управлять поведением ассоциации.
ms.assetid: f2b666d6-bf22-47b5-87e1-8de5ff51c152
title: Программные идентификаторы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67720fed1ad4b8401d11f6532cdc79836911e7cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997222"
---
# <a name="programmatic-identifiers"></a><span data-ttu-id="70941-103">Программные идентификаторы</span><span class="sxs-lookup"><span data-stu-id="70941-103">Programmatic Identifiers</span></span>

<span data-ttu-id="70941-104">Оболочка использует подраздел реестра программного идентификатора (ProgID), чтобы связать тип файла с приложением и управлять поведением ассоциации.</span><span class="sxs-lookup"><span data-stu-id="70941-104">The Shell uses a programmatic identifier (ProgID) registry subkey to associate a file type with an application, and to control the behavior of the association.</span></span> <span data-ttu-id="70941-105">Записи ProgID, используемые для сопоставления файлов, находятся в **разделе \_ \_ корневые классы hKey** в реестре.</span><span class="sxs-lookup"><span data-stu-id="70941-105">The ProgID entries used for file associations are located under **HKEY\_CLASSES\_ROOT** in the registry.</span></span>

<span data-ttu-id="70941-106">Этот раздел организован следующим образом:</span><span class="sxs-lookup"><span data-stu-id="70941-106">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="70941-107">Программные элементы идентификаторов, используемые при сопоставлении файлов</span><span class="sxs-lookup"><span data-stu-id="70941-107">Programmatic Identifier Elements Used by File Associations</span></span>](#programmatic-identifier-elements-used-by-file-associations)
-   [<span data-ttu-id="70941-108">Использование программных идентификаторов с управлением версиями</span><span class="sxs-lookup"><span data-stu-id="70941-108">Using Versioned Programmatic Identifiers</span></span>](#using-versioned-programmatic-identifiers)
-   [<span data-ttu-id="70941-109">См. также</span><span class="sxs-lookup"><span data-stu-id="70941-109">Related topics</span></span>](#related-topics)

<span data-ttu-id="70941-110">Дополнительные сведения см. [в статье регистрация типа файла для нового приложения](how-to-register-a-file-type-for-a-new-application.md) .</span><span class="sxs-lookup"><span data-stu-id="70941-110">For additional information, read [How To Register a File Type for a New Application](how-to-register-a-file-type-for-a-new-application.md)</span></span>

## <a name="programmatic-identifier-elements-used-by-file-associations"></a><span data-ttu-id="70941-111">Программные элементы идентификаторов, используемые при сопоставлении файлов</span><span class="sxs-lookup"><span data-stu-id="70941-111">Programmatic Identifier Elements Used by File Associations</span></span>

<span data-ttu-id="70941-112">Правильный формат имени ключа ProgID — « \[ *поставщик» или «приложение* \] ». \[ *Компонент* \] . \[ *Версии* \] , разделенные точками и без пробелов, как в Word.Docумент. 6.</span><span class="sxs-lookup"><span data-stu-id="70941-112">The proper format of a ProgID key name is \[*Vendor or Application*\].\[*Component*\].\[*Version*\], separated by periods and with no spaces, as in Word.Document.6.</span></span> <span data-ttu-id="70941-113">Часть *версии* является необязательной, но настоятельно рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="70941-113">The *Version* portion is optional but strongly recommended.</span></span> <span data-ttu-id="70941-114">Дополнительные сведения см. [в разделе Использование программных идентификаторов с управлением версиями](#using-versioned-programmatic-identifiers).</span><span class="sxs-lookup"><span data-stu-id="70941-114">For more information, see [Using Versioned Programmatic Identifiers](#using-versioned-programmatic-identifiers).</span></span>

<span data-ttu-id="70941-115">Подраздел ProgID должен содержать следующие элементы.</span><span class="sxs-lookup"><span data-stu-id="70941-115">A ProgID subkey should include the following elements.</span></span> <span data-ttu-id="70941-116">Обратите внимание, что для некоторых строковых данных в этом ключе требуется определенное форматирование.</span><span class="sxs-lookup"><span data-stu-id="70941-116">Note that some string data in this key requires specific formatting.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="70941-117">Элемент</span><span class="sxs-lookup"><span data-stu-id="70941-117">Element</span></span></th>
<th><span data-ttu-id="70941-118">Описание</span><span class="sxs-lookup"><span data-stu-id="70941-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="70941-119"><strong>Параметры</strong></span><span class="sxs-lookup"><span data-stu-id="70941-119"><strong>(Default)</strong></span></span></td>
<td><span data-ttu-id="70941-120">Задайте в качестве записи по умолчанию подраздела ProgID понятное имя для этого ProgID, которое будет отображаться для пользователя.</span><span class="sxs-lookup"><span data-stu-id="70941-120">Set the default entry of the ProgID subkey to a friendly name for that ProgID, suitable to display to the user.</span></span> <span data-ttu-id="70941-121">Использование этой записи для хранения понятного имени не рекомендуется для записи Фриендлитипенаме в системах под управлением Windows 2000 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="70941-121">The use of this entry to hold the friendly name is deprecated by the FriendlyTypeName entry on systems running Windows 2000 or later.</span></span> <span data-ttu-id="70941-122">Однако это значение следует задавать для обратной совместимости.</span><span class="sxs-lookup"><span data-stu-id="70941-122">However, you should set this value for backward compatibility.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70941-123"><strong>Алловсилентдефаулттакеовер</strong> (введено в Windows 8)</span><span class="sxs-lookup"><span data-stu-id="70941-123"><strong>AllowSilentDefaultTakeOver</strong> (introduced in Windows 8)</span></span></td>
<td><span data-ttu-id="70941-124">Установите эту необязательную запись, чтобы сообщить, что Windows должен игнорировать этот идентификатор ProgID при определении обработчика по умолчанию для типа общедоступного файла.</span><span class="sxs-lookup"><span data-stu-id="70941-124">Set this optional entry to signal that Windows should ignore this ProgID when determining a default handler for a public file type.</span></span> <span data-ttu-id="70941-125">Независимо от того, задано ли это значение, идентификатор ProgID по-видимому отображается в контекстном меню Опенвис и диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="70941-125">Regardless of whether this value is set, the ProgID continues to appear in the OpenWith shortcut menu and dialog.</span></span> <span data-ttu-id="70941-126">Это REG_NONE значение.</span><span class="sxs-lookup"><span data-stu-id="70941-126">This is a REG_NONE value.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70941-127"><strong>AppUserModelID</strong> (впервые появился в Windows 7)</span><span class="sxs-lookup"><span data-stu-id="70941-127"><strong>AppUserModelID</strong> (introduced in Windows 7)</span></span></td>
<td><span data-ttu-id="70941-128">Установите эту необязательную запись в явном ИДЕНТИФИКАТОРе пользовательской модели приложения (AppUserModelID), если приложение использует явный AppUserModelID и использует автоматически созданные <strong>последние</strong> или <strong>частые</strong> списки переходов или пользовательский список переходов.</span><span class="sxs-lookup"><span data-stu-id="70941-128">Set this optional entry to the application's explicit Application User Model ID (AppUserModelID) if the application uses an explicit AppUserModelID and uses either the system's automatically generated <strong>Recent</strong> or <strong>Frequent</strong> Jump Lists or provides a custom Jump List.</span></span> <span data-ttu-id="70941-129">Если приложение использует явный AppUserModelID и не устанавливает это значение, элементы не будут отображаться в списках переходов этого приложения.</span><span class="sxs-lookup"><span data-stu-id="70941-129">If an application uses an explicit AppUserModelID and does not set this value, items will not appear in that application's Jump Lists.</span></span> <span data-ttu-id="70941-130">Это REG_SZ строка.</span><span class="sxs-lookup"><span data-stu-id="70941-130">This is a REG_SZ string.</span></span> <span data-ttu-id="70941-131">Дополнительные сведения см. в разделе <a href="appids.md">идентификаторы моделей пользователей приложения (аппусермоделидс)</a>.</span><span class="sxs-lookup"><span data-stu-id="70941-131">For more information, see <a href="appids.md">Application User Model IDs (AppUserModelIDs)</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70941-132"><strong>EditFlags</strong></span><span class="sxs-lookup"><span data-stu-id="70941-132"><strong>EditFlags</strong></span></span></td>
<td><span data-ttu-id="70941-133">Установите эту необязательную запись с помощью флагов из перечисления <a href="/windows/desktop/api/Shlwapi/ne-shlwapi-filetypeattributeflags"><strong>филетипеаттрибутефлагс</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="70941-133">Set this optional entry using flags from the <a href="/windows/desktop/api/Shlwapi/ne-shlwapi-filetypeattributeflags"><strong>FILETYPEATTRIBUTEFLAGS</strong></a> enumeration.</span></span> <span data-ttu-id="70941-134">Запись Едитфлагс управляет некоторыми аспектами обработки типов файлов, связанных с этим ProgID, в оболочке.</span><span class="sxs-lookup"><span data-stu-id="70941-134">The EditFlags entry controls some aspects of the Shell's handling of the file types linked to this ProgID.</span></span> <span data-ttu-id="70941-135">Кроме того, можно использовать запись Едитфлагс для ограничения объема, который пользователь может изменять в определенных аспектах этих типов файлов, с помощью страницы свойств файла.</span><span class="sxs-lookup"><span data-stu-id="70941-135">You can also use the EditFlags entry to limit how much the user can modify certain aspects of these file types using a file's property sheet.</span></span> <span data-ttu-id="70941-136">Значения <strong>филетипеаттрибутефлагс</strong> , используемые для едитфлагс, — это двоичные значения, разработанные таким образом, что можно объединить несколько атрибутов в одно значение в битовой операции OR.</span><span class="sxs-lookup"><span data-stu-id="70941-136">The <strong>FILETYPEATTRIBUTEFLAGS</strong> values used for EditFlags are binary values designed so that you can combine multiple attributes into a single value in a bitwise OR operation.</span></span> <span data-ttu-id="70941-137">Это REG_DWORD или REG_BINARY значение.</span><span class="sxs-lookup"><span data-stu-id="70941-137">This is a REG_DWORD or REG_BINARY value.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70941-138"><strong>фриендлитипенаме</strong></span><span class="sxs-lookup"><span data-stu-id="70941-138"><strong>FriendlyTypeName</strong></span></span></td>
<td><span data-ttu-id="70941-139">Задайте для этой записи понятное имя ProgID, которое будет отображаться для пользователя.</span><span class="sxs-lookup"><span data-stu-id="70941-139">Set this entry to a friendly name for the ProgID, suitable to display to the user.</span></span> <span data-ttu-id="70941-140">Для обеспечения согласованности эта строка должна содержать те же данные, что и запись по умолчанию для этого ключа ProgID.</span><span class="sxs-lookup"><span data-stu-id="70941-140">For consistency, this string should contain the same data as the Default entry for this ProgID key.</span></span> <span data-ttu-id="70941-141">Эта запись может быть либо REG_SZ, либо REG_EXPAND_SZ строкой, но ее необходимо отформатировать как косвенную строку (полное имя файла и значение ресурса, предшествующее символу @), например, для экземпляра <em>@% systemroot% \shell32.dll,-154</em>.</span><span class="sxs-lookup"><span data-stu-id="70941-141">This entry can be either a REG_SZ or REG_EXPAND_SZ string, but it must be formatted as an indirect string (a fully qualified file name and resource value preceded by the @ symbol), for instance <em>@%SystemRoot%\shell32.dll,-154</em>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70941-142"><strong>InfoTip</strong></span><span class="sxs-lookup"><span data-stu-id="70941-142"><strong>InfoTip</strong></span></span></td>
<td><span data-ttu-id="70941-143">Задайте для этой записи краткое справочное сообщение, отображаемое оболочкой для этого ProgID.</span><span class="sxs-lookup"><span data-stu-id="70941-143">Set this entry to a brief help message that the Shell displays for this ProgID.</span></span> <span data-ttu-id="70941-144">Запись подсказки отображается в диалоговом окне, наведении указателя мыши.</span><span class="sxs-lookup"><span data-stu-id="70941-144">The InfoTip entry displays in a mouse-over dialog box.</span></span> <span data-ttu-id="70941-145">Это значение может быть либо REG_SZ, либо REG_EXPAND_SZ строкой, но, как Фриендлитипенаме, оно должно быть отформатировано как непрямая строка.</span><span class="sxs-lookup"><span data-stu-id="70941-145">This value can be either a REG_SZ or REG_EXPAND_SZ string but, like FriendlyTypeName, it must be formatted as an indirect string.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="70941-146"><strong>CurVer</strong></span><span class="sxs-lookup"><span data-stu-id="70941-146"><strong>CurVer</strong></span></span></td>
<td><span data-ttu-id="70941-147">Задайте в качестве записи (по умолчанию) этого подраздела самую последнюю версию этого ProgID.</span><span class="sxs-lookup"><span data-stu-id="70941-147">Set the (Default) entry of this subkey to the most current version of this ProgID.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="70941-148">Если у вас нет параллельных версий приложений, то есть несколько версий, установленных в одной системе, следует избегать использования <strong>CurVer</strong>.</span><span class="sxs-lookup"><span data-stu-id="70941-148">Unless you have side-by-side application versions, that is, multiple versions installed on the same system, you should avoid using <strong>CurVer</strong>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70941-149"><strong>Дефаултикон</strong>.</span><span class="sxs-lookup"><span data-stu-id="70941-149"><strong>DefaultIcon</strong>.</span></span></td>
<td><span data-ttu-id="70941-150">Присвойте записи (по умолчанию) этого подраздела значок по умолчанию, который будет отображаться для типов файлов, связанных с этим ProgID.</span><span class="sxs-lookup"><span data-stu-id="70941-150">Set the (Default) entry of this subkey to the default icon that you want to display for file types associated with this ProgID.</span></span> <span data-ttu-id="70941-151">Это значение может быть либо REG_SZ, либо REG_EXPAND_SZ строкой, но оно должно быть указано как полное имя файла со значением ресурса помощника, например <em>% systemroot% \shell32.dll,-154</em>.</span><span class="sxs-lookup"><span data-stu-id="70941-151">This value can be either a REG_SZ or REG_EXPAND_SZ string, but it must be provided as a fully qualified file name with its attendant resource value, for instance <em>%SystemRoot%\shell32.dll,-154</em>.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="70941-152">В следующем примере раздела реестра показан узел ключа ProgID для сопоставления файлов:</span><span class="sxs-lookup"><span data-stu-id="70941-152">The following registry key example illustrates a file association ProgID key node:</span></span>

```
HKEY_CLASSES_ROOT
   Vendor.App.1
      (Default) = My Friendly Name
      AllowSilentDefaultTakeOver
      AppUserModelID = Vendor.Application
      EditFlags = 0x00000001
      FriendlyTypeName = @%SystemRoot%\shell32.dll,-154
      InfoTip = @%SystemRoot%\shell32.dll,-54
      CurVer
         (Default) = Vendor.App.1
      DefaultIcon
         (Default) = %SystemRoot%\shell32.dll,-1
```

## <a name="using-versioned-programmatic-identifiers"></a><span data-ttu-id="70941-153">Использование программных идентификаторов с управлением версиями</span><span class="sxs-lookup"><span data-stu-id="70941-153">Using Versioned Programmatic Identifiers</span></span>

<span data-ttu-id="70941-154">Версия ProgID, версия которой указывается в имени.</span><span class="sxs-lookup"><span data-stu-id="70941-154">A versioned ProgID is one whose version is indicated in its name.</span></span> <span data-ttu-id="70941-155">Обычно это делается путем добавления точки и номера версии к имени.</span><span class="sxs-lookup"><span data-stu-id="70941-155">You typically do this by adding a period and the version number to the name.</span></span> <span data-ttu-id="70941-156">Например:</span><span class="sxs-lookup"><span data-stu-id="70941-156">For example:</span></span>

-   <span data-ttu-id="70941-157">Word.Docумент. 6</span><span class="sxs-lookup"><span data-stu-id="70941-157">Word.Document.6</span></span>
-   <span data-ttu-id="70941-158">Word.Docумент. 8</span><span class="sxs-lookup"><span data-stu-id="70941-158">Word.Document.8</span></span>

<span data-ttu-id="70941-159">Это идентификаторы ProgID с версиями 6 и 8 соответственно.</span><span class="sxs-lookup"><span data-stu-id="70941-159">These are versioned ProgIDs, with versions 6 and 8 respectively.</span></span> <span data-ttu-id="70941-160">Если у вас есть параллельное приложение, то есть одновременно поддерживает несколько версий приложения, используйте CurVer и независимые от версии идентификаторы ProgID.</span><span class="sxs-lookup"><span data-stu-id="70941-160">If you have a side-by-side application, that is, one that supports multiple versions of your application installed at the same time, then use CurVer and Version Independent ProgIDs.</span></span> <span data-ttu-id="70941-161">В противном случае CurVer и независимые от версии идентификаторы ProgID следует избегать, поскольку они приводят к неэффективному повышению эффективности.</span><span class="sxs-lookup"><span data-stu-id="70941-161">Otherwise, CurVer and Version Independent ProgIDs should be avoided because they will lead to inefficiency.</span></span>

## <a name="related-topics"></a><span data-ttu-id="70941-162">См. также</span><span class="sxs-lookup"><span data-stu-id="70941-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="70941-163">Как зарегистрировать тип файла для нового приложения</span><span class="sxs-lookup"><span data-stu-id="70941-163">How To Register a File Type for a New Application</span></span>](how-to-register-a-file-type-for-a-new-application.md)
</dt> <dt>

[<span data-ttu-id="70941-164">Регистрация приложения</span><span class="sxs-lookup"><span data-stu-id="70941-164">Application Registration</span></span>](app-registration.md)
</dt> <dt>

[<span data-ttu-id="70941-165">Типы файлов</span><span class="sxs-lookup"><span data-stu-id="70941-165">File Types</span></span>](fa-file-types.md)
</dt> <dt>

[<span data-ttu-id="70941-166">Как работают сопоставления файлов</span><span class="sxs-lookup"><span data-stu-id="70941-166">How File Associations Work</span></span>](fa-how-work.md)
</dt> <dt>

[<span data-ttu-id="70941-167">Представление содержимого по типу или виду файла</span><span class="sxs-lookup"><span data-stu-id="70941-167">Content View By File Type or Kind</span></span>](prophand-content-view.md)
</dt> <dt>

[<span data-ttu-id="70941-168">Средство проверки типов файлов</span><span class="sxs-lookup"><span data-stu-id="70941-168">File Type Verifier</span></span>](file-type-verifier.md)
</dt> <dt>

[<span data-ttu-id="70941-169">Обработчики типов файлов</span><span class="sxs-lookup"><span data-stu-id="70941-169">File Type Handlers</span></span>](fa-file-extensions.md)
</dt> <dt>

[<span data-ttu-id="70941-170">Наблюдаемые типы</span><span class="sxs-lookup"><span data-stu-id="70941-170">Perceived Types</span></span>](fa-perceivedtypes.md)
</dt> <dt>

[<span data-ttu-id="70941-171">Массивы ассоциаций</span><span class="sxs-lookup"><span data-stu-id="70941-171">Association Arrays</span></span>](fa-associationarray.md)
</dt> </dl>

 

 




