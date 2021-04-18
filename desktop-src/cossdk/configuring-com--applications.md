---
description: Приложение COM+ — это, по сути, декларативная конструкция, которая позволяет настроить любое общее количество компонентов. Например, можно настроить компоненты в приложении с помощью общей политики безопасности.
ms.assetid: 50039b30-1c91-4e93-9f23-873accb651cf
title: Настройка приложений COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16319baf7e34348751e9cafd0efcbd99906d0985
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701180"
---
# <a name="configuring-com-applications"></a><span data-ttu-id="4c435-104">Настройка приложений COM+</span><span class="sxs-lookup"><span data-stu-id="4c435-104">Configuring COM+ Applications</span></span>

<span data-ttu-id="4c435-105">Приложение COM+ — это, по сути, декларативная конструкция, которая позволяет настроить любое общее количество компонентов.</span><span class="sxs-lookup"><span data-stu-id="4c435-105">A COM+ application is essentially a declarative construct that enables you to configure any number of components in common.</span></span> <span data-ttu-id="4c435-106">Например, можно настроить компоненты в приложении с помощью общей политики безопасности.</span><span class="sxs-lookup"><span data-stu-id="4c435-106">For example, you can configure the components in an application with a common security policy.</span></span>

<span data-ttu-id="4c435-107">Настройка является важнейшей частью процесса разработки приложений COM+.</span><span class="sxs-lookup"><span data-stu-id="4c435-107">Configuration is an essential part of the development process for COM+ applications.</span></span> <span data-ttu-id="4c435-108">Настройка приложения определяет, как COM+ будет предоставлять службы для него и как он работает при запуске.</span><span class="sxs-lookup"><span data-stu-id="4c435-108">How you configure an application will determine how COM+ will provide services for it and how it behaves when running.</span></span>

<span data-ttu-id="4c435-109">Вы можете настроить приложения COM+ с помощью средства администрирования служб компонентов или сценариев объектов администрирования и интерфейсов, которые предоставляют базовые функциональные возможности средства администрирования.</span><span class="sxs-lookup"><span data-stu-id="4c435-109">You can configure COM+ applications using either the Component Services administration tool or the scriptable administration objects and interfaces that provide the underlying functionality of the administration tool.</span></span> <span data-ttu-id="4c435-110">Дополнительные сведения о выполнении сценариев администрирования см. в разделе [Автоматизация администрирования com+](automating-com--administration.md).</span><span class="sxs-lookup"><span data-stu-id="4c435-110">For details on performing scripted administration, see [Automating COM+ Administration](automating-com--administration.md).</span></span>

<span data-ttu-id="4c435-111">Элементы можно настроить на следующих уровнях в приложениях COM+:</span><span class="sxs-lookup"><span data-stu-id="4c435-111">You can configure elements at the following levels within COM+ applications:</span></span>

-   [<span data-ttu-id="4c435-112">Параметры уровня приложения</span><span class="sxs-lookup"><span data-stu-id="4c435-112">Application-Level Settings</span></span>](#application-level-settings)
-   [<span data-ttu-id="4c435-113">Параметры уровня компонента (уровня класса)</span><span class="sxs-lookup"><span data-stu-id="4c435-113">Component-Level (Class-Level) Settings</span></span>](#component-level-class-level-settings)
-   [<span data-ttu-id="4c435-114">Настройка уровня интерфейса</span><span class="sxs-lookup"><span data-stu-id="4c435-114">Interface-Level Setting</span></span>](#interface-level-setting)
-   [<span data-ttu-id="4c435-115">Настройка уровня метода</span><span class="sxs-lookup"><span data-stu-id="4c435-115">Method-Level Setting</span></span>](#method-level-setting)
-   [<span data-ttu-id="4c435-116">См. также</span><span class="sxs-lookup"><span data-stu-id="4c435-116">Related topics</span></span>](#related-topics)

<span data-ttu-id="4c435-117">Установка компонентов в приложение может повлиять на их настройку.</span><span class="sxs-lookup"><span data-stu-id="4c435-117">How you install components into an application can affect how you can configure them.</span></span> <span data-ttu-id="4c435-118">Компоненты всегда следует устанавливать в приложения COM+ (в отличие от их импорта).</span><span class="sxs-lookup"><span data-stu-id="4c435-118">You should always install components into COM+ applications (as opposed to importing them).</span></span> <span data-ttu-id="4c435-119">При установке компонентов они будут полностью зарегистрированы вместе с интерфейсами и библиотеками типов в базе данных регистрации классов COM+ (Регдб), чтобы их можно было настроить.</span><span class="sxs-lookup"><span data-stu-id="4c435-119">Installing components will fully register them, along with interfaces and type libraries, in the COM+ class registration database (RegDB) so that you can configure them.</span></span>

## <a name="application-level-settings"></a><span data-ttu-id="4c435-120">Параметры Application-Level</span><span class="sxs-lookup"><span data-stu-id="4c435-120">Application-Level Settings</span></span>



| <span data-ttu-id="4c435-121">attribute</span><span class="sxs-lookup"><span data-stu-id="4c435-121">Attribute</span></span>                                                                                        | <span data-ttu-id="4c435-122">Описание</span><span class="sxs-lookup"><span data-stu-id="4c435-122">Description</span></span>                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4c435-123">Активация</span><span class="sxs-lookup"><span data-stu-id="4c435-123">Activation</span></span>](context-activation.md)<br/>                                                  | <span data-ttu-id="4c435-124">Указывает тип приложения: серверное приложение или приложение библиотеки.</span><span class="sxs-lookup"><span data-stu-id="4c435-124">Specifies application type: either server application or library application.</span></span><br/>                                                                                                            |
| [<span data-ttu-id="4c435-125">Включение проверок доступа</span><span class="sxs-lookup"><span data-stu-id="4c435-125">Enabling access checks</span></span>](enabling-access-checks-for-an-application.md)<br/>               | <span data-ttu-id="4c435-126">Включает и выключает проверку безопасности.</span><span class="sxs-lookup"><span data-stu-id="4c435-126">Turns security checking on and off.</span></span><br/>                                                                                                                                                      |
| [<span data-ttu-id="4c435-127">Уровень безопасности</span><span class="sxs-lookup"><span data-stu-id="4c435-127">Security level</span></span>](setting-a-security-level-for-access-checks.md)<br/>                      | <span data-ttu-id="4c435-128">Указывает, что проверки доступа будут выполняться на уровне процесса (уровни проверки доступа, созданные из ролей) или как на уровне процесса, так и на уровне компонентов (полная безопасность на основе ролей).</span><span class="sxs-lookup"><span data-stu-id="4c435-128">Specifies that access checks will be performed at the process level (access-checking levels generated from roles) or both at process and at component levels (full role-based security).</span></span><br/> |
| [<span data-ttu-id="4c435-129">Уровень проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="4c435-129">Authentication level</span></span>](setting-an-authentication-level-for-a-server-application.md)<br/>  | <span data-ttu-id="4c435-130">Задает уровень проверки подлинности, используемый при вызовах приложения.</span><span class="sxs-lookup"><span data-stu-id="4c435-130">Sets the authentication level used on calls into the application.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="4c435-131">Уровень олицетворения</span><span class="sxs-lookup"><span data-stu-id="4c435-131">Impersonation level</span></span>](setting-an-impersonation-level.md)<br/>                             | <span data-ttu-id="4c435-132">Задает уровень олицетворения, используемый при вызовах других приложений.</span><span class="sxs-lookup"><span data-stu-id="4c435-132">Sets the impersonation level used on calls to other applications.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="4c435-133">Управление</span><span class="sxs-lookup"><span data-stu-id="4c435-133">Queuing</span></span>](creating-queuable-components.md)<br/>                                           | <span data-ttu-id="4c435-134">Указывает, что компоненты приложения будут использовать службы очередей.</span><span class="sxs-lookup"><span data-stu-id="4c435-134">Specifies that application components will use queuing services.</span></span><br/>                                                                                                                         |
| [<span data-ttu-id="4c435-135">Включить CRM</span><span class="sxs-lookup"><span data-stu-id="4c435-135">Enable CRM</span></span>](configuring-com--crm-components.md)<br/>                                     | <span data-ttu-id="4c435-136">Позволяет использовать компенсирующие диспетчеры ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4c435-136">Enables use of Compensating Resource Managers.</span></span><br/>                                                                                                                                           |
| [<span data-ttu-id="4c435-137">Запуск приложения как службы</span><span class="sxs-lookup"><span data-stu-id="4c435-137">Run application as a service</span></span>](com--applications-running-as-service-applications.md)<br/> | <span data-ttu-id="4c435-138">Настраивает и реализует серверное приложение COM+ как службу NT.</span><span class="sxs-lookup"><span data-stu-id="4c435-138">Configures and implements a COM+ server application as an NT service.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="4c435-139">Служба COM+ SOAP</span><span class="sxs-lookup"><span data-stu-id="4c435-139">COM+ SOAP service</span></span>](com--soap-service.md)<br/>                                            | <span data-ttu-id="4c435-140">Предоставляет приложение COM+ в виде веб-службы XML.</span><span class="sxs-lookup"><span data-stu-id="4c435-140">Exposes a COM+ application as an XML web service.</span></span><br/>                                                                                                                                        |
| [<span data-ttu-id="4c435-141">Объединение приложений в пул</span><span class="sxs-lookup"><span data-stu-id="4c435-141">Application pooling</span></span>](com--application-pooling.md)<br/>                                   | <span data-ttu-id="4c435-142">Добавляет масштабируемость для однопотоковых процессов и интегрируется со службой перезапуска приложений COM+.</span><span class="sxs-lookup"><span data-stu-id="4c435-142">Adds scalability for single-threaded processes and integrates with the COM+ Application Recycling service.</span></span><br/>                                                                               |
| [<span data-ttu-id="4c435-143">Перезапуск приложений</span><span class="sxs-lookup"><span data-stu-id="4c435-143">Application recycling</span></span>](com--application-recycling.md)<br/>                               | <span data-ttu-id="4c435-144">Повышает стабильность приложений за счет корректного завершения процесса, связанного с приложением, и его перезапуска.</span><span class="sxs-lookup"><span data-stu-id="4c435-144">Increases application stability by gracefully shutting down a process associated with an application and restarting it.</span></span><br/>                                                                  |
| [<span data-ttu-id="4c435-145">Дамп процесса</span><span class="sxs-lookup"><span data-stu-id="4c435-145">Process dumping</span></span>](what-s-new-in-com--1-5.md)<br/>                                         | <span data-ttu-id="4c435-146">Выводит все состояние процесса, не прерывая его выполнения, в целях отладки.</span><span class="sxs-lookup"><span data-stu-id="4c435-146">Dumps the entire state of a process without terminating it, for debugging purposes.</span></span><br/>                                                                                                      |
| <span data-ttu-id="4c435-147">Завершение работы серверного процесса</span><span class="sxs-lookup"><span data-stu-id="4c435-147">Server process shutdown</span></span><br/>                                                               | <span data-ttu-id="4c435-148">Завершает процесс после указанного периода простоя.</span><span class="sxs-lookup"><span data-stu-id="4c435-148">Shuts down a process after a specified idle period.</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="4c435-149">Разрешения</span><span class="sxs-lookup"><span data-stu-id="4c435-149">Permissions</span></span><br/>                                                                           | <span data-ttu-id="4c435-150">Отключает изменения параметров конфигурации, включая удаление.</span><span class="sxs-lookup"><span data-stu-id="4c435-150">Disables changes to configuration settings, including deletion.</span></span><br/>                                                                                                                          |
| <span data-ttu-id="4c435-151">Удостоверение безопасности</span><span class="sxs-lookup"><span data-stu-id="4c435-151">Security identity</span></span><br/>                                                                     | <span data-ttu-id="4c435-152">Указывает удостоверение, под которым выполняется приложение.</span><span class="sxs-lookup"><span data-stu-id="4c435-152">Specifies the identity under which the application runs.</span></span><br/>                                                                                                                                 |
| <span data-ttu-id="4c435-153">Запустить в отладчике</span><span class="sxs-lookup"><span data-stu-id="4c435-153">Launch in debugger</span></span><br/>                                                                    | <span data-ttu-id="4c435-154">Указывает, что приложение будет запускаться в отладчике с параметрами командной строки, заданными пользователем.</span><span class="sxs-lookup"><span data-stu-id="4c435-154">Specifies that the application will be launched in a debugger, with user-specified command-line settings.</span></span><br/>                                                                                |
| <span data-ttu-id="4c435-155">Включить поддержку 3 ГБ</span><span class="sxs-lookup"><span data-stu-id="4c435-155">Enable 3GB support</span></span><br/>                                                                    | <span data-ttu-id="4c435-156">Включает использование адресного пространства расширенной памяти процесса.</span><span class="sxs-lookup"><span data-stu-id="4c435-156">Enables use of extended process memory address space.</span></span><br/>                                                                                                                                    |



 

## <a name="component-level-class-level-settings"></a><span data-ttu-id="4c435-157">Параметры Component-Level (уровня класса)</span><span class="sxs-lookup"><span data-stu-id="4c435-157">Component-Level (Class-Level) Settings</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4c435-158">attribute</span><span class="sxs-lookup"><span data-stu-id="4c435-158">Attribute</span></span></th>
<th><span data-ttu-id="4c435-159">Описание</span><span class="sxs-lookup"><span data-stu-id="4c435-159">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4c435-160"><a href="configuring-transactions.md">Транзакции</a></span><span class="sxs-lookup"><span data-stu-id="4c435-160"><a href="configuring-transactions.md">Transactions</a></span></span><br/></td>
<td><span data-ttu-id="4c435-161">Задает требования к автоматическим транзакциям отключены, не поддерживаются, поддерживаются, являются обязательными или требуют новых.</span><span class="sxs-lookup"><span data-stu-id="4c435-161">Sets automatic transaction requirements Disabled, Not Supported, Supported, Required, or Requires New.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4c435-162"><a href="setting-the-synchronization-attribute.md">Синхронизация</a></span><span class="sxs-lookup"><span data-stu-id="4c435-162"><a href="setting-the-synchronization-attribute.md">Synchronization</a></span></span><br/></td>
<td><span data-ttu-id="4c435-163">Задает требования к синхронизации отключены, не поддерживаются, поддерживаются, обязательны или требуют новых.</span><span class="sxs-lookup"><span data-stu-id="4c435-163">Sets synchronization requirements Disabled, Not Supported, Supported, Required, or Requires New.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4c435-164"><a href="enabling-jit-activation-for-a-component.md">JIT-активация</a></span><span class="sxs-lookup"><span data-stu-id="4c435-164"><a href="enabling-jit-activation-for-a-component.md">JIT Activation</a></span></span><br/></td>
<td><span data-ttu-id="4c435-165">Включает JIT-активацию.</span><span class="sxs-lookup"><span data-stu-id="4c435-165">Enables just-in-time activation.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4c435-166"><a href="configuring-a-component-to-be-pooled.md">Использование пулов объектов</a></span><span class="sxs-lookup"><span data-stu-id="4c435-166"><a href="configuring-a-component-to-be-pooled.md">Object pooling</a></span></span><br/></td>
<td><span data-ttu-id="4c435-167">Включает группировку объектов в пул.</span><span class="sxs-lookup"><span data-stu-id="4c435-167">Enables object pooling.</span></span> <span data-ttu-id="4c435-168">Параметры минимального и максимального размера пула и времени ожидания объекта можно настроить.</span><span class="sxs-lookup"><span data-stu-id="4c435-168">Minimum and maximum pool size and object time-out values are configurable.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4c435-169"><a href="specifying-an-object-constructor-string-for-a-component.md">Создание объекта</a></span><span class="sxs-lookup"><span data-stu-id="4c435-169"><a href="specifying-an-object-constructor-string-for-a-component.md">Object construction</a></span></span><br/></td>
<td><span data-ttu-id="4c435-170">Включает параметризованную конструкцию объекта с административно заданной строкой конструктора.</span><span class="sxs-lookup"><span data-stu-id="4c435-170">Enables parameterized object construction with an administratively specified constructor string.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="4c435-171">Строку конструктора не следует использовать для хранения конфиденциальных данных.</span><span class="sxs-lookup"><span data-stu-id="4c435-171">The constructor string should not be used to store security-sensitive information.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4c435-172"><a href="enabling-access-checks-at-the-component-level.md">Проверки доступа на уровне компонентов</a></span><span class="sxs-lookup"><span data-stu-id="4c435-172"><a href="enabling-access-checks-at-the-component-level.md">Component-level access checks</a></span></span><br/></td>
<td><span data-ttu-id="4c435-173">Включает или выключает проверку безопасности на основе ролей на уровне компонентов.</span><span class="sxs-lookup"><span data-stu-id="4c435-173">Turns on or off component-level role-based security checking.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4c435-174"><a href="assigning-roles-to-components--interfaces--or-methods.md">Декларативное назначение ролей</a></span><span class="sxs-lookup"><span data-stu-id="4c435-174"><a href="assigning-roles-to-components--interfaces--or-methods.md">Declarative role assignment</a></span></span><br/></td>
<td><span data-ttu-id="4c435-175">Разрешает явное назначение ролей компоненту.</span><span class="sxs-lookup"><span data-stu-id="4c435-175">Enables explicit assignment of roles to the component.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4c435-176"><a href="persistent-client-side-failures.md">Класс исключения очереди</a></span><span class="sxs-lookup"><span data-stu-id="4c435-176"><a href="persistent-client-side-failures.md">Queuing exception class</a></span></span><br/></td>
<td><span data-ttu-id="4c435-177">Указывает класс исключений для обработки сбоев на стороне клиента.</span><span class="sxs-lookup"><span data-stu-id="4c435-177">Indicates an exception class for handling client-side failures.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4c435-178"><a href="com--instrumentation-concepts.md">События и статистика инструментирования</a></span><span class="sxs-lookup"><span data-stu-id="4c435-178"><a href="com--instrumentation-concepts.md">Instrumentation events and statistics</a></span></span><br/></td>
<td><span data-ttu-id="4c435-179">Включает подробные отчеты о системных событиях и статистиках объектов.</span><span class="sxs-lookup"><span data-stu-id="4c435-179">Enables detailed system event and object statistics reporting.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4c435-180"><a href="context-activation.md">Контекст активации</a></span><span class="sxs-lookup"><span data-stu-id="4c435-180"><a href="context-activation.md">Activation context</a></span></span><br/></td>
<td><span data-ttu-id="4c435-181">Включает принудительную активацию объекта в контексте вызывающего объекта или контексте по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="4c435-181">Enables forced activation of an object in the caller's context or default context.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4c435-182"><a href="what-s-new-in-com--1-5.md">Создание частных компонентов</a></span><span class="sxs-lookup"><span data-stu-id="4c435-182"><a href="what-s-new-in-com--1-5.md">Creating private components</a></span></span><br/></td>
<td><span data-ttu-id="4c435-183">Помечает компонент как частный для приложения.</span><span class="sxs-lookup"><span data-stu-id="4c435-183">Marks component as private to the application.</span></span> <span data-ttu-id="4c435-184">Закрытый компонент могут видеть и активировать только другие компоненты в пределах одного приложения.</span><span class="sxs-lookup"><span data-stu-id="4c435-184">A private component can be seen and activated only by other components in the same application.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="interface-level-setting"></a><span data-ttu-id="4c435-185">Параметр Interface-Level</span><span class="sxs-lookup"><span data-stu-id="4c435-185">Interface-Level Setting</span></span>



| <span data-ttu-id="4c435-186">attribute</span><span class="sxs-lookup"><span data-stu-id="4c435-186">Attribute</span></span>                                                                                           | <span data-ttu-id="4c435-187">Описание</span><span class="sxs-lookup"><span data-stu-id="4c435-187">Description</span></span>                                                                                                                      |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4c435-188">Поставлено в очередь</span><span class="sxs-lookup"><span data-stu-id="4c435-188">Queued</span></span>](creating-queuable-components.md)<br/>                                               | <span data-ttu-id="4c435-189">Указывает интерфейс куеуабле, определенный в IDL.</span><span class="sxs-lookup"><span data-stu-id="4c435-189">Indicates a queuable interface, defined in IDL.</span></span><br/>                                                                       |
| [<span data-ttu-id="4c435-190">Декларативное назначение ролей</span><span class="sxs-lookup"><span data-stu-id="4c435-190">Declarative role assignment</span></span>](assigning-roles-to-components--interfaces--or-methods.md)<br/> | <span data-ttu-id="4c435-191">Разрешает явное назначение ролей интерфейсу, а также неявно наследуемые роли от уровня компонента.</span><span class="sxs-lookup"><span data-stu-id="4c435-191">Enables explicit assignment of roles to the interface as well as implicitly inherited roles from the component level.</span></span><br/> |



 

## <a name="method-level-setting"></a><span data-ttu-id="4c435-192">Параметр Method-Level</span><span class="sxs-lookup"><span data-stu-id="4c435-192">Method-Level Setting</span></span>



| <span data-ttu-id="4c435-193">attribute</span><span class="sxs-lookup"><span data-stu-id="4c435-193">Attribute</span></span>                                                                                           | <span data-ttu-id="4c435-194">Описание</span><span class="sxs-lookup"><span data-stu-id="4c435-194">Description</span></span>                                                                                                                                  |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4c435-195">Автоматическое завершение</span><span class="sxs-lookup"><span data-stu-id="4c435-195">Auto-done</span></span>](enabling-auto-done-for-a-method.md)<br/>                                         | <span data-ttu-id="4c435-196">Автоматически деактивирует объект при возврате метода и голосов в транзакции.</span><span class="sxs-lookup"><span data-stu-id="4c435-196">Automatically deactivates object on method return and votes in transaction.</span></span><br/>                                                       |
| [<span data-ttu-id="4c435-197">Декларативное назначение ролей</span><span class="sxs-lookup"><span data-stu-id="4c435-197">Declarative role assignment</span></span>](assigning-roles-to-components--interfaces--or-methods.md)<br/> | <span data-ttu-id="4c435-198">Разрешает явное назначение ролей методу, а также неявно наследуемые роли от уровней интерфейса и компонента.</span><span class="sxs-lookup"><span data-stu-id="4c435-198">Enables explicit assignment of roles to the method as well as implicitly inherited roles from the interface and component levels.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="4c435-199">См. также</span><span class="sxs-lookup"><span data-stu-id="4c435-199">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4c435-200">Автоматизация администрирования COM+</span><span class="sxs-lookup"><span data-stu-id="4c435-200">Automating COM+ Administration</span></span>](automating-com--administration.md)
</dt> <dt>

[<span data-ttu-id="4c435-201">Создание приложений COM+</span><span class="sxs-lookup"><span data-stu-id="4c435-201">Creating COM+ Applications</span></span>](creating-com--applications.md)
</dt> <dt>

[<span data-ttu-id="4c435-202">Развертывание приложений COM+</span><span class="sxs-lookup"><span data-stu-id="4c435-202">Deploying COM+ Applications</span></span>](deploying-com--applications.md)
</dt> </dl>

 

 




