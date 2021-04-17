---
description: Функции дополнительной телефонной службы перечислены по категориям в следующих разделах.
ms.assetid: 0d1a81d2-aa9e-4a85-85d3-aa4eabb26eb5
title: Функции дополнительной телефонной службы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 527c39441a924a4f9787d22bf8db596882e7f257
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673701"
---
# <a name="supplementary-phone-service-functions"></a><span data-ttu-id="3fd1a-103">Функции дополнительной телефонной службы</span><span class="sxs-lookup"><span data-stu-id="3fd1a-103">Supplementary Phone Service Functions</span></span>

<span data-ttu-id="3fd1a-104">Функции дополнительной телефонной службы перечислены по категориям в следующих разделах.</span><span class="sxs-lookup"><span data-stu-id="3fd1a-104">The supplementary phone service functions are listed by category in the following topics.</span></span> <span data-ttu-id="3fd1a-105">Функция определяется как [*асинхронная*](a-tapgloss.md) , если она указывает на завершение в ответном сообщении для приложения.</span><span class="sxs-lookup"><span data-stu-id="3fd1a-105">A function is identified as [*asynchronous*](a-tapgloss.md) if it will indicate completion in a REPLY message to the application.</span></span> <span data-ttu-id="3fd1a-106">Если функция всегда возвращает результат в приложение немедленно, функция считается [*синхронной*](s-tapgloss.md).</span><span class="sxs-lookup"><span data-stu-id="3fd1a-106">If the function always returns its result to the application immediately, the function is considered [*synchronous*](s-tapgloss.md).</span></span>

<span data-ttu-id="3fd1a-107">Ниже приведена функциональная группировка функций дополнительных телефонных услуг.</span><span class="sxs-lookup"><span data-stu-id="3fd1a-107">Following is a functional grouping of the supplementary phone service functions:</span></span>

-   [<span data-ttu-id="3fd1a-108">Кнопки</span><span class="sxs-lookup"><span data-stu-id="3fd1a-108">Buttons</span></span>](#buttons)
-   [<span data-ttu-id="3fd1a-109">Области данных</span><span class="sxs-lookup"><span data-stu-id="3fd1a-109">Data areas</span></span>](#data-areas)
-   [<span data-ttu-id="3fd1a-110">Дисплей</span><span class="sxs-lookup"><span data-stu-id="3fd1a-110">Display</span></span>](#display)
-   [<span data-ttu-id="3fd1a-111">Устройства хуксвитч</span><span class="sxs-lookup"><span data-stu-id="3fd1a-111">Hookswitch devices</span></span>](#hookswitch-devices)
-   [<span data-ttu-id="3fd1a-112">Ламп</span><span class="sxs-lookup"><span data-stu-id="3fd1a-112">Lamps</span></span>](#lamps)
-   [<span data-ttu-id="3fd1a-113">Открытие и закрытие телефонных устройств</span><span class="sxs-lookup"><span data-stu-id="3fd1a-113">Opening and closing phone devices</span></span>](#opening-and-closing-phone-devices)
-   [<span data-ttu-id="3fd1a-114">Инициализация и завершение работы телефона</span><span class="sxs-lookup"><span data-stu-id="3fd1a-114">Phone initialization and shutdown</span></span>](#phone-initialization-and-shutdown)
-   [<span data-ttu-id="3fd1a-115">Состояние телефона и возможности</span><span class="sxs-lookup"><span data-stu-id="3fd1a-115">Phone status and capabilities</span></span>](#phone-status-and-capabilities)
-   [<span data-ttu-id="3fd1a-116">Согласование версии телефона</span><span class="sxs-lookup"><span data-stu-id="3fd1a-116">Phone version negotiation</span></span>](#phone-version-negotiation)
-   [<span data-ttu-id="3fd1a-117">Кольцо</span><span class="sxs-lookup"><span data-stu-id="3fd1a-117">Ring</span></span>](#ring)
-   [<span data-ttu-id="3fd1a-118">Состояние</span><span class="sxs-lookup"><span data-stu-id="3fd1a-118">Status</span></span>](#status)

## <a name="phone-initialization-and-shutdown"></a><span data-ttu-id="3fd1a-119">Инициализация и завершение работы телефона</span><span class="sxs-lookup"><span data-stu-id="3fd1a-119">Phone Initialization and Shutdown</span></span>



| <span data-ttu-id="3fd1a-120">Функция</span><span class="sxs-lookup"><span data-stu-id="3fd1a-120">Function</span></span>                                       | <span data-ttu-id="3fd1a-121">Описание</span><span class="sxs-lookup"><span data-stu-id="3fd1a-121">Description</span></span>                                                                          |
|------------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="3fd1a-122">**фонеинитиализикс**</span><span class="sxs-lookup"><span data-stu-id="3fd1a-122">**phoneInitializeEx**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa) | <span data-ttu-id="3fd1a-123">Инициализирует абстракцию телефона TAPI для использования вызывающим приложением.</span><span class="sxs-lookup"><span data-stu-id="3fd1a-123">Initializes TAPI phone abstraction for use by the invoking application.</span></span> <span data-ttu-id="3fd1a-124">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="3fd1a-124">Synchronous.</span></span> |
| [<span data-ttu-id="3fd1a-125">**фонешутдовн**</span><span class="sxs-lookup"><span data-stu-id="3fd1a-125">**phoneShutdown**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneshutdown)         | <span data-ttu-id="3fd1a-126">Завершает работу приложения с использованием абстракции телефона TAPI.</span><span class="sxs-lookup"><span data-stu-id="3fd1a-126">Shuts down an application's use of TAPI's phone abstraction.</span></span> <span data-ttu-id="3fd1a-127">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="3fd1a-127">Synchronous.</span></span>            |



 

## <a name="phone-version-negotiation"></a><span data-ttu-id="3fd1a-128">Согласование версии телефона</span><span class="sxs-lookup"><span data-stu-id="3fd1a-128">Phone Version Negotiation</span></span>



| <span data-ttu-id="3fd1a-129">Функция</span><span class="sxs-lookup"><span data-stu-id="3fd1a-129">Function</span></span>                                                     | <span data-ttu-id="3fd1a-130">Описание</span><span class="sxs-lookup"><span data-stu-id="3fd1a-130">Description</span></span>                                                            |
|--------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="3fd1a-131">**фоненеготиатеапиверсион**</span><span class="sxs-lookup"><span data-stu-id="3fd1a-131">**phoneNegotiateAPIVersion**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonenegotiateapiversion) | <span data-ttu-id="3fd1a-132">Позволяет приложению согласовывать версию TAPI для использования.</span><span class="sxs-lookup"><span data-stu-id="3fd1a-132">Allows an application to negotiate a TAPI version to use.</span></span> <span data-ttu-id="3fd1a-133">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="3fd1a-133">Synchronous.</span></span> |



 

## <a name="opening-and-closing-phone-devices"></a><span data-ttu-id="3fd1a-134">Открытие и закрытие телефонных устройств</span><span class="sxs-lookup"><span data-stu-id="3fd1a-134">Opening and Closing Phone Devices</span></span>



| <span data-ttu-id="3fd1a-135">Функция</span><span class="sxs-lookup"><span data-stu-id="3fd1a-135">Function</span></span>                         | <span data-ttu-id="3fd1a-136">Описание</span><span class="sxs-lookup"><span data-stu-id="3fd1a-136">Description</span></span>                                                                                               |
|----------------------------------|-----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3fd1a-137">**фонеопен**</span><span class="sxs-lookup"><span data-stu-id="3fd1a-137">**phoneOpen**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneopen)   | <span data-ttu-id="3fd1a-138">Открывает указанное телефонное устройство, предоставляя приложению права владельца или монитора.</span><span class="sxs-lookup"><span data-stu-id="3fd1a-138">Opens the specified phone device, giving the application either owner or monitor privileges.</span></span> <span data-ttu-id="3fd1a-139">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="3fd1a-139">Synchronous.</span></span> |
| [<span data-ttu-id="3fd1a-140">**фонеклосе**</span><span class="sxs-lookup"><span data-stu-id="3fd1a-140">**phoneClose**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneclose) | <span data-ttu-id="3fd1a-141">Закрытие указанного открытого телефонного устройства.</span><span class="sxs-lookup"><span data-stu-id="3fd1a-141">Closes a specified open phone device.</span></span> <span data-ttu-id="3fd1a-142">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="3fd1a-142">Synchronous.</span></span>                                                        |



 

## <a name="phone-status-and-capabilities"></a><span data-ttu-id="3fd1a-143">Состояние телефона и возможности</span><span class="sxs-lookup"><span data-stu-id="3fd1a-143">Phone Status and Capabilities</span></span>



| <span data-ttu-id="3fd1a-144">Функция</span><span class="sxs-lookup"><span data-stu-id="3fd1a-144">Function</span></span>                                       | <span data-ttu-id="3fd1a-145">Описание</span><span class="sxs-lookup"><span data-stu-id="3fd1a-145">Description</span></span>                                                                                                                                                      |
|------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3fd1a-146">**фонежетдевкапс**</span><span class="sxs-lookup"><span data-stu-id="3fd1a-146">**phoneGetDevCaps**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps)     | <span data-ttu-id="3fd1a-147">Возвращает возможности данного телефонного устройства.</span><span class="sxs-lookup"><span data-stu-id="3fd1a-147">Returns the capabilities of a given phone device.</span></span> <span data-ttu-id="3fd1a-148">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="3fd1a-148">Synchronous.</span></span>                                                                                                   |
| [<span data-ttu-id="3fd1a-149">**фонежетид**</span><span class="sxs-lookup"><span data-stu-id="3fd1a-149">**phoneGetID**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegetid)               | <span data-ttu-id="3fd1a-150">Возвращает идентификатор устройства для указанного класса устройств, связанного с указанным телефонным устройством.</span><span class="sxs-lookup"><span data-stu-id="3fd1a-150">Returns a device ID for the given device class associated with the specified phone device.</span></span> <span data-ttu-id="3fd1a-151">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="3fd1a-151">Synchronous.</span></span>                                                          |
| [<span data-ttu-id="3fd1a-152">**фонежетикон**</span><span class="sxs-lookup"><span data-stu-id="3fd1a-152">**phoneGetIcon**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegeticon)           | <span data-ttu-id="3fd1a-153">Позволяет приложению получить значок для показа пользователю.</span><span class="sxs-lookup"><span data-stu-id="3fd1a-153">Allows an application to retrieve an icon for display to the user.</span></span> <span data-ttu-id="3fd1a-154">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="3fd1a-154">Synchronous.</span></span>                                                                                  |
| [<span data-ttu-id="3fd1a-155">**фонеконфигдиалог**</span><span class="sxs-lookup"><span data-stu-id="3fd1a-155">**phoneConfigDialog**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneconfigdialog) | <span data-ttu-id="3fd1a-156">Вызывает отображение в поставщике указанного телефонного устройства диалогового окна, позволяющего пользователю настраивать параметры, связанные с телефонным устройством.</span><span class="sxs-lookup"><span data-stu-id="3fd1a-156">Causes the provider of the specified phone device to display a dialog box that allows the user to configure parameters related to the phone device.</span></span> <span data-ttu-id="3fd1a-157">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="3fd1a-157">Synchronous.</span></span> |



 

## <a name="hookswitch-devices"></a><span data-ttu-id="3fd1a-158">Устройства хуксвитч</span><span class="sxs-lookup"><span data-stu-id="3fd1a-158">Hookswitch Devices</span></span>



| <span data-ttu-id="3fd1a-159">Функция</span><span class="sxs-lookup"><span data-stu-id="3fd1a-159">Function</span></span>                                         | <span data-ttu-id="3fd1a-160">Описание</span><span class="sxs-lookup"><span data-stu-id="3fd1a-160">Description</span></span>                                                                                       |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3fd1a-161">**фонесесуксвитч**</span><span class="sxs-lookup"><span data-stu-id="3fd1a-161">**phoneSetHookSwitch**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonesethookswitch) | <span data-ttu-id="3fd1a-162">Устанавливает состояние обработчика для устройств хуксвитч открытого телефона в указанный режим.</span><span class="sxs-lookup"><span data-stu-id="3fd1a-162">Sets the hook state of an open phone's hookswitch devices to a specified mode.</span></span> <span data-ttu-id="3fd1a-163">Асинхронная.</span><span class="sxs-lookup"><span data-stu-id="3fd1a-163">Asynchronous.</span></span>      |
| [<span data-ttu-id="3fd1a-164">**фонежесуксвитч**</span><span class="sxs-lookup"><span data-stu-id="3fd1a-164">**phoneGetHookSwitch**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegethookswitch) | <span data-ttu-id="3fd1a-165">Запрашивает режим хуксвитч устройства хуксвитч для открытого телефонного устройства.</span><span class="sxs-lookup"><span data-stu-id="3fd1a-165">Queries the hookswitch mode of a hookswitch device of an open phone device.</span></span> <span data-ttu-id="3fd1a-166">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="3fd1a-166">Synchronous.</span></span>          |
| [<span data-ttu-id="3fd1a-167">**фонесетволуме**</span><span class="sxs-lookup"><span data-stu-id="3fd1a-167">**phoneSetVolume**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonesetvolume)         | <span data-ttu-id="3fd1a-168">Задает громкость динамика устройства хуксвитч для открытого телефонного устройства.</span><span class="sxs-lookup"><span data-stu-id="3fd1a-168">Sets the volume of a hookswitch device's speaker of an open phone device.</span></span> <span data-ttu-id="3fd1a-169">Асинхронная.</span><span class="sxs-lookup"><span data-stu-id="3fd1a-169">Asynchronous.</span></span>           |
| [<span data-ttu-id="3fd1a-170">**фонежетволуме**</span><span class="sxs-lookup"><span data-stu-id="3fd1a-170">**phoneGetVolume**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegetvolume)         | <span data-ttu-id="3fd1a-171">Возвращает настройку громкости динамика устройства хуксвитч для открытого телефонного устройства.</span><span class="sxs-lookup"><span data-stu-id="3fd1a-171">Returns the volume setting of a hookswitch device's speaker of an open phone device.</span></span> <span data-ttu-id="3fd1a-172">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="3fd1a-172">Synchronous.</span></span> |
| [<span data-ttu-id="3fd1a-173">**фонесетгаин**</span><span class="sxs-lookup"><span data-stu-id="3fd1a-173">**phoneSetGain**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonesetgain)             | <span data-ttu-id="3fd1a-174">Задает Усиление микрофона устройства хуксвитч для открытого телефонного устройства.</span><span class="sxs-lookup"><span data-stu-id="3fd1a-174">Sets the gain of a hookswitch device's mic of an open phone device.</span></span> <span data-ttu-id="3fd1a-175">Асинхронная.</span><span class="sxs-lookup"><span data-stu-id="3fd1a-175">Asynchronous.</span></span>                 |
| [<span data-ttu-id="3fd1a-176">**фонежетгаин**</span><span class="sxs-lookup"><span data-stu-id="3fd1a-176">**phoneGetGain**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegetgain)             | <span data-ttu-id="3fd1a-177">Возвращает параметр усиления микрофона устройства хуксвитч на открытом телефоне.</span><span class="sxs-lookup"><span data-stu-id="3fd1a-177">Returns the gain setting of a hookswitch device's mic of an open phone.</span></span> <span data-ttu-id="3fd1a-178">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="3fd1a-178">Synchronous.</span></span>              |



 

## <a name="display"></a><span data-ttu-id="3fd1a-179">Отображение</span><span class="sxs-lookup"><span data-stu-id="3fd1a-179">Display</span></span>



| <span data-ttu-id="3fd1a-180">Функция</span><span class="sxs-lookup"><span data-stu-id="3fd1a-180">Function</span></span>                                   | <span data-ttu-id="3fd1a-181">Описание</span><span class="sxs-lookup"><span data-stu-id="3fd1a-181">Description</span></span>                                                              |
|--------------------------------------------|--------------------------------------------------------------------------|
| [<span data-ttu-id="3fd1a-182">**фонесетдисплай**</span><span class="sxs-lookup"><span data-stu-id="3fd1a-182">**phoneSetDisplay**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonesetdisplay) | <span data-ttu-id="3fd1a-183">Записывает сведения в дисплей устройства с открытым телефоном.</span><span class="sxs-lookup"><span data-stu-id="3fd1a-183">Writes information to the display of an open phone device.</span></span> <span data-ttu-id="3fd1a-184">Асинхронная.</span><span class="sxs-lookup"><span data-stu-id="3fd1a-184">Asynchronous.</span></span> |
| [<span data-ttu-id="3fd1a-185">**фонежетдисплай**</span><span class="sxs-lookup"><span data-stu-id="3fd1a-185">**phoneGetDisplay**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegetdisplay) | <span data-ttu-id="3fd1a-186">Возвращает текущее содержимое экрана телефона.</span><span class="sxs-lookup"><span data-stu-id="3fd1a-186">Returns the current contents of a phone's display.</span></span> <span data-ttu-id="3fd1a-187">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="3fd1a-187">Synchronous.</span></span>          |



 

## <a name="ring"></a><span data-ttu-id="3fd1a-188">Кольцо</span><span class="sxs-lookup"><span data-stu-id="3fd1a-188">Ring</span></span>



| <span data-ttu-id="3fd1a-189">Функция</span><span class="sxs-lookup"><span data-stu-id="3fd1a-189">Function</span></span>                             | <span data-ttu-id="3fd1a-190">Описание</span><span class="sxs-lookup"><span data-stu-id="3fd1a-190">Description</span></span>                                                              |
|--------------------------------------|--------------------------------------------------------------------------|
| [<span data-ttu-id="3fd1a-191">**фонесетринг**</span><span class="sxs-lookup"><span data-stu-id="3fd1a-191">**phoneSetRing**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonesetring) | <span data-ttu-id="3fd1a-192">Обзвонит открытое телефонное устройство в соответствии с заданным режимом кольца.</span><span class="sxs-lookup"><span data-stu-id="3fd1a-192">Rings an open phone device according to a given ring mode.</span></span> <span data-ttu-id="3fd1a-193">Асинхронная.</span><span class="sxs-lookup"><span data-stu-id="3fd1a-193">Asynchronous.</span></span> |
| [<span data-ttu-id="3fd1a-194">**фонежетринг**</span><span class="sxs-lookup"><span data-stu-id="3fd1a-194">**phoneGetRing**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegetring) | <span data-ttu-id="3fd1a-195">Возвращает текущий режим звонка открытого телефонного устройства.</span><span class="sxs-lookup"><span data-stu-id="3fd1a-195">Returns the current ring mode of an opened phone device.</span></span> <span data-ttu-id="3fd1a-196">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="3fd1a-196">Synchronous.</span></span>    |



 

## <a name="buttons"></a><span data-ttu-id="3fd1a-197">Кнопки</span><span class="sxs-lookup"><span data-stu-id="3fd1a-197">Buttons</span></span>



| <span data-ttu-id="3fd1a-198">Функция</span><span class="sxs-lookup"><span data-stu-id="3fd1a-198">Function</span></span>                                         | <span data-ttu-id="3fd1a-199">Описание</span><span class="sxs-lookup"><span data-stu-id="3fd1a-199">Description</span></span>                                                                    |
|--------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="3fd1a-200">**фонесетбуттонинфо**</span><span class="sxs-lookup"><span data-stu-id="3fd1a-200">**phoneSetButtonInfo**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonesetbuttoninfo) | <span data-ttu-id="3fd1a-201">Задает сведения, связанные с кнопкой на телефонном устройстве.</span><span class="sxs-lookup"><span data-stu-id="3fd1a-201">Sets the information associated with a button on a phone device.</span></span> <span data-ttu-id="3fd1a-202">Асинхронная.</span><span class="sxs-lookup"><span data-stu-id="3fd1a-202">Asynchronous.</span></span> |
| [<span data-ttu-id="3fd1a-203">**фонежетбуттонинфо**</span><span class="sxs-lookup"><span data-stu-id="3fd1a-203">**phoneGetButtonInfo**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegetbuttoninfo) | <span data-ttu-id="3fd1a-204">Возвращает сведения, связанные с кнопкой на телефонном устройстве.</span><span class="sxs-lookup"><span data-stu-id="3fd1a-204">Returns information associated with a button on a phone device.</span></span> <span data-ttu-id="3fd1a-205">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="3fd1a-205">Synchronous.</span></span>   |



 

## <a name="lamps"></a><span data-ttu-id="3fd1a-206">Ламп</span><span class="sxs-lookup"><span data-stu-id="3fd1a-206">Lamps</span></span>



| <span data-ttu-id="3fd1a-207">Функция</span><span class="sxs-lookup"><span data-stu-id="3fd1a-207">Function</span></span>                             | <span data-ttu-id="3fd1a-208">Описание</span><span class="sxs-lookup"><span data-stu-id="3fd1a-208">Description</span></span>                                                                                 |
|--------------------------------------|---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3fd1a-209">**фонесетламп**</span><span class="sxs-lookup"><span data-stu-id="3fd1a-209">**phoneSetLamp**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonesetlamp) | <span data-ttu-id="3fd1a-210">Лампочка на указанном устройстве с открытым телефоном в заданном режиме освещения лампы.</span><span class="sxs-lookup"><span data-stu-id="3fd1a-210">Lights a lamp on a specified open phone device in a given lamp lighting mode.</span></span> <span data-ttu-id="3fd1a-211">Асинхронная.</span><span class="sxs-lookup"><span data-stu-id="3fd1a-211">Asynchronous.</span></span> |
| [<span data-ttu-id="3fd1a-212">**фонежетламп**</span><span class="sxs-lookup"><span data-stu-id="3fd1a-212">**phoneGetLamp**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegetlamp) | <span data-ttu-id="3fd1a-213">Возвращает текущий режим лампы указанной лампы.</span><span class="sxs-lookup"><span data-stu-id="3fd1a-213">Returns the current lamp mode of the specified lamp.</span></span> <span data-ttu-id="3fd1a-214">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="3fd1a-214">Synchronous.</span></span>                           |



 

## <a name="data-areas"></a><span data-ttu-id="3fd1a-215">Области данных</span><span class="sxs-lookup"><span data-stu-id="3fd1a-215">Data Areas</span></span>



| <span data-ttu-id="3fd1a-216">Функция</span><span class="sxs-lookup"><span data-stu-id="3fd1a-216">Function</span></span>                             | <span data-ttu-id="3fd1a-217">Описание</span><span class="sxs-lookup"><span data-stu-id="3fd1a-217">Description</span></span>                                                                             |
|--------------------------------------|-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="3fd1a-218">**фонесетдата**</span><span class="sxs-lookup"><span data-stu-id="3fd1a-218">**phoneSetData**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonesetdata) | <span data-ttu-id="3fd1a-219">Скачивает буфер данных в заданную область данных телефонного устройства.</span><span class="sxs-lookup"><span data-stu-id="3fd1a-219">Downloads a buffer of data to a given data area in the phone device.</span></span> <span data-ttu-id="3fd1a-220">Асинхронная.</span><span class="sxs-lookup"><span data-stu-id="3fd1a-220">Asynchronous.</span></span>      |
| [<span data-ttu-id="3fd1a-221">**фонежетдата**</span><span class="sxs-lookup"><span data-stu-id="3fd1a-221">**phoneGetData**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegetdata) | <span data-ttu-id="3fd1a-222">Передает содержимое заданной области данных телефонного устройства в буфер.</span><span class="sxs-lookup"><span data-stu-id="3fd1a-222">Uploads the contents of a given data area in the phone device to a buffer.</span></span> <span data-ttu-id="3fd1a-223">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="3fd1a-223">Synchronous.</span></span> |



 

## <a name="status"></a><span data-ttu-id="3fd1a-224">Состояние</span><span class="sxs-lookup"><span data-stu-id="3fd1a-224">Status</span></span>



| <span data-ttu-id="3fd1a-225">Функция</span><span class="sxs-lookup"><span data-stu-id="3fd1a-225">Function</span></span>                                                 | <span data-ttu-id="3fd1a-226">Описание</span><span class="sxs-lookup"><span data-stu-id="3fd1a-226">Description</span></span>                                                                               |
|----------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3fd1a-227">**фонесетстатусмессажес**</span><span class="sxs-lookup"><span data-stu-id="3fd1a-227">**phoneSetStatusMessages**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonesetstatusmessages) | <span data-ttu-id="3fd1a-228">Указывает изменения состояния, для которых приложение должно получать уведомления.</span><span class="sxs-lookup"><span data-stu-id="3fd1a-228">Specifies the status changes for which the application wants to be notified.</span></span> <span data-ttu-id="3fd1a-229">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="3fd1a-229">Synchronous.</span></span> |
| [<span data-ttu-id="3fd1a-230">**фонежетстатусмессажес**</span><span class="sxs-lookup"><span data-stu-id="3fd1a-230">**phoneGetStatusMessages**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegetstatusmessages) | <span data-ttu-id="3fd1a-231">Возвращает изменения состояния, для которых приложение должно получать уведомления.</span><span class="sxs-lookup"><span data-stu-id="3fd1a-231">Returns the status changes for which the application wants to be notified.</span></span> <span data-ttu-id="3fd1a-232">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="3fd1a-232">Synchronous.</span></span>   |
| [<span data-ttu-id="3fd1a-233">**фонежетстатус**</span><span class="sxs-lookup"><span data-stu-id="3fd1a-233">**phoneGetStatus**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegetstatus)                 | <span data-ttu-id="3fd1a-234">Возвращает полное состояние открытого телефонного устройства.</span><span class="sxs-lookup"><span data-stu-id="3fd1a-234">Returns the complete status of an open phone device.</span></span> <span data-ttu-id="3fd1a-235">Синхронный.</span><span class="sxs-lookup"><span data-stu-id="3fd1a-235">Synchronous.</span></span>                         |



 

 

 



