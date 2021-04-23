---
description: Таблица Сервицеинсталл используется для установки службы и содержит следующие столбцы.
ms.assetid: 81688d31-e560-4dd0-8d84-efb50206c76e
title: Таблица Сервицеинсталл
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b502583802a26c10bfd9572375149720c7c597f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663655"
---
# <a name="serviceinstall-table"></a><span data-ttu-id="51205-103">Таблица Сервицеинсталл</span><span class="sxs-lookup"><span data-stu-id="51205-103">ServiceInstall Table</span></span>

<span data-ttu-id="51205-104">Таблица Сервицеинсталл используется для установки службы и содержит следующие столбцы.</span><span class="sxs-lookup"><span data-stu-id="51205-104">The ServiceInstall table is used to install a service and has the following columns.</span></span>



| <span data-ttu-id="51205-105">Столбец</span><span class="sxs-lookup"><span data-stu-id="51205-105">Column</span></span>         | <span data-ttu-id="51205-106">Type</span><span class="sxs-lookup"><span data-stu-id="51205-106">Type</span></span>                               | <span data-ttu-id="51205-107">Ключ</span><span class="sxs-lookup"><span data-stu-id="51205-107">Key</span></span> | <span data-ttu-id="51205-108">Допускает значения NULL</span><span class="sxs-lookup"><span data-stu-id="51205-108">Nullable</span></span> |
|----------------|------------------------------------|-----|----------|
| <span data-ttu-id="51205-109">сервицеинсталл</span><span class="sxs-lookup"><span data-stu-id="51205-109">ServiceInstall</span></span> | [<span data-ttu-id="51205-110">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="51205-110">Identifier</span></span>](identifier.md)       | <span data-ttu-id="51205-111">Да</span><span class="sxs-lookup"><span data-stu-id="51205-111">Y</span></span>   | <span data-ttu-id="51205-112">Нет</span><span class="sxs-lookup"><span data-stu-id="51205-112">N</span></span>        |
| <span data-ttu-id="51205-113">Имя</span><span class="sxs-lookup"><span data-stu-id="51205-113">Name</span></span>           | [<span data-ttu-id="51205-114">Формате</span><span class="sxs-lookup"><span data-stu-id="51205-114">Formatted</span></span>](formatted.md)         | <span data-ttu-id="51205-115">Нет</span><span class="sxs-lookup"><span data-stu-id="51205-115">N</span></span>   | <span data-ttu-id="51205-116">Нет</span><span class="sxs-lookup"><span data-stu-id="51205-116">N</span></span>        |
| <span data-ttu-id="51205-117">DisplayName</span><span class="sxs-lookup"><span data-stu-id="51205-117">DisplayName</span></span>    | [<span data-ttu-id="51205-118">Формате</span><span class="sxs-lookup"><span data-stu-id="51205-118">Formatted</span></span>](formatted.md)         | <span data-ttu-id="51205-119">Нет</span><span class="sxs-lookup"><span data-stu-id="51205-119">N</span></span>   | <span data-ttu-id="51205-120">Да</span><span class="sxs-lookup"><span data-stu-id="51205-120">Y</span></span>        |
| <span data-ttu-id="51205-121">ServiceType</span><span class="sxs-lookup"><span data-stu-id="51205-121">ServiceType</span></span>    | [<span data-ttu-id="51205-122">даублеинтежер</span><span class="sxs-lookup"><span data-stu-id="51205-122">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="51205-123">Нет</span><span class="sxs-lookup"><span data-stu-id="51205-123">N</span></span>   | <span data-ttu-id="51205-124">Нет</span><span class="sxs-lookup"><span data-stu-id="51205-124">N</span></span>        |
| <span data-ttu-id="51205-125">StartType</span><span class="sxs-lookup"><span data-stu-id="51205-125">StartType</span></span>      | [<span data-ttu-id="51205-126">даублеинтежер</span><span class="sxs-lookup"><span data-stu-id="51205-126">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="51205-127">Нет</span><span class="sxs-lookup"><span data-stu-id="51205-127">N</span></span>   | <span data-ttu-id="51205-128">Нет</span><span class="sxs-lookup"><span data-stu-id="51205-128">N</span></span>        |
| <span data-ttu-id="51205-129">ErrorControl</span><span class="sxs-lookup"><span data-stu-id="51205-129">ErrorControl</span></span>   | [<span data-ttu-id="51205-130">даублеинтежер</span><span class="sxs-lookup"><span data-stu-id="51205-130">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="51205-131">Нет</span><span class="sxs-lookup"><span data-stu-id="51205-131">N</span></span>   | <span data-ttu-id="51205-132">Нет</span><span class="sxs-lookup"><span data-stu-id="51205-132">N</span></span>        |
| <span data-ttu-id="51205-133">LoadOrderGroup</span><span class="sxs-lookup"><span data-stu-id="51205-133">LoadOrderGroup</span></span> | [<span data-ttu-id="51205-134">Формате</span><span class="sxs-lookup"><span data-stu-id="51205-134">Formatted</span></span>](formatted.md)         | <span data-ttu-id="51205-135">Нет</span><span class="sxs-lookup"><span data-stu-id="51205-135">N</span></span>   | <span data-ttu-id="51205-136">Да</span><span class="sxs-lookup"><span data-stu-id="51205-136">Y</span></span>        |
| <span data-ttu-id="51205-137">Зависимости</span><span class="sxs-lookup"><span data-stu-id="51205-137">Dependencies</span></span>   | [<span data-ttu-id="51205-138">Формате</span><span class="sxs-lookup"><span data-stu-id="51205-138">Formatted</span></span>](formatted.md)         | <span data-ttu-id="51205-139">Нет</span><span class="sxs-lookup"><span data-stu-id="51205-139">N</span></span>   | <span data-ttu-id="51205-140">Да</span><span class="sxs-lookup"><span data-stu-id="51205-140">Y</span></span>        |
| <span data-ttu-id="51205-141">StartName</span><span class="sxs-lookup"><span data-stu-id="51205-141">StartName</span></span>      | [<span data-ttu-id="51205-142">Формате</span><span class="sxs-lookup"><span data-stu-id="51205-142">Formatted</span></span>](formatted.md)         | <span data-ttu-id="51205-143">Нет</span><span class="sxs-lookup"><span data-stu-id="51205-143">N</span></span>   | <span data-ttu-id="51205-144">Да</span><span class="sxs-lookup"><span data-stu-id="51205-144">Y</span></span>        |
| <span data-ttu-id="51205-145">Пароль</span><span class="sxs-lookup"><span data-stu-id="51205-145">Password</span></span>       | [<span data-ttu-id="51205-146">Формате</span><span class="sxs-lookup"><span data-stu-id="51205-146">Formatted</span></span>](formatted.md)         | <span data-ttu-id="51205-147">Нет</span><span class="sxs-lookup"><span data-stu-id="51205-147">N</span></span>   | <span data-ttu-id="51205-148">Да</span><span class="sxs-lookup"><span data-stu-id="51205-148">Y</span></span>        |
| <span data-ttu-id="51205-149">Аргументы</span><span class="sxs-lookup"><span data-stu-id="51205-149">Arguments</span></span>      | [<span data-ttu-id="51205-150">Формате</span><span class="sxs-lookup"><span data-stu-id="51205-150">Formatted</span></span>](formatted.md)         | <span data-ttu-id="51205-151">Нет</span><span class="sxs-lookup"><span data-stu-id="51205-151">N</span></span>   | <span data-ttu-id="51205-152">Да</span><span class="sxs-lookup"><span data-stu-id="51205-152">Y</span></span>        |
| <span data-ttu-id="51205-153">Компонент\_</span><span class="sxs-lookup"><span data-stu-id="51205-153">Component\_</span></span>    | [<span data-ttu-id="51205-154">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="51205-154">Identifier</span></span>](identifier.md)       | <span data-ttu-id="51205-155">Нет</span><span class="sxs-lookup"><span data-stu-id="51205-155">N</span></span>   | <span data-ttu-id="51205-156">Нет</span><span class="sxs-lookup"><span data-stu-id="51205-156">N</span></span>        |
| <span data-ttu-id="51205-157">Описание</span><span class="sxs-lookup"><span data-stu-id="51205-157">Description</span></span>    | [<span data-ttu-id="51205-158">Формате</span><span class="sxs-lookup"><span data-stu-id="51205-158">Formatted</span></span>](formatted.md)         | <span data-ttu-id="51205-159">Нет</span><span class="sxs-lookup"><span data-stu-id="51205-159">N</span></span>   | <span data-ttu-id="51205-160">Да</span><span class="sxs-lookup"><span data-stu-id="51205-160">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="51205-161">Столбцы</span><span class="sxs-lookup"><span data-stu-id="51205-161">Columns</span></span>

<dl> <dt>

<span data-ttu-id="51205-162"><span id="ServiceInstall"></span><span id="serviceinstall"></span><span id="SERVICEINSTALL"></span>сервицеинсталл</span><span class="sxs-lookup"><span data-stu-id="51205-162"><span id="ServiceInstall"></span><span id="serviceinstall"></span><span id="SERVICEINSTALL"></span>ServiceInstall</span></span>
</dt> <dd>

<span data-ttu-id="51205-163">Это первичный ключ для таблицы.</span><span class="sxs-lookup"><span data-stu-id="51205-163">This is the primary key for the table.</span></span>

</dd> <dt>

<span data-ttu-id="51205-164"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Безымян</span><span class="sxs-lookup"><span data-stu-id="51205-164"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span></span>
</dt> <dd>

<span data-ttu-id="51205-165">Этот столбец представляет собой строку, которая предоставляет имя службы для установки.</span><span class="sxs-lookup"><span data-stu-id="51205-165">This column is the string that gives the service name to install.</span></span> <span data-ttu-id="51205-166">Максимальная длина строки — 256 символов.</span><span class="sxs-lookup"><span data-stu-id="51205-166">The string has a maximum length of 256 characters.</span></span> <span data-ttu-id="51205-167">База данных диспетчера управления службами сохраняет регистр символов в имени службы, но при сравнении имен служб регистр не учитывается.</span><span class="sxs-lookup"><span data-stu-id="51205-167">The service control manager database preserves the case of the characters in the service name, but comparisons of service names are case insensitive.</span></span> <span data-ttu-id="51205-168">Прямые косая черта (/) и обратная косая черта ( \\ ) являются недопустимыми символами имени службы.</span><span class="sxs-lookup"><span data-stu-id="51205-168">Forward-slash (/) and back-slash (\\) are invalid service name characters.</span></span>

</dd> <dt>

<span data-ttu-id="51205-169"><span id="DisplayName"></span><span id="displayname"></span><span id="DISPLAYNAME"></span>DisplayName</span><span class="sxs-lookup"><span data-stu-id="51205-169"><span id="DisplayName"></span><span id="displayname"></span><span id="DISPLAYNAME"></span>DisplayName</span></span>
</dt> <dd>

<span data-ttu-id="51205-170">Этот столбец является локализуемой строкой, используемой программами пользовательского интерфейса для обнаружения службы.</span><span class="sxs-lookup"><span data-stu-id="51205-170">This column is the localizable string that user interface programs use to identify the service.</span></span> <span data-ttu-id="51205-171">Максимальная длина строки — 256 символов.</span><span class="sxs-lookup"><span data-stu-id="51205-171">The string has a maximum length of 256 characters.</span></span> <span data-ttu-id="51205-172">Диспетчер управления службами сохраняет регистр отображаемого имени, но при сравнении отображаемых имен регистр не учитывается.</span><span class="sxs-lookup"><span data-stu-id="51205-172">The service control manager preserves the case of the display name, but display name comparisons are case insensitive.</span></span>

</dd> <dt>

<span data-ttu-id="51205-173"><span id="ServiceType"></span><span id="servicetype"></span><span id="SERVICETYPE"></span>ServiceType</span><span class="sxs-lookup"><span data-stu-id="51205-173"><span id="ServiceType"></span><span id="servicetype"></span><span id="SERVICETYPE"></span>ServiceType</span></span>
</dt> <dd>

<span data-ttu-id="51205-174">Этот столбец представляет собой набор битовых флагов, указывающих тип службы.</span><span class="sxs-lookup"><span data-stu-id="51205-174">This column is a set of bit flags that specify the type of service.</span></span> <span data-ttu-id="51205-175">В этом столбце должен быть указан один из следующих типов служб.</span><span class="sxs-lookup"><span data-stu-id="51205-175">One of the following service types must be specified in this column.</span></span>



| <span data-ttu-id="51205-176">Тип службы</span><span class="sxs-lookup"><span data-stu-id="51205-176">Type of service</span></span>                | <span data-ttu-id="51205-177">Значение</span><span class="sxs-lookup"><span data-stu-id="51205-177">Value</span></span>      | <span data-ttu-id="51205-178">Описание</span><span class="sxs-lookup"><span data-stu-id="51205-178">Description</span></span>                                                                                                                                                                                                                  |
|--------------------------------|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51205-179">\_ \_ Собственный процесс Win32 \_ службы</span><span class="sxs-lookup"><span data-stu-id="51205-179">SERVICE\_WIN32\_OWN\_PROCESS</span></span>   | <span data-ttu-id="51205-180">0x00000010</span><span class="sxs-lookup"><span data-stu-id="51205-180">0x00000010</span></span> | <span data-ttu-id="51205-181">Служба Microsoft Win32, которая выполняет собственный процесс.</span><span class="sxs-lookup"><span data-stu-id="51205-181">A Microsoft Win32 service that runs its own process.</span></span>                                                                                                                                                                         |
| <span data-ttu-id="51205-182">\_ \_ Общий процесс Win32 \_ для службы</span><span class="sxs-lookup"><span data-stu-id="51205-182">SERVICE\_WIN32\_SHARE\_PROCESS</span></span> | <span data-ttu-id="51205-183">0x00000020</span><span class="sxs-lookup"><span data-stu-id="51205-183">0x00000020</span></span> | <span data-ttu-id="51205-184">Служба Win32, которая совместно использует процесс.</span><span class="sxs-lookup"><span data-stu-id="51205-184">A Win32 service that shares a process.</span></span>                                                                                                                                                                                       |
| <span data-ttu-id="51205-185">\_Интерактивный \_ процесс службы</span><span class="sxs-lookup"><span data-stu-id="51205-185">SERVICE\_INTERACTIVE\_PROCESS</span></span>  | <span data-ttu-id="51205-186">0x00000100</span><span class="sxs-lookup"><span data-stu-id="51205-186">0x00000100</span></span> | <span data-ttu-id="51205-187">Служба Win32, взаимодействующая с рабочим столом.</span><span class="sxs-lookup"><span data-stu-id="51205-187">A Win32 service that interacts with the desktop.</span></span> <span data-ttu-id="51205-188">Это значение не может использоваться отдельно и должно быть добавлено к одному из двух предыдущих типов. При использовании этого флага для столбца StartName должно быть задано значение LocalSystem или null.</span><span class="sxs-lookup"><span data-stu-id="51205-188">This value cannot be used alone and must be added to one of the two previous types.The StartName column must be set to LocalSystem or null when using this flag.</span></span><br/> |



 

<span data-ttu-id="51205-189">Следующие типы служб не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="51205-189">The following types of service are unsupported.</span></span>



| <span data-ttu-id="51205-190">Тип службы</span><span class="sxs-lookup"><span data-stu-id="51205-190">Type of service</span></span>               | <span data-ttu-id="51205-191">Значение</span><span class="sxs-lookup"><span data-stu-id="51205-191">Value</span></span>      | <span data-ttu-id="51205-192">Описание</span><span class="sxs-lookup"><span data-stu-id="51205-192">Description</span></span>                   |
|-------------------------------|------------|-------------------------------|
| <span data-ttu-id="51205-193">\_драйвер ядра \_ службы</span><span class="sxs-lookup"><span data-stu-id="51205-193">SERVICE\_KERNEL\_DRIVER</span></span>       | <span data-ttu-id="51205-194">0x00000001</span><span class="sxs-lookup"><span data-stu-id="51205-194">0x00000001</span></span> | <span data-ttu-id="51205-195">Служба драйверов.</span><span class="sxs-lookup"><span data-stu-id="51205-195">A driver service.</span></span>             |
| <span data-ttu-id="51205-196">\_драйвер файловой \_ системы \_ службы</span><span class="sxs-lookup"><span data-stu-id="51205-196">SERVICE\_FILE\_SYSTEM\_DRIVER</span></span> | <span data-ttu-id="51205-197">0x00000002</span><span class="sxs-lookup"><span data-stu-id="51205-197">0x00000002</span></span> | <span data-ttu-id="51205-198">Служба драйвера файловой системы.</span><span class="sxs-lookup"><span data-stu-id="51205-198">A file system driver service.</span></span> |



 

</dd> <dt>

<span data-ttu-id="51205-199"><span id="StartType"></span><span id="starttype"></span><span id="STARTTYPE"></span>старттипе</span><span class="sxs-lookup"><span data-stu-id="51205-199"><span id="StartType"></span><span id="starttype"></span><span id="STARTTYPE"></span>StartType</span></span>
</dt> <dd>

<span data-ttu-id="51205-200">Этот столбец представляет собой набор битовых флагов, указывающих время запуска службы.</span><span class="sxs-lookup"><span data-stu-id="51205-200">This column is a set of bit flags that specify when to start the service.</span></span> <span data-ttu-id="51205-201">В этом столбце должен быть указан один из следующих типов запуска службы.</span><span class="sxs-lookup"><span data-stu-id="51205-201">One of the following types of service start must be specified in this column.</span></span>



| <span data-ttu-id="51205-202">Тип запуска службы</span><span class="sxs-lookup"><span data-stu-id="51205-202">Type of service start</span></span>  | <span data-ttu-id="51205-203">Значение</span><span class="sxs-lookup"><span data-stu-id="51205-203">Value</span></span>      | <span data-ttu-id="51205-204">Описание</span><span class="sxs-lookup"><span data-stu-id="51205-204">Description</span></span>                                                                                                |
|------------------------|------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51205-205">\_Автоматический \_ Запуск службы</span><span class="sxs-lookup"><span data-stu-id="51205-205">SERVICE\_AUTO\_START</span></span>   | <span data-ttu-id="51205-206">0x00000002</span><span class="sxs-lookup"><span data-stu-id="51205-206">0x00000002</span></span> | <span data-ttu-id="51205-207">Запуск службы во время запуска системы.</span><span class="sxs-lookup"><span data-stu-id="51205-207">A service start during startup of the system.</span></span>                                                              |
| <span data-ttu-id="51205-208">\_Запуск запроса на обслуживание \_</span><span class="sxs-lookup"><span data-stu-id="51205-208">SERVICE\_DEMAND\_START</span></span> | <span data-ttu-id="51205-209">0x00000003</span><span class="sxs-lookup"><span data-stu-id="51205-209">0x00000003</span></span> | <span data-ttu-id="51205-210">Служба запускается, когда диспетчер управления службами вызывает функцию [**StartService**](/windows/win32/api/winsvc/nf-winsvc-startservicea) .</span><span class="sxs-lookup"><span data-stu-id="51205-210">A service start when the service control manager calls the [**StartService**](/windows/win32/api/winsvc/nf-winsvc-startservicea) function.</span></span> |
| <span data-ttu-id="51205-211">Служба \_ отключена</span><span class="sxs-lookup"><span data-stu-id="51205-211">SERVICE\_DISABLED</span></span>      | <span data-ttu-id="51205-212">0x00000004</span><span class="sxs-lookup"><span data-stu-id="51205-212">0x00000004</span></span> | <span data-ttu-id="51205-213">Указывает службу, которая больше не может быть запущена.</span><span class="sxs-lookup"><span data-stu-id="51205-213">Specifies a service that can no longer be started.</span></span>                                                         |



 

<span data-ttu-id="51205-214">Установщик Windows не может использовать параметры запуска \_ \_ запуска службы и \_ системы службы \_ .</span><span class="sxs-lookup"><span data-stu-id="51205-214">The Windows Installer cannot use the SERVICE\_BOOT\_START and SERVICE\_SYSTEM\_START options.</span></span>

</dd> <dt>

<span data-ttu-id="51205-215"><span id="ErrorControl"></span><span id="errorcontrol"></span><span id="ERRORCONTROL"></span>ErrorControl</span><span class="sxs-lookup"><span data-stu-id="51205-215"><span id="ErrorControl"></span><span id="errorcontrol"></span><span id="ERRORCONTROL"></span>ErrorControl</span></span>
</dt> <dd>

<span data-ttu-id="51205-216">В этом столбце указывается действие, предпринимаемое программой запуска, если не удается запустить службу во время запуска.</span><span class="sxs-lookup"><span data-stu-id="51205-216">This column specifies the action taken by the startup program if the service fails to start during startup.</span></span> <span data-ttu-id="51205-217">Эти значения влияют на события ServiceControl StartService для установленных служб.</span><span class="sxs-lookup"><span data-stu-id="51205-217">These values affect the ServiceControl StartService events for installed services.</span></span> <span data-ttu-id="51205-218">В этом столбце должен быть указан один из следующих флагов управления ошибками.</span><span class="sxs-lookup"><span data-stu-id="51205-218">One of the following error control flags must be specified in this column.</span></span>

<span data-ttu-id="51205-219">Добавление константы **мсидбсервицеинсталлеррорконтролвитал** (value = 0x08000) к флагам в следующей таблице указывает на то, что общая установка должна завершиться ошибкой, если не удается установить службу в системе.</span><span class="sxs-lookup"><span data-stu-id="51205-219">Adding the constant **msidbServiceInstallErrorControlVital** (value = 0x08000) to the flags in the following table specifies that the overall install should fail if the service cannot be installed into the system.</span></span>



| <span data-ttu-id="51205-220">Флаг управления ошибками</span><span class="sxs-lookup"><span data-stu-id="51205-220">Error control flag</span></span>       | <span data-ttu-id="51205-221">Значение</span><span class="sxs-lookup"><span data-stu-id="51205-221">Value</span></span>      | <span data-ttu-id="51205-222">Действие программы запуска</span><span class="sxs-lookup"><span data-stu-id="51205-222">Startup program's action</span></span>                                                                                                                                                                       |
|--------------------------|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51205-223">Ошибка службы — \_ \_ пропустить</span><span class="sxs-lookup"><span data-stu-id="51205-223">SERVICE\_ERROR\_IGNORE</span></span>   | <span data-ttu-id="51205-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="51205-224">0x00000000</span></span> | <span data-ttu-id="51205-225">Записывает в журнал ошибку и переходит к выполнению операции запуска.</span><span class="sxs-lookup"><span data-stu-id="51205-225">Logs the error and continues with the startup operation.</span></span>                                                                                                                                       |
| <span data-ttu-id="51205-226">Ошибка службы — \_ \_ Обычная</span><span class="sxs-lookup"><span data-stu-id="51205-226">SERVICE\_ERROR\_NORMAL</span></span>   | <span data-ttu-id="51205-227">0x00000001</span><span class="sxs-lookup"><span data-stu-id="51205-227">0x00000001</span></span> | <span data-ttu-id="51205-228">Записывает в журнал ошибку, отображает окно сообщения и возобновляет операцию запуска.</span><span class="sxs-lookup"><span data-stu-id="51205-228">Logs the error, displays a message box and continues the startup operation.</span></span>                                                                                                                    |
| <span data-ttu-id="51205-229">\_ \_ критическая ошибка службы</span><span class="sxs-lookup"><span data-stu-id="51205-229">SERVICE\_ERROR\_CRITICAL</span></span> | <span data-ttu-id="51205-230">0x00000003</span><span class="sxs-lookup"><span data-stu-id="51205-230">0x00000003</span></span> | <span data-ttu-id="51205-231">Регистрирует ошибку, если это возможно, а система перезапускается с последней конфигурацией, которая хорошо известна.</span><span class="sxs-lookup"><span data-stu-id="51205-231">Logs the error if it is possible and the system is restarted with the last configuration known to be good.</span></span> <span data-ttu-id="51205-232">При запуске последней удачной конфигурации операция запуска завершается ошибкой.</span><span class="sxs-lookup"><span data-stu-id="51205-232">If the last-known-good configuration is being started, the startup operation fails.</span></span> |



 

</dd> <dt>

<span data-ttu-id="51205-233"><span id="LoadOrderGroup"></span><span id="loadordergroup"></span><span id="LOADORDERGROUP"></span>лоадордерграуп</span><span class="sxs-lookup"><span data-stu-id="51205-233"><span id="LoadOrderGroup"></span><span id="loadordergroup"></span><span id="LOADORDERGROUP"></span>LoadOrderGroup</span></span>
</dt> <dd>

<span data-ttu-id="51205-234">Этот столбец содержит строку с именем группы порядка загрузки, членом которой является эта служба.</span><span class="sxs-lookup"><span data-stu-id="51205-234">This column contains the string that names the load ordering group of which this service is a member.</span></span> <span data-ttu-id="51205-235">Если служба не принадлежит группе, укажите значение null или пустую строку.</span><span class="sxs-lookup"><span data-stu-id="51205-235">Specify null or an empty string if the service does not belong to a group.</span></span>

</dd> <dt>

<span data-ttu-id="51205-236"><span id="Dependencies"></span><span id="dependencies"></span><span id="DEPENDENCIES"></span>Сборки</span><span class="sxs-lookup"><span data-stu-id="51205-236"><span id="Dependencies"></span><span id="dependencies"></span><span id="DEPENDENCIES"></span>Dependencies</span></span>
</dt> <dd>

<span data-ttu-id="51205-237">Этот столбец представляет собой список имен служб или групп порядка загрузки, которые система должна запустить перед этой службой.</span><span class="sxs-lookup"><span data-stu-id="51205-237">This column is a list of names of services or load ordering groups that the system must start before this service.</span></span> <span data-ttu-id="51205-238">Разделяйте имена значениями NULL в списке.</span><span class="sxs-lookup"><span data-stu-id="51205-238">Separate names in the list by Nulls.</span></span> <span data-ttu-id="51205-239">Если служба не имеет зависимостей, укажите значение null или пустую строку.</span><span class="sxs-lookup"><span data-stu-id="51205-239">If the service has no dependencies, then specify Null or an empty string.</span></span> <span data-ttu-id="51205-240">Используйте синтаксис \[ ~ \] для вставки значения NULL.</span><span class="sxs-lookup"><span data-stu-id="51205-240">Use the syntax \[~\] to insert a Null.</span></span> <span data-ttu-id="51205-241">Зависимость от группы означает, что эту службу можно запустить, если хотя бы один член группы запущен после попытки запуска всех членов группы.</span><span class="sxs-lookup"><span data-stu-id="51205-241">Dependency on a group means that this service can run if at least one member of the group is running after an attempt to start all members of the group.</span></span>

<span data-ttu-id="51205-242">Например, чтобы затребовать, чтобы система запускала Service1 и S2, перед запуском службы, указанной в столбце сервицеинсталл, введите Service1 \[ ~ \] S2 \[ ~ \] \[ ~ \] в столбец зависимости.</span><span class="sxs-lookup"><span data-stu-id="51205-242">For example, to require that the system start service1 and service2, before starting the service listed in the ServiceInstall column, enter service1\[~\]service2\[~\]\[~\] into the Dependencies column.</span></span> <span data-ttu-id="51205-243">Идентификаторы Service1 и S2 должны либо находиться в первичном ключе таблицы, либо быть именем уже установленной службы.</span><span class="sxs-lookup"><span data-stu-id="51205-243">The identifiers service1 and service2 must either occur in the primary key of the table or be the name of the service that is already installed.</span></span>

<span data-ttu-id="51205-244">Имена групп должны иметь префикс +, чтобы их можно было отличать от имени службы.</span><span class="sxs-lookup"><span data-stu-id="51205-244">You must prefix group names with + so that they can be distinguished from a service name.</span></span> <span data-ttu-id="51205-245">Чтобы затребовать, чтобы система запускала Service1 и хотя бы один член группы упорядочения MyGroup перед запуском службы, указанной в столбце сервицеинсталл, введите Service1 \[ ~ \] + MyGroup \[ ~ \] \[ ~ \] .</span><span class="sxs-lookup"><span data-stu-id="51205-245">To require that the system start service1 and at least one member of the ordering group MyGroup before starting the service listed in the ServiceInstall column, enter service1\[~\]+MyGroup\[~\]\[~\].</span></span>

</dd> <dt>

<span data-ttu-id="51205-246"><span id="StartName"></span><span id="startname"></span><span id="STARTNAME"></span>StartName</span><span class="sxs-lookup"><span data-stu-id="51205-246"><span id="StartName"></span><span id="startname"></span><span id="STARTNAME"></span>StartName</span></span>
</dt> <dd>

<span data-ttu-id="51205-247">Служба входит в систему как имя, заданное строкой в этом столбце.</span><span class="sxs-lookup"><span data-stu-id="51205-247">The service is logged on as the name given by the string in this column.</span></span> <span data-ttu-id="51205-248">Если тип службы является \_ \_ собственным процессом Win32, \_ Используйте имя учетной записи в формате имя_домена \\ имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="51205-248">If the service type is SERVICE\_WIN32\_OWN\_PROCESS use an account name in the form: DomainName\\UserName.</span></span> <span data-ttu-id="51205-249">Если учетная запись принадлежит встроенному домену, ей разрешается указывать. \\ Имен.</span><span class="sxs-lookup"><span data-stu-id="51205-249">If the account belongs to the built-in domain it is permitted to specify .\\UserName.</span></span> <span data-ttu-id="51205-250">Учетная запись LocalSystem должна использоваться, если типом службы является служба \_ \_ общих процессов Win32 \_ или \_ Интерактивный \_ процесс службы.</span><span class="sxs-lookup"><span data-stu-id="51205-250">The LocalSystem account must be used if the type of service is SERVICE\_WIN32\_SHARE\_PROCESS or SERVICE\_INTERACTIVE\_PROCESS.</span></span> <span data-ttu-id="51205-251">Функция [**CreateService**](/windows/win32/api/winsvc/nf-winsvc-createservicea) использует учетную запись LocalSystem, если параметру StartName задано значение NULL и большинство служб, поэтому оставить этот столбец пустым.</span><span class="sxs-lookup"><span data-stu-id="51205-251">The [**CreateService**](/windows/win32/api/winsvc/nf-winsvc-createservicea) function uses the LocalSystem account if StartName is specified as null and most services therefore leave this column blank.</span></span>

</dd> <dt>

<span data-ttu-id="51205-252"><span id="Password"></span><span id="password"></span><span id="PASSWORD"></span>Пароль</span><span class="sxs-lookup"><span data-stu-id="51205-252"><span id="Password"></span><span id="password"></span><span id="PASSWORD"></span>Password</span></span>
</dt> <dd>

<span data-ttu-id="51205-253">Эта строка представляет собой пароль для имени учетной записи, указанной в столбце StartName.</span><span class="sxs-lookup"><span data-stu-id="51205-253">This string is the password to the account name specified in the StartName column.</span></span> <span data-ttu-id="51205-254">Обратите внимание, что пользователь должен иметь разрешения на вход в систему в качестве службы.</span><span class="sxs-lookup"><span data-stu-id="51205-254">Note that the user must have permissions to log on as a service.</span></span> <span data-ttu-id="51205-255">Служба не имеет пароля, если значение StartName равно null или является пустой строкой.</span><span class="sxs-lookup"><span data-stu-id="51205-255">The service has no password if StartName is null or an empty string.</span></span> <span data-ttu-id="51205-256">Значение StartName для LocalSystem равно null, поэтому пароль в этом экземпляре равен null, поэтому большинство служб оставляет этот столбец пустым.</span><span class="sxs-lookup"><span data-stu-id="51205-256">The Startname of LocalSystem is null, and therefore the password in this instance is null, so most services leave this column blank.</span></span>

<span data-ttu-id="51205-257">Обратите внимание, что после удаления службы, которая была установлена с именем пользователя и паролем, установщик не сможет выполнить откат службы без предварительного использования настраиваемого действия для получения пароля.</span><span class="sxs-lookup"><span data-stu-id="51205-257">Note that after deleting a service that was installed with a user name and password, the installer cannot rollback the service without first using a custom action to get the password.</span></span> <span data-ttu-id="51205-258">Установщик может получить все необходимые сведения о службе, за исключением пароля, который хранится в защищенной части системы.</span><span class="sxs-lookup"><span data-stu-id="51205-258">The installer can acquire all the necessary information about the service except the password, which is stored in a protected part of the system.</span></span> <span data-ttu-id="51205-259">Пользовательское действие получает пароль, запрашивая пользователя, считывая свойство из базы данных или считывая файл.</span><span class="sxs-lookup"><span data-stu-id="51205-259">The custom action acquires the password by prompting the user, reading a property from the database, or reading a file.</span></span> <span data-ttu-id="51205-260">После этого пользовательское действие должно вызвать [**чанжесервицеконфиг**](/windows/win32/api/winsvc/nf-winsvc-changeserviceconfiga)для указания пароля перед переустановкой службы.</span><span class="sxs-lookup"><span data-stu-id="51205-260">The custom action must then call [**ChangeServiceConfig**](/windows/win32/api/winsvc/nf-winsvc-changeserviceconfiga), to supply the password, before reinstalling the service.</span></span>

<span data-ttu-id="51205-261">Установщик Windows не записывает значение, указанное в поле пароль, в файл журнала.</span><span class="sxs-lookup"><span data-stu-id="51205-261">Windows Installer does not write the value entered into the Password field into the log file.</span></span>

</dd> <dt>

<span data-ttu-id="51205-262"><span id="Arguments"></span><span id="arguments"></span><span id="ARGUMENTS"></span>Даваемых</span><span class="sxs-lookup"><span data-stu-id="51205-262"><span id="Arguments"></span><span id="arguments"></span><span id="ARGUMENTS"></span>Arguments</span></span>
</dt> <dd>

<span data-ttu-id="51205-263">Этот столбец содержит все аргументы командной строки или свойства, необходимые для запуска службы.</span><span class="sxs-lookup"><span data-stu-id="51205-263">This column contains any command line arguments or properties required to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="51205-264"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>См\_</span><span class="sxs-lookup"><span data-stu-id="51205-264"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="51205-265">Внешний ключ к столбцу одной из [таблиц Component](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="51205-265">External key to column one of the [Component Table](component-table.md).</span></span> <span data-ttu-id="51205-266">Обратите внимание, что для установки этой службы с помощью таблицы Инсталлсервице ключевой путь для этого компонента должен быть исполняемым файлом для службы.</span><span class="sxs-lookup"><span data-stu-id="51205-266">Note that to install this service using the InstallService table, the KeyPath for this component must be the executable file for the service.</span></span>

</dd> <dt>

<span data-ttu-id="51205-267"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Nописание</span><span class="sxs-lookup"><span data-stu-id="51205-267"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="51205-268">Этот столбец содержит Локализуемое описание для настраиваемой службы.</span><span class="sxs-lookup"><span data-stu-id="51205-268">This column contains a localizable description for the service being configured.</span></span> <span data-ttu-id="51205-269">Если этот столбец остается пустым, установщик использует существующее описание службы, если оно существует.</span><span class="sxs-lookup"><span data-stu-id="51205-269">If this column is left blank the installer uses the existing description of the service if one exists.</span></span> <span data-ttu-id="51205-270">Дополнительные сведения см \_ . в статье Описание службы в пакете средств разработки программного обеспечения (SDK) для Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="51205-270">For more information, see SERVICE\_DESCRIPTION in the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="51205-271">Чтобы стереть существующее описание, введите " \[ ~ \] " в этом столбце.</span><span class="sxs-lookup"><span data-stu-id="51205-271">To erase an existing description enter "\[~\]" in this column.</span></span> <span data-ttu-id="51205-272">Это приводит к пустому описанию для новой или существующей службы.</span><span class="sxs-lookup"><span data-stu-id="51205-272">This results in a blank description for either a new or existing service.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="51205-273">Комментарии</span><span class="sxs-lookup"><span data-stu-id="51205-273">Remarks</span></span>

<span data-ttu-id="51205-274">Действие [инсталлсервицес](installservices-action.md) в [*таблицах последовательностей*](s-gly.md) обрабатывает сведения в этой таблице.</span><span class="sxs-lookup"><span data-stu-id="51205-274">The [InstallServices](installservices-action.md) action in [*sequence tables*](s-gly.md) processes the information in this table.</span></span> <span data-ttu-id="51205-275">Дополнительные сведения об использовании *таблиц последовательности* см. [в разделе Использование таблицы последовательностей](using-a-sequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="51205-275">For information about using *sequence tables*, see [Using a Sequence Table](using-a-sequence-table.md).</span></span>

<span data-ttu-id="51205-276">Эта таблица имеет большую часть параметров функции Win32 [**CreateService**](/windows/win32/api/winsvc/nf-winsvc-createservicea) .</span><span class="sxs-lookup"><span data-stu-id="51205-276">This table has most of the parameters to the Win32 [**CreateService**](/windows/win32/api/winsvc/nf-winsvc-createservicea) function.</span></span>

<span data-ttu-id="51205-277">Хотя можно использовать пользовательский интерфейс, чтобы указать, что служба должна быть установлена как запускаемая из исходного кода, установщик на самом деле не поддерживает этот тип установки.</span><span class="sxs-lookup"><span data-stu-id="51205-277">Although it is possible to use the user interface to specify that a service be installed as run-from-source, the installer does not actually support this type of installation.</span></span> <span data-ttu-id="51205-278">Службы, запускаемые с уровнем привилегий локальной системы, должны быть установлены для запуска с локального жесткого диска.</span><span class="sxs-lookup"><span data-stu-id="51205-278">Services that run with the privilege level of the local system must be installed to run from the local hard drive.</span></span> <span data-ttu-id="51205-279">Избегайте установки служб, имитирующих привилегии конкретного пользователя, так как это может записать данные безопасности в журнал или системный реестр.</span><span class="sxs-lookup"><span data-stu-id="51205-279">Avoid installing services that impersonate the privileges of a particular user because this may write security data into a log or the system registry.</span></span> <span data-ttu-id="51205-280">Это может вызвать проблемы безопасности, конфликт паролей или потери данных конфигурации при перезапуске системы.</span><span class="sxs-lookup"><span data-stu-id="51205-280">This can potentially create a security problem, password conflict, or the loss of configuration data when the system is restarted.</span></span>

<span data-ttu-id="51205-281">Чтобы удалить службу во время удаления, должна быть соответствующая запись для службы в [таблице ServiceControl](servicecontrol-table.md) , а флаг **мсидбсервицеконтролевентунинсталлделете** должен появиться в столбце событий.</span><span class="sxs-lookup"><span data-stu-id="51205-281">To delete a service during an uninstallation, there must be a corresponding record for the service in the [ServiceControl table](servicecontrol-table.md) and the **msidbServiceControlEventUninstallDelete** flag must appear in the Event column.</span></span> <span data-ttu-id="51205-282">Установщик не удаляет службу в таблице Сервицеинсталл во время удаления без этой записи в таблице ServiceControl.</span><span class="sxs-lookup"><span data-stu-id="51205-282">The installer does not delete a service in the ServiceInstall table during uninstallation without this entry in the ServiceControl table.</span></span>

<span data-ttu-id="51205-283">Сведения о защите службы см. в [таблице мсилоккпермиссионсекс](msilockpermissionsex-table.md).</span><span class="sxs-lookup"><span data-stu-id="51205-283">For information on how to secure a service see the [MsiLockPermissionsEx Table](msilockpermissionsex-table.md).</span></span>

## <a name="validation"></a><span data-ttu-id="51205-284">Проверка</span><span class="sxs-lookup"><span data-stu-id="51205-284">Validation</span></span>

<dl>

[<span data-ttu-id="51205-285">ICE03</span><span class="sxs-lookup"><span data-stu-id="51205-285">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="51205-286">ICE06</span><span class="sxs-lookup"><span data-stu-id="51205-286">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="51205-287">ICE32</span><span class="sxs-lookup"><span data-stu-id="51205-287">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="51205-288">ICE45</span><span class="sxs-lookup"><span data-stu-id="51205-288">ICE45</span></span>](ice45.md)  
[<span data-ttu-id="51205-289">ICE46</span><span class="sxs-lookup"><span data-stu-id="51205-289">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="51205-290">ICE66</span><span class="sxs-lookup"><span data-stu-id="51205-290">ICE66</span></span>](ice66.md)  
[<span data-ttu-id="51205-291">ICE69</span><span class="sxs-lookup"><span data-stu-id="51205-291">ICE69</span></span>](ice69.md)  
</dl>

 

 
