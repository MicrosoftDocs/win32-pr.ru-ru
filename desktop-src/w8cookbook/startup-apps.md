---
title: Автозагружаемые приложения
description: Автозагружаемые приложения
ms.assetid: 3519CB52-A6EC-4819-87FE-C144801BDD9F
keywords:
- запускаемое приложение
- Фоновая задача
- Запустить ключ
- RunOnce
- папка автозагрузки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75a12f01dac073712512206a5c432561b4a0b75e
ms.sourcegitcommit: 46376be61d3fa308f9b1a06d7e2fa122a39755af
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "103797124"
---
# <a name="startup-apps"></a><span data-ttu-id="f8670-108">Автозагружаемые приложения</span><span class="sxs-lookup"><span data-stu-id="f8670-108">Startup apps</span></span>

## <a name="platform"></a><span data-ttu-id="f8670-109">Платформа</span><span class="sxs-lookup"><span data-stu-id="f8670-109">Platform</span></span>

<span data-ttu-id="f8670-110">**Клиенты**   Windows 8</span><span class="sxs-lookup"><span data-stu-id="f8670-110">**Clients**   Windows 8</span></span>  


## <a name="description"></a><span data-ttu-id="f8670-111">Описание</span><span class="sxs-lookup"><span data-stu-id="f8670-111">Description</span></span>

<span data-ttu-id="f8670-112">Одним из больших элементов с Windows является возможность освещения различных форм-факторов, от традиционных настольных компьютеров и ноутбуков до планшетов с низким энергопотреблением.</span><span class="sxs-lookup"><span data-stu-id="f8670-112">One of the big bets with Windows is the ability to light up various form factors, from the traditional desktops and laptops to low-powered tablets.</span></span> <span data-ttu-id="f8670-113">Чтобы гарантировать, что наши взаимные клиенты работают с любыми конструктивными факторами, которые они выбирают в Windows, две метрики успеха, которые необходимо решить, — это увеличение времени работы аккумулятора и отклика ПК.</span><span class="sxs-lookup"><span data-stu-id="f8670-113">To ensure that our mutual customers have a great experience on any form factor they choose with Windows, two key success metrics that need to be addressed are increased battery life and excellent PC responsiveness.</span></span> <span data-ttu-id="f8670-114">Для достижения этих целей усовершенствования были внесены в несколько областей Windows, включая жизненный цикл процесса, состояния спящего режима и запускаемые приложения (приложения с автоматическим запуском после загрузки компьютера).</span><span class="sxs-lookup"><span data-stu-id="f8670-114">In order to achieve these, improvements have been made in multiple areas of Windows including process life cycle, sleep states and startup apps (apps with automated launch after machine boot).</span></span> <span data-ttu-id="f8670-115">В этом разделе рассматриваются некоторые аспекты влияния запуска приложений на устройство Windows, а также предоставляются рекомендации для разработчиков (ISV/IHV) и OEM-производителей для пересмотра шаблонов использования запускаемых приложений с целью повышения времени работы аккумулятора и скорости реагирования для наших клиентов.</span><span class="sxs-lookup"><span data-stu-id="f8670-115">This topic highlights some of the impacts that startup apps have on a Windows device, and provides guidance to developers (ISV/IHV) and OEMs to rethink the usage patterns of startup apps in order to improve battery life and responsiveness for our mutual customers.</span></span> <span data-ttu-id="f8670-116">В нем также описываются изменения в Windows, которые позволяют пользователям управлять определением того, какие из запускаемых приложений действительно будут выполняться.</span><span class="sxs-lookup"><span data-stu-id="f8670-116">It also describes the changes in Windows that put users in control of determining which of the startup apps actually get to execute.</span></span>

<span data-ttu-id="f8670-117">Приложения для Магазина Windows предназначены для соблюдения новых стандартов потребления аккумулятора и скорости реагирования, и Windows управляет их жизненным циклом, приостанавливая и/или прерывая их работу.</span><span class="sxs-lookup"><span data-stu-id="f8670-117">Windows Store apps are designed to adhere to new standards of battery consumption and responsiveness, and Windows manages their life cycle by suspending and/or terminating them.</span></span> <span data-ttu-id="f8670-118">Однако настольные приложения, предназначенные для предыдущих версий Windows, не обязательно были разработаны для сохранения времени работы аккумулятора или обеспечения чувствительности к активности пользователей, а также могут повлиять на скорость реагирования системы (например, когда приложение отправляет стандартный период пульса с 1 секундей для проверки наличия обновлений или предварительно выделяет память до тех пор, пока она потребуется позже).</span><span class="sxs-lookup"><span data-stu-id="f8670-118">However, desktop apps designed for prior Windows versions have not necessarily been designed to preserve battery life or be sensitive to user activity, and can affect system responsiveness (for example, when an app sends a regular 1-second heartbeat to check for updates, or pre-allocates memory upfront in case it needs it later).</span></span> <span data-ttu-id="f8670-119">Это может понижать удобство работы пользователя, который покупает Windows Tablet PC с ожидаемым временем жизни аккумулятора и неделями в режиме ожидания, но обнаруживает, что батарея планшета не достигает этих целей.</span><span class="sxs-lookup"><span data-stu-id="f8670-119">This can create a poor experience for the user who buys a Windows tablet PC with a long battery life expectancy and weeks of standby, but discovers the tablet s battery life does not achieve these goals.</span></span> <span data-ttu-id="f8670-120">Кроме того, поскольку запускаемые приложения выполняются в фоновом режиме, количество приложений, работающих в системе, может быть значительно больше, чем известно пользователю, и влияет на скорость реагирования системы.</span><span class="sxs-lookup"><span data-stu-id="f8670-120">Also, since startup apps run in the background, the number of apps running on the system can be significantly more than what the user is aware of and affect system responsiveness.</span></span> <span data-ttu-id="f8670-121">Приложения, запускаемые при запуске, классифицируются так, чтобы использовать эти механизмы для запуска:</span><span class="sxs-lookup"><span data-stu-id="f8670-121">Startup apps are classified to include those leveraging these mechanisms to start:</span></span>

-   <span data-ttu-id="f8670-122">Запуск разделов реестра (HKLM, HKCU, подсистемы WOW64)</span><span class="sxs-lookup"><span data-stu-id="f8670-122">Run registry keys (HKLM, HKCU, wow64 nodes included)</span></span>
-   <span data-ttu-id="f8670-123">Разделы реестра RunOnce</span><span class="sxs-lookup"><span data-stu-id="f8670-123">RunOnce registry keys</span></span>
-   <span data-ttu-id="f8670-124">Папки автозагрузки в меню "Пуск" для каждого пользователя и общедоступных расположений</span><span class="sxs-lookup"><span data-stu-id="f8670-124">Startup folders under the start menu for per user and public locations</span></span>

<span data-ttu-id="f8670-125">В Windows добавлены новые функции, гарантирующие, что конечные пользователи всегда управляют приложениями, выполняемыми на их системах.</span><span class="sxs-lookup"><span data-stu-id="f8670-125">New functionality has been added to Windows to ensure that end users are always in control of the apps that run on their systems.</span></span> <span data-ttu-id="f8670-126">На вкладке Автозагрузка в диспетчере задач отображается список запускаемых приложений, а также элементы управления, позволяющие пользователям отключить запускаемые приложения.</span><span class="sxs-lookup"><span data-stu-id="f8670-126">The Startup tab in Task Manager shows a list of startup apps, along with controls that allow users to disable startup apps.</span></span> <span data-ttu-id="f8670-127">Чтобы помочь пользователям определить, что следует отключить, в диспетчере задач отображается мера влияния каждого запускаемого приложения.</span><span class="sxs-lookup"><span data-stu-id="f8670-127">To help users determine what to disable, Task Manager displays a measure of each startup app s impact.</span></span> <span data-ttu-id="f8670-128">Оценка влияния зависит от использования ЦП и места на диске приложением при запуске.</span><span class="sxs-lookup"><span data-stu-id="f8670-128">Impact is assessed based on an app s CPU and disk usage at startup.</span></span> <span data-ttu-id="f8670-129">Значения влияния определяются применением следующих критериев:</span><span class="sxs-lookup"><span data-stu-id="f8670-129">Impact values are determined by applying these criteria:</span></span>

-   <span data-ttu-id="f8670-130">**Высокая степень влияния**   Приложения, использующие более 1 секунды времени ЦП или более 3 МБ дискового ввода-вывода при запуске</span><span class="sxs-lookup"><span data-stu-id="f8670-130">**High impact**   Apps that use more than 1 second of CPU time or more than 3 MB of disk I/O at startup</span></span>
-   <span data-ttu-id="f8670-131">**Средний уровень влияния**   Приложения, использующие 300 MS-1000 мс времени ЦП или 300 КБ – 3 МБ дискового ввода-вывода</span><span class="sxs-lookup"><span data-stu-id="f8670-131">**Medium impact**   Apps that use 300 ms - 1000 ms of CPU time or 300 KB - 3 MB of disk I/O</span></span>
-   <span data-ttu-id="f8670-132">**Низкая степень влияния**   Приложения, которые используют менее 300 мс времени ЦП и менее 300 КБ дискового ввода-вывода</span><span class="sxs-lookup"><span data-stu-id="f8670-132">**Low impact**   Apps that use less than 300 ms of CPU time and less than 300 KB of disk I/O</span></span>

<span data-ttu-id="f8670-133">Корпорация Майкрософт предоставляет средства, помогающие разработчикам приложений оценивать, анализировать и предпринимать меры для снижения влияния на запуск и улучшения взаимодействия с пользователем.</span><span class="sxs-lookup"><span data-stu-id="f8670-133">Microsoft provides tools to help app developers assess, analyze and take steps to reduce their startup impact and improve the user experience.</span></span> <span data-ttu-id="f8670-134">Комплект средств для оценки и развертывания позволяет выполнять оценку производительности загрузки и измерять влияние приложений, запускаемых при запуске.</span><span class="sxs-lookup"><span data-stu-id="f8670-134">The Assessment and Deployment Kit provides the ability to run a boot performance assessment and measure the impact of apps that run at startup.</span></span> <span data-ttu-id="f8670-135">Результаты оценки содержат подробный анализ и сведения об исправлении, где это возможно, для компонентов с наибольшим влиянием при запуске Windows.</span><span class="sxs-lookup"><span data-stu-id="f8670-135">The assessment results contain detailed analysis and remediation info where applicable, for the top-impacting components at Windows startup.</span></span> <span data-ttu-id="f8670-136">С помощью анализатора производительности Windows разработчики приложений могут выполнять глубокий анализ, чтобы найти основную причину влияния на производительность и повысить производительность запуска Windows.</span><span class="sxs-lookup"><span data-stu-id="f8670-136">Using the Windows Performance Analyzer, app developers can perform deep analysis to find the root cause of the performance impact and improve Windows startup performance.</span></span> <span data-ttu-id="f8670-137">Установите Windows ADK [отсюда.](/previous-versions/windows/hh825494(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="f8670-137">Install the Windows ADK from [here](/previous-versions/windows/hh825494(v=win.10)).</span></span>

## <a name="guidance"></a><span data-ttu-id="f8670-138">Руководство</span><span class="sxs-lookup"><span data-stu-id="f8670-138">Guidance</span></span>

<span data-ttu-id="f8670-139">Запускаемые приложения охватывают несколько категорий, как описано в таблице ниже.</span><span class="sxs-lookup"><span data-stu-id="f8670-139">Startup apps span multiple categories as described in the table below.</span></span> <span data-ttu-id="f8670-140">Набор рекомендаций для разработчиков сопоставляется со категориями автоматически запускаемых приложений для согласования с функциональными изменениями Windows, описанными выше.</span><span class="sxs-lookup"><span data-stu-id="f8670-140">A set of recommendations for developers is mapped to the categories of startup apps to align with the Windows functional changes described above.</span></span>



<span data-ttu-id="f8670-141">Категории запускаемых приложений</span><span class="sxs-lookup"><span data-stu-id="f8670-141">Startup Apps Categories</span></span>

<span data-ttu-id="f8670-142">Описание</span><span class="sxs-lookup"><span data-stu-id="f8670-142">Description</span></span>

<span data-ttu-id="f8670-143">Рекомендация</span><span class="sxs-lookup"><span data-stu-id="f8670-143">Recommendation</span></span>

<span data-ttu-id="f8670-144">**Предотвратят**</span><span class="sxs-lookup"><span data-stu-id="f8670-144">**Updaters**</span></span>

<span data-ttu-id="f8670-145">Мониторинг и обновление пользователей для интерактивных обновлений</span><span class="sxs-lookup"><span data-stu-id="f8670-145">Monitor and update users for online updates</span></span>

<span data-ttu-id="f8670-146">**Задача обслуживания**</span><span class="sxs-lookup"><span data-stu-id="f8670-146">**Maintenance Task**</span></span>

> [!Note]  
> <span data-ttu-id="f8670-147">Все обновления должны быть задачами обслуживания без каких бы то ни было требований к взаимодействию с ИП.</span><span class="sxs-lookup"><span data-stu-id="f8670-147">All updates should be maintenance tasks, without any UI interaction requirements.</span></span> <span data-ttu-id="f8670-148">Приложения должны быть беззвучно обновляться и выполнять откат при сбое</span><span class="sxs-lookup"><span data-stu-id="f8670-148">Apps should just update themselves quietly, and rollback on failure</span></span>

<br/>

<span data-ttu-id="f8670-149">$ {ROWSPAN2} $**помощь по оборудованию**$ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="f8670-149">${ROWSPAN2}$**Hardware Assistance**${REMOVE}$</span></span>  

<span data-ttu-id="f8670-150">Альтернативные точки доступа</span><span class="sxs-lookup"><span data-stu-id="f8670-150">Alternative Access Points</span></span>

<span data-ttu-id="f8670-151">Предоставление доступа к функциям и приложениям Windows, доступным через другие точки доступа в Windows</span><span class="sxs-lookup"><span data-stu-id="f8670-151">Provide access to Windows features and apps that are accessible via other access points in Windows</span></span>

<span data-ttu-id="f8670-152">**Удалить**</span><span class="sxs-lookup"><span data-stu-id="f8670-152">**Remove**</span></span>

> [!Note]  
> <span data-ttu-id="f8670-153">Ключ состоит в сокращении числа повторяющихся функций, существующих в Windows.</span><span class="sxs-lookup"><span data-stu-id="f8670-153">The key is to reduce duplicate features that exist in Windows</span></span>

<br/>

<span data-ttu-id="f8670-154">Уведомления</span><span class="sxs-lookup"><span data-stu-id="f8670-154">Notifiers</span></span>

<span data-ttu-id="f8670-155">Предоставление пользователям уведомлений о своих устройствах</span><span class="sxs-lookup"><span data-stu-id="f8670-155">Provide users with notifications regarding their devices</span></span>

<span data-ttu-id="f8670-156">**Удалить**</span><span class="sxs-lookup"><span data-stu-id="f8670-156">**Remove**</span></span>

> [!Note]  
> <span data-ttu-id="f8670-157">Windows предоставляет пользователям уведомления о своих устройствах.</span><span class="sxs-lookup"><span data-stu-id="f8670-157">Windows provides notifications to users about their devices</span></span>

<br/>

<span data-ttu-id="f8670-158">**Предварительные запуска**</span><span class="sxs-lookup"><span data-stu-id="f8670-158">**Pre-launchers**</span></span>

<span data-ttu-id="f8670-159">Некоторые предварительные действия, необходимые для приложений, перегружаются в запускаемое приложение во время входа пользователя.</span><span class="sxs-lookup"><span data-stu-id="f8670-159">Some of preliminary activities needed by apps is offloaded to a startup app during user login</span></span>

<span data-ttu-id="f8670-160">**Удалить**</span><span class="sxs-lookup"><span data-stu-id="f8670-160">**Remove**</span></span>

> [!Note]  
> <span data-ttu-id="f8670-161">Windows 8 оптимизирована для быстрого запуска приложений.</span><span class="sxs-lookup"><span data-stu-id="f8670-161">Windows 8 is optimized for a fast experience for app launches.</span></span>

<br/>

<span data-ttu-id="f8670-162">$ {ROWSPAN4} $**служебная программа**$ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="f8670-162">${ROWSPAN4}$**Utility**${REMOVE}$</span></span>  

<span data-ttu-id="f8670-163">Синхронизация ПК</span><span class="sxs-lookup"><span data-stu-id="f8670-163">PC Sync</span></span>

<span data-ttu-id="f8670-164">Обеспечение функций синхронизации в нескольких системах</span><span class="sxs-lookup"><span data-stu-id="f8670-164">Provide sync functionality across multiple systems</span></span>

<span data-ttu-id="f8670-165">**Запуск** (потенциальные обновления в бета-версии)</span><span class="sxs-lookup"><span data-stu-id="f8670-165">**Startup** (Potential updates in Beta)</span></span>

<span data-ttu-id="f8670-166">Восстановление & резервного копирования</span><span class="sxs-lookup"><span data-stu-id="f8670-166">Backup & Recovery</span></span>

<span data-ttu-id="f8670-167">Точка входа для сохранения и восстановления состояния файлов, параметров или целых систем</span><span class="sxs-lookup"><span data-stu-id="f8670-167">Entry point to save and restore the state of files, settings, or entire systems</span></span>

<span data-ttu-id="f8670-168">**Приложение Магазина Windows для взаимодействия с пользователями**</span><span class="sxs-lookup"><span data-stu-id="f8670-168">**Windows Store app for interfacing with the users**</span></span>

<span data-ttu-id="f8670-169">Телеметрия</span><span class="sxs-lookup"><span data-stu-id="f8670-169">Telemetry</span></span>

<span data-ttu-id="f8670-170">Собирайте и отправляйте сведения о пользовательском интерфейсе и среде.</span><span class="sxs-lookup"><span data-stu-id="f8670-170">Collect and send info about the user experience and environment</span></span>

<span data-ttu-id="f8670-171">**Задача обслуживания**</span><span class="sxs-lookup"><span data-stu-id="f8670-171">**Maintenance Task**</span></span>

<span data-ttu-id="f8670-172">Мониторинг ПК</span><span class="sxs-lookup"><span data-stu-id="f8670-172">PC Monitoring</span></span>

<span data-ttu-id="f8670-173">Предоставление незапрошенного мониторинга состояния системы и уведомлений, дублирующих существующие функции входящих сообщений</span><span class="sxs-lookup"><span data-stu-id="f8670-173">Provide unsolicited system state monitoring and notifications that duplicate existing inbox functionality</span></span>

<span data-ttu-id="f8670-174">**Удалить**</span><span class="sxs-lookup"><span data-stu-id="f8670-174">**Remove**</span></span>

> [!Note]  
> <span data-ttu-id="f8670-175">Ключ состоит в сокращении числа повторяющихся функций, существующих в Windows.</span><span class="sxs-lookup"><span data-stu-id="f8670-175">The key is to reduce duplicate features that exist in Windows</span></span>

<br/>

<span data-ttu-id="f8670-176">$ {ROWSPAN2} $**Security**$ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="f8670-176">${ROWSPAN2}$**Security**${REMOVE}$</span></span>  

<span data-ttu-id="f8670-177">Фильтры & родительского контроля</span><span class="sxs-lookup"><span data-stu-id="f8670-177">Parental Control & Filters</span></span>

<span data-ttu-id="f8670-178">Применение правил и ограничений, установленных для доступа к Интернету и их использования</span><span class="sxs-lookup"><span data-stu-id="f8670-178">Enforce rules and restrictions established for Internet access and usage</span></span>

<span data-ttu-id="f8670-179">**Запуск**</span><span class="sxs-lookup"><span data-stu-id="f8670-179">**Startup**</span></span>

<span data-ttu-id="f8670-180">Настройка и управление</span><span class="sxs-lookup"><span data-stu-id="f8670-180">Configuration & Management</span></span>

<span data-ttu-id="f8670-181">Разрешить пользователям управлять параметрами диагностики и исправления для мониторинга безопасности системы уведомлять пользователей о выводах и действиях по обеспечению безопасности</span><span class="sxs-lookup"><span data-stu-id="f8670-181">Allow users to control diagnostic and remediation options for system security monitoring Notify users of findings and security actions</span></span>

<span data-ttu-id="f8670-182">**Приложение Магазина Windows для взаимодействия с пользователями**</span><span class="sxs-lookup"><span data-stu-id="f8670-182">**Windows Store app for interfacing with the users**</span></span>

<span data-ttu-id="f8670-183">**Связь & Интернет** (IM & VoIP)</span><span class="sxs-lookup"><span data-stu-id="f8670-183">**Communication & Internet** (IM & VoIP)</span></span>

<span data-ttu-id="f8670-184">Отправка и получение сообщений и вызовов</span><span class="sxs-lookup"><span data-stu-id="f8670-184">Send and receive messages and calls</span></span>

<span data-ttu-id="f8670-185">**Приложение Магазина Windows**</span><span class="sxs-lookup"><span data-stu-id="f8670-185">**Windows Store app**</span></span>

<span data-ttu-id="f8670-186">**Музыка & MP3**</span><span class="sxs-lookup"><span data-stu-id="f8670-186">**Music & MP3**</span></span>

<span data-ttu-id="f8670-187">Воспроизведение музыки, хранение и управление музыкой</span><span class="sxs-lookup"><span data-stu-id="f8670-187">Play, store, and manage music</span></span>

<span data-ttu-id="f8670-188">**Приложение Магазина Windows**</span><span class="sxs-lookup"><span data-stu-id="f8670-188">**Windows Store app**</span></span>

<span data-ttu-id="f8670-189">**Фото & видео**</span><span class="sxs-lookup"><span data-stu-id="f8670-189">**Photo & Video**</span></span>

<span data-ttu-id="f8670-190">Обнаружение, запись, подготовка и хранение фотографий и видео, а затем управление ими</span><span class="sxs-lookup"><span data-stu-id="f8670-190">Detect, record, render, store and manage photos and videos</span></span>

<span data-ttu-id="f8670-191">**Приложение Магазина Windows**</span><span class="sxs-lookup"><span data-stu-id="f8670-191">**Windows Store app**</span></span>

<span data-ttu-id="f8670-192">**Компьютерные игры**</span><span class="sxs-lookup"><span data-stu-id="f8670-192">**PC Gaming**</span></span>

<span data-ttu-id="f8670-193">Запуск игр в различных доменах</span><span class="sxs-lookup"><span data-stu-id="f8670-193">Launch games across various domains</span></span>

<span data-ttu-id="f8670-194">**Приложение Магазина Windows**</span><span class="sxs-lookup"><span data-stu-id="f8670-194">**Windows Store app**</span></span>

<span data-ttu-id="f8670-195">**& объявление**</span><span class="sxs-lookup"><span data-stu-id="f8670-195">**Upsell & Advertisement**</span></span>

<span data-ttu-id="f8670-196">Привлечь внимание к товарам и услугам, доступным для покупки</span><span class="sxs-lookup"><span data-stu-id="f8670-196">Draw attention to goods and services available for purchase</span></span>

<span data-ttu-id="f8670-197">**Удалить**</span><span class="sxs-lookup"><span data-stu-id="f8670-197">**Remove**</span></span>



 

> [!Note]  
> <span data-ttu-id="f8670-198">Рекомендации по приложениям специальных возможностей покрываются отдельными прямыми обязательствами с ISV.</span><span class="sxs-lookup"><span data-stu-id="f8670-198">Accessibility apps guidelines are covered by separate direct engagements with ISVs.</span></span> <span data-ttu-id="f8670-199">Дополнительные сведения см. в разделе [*программирование для простоты доступа*](../winauto/ease-of-access---assistive-technology-registration.md) .</span><span class="sxs-lookup"><span data-stu-id="f8670-199">See [*Programming for Ease of Access*](../winauto/ease-of-access---assistive-technology-registration.md) for details.</span></span>

 

<span data-ttu-id="f8670-200">**Приложения для Магазина Windows**</span><span class="sxs-lookup"><span data-stu-id="f8670-200">**Windows Store apps**</span></span>

<span data-ttu-id="f8670-201">Приложения для Магазина Windows улучшают работу пользователей, представляя пространство Windows с новыми координатами: новую модель приложения, новый пользовательский интерфейс и магазин Windows.</span><span class="sxs-lookup"><span data-stu-id="f8670-201">Windows Store apps enhance the user experience by introducing a Windows space with new coordinates: a new app model, a new user interface, and a Windows Store.</span></span> <span data-ttu-id="f8670-202">Для разработки приложений для Магазина Windows доступны следующие параметры языка и представления платформы.</span><span class="sxs-lookup"><span data-stu-id="f8670-202">These language and presentation framework options are available for developing Windows Store apps:</span></span>

-   <span data-ttu-id="f8670-203">HTML/JavaScript/CSS</span><span class="sxs-lookup"><span data-stu-id="f8670-203">HTML/JavaScript/CSS</span></span>
-   <span data-ttu-id="f8670-204">XAML/C #</span><span class="sxs-lookup"><span data-stu-id="f8670-204">XAML/C#</span></span>
-   <span data-ttu-id="f8670-205">XAML/C++</span><span class="sxs-lookup"><span data-stu-id="f8670-205">XAML/C++</span></span>

<span data-ttu-id="f8670-206">Агрегированные сведения о разработке приложений для Магазина Windows доступны в [центре разработки для Windows](https://msdn.microsoft.com/windows/apps/).</span><span class="sxs-lookup"><span data-stu-id="f8670-206">Aggregated info for developing Windows Store apps is available at the [Windows Dev Center](https://msdn.microsoft.com/windows/apps/).</span></span>

<span data-ttu-id="f8670-207">Примеры:</span><span class="sxs-lookup"><span data-stu-id="f8670-207">Examples:</span></span>

-   <span data-ttu-id="f8670-208">[Разработка игр для Магазина Windows](/previous-versions/windows/apps/hh452744(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="f8670-208">[Developing Windows Store games](/previous-versions/windows/apps/hh452744(v=win.10))</span></span>
-   <span data-ttu-id="f8670-209">[Разработка приложения для Магазина Windows, использующего мультимедиа](/previous-versions/windows/apps/hh465132(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="f8670-209">[Developing Windows Store app that use Media](/previous-versions/windows/apps/hh465132(v=win.10))</span></span>

<span data-ttu-id="f8670-210">**Задачи автоматического обслуживания**</span><span class="sxs-lookup"><span data-stu-id="f8670-210">**Automatic maintenance tasks**</span></span>

<span data-ttu-id="f8670-211">Периодические фоновые действия должны быть спроектированы как задачи автоматического обслуживания.</span><span class="sxs-lookup"><span data-stu-id="f8670-211">Periodic background activity should be designed as Automatic Maintenance tasks.</span></span> <span data-ttu-id="f8670-212">Они планируются на время простоя системы, чтобы повысить скорость реагирования и экономичность компьютеров Windows.</span><span class="sxs-lookup"><span data-stu-id="f8670-212">These are scheduled at system idle time to increase the responsiveness and energy efficiency of Windows PCs.</span></span> <span data-ttu-id="f8670-213">Задачи обслуживания могут быть созданы и настроены в классическом приложении во время установки с помощью пакета SDK для настольных систем.</span><span class="sxs-lookup"><span data-stu-id="f8670-213">Maintenance tasks can be created and configured by a desktop app at install time, using the desktop SDK.</span></span> <span data-ttu-id="f8670-214">Дополнительные сведения см. в разделе Автоматическое обслуживание.</span><span class="sxs-lookup"><span data-stu-id="f8670-214">See the Automatic Maintenance topic that follows for details.</span></span>

## <a name="resources"></a><span data-ttu-id="f8670-215">Ресурсы</span><span class="sxs-lookup"><span data-stu-id="f8670-215">Resources</span></span>

-   [<span data-ttu-id="f8670-216">Рекомендации по специальным возможностям</span><span class="sxs-lookup"><span data-stu-id="f8670-216">Accessibility Guidelines</span></span>](../winauto/ease-of-access---assistive-technology-registration.md)
-   [<span data-ttu-id="f8670-217">Центр разработки для Windows</span><span class="sxs-lookup"><span data-stu-id="f8670-217">Windows Dev Center</span></span>](https://msdn.microsoft.com/windows/apps/)
-   <span data-ttu-id="f8670-218">[Windows ADK](/previous-versions/windows/hh825494(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="f8670-218">[Windows ADK](/previous-versions/windows/hh825494(v=win.10))</span></span>

 

