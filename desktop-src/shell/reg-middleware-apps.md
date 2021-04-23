---
description: 'В этом разделе объясняется, как зарегистрировать программу в реестре Windows как один из следующих типов клиентов: браузер, электронная почта, воспроизведение мультимедиа, Обмен мгновенными сообщениями или виртуальная машина для Java.'
title: Регистрация программ с помощью клиентских типов
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 33fcb63c-3db2-44df-acfe-8c88e2e634e4
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 71dd4e3192dc75821fd0a3e8c0d4742e1a8d571a
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "103914244"
---
# <a name="registering-programs-with-client-types"></a><span data-ttu-id="695ff-103">Регистрация программ с помощью клиентских типов</span><span class="sxs-lookup"><span data-stu-id="695ff-103">Registering Programs with Client Types</span></span>

<span data-ttu-id="695ff-104">В этом разделе объясняется, как зарегистрировать программу в реестре Windows как один из следующих типов клиентов: браузер, электронная почта, воспроизведение мультимедиа, Обмен мгновенными сообщениями или виртуальная машина для Java.</span><span class="sxs-lookup"><span data-stu-id="695ff-104">This topic explains how to register a program in the Windows registry as one of the following client types: browser, email, media playback, instant messaging, or virtual machine for Java.</span></span>

> [!Note]  
> <span data-ttu-id="695ff-105">Эти сведения относятся к следующим операционным системам:</span><span class="sxs-lookup"><span data-stu-id="695ff-105">This information applies to the following operating systems:</span></span>
> 
> -   <span data-ttu-id="695ff-106">Windows 2000 с пакетом обновления 3 (SP3)</span><span class="sxs-lookup"><span data-stu-id="695ff-106">Windows 2000 Service Pack 3 (SP3)</span></span>
> -   <span data-ttu-id="695ff-107">Windows 2000 с пакетом обновления 4 (SP4)</span><span class="sxs-lookup"><span data-stu-id="695ff-107">Windows 2000 Service Pack 4 (SP4)</span></span>
> -   <span data-ttu-id="695ff-108">Пакет обновления 1 (SP1) для Windows XP</span><span class="sxs-lookup"><span data-stu-id="695ff-108">Windows XP Service Pack 1 (SP1)</span></span>
> -   <span data-ttu-id="695ff-109">Пакет обновления 2 (SP2) для Windows XP</span><span class="sxs-lookup"><span data-stu-id="695ff-109">Windows XP Service Pack 2 (SP2)</span></span>
> -   <span data-ttu-id="695ff-110">Пакет обновления 3 (SP3) для Windows XP</span><span class="sxs-lookup"><span data-stu-id="695ff-110">Windows XP Service Pack 3 (SP3)</span></span>
> -   <span data-ttu-id="695ff-111">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="695ff-111">Windows Server 2003</span></span>
> -   <span data-ttu-id="695ff-112">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="695ff-112">Windows Vista</span></span>
> -   <span data-ttu-id="695ff-113">Пакет обновления 1 (SP1) для Windows Vista</span><span class="sxs-lookup"><span data-stu-id="695ff-113">Windows Vista Service Pack 1 (SP1)</span></span>
> -   <span data-ttu-id="695ff-114">Windows 8</span><span class="sxs-lookup"><span data-stu-id="695ff-114">Windows 8</span></span>

 

<span data-ttu-id="695ff-115">Этот раздел включает следующие подразделы:</span><span class="sxs-lookup"><span data-stu-id="695ff-115">This topic includes the following sections.</span></span>

-   [<span data-ttu-id="695ff-116">Общие элементы регистрации для всех типов клиентов</span><span class="sxs-lookup"><span data-stu-id="695ff-116">Common Registration Elements for All Client Types</span></span>](#common-registration-elements-for-all-client-types)
    -   [<span data-ttu-id="695ff-117">Выбор канонического имени</span><span class="sxs-lookup"><span data-stu-id="695ff-117">Selecting a Canonical Name</span></span>](#selecting-a-canonical-name)
    -   [<span data-ttu-id="695ff-118">Регистрация отображаемого имени программы</span><span class="sxs-lookup"><span data-stu-id="695ff-118">Registering a Program's Display Name</span></span>](#registering-a-programs-display-name)
    -   [<span data-ttu-id="695ff-119">Регистрация значка программы</span><span class="sxs-lookup"><span data-stu-id="695ff-119">Registering a Program's Icon</span></span>](#registering-a-programs-icon)
    -   [<span data-ttu-id="695ff-120">Регистрация команды Open</span><span class="sxs-lookup"><span data-stu-id="695ff-120">Registering an Open Verb</span></span>](#registering-an-open-verb)
    -   [<span data-ttu-id="695ff-121">Регистрация сведений об установке</span><span class="sxs-lookup"><span data-stu-id="695ff-121">Registering Installation Information</span></span>](#registering-installation-information)
-   [<span data-ttu-id="695ff-122">Элементы регистрации для конкретных типов клиентов</span><span class="sxs-lookup"><span data-stu-id="695ff-122">Registration Elements for Specific Client Types</span></span>](#registration-elements-for-specific-client-types)
    -   [<span data-ttu-id="695ff-123">Регистрация в меню "Пуск"</span><span class="sxs-lookup"><span data-stu-id="695ff-123">Start Menu Registration</span></span>](#start-menu-registration)
    -   [<span data-ttu-id="695ff-124">Регистрация почтового клиента</span><span class="sxs-lookup"><span data-stu-id="695ff-124">Mail Client Registration</span></span>](#mail-client-registration)
-   [<span data-ttu-id="695ff-125">Полные примеры регистраций</span><span class="sxs-lookup"><span data-stu-id="695ff-125">Complete Sample Registrations</span></span>](#complete-sample-registrations)
    -   [<span data-ttu-id="695ff-126">Пример браузера</span><span class="sxs-lookup"><span data-stu-id="695ff-126">A Sample Browser</span></span>](#a-sample-browser)
    -   [<span data-ttu-id="695ff-127">Пример почтового браузера</span><span class="sxs-lookup"><span data-stu-id="695ff-127">A Sample Mail Browser</span></span>](#a-sample-mail-browser)
    -   [<span data-ttu-id="695ff-128">Пример проигрывателя мультимедиа</span><span class="sxs-lookup"><span data-stu-id="695ff-128">A Sample Media Player</span></span>](#a-sample-media-player)
    -   [<span data-ttu-id="695ff-129">Пример программы мгновенных сообщений</span><span class="sxs-lookup"><span data-stu-id="695ff-129">A Sample Instant Messenger Program</span></span>](#a-sample-instant-messenger-program)
    -   [<span data-ttu-id="695ff-130">Пример виртуальной машины для Java</span><span class="sxs-lookup"><span data-stu-id="695ff-130">A Sample Virtual Machine for Java</span></span>](#a-sample-virtual-machine-for-java)
-   [<span data-ttu-id="695ff-131">См. также</span><span class="sxs-lookup"><span data-stu-id="695ff-131">Related topics</span></span>](#related-topics)

<span data-ttu-id="695ff-132">Этот раздел расширяет существующую документацию о регистрации программы в качестве конкретного типа клиента.</span><span class="sxs-lookup"><span data-stu-id="695ff-132">This topic extends existing documentation about registering a program as a particular client type.</span></span> <span data-ttu-id="695ff-133">Ссылки на эту документацию см. в разделе "связанные разделы".</span><span class="sxs-lookup"><span data-stu-id="695ff-133">For links to that documentation, see the Related Topics section.</span></span>

## <a name="common-registration-elements-for-all-client-types"></a><span data-ttu-id="695ff-134">Общие элементы регистрации для всех типов клиентов</span><span class="sxs-lookup"><span data-stu-id="695ff-134">Common Registration Elements for All Client Types</span></span>

<span data-ttu-id="695ff-135">При регистрации программы в качестве типа клиента большая часть записей реестра одинакова независимо от типа клиента.</span><span class="sxs-lookup"><span data-stu-id="695ff-135">When registering a program as a client type, most of the registry entries are the same regardless of the client type.</span></span> <span data-ttu-id="695ff-136">Некоторые записи реестра, однако, относятся к типу клиента, и они указаны в разделе [элементы регистрации для конкретных типов клиентов](#registration-elements-for-specific-client-types) .</span><span class="sxs-lookup"><span data-stu-id="695ff-136">Some registry entries, however, are specific to the client type and these are noted in the [Registration Elements for Specific Client Types](#registration-elements-for-specific-client-types) section.</span></span>

<span data-ttu-id="695ff-137">В этом разделе рассматриваются следующие темы:</span><span class="sxs-lookup"><span data-stu-id="695ff-137">This section discusses the following topics:</span></span>

-   [<span data-ttu-id="695ff-138">Выбор канонического имени</span><span class="sxs-lookup"><span data-stu-id="695ff-138">Selecting a Canonical Name</span></span>](#selecting-a-canonical-name)
-   [<span data-ttu-id="695ff-139">Регистрация отображаемого имени программы</span><span class="sxs-lookup"><span data-stu-id="695ff-139">Registering a Program's Display Name</span></span>](#registering-a-programs-display-name)
-   [<span data-ttu-id="695ff-140">Регистрация значка программы</span><span class="sxs-lookup"><span data-stu-id="695ff-140">Registering a Program's Icon</span></span>](#registering-a-programs-icon)
-   [<span data-ttu-id="695ff-141">Регистрация команды Open</span><span class="sxs-lookup"><span data-stu-id="695ff-141">Registering an Open Verb</span></span>](#registering-an-open-verb)
-   [<span data-ttu-id="695ff-142">Регистрация сведений об установке</span><span class="sxs-lookup"><span data-stu-id="695ff-142">Registering Installation Information</span></span>](#registering-installation-information)

> [!Note]  
> <span data-ttu-id="695ff-143">Имена подразделов, заданные курсивом в этом разделе, являются заполнителями для имен пользовательских подразделов или набора возможных значений.</span><span class="sxs-lookup"><span data-stu-id="695ff-143">Subkey names given in italics throughout this topic are placeholders for user-defined subkey names or a set of possible values.</span></span> <span data-ttu-id="695ff-144">Полные примеры с именами примеров на месте приведены в разделе [полный пример регистраций](#complete-sample-registrations) .</span><span class="sxs-lookup"><span data-stu-id="695ff-144">Full examples with example names in place are provided in the [Complete Sample Registrations](#complete-sample-registrations) section.</span></span>

 

<span data-ttu-id="695ff-145">Все сведения о регистрации типа клиента хранятся в следующем подразделе:</span><span class="sxs-lookup"><span data-stu-id="695ff-145">All client type registration information is stored under the following subkey:</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
```

<span data-ttu-id="695ff-146">*Клиенттипенаме* является одним из следующих имен подразделов:</span><span class="sxs-lookup"><span data-stu-id="695ff-146">*ClientTypeName* is one of the following subkey names:</span></span>

-   <span data-ttu-id="695ff-147">Стартменуинтернет (для браузеров)</span><span class="sxs-lookup"><span data-stu-id="695ff-147">StartMenuInternet (for browsers)</span></span>
-   <span data-ttu-id="695ff-148">Почта (для электронной почты)</span><span class="sxs-lookup"><span data-stu-id="695ff-148">Mail (for email)</span></span>
-   <span data-ttu-id="695ff-149">Носитель (для воспроизведения мультимедиа)</span><span class="sxs-lookup"><span data-stu-id="695ff-149">Media (for media playback)</span></span>
-   <span data-ttu-id="695ff-150">IM (для обмена мгновенными сообщениями)</span><span class="sxs-lookup"><span data-stu-id="695ff-150">IM (for instant messaging)</span></span>
-   <span data-ttu-id="695ff-151">Жававм (для виртуальной машины для Java)</span><span class="sxs-lookup"><span data-stu-id="695ff-151">JavaVM (for virtual machine for Java)</span></span>

<span data-ttu-id="695ff-152">В этой статье вы запишете ссылки на вымышленную компьютерную программу с именем "освещенное представление", Litware Inc., с исполняемым файлом с именем Litview.exe.</span><span class="sxs-lookup"><span data-stu-id="695ff-152">Throughout this topic, you will note references to a fictional computer program named "Lit View" by Litware Inc., with an executable file named Litview.exe.</span></span> <span data-ttu-id="695ff-153">Эта гипотетическая программа используется в качестве службы мгновенных сообщений, браузера или другого типа клиентской программы по мере необходимости для наглядных целей.</span><span class="sxs-lookup"><span data-stu-id="695ff-153">This hypothetical program is used interchangeably as an instant messenger, a browser, or another type of client program as needed for illustrative purposes.</span></span>

### <a name="selecting-a-canonical-name"></a><span data-ttu-id="695ff-154">Выбор канонического имени</span><span class="sxs-lookup"><span data-stu-id="695ff-154">Selecting a Canonical Name</span></span>

<span data-ttu-id="695ff-155">Поставщик должен выбрать *каноническое имя* для программы.</span><span class="sxs-lookup"><span data-stu-id="695ff-155">The vendor must choose a *canonical name* for the program.</span></span> <span data-ttu-id="695ff-156">Каноническое имя никогда не отображается для пользователя, поэтому его локализация не требуется.</span><span class="sxs-lookup"><span data-stu-id="695ff-156">The canonical name is never shown to the user, so it does not need to be localized.</span></span> <span data-ttu-id="695ff-157">Его единственная задача — предоставить уникальную строку, которую можно использовать для распознавания программы.</span><span class="sxs-lookup"><span data-stu-id="695ff-157">Its only purpose is to provide a unique string that can be used to identify the program.</span></span> <span data-ttu-id="695ff-158">Обычно это то же самое, что и имя программы на английском языке, но это просто соглашение.</span><span class="sxs-lookup"><span data-stu-id="695ff-158">It is typically the same as the English name of the program, but this is merely a convention.</span></span>

<span data-ttu-id="695ff-159">Для клиентских типов, отличных от браузеров, каноническое имя может быть любой строкой.</span><span class="sxs-lookup"><span data-stu-id="695ff-159">For client types other than browsers, the canonical name can be any string.</span></span> <span data-ttu-id="695ff-160">Выберите уникальное имя, которое, скорее всего, не будет использоваться другим поставщиком.</span><span class="sxs-lookup"><span data-stu-id="695ff-160">Choose a unique name, one that is not likely to be used by another vendor.</span></span>

<span data-ttu-id="695ff-161">Для клиентов браузера каноническое имя должно быть именем, включая расширение, связанного исполняемого файла. Например, "Litview.exe".</span><span class="sxs-lookup"><span data-stu-id="695ff-161">For browser clients, the canonical name must be the name—including the extension—of the associated executable; for instance, "Litview.exe".</span></span>

<span data-ttu-id="695ff-162">Ниже приведены некоторые примеры канонических имен.</span><span class="sxs-lookup"><span data-stu-id="695ff-162">Here are some examples of canonical names.</span></span>

-   <span data-ttu-id="695ff-163">Iexplore.exe (браузер)</span><span class="sxs-lookup"><span data-stu-id="695ff-163">Iexplore.exe (browser)</span></span>
-   <span data-ttu-id="695ff-164">Почта Windows (электронная почта)</span><span class="sxs-lookup"><span data-stu-id="695ff-164">Windows Mail (email)</span></span>
-   <span data-ttu-id="695ff-165">Проигрыватель Windows Media (мультимедиа)</span><span class="sxs-lookup"><span data-stu-id="695ff-165">Windows Media Player (media)</span></span>
-   <span data-ttu-id="695ff-166">Windows Messenger (мгновенный обмен сообщениями)</span><span class="sxs-lookup"><span data-stu-id="695ff-166">Windows Messenger (instant messaging)</span></span>

<span data-ttu-id="695ff-167">Зарегистрируйте каноническое имя, создав подраздел, как показано здесь.</span><span class="sxs-lookup"><span data-stu-id="695ff-167">Register the canonical name by creating a subkey as shown here.</span></span> <span data-ttu-id="695ff-168">Имя подраздела представляет собой каноническое имя.</span><span class="sxs-lookup"><span data-stu-id="695ff-168">The name of the subkey is the canonical name.</span></span> <span data-ttu-id="695ff-169">Все сведения, относящиеся к регистрации этой программы, будут находиться в этом подразделе.</span><span class="sxs-lookup"><span data-stu-id="695ff-169">All information relating to that program's registration will exist under this subkey.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
```

### <a name="registering-a-programs-display-name"></a><span data-ttu-id="695ff-170">Регистрация отображаемого имени программы</span><span class="sxs-lookup"><span data-stu-id="695ff-170">Registering a Program's Display Name</span></span>

<span data-ttu-id="695ff-171">Следующим шагом в регистрации является указание отображаемого имени программы.</span><span class="sxs-lookup"><span data-stu-id="695ff-171">The next step in registration is to specify the program's display name.</span></span> <span data-ttu-id="695ff-172">Он указывается как значение под каноническим ключом имени, как показано здесь.</span><span class="sxs-lookup"><span data-stu-id="695ff-172">It is given as a value under the canonical name key as shown here.</span></span> <span data-ttu-id="695ff-173">Обратите внимание, что *каноникалнаме* и *клиенттипенаме* не являются реальными именами ключей, а только заполнители для истинных имен, например, *представление освещенности*.</span><span class="sxs-lookup"><span data-stu-id="695ff-173">Note again that *CanonicalName* and *ClientTypeName* are not the actual names of the keys, but only placeholders for the true names, such as *Lit View*.</span></span>

> [!Note]  
> <span data-ttu-id="695ff-174">Начиная с Windows 8, имя, используемое для регистрации в [параметре "задать доступ к программе" и "параметры по умолчанию" (SPAD)](cpl-setprogramaccess.md) и [программы по умолчанию](default-programs.md) , должно совпадать для того, чтобы изменения SPAD активировали регистрации программ по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="695ff-174">As of Windows 8, the name used to register for [Set Program Access and Computer Defaults (SPAD)](cpl-setprogramaccess.md) and for [Default Programs](default-programs.md) should match in order for SPAD changes to trigger Default Programs registrations.</span></span>

 

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
               LocalizedString = @FilePath,-StringID
```

<span data-ttu-id="695ff-175">Значение **локализедстринг** является \_ строкой reg SZ и состоит из знака "at" (@), полного пути к DLL-или EXE-файлу, запятой, знака "минус" и десятичного целого числа.</span><span class="sxs-lookup"><span data-stu-id="695ff-175">The **LocalizedString** value is a REG\_SZ string and consists of an "at" sign (@), the full path to a .dll or .exe file, a comma, a minus sign, and a decimal integer.</span></span> <span data-ttu-id="695ff-176">Десятичное целое число — это идентификатор строкового ресурса, содержащийся в DLL-или exe-файле, значение которого будет отображаться для пользователя в качестве имени этого клиента.</span><span class="sxs-lookup"><span data-stu-id="695ff-176">The decimal integer is the ID of a string resource—contained within the .dll or .exe file—whose value is to be displayed to the user as the name of this client.</span></span> <span data-ttu-id="695ff-177">Обратите внимание, что путь к файлу не требует кавычек, даже если он содержит пробелы.</span><span class="sxs-lookup"><span data-stu-id="695ff-177">Note that the file path does not require quotation marks, even if it contains spaces.</span></span>

<span data-ttu-id="695ff-178">Регистрация строки отображаемого имени таким образом позволяет использовать одну и ту же регистрацию для нескольких языков.</span><span class="sxs-lookup"><span data-stu-id="695ff-178">Registering the display name string in this manner allows the same registration to be used for multiple languages.</span></span> <span data-ttu-id="695ff-179">При установке каждого языка предоставляется отдельный файл ресурсов с отображаемым именем, хранящимся по тому же ИДЕНТИФИКАТОРу ресурса.</span><span class="sxs-lookup"><span data-stu-id="695ff-179">Each language installation provides a different resource file with the display name stored at the same resource ID.</span></span>

<span data-ttu-id="695ff-180">В следующем примере показана регистрация для вымышленной программы обмена мгновенными сообщениями.</span><span class="sxs-lookup"><span data-stu-id="695ff-180">The following example shows the registration for a fictional Lit View instant messaging program.</span></span> <span data-ttu-id="695ff-181">Так как это программа обмена мгновенными сообщениями, подраздел *каноникалнаме* (в данном случае — « *освещено»*) хранится в подразделе **IM** .</span><span class="sxs-lookup"><span data-stu-id="695ff-181">Because it is an instant messaging program, the *CanonicalName* subkey (in this case *Lit View*) is stored under the **IM** subkey.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         IM
            Lit View
               (Default) = Lit View
               LocalizedString = @C:\Program Files\LitwareInc\ResourceDLL.dll,-123
```

<span data-ttu-id="695ff-182">Обратите внимание на использование записи (по умолчанию) в качестве дополнительного объявления отображаемого имени клиента.</span><span class="sxs-lookup"><span data-stu-id="695ff-182">Note the use of the (Default) entry as a secondary declaration of the client's display name.</span></span> <span data-ttu-id="695ff-183">Если **локализедстринг** отсутствует, вместо него используется значение (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="695ff-183">If the **LocalizedString** is not present, the (Default) value is used instead.</span></span> <span data-ttu-id="695ff-184">Это работает со всеми типами клиентов (интернет-браузерами, обозревателями электронной почты, мгновенными сообщениями и проигрывателями мультимедиа).</span><span class="sxs-lookup"><span data-stu-id="695ff-184">This works with all client types (Internet browsers, email browsers, instant messengers, and media players).</span></span> <span data-ttu-id="695ff-185">Чтобы обеспечить обратную совместимость с [макетом реестра клиента Internet Explorer](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa753633(v=vs.85)), программы электронной почты должны установить значение (по умолчанию) для подраздела *каноникалнаме* на отображаемое имя клиента в текущем установленном языке.</span><span class="sxs-lookup"><span data-stu-id="695ff-185">For backward compatibility with the [Internet Explorer Client Registry Layout](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa753633(v=vs.85)), email programs should set the (Default) value of the *CanonicalName* subkey to the client's display name in the currently installed language.</span></span>

### <a name="registering-a-programs-icon"></a><span data-ttu-id="695ff-186">Регистрация значка программы</span><span class="sxs-lookup"><span data-stu-id="695ff-186">Registering a Program's Icon</span></span>

> [!Note]  
> <span data-ttu-id="695ff-187">Этот раздел не относится к Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="695ff-187">This section does not apply to Windows 2000.</span></span>

 

<span data-ttu-id="695ff-188">По умолчанию верхний раздел меню **Пуск** Windows XP и Windows Vista содержит значки " **Интернет** " и " **Электронная почта** ".</span><span class="sxs-lookup"><span data-stu-id="695ff-188">By default, the upper section of the Windows XP and Windows Vista **Start** menu contains **Internet** and **E-mail** icons.</span></span> <span data-ttu-id="695ff-189">Эти значки отсутствуют в Windows 7 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="695ff-189">These icons are not present in Windows 7 and later.</span></span> <span data-ttu-id="695ff-190">Для клиентов браузера и электронной почты, когда для типа клиента по умолчанию назначена программа, для этих записей меню « **Пуск** » отображается значок зарегистрированной программы.</span><span class="sxs-lookup"><span data-stu-id="695ff-190">For browser and email clients, when a program is assigned as the default for their client type, that program's registered icon is displayed for those **Start** menu entries.</span></span>

<span data-ttu-id="695ff-191">Регистрация значка программы является обязательной для клиентов браузера и электронной почты.</span><span class="sxs-lookup"><span data-stu-id="695ff-191">Registering a program's icon is mandatory for browser and email clients.</span></span> <span data-ttu-id="695ff-192">Регистрация значка для типа клиента "воспроизведение мультимедиа", "обмен мгновенными сообщениями" или "виртуальная машина для клиентов Java" не является обязательной, а зарегистрированные значки для этих типов клиентов в настоящее время не используются Windows и не отображаются в верхней части меню " **Пуск** " Windows XP или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="695ff-192">Registering an icon for the media playback, instant messaging, or virtual machine for Java client types is optional, and registered icons for those client types are not currently used by Windows and are not displayed in the upper section of the Windows XP or Windows Vista **Start** menus.</span></span>

<span data-ttu-id="695ff-193">Чтобы зарегистрировать значок для клиентской программы, добавьте подраздел **дефаултикон** со значением по умолчанию, как показано здесь.</span><span class="sxs-lookup"><span data-stu-id="695ff-193">To register an icon for a client program, add a **DefaultIcon** subkey with a default value as shown here.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
               DefaultIcon
                  (Default) = FilePath,IconIndex
```

<span data-ttu-id="695ff-194">Значение **FilePath** — это полный путь к файлу, содержащему значок.</span><span class="sxs-lookup"><span data-stu-id="695ff-194">The **FilePath** value is the full path to the file that contains the icon.</span></span> <span data-ttu-id="695ff-195">Этот путь не требует кавычек, даже если он содержит пробелы.</span><span class="sxs-lookup"><span data-stu-id="695ff-195">This path does not require quotation marks, even if it contains spaces.</span></span>

<span data-ttu-id="695ff-196">Значение **икониндекс** интерпретируется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="695ff-196">The **IconIndex** value is interpreted as follows:</span></span>

-   <span data-ttu-id="695ff-197">Если **икониндекс** является положительным числом, то это число используется в качестве индекса массива значков, отходящихся от *нуля* , хранящихся в файле.</span><span class="sxs-lookup"><span data-stu-id="695ff-197">If **IconIndex** is a positive number, the number is used as the index of the *zero-based* array of icons stored in the file.</span></span> <span data-ttu-id="695ff-198">Например, если **икониндекс** имеет значение 1, второй значок загружается из файла.</span><span class="sxs-lookup"><span data-stu-id="695ff-198">For example, if **IconIndex** is 1, the second icon is loaded from the file.</span></span>
-   <span data-ttu-id="695ff-199">Если **икониндекс** является отрицательным числом, абсолютное значение **икониндекс** используется в качестве идентификатора ресурса (а не индекса) для значка.</span><span class="sxs-lookup"><span data-stu-id="695ff-199">If **IconIndex** is a negative number, the absolute value of **IconIndex** is used as the resource identifier (rather than the index) for the icon.</span></span> <span data-ttu-id="695ff-200">Например, если **икониндекс** имеет значение-3, в файле загружается значок, идентификатор ресурса которого равен 3.</span><span class="sxs-lookup"><span data-stu-id="695ff-200">For example, if **IconIndex** is -3, the icon whose resource identifier is 3 is loaded from the file.</span></span>

<span data-ttu-id="695ff-201">В следующем примере показана регистрация гипотетических браузеров представлений освещенности.</span><span class="sxs-lookup"><span data-stu-id="695ff-201">The following example shows the registration of a hypothetical Lit View browser.</span></span> <span data-ttu-id="695ff-202">В качестве значения по умолчанию используется второй значок, хранящийся в файле Litview.exe.</span><span class="sxs-lookup"><span data-stu-id="695ff-202">The second icon stored in the Litview.exe file is used as the default.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         StartMenuInternet
            LITVIEW.EXE
               DefaultIcon
                  (Default) = C:\Program Files\LitwareInc\Litview.exe,1
```

### <a name="registering-an-open-verb"></a><span data-ttu-id="695ff-203">Регистрация команды Open</span><span class="sxs-lookup"><span data-stu-id="695ff-203">Registering an Open Verb</span></span>

> [!Note]  
> <span data-ttu-id="695ff-204">Этот раздел не относится к Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="695ff-204">This section does not apply to Windows 2000.</span></span> <span data-ttu-id="695ff-205">Следующий шаг необходим только для клиентов браузера и электронной почты.</span><span class="sxs-lookup"><span data-stu-id="695ff-205">The following step is necessary only for browser and email clients.</span></span>

 

<span data-ttu-id="695ff-206">Предположим, что пользователь выбрал вашу программу в качестве программы Интернета или электронной почты по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="695ff-206">Assume that a user has selected your program as the default Internet or email program.</span></span> <span data-ttu-id="695ff-207">Этот пользователь щелкает значок **Интернета** или **электронной почты** в меню **Пуск** Windows XP или Windows Vista, чтобы открыть программу.</span><span class="sxs-lookup"><span data-stu-id="695ff-207">That user clicks the **Internet** or **E-mail** icon in the Windows XP or Windows Vista **Start** menu to open the program.</span></span> <span data-ttu-id="695ff-208">В этот момент выполняется Командная строка, зарегистрированная, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="695ff-208">At that point, the command line registered as shown here is executed.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
               shell
                  open
                     command
                        (Default) = command line
```

<span data-ttu-id="695ff-209">Командная строка должна указывать полный абсолютный путь к файлу, за которым следуют дополнительные параметры командной строки.</span><span class="sxs-lookup"><span data-stu-id="695ff-209">The command line must specify a fully qualified absolute path to the file, followed by optional command-line options.</span></span> <span data-ttu-id="695ff-210">Если тип записи — \_ \_ SZ, то в пути можно использовать переменные среды.</span><span class="sxs-lookup"><span data-stu-id="695ff-210">If the entry type is REG\_EXPAND\_SZ, environment variables can be used in the path.</span></span> <span data-ttu-id="695ff-211">Используйте кавычки, чтобы гарантировать неправильное интерпретацию пробелов в командной строке.</span><span class="sxs-lookup"><span data-stu-id="695ff-211">Use quotation marks appropriately to ensure that spaces in the command line are not misinterpreted.</span></span> <span data-ttu-id="695ff-212">Командная строка должна выполнять программу с соответствующими значениями по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="695ff-212">The command line should execute the program with appropriate defaults.</span></span> <span data-ttu-id="695ff-213">Обычно браузеры по умолчанию используют домашнюю страницу пользователя.</span><span class="sxs-lookup"><span data-stu-id="695ff-213">Browsers generally default to the user's home page.</span></span> <span data-ttu-id="695ff-214">Обычно программы электронной почты открывают **папку "Входящие"** пользователя.</span><span class="sxs-lookup"><span data-stu-id="695ff-214">Email programs generally open the user's **Inbox**.</span></span>

<span data-ttu-id="695ff-215">В следующем примере показана регистрация `open` команды для гипотетических браузеров представлений освещенности.</span><span class="sxs-lookup"><span data-stu-id="695ff-215">The following example shows the registration of an `open` verb for a hypothetical Lit View browser.</span></span> <span data-ttu-id="695ff-216">В нем не указаны параметры командной строки.</span><span class="sxs-lookup"><span data-stu-id="695ff-216">It specifies no command-line options.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         StartMenuInternet
            LITVIEW.EXE
               shell
                  open
                     command
                        (Default) = "C:\Program Files\LitwareInc\Litview.exe"
```

<span data-ttu-id="695ff-217">Обратите внимание, что в этом значении символы кавычек размещаются вокруг пути, так как они содержат пробелы.</span><span class="sxs-lookup"><span data-stu-id="695ff-217">Note that in this value, quotation marks are placed around the path because it contains embedded spaces.</span></span> <span data-ttu-id="695ff-218">Пропуск этих кавычек может привести к неправильной интерпретации командной строки.</span><span class="sxs-lookup"><span data-stu-id="695ff-218">Omitting these quotation marks could cause the command line to be misinterpreted.</span></span>

### <a name="registering-installation-information"></a><span data-ttu-id="695ff-219">Регистрация сведений об установке</span><span class="sxs-lookup"><span data-stu-id="695ff-219">Registering Installation Information</span></span>

> [!Note]  
> <span data-ttu-id="695ff-220">Этот раздел не относится к Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="695ff-220">This section does not apply to Windows Server 2003.</span></span>

 

-   [<span data-ttu-id="695ff-221">Команда переустановки</span><span class="sxs-lookup"><span data-stu-id="695ff-221">The Reinstall Command</span></span>](#the-reinstall-command)
-   [<span data-ttu-id="695ff-222">Команда «скрыть значки»</span><span class="sxs-lookup"><span data-stu-id="695ff-222">The Hide Icons Command</span></span>](#the-hide-icons-command)
-   [<span data-ttu-id="695ff-223">Команда "отобразить значки"</span><span class="sxs-lookup"><span data-stu-id="695ff-223">The Show Icons Command</span></span>](#the-show-icons-command)
-   [<span data-ttu-id="695ff-224">Конфигурация программы группы</span><span class="sxs-lookup"><span data-stu-id="695ff-224">Group Program Configuration</span></span>](#group-program-configuration)
-   [<span data-ttu-id="695ff-225">Пример регистрации в браузере</span><span class="sxs-lookup"><span data-stu-id="695ff-225">Browser Registration Example</span></span>](#browser-registration-example)

<span data-ttu-id="695ff-226">Компонент, по которому пользователь выбирает программы по умолчанию для каждого компьютера, именуется и доступен, как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="695ff-226">The feature by which the user selects per-machine default programs is named and accessed as shown in the following table.</span></span> <span data-ttu-id="695ff-227">(В Windows Vista появилась новая функция, **устанавливающая программы по умолчанию**, с помощью которых пользователь может устанавливать параметры по умолчанию для каждого пользователя.)</span><span class="sxs-lookup"><span data-stu-id="695ff-227">(Windows Vista introduced a new feature, **Set your default programs**, by which a user can set per-user defaults.)</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="695ff-228">Операционная система</span><span class="sxs-lookup"><span data-stu-id="695ff-228">Operating System</span></span></th>
<th><span data-ttu-id="695ff-229">Заголовок</span><span class="sxs-lookup"><span data-stu-id="695ff-229">Title</span></span></th>
<th><span data-ttu-id="695ff-230">Расположение доступа</span><span class="sxs-lookup"><span data-stu-id="695ff-230">Access Location</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="695ff-231">Windows 7</span><span class="sxs-lookup"><span data-stu-id="695ff-231">Windows 7</span></span></td>
<td><span data-ttu-id="695ff-232">Настройка доступа к программе и параметров по умолчанию для компьютера</span><span class="sxs-lookup"><span data-stu-id="695ff-232">Set Program Access and Computer Defaults</span></span></td>
<td><ul>
<li><span data-ttu-id="695ff-233">Меню " <strong>Пуск</strong> " <strong>программы по умолчанию</strong></span><span class="sxs-lookup"><span data-stu-id="695ff-233"><strong>Start</strong> menu <strong>Default Programs</strong> option</span></span></li>
<li><span data-ttu-id="695ff-234"><strong>Программы по умолчанию</strong> Элемент панели управления</span><span class="sxs-lookup"><span data-stu-id="695ff-234"><strong>Default Programs</strong> Control Panel item</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="695ff-235">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="695ff-235">Windows Vista</span></span></td>
<td><span data-ttu-id="695ff-236">Настройка доступа к программе и параметров по умолчанию для компьютера</span><span class="sxs-lookup"><span data-stu-id="695ff-236">Set Program Access and Computer Defaults</span></span></td>
<td><ul>
<li><span data-ttu-id="695ff-237">Меню " <strong>Пуск</strong> " <strong>программы по умолчанию</strong></span><span class="sxs-lookup"><span data-stu-id="695ff-237"><strong>Start</strong> menu <strong>Default Programs</strong> option</span></span></li>
<li><span data-ttu-id="695ff-238"><strong>Программы по умолчанию</strong> Элемент панели управления</span><span class="sxs-lookup"><span data-stu-id="695ff-238"><strong>Default Programs</strong> Control Panel item</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="695ff-239">Windows XP с пакетом обновления 2 (SP2)</span><span class="sxs-lookup"><span data-stu-id="695ff-239">Windows XP SP2</span></span></td>
<td><span data-ttu-id="695ff-240">Настройка доступа к программам и параметров по умолчанию</span><span class="sxs-lookup"><span data-stu-id="695ff-240">Set Program Access and Defaults</span></span></td>
<td><ul>
<li><span data-ttu-id="695ff-241">Меню " <strong>Пуск</strong> "</span><span class="sxs-lookup"><span data-stu-id="695ff-241"><strong>Start</strong> menu</span></span></li>
<li><span data-ttu-id="695ff-242"><strong>Установка и удаление программ</strong> Элемент панели управления</span><span class="sxs-lookup"><span data-stu-id="695ff-242"><strong>Add or Remove Programs</strong> Control Panel item</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="695ff-243">Windows XP с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="695ff-243">Windows XP SP1</span></span></td>
<td><span data-ttu-id="695ff-244">Настройка программ</span><span class="sxs-lookup"><span data-stu-id="695ff-244">Configure Programs</span></span></td>
<td><ul>
<li><span data-ttu-id="695ff-245"><strong>Установка и удаление программ</strong> Элемент панели управления</span><span class="sxs-lookup"><span data-stu-id="695ff-245"><strong>Add or Remove Programs</strong> Control Panel item</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="695ff-246">Для простоты в этом разделе используется название функции в Windows 7.</span><span class="sxs-lookup"><span data-stu-id="695ff-246">For simplicity, this topic uses the Windows 7 title of the feature.</span></span> <span data-ttu-id="695ff-247">Все версии этой функции часто называются SPAD.</span><span class="sxs-lookup"><span data-stu-id="695ff-247">All versions of the feature are popularly referred to as SPAD.</span></span>

> [!Note]  
> <span data-ttu-id="695ff-248">Если вы используете Windows 2000 или Windows XP, необходимо установить по меньшей мере Windows 2000 SP3 или Windows XP с пакетом обновления 1 (SP1), чтобы увидеть страницу « **Настройка доступа к программам и значений по умолчанию** ».</span><span class="sxs-lookup"><span data-stu-id="695ff-248">If you are running Windows 2000 or Windows XP, you must have at least Windows 2000 SP3 or Windows XP SP1 installed to see the **Set Program Access and Defaults** page.</span></span> <span data-ttu-id="695ff-249">В Windows Vista и более поздних версиях для доступа к странице **Настройка доступа к программам и параметров по умолчанию** требуются права администратора.</span><span class="sxs-lookup"><span data-stu-id="695ff-249">In Windows Vista and later, access to the **Set Program Access and Computer Defaults** page requires Administrator privileges.</span></span> <span data-ttu-id="695ff-250">По этой причине разработчикам рекомендуется зарегистрироваться для установки элемента панели управления [программы по умолчанию](default-programs.md) , чтобы любой пользователь мог управлять параметрами приложения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="695ff-250">For this reason, developers are encouraged to register for the [Set your default programs](default-programs.md) Control Panel item so that any user can manage application defaults.</span></span>

 

<span data-ttu-id="695ff-251">В следующем дереве реестра показаны разнообразные сведения, которые должны быть зарегистрированы в ключе **инсталлинфо** программы, чтобы программа отображалась на странице **Настройка доступа к программам и параметров компьютера по умолчанию** в качестве параметра для своего типа клиента.</span><span class="sxs-lookup"><span data-stu-id="695ff-251">The following registry tree shows the variety of information that must be registered in the program's **InstallInfo** key in order for the program to appear on the **Set Program Access and Computer Defaults** page as an option for its client type.</span></span> <span data-ttu-id="695ff-252">Каждое из этих значений подробно описано в следующих разделах.</span><span class="sxs-lookup"><span data-stu-id="695ff-252">Each of these values is discussed in detail in the following sections.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
               InstallInfo
                  HideIconsCommand = command line
                  ReinstallCommand = command line
                  ShowIconsCommand = command line
                  IconsVisible = 1
```

<span data-ttu-id="695ff-253">Командная строка должна указывать полный абсолютный путь к файлу, за которым следуют дополнительные параметры командной строки.</span><span class="sxs-lookup"><span data-stu-id="695ff-253">The command line must specify a fully qualified absolute path to the file, followed by optional command-line options.</span></span> <span data-ttu-id="695ff-254">Используйте кавычки, чтобы гарантировать неправильное интерпретацию пробелов в командной строке.</span><span class="sxs-lookup"><span data-stu-id="695ff-254">Use quotation marks appropriately to ensure that spaces in the command line are not misinterpreted.</span></span>

### <a name="the-reinstall-command"></a><span data-ttu-id="695ff-255">Команда переустановки</span><span class="sxs-lookup"><span data-stu-id="695ff-255">The Reinstall Command</span></span>

<span data-ttu-id="695ff-256">Командная строка REINSTALL, объявленная в значении Реинсталлкомманд, выполняется, когда пользователь использует страницу **Настройка доступа к программам и параметров по умолчанию** , чтобы выбрать программу в качестве типа клиента по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="695ff-256">The reinstall command line declared in the ReinstallCommand value is executed when the user uses the **Set Program Access and Computer Defaults** page to select your program as the default for its client type.</span></span> <span data-ttu-id="695ff-257">В Windows Vista и более поздних версиях для доступа к этой странице требуется уровень привилегий администратора.</span><span class="sxs-lookup"><span data-stu-id="695ff-257">In Windows Vista and later, access to this page requires an Administrator privilege level.</span></span> <span data-ttu-id="695ff-258">В Windows 8, если приложение зарегистрировано с использованием того же имени, что и для **параметра задать доступ к программе и параметры по** умолчанию для компьютера и **программы по умолчанию**, то для текущего пользователя будут применены значения по умолчанию, указанные в списке **программы по умолчанию** для данного приложения, а также выполняется команда REINSTALL.</span><span class="sxs-lookup"><span data-stu-id="695ff-258">In Windows 8, if you have registered your application using the same name for both **Set Program Access and Computer Defaults** and **Default Programs**, the defaults specified in **Default Programs** for that application will be applied for the current user as well as running the reinstall command.</span></span>

<span data-ttu-id="695ff-259">Программа, запускаемая с помощью командной строки переустановки, должна связать приложение с полным набором типов [файлов](fa-intro.md) и [протоколов](/previous-versions//aa767743(v=vs.85)) , которые может выполнять приложение.</span><span class="sxs-lookup"><span data-stu-id="695ff-259">The program launched by the reinstall command line must associate the application with the complete set of [file](fa-intro.md) and [protocol](/previous-versions//aa767743(v=vs.85)) types the application can handle.</span></span> <span data-ttu-id="695ff-260">Все приложения должны устанавливать функции обработчика в команде REINSTALL.</span><span class="sxs-lookup"><span data-stu-id="695ff-260">All applications must establish handler capability in the reinstall command.</span></span> <span data-ttu-id="695ff-261">Приложения могут использовать команду REINSTALL для регистрации возможностей, а также при необходимости устанавливать состояние по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="695ff-261">Applications can use the reinstall command to register capability as well as optionally establish default status.</span></span> <span data-ttu-id="695ff-262">Если приложение решило реализовать как возможности, так и состояние обработчика по умолчанию в команде REINSTALL, оно также должно возобновить все отображаемые ссылки или ярлыки.</span><span class="sxs-lookup"><span data-stu-id="695ff-262">When an application chooses to implement both capability and default handler status in the reinstall command, it should also reinstate any visible links or shortcuts desired.</span></span> <span data-ttu-id="695ff-263">Видимые точки входа большинство приложений выбираются в списке в [команде скрыть значки](#the-hide-icons-command).</span><span class="sxs-lookup"><span data-stu-id="695ff-263">The visible entry points most applications choose are listed in [The Hide Icons Command](#the-hide-icons-command).</span></span>

> [!Note]  
> <span data-ttu-id="695ff-264">Настоятельно рекомендуется, чтобы приложения реализовали возможности обработки в команде REINSTALL.</span><span class="sxs-lookup"><span data-stu-id="695ff-264">It is highly recommended that applications implement handling capability in the reinstall command.</span></span>

 

<span data-ttu-id="695ff-265">После завершения переустановки программа, запускаемая командной строкой переустановки, должна выйти из программы.</span><span class="sxs-lookup"><span data-stu-id="695ff-265">Once the reinstall process is complete, the program launched by the reinstall command line should exit.</span></span> <span data-ttu-id="695ff-266">Он не должен запускать соответствующую программу; Он должен просто регистрировать значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="695ff-266">It should not launch the corresponding program; it should merely register defaults.</span></span> <span data-ttu-id="695ff-267">Например, команда переустановки браузера не должна открывать домашнюю страницу пользователя.</span><span class="sxs-lookup"><span data-stu-id="695ff-267">For example, the reinstall command for a browser should not open the user's home page.</span></span>

> [!Note]  
> <span data-ttu-id="695ff-268">Для клиентов браузера и электронной почты в Windows XP и Windows Vista в верхней части меню "Пуск" для приложений, которые устанавливают возможность обработки и состояния по умолчанию, необходимо зарегистрироваться для получения соответствующего значка.</span><span class="sxs-lookup"><span data-stu-id="695ff-268">For browser and email clients in Windows XP and Windows Vista, applications that choose to establish both handling capability and default status in the reinstall command should register for the corresponding icon at the top of the Start menu.</span></span> <span data-ttu-id="695ff-269">Дополнительные сведения см. в разделе [Регистрация меню "Пуск](#start-menu-registration) ".</span><span class="sxs-lookup"><span data-stu-id="695ff-269">See [Start Menu Registration](#start-menu-registration) for additional information.</span></span>

 

### <a name="the-hide-icons-command"></a><span data-ttu-id="695ff-270">Команда «скрыть значки»</span><span class="sxs-lookup"><span data-stu-id="695ff-270">The Hide Icons Command</span></span>

<span data-ttu-id="695ff-271">Командная строка, объявленная в значении Хидеиконскомманд, выполняется, когда пользователь очищает поле **Разрешить доступ к этой программе** на странице **Настройка доступа к программам и параметров компьютера по умолчанию** .</span><span class="sxs-lookup"><span data-stu-id="695ff-271">The command line declared in the HideIconsCommand value is executed when the user clears the **Enable access to this program** box in the **Set Program Access and Computer Defaults** page.</span></span> <span data-ttu-id="695ff-272">Эта командная строка должна скрывать все точки доступа программы, которые видны в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="695ff-272">This command line must hide all of your program's access points that are visible in the user interface.</span></span> <span data-ttu-id="695ff-273">Конкретные рекомендации предназначены для удаления ярлыков и значков из следующих расположений:</span><span class="sxs-lookup"><span data-stu-id="695ff-273">The specific guidelines are to remove shortcuts and icons from the following locations:</span></span>

-   <span data-ttu-id="695ff-274">Значки рабочего стола</span><span class="sxs-lookup"><span data-stu-id="695ff-274">Desktop icons</span></span>
-   <span data-ttu-id="695ff-275">Ссылки меню "Пуск", включая группу **автозагрузки**</span><span class="sxs-lookup"><span data-stu-id="695ff-275">Start menu links, including the **Startup** group</span></span>
-   <span data-ttu-id="695ff-276">Ссылки на панели быстрого запуска</span><span class="sxs-lookup"><span data-stu-id="695ff-276">Quick Launch bar links</span></span>
-   <span data-ttu-id="695ff-277">Область "Уведомления"</span><span class="sxs-lookup"><span data-stu-id="695ff-277">Notification area</span></span>
-   <span data-ttu-id="695ff-278">Контекстные меню</span><span class="sxs-lookup"><span data-stu-id="695ff-278">Shortcut menus</span></span>
-   <span data-ttu-id="695ff-279">Полоса задач для папки</span><span class="sxs-lookup"><span data-stu-id="695ff-279">Folder task band</span></span>

<span data-ttu-id="695ff-280">Эта командная строка также должна препятствовать автоматическому вызову программы, например указанным в разделе **Run** реестра.</span><span class="sxs-lookup"><span data-stu-id="695ff-280">This command line must also prevent automatic invocations of the program, such as those specified in the **Run** registry key.</span></span> <span data-ttu-id="695ff-281">Поставщикам рекомендуется реализовать эти рекомендации в обратном вызове функции скрытия доступа приложения.</span><span class="sxs-lookup"><span data-stu-id="695ff-281">Vendors are encouraged to implement these guidelines in the application's Hide Access callback.</span></span>

<span data-ttu-id="695ff-282">При скрытии значков не требуется повторная регистрация (возможность приложения) типов файлов.</span><span class="sxs-lookup"><span data-stu-id="695ff-282">You do not need to relinquish registration (application capability) of file types when icons are hidden.</span></span> <span data-ttu-id="695ff-283">Кроме того, не нужно освобождать состояние приложения по умолчанию для типов файлов и протоколов.</span><span class="sxs-lookup"><span data-stu-id="695ff-283">You also do not need to relinquish the application's default status for file and protocol types.</span></span> <span data-ttu-id="695ff-284">Это может привести к неправильному взаимодействиям с пользователем при обнаружении этих типов в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="695ff-284">Doing so can lead to a bad user experience when these types are encountered in the UI.</span></span>

<span data-ttu-id="695ff-285">После успешного скрытия значков необходимо изменить значение реестра Иконсвисибле на 0, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="695ff-285">After successfully hiding icons, you must update the IconsVisible registry value to 0 as shown:</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
               InstallInfo
                  IconsVisible = 0
```

<span data-ttu-id="695ff-286">Запись Иконсвисибле имеет тип **reg \_ DWORD**.</span><span class="sxs-lookup"><span data-stu-id="695ff-286">The IconsVisible entry is of type **REG\_DWORD**.</span></span>

### <a name="an-alternate-hide-icons-method-in-spad"></a><span data-ttu-id="695ff-287">Альтернативный метод скрытия значков в SPAD</span><span class="sxs-lookup"><span data-stu-id="695ff-287">An Alternate Hide Icons Method in SPAD</span></span>

<span data-ttu-id="695ff-288">Для некоторых устаревших приложений полная реализация скрытия доступа может оказаться непрактичной.</span><span class="sxs-lookup"><span data-stu-id="695ff-288">For some legacy applications, a full implementation of Hide Access may not be practical.</span></span> <span data-ttu-id="695ff-289">Альтернативным методом, который достигает того же результата, является удаление приложения.</span><span class="sxs-lookup"><span data-stu-id="695ff-289">An alternative method that achieves the same effect is to uninstall the application.</span></span> <span data-ttu-id="695ff-290">В разделе ниже показан пример поведения и примеры кода для реализации этой альтернативы.</span><span class="sxs-lookup"><span data-stu-id="695ff-290">The section below shows example behavior and sample code to implement this alternative.</span></span> <span data-ttu-id="695ff-291">В общем случае независимые поставщики программного обеспечения не должны использовать эту альтернативу, так как она будет:</span><span class="sxs-lookup"><span data-stu-id="695ff-291">In general, independent software vendors (ISVs) should avoid this alternative since it will:</span></span>

-   <span data-ttu-id="695ff-292">Полностью удалите приложение из системы.</span><span class="sxs-lookup"><span data-stu-id="695ff-292">Uninstall the application completely from the system.</span></span>
-   <span data-ttu-id="695ff-293">Удалить ранее выбранные значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="695ff-293">Remove previously selected defaults.</span></span>
-   <span data-ttu-id="695ff-294">Не устанавливайте параметр UI, чтобы переустановить приложение.</span><span class="sxs-lookup"><span data-stu-id="695ff-294">Leave no UI option to reinstall the application.</span></span>
-   <span data-ttu-id="695ff-295">Сделать функцию "включить доступ" более недоступной, так как удаление полностью удаляет приложение из SPAD.</span><span class="sxs-lookup"><span data-stu-id="695ff-295">Make the enable access feature no longer available, since an uninstallation removes the application completely from SPAD.</span></span>

<span data-ttu-id="695ff-296">Рекомендуемый пользовательский интерфейс выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="695ff-296">The recommended user experience is as follows:</span></span>

-   <span data-ttu-id="695ff-297">Когда пользователь снимает флажок **включить доступ к этой программе** в SPAD, отображается следующий пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="695ff-297">When the user unchecks the **Enable access to this program** box in SPAD, the following UI is presented.</span></span>

    ![диалоговое окно "Скрытие доступа к программе"](images/hideaccessvista.png)

-   <span data-ttu-id="695ff-299">Когда пользователь нажмет **кнопку ОК**, запускается элемент Панель управления **программы и компоненты** , позволяющий пользователю удалить приложение.</span><span class="sxs-lookup"><span data-stu-id="695ff-299">When the user selects **OK**, the **Programs and Features** Control Panel item launches to allow the user to uninstall the application.</span></span>
-   <span data-ttu-id="695ff-300">Пользователи Windows XP должны быть представлены в этом диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="695ff-300">Windows XP users should be presented with this dialog box.</span></span>

    ![эквивалентное диалоговое окно Windows XP](images/hideaccessxp.png)

-   <span data-ttu-id="695ff-302">После нажатия **кнопки ОК** пользователем Windows XP запускается элемент панели управления **Установка и удаление программ** , позволяющий пользователю удалить приложение.</span><span class="sxs-lookup"><span data-stu-id="695ff-302">When the Windows XP user selects **OK**, the **Add or Remove Programs** Control Panel item launches to allow the user to uninstall the application.</span></span>

<span data-ttu-id="695ff-303">Следующий код предоставляет многократно используемую реализацию функции скрытия доступа, как описано выше.</span><span class="sxs-lookup"><span data-stu-id="695ff-303">The following code provides a reusable implementation for the Hide Access feature as outlined above.</span></span> <span data-ttu-id="695ff-304">Его можно использовать в Windows XP, Windows Vista и Windows 7.</span><span class="sxs-lookup"><span data-stu-id="695ff-304">It can be used on Windows XP, Windows Vista, and Windows 7.</span></span>


```
#include <windows.h>
#include <shlwapi.h>
#include <strsafe.h>

PCWSTR c_pszMessage1 = L"To hide access to this program, you need to uninstall it by ";
PCWSTR c_pszMessage2 = L"using\n%s in Control Panel.\n\nWould you like to start %s?";
PCWSTR c_pszApplicationName  = L"Sample App";

int _tmain(int argc, WCHAR* argv[])
{
    OSVERSIONINFO version;
    version.dwOSVersionInfoSize = sizeof(version);

    if (GetVersionEx(&version))
    {
        PCWSTR pszCPLName = NULL;

        if (version.dwMajorVersion >= 6)
        {
            // Windows Vista and later
            pszCPLName = L"Programs and Features";
        }
        else if (version.dwMajorVersion == 5 &&
                 version.dwMinorVersion == 1)
        {
            // Windows XP
            pszCPLName = L"Add/Remove Programs";
        }

        if (pszCPLName != NULL)
        {
            WCHAR szMessage[256], szScratch[256];
            if (SUCCEEDED(StringCchPrintf(szScratch, 
                                          ARRAYSIZE(szScratch), 
                                          c_pszMessage2, 
                                          pszCPLName, 
                                          pszCPLName)))
            {
                if (SUCCEEDED(StringCchCopy(szMessage, 
                                            ARRAYSIZE(szMessage), 
                                            c_pszMessage1)))
                {
                    if (SUCCEEDED(StringCchCat(szMessage, 
                                               ARRAYSIZE(szMessage), 
                                               szScratch)))
                    {
                        if (IDOK == MessageBox(NULL, 
                                               szMessage, 
                                               c_pszApplicationName, 
                                               MB_OKCANCEL))
                        {
                            ShellExecute(NULL, 
                                         NULL, 
                                         L"appwiz.cpl", 
                                         NULL, 
                                         NULL, 
                                         SW_SHOWNORMAL);
                        }
                    }
                }
            }
        }
    }
    return 0;
}
```



### <a name="the-show-icons-command"></a><span data-ttu-id="695ff-305">Команда "отобразить значки"</span><span class="sxs-lookup"><span data-stu-id="695ff-305">The Show Icons Command</span></span>

<span data-ttu-id="695ff-306">Командная строка, объявленная в записи Шовиконскомманд, выполняется, когда пользователь устанавливает флажок **включить доступ к этой программе** на странице **Настройка доступа к программам и параметров компьютера по умолчанию** .</span><span class="sxs-lookup"><span data-stu-id="695ff-306">The command line declared in the ShowIconsCommand entry is executed when the user checks the **Enable access to this program** box in the **Set Program Access and Computer Defaults** page.</span></span> <span data-ttu-id="695ff-307">Эта командная строка может восстановить точки доступа программы, включая те, что находятся в меню " **Пуск** ", на рабочем столе и в группе **автозагрузки** , а также в обычных автоматических вызовах, таких как указанные в разделе " **Запуск** реестра".</span><span class="sxs-lookup"><span data-stu-id="695ff-307">This command line may restore your program's access points, including those in the **Start** menu, on the desktop, and in the **Startup** group, as well as normal automatic invocations, such as those specified in the **Run** registry key.</span></span> <span data-ttu-id="695ff-308">Видимые точки доступа, представляющие интерес для большинства приложений, перечислены в [команде скрыть значки](#the-hide-icons-command).</span><span class="sxs-lookup"><span data-stu-id="695ff-308">The visible access points of interest to most applications are listed in [The Hide Icons Command](#the-hide-icons-command).</span></span> <span data-ttu-id="695ff-309">Приложение не должно изменять значения по умолчанию для каждого пользователя; Это изменение должно выполняться пользователем с помощью **программ по умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="695ff-309">The application should not change per-user defaults; that change should be done by the user through **Default Programs**.</span></span>

<span data-ttu-id="695ff-310">После успешного отображения значков необходимо изменить значение реестра Иконсвисибле на 1, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="695ff-310">After successfully showing your icons, you must update the IconsVisible registry value to 1 as shown:</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
               InstallInfo
                  IconsVisible = 1
```

<span data-ttu-id="695ff-311">Обратите внимание, что если вы использовали запись Хидеиконскомманд для запроса удаления приложения, запись Шовиконскомманд не используется.</span><span class="sxs-lookup"><span data-stu-id="695ff-311">Note that if you have used the HideIconsCommand entry to prompt an uninstall of the application, the ShowIconsCommand entry is of no use.</span></span> <span data-ttu-id="695ff-312">Он должен быть удален из реестра с остальными сведениями о приложении в процессе удаления.</span><span class="sxs-lookup"><span data-stu-id="695ff-312">It should be removed from the registry with the rest of the application's information during the uninstall process.</span></span>

### <a name="group-program-configuration"></a><span data-ttu-id="695ff-313">Конфигурация программы группы</span><span class="sxs-lookup"><span data-stu-id="695ff-313">Group Program Configuration</span></span>

> [!Note]  
> <span data-ttu-id="695ff-314">Этот раздел не относится к Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="695ff-314">This section does not apply to Windows 2000.</span></span>

 

<span data-ttu-id="695ff-315">В процессе подготовки системы изготовитель оборудования может установить конфигурацию, которая скрывает точки доступа для браузера, электронной почты, воспроизведения мультимедиа, обмена мгновенными сообщениями или виртуальной машины для клиентских программ Java и задает собственные программы по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="695ff-315">As part of system preparation, an OEM can establish a configuration that hides access points for the Microsoft browser, email, media playback, instant messaging, or virtual machine for Java client programs and specifies their own default programs.</span></span> <span data-ttu-id="695ff-316">Изготовители оборудования могут разрешить пользователям сбрасывать свои компьютеры в любое время до этой конфигурации по умолчанию, задав следующие значения реестра.</span><span class="sxs-lookup"><span data-stu-id="695ff-316">OEMs can enable users to reset their computers at any time to this default configuration by setting the following registry values.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
               InstallInfo
                  OEMShowIcons = 1
                  OEMDefault = 1
```

<span data-ttu-id="695ff-317">Если эти ключи установлены, пользователи могут восстановить конфигурацию изготовителя оборудования, выбрав параметр **Изготовитель компьютера** на странице **Настройка доступа к программам и параметров компьютера по умолчанию** .</span><span class="sxs-lookup"><span data-stu-id="695ff-317">If these keys are set, users can restore the OEM configuration by selecting the **Computer Manufacturer** option on the **Set Program Access and Computer Defaults** page.</span></span> <span data-ttu-id="695ff-318">Если эти ключи не заданы, параметр **Изготовитель компьютера** не отображается.</span><span class="sxs-lookup"><span data-stu-id="695ff-318">If these keys are not set, the **Computer Manufacturer** option is not shown.</span></span>

<span data-ttu-id="695ff-319">Запись **оемшовиконс** , если она есть, устанавливает значок отображения состояния для указанного клиента, который применяется, если пользователь выбирает **изготовителя компьютера**.</span><span class="sxs-lookup"><span data-stu-id="695ff-319">The **OEMShowIcons** entry, if present, sets the icon show state for the specified client that is applied if the user selects **Computer Manufacturer**.</span></span> <span data-ttu-id="695ff-320">Значение 1 приводит к отображению значков, а значение 0 приводит к тому, что значки не отображаются.</span><span class="sxs-lookup"><span data-stu-id="695ff-320">A value of 1 causes icons to be shown, and a value of 0 causes icons to not be shown.</span></span> <span data-ttu-id="695ff-321">Если **оемшовиконс** отсутствует, выбор параметра " **Изготовитель компьютера** " не влияет на значок "отобразить параметр".</span><span class="sxs-lookup"><span data-stu-id="695ff-321">If **OEMShowIcons** is absent, selecting **Computer Manufacturer** has no effect on the icon show setting.</span></span> <span data-ttu-id="695ff-322">**Оемшовиконс** имеет тип **reg \_ DWORD**.</span><span class="sxs-lookup"><span data-stu-id="695ff-322">**OEMShowIcons** is of type **REG\_DWORD**.</span></span>

<span data-ttu-id="695ff-323">Запись **оемдефаулт** , если она имеется и имеет значение 1, устанавливает OEM-предпочтение для клиента по умолчанию указанного типа.</span><span class="sxs-lookup"><span data-stu-id="695ff-323">The **OEMDefault** entry, if present and set to 1, establishes the OEM preference for the default client of the indicated type.</span></span> <span data-ttu-id="695ff-324">Только один клиент определенного типа может быть помечен как OEM по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="695ff-324">Only one client of a particular type can be marked as the OEM default.</span></span> <span data-ttu-id="695ff-325">Если более чем одна регистрация клиента содержит запись **оемдефаулт** , то все они игнорируются, а текущий клиент по умолчанию будет использоваться в качестве клиента.</span><span class="sxs-lookup"><span data-stu-id="695ff-325">If more then one client's registration contains the **OEMDefault** entry, then all are ignored and the current client continues to be used as default client.</span></span> <span data-ttu-id="695ff-326">Если запись **оемдефаулт** отсутствует или имеет значение 0, то этот конкретный клиент не используется в качестве клиента по умолчанию, если пользователь выбрал **изготовителя компьютера**.</span><span class="sxs-lookup"><span data-stu-id="695ff-326">If the **OEMDefault** entry is not present or is present and set to 0, then that particular client is not used as the default client if the user selects **Computer Manufacturer**.</span></span> <span data-ttu-id="695ff-327">**Оемдефаулт** имеет тип **reg \_ DWORD**.</span><span class="sxs-lookup"><span data-stu-id="695ff-327">**OEMDefault** is of type **REG\_DWORD**.</span></span>

<span data-ttu-id="695ff-328">Помимо возможности сброса компьютеров к конфигурации по умолчанию, установленной поставщиком вычислительной техники, пользователи имеют три других варианта настройки:</span><span class="sxs-lookup"><span data-stu-id="695ff-328">In addition to the option to reset their computers to the default configuration established by the OEM, users have three other configuration options:</span></span>

-   <span data-ttu-id="695ff-329">Задайте для компьютера конфигурацию Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="695ff-329">Set their computer to a Microsoft Windows configuration.</span></span> <span data-ttu-id="695ff-330">В этом случае страница « **Настройка доступа к программам и параметров по умолчанию** » обеспечивает доступ ко всем программам Майкрософт и сторонних разработчиков на компьютере, зарегистрированном в соответствующих категориях продуктов.</span><span class="sxs-lookup"><span data-stu-id="695ff-330">In this case, the **Set Program Access and Computer Defaults** page enables access to all Microsoft and non-Microsoft software on the computer registered in the relevant product categories.</span></span> <span data-ttu-id="695ff-331">Для каждой категории выбран параметр программы Microsoft Windows по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="695ff-331">Microsoft Windows programs are selected as the default option for each category.</span></span>
-   <span data-ttu-id="695ff-332">Задайте для компьютера конфигурацию, не связанную с Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="695ff-332">Set their computer to a non-Microsoft configuration.</span></span> <span data-ttu-id="695ff-333">Эта конфигурация скрывает точки доступа (например, меню " **Пуск** ") к Windows Internet Explorer, проигрывателю Windows Media, Windows Messenger и Microsoft Outlook Express.</span><span class="sxs-lookup"><span data-stu-id="695ff-333">This configuration hides access points (such as the **Start** menu) to Windows Internet Explorer, Windows Media Player, Windows Messenger, and Microsoft Outlook Express.</span></span> <span data-ttu-id="695ff-334">Он обеспечивает доступ к программному обеспечению, не являющемуся Майкрософт, на компьютере в этих категориях.</span><span class="sxs-lookup"><span data-stu-id="695ff-334">It enables access to the non-Microsoft software on the computer in these categories.</span></span> <span data-ttu-id="695ff-335">Кроме того, если в категории имеется программа, не относящаяся к корпорации Майкрософт, она задается в качестве по умолчанию для этой категории.</span><span class="sxs-lookup"><span data-stu-id="695ff-335">Furthermore, if a non-Microsoft program is available in a category, it is set as the default for that category.</span></span> <span data-ttu-id="695ff-336">Если в категории доступно более одной программы, отличной от Майкрософт, пользователю предлагается выбрать, какую программу не следует использовать по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="695ff-336">If more than one non-Microsoft program is available in a category, the user is asked to choose which non-Microsoft program should be used as the default.</span></span>
-   <span data-ttu-id="695ff-337">Установите пользовательскую конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="695ff-337">Establish a custom configuration.</span></span> <span data-ttu-id="695ff-338">Пользователи могут выбирать собственные параметры для включения или удаления доступа, совместного применения программ Майкрософт и сторонних разработчиков по мере их появлении.</span><span class="sxs-lookup"><span data-stu-id="695ff-338">Users make their own selections for enabling or removing access, mixing Microsoft and non-Microsoft programs as they see fit.</span></span> <span data-ttu-id="695ff-339">Пользователи устанавливают параметры по умолчанию для отдельных категорий.</span><span class="sxs-lookup"><span data-stu-id="695ff-339">Users establish default options on a category-by-category basis.</span></span>

<span data-ttu-id="695ff-340">В любое время пользователи могут изменять любые из этих параметров.</span><span class="sxs-lookup"><span data-stu-id="695ff-340">Users are free to change any of these options at any time.</span></span>

### <a name="browser-registration-example"></a><span data-ttu-id="695ff-341">Пример регистрации в браузере</span><span class="sxs-lookup"><span data-stu-id="695ff-341">Browser Registration Example</span></span>

<span data-ttu-id="695ff-342">В следующем примере показана полная регистрация **инсталлинфо** для вымышленного обозревателя представления освещенности.</span><span class="sxs-lookup"><span data-stu-id="695ff-342">The following example shows the full **InstallInfo** registration for a fictional Lit View browser.</span></span> <span data-ttu-id="695ff-343">В этом случае параметры командной строки позволяют файлу Litview.exe выполнять любые действия, необходимые для каждого значения.</span><span class="sxs-lookup"><span data-stu-id="695ff-343">In this case the command line switches allow the Litview.exe file to perform whatever actions are necessary for each value.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         StartMenuInternet
            LITVIEW.EXE
               InstallInfo
                  ReinstallCommand = "C:\Program Files\LitwareInc\Litview.exe" /reinstall
                  HideIconsCommand = "C:\Program Files\LitwareInc\Litview.exe" /hideicons
                  ShowIconsCommand = "C:\Program Files\LitwareInc\Litview.exe" /showicons
                  IconsVisible = 1
```

<span data-ttu-id="695ff-344">Обратите внимание, что кавычки размещаются вокруг путей, так как они содержат внедренные пробелы.</span><span class="sxs-lookup"><span data-stu-id="695ff-344">Note that quotation marks are placed around the paths because they contain embedded spaces.</span></span>

## <a name="registration-elements-for-specific-client-types"></a><span data-ttu-id="695ff-345">Элементы регистрации для конкретных типов клиентов</span><span class="sxs-lookup"><span data-stu-id="695ff-345">Registration Elements for Specific Client Types</span></span>

<span data-ttu-id="695ff-346">Следующие сведения также можно найти в ресурсах, перечисленных в разделе связанные разделы в конце этого раздела.</span><span class="sxs-lookup"><span data-stu-id="695ff-346">The following information also can be found in the resources listed in the Related Topics section at the end of this topic.</span></span>

-   [<span data-ttu-id="695ff-347">Регистрация в меню "Пуск"</span><span class="sxs-lookup"><span data-stu-id="695ff-347">Start Menu Registration</span></span>](#start-menu-registration)
-   [<span data-ttu-id="695ff-348">Регистрация почтового клиента</span><span class="sxs-lookup"><span data-stu-id="695ff-348">Mail Client Registration</span></span>](#mail-client-registration)

### <a name="start-menu-registration"></a><span data-ttu-id="695ff-349">Регистрация в меню "Пуск"</span><span class="sxs-lookup"><span data-stu-id="695ff-349">Start Menu Registration</span></span>

<span data-ttu-id="695ff-350">В Windows XP приложения, как правило, зарегистрированы по умолчанию на уровне компьютера (на **\_ локальном \_ компьютере**), а не в области пользователя (**hKey \_ текущий \_ пользователь**).</span><span class="sxs-lookup"><span data-stu-id="695ff-350">Under Windows XP, applications typically registered defaults on a machine-wide (**HKEY\_LOCAL\_MACHINE**) rather than a user (**HKEY\_CURRENT\_USER**) scope.</span></span> <span data-ttu-id="695ff-351">С появлением контроля учетных записей (UAC) в Windows Vista приложения, которые заявляют **Интернет** и слоты **электронной почты** в меню " **Пуск** ", должны реализовать команду переустановки в правильном контексте выполнения.</span><span class="sxs-lookup"><span data-stu-id="695ff-351">With the Windows Vista introduction of the User Account Control (UAC), applications that claim the **Internet** and **E-mail** slots in the **Start** menu must implement the reinstall command within the correct execution context.</span></span>

> [!Note]  
> <span data-ttu-id="695ff-352">Ссылка на **электронную почту** меню "Пуск" была удалена в Windows 7.</span><span class="sxs-lookup"><span data-stu-id="695ff-352">The Start menu **E-mail** link has been removed as of Windows 7.</span></span> <span data-ttu-id="695ff-353">Однако регистрация, обсуждаемая в этом разделе, по-прежнему должна быть выполнена, так как назначает клиент MAPI по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="695ff-353">However, the registration discussed in this section should still be performed because it assigns the default MAPI client.</span></span>

 

<span data-ttu-id="695ff-354">Ограниченный пользователь в Windows XP, Windows Vista или Windows 7 не может получить доступ к SPAD.</span><span class="sxs-lookup"><span data-stu-id="695ff-354">A limited user on Windows XP, Windows Vista, or Windows 7 cannot access SPAD.</span></span> <span data-ttu-id="695ff-355">По этой причине разработчикам рекомендуется зарегистрироваться для установки элемента панели управления " **программы по умолчанию** ", чтобы любой пользователь мог управлять параметрами по умолчанию приложения для каждого пользователя.</span><span class="sxs-lookup"><span data-stu-id="695ff-355">For this reason, developers are encouraged to register for the **Set your default programs** Control Panel item so that any user can manage per-user application defaults.</span></span>

<span data-ttu-id="695ff-356">Выбор, сделанный в SPAD, должен влиять только на параметры компьютера.</span><span class="sxs-lookup"><span data-stu-id="695ff-356">Selections made in SPAD should only affect per-machine settings.</span></span>

<span data-ttu-id="695ff-357">Задайте значение реестра следующим образом.</span><span class="sxs-lookup"><span data-stu-id="695ff-357">Set the registry value as follows.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            (Default) = CanonicalName
```

> [!Note]
> 
> <span data-ttu-id="695ff-358">**Приведенные ниже сведения относятся только к Windows XP.**</span><span class="sxs-lookup"><span data-stu-id="695ff-358">**The following information applies to Windows XP only.**</span></span>
> 
> <span data-ttu-id="695ff-359">Если регистрация по умолчанию на уровне компьютера в разделе HKEY " \_ локальный \_ компьютер" прошла успешно, приложение должно удалить значение, присвоенное записи по умолчанию в следующем подразделе:</span><span class="sxs-lookup"><span data-stu-id="695ff-359">If the registration of the computer-level default under HKEY\_LOCAL\_MACHINE as shown above is successful, the application should delete the value assigned to the Default entry under the following subkey:</span></span>
> 
> ```
> HKEY_CURRENT_USER
>    SOFTWARE
>       Clients
>          ClientTypeName
> ```
> 
> <span data-ttu-id="695ff-360">Если при регистрации по умолчанию на уровне компьютера в разделе HKEY \_ локальный \_ компьютер происходит сбой, как правило, потому, что пользователь не имеет разрешения на запись в подразделе, приложение должно установить следующее значение:</span><span class="sxs-lookup"><span data-stu-id="695ff-360">If the registration of the computer-level default under HKEY\_LOCAL\_MACHINE as shown above fails, usually because the user does not have write permission to the subkey, the application should set the following value:</span></span>
> 
> ```
> HKEY_CURRENT_USER
>    SOFTWARE
>       Clients
>          ClientTypeName
>             (Default) = CanonicalName
> ```
> 
> <span data-ttu-id="695ff-361">Он регистрирует каноническое имя только для текущего пользователя, а не для всех пользователей.</span><span class="sxs-lookup"><span data-stu-id="695ff-361">This registers the canonical name only for the current user, not for all users.</span></span>

 

<span data-ttu-id="695ff-362">После обновления разделов реестра программа должна выполнить широковещательную рассылку сообщения [**WM \_ сеттингчанже**](../winmsg/wm-settingchange.md) с параметром **wParam** = 0 и **lParam** , указывающим на строку "Software Clients клиенттипенаме, заканчивающуюся нулем" \\ \\ , чтобы уведомить операционную систему об изменении клиента по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="695ff-362">After updating the registry keys, the program should broadcast the [**WM\_SETTINGCHANGE**](../winmsg/wm-settingchange.md) message with **wParam** = 0 and **lParam** pointing to the null-terminated string "Software\\Clients\\**ClientTypeName**" to notify the operating system that the default client has changed.</span></span>

### <a name="mail-client-registration"></a><span data-ttu-id="695ff-363">Регистрация почтового клиента</span><span class="sxs-lookup"><span data-stu-id="695ff-363">Mail Client Registration</span></span>

<span data-ttu-id="695ff-364">Для почтового клиента программе необходимо зарегистрировать параметры в **\_ \_ корневом разделе "классы hKey**", \\  чтобы использовать URL-адреса, использующие `mailto` протокол.</span><span class="sxs-lookup"><span data-stu-id="695ff-364">For a mail client, the program needs to have registered settings under the **HKEY\_CLASSES\_ROOT**\\**mailto** key in order to service URLs that use the `mailto` protocol.</span></span> <span data-ttu-id="695ff-365">Задайте значения и ключи, отражающие эти параметры в следующем разделе.</span><span class="sxs-lookup"><span data-stu-id="695ff-365">Set values and keys that mirror those settings under the following key.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         Mail
            CanonicalName
               Protocols
                  mailto
```

<span data-ttu-id="695ff-366">Эта иерархия реестра заменяет существующую `mailto` иерархию реестра, найденную в разделе **\_ классы hKey \_ root** \\ **mailto**.</span><span class="sxs-lookup"><span data-stu-id="695ff-366">This registry hierarchy replaces the existing `mailto` registry hierarchy found at **HKEY\_CLASSES\_ROOT**\\**mailto**.</span></span> <span data-ttu-id="695ff-367">Иерархия остается неизменной, изменилось только расположение.</span><span class="sxs-lookup"><span data-stu-id="695ff-367">The hierarchy remains the same, only the location has changed.</span></span> <span data-ttu-id="695ff-368">Формат этой иерархии описан на сайте MSDN в разделе [Обзор асинхронных подключаемых протоколов и учебников](/previous-versions//aa767913(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="695ff-368">The format of this hierarchy is documented on MSDN under [Asynchronous Pluggable Protocol Overviews and Tutorials](/previous-versions//aa767913(v=vs.85)).</span></span> <span data-ttu-id="695ff-369">Обычно `mailto` протокол регистрируется в программе, а не в асинхронном протоколе. в этом случае применяется документация по [регистрации приложения в схеме универсального кода ресурса (URI)](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767914(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="695ff-369">Typically, the `mailto` protocol is registered to a program rather than an asynchronous protocol, in which case the documentation on [Registering an Application to a URI Scheme](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767914(v=vs.85)) applies.</span></span>

<span data-ttu-id="695ff-370">В следующем примере показан `mailto` раздел регистрации `mailto` обработчика, зарегистрированного в программе.</span><span class="sxs-lookup"><span data-stu-id="695ff-370">The following example shows the `mailto` section of the registration for a `mailto` handler registered to a program.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         Mail
            CanonicalName
               Protocols
                  mailto
                     (Default) = URL:MailTo Protocol
                     EditFlags = 02 00 00 00
                     URL Protocol
                     DefaultIcon
                        (Default) = %FilePath%,IconIndex
                     shell
                        open
                           command
                              (Default) = command line
```

<span data-ttu-id="695ff-371">Значение реестра Едитфлагс описано в разделе « [типы файлов](fa-file-types.md) » раздела «Определение атрибутов типа файла».</span><span class="sxs-lookup"><span data-stu-id="695ff-371">The EditFlags registry value is documented in [File Types](fa-file-types.md) in the section titled "Defining File Type Attributes."</span></span>

## <a name="complete-sample-registrations"></a><span data-ttu-id="695ff-372">Полные примеры регистраций</span><span class="sxs-lookup"><span data-stu-id="695ff-372">Complete Sample Registrations</span></span>

<span data-ttu-id="695ff-373">Ниже приведены примеры, в которых показаны полные требования к регистрации для различных типов клиентов.</span><span class="sxs-lookup"><span data-stu-id="695ff-373">The following examples are provided to show the complete registration requirements for the various client types.</span></span>

-   [<span data-ttu-id="695ff-374">Пример браузера</span><span class="sxs-lookup"><span data-stu-id="695ff-374">A Sample Browser</span></span>](#a-sample-browser)
-   [<span data-ttu-id="695ff-375">Пример почтового браузера</span><span class="sxs-lookup"><span data-stu-id="695ff-375">A Sample Mail Browser</span></span>](#a-sample-mail-browser)
-   [<span data-ttu-id="695ff-376">Пример проигрывателя мультимедиа</span><span class="sxs-lookup"><span data-stu-id="695ff-376">A Sample Media Player</span></span>](#a-sample-media-player)
-   [<span data-ttu-id="695ff-377">Пример программы мгновенных сообщений</span><span class="sxs-lookup"><span data-stu-id="695ff-377">A Sample Instant Messenger Program</span></span>](#a-sample-instant-messenger-program)
-   [<span data-ttu-id="695ff-378">Пример виртуальной машины для Java</span><span class="sxs-lookup"><span data-stu-id="695ff-378">A Sample Virtual Machine for Java</span></span>](#a-sample-virtual-machine-for-java)

### <a name="a-sample-browser"></a><span data-ttu-id="695ff-379">Пример браузера</span><span class="sxs-lookup"><span data-stu-id="695ff-379">A Sample Browser</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         StartMenuInternet
            LITVIEW.EXE
               (Default) = Lit View
               LocalizedString = @C:\Program Files\LitwareInc\ResourceDLL.dll,-123
               DefaultIcon
                  (Default) = C:\Program Files\LitwareInc\LITVIEW.EXE,1
               InstallInfo
                  ReinstallCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /reinstall
                  HideIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /hideicons
                  ShowIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /showicons
                  IconsVisible = 1
                  shell
                     open
                        command
                           (Default) = "C:\Program Files\LitwareInc\LITVIEW.EXE" /homepage
```

### <a name="a-sample-mail-browser"></a><span data-ttu-id="695ff-380">Пример почтового браузера</span><span class="sxs-lookup"><span data-stu-id="695ff-380">A Sample Mail Browser</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         Mail
            Lit View
               (Default) = Lit View
               DLLPath = @C:\Program Files\LItwareInc\LitwareMAPI.dll
               LocalizedString = @C:\Program Files\LitwareInc\ResourceDLL.dll,-123
               DefaultIcon
                  (Default) = C:\Program Files\LitwareInc\LITVIEW.EXE,1
               InstallInfo
                  ReinstallCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /reinstall
                  HideIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /hideicons
                  ShowIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /showicons
                  IconsVisible = 1
               shell
                  open
                     command
                        (Default) = "C:\Program Files\LitwareInc\LITVIEW.EXE" /inbox
               protocols
                  mailto
                     (Default) = URL:MailTo Protocol
                     EditFlags = 02 00 00 00
                     URL Protocol
                     DefaultIcon
                        (Default) = C:\Program Files\LitwareInc\LITVIEW.EXE,1
                     shell
                        open
                           command
                              (Default) = "C:\Program Files\LitwareInc\LITVIEW.EXE" /mailto:%1
```

### <a name="a-sample-media-player"></a><span data-ttu-id="695ff-381">Пример проигрывателя мультимедиа</span><span class="sxs-lookup"><span data-stu-id="695ff-381">A Sample Media Player</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         Media
            Lit View
               (Default) = Lit View
               LocalizedString = @C:\Program Files\LitwareInc\ResourceDLL.dll,-123
               DefaultIcon
                  (Default) = C:\Program Files\LitwareInc\LITVIEW.EXE,1
               InstallInfo
                  ReinstallCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /reinstall
                  HideIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /hideicons
                  ShowIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /showicons
                  IconsVisible = 1
```

### <a name="a-sample-instant-messenger-program"></a><span data-ttu-id="695ff-382">Пример программы мгновенных сообщений</span><span class="sxs-lookup"><span data-stu-id="695ff-382">A Sample Instant Messenger Program</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         IM
            Lit View
               (Default) = Lit View
               LocalizedString = @C:\Program Files\LitwareInc\ResourceDLL.dll,-123
               DefaultIcon
                  (Default) = C:\Program Files\LitwareInc\LITVIEW.EXE,1
               InstallInfo
                  ReinstallCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /reinstall
                  HideIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /hideicons
                  ShowIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /showicons
                  IconsVisible = 1
```

### <a name="a-sample-virtual-machine-for-java"></a><span data-ttu-id="695ff-383">Пример виртуальной машины для Java</span><span class="sxs-lookup"><span data-stu-id="695ff-383">A Sample Virtual Machine for Java</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         JavaVM
            Lit View
               (Default) = Lit View
               LocalizedString = @C:\Program Files\LitwareInc\ResourceDLL.dll,-123
               DefaultIcon
                  (Default) = C:\Program Files\LitwareInc\LITVIEW.EXE,1
               InstallInfo
                  ReinstallCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /reinstall
                  HideIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /hideicons
                  ShowIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /showicons
                  IconsVisible = 1
```

<span data-ttu-id="695ff-384">*Примеры компаний, организаций, продуктов, доменных имен, адресов электронной почты, эмблем, людей, мест и событий являются вымышленными. Нет связи с реальными компаниями, организациями, продуктами, именами доменов, адресами электронной почты, логотипами, лицами, местами и событиями.*</span><span class="sxs-lookup"><span data-stu-id="695ff-384">*The example companies, organizations, products, domain names, email addresses, logos, people, places, and events depicted herein are fictitious. No association with any real company, organization, product, domain name, email address, logo, person, place, or event is intended or should be inferred.*</span></span>

## <a name="related-topics"></a><span data-ttu-id="695ff-385">См. также</span><span class="sxs-lookup"><span data-stu-id="695ff-385">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="695ff-386">Программы по умолчанию</span><span class="sxs-lookup"><span data-stu-id="695ff-386">Default Programs</span></span>](default-programs.md)
</dt> <dt>

[<span data-ttu-id="695ff-387">Как зарегистрировать Интернет браузер или почтовый клиент в меню "Пуск" Windows</span><span class="sxs-lookup"><span data-stu-id="695ff-387">How to Register an Internet Browser or Email Client With the Windows Start Menu</span></span>](start-menu-reg.md)
</dt> <dt>

<span data-ttu-id="695ff-388">[Макет реестра клиента Internet Explorer (см. раздел "определения разделов реестра клиента")](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa753633(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="695ff-388">[Internet Explorer Client Registry Layout (see the "Client Registry Key Definitions" section)](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa753633(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="695ff-389">[Обзор асинхронного подключаемого протокола и учебники](/previous-versions//aa767913(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="695ff-389">[Asynchronous Pluggable Protocol Overviews and Tutorials](/previous-versions//aa767913(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="695ff-390">[Регистрация приложения в схеме URI](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767914(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="695ff-390">[Registering an Application to a URI Scheme](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767914(v=vs.85))</span></span>
</dt> </dl>

 

 
