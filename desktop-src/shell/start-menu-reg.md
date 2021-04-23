---
description: Меню Пуск в Windows XP и Windows Vista содержит зарезервированные слоты для клиентов Интернета (браузер) и электронной почты (почты), которые обычно называются Интернет-приложениями «Пуск».
ms.assetid: a3d7416f-0dbd-4af2-ab38-758f9cc8aec5
title: Как зарегистрировать Интернет браузер или почтовый клиент в меню "Пуск" Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eccdd8fb8efe32522947b30ab2ce1a50b7058e97
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "104273314"
---
# <a name="how-to-register-an-internet-browser-or-email-client-with-the-windows-start-menu"></a><span data-ttu-id="2c6ba-103">Как зарегистрировать Интернет браузер или почтовый клиент в меню "Пуск" Windows</span><span class="sxs-lookup"><span data-stu-id="2c6ba-103">How to Register an Internet Browser or Email Client With the Windows Start Menu</span></span>

> [!Note]  
> <span data-ttu-id="2c6ba-104">Этот раздел относится к Windows XP, Windows Vista и Windows 7.</span><span class="sxs-lookup"><span data-stu-id="2c6ba-104">This topic applies to Windows XP, Windows Vista, and Windows 7.</span></span>

 

<span data-ttu-id="2c6ba-105">Меню Пуск в Windows XP и Windows Vista содержит зарезервированные слоты для клиентов **Интернета** (браузер) и **электронной почты** (почты), которые обычно называются *Интернет-приложениями «Пуск*».</span><span class="sxs-lookup"><span data-stu-id="2c6ba-105">The Start menu in Windows XP and Windows Vista contains reserved slots for the default **Internet** (browser) and **E-mail** (mail) clients, together commonly known as *Start Menu Internet Applications*.</span></span> <span data-ttu-id="2c6ba-106">Приложения, которые регистрируются как меню "Пуск", Интернет-приложения выполняют все это во всей системе (на компьютере).</span><span class="sxs-lookup"><span data-stu-id="2c6ba-106">Applications which register as Start Menu Internet Applications do so across the entire system (per-machine).</span></span> <span data-ttu-id="2c6ba-107">В Windows Vista пользователь может использовать функцию **по умолчанию** для настройки параметров по умолчанию для каждого пользователя.</span><span class="sxs-lookup"><span data-stu-id="2c6ba-107">In Windows Vista, the user may use the **Default Programs** feature to set a per-user default.</span></span>

<span data-ttu-id="2c6ba-108">Когда приложения регистрируются как меню "Пуск" в Интернете, Windows XP и Windows Vista создают значки " **Интернет** " и " **Электронная почта** " в меню "Пуск".</span><span class="sxs-lookup"><span data-stu-id="2c6ba-108">When applications register as Start Menu Internet Applications, Windows XP and Windows Vista create **Internet** and **E-mail** icons on the Start menu.</span></span> <span data-ttu-id="2c6ba-109">Если щелкнуть эти значки, в меню "Пуск" будет проверяться поддерево реестра для каждого пользователя (**hKey \_ текущий \_ пользователь**).</span><span class="sxs-lookup"><span data-stu-id="2c6ba-109">Clicking these icons causes the Start menu to check the per-user registry subtree (**HKEY\_CURRENT\_USER**).</span></span> <span data-ttu-id="2c6ba-110">Если параметр по умолчанию для каждого пользователя не найден, меню "Пуск" выполняет поиск подраздела по умолчанию на компьютере в поддереве " **\_ локальный \_ компьютер" hKey** .</span><span class="sxs-lookup"><span data-stu-id="2c6ba-110">If no per-user default setting is found, the Start menu looks for the per-machine default subkey in the **HKEY\_LOCAL\_MACHINE** subtree.</span></span>

> [!Note]  
> <span data-ttu-id="2c6ba-111">Установка Windows по умолчанию не регистрирует программу Интернет или электронную почту по умолчанию для каждого пользователя, а только для всей системы по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2c6ba-111">The default installation of Windows does not register a per-user default Internet or email program, only a system-wide default.</span></span> <span data-ttu-id="2c6ba-112">Это обеспечивает плавный переход от предыдущих версий операционной системы, в которых \_ поддерживается только поддерево "локальный компьютер" hKey \_ для регистрации клиентов.</span><span class="sxs-lookup"><span data-stu-id="2c6ba-112">This provides a smooth upgrade path from previous versions of the operating system, in which only the HKEY\_LOCAL\_MACHINE subtree is supported for client registrations.</span></span>

 

<span data-ttu-id="2c6ba-113">В этом разделе обсуждаются следующие элементы:</span><span class="sxs-lookup"><span data-stu-id="2c6ba-113">This topic discusses the following items:</span></span>

-   [<span data-ttu-id="2c6ba-114">Регистрация для подключения к Интернету в меню "Пуск"</span><span class="sxs-lookup"><span data-stu-id="2c6ba-114">Registering for the Start Menu Internet Link</span></span>](#registering-for-the-start-menu-internet-link)
    -   [<span data-ttu-id="2c6ba-115">Как зарегистрироваться в качестве Интернет клиента по умолчанию</span><span class="sxs-lookup"><span data-stu-id="2c6ba-115">How to Register as the Default Internet Client</span></span>](#how-to-register-as-the-default-internet-client)
-   [<span data-ttu-id="2c6ba-116">Регистрация для ссылки на электронную почту меню "Пуск"</span><span class="sxs-lookup"><span data-stu-id="2c6ba-116">Registering for the Start Menu Email Link</span></span>](#registering-for-the-start-menu-email-link)
    -   [<span data-ttu-id="2c6ba-117">Как в меню «Пуск» отображается почтовый клиент по умолчанию</span><span class="sxs-lookup"><span data-stu-id="2c6ba-117">How the Start Menu Displays the Default Email Client</span></span>](#how-the-start-menu-displays-the-default-email-client)
    -   [<span data-ttu-id="2c6ba-118">Как зарегистрироваться в качестве почтового клиента по умолчанию</span><span class="sxs-lookup"><span data-stu-id="2c6ba-118">How to Register as the Default EMail Client</span></span>](#how-to-register-as-the-default-email-client)
-   [<span data-ttu-id="2c6ba-119">Настройка контекстного меню</span><span class="sxs-lookup"><span data-stu-id="2c6ba-119">Customizing the Context Menu</span></span>](#customizing-the-context-menu)

## <a name="registering-for-the-start-menu-internet-link"></a><span data-ttu-id="2c6ba-120">Регистрация для подключения к Интернету в меню "Пуск"</span><span class="sxs-lookup"><span data-stu-id="2c6ba-120">Registering for the Start Menu Internet Link</span></span>

> [!Note]  
> <span data-ttu-id="2c6ba-121">Эта регистрация является устаревшей по отношению к Windows 7, которая больше не предоставляет Интернет-ссылку меню "Пуск".</span><span class="sxs-lookup"><span data-stu-id="2c6ba-121">This registration is deprecated as of Windows 7, which no longer provides a Start menu Internet link.</span></span> <span data-ttu-id="2c6ba-122">Существующие регистрации игнорируются в Windows 7 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="2c6ba-122">Existing registrations are ignored in Windows 7 and later.</span></span> <span data-ttu-id="2c6ba-123">Регистрация в качестве Интернет-приложения по умолчанию в меню "Пуск" не аналогична регистрации в качестве браузера по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2c6ba-123">Being registered as the default Start menu Internet application is not the same as being registered as the default web browser.</span></span> <span data-ttu-id="2c6ba-124">Веб-браузер по умолчанию используется для запуска произвольных URL-адресов из любого места в системе.</span><span class="sxs-lookup"><span data-stu-id="2c6ba-124">The default web browser is used for launching arbitrary URLs from anywhere in the system.</span></span> <span data-ttu-id="2c6ba-125">Интернет-приложение "Пуск" просто управляет программой, которая запускается, когда пользователь щелкает значок Интернета в меню "Пуск".</span><span class="sxs-lookup"><span data-stu-id="2c6ba-125">The Start menu Internet application merely controls the program that is started when the user clicks the Internet icon on the Start menu.</span></span>

 

<span data-ttu-id="2c6ba-126">Любое приложение браузера может зарегистрироваться в качестве Интернет-клиента в меню "Пуск".</span><span class="sxs-lookup"><span data-stu-id="2c6ba-126">Any web browser application can register to appear as an Internet client on the Start menu.</span></span> <span data-ttu-id="2c6ba-127">Эта видимость, связанная с правильной регистрацией [файлов](fa-intro.md) и типов [протоколов](/previous-versions//aa767743(v=vs.85)) приложения, предоставляет состояние браузера по умолчанию для приложения.</span><span class="sxs-lookup"><span data-stu-id="2c6ba-127">This visibility, coupled with proper registration for an application's [file](fa-intro.md) and [protocol](/previous-versions//aa767743(v=vs.85)) types, gives an application default browser status.</span></span>

<span data-ttu-id="2c6ba-128">Регистрации, сделанные в поддереве **hKey \_ Current \_ User** , имеют более высокий приоритет, чем соответствующие регистрации, сделанные на **\_ локальном \_ компьютере hKey**.</span><span class="sxs-lookup"><span data-stu-id="2c6ba-128">Registrations made in the **HKEY\_CURRENT\_USER** subtree have higher precedence for the console user than corresponding registrations made in the **HKEY\_LOCAL\_MACHINE**.</span></span> <span data-ttu-id="2c6ba-129">Для новых пользователей в системе используются параметры, хранящиеся на **\_ локальном \_ компьютере hKey** .</span><span class="sxs-lookup"><span data-stu-id="2c6ba-129">For new users on the system, the settings stored in **HKEY\_LOCAL\_MACHINE** are used.</span></span> <span data-ttu-id="2c6ba-130">Начиная с Windows XP, в меню "Пуск" параметры Internet сохраняются в записях по умолчанию в двух расположениях реестра:</span><span class="sxs-lookup"><span data-stu-id="2c6ba-130">As of Windows XP, Start menu Internet settings are kept in the default entries of two registry locations:</span></span>

-   <span data-ttu-id="2c6ba-131">**HKey \_ Клиенты текущего \_ пользовательского** \\ **программного обеспечения** \\  \\ **стартменуинтернет**</span><span class="sxs-lookup"><span data-stu-id="2c6ba-131">**HKEY\_CURRENT\_USER**\\**SOFTWARE**\\**Clients**\\**StartMenuInternet**</span></span>
-   <span data-ttu-id="2c6ba-132">**HKey \_ Клиенты по для локального \_ компьютера** \\  \\  \\ **стартменуинтернет**</span><span class="sxs-lookup"><span data-stu-id="2c6ba-132">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Clients**\\**StartMenuInternet**</span></span>

<span data-ttu-id="2c6ba-133">В подразделе **hKey \_ Current \_ User** \\ **Software** \\ **Clients** \\ **стартменуинтернет** описывается Интернет-браузер, который запускается, когда пользователь щелкает значок **Интернета** в меню "Пуск".</span><span class="sxs-lookup"><span data-stu-id="2c6ba-133">The subkey **HKEY\_CURRENT\_USER**\\**SOFTWARE**\\**Clients**\\**StartMenuInternet** describes the Internet browser that is started when the user clicks the **Internet** icon on the Start menu.</span></span> <span data-ttu-id="2c6ba-134">Если этот подраздел пуст или отсутствует, значок **Интернета** в меню "Пуск" будет иметь значение по умолчанию, которое хранится во втором расположении в разделе **hKey \_ Local \_ Machine** \\ **Software** \\ **Clients** \\ **стартменуинтернет** , где описаны все приложения браузера, установленные в системе.</span><span class="sxs-lookup"><span data-stu-id="2c6ba-134">If that subkey is blank or missing, then the **Internet** icon on the Start menu is set to the system default stored in the second location at **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Clients**\\**StartMenuInternet** , which describes all Internet browser applications that are installed on the system.</span></span>

<span data-ttu-id="2c6ba-135">Когда новый пользователь входит в систему, в меню "Пуск" используется значение по умолчанию в подразделе раздела **hKey \_ Local \_ Machine** \\ **Software** \\ **Clients** \\ **стартменуинтернет** to отображать Интернет-клиент по умолчанию и запускать зарегистрированное приложение при нажатии на этот значок.</span><span class="sxs-lookup"><span data-stu-id="2c6ba-135">When a new user logs onto the system, the Start menu uses the default value in the subkey at **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Clients**\\**StartMenuInternet** to display the default Internet client and starts the registered application when that icon is clicked.</span></span>

### <a name="how-to-register-as-the-default-internet-client"></a><span data-ttu-id="2c6ba-136">Как зарегистрироваться в качестве Интернет клиента по умолчанию</span><span class="sxs-lookup"><span data-stu-id="2c6ba-136">How to Register as the Default Internet Client</span></span>

<span data-ttu-id="2c6ba-137">Под подразделом **hKey Software \_ Local \_ Machine** \\  \\ **Clients** \\ **стартменуинтернет** может быть ноль или более подразделов, по одному для каждого зарегистрированного приложения браузера Интернета.</span><span class="sxs-lookup"><span data-stu-id="2c6ba-137">Below the subkey **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Clients**\\**StartMenuInternet** there can be zero or more subkeys, one for each registered Internet browser application.</span></span> <span data-ttu-id="2c6ba-138">Например, гипотетическая система может иметь следующее расположение:</span><span class="sxs-lookup"><span data-stu-id="2c6ba-138">For example, a hypothetical system might have this arrangement:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         StartMenuInternet
            IEXPLORE.EXE
            BROWSER2.EXE
            BROWSER3.EXE
```

<span data-ttu-id="2c6ba-139">Мы покажем записи реестра с гипотетическым браузером под названием «освещенное представление» от вымышленной компании с именем Litware Inc. Предположим, что имя исполняемого файла для представления «освещенность» Litview.exe.</span><span class="sxs-lookup"><span data-stu-id="2c6ba-139">We will demonstrate registry entries with a hypothetical browser called "Lit View" from a fictional company called Litware Inc. Suppose that the executable name for Lit View is Litview.exe.</span></span> <span data-ttu-id="2c6ba-140">Регистрация светового представления выполняется, как показано ниже:</span><span class="sxs-lookup"><span data-stu-id="2c6ba-140">The registration of Lit View occurs as shown here:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         StartMenuInternet
            LITVIEW.EXE
               LocalizedString = @C:\Program Files\LitwareInc\ResourceDLL.dll,-123
```

<span data-ttu-id="2c6ba-141">Данные Локализедстринг имеют тип REG \_ SZ или REG \_ expand \_ SZ, если используются переменные пути, такие как `%programfiles%` .</span><span class="sxs-lookup"><span data-stu-id="2c6ba-141">The LocalizedString data is of type REG\_SZ, or REG\_EXPAND\_SZ if path variables such as `%programfiles%` are used.</span></span> <span data-ttu-id="2c6ba-142">Локализедстринг предоставляет путь к исполняемому файлу (exe) или библиотеке (DLL).</span><span class="sxs-lookup"><span data-stu-id="2c6ba-142">LocalizedString provides the path to an executable (.exe) or library (.dll) file.</span></span> <span data-ttu-id="2c6ba-143">Обратите внимание, что строка пути начинается со знака «at» (@) и не требует ввода кавычек для пути, независимо от пробелов в нем.</span><span class="sxs-lookup"><span data-stu-id="2c6ba-143">Note that the path string begins with an "at" sign (@) and that no quotation marks are required around the path regardless of spaces within it.</span></span> <span data-ttu-id="2c6ba-144">Десятичное целое число — это идентификатор строкового ресурса, содержащийся в указанной библиотеке DLL, значение которого должно отображаться для пользователя.</span><span class="sxs-lookup"><span data-stu-id="2c6ba-144">The decimal integer is the ID of a string resource, contained within the specified DLL, whose value is to be displayed to the user.</span></span> <span data-ttu-id="2c6ba-145">Это позволяет использовать одну и ту же регистрацию для нескольких языков.</span><span class="sxs-lookup"><span data-stu-id="2c6ba-145">This enables the same registration to be used for multiple languages.</span></span> <span data-ttu-id="2c6ba-146">Каждый язык предоставляет разные ResourceDLL.dll.</span><span class="sxs-lookup"><span data-stu-id="2c6ba-146">Each language provides a different ResourceDLL.dll.</span></span> <span data-ttu-id="2c6ba-147">Это позволяет системе отображать правильную строку на основе текущего выбранного языка.</span><span class="sxs-lookup"><span data-stu-id="2c6ba-147">This enables the system to display the correct string based on the currently selected language.</span></span>

<span data-ttu-id="2c6ba-148">Следующее значение REG \_ SZ или REG \_ expand \_ SZ информирует меню "Пуск" значка по умолчанию, которое отображается, когда пользователь выбирает представление "освещенность" в браузере в меню "Пуск" в Интернете.</span><span class="sxs-lookup"><span data-stu-id="2c6ba-148">The following REG\_SZ or REG\_EXPAND\_SZ value informs the Start menu of the default icon to display when the user selects Lit View as the Start menu Internet browser.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         StartMenuInternet
            LITVIEW.EXE
               DefaultIcon
                  (Default) = C:\Program Files\LitwareInc\LitView.exe,1
```

<span data-ttu-id="2c6ba-149">В следующем подразделе реестра указана Командная строка, которая будет запускаться при нажатии пользователем команды меню "Интернет" в меню "Пуск" при условии, что режим освещенности является выбранным веб-браузером меню "Пуск".</span><span class="sxs-lookup"><span data-stu-id="2c6ba-149">The following registry subkey specifies a command line to run when the user clicks the Internet menu command on the Start menu, assuming that Lit View is the selected Start menu Internet browser.</span></span> <span data-ttu-id="2c6ba-150">Например, команда может открыть браузер с помощью домашней страницы пользователя, или команда может запустить вводный пользовательский интерфейс, подходящий для независимого поставщика программного обеспечения (ISV).</span><span class="sxs-lookup"><span data-stu-id="2c6ba-150">For example, the command might open the browser with the user's home page or the command could launch an introductory user interface that the independent software vendor (ISV) feels is appropriate.</span></span> <span data-ttu-id="2c6ba-151">Данные имеют тип REG \_ SZ или REG \_ expand \_ SZ, но обратите внимание, что, поскольку в пути командной строки имеется пробел, путь к исполняемому файлу заключается в кавычки.</span><span class="sxs-lookup"><span data-stu-id="2c6ba-151">The data is of type REG\_SZ or REG\_EXPAND\_SZ, but notice that because there is a space in the command-line path, the executable path is enclosed in quotation marks.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         StartMenuInternet
            LITVIEW.EXE
               shell
                  open
                     (Default) = "C:\Program Files\LitwareInc\LitView.exe" -welcome
```

<span data-ttu-id="2c6ba-152">Если пользователь указывает, что в качестве веб-браузера по умолчанию на уровне компьютера следует использовать режим [доступа к программам и параметры по умолчанию (SPAD)](cpl-setprogramaccess.md) , приложение должно задать следующую \_ запись reg SZ.</span><span class="sxs-lookup"><span data-stu-id="2c6ba-152">When the user specifies through [Set Program Access and Computer Defaults (SPAD)](cpl-setprogramaccess.md) that Lit View should be used as the computer-level default web browser, the application should set the following REG\_SZ entry.</span></span> <span data-ttu-id="2c6ba-153">Обратите внимание, что, поскольку SPAD работает с правами администратора, доступ к этому подразделу разрешен.</span><span class="sxs-lookup"><span data-stu-id="2c6ba-153">Note that because SPAD runs with Administrator privileges, access to this subkey is allowed.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         StartMenuInternet
            (Default) = LITVIEW.EXE
```

> [!Note]
> <span data-ttu-id="2c6ba-154">В Windows Vista веб-браузер по умолчанию на уровне пользователя должен быть установлен с помощью средства **программы по умолчанию** , а не [SPAD](cpl-setprogramaccess.md).</span><span class="sxs-lookup"><span data-stu-id="2c6ba-154">In Windows Vista, the user-level default web browser should be set using the **Default Programs** tool, not [SPAD](cpl-setprogramaccess.md).</span></span>
> 
> <span data-ttu-id="2c6ba-155">**Приведенные ниже сведения относятся только к Windows XP.**</span><span class="sxs-lookup"><span data-stu-id="2c6ba-155">**The following information applies to Windows XP only.**</span></span>
> 
> <span data-ttu-id="2c6ba-156">Если регистрация веб-браузера по умолчанию на уровне компьютера в разделе HKEY \_ локальный \_ компьютер, как показано выше, выполняется успешно, приложение должно удалить запись по умолчанию в следующем подразделе:</span><span class="sxs-lookup"><span data-stu-id="2c6ba-156">If the registration of the computer-level default web browser under HKEY\_LOCAL\_MACHINE as shown above is successful, the application should delete the Default entry under the following subkey:</span></span>
> 
> ```
> HKEY_CURRENT_USER
>    SOFTWARE
>       Clients
>          StartMenuInternet
> ```
> 
> <span data-ttu-id="2c6ba-157">Если при регистрации веб-браузера по умолчанию на уровне компьютера в разделе HKEY \_ \_ на локальном компьютере происходит сбой, приложение должно задать \_ данные reg SZ, как показано в следующем примере для приложения с представлением "освещенность":</span><span class="sxs-lookup"><span data-stu-id="2c6ba-157">If the registration of the computer-level default web browser under HKEY\_LOCAL\_MACHINE fails, the application should set the REG\_SZ data as shown in this example for the Lit View application:</span></span>
> 
> ```
> HKEY_CURRENT_USER
>    SOFTWARE
>       Clients
>          (Default) = LITVIEW.EXE
> ```

 

<span data-ttu-id="2c6ba-158">После обновления соответствующих подразделов приложение передает сообщение [**WM \_ сеттингчанже**](../winmsg/wm-settingchange.md) с его параметром *wParam* , имеющим значение 0, и параметр *lParam* , указывающий на строку, завершающуюся нулем `"Software\Clients\StartMenuInternet"` .</span><span class="sxs-lookup"><span data-stu-id="2c6ba-158">After updating the appropriate subkeys, the application broadcasts the [**WM\_SETTINGCHANGE**](../winmsg/wm-settingchange.md) message with its *wParam* parameter set to 0 and its *lParam* parameter pointing to the null-terminated string `"Software\Clients\StartMenuInternet"`.</span></span> <span data-ttu-id="2c6ba-159">Это уведомление операционной системы о том, что клиент по умолчанию изменился.</span><span class="sxs-lookup"><span data-stu-id="2c6ba-159">This notifies the operating system that the default client has changed.</span></span>

<span data-ttu-id="2c6ba-160">Установка этих подразделов для веб-браузера по умолчанию в меню "Пуск" необходима для сохранения обратной совместимости со старыми браузерами, которые не поддерживают регистрацию для каждого пользователя.</span><span class="sxs-lookup"><span data-stu-id="2c6ba-160">Setting these subkeys for the default Start menu Internet browser is necessary to preserve backward compatibility with old web browsers that do not support per-user registrations.</span></span>

## <a name="registering-for-the-start-menu-email-link"></a><span data-ttu-id="2c6ba-161">Регистрация для ссылки на электронную почту меню "Пуск"</span><span class="sxs-lookup"><span data-stu-id="2c6ba-161">Registering for the Start Menu Email Link</span></span>

> [!Note]  
> <span data-ttu-id="2c6ba-162">Ссылка на электронную почту меню "Пуск" была удалена в Windows 7.</span><span class="sxs-lookup"><span data-stu-id="2c6ba-162">The Start menu Email link has been removed as of Windows 7.</span></span> <span data-ttu-id="2c6ba-163">Однако эта регистрация, обсуждаемая в этом разделе, по-прежнему должна выполняться при назначении клиента MAPI по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2c6ba-163">However, this registration discussed in this section should still be performed for its effect in assigning the default MAPI client.</span></span>

 

### <a name="how-the-start-menu-displays-the-default-email-client"></a><span data-ttu-id="2c6ba-164">Как в меню «Пуск» отображается почтовый клиент по умолчанию</span><span class="sxs-lookup"><span data-stu-id="2c6ba-164">How the Start Menu Displays the Default Email Client</span></span>

<span data-ttu-id="2c6ba-165">Любое приложение электронной почты может зарегистрироваться, чтобы оно отображалось как почтовый клиент в меню "Пуск".</span><span class="sxs-lookup"><span data-stu-id="2c6ba-165">Any email application can register to appear as an email client on the Start menu.</span></span> <span data-ttu-id="2c6ba-166">Эта видимость, связанная с правильной регистрацией [файлов](fa-intro.md) и типов [протоколов](/previous-versions//aa767743(v=vs.85)) приложения, предоставляет состояние почты приложения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2c6ba-166">This visibility, coupled with proper registration for an application's [file](fa-intro.md) and [protocol](/previous-versions//aa767743(v=vs.85)) types, gives an application default mail status.</span></span>

<span data-ttu-id="2c6ba-167">Регистрации, сделанные в поддереве **hKey \_ Current \_ User** , имеют более высокий приоритет, чем соответствующие регистрации, сделанные на **\_ локальном \_ компьютере hKey**.</span><span class="sxs-lookup"><span data-stu-id="2c6ba-167">Registrations made in the **HKEY\_CURRENT\_USER** subtree have higher precedence for the console user than corresponding registrations made in the **HKEY\_LOCAL\_MACHINE**.</span></span> <span data-ttu-id="2c6ba-168">Для новых пользователей в системе используются параметры, хранящиеся на **\_ локальном \_ компьютере hKey** .</span><span class="sxs-lookup"><span data-stu-id="2c6ba-168">For new users on the system, the settings stored in **HKEY\_LOCAL\_MACHINE** are used.</span></span> <span data-ttu-id="2c6ba-169">Начиная с Windows XP параметры электронной почты в меню "Пуск" хранятся в записях по умолчанию в двух расположениях реестра:</span><span class="sxs-lookup"><span data-stu-id="2c6ba-169">As of Windows XP, Start menu Email settings are kept in the default entries of two registry locations:</span></span>

-   <span data-ttu-id="2c6ba-170">**HKey \_ Почта клиентов текущего \_ пользовательского** \\ **программного обеспечения** \\  \\ </span><span class="sxs-lookup"><span data-stu-id="2c6ba-170">**HKEY\_CURRENT\_USER**\\**SOFTWARE**\\**Clients**\\**Mail**</span></span>
-   <span data-ttu-id="2c6ba-171">**HKey \_ \_** Почта для \\  \\ **клиентов** \\  по локальному компьютеру</span><span class="sxs-lookup"><span data-stu-id="2c6ba-171">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Clients**\\**Mail**</span></span>

<span data-ttu-id="2c6ba-172">В подразделе **hKey \_ Current \_ User** \\ **Software** \\ **Clients** \\ **mail описывается почтовый** клиент, который запускается, когда пользователь щелкает значок **электронной почты** в меню "Пуск".</span><span class="sxs-lookup"><span data-stu-id="2c6ba-172">The subkey **HKEY\_CURRENT\_USER**\\**SOFTWARE**\\**Clients**\\**Mail** describes the email client that is started when the user clicks the **E-mail** icon on the Start menu.</span></span>

<span data-ttu-id="2c6ba-173">В подразделе **hKey \_ Local \_ Machine** \\ **Software** \\ **Clients** \\ **mail** описываются приложения электронной почты, установленные в системе, а также приложение электронной почты по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2c6ba-173">The subkey **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Clients**\\**Mail** describes the email applications that are installed on the system, as well as the default email application.</span></span>

<span data-ttu-id="2c6ba-174">Если почта " **hKey \_ Current \_ User** \\ **Software** \\ **Clients**" \\  пуста или отсутствует, значение по умолчанию, определенное в списке "программное обеспечение на **\_ локальном \_ компьютере**", \\  \\  \\  используется для выбора почтового приложения, отображаемого в меню "Пуск".</span><span class="sxs-lookup"><span data-stu-id="2c6ba-174">If the **HKEY\_CURRENT\_USER**\\**SOFTWARE**\\**Clients**\\**Mail** is blank or missing, the default value defined in **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Clients**\\**Mail** is used to select the email application that appears on the Start menu.</span></span>

<span data-ttu-id="2c6ba-175">При входе нового пользователя в систему в меню "Пуск" используется значение по умолчанию в подразделе раздела **hKey \_ Local \_ Machine** \\ **Software** \\ **Clients** \\ **mail** , чтобы отобразить почтовый клиент по умолчанию и запустить зарегистрированное приложение при нажатии этого значка.</span><span class="sxs-lookup"><span data-stu-id="2c6ba-175">When a new user logs onto the system, the Start menu uses the default value in the subkey at **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Clients**\\**Mail** to display the default email client and starts the registered application when that icon is clicked.</span></span>

### <a name="how-to-register-as-the-default-email-client"></a><span data-ttu-id="2c6ba-176">Как зарегистрироваться в качестве почтового клиента по умолчанию</span><span class="sxs-lookup"><span data-stu-id="2c6ba-176">How to Register as the Default EMail Client</span></span>

<span data-ttu-id="2c6ba-177">**HKey \_ \_** \\ **По** электронной почте клиенты локального компьютера \\  \\  могут содержать ноль или более подразделов, по одному для каждого зарегистрированного приложения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="2c6ba-177">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Clients**\\**Mail** can contain zero or more subkeys, one for each registered email application.</span></span> <span data-ttu-id="2c6ba-178">Например, гипотетическая система может определять следующие подразделы:</span><span class="sxs-lookup"><span data-stu-id="2c6ba-178">For example, a hypothetical system might define the following subkeys:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            Eudora
            Windows Mail
```

<span data-ttu-id="2c6ba-179">Мы покажем записи реестра с гипотетическим почтовым клиентом, именуемым «освещенная почта», из вымышленной компании с именем Litware Inc. Litware Inc. решает зарегистрировать почтовый клиент по внутреннему имени «Литмаил».</span><span class="sxs-lookup"><span data-stu-id="2c6ba-179">We will demonstrate registry entries with a hypothetical email client called "Lit Mail" from the fictional company called Litware Inc. Litware Inc. decides to register this email client under the internal name "LitMail".</span></span> <span data-ttu-id="2c6ba-180">Как и в случае с браузером, внутреннее имя — это уникальная строка, используемая в качестве имени подраздела, но она никогда не отображается для пользователя.</span><span class="sxs-lookup"><span data-stu-id="2c6ba-180">As with a browser, the internal name is a unique string used as the subkey name, but it is never shown to the user.</span></span>

<span data-ttu-id="2c6ba-181">Чтобы установить клиент электронной почты освещенности по умолчанию, он использует следующий подраздел и его записи:</span><span class="sxs-lookup"><span data-stu-id="2c6ba-181">To install the Lit Mail email client as the default, they use the following subkey and its entries:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            LitMail
               (Default) = Lit Mail
               LocalizedString = @C:\Program Files\LitwareInc\ResourceDLL.dll,-456
```

<span data-ttu-id="2c6ba-182">Данные Локализедстринг имеют тип REG \_ SZ или REG \_ expand \_ SZ, если используются переменные пути, такие как `%programfiles%` .</span><span class="sxs-lookup"><span data-stu-id="2c6ba-182">The LocalizedString data is of type REG\_SZ, or REG\_EXPAND\_SZ if path variables such as `%programfiles%` are used.</span></span> <span data-ttu-id="2c6ba-183">Локализедстринг предоставляет путь к исполняемому файлу (exe) или библиотеке (DLL).</span><span class="sxs-lookup"><span data-stu-id="2c6ba-183">LocalizedString provides the path to an executable (.exe) or library (.dll) file.</span></span> <span data-ttu-id="2c6ba-184">Обратите внимание, что строка пути начинается со знака «at» (@) и не требует ввода кавычек для пути, независимо от пробелов в нем.</span><span class="sxs-lookup"><span data-stu-id="2c6ba-184">Note that the path string begins with an "at" sign (@) and that no quotation marks are required around the path regardless of spaces within it.</span></span> <span data-ttu-id="2c6ba-185">Десятичное целое число — это идентификатор строкового ресурса, содержащийся в указанной библиотеке DLL, значение которого должно отображаться для пользователя.</span><span class="sxs-lookup"><span data-stu-id="2c6ba-185">The decimal integer is the ID of a string resource, contained within the specified DLL, whose value is to be displayed to the user.</span></span> <span data-ttu-id="2c6ba-186">Это позволяет использовать одну и ту же регистрацию для нескольких языков.</span><span class="sxs-lookup"><span data-stu-id="2c6ba-186">This enables the same registration to be used for multiple languages.</span></span> <span data-ttu-id="2c6ba-187">Каждый язык предоставляет разные ResourceDLL.dll.</span><span class="sxs-lookup"><span data-stu-id="2c6ba-187">Each language provides a different ResourceDLL.dll.</span></span> <span data-ttu-id="2c6ba-188">Это позволяет системе отображать правильную строку на основе текущего выбранного языка.</span><span class="sxs-lookup"><span data-stu-id="2c6ba-188">This enables the system to display the correct string based on the currently selected language.</span></span>

<span data-ttu-id="2c6ba-189">После обновления соответствующих подразделов приложение передает сообщение [**WM \_ сеттингчанже**](../winmsg/wm-settingchange.md) с его параметром *wParam* , имеющим значение 0, и параметр *lParam* , указывающий на строку, завершающуюся нулем `"Software\Clients\Mail"` .</span><span class="sxs-lookup"><span data-stu-id="2c6ba-189">After updating the appropriate subkeys, the application broadcasts the [**WM\_SETTINGCHANGE**](../winmsg/wm-settingchange.md) message with its *wParam* parameter set to 0 and its *lParam* parameter pointing to the null-terminated string `"Software\Clients\Mail"`.</span></span> <span data-ttu-id="2c6ba-190">Это уведомление операционной системы о том, что клиент по умолчанию изменился.</span><span class="sxs-lookup"><span data-stu-id="2c6ba-190">This notifies the operating system that the default client has changed.</span></span>

<span data-ttu-id="2c6ba-191">Для обеспечения обратной совместимости с приложениями, которые не поддерживают локализованные строки, имя приложения на установленном языке также должно быть задано в качестве значения по умолчанию для подраздела.</span><span class="sxs-lookup"><span data-stu-id="2c6ba-191">For backward compatibility with applications that do not support localized strings, the name of the application in the installed language should also be set as the default value for the subkey.</span></span>

<span data-ttu-id="2c6ba-192">Следующее значение **reg \_ SZ** или **reg \_ expand \_ SZ** информирует меню "Пуск" значка по умолчанию, которое отображается, когда пользователь выбирает в меню "Пуск" пункт "Освещенная почта":</span><span class="sxs-lookup"><span data-stu-id="2c6ba-192">The following **REG\_SZ** or **REG\_EXPAND\_SZ** value informs the Start menu of the default icon to display when the user selects Lit Mail as the Start menu mail program:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            LitMail
               DefaultIcon
                  (Default) = C:\Program Files\LitwareInc\LitMail.exe,1
```

<span data-ttu-id="2c6ba-193">Следующая запись указывает командную строку, которая будет запускаться, когда пользователь щелкает пункт меню " **Электронная почта** " в меню "Пуск", предполагая, что в меню "Пуск" выбрана программа электронной почты "горит".</span><span class="sxs-lookup"><span data-stu-id="2c6ba-193">The following entry specifies a command line to run when the user clicks the **E-mail** menu item on the Start menu, assuming that Lit Mail is the selected Start menu email program.</span></span> <span data-ttu-id="2c6ba-194">Эта командная строка также выполняется, если пользователь выбирает пункт **Чтение электронной почты** из меню **Сервис** Windows Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="2c6ba-194">This command line is also run if the user selects **Read email** from the Windows Internet Explorer **Tools** menu.</span></span> <span data-ttu-id="2c6ba-195">Данные имеют тип **reg \_ SZ** или **reg \_ expand \_ SZ**, но обратите внимание, что, поскольку в пути командной строки имеется пробел, путь к исполняемому файлу заключается в кавычки.</span><span class="sxs-lookup"><span data-stu-id="2c6ba-195">The data is of type **REG\_SZ** or **REG\_EXPAND\_SZ**, but notice that because there is a space in the command-line path, the executable path is enclosed in quotation marks.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            shell
               open
                  command
                     (Default) = "C:\Program Files\LitwareInc\LitMail.exe" -inbox
```

<span data-ttu-id="2c6ba-196">Если (и только в том случае, если) *пользователь* указывает, что в меню "Пуск" по умолчанию задано освещенное сообщение электронной почты, оно может записать свое внутреннее имя в следующее значение **reg \_ SZ** :</span><span class="sxs-lookup"><span data-stu-id="2c6ba-196">If (and only if) *the user* specifies Lit Mail to be the default Start menu email application, the Lit Mail application may write its internal name to the following **REG\_SZ** value:</span></span>

```
HKEY_CURRENT_USER
   SOFTWARE
      Clients
         Mail
            (Default) = LitMail
```

<span data-ttu-id="2c6ba-197">Если (и только в том случае, если) *пользователь* указал свою почтовые сообщения как приложение электронной почты по умолчанию, оно может записать свое внутреннее имя в значение **reg \_ SZ** , указанное ниже.</span><span class="sxs-lookup"><span data-stu-id="2c6ba-197">If (and only if) *the user* specifies Lit Mail to be the system-wide default email application, the Lit Mail application may write its internal name to the **REG\_SZ** value specified below.</span></span> <span data-ttu-id="2c6ba-198">Обратите внимание, что доступ к этому подразделу может быть ограничен.</span><span class="sxs-lookup"><span data-stu-id="2c6ba-198">Note that access to this subkey might be restricted.</span></span> <span data-ttu-id="2c6ba-199">В приложениях не следует рассчитывать, что все пользователи имеют разрешение на изменение приложения электронной почты по умолчанию в масштабе всей системы.</span><span class="sxs-lookup"><span data-stu-id="2c6ba-199">Applications should not assume that all users have permission to change the system-wide default email application.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            (Default) = LitMail
```

<span data-ttu-id="2c6ba-200">Регистрация в качестве приложения электронной почты в меню "Пуск" по умолчанию не эквивалентна регистрации в качестве почтового клиента по умолчанию для системы или зарегистрированного обработчика *mailto* .</span><span class="sxs-lookup"><span data-stu-id="2c6ba-200">Registration as the default Start menu email application is not equivalent to registration as the system default email client or the registered *mailto* handler.</span></span>

-   <span data-ttu-id="2c6ba-201">Почтовый клиент по умолчанию запускается, когда пользователь щелкает пункт **Чтение электронной почты** из меню **Сервис** Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="2c6ba-201">The system default email client is started when the user clicks **Read email** from the Internet Explorer **Tools** menu.</span></span>
-   <span data-ttu-id="2c6ba-202">Зарегистрированный обработчик *mailto* запускается, когда пользователь щелкает URL-адрес формы `mailto:someone@example.com` .</span><span class="sxs-lookup"><span data-stu-id="2c6ba-202">The registered *mailto* handler is started when the user clicks a URL of the form `mailto:someone@example.com`.</span></span>
-   <span data-ttu-id="2c6ba-203">Приложение электронной почты меню "Пуск" запускается, когда пользователь щелкает значок **электронной почты** в меню "Пуск".</span><span class="sxs-lookup"><span data-stu-id="2c6ba-203">The Start menu email application is started when the user clicks the **E-mail** icon on the Start menu.</span></span>

<span data-ttu-id="2c6ba-204">Если не указано почтовое приложение по умолчанию меню "Пуск", значок электронной почты в меню "Пуск" запускает почтовый клиент по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2c6ba-204">If no default Start menu email application is specified, the Email icon on the Start menu launches the system default email client.</span></span>

<span data-ttu-id="2c6ba-205">В этом разделе не рассматривается регистрация приложения в качестве обработчика протокола *mailto* по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2c6ba-205">This topic does not cover registration of the application as the default *mailto* protocol handler.</span></span> <span data-ttu-id="2c6ba-206">Приложения, которые требуется зарегистрировать таким образом, должны продолжать следовать существующим спецификациям в этой теме.</span><span class="sxs-lookup"><span data-stu-id="2c6ba-206">Applications that want to register in such a manner should continue to follow existing specifications on this subject.</span></span>

## <a name="customizing-the-context-menu"></a><span data-ttu-id="2c6ba-207">Настройка контекстного меню</span><span class="sxs-lookup"><span data-stu-id="2c6ba-207">Customizing the Context Menu</span></span>

<span data-ttu-id="2c6ba-208">Приложение может настраивать страницы свойств, отображаемые, когда пользователь выбирает **Свойства** из контекстного меню значка **электронной почты** (или **Интернета**).</span><span class="sxs-lookup"><span data-stu-id="2c6ba-208">An application can customize the property pages that are displayed when the user selects **Properties** from the **E-mail** (or **Internet**) icon's shortcut menu.</span></span> <span data-ttu-id="2c6ba-209">Например, приложение электронной почты Litware добавляет следующие данные **reg \_ SZ** или **reg \_ expand \_ SZ** , чтобы отобразить настраиваемую страницу свойств для значка **электронной почты** , а не страницу свойств по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2c6ba-209">For example, the Litware email application adds the following **REG\_SZ** or **REG\_EXPAND\_SZ** data to display a custom property sheet for the **E-mail** icon rather than its default property sheet.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            LitMail
               shell
                  properties
                     MUIVerb = @C:\Program Files\LitwareInc\ResourceDLL.dll,-789
                     command
                        (Default) = "C:\Program Files\LitwareInc\LitMail.exe" -properties
```

<span data-ttu-id="2c6ba-210">Элемент данных Муиверб создается, начиная с знака «at» (@), за которым следует полный путь к библиотеке DLL ресурсов, запятая, знак минуса (-), а затем отображаемый десятичный строковый идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="2c6ba-210">The MUIVerb data item is constructed beginning with an "at" sign (@), followed by the full path to the resource DLL, a comma, a minus sign (-), and then the decimal string resource identifier to display.</span></span> <span data-ttu-id="2c6ba-211">Обратите внимание, что путь к программе LitMail.exe содержит пробелы, поэтому строка пути помещается в кавычки.</span><span class="sxs-lookup"><span data-stu-id="2c6ba-211">Note that the path to the LitMail.exe program contains spaces, so the path string is placed inside quotation marks.</span></span>

<span data-ttu-id="2c6ba-212">Приложение также может добавлять в контекстное меню дополнительные команды.</span><span class="sxs-lookup"><span data-stu-id="2c6ba-212">An application can also add additional commands to the context menu.</span></span> <span data-ttu-id="2c6ba-213">Например, приложение электронной почты Litware добавляет команду **Find** со следующими данными **реестра \_ SZ** :</span><span class="sxs-lookup"><span data-stu-id="2c6ba-213">For example, the Litware email application adds a **find** command with the following **REG\_SZ** data:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            LitMail
               shell
                  find
                     MUIVerb = @C:\Program File\LitwareInc\ResourceDLL.dll,-790
                     command
                        (Default) = "C:\Program Files\LitwareInc\LitMail.exe" -contacts
```

<span data-ttu-id="2c6ba-214">Имя подраздела под **оболочкой** (в данном случае "Find") является произвольным нелокализованным именем.</span><span class="sxs-lookup"><span data-stu-id="2c6ba-214">The subkey name below **shell** (in this case, "find") is an arbitrary, nonlocalized name.</span></span> <span data-ttu-id="2c6ba-215">Опять же, данные Муиверб содержат знак "at" (@) в качестве первого элемента, за которым следует путь к DLL-файлу ресурсов, разделитель запятой, а затем знак "минус" перед идентификатором десятичной строки.</span><span class="sxs-lookup"><span data-stu-id="2c6ba-215">Once again the MUIVerb data contains an "at" sign (@) as the first element, followed by the path to a resource DLL, a comma separator, and then a minus sign preceding the decimal string resource identifier.</span></span> <span data-ttu-id="2c6ba-216">Например, строковый ресурс может иметь значение "открыть адресную книгу".</span><span class="sxs-lookup"><span data-stu-id="2c6ba-216">For example, that string resource might be "Open Address Book".</span></span> <span data-ttu-id="2c6ba-217">Наконец, обратите внимание, что строка командной строки содержит пробелы, поэтому она заключается в кавычки.</span><span class="sxs-lookup"><span data-stu-id="2c6ba-217">Finally, note that the command-line string contains spaces, so it is enclosed in quotation marks.</span></span>

 

 
