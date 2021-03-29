---
title: начало работы с Ксинпут
description: Ксинпут — это API, позволяющий приложениям принимать входные данные с контроллера Xbox для Windows. Поддерживаются эффекты румблеа контроллера, речевой ввод и вывод.
ms.assetid: 7b5eec3e-b3da-de5c-c926-8258c1418ef0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91f590f54bbb2641881cf89cd6d31539d75665c0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103791893"
---
# <a name="getting-started-with-xinput"></a><span data-ttu-id="5c3d0-104">начало работы с Ксинпут</span><span class="sxs-lookup"><span data-stu-id="5c3d0-104">Getting Started With XInput</span></span>

<span data-ttu-id="5c3d0-105">Ксинпут — это API, позволяющий приложениям принимать входные данные с контроллера Xbox для Windows.</span><span class="sxs-lookup"><span data-stu-id="5c3d0-105">XInput is an API that allows applications to receive input from the Xbox Controller for Windows.</span></span> <span data-ttu-id="5c3d0-106">Поддерживаются эффекты румблеа контроллера, речевой ввод и вывод.</span><span class="sxs-lookup"><span data-stu-id="5c3d0-106">Controller rumble effects and voice input and output are supported.</span></span>

<span data-ttu-id="5c3d0-107">В этом разделе содержится краткий обзор возможностей Ксинпут и их настройки в приложении.</span><span class="sxs-lookup"><span data-stu-id="5c3d0-107">This topic provides a brief overview of the capabilities of XInput and how to set it up in an application.</span></span> <span data-ttu-id="5c3d0-108">Он включает в себя следующее:</span><span class="sxs-lookup"><span data-stu-id="5c3d0-108">It includes the following:</span></span>

-   [<span data-ttu-id="5c3d0-109">Введение в Ксинпут</span><span class="sxs-lookup"><span data-stu-id="5c3d0-109">Introduction to XInput</span></span>](#introduction-to-xinput)
    -   [<span data-ttu-id="5c3d0-110">Контроллер Xbox</span><span class="sxs-lookup"><span data-stu-id="5c3d0-110">The Xbox Controller</span></span>](#the-xbox-controller)
-   [<span data-ttu-id="5c3d0-111">Использование Ксинпут</span><span class="sxs-lookup"><span data-stu-id="5c3d0-111">Using XInput</span></span>](#using-xinput)
    -   [<span data-ttu-id="5c3d0-112">Несколько контроллеров</span><span class="sxs-lookup"><span data-stu-id="5c3d0-112">Multiple Controllers</span></span>](#multiple-controllers)
    -   [<span data-ttu-id="5c3d0-113">Получение состояния контроллера</span><span class="sxs-lookup"><span data-stu-id="5c3d0-113">Getting Controller State</span></span>](#getting-controller-state)
    -   [<span data-ttu-id="5c3d0-114">Неработающая зона</span><span class="sxs-lookup"><span data-stu-id="5c3d0-114">Dead Zone</span></span>](#dead-zone)
    -   [<span data-ttu-id="5c3d0-115">Установка эффектов вибрации</span><span class="sxs-lookup"><span data-stu-id="5c3d0-115">Setting Vibration Effects</span></span>](#setting-vibration-effects)
    -   [<span data-ttu-id="5c3d0-116">Получение идентификаторов звуковых устройств</span><span class="sxs-lookup"><span data-stu-id="5c3d0-116">Getting Audio Device Identifiers</span></span>](#getting-audio-device-identifiers)
    -   [<span data-ttu-id="5c3d0-117">Получение идентификаторов GUID DirectSound (только для устаревших пакетов SDK DirectX)</span><span class="sxs-lookup"><span data-stu-id="5c3d0-117">Getting DirectSound GUIDs (legacy DirectX SDK only)</span></span>](#getting-directsound-guids-legacy-directx-sdk-only)
-   [<span data-ttu-id="5c3d0-118">См. также</span><span class="sxs-lookup"><span data-stu-id="5c3d0-118">Related topics</span></span>](#related-topics)

## <a name="introduction-to-xinput"></a><span data-ttu-id="5c3d0-119">Введение в Ксинпут</span><span class="sxs-lookup"><span data-stu-id="5c3d0-119">Introduction to XInput</span></span>

<span data-ttu-id="5c3d0-120">Консоль Xbox использует игровой контроллер, совместимый с Windows.</span><span class="sxs-lookup"><span data-stu-id="5c3d0-120">The Xbox console uses a gaming controller that is compatible with Windows.</span></span> <span data-ttu-id="5c3d0-121">Приложения могут использовать API Ксинпут для взаимодействия с этими контроллерами при их подключении к компьютеру под управлением Windows (за один раз может быть подключено до четырех уникальных контроллеров).</span><span class="sxs-lookup"><span data-stu-id="5c3d0-121">Applications can use the XInput API to communicate with these controllers when they are plugged into a Windows PC (up to four unique controllers can be plugged in at a time).</span></span>

<span data-ttu-id="5c3d0-122">С помощью этого API можно запрашивать состояние любого подключенного контроллера Xbox, а также устанавливать эффекты вибрации.</span><span class="sxs-lookup"><span data-stu-id="5c3d0-122">Using this API, any connected Xbox Controller can be queried for its state, and vibration effects can be set.</span></span> <span data-ttu-id="5c3d0-123">Контроллеры, подключенные к гарнитуре, также могут быть запрошены для устройств ввода и вывода звука, которые можно использовать с гарнитурой для обработки голоса.</span><span class="sxs-lookup"><span data-stu-id="5c3d0-123">Controllers that have the headset attached can also be queried for sound input and output devices that can be used with the headset for voice processing.</span></span>

### <a name="the-xbox-controller"></a><span data-ttu-id="5c3d0-124">Контроллер Xbox</span><span class="sxs-lookup"><span data-stu-id="5c3d0-124">The Xbox Controller</span></span>

<span data-ttu-id="5c3d0-125">Контроллер Xbox имеет два аналоговых устройства направления, каждое с цифровой кнопкой, два аналоговых триггера, цифровую клавиатуру с четырьмя направлениями и восемь цифровых кнопок.</span><span class="sxs-lookup"><span data-stu-id="5c3d0-125">The Xbox Controller has two analog directional sticks, each with a digital button, two analog triggers, a digital directional pad with four directions, and eight digital buttons.</span></span> <span data-ttu-id="5c3d0-126">Состояния каждого из этих входных данных возвращаются в структуре [**\_ игрового ксинпут**](/windows/desktop/api/XInput/ns-xinput-xinput_gamepad) при вызове функции [**ксинпутжетстате**](/windows/desktop/api/XInput/nf-xinput-xinputgetstate) .</span><span class="sxs-lookup"><span data-stu-id="5c3d0-126">The states of each of these inputs are returned in the [**XINPUT\_GAMEPAD**](/windows/desktop/api/XInput/ns-xinput-xinput_gamepad) structure when the [**XInputGetState**](/windows/desktop/api/XInput/nf-xinput-xinputgetstate) function is called.</span></span>

<span data-ttu-id="5c3d0-127">Контроллер также имеет два мотора вибрации, чтобы предоставить пользователю возможность принудительной обратной связи.</span><span class="sxs-lookup"><span data-stu-id="5c3d0-127">The controller also has two vibration motors to supply force feedback effects to the user.</span></span> <span data-ttu-id="5c3d0-128">Скорость этих моторов задается в структуре [**\_ вибрации ксинпут**](/windows/desktop/api/XInput/ns-xinput-xinput_vibration) , которая передается в функцию [**ксинпутсетстате**](/windows/desktop/api/XInput/nf-xinput-xinputsetstate) для установки эффектов вибрации.</span><span class="sxs-lookup"><span data-stu-id="5c3d0-128">The speeds of these motors are specified in the [**XINPUT\_VIBRATION**](/windows/desktop/api/XInput/ns-xinput-xinput_vibration) structure that is passed to the [**XInputSetState**](/windows/desktop/api/XInput/nf-xinput-xinputsetstate) function to set vibration effects.</span></span>

<span data-ttu-id="5c3d0-129">При необходимости можно подключить гарнитуру к контроллеру.</span><span class="sxs-lookup"><span data-stu-id="5c3d0-129">Optionally, a headset can be connected to the controller.</span></span> <span data-ttu-id="5c3d0-130">Гарнитура имеет микрофон для речевого ввода и наушники для вывода звука.</span><span class="sxs-lookup"><span data-stu-id="5c3d0-130">The headset has a microphone for voice input, and a headphone for sound output.</span></span> <span data-ttu-id="5c3d0-131">Вы можете вызвать функцию [**ксинпутжетаудиодевицеидс**](/windows/desktop/api/XInput/nf-xinput-xinputgetaudiodeviceids) или Legacy [**ксинпутжетдсаундаудиодевицегуидс**](/windows/desktop/api/XInput/nf-xinput-xinputgetdsoundaudiodeviceguids) , чтобы получить идентификаторы устройств, которые соответствуют устройствам для микрофона и наушников.</span><span class="sxs-lookup"><span data-stu-id="5c3d0-131">You can call the [**XInputGetAudioDeviceIds**](/windows/desktop/api/XInput/nf-xinput-xinputgetaudiodeviceids) or legacy [**XInputGetDSoundAudioDeviceGuids**](/windows/desktop/api/XInput/nf-xinput-xinputgetdsoundaudiodeviceguids) function to obtain the device identifiers that correspond to the devices for the microphone and headphone.</span></span> <span data-ttu-id="5c3d0-132">Затем можно использовать [Основные API аудио](/windows/desktop/CoreAudio/core-audio-apis-in-windows-vista) для получения голосового ввода и отправки звуковых данных.</span><span class="sxs-lookup"><span data-stu-id="5c3d0-132">You can then use the [Core Audio APIs](/windows/desktop/CoreAudio/core-audio-apis-in-windows-vista) to receive voice input and send sound output.</span></span>

## <a name="using-xinput"></a><span data-ttu-id="5c3d0-133">Использование Ксинпут</span><span class="sxs-lookup"><span data-stu-id="5c3d0-133">Using XInput</span></span>

<span data-ttu-id="5c3d0-134">Использование Ксинпут — это просто вызов функций Ксинпут по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="5c3d0-134">Using XInput is as simple as calling the XInput functions as required.</span></span> <span data-ttu-id="5c3d0-135">С помощью функций Ксинпут можно получить состояние контроллера, получить идентификаторы головного телефона и установить эффекты румбле контроллера.</span><span class="sxs-lookup"><span data-stu-id="5c3d0-135">Using the XInput functions, you can retrieve controller state, get headset audio IDs, and set controller rumble effects.</span></span>

### <a name="multiple-controllers"></a><span data-ttu-id="5c3d0-136">Несколько контроллеров</span><span class="sxs-lookup"><span data-stu-id="5c3d0-136">Multiple Controllers</span></span>

<span data-ttu-id="5c3d0-137">API Ксинпут поддерживает до четырех контроллеров, подключенных в любое время.</span><span class="sxs-lookup"><span data-stu-id="5c3d0-137">The XInput API supports up to four controllers connected at any time.</span></span> <span data-ttu-id="5c3d0-138">Для всех функций Ксинпут требуется параметр *двусериндекс* , который передается для указания устанавливаемого или запрашиваемого контроллера.</span><span class="sxs-lookup"><span data-stu-id="5c3d0-138">The XInput functions all require a *dwUserIndex* parameter that is passed in to identify the controller being set or queried.</span></span> <span data-ttu-id="5c3d0-139">Этот идентификатор будет находиться в диапазоне 0-3 и автоматически задается Ксинпут.</span><span class="sxs-lookup"><span data-stu-id="5c3d0-139">This ID will be in the range of 0-3 and is set automatically by XInput.</span></span> <span data-ttu-id="5c3d0-140">Число соответствует порту, в который подключен контроллер, и не может быть изменен.</span><span class="sxs-lookup"><span data-stu-id="5c3d0-140">The number corresponds to the port that the controller is plugged into, and is not modifiable.</span></span>

<span data-ttu-id="5c3d0-141">Каждый контроллер отображает, какой идентификатор используется, выосвещения квадранта в «кольце света» в центре контроллера.</span><span class="sxs-lookup"><span data-stu-id="5c3d0-141">Each controller displays which ID it is using by lighting up a quadrant on the "ring of light" in the center of the controller.</span></span> <span data-ttu-id="5c3d0-142">Значение *двусериндекс* , равное 0, соответствует верхнему левому квадранту; Нумерация продолжается вокруг кольца в порядке по часовой стрелке.</span><span class="sxs-lookup"><span data-stu-id="5c3d0-142">A *dwUserIndex* value of 0 corresponds to the top-left quadrant; the numbering proceeds around the ring in clockwise order.</span></span>

<span data-ttu-id="5c3d0-143">Приложения должны поддерживать несколько контроллеров.</span><span class="sxs-lookup"><span data-stu-id="5c3d0-143">Applications should support multiple controllers.</span></span>

### <a name="getting-controller-state"></a><span data-ttu-id="5c3d0-144">Получение состояния контроллера</span><span class="sxs-lookup"><span data-stu-id="5c3d0-144">Getting Controller State</span></span>

<span data-ttu-id="5c3d0-145">В течение всего времени работы приложения получение состояния от контроллера, вероятно, будет выполняться чаще всего.</span><span class="sxs-lookup"><span data-stu-id="5c3d0-145">Throughout the duration of an application, getting state from a controller will probably be done most often.</span></span> <span data-ttu-id="5c3d0-146">Из фрейма в кадр в игровом приложении необходимо получить состояние и сведения об игре, обновленные для отражения изменений контроллера.</span><span class="sxs-lookup"><span data-stu-id="5c3d0-146">From frame to frame in a game application, state should be retrieved and game information updated to reflect the controller changes.</span></span>

<span data-ttu-id="5c3d0-147">Чтобы получить состояние, используйте функцию [**ксинпутжетстате**](/windows/desktop/api/XInput/nf-xinput-xinputgetstate) :</span><span class="sxs-lookup"><span data-stu-id="5c3d0-147">To retrieve state, use the [**XInputGetState**](/windows/desktop/api/XInput/nf-xinput-xinputgetstate) function:</span></span>

```cpp
DWORD dwResult;    
for (DWORD i=0; i< XUSER_MAX_COUNT; i++ )
{
    XINPUT_STATE state;
    ZeroMemory( &state, sizeof(XINPUT_STATE) );

    // Simply get the state of the controller from XInput.
    dwResult = XInputGetState( i, &state );

    if( dwResult == ERROR_SUCCESS )
    {
        // Controller is connected
    }
    else
    {
        // Controller is not connected
    }
}
```

<span data-ttu-id="5c3d0-148">Обратите внимание, что возвращаемое значение [**ксинпутжетстате**](/windows/desktop/api/XInput/nf-xinput-xinputgetstate) можно использовать, чтобы определить, подключен ли контроллер.</span><span class="sxs-lookup"><span data-stu-id="5c3d0-148">Note that the return value of [**XInputGetState**](/windows/desktop/api/XInput/nf-xinput-xinputgetstate) can be used to determine if the controller is connected.</span></span> <span data-ttu-id="5c3d0-149">Приложения должны определять структуру для хранения сведений о внутреннем контроллере; Эти сведения следует сравнить с результатами **ксинпутжетстате** , чтобы определить, какие изменения, например нажатия кнопок или аналогового контроллера, были сделаны в кадре.</span><span class="sxs-lookup"><span data-stu-id="5c3d0-149">Applications should define a structure to hold internal controller information; this information should be compared against the results of **XInputGetState** to determine what changes, such as button presses or analog controller deltas, were made that frame.</span></span> <span data-ttu-id="5c3d0-150">В приведенном выше примере *g \_ Controllers* представляет такую структуру.</span><span class="sxs-lookup"><span data-stu-id="5c3d0-150">In the above example, *g\_Controllers* represents such a structure.</span></span>

<span data-ttu-id="5c3d0-151">После того как состояние получено в структуре [**\_ состояния ксинпут**](/windows/desktop/api/XInput/ns-xinput-xinput_state) , его можно проверить на наличие изменений и получить конкретные сведения о состоянии контроллера.</span><span class="sxs-lookup"><span data-stu-id="5c3d0-151">Once the state has been retrieved in a [**XINPUT\_STATE**](/windows/desktop/api/XInput/ns-xinput-xinput_state) structure, you can check it for changes and get specific information about controller state.</span></span>

<span data-ttu-id="5c3d0-152">Элемент *двпаккетнумбер* структуры [**\_ состояния ксинпут**](/windows/desktop/api/XInput/ns-xinput-xinput_state) можно использовать, чтобы проверить, изменилось ли состояние контроллера с момента последнего вызова [**ксинпутжетстате**](/windows/desktop/api/XInput/nf-xinput-xinputgetstate).</span><span class="sxs-lookup"><span data-stu-id="5c3d0-152">The *dwPacketNumber* member of the [**XINPUT\_STATE**](/windows/desktop/api/XInput/ns-xinput-xinput_state) structure can be used to check if the state of the controller has changed since the last call to [**XInputGetState**](/windows/desktop/api/XInput/nf-xinput-xinputgetstate).</span></span> <span data-ttu-id="5c3d0-153">Если *двпаккетнумбер* не меняется между двумя последовательными вызовами **ксинпутжетстате**, то состояние не изменилось.</span><span class="sxs-lookup"><span data-stu-id="5c3d0-153">If *dwPacketNumber* does not change between two sequential calls to **XInputGetState**, then there has been no change in state.</span></span> <span data-ttu-id="5c3d0-154">Если он отличается, приложение должно проверить элемент *планшета* в структуре **\_ состояния ксинпут** , чтобы получить более подробные сведения о состоянии.</span><span class="sxs-lookup"><span data-stu-id="5c3d0-154">If it differs, then the application should check the *Gamepad* member of the **XINPUT\_STATE** structure to get more detailed state information.</span></span>

<span data-ttu-id="5c3d0-155">По соображениям производительности не вызывайте [**ксинпутжетстате**](/windows/desktop/api/XInput/nf-xinput-xinputgetstate) для пустого слота пользователя в каждом кадре.</span><span class="sxs-lookup"><span data-stu-id="5c3d0-155">For performance reasons, don't call [**XInputGetState**](/windows/desktop/api/XInput/nf-xinput-xinputgetstate) for an 'empty' user slot every frame.</span></span> <span data-ttu-id="5c3d0-156">Рекомендуется проделать проверки для новых контроллеров каждые несколько секунд.</span><span class="sxs-lookup"><span data-stu-id="5c3d0-156">We recommend that you space out checks for new controllers every few seconds instead.</span></span>

### <a name="dead-zone"></a><span data-ttu-id="5c3d0-157">Неработающая зона</span><span class="sxs-lookup"><span data-stu-id="5c3d0-157">Dead Zone</span></span>

<span data-ttu-id="5c3d0-158">Чтобы пользователи имели единообразный интерфейс игрового процесса, игра должна правильно реализовать неработающую зону.</span><span class="sxs-lookup"><span data-stu-id="5c3d0-158">In order for users to have a consistent gameplay experience, your game must implement dead zone correctly.</span></span> <span data-ttu-id="5c3d0-159">Недействующая зона — это значения перемещения, сообщаемые контроллером даже в том случае, если аналоговые сумбстиккс не были затронуты и центрированы.</span><span class="sxs-lookup"><span data-stu-id="5c3d0-159">The dead zone is "movement" values reported by the controller even when the analog thumbsticks are untouched and centered.</span></span> <span data-ttu-id="5c3d0-160">Существует также некоторая зона для двух аналоговых триггеров.</span><span class="sxs-lookup"><span data-stu-id="5c3d0-160">There is also a dead zone for the 2 analog triggers.</span></span>

> [!Note]  
> <span data-ttu-id="5c3d0-161">Игры, использующие Ксинпут, которые не фильтруют неработающую зону, будут испытывать низкую игрового процессау.</span><span class="sxs-lookup"><span data-stu-id="5c3d0-161">Games that use XInput that do not filter dead zone at all will experience poor gameplay.</span></span> <span data-ttu-id="5c3d0-162">Обратите внимание, что некоторые контроллеры являются более важными, чем другие, поэтому неработающая зона может отличаться от единицы к единице.</span><span class="sxs-lookup"><span data-stu-id="5c3d0-162">Please note that some controllers are more sensitive than others, thus the dead zone may vary from unit to unit.</span></span> <span data-ttu-id="5c3d0-163">Рекомендуется тестировать игры с несколькими контроллерами Xbox в разных системах.</span><span class="sxs-lookup"><span data-stu-id="5c3d0-163">It is recommended that you test your games with several Xbox controllers on different systems.</span></span>

<span data-ttu-id="5c3d0-164">Приложения должны использовать "неработающие зоны" в аналоговых входах (триггеры, устройства), чтобы указать, когда перемещение было достаточно, чтобы подсчитаться допустимым.</span><span class="sxs-lookup"><span data-stu-id="5c3d0-164">Applications should use "dead zones" on analog inputs (triggers, sticks) to indicate when a movement has been made sufficiently on the stick or trigger to be considered valid.</span></span>

<span data-ttu-id="5c3d0-165">Приложение должно проверить неработающие зоны и ответить на аппоприатели, как показано в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="5c3d0-165">Your application should check for dead zones and respond appopriately, as in this example:</span></span>

```cpp
XINPUT_STATE state = g_Controllers[i].state;

float LX = state.Gamepad.sThumbLX;
float LY = state.Gamepad.sThumbLY;

//determine how far the controller is pushed
float magnitude = sqrt(LX*LX + LY*LY);

//determine the direction the controller is pushed
float normalizedLX = LX / magnitude;
float normalizedLY = LY / magnitude;

float normalizedMagnitude = 0;

//check if the controller is outside a circular dead zone
if (magnitude > INPUT_DEADZONE)
{
    //clip the magnitude at its expected maximum value
    if (magnitude > 32767) magnitude = 32767;

    //adjust magnitude relative to the end of the dead zone
    magnitude -= INPUT_DEADZONE;

    //optionally normalize the magnitude with respect to its expected range
    //giving a magnitude value of 0.0 to 1.0
    normalizedMagnitude = magnitude / (32767 - INPUT_DEADZONE);
}
else //if the controller is in the deadzone zero out the magnitude
{
    magnitude = 0.0;
    normalizedMagnitude = 0.0;
}

//repeat for right thumb stick
```

<span data-ttu-id="5c3d0-166">В этом примере вычисляется вектор направления контроллера и расстояние от вектора, который был отправлен контроллером.</span><span class="sxs-lookup"><span data-stu-id="5c3d0-166">This example calculates the controller's direction vector and how far along the vector the controller has been pushed.</span></span> <span data-ttu-id="5c3d0-167">Это позволяет принудительно применять циклическое деадзоне, просто проверяя, превышает ли величина контроллера значение деадзоне.</span><span class="sxs-lookup"><span data-stu-id="5c3d0-167">This allows enforcement of a circular deadzone by simply checking whether the controller's magnitude is greater than the deadzone value.</span></span> <span data-ttu-id="5c3d0-168">Кроме того, код нормализует величину контроллера, которую затем можно умножить на фактор для определенной игры, чтобы преобразовать расположение контроллера в единицы, относящиеся к игре.</span><span class="sxs-lookup"><span data-stu-id="5c3d0-168">In addition the code normalizes the controller's magnitude which can then be multiplied by a game specific factor to convert the controller's position to units relevant to the game.</span></span>

<span data-ttu-id="5c3d0-169">Обратите внимание, что вы можете определить собственные зоны для устройств и триггеров (в любом месте от 0-65534) или использовать предоставленный деадзонес, определенный как \_ левый игровой планшет ксинпут \_ \_ \_ деадзоне, ксинпут \_ игровой планшет, \_ правый \_ бегунок \_ и \_ \_ \_ пороговое значение триггера игровой планшет в деадзоне. h:</span><span class="sxs-lookup"><span data-stu-id="5c3d0-169">Note that you may define your own dead zones for the sticks and triggers (anywhere from 0-65534), or you may use the provided deadzones defined as XINPUT\_GAMEPAD\_LEFT\_THUMB\_DEADZONE, XINPUT\_GAMEPAD\_RIGHT\_THUMB\_DEADZONE, and XINPUT\_GAMEPAD\_TRIGGER\_THRESHOLD in XInput.h:</span></span>

```cpp
#define XINPUT_GAMEPAD_LEFT_THUMB_DEADZONE  7849
#define XINPUT_GAMEPAD_RIGHT_THUMB_DEADZONE 8689
#define XINPUT_GAMEPAD_TRIGGER_THRESHOLD    30
```

<span data-ttu-id="5c3d0-170">После применения деадзоне может оказаться полезным масштабировать результирующий диапазон \[ 0,0.. 1.0 \] с плавающей запятой (как в примере выше) и при необходимости применить нелинейное преобразование.</span><span class="sxs-lookup"><span data-stu-id="5c3d0-170">Once the deadzone is enforced, you may find it useful to scale the resulting range \[0.0..1.0\] floating point (as in the example above), and optionally apply a non-linear transform.</span></span>

<span data-ttu-id="5c3d0-171">Например, при работе с играми может быть полезно выполнить куб результата, чтобы лучше поработать с автомобилями с помощью игрового планшета, так как кубинг дает больше точности в нижних диапазонах, что желательно, так как игроки обычно применяют мягкую принудительную работу, чтобы получить незаметное перемещение или применить жесткое принудительное выполнение в одном направлении для получения ответа на Rd.</span><span class="sxs-lookup"><span data-stu-id="5c3d0-171">For example, with driving games, it may be helpful to cube the result to provide a better feel to driving the cars using a gamepad, as cubing the result gives you more precision in the lower ranges, which is desirable, since gamers typically either apply soft force to get subtle movement or apply hard force all the way in one direction to get rd response.</span></span>

### <a name="setting-vibration-effects"></a><span data-ttu-id="5c3d0-172">Установка эффектов вибрации</span><span class="sxs-lookup"><span data-stu-id="5c3d0-172">Setting Vibration Effects</span></span>

<span data-ttu-id="5c3d0-173">Помимо состояния контроллера, вы также можете отправить данные вибрации на контроллер, чтобы изменить отзыв, предоставленный пользователю контроллера.</span><span class="sxs-lookup"><span data-stu-id="5c3d0-173">In addition to getting the state of the controller, you may also send vibration data to the controller to alter the feedback provided to the user of the controller.</span></span> <span data-ttu-id="5c3d0-174">Контроллер содержит два румбленых мотора, которые можно независимо контролировать путем передачи значений в функцию [**ксинпутсетстате**](/windows/desktop/api/XInput/nf-xinput-xinputsetstate) .</span><span class="sxs-lookup"><span data-stu-id="5c3d0-174">The controller contains two rumble motors that can be independently controlled by passing values to the [**XInputSetState**](/windows/desktop/api/XInput/nf-xinput-xinputsetstate) function.</span></span>

<span data-ttu-id="5c3d0-175">Скорость каждого мотора может быть указана с помощью значения WORD в структуре [**\_ вибрации ксинпут**](/windows/desktop/api/XInput/ns-xinput-xinput_vibration) , которая передается в функцию [**ксинпутсетстате**](/windows/desktop/api/XInput/nf-xinput-xinputsetstate) следующим образом:</span><span class="sxs-lookup"><span data-stu-id="5c3d0-175">The speed of each motor can be specified using a WORD value in the [**XINPUT\_VIBRATION**](/windows/desktop/api/XInput/ns-xinput-xinput_vibration) structure that is passed to the [**XInputSetState**](/windows/desktop/api/XInput/nf-xinput-xinputsetstate) function as follows:</span></span>

```cpp
XINPUT_VIBRATION vibration;
ZeroMemory( &vibration, sizeof(XINPUT_VIBRATION) );
vibration.wLeftMotorSpeed = 32000; // use any value between 0-65535 here
vibration.wRightMotorSpeed = 16000; // use any value between 0-65535 here
XInputSetState( i, &vibration );
```

<span data-ttu-id="5c3d0-176">Обратите внимание, что правый мотор является высокочастотным мотором, левый мотор — это двигатель с низкой частотой.</span><span class="sxs-lookup"><span data-stu-id="5c3d0-176">Note that the right motor is the high-frequency motor, the left motor is the low-frequency motor.</span></span> <span data-ttu-id="5c3d0-177">Им не всегда нужно присвоить одинаковую сумму, так как они предоставляют различные эффекты.</span><span class="sxs-lookup"><span data-stu-id="5c3d0-177">They do not always need to be set to the same amount, as they provide different effects.</span></span>

### <a name="getting-audio-device-identifiers"></a><span data-ttu-id="5c3d0-178">Получение идентификаторов звуковых устройств</span><span class="sxs-lookup"><span data-stu-id="5c3d0-178">Getting Audio Device Identifiers</span></span>

<span data-ttu-id="5c3d0-179">Головной телефон для контроллера Xbox имеет следующие функции:</span><span class="sxs-lookup"><span data-stu-id="5c3d0-179">The headset for an Xbox Controller has these functions:</span></span>

-   <span data-ttu-id="5c3d0-180">Запись звука с помощью микрофона</span><span class="sxs-lookup"><span data-stu-id="5c3d0-180">Record sound using a microphone</span></span>
-   <span data-ttu-id="5c3d0-181">Воспроизведение звука с помощью наушников</span><span class="sxs-lookup"><span data-stu-id="5c3d0-181">Play back sound using a headphone</span></span>

<span data-ttu-id="5c3d0-182">Используйте этот код для получения идентификаторов устройств для гарнитуры:</span><span class="sxs-lookup"><span data-stu-id="5c3d0-182">Use this code to obtain the device identifiers for the headset:</span></span>

```cpp
WCHAR renderId[ 256 ] = {0};
WCHAR captureId[ 256 ] = {0};
UINT rcount = 256;
UINT ccount = 256;

XInputGetAudioDeviceIds( i, renderId, &rcount, captureId, &ccount );
```

<span data-ttu-id="5c3d0-183">После получения идентификаторов устройств можно создать соответствующие интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="5c3d0-183">After you obtain the device identifiers, you can create the appropriate interfaces.</span></span> <span data-ttu-id="5c3d0-184">Например, если вы используете Ксаудио 2,8, используйте этот код для создания главной речи для этого устройства:</span><span class="sxs-lookup"><span data-stu-id="5c3d0-184">For example, if you use XAudio 2.8, use this code to create a mastering voice for this device:</span></span>

```cpp
IXAudio2* pXAudio2 = NULL;
HRESULT hr;
if ( FAILED(hr = XAudio2Create( &pXAudio2, 0, XAUDIO2_DEFAULT_PROCESSOR ) ) )
    return hr;

IXAudio2MasteringVoice* pMasterVoice = NULL;
if ( FAILED(hr = pXAudio2->CreateMasteringVoice( &pMasterVoice, XAUDIO2_DEFAULT_CHANNELS, XAUDIO2_DEFAULT_SAMPLERATE, 0, renderId, NULL, AudioCategory_Communications ) ) )
    return hr;
```

<span data-ttu-id="5c3d0-185">Сведения об использовании идентификатора устройства Каптуреид см. в разделе [запись потока](/windows/desktop/CoreAudio/capturing-a-stream).</span><span class="sxs-lookup"><span data-stu-id="5c3d0-185">For info about how to use the captureId device identifier, see [Capturing a Stream](/windows/desktop/CoreAudio/capturing-a-stream).</span></span>

### <a name="getting-directsound-guids-legacy-directx-sdk-only"></a><span data-ttu-id="5c3d0-186">Получение идентификаторов GUID DirectSound (только для устаревших пакетов SDK DirectX)</span><span class="sxs-lookup"><span data-stu-id="5c3d0-186">Getting DirectSound GUIDs (legacy DirectX SDK only)</span></span>

<span data-ttu-id="5c3d0-187">Гарнитура, которую можно подключить к контроллеру Xbox, имеет две функции: она может записывать звук с помощью микрофона, а также воспроизводить звук с помощью наушников.</span><span class="sxs-lookup"><span data-stu-id="5c3d0-187">The headset that can be connected to an Xbox Controller has two functions: it can record sound using a microphone, and it can play back sound using a headphone.</span></span> <span data-ttu-id="5c3d0-188">В API Ксинпут эти функции выполняются через [DirectSound](/previous-versions/windows/desktop/ee416960(v=vs.85))с использованием интерфейсов **IDirectSound8** и **IDirectSoundCapture8** .</span><span class="sxs-lookup"><span data-stu-id="5c3d0-188">In the XInput API, these functions are accomplished through [DirectSound](/previous-versions/windows/desktop/ee416960(v=vs.85)), using the **IDirectSound8** and **IDirectSoundCapture8** interfaces.</span></span>

<span data-ttu-id="5c3d0-189">Чтобы связать микрофон и наушники гарнитуры с соответствующими интерфейсами [DirectSound](/previous-versions/windows/desktop/ee416960(v=vs.85)) , необходимо получить директсаундгуидс для записи и отрисовки устройств, вызвав [**ксинпутжетдсаундаудиодевицегуидс**](/windows/desktop/api/XInput/nf-xinput-xinputgetdsoundaudiodeviceguids).</span><span class="sxs-lookup"><span data-stu-id="5c3d0-189">To associate the headset microphone and headphone with their appropriate [DirectSound](/previous-versions/windows/desktop/ee416960(v=vs.85)) interfaces, you must get the DirectSoundGUIDs for the capture and render devices by calling [**XInputGetDSoundAudioDeviceGuids**](/windows/desktop/api/XInput/nf-xinput-xinputgetdsoundaudiodeviceguids).</span></span>

> [!Note]  
> <span data-ttu-id="5c3d0-190">Использование устаревшей [DirectSound](/previous-versions/windows/desktop/ee416960(v=vs.85)) не рекомендуется и недоступно в приложениях для Магазина Windows.</span><span class="sxs-lookup"><span data-stu-id="5c3d0-190">Use of the legacy [DirectSound](/previous-versions/windows/desktop/ee416960(v=vs.85)) is not recommended, and is not available in Windows Store apps.</span></span> <span data-ttu-id="5c3d0-191">Сведения в этом разделе относятся только к версии пакета SDK для DirectX Ксинпут (Ксинпут 1,3).</span><span class="sxs-lookup"><span data-stu-id="5c3d0-191">The info in this section only applies to the DirectX SDK version of XInput (XInput 1.3).</span></span> <span data-ttu-id="5c3d0-192">Версия Ксинпут (Ксинпут 1,4) для Windows 8 использует только идентификаторы устройств API Windows Audio (ВАСАПИ), полученные через [**ксинпутжетаудиодевицеидс**](/windows/desktop/api/XInput/nf-xinput-xinputgetaudiodeviceids).</span><span class="sxs-lookup"><span data-stu-id="5c3d0-192">The Windows 8 version of XInput (XInput 1.4) exclusively uses Windows Audio Session API (WASAPI) device identifiers that are obtained through [**XInputGetAudioDeviceIds**](/windows/desktop/api/XInput/nf-xinput-xinputgetaudiodeviceids).</span></span>

```cpp
XInputGetDSoundAudioDeviceGuids( i, &dsRenderGuid, &dsCaptureGuid );

```

<span data-ttu-id="5c3d0-193">После получения идентификаторов GUID можно создать соответствующие интерфейсы, вызвав DirectSoundCreate8 и DirectSoundCaptureCreate8 следующим образом:</span><span class="sxs-lookup"><span data-stu-id="5c3d0-193">Once you have retrieved the GUIDs you can create the appropriate interfaces by calling DirectSoundCreate8 and DirectSoundCaptureCreate8 like this:</span></span>

```cpp
// Create IDirectSound8 using the controller's render device
if( FAILED( hr = DirectSoundCreate8( &dsRenderGuid, &pDS, NULL ) ) )
   return hr;

// Set coop level to DSSCL_PRIORITY
if( FAILED( hr = pDS->SetCooperativeLevel( hWnd, DSSCL_NORMAL ) ) )
   return hr;

// Create IDirectSoundCapture using the controller's capture device
if( FAILED( hr = DirectSoundCaptureCreate8( &dsCaptureGuid, &pDSCapture, NULL ) ) )
   return hr;
```

## <a name="related-topics"></a><span data-ttu-id="5c3d0-194">См. также</span><span class="sxs-lookup"><span data-stu-id="5c3d0-194">Related topics</span></span>

[<span data-ttu-id="5c3d0-195">Справочник по программированию</span><span class="sxs-lookup"><span data-stu-id="5c3d0-195">Programming Reference</span></span>](programming-reference.md)