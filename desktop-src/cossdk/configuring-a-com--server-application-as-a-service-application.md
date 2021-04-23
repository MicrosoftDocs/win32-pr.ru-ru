---
description: Серверное приложение COM+ можно создать как службу для автоматического запуска во время запуска системы или вручную при активации.
ms.assetid: 56487746-328d-4435-af58-368aaa15b32a
title: Настройка серверного приложения COM+ как приложения службы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3b3bbf8b691221590d6588c48dbef5198772439
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895621"
---
# <a name="configuring-a-com-server-application-as-a-service-application"></a><span data-ttu-id="7a7d5-103">Настройка серверного приложения COM+ как приложения службы</span><span class="sxs-lookup"><span data-stu-id="7a7d5-103">Configuring a COM+ Server Application as a Service Application</span></span>

<span data-ttu-id="7a7d5-104">Серверное приложение COM+ можно создать как службу для автоматического запуска во время запуска системы или вручную при активации.</span><span class="sxs-lookup"><span data-stu-id="7a7d5-104">A COM+ server application can be created as a service to start either automatically during the system startup or manually by activations.</span></span> <span data-ttu-id="7a7d5-105">Если служба не запускается, параметр обработки ошибок указывает серьезность ошибки и определяет выполняемое действие.</span><span class="sxs-lookup"><span data-stu-id="7a7d5-105">If the service fails to start, the option for error handling specifies the severity of the error and determines the action to be taken.</span></span> <span data-ttu-id="7a7d5-106">Также доступна возможность настройки службы для запуска от имени локальной системной учетной записи, а также возможность назначения конкретной учетной записи пользователя, для которой будет выполняться серверное приложение COM+.</span><span class="sxs-lookup"><span data-stu-id="7a7d5-106">The option to configure a service to run as the local system account is also available, as well as the option to assign a specific user account for which the COM+ server application will run.</span></span> <span data-ttu-id="7a7d5-107">Зависимости также можно выбрать из списка служб, зарегистрированных на компьютере, с помощью служб компонентов.</span><span class="sxs-lookup"><span data-stu-id="7a7d5-107">Dependencies can also be selected from a list of services registered on the computer using Component Services.</span></span> <span data-ttu-id="7a7d5-108">Это определит, какие службы должны быть выполнены перед запуском этой службы.</span><span class="sxs-lookup"><span data-stu-id="7a7d5-108">This will determine which services must be executed before this service is started.</span></span>

<span data-ttu-id="7a7d5-109">**Настройка приложения COM+ для запуска в качестве службы**</span><span class="sxs-lookup"><span data-stu-id="7a7d5-109">**To configure a COM+ application to run as a service**</span></span>

1.  <span data-ttu-id="7a7d5-110">В дереве консоли средства администрирования "службы компонентов" выберите серверное приложение COM+, которое требуется запустить в качестве службы.</span><span class="sxs-lookup"><span data-stu-id="7a7d5-110">In the console tree of the Component Services administrative tool, locate the COM+ server application you want to run as a service.</span></span>

2.  <span data-ttu-id="7a7d5-111">Щелкните правой кнопкой мыши серверное приложение COM+ и выберите пункт **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="7a7d5-111">Right-click the COM+ server application, and then click **Properties**.</span></span>

3.  <span data-ttu-id="7a7d5-112">В диалоговом окне **Свойства** перейдите на вкладку **Активация** .</span><span class="sxs-lookup"><span data-stu-id="7a7d5-112">In the **Properties** dialog box, click the **Activation** tab.</span></span>

4.  <span data-ttu-id="7a7d5-113">В поле " **тип активации** " установите флажок **запустить приложение как службу NT** .</span><span class="sxs-lookup"><span data-stu-id="7a7d5-113">In the **Activation type** box, check the **Run application as NT Service** check box.</span></span>

    > [!Note]  
    > <span data-ttu-id="7a7d5-114">Флажок " **запустить приложение как службу NT** " включен только для серверных приложений и отключен для библиотечных приложений.</span><span class="sxs-lookup"><span data-stu-id="7a7d5-114">The **Run application as NT Service** check box is enabled only for server applications and is disabled for library applications.</span></span>

     

5.  <span data-ttu-id="7a7d5-115">Нажмите кнопку **настроить новую службу** .</span><span class="sxs-lookup"><span data-stu-id="7a7d5-115">Click the **Setup New Service** button.</span></span>

6.  <span data-ttu-id="7a7d5-116">В поле **Тип запуска** диалогового окна **имя службы** выберите значение **автоматически** или **вручную**.</span><span class="sxs-lookup"><span data-stu-id="7a7d5-116">In the **Startup type** box in the **Service Name** dialog box, select **Automatic** or **Manual**.</span></span>

7.  <span data-ttu-id="7a7d5-117">Используемых Чтобы указать действие, выполняемое для конкретной ошибки, выберите параметр **пропустить**, **Обычная**, **серьезная** или **критическая** в поле **Обработка ошибок** .</span><span class="sxs-lookup"><span data-stu-id="7a7d5-117">(Optional) To specify the action to be taken for a particular error, select **Ignore**, **Normal**, **Severe**, or **Critical** in the **Error Handling** box.</span></span> <span data-ttu-id="7a7d5-118">Поведение, связанное с каждым из параметров, выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="7a7d5-118">The behavior associated with each option is as follows:</span></span>

    1.  <span data-ttu-id="7a7d5-119">**Пропуск**.</span><span class="sxs-lookup"><span data-stu-id="7a7d5-119">**Ignore**.</span></span> <span data-ttu-id="7a7d5-120">Программа запуска зарегистрирует ошибку, но продолжит операцию запуска.</span><span class="sxs-lookup"><span data-stu-id="7a7d5-120">The startup program logs the error but continues the startup operation.</span></span>
    2.  <span data-ttu-id="7a7d5-121">**Обычная**.</span><span class="sxs-lookup"><span data-stu-id="7a7d5-121">**Normal**.</span></span> <span data-ttu-id="7a7d5-122">Эта ошибка заносится в журнал, отображается окно сообщения, а программа запуска возобновляет работу.</span><span class="sxs-lookup"><span data-stu-id="7a7d5-122">The error is logged, a message box is displayed, and the startup program continues the startup operation.</span></span>
    3.  <span data-ttu-id="7a7d5-123">**Серьезная**.</span><span class="sxs-lookup"><span data-stu-id="7a7d5-123">**Severe**.</span></span> <span data-ttu-id="7a7d5-124">Ошибка заносится в журнал, и система перезапускается с последней удачной конфигурацией.</span><span class="sxs-lookup"><span data-stu-id="7a7d5-124">The error is logged, and the system is restarted with the last known good configuration.</span></span> <span data-ttu-id="7a7d5-125">Если это последняя удачная конфигурация, которая запускается при занесении в журнал ошибки, операция запуска продолжится.</span><span class="sxs-lookup"><span data-stu-id="7a7d5-125">If it is the last known good configuration that is being started when the error is logged, the startup operation continues.</span></span>
    4.  <span data-ttu-id="7a7d5-126">**Критическое** —</span><span class="sxs-lookup"><span data-stu-id="7a7d5-126">**Critical**.</span></span> <span data-ttu-id="7a7d5-127">Ошибка заносится в журнал, и система перезапускается с последней удачной конфигурацией.</span><span class="sxs-lookup"><span data-stu-id="7a7d5-127">The error is logged, and the system is restarted with the last known good configuration.</span></span> <span data-ttu-id="7a7d5-128">Если это последняя удачная конфигурация, которая запускается при занесении в журнал ошибки, операция запуска завершается ошибкой.</span><span class="sxs-lookup"><span data-stu-id="7a7d5-128">If it is the last known good configuration that is being started when the error is logged, the startup operation fails.</span></span>

8.  <span data-ttu-id="7a7d5-129">Используемых Чтобы задать другие службы как зависимые, выберите зависимые службы из списка в поле **зависимости** .</span><span class="sxs-lookup"><span data-stu-id="7a7d5-129">(Optional) To set other services as dependent, select the dependent services from the list in the **Dependencies** box.</span></span>

9.  <span data-ttu-id="7a7d5-130">Используемых Чтобы указать, что службе должно быть разрешено взаимодействовать с рабочим столом, установите флажок **Разрешить взаимодействие со службой "Рабочий стол** ".</span><span class="sxs-lookup"><span data-stu-id="7a7d5-130">(Optional) To indicate that the service should be allowed to interact with the desktop, check the **Allow service to interact with desktop** check box.</span></span>

10. <span data-ttu-id="7a7d5-131">Нажмите кнопку **Создать**.</span><span class="sxs-lookup"><span data-stu-id="7a7d5-131">Click **Create**.</span></span>

11. <span data-ttu-id="7a7d5-132">Используемых Чтобы назначить службу учетной записи пользователя, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="7a7d5-132">(Optional) To assign the service to a user account:</span></span>

    1.  <span data-ttu-id="7a7d5-133">На вкладке **удостоверение** выберите **этот пользователь**.</span><span class="sxs-lookup"><span data-stu-id="7a7d5-133">In the **Identity** tab, select **This user**.</span></span>
    2.  <span data-ttu-id="7a7d5-134">Чтобы выбрать пользователя, введите имя пользователя в поле **пользователь** или нажмите кнопку **Обзор** .</span><span class="sxs-lookup"><span data-stu-id="7a7d5-134">To select the user, enter the user name in the **User** box or click the **Browse** button.</span></span>
    3.  <span data-ttu-id="7a7d5-135">Введите пароль для учетной записи пользователя в поле **пароль** .</span><span class="sxs-lookup"><span data-stu-id="7a7d5-135">Enter the password for the user account in the **Password** box.</span></span>
    4.  <span data-ttu-id="7a7d5-136">Введите тот же пароль в поле **Подтверждение пароля** .</span><span class="sxs-lookup"><span data-stu-id="7a7d5-136">Enter the same password in the **Confirm Password** box.</span></span>

 

 



