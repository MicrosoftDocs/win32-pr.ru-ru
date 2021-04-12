---
title: Сообщение WM_GESTURE (Winuser. h)
description: Передает сведения о жесте.
ms.assetid: 4167aeb0-2c31-4b7b-ad1b-e6d37da09ef8
keywords:
- WM_GESTURE сообщений Windows Touch
topic_type:
- apiref
api_name:
- WM_GESTURE
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d1184d1f54d110f84630a727decb91ad28e6c08
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415813"
---
# <a name="wm_gesture-message"></a><span data-ttu-id="c0cb7-104">\_Сообщение жеста WM</span><span class="sxs-lookup"><span data-stu-id="c0cb7-104">WM\_GESTURE message</span></span>

<span data-ttu-id="c0cb7-105">Передает сведения о жесте.</span><span class="sxs-lookup"><span data-stu-id="c0cb7-105">Passes information about a gesture.</span></span>

## <a name="parameters"></a><span data-ttu-id="c0cb7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c0cb7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0cb7-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c0cb7-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c0cb7-108">Предоставляет сведения, идентифицирующие команду жеста и значения аргумента, относящиеся к жесту.</span><span class="sxs-lookup"><span data-stu-id="c0cb7-108">Provides information identifying the gesture command and gesture-specific argument values.</span></span> <span data-ttu-id="c0cb7-109">Эти сведения являются теми же данными, которые передаются в члене **улларгументс** структуры [**GESTUREINFO**](/windows/win32/api/winuser/ns-winuser-gestureinfo) .</span><span class="sxs-lookup"><span data-stu-id="c0cb7-109">This information is the same information passed in the **ullArguments** member of the [**GESTUREINFO**](/windows/win32/api/winuser/ns-winuser-gestureinfo) structure.</span></span>

</dd> <dt>

<span data-ttu-id="c0cb7-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c0cb7-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c0cb7-111">Предоставляет описатель для сведений, идентифицирующих команду жеста и значения аргумента, относящиеся к жесту.</span><span class="sxs-lookup"><span data-stu-id="c0cb7-111">Provides a handle to information identifying the gesture command and gesture-specific argument values.</span></span> <span data-ttu-id="c0cb7-112">Эти сведения извлекаются путем вызова [**жетжестуреинфо**](/windows/desktop/api/winuser/nf-winuser-getgestureinfo).</span><span class="sxs-lookup"><span data-stu-id="c0cb7-112">This information is retrieved by calling [**GetGestureInfo**](/windows/desktop/api/winuser/nf-winuser-getgestureinfo).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0cb7-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c0cb7-113">Return value</span></span>

<span data-ttu-id="c0cb7-114">Если приложение обрабатывает это сообщение, оно должно возвращать значение 0.</span><span class="sxs-lookup"><span data-stu-id="c0cb7-114">If an application processes this message, it should return 0.</span></span>

<span data-ttu-id="c0cb7-115">Если приложение не обрабатывает сообщение, оно должно вызвать [дефвиндовпрок](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="c0cb7-115">If the application does not process the message, it must call [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span> <span data-ttu-id="c0cb7-116">Это приведет к утечке памяти в приложении, поскольку дескриптор сенсорного ввода не будет закрыт, а связанная память процесса не будет освобождена.</span><span class="sxs-lookup"><span data-stu-id="c0cb7-116">Not doing so will cause the application to leak memory because the touch input handle will not be closed and associated process memory will not be freed.</span></span>

## <a name="remarks"></a><span data-ttu-id="c0cb7-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c0cb7-117">Remarks</span></span>

<span data-ttu-id="c0cb7-118">В следующей таблице перечислены поддерживаемые команды жестов.</span><span class="sxs-lookup"><span data-stu-id="c0cb7-118">The following table lists the supported gesture commands.</span></span>



| <span data-ttu-id="c0cb7-119">Идентификатор жеста</span><span class="sxs-lookup"><span data-stu-id="c0cb7-119">Gesture ID</span></span>            | <span data-ttu-id="c0cb7-120">Значение (*ДВИД*)</span><span class="sxs-lookup"><span data-stu-id="c0cb7-120">Value (*dwID*)</span></span> | <span data-ttu-id="c0cb7-121">Описание</span><span class="sxs-lookup"><span data-stu-id="c0cb7-121">Description</span></span>                                                                                                                                                                                                                                                                          |
|-----------------------|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0cb7-122">**\_Начало GID**</span><span class="sxs-lookup"><span data-stu-id="c0cb7-122">**GID\_BEGIN**</span></span>        | <span data-ttu-id="c0cb7-123">1</span><span class="sxs-lookup"><span data-stu-id="c0cb7-123">1</span></span>              | <span data-ttu-id="c0cb7-124">Указывает, что начинается универсальный жест.</span><span class="sxs-lookup"><span data-stu-id="c0cb7-124">Indicates a generic gesture is beginning.</span></span>                                                                                                                                                                                                                                            |
| <span data-ttu-id="c0cb7-125">**\_конец GID**</span><span class="sxs-lookup"><span data-stu-id="c0cb7-125">**GID\_END**</span></span>          | <span data-ttu-id="c0cb7-126">2</span><span class="sxs-lookup"><span data-stu-id="c0cb7-126">2</span></span>              | <span data-ttu-id="c0cb7-127">Указывает на завершение универсального жеста.</span><span class="sxs-lookup"><span data-stu-id="c0cb7-127">Indicates a generic gesture end.</span></span>                                                                                                                                                                                                                                                     |
| <span data-ttu-id="c0cb7-128">**\_масштаб GID**</span><span class="sxs-lookup"><span data-stu-id="c0cb7-128">**GID\_ZOOM**</span></span>         | <span data-ttu-id="c0cb7-129">3</span><span class="sxs-lookup"><span data-stu-id="c0cb7-129">3</span></span>              | <span data-ttu-id="c0cb7-130">Указывает на начало и перемещение масштаба, а также на отмену масштабирования.</span><span class="sxs-lookup"><span data-stu-id="c0cb7-130">Indicates zoom start, zoom move, or zoom stop.</span></span> <span data-ttu-id="c0cb7-131">Первое сообщение **команды \_ масштабирования GID** начинает масштаб, но не приводит к его уменьшению.</span><span class="sxs-lookup"><span data-stu-id="c0cb7-131">The first **GID\_ZOOM** command message begins a zoom but does not cause any zooming.</span></span> <span data-ttu-id="c0cb7-132">Вторая команда **GID \_ Zoom** активирует масштаб относительно состояния, содержащегося в первом **\_ масштабе GID**.</span><span class="sxs-lookup"><span data-stu-id="c0cb7-132">The second **GID\_ZOOM** command triggers a zoom relative to the state contained in the first **GID\_ZOOM**.</span></span>                                    |
| <span data-ttu-id="c0cb7-133">**\_сдвиг GID**</span><span class="sxs-lookup"><span data-stu-id="c0cb7-133">**GID\_PAN**</span></span>          | <span data-ttu-id="c0cb7-134">4</span><span class="sxs-lookup"><span data-stu-id="c0cb7-134">4</span></span>              | <span data-ttu-id="c0cb7-135">Указывает на начало перемещения или сдвиг.</span><span class="sxs-lookup"><span data-stu-id="c0cb7-135">Indicates pan move or pan start.</span></span> <span data-ttu-id="c0cb7-136">Первая команда **" \_ сдвиг GID** " указывает на начало Pan, но не выполняет панорамирование.</span><span class="sxs-lookup"><span data-stu-id="c0cb7-136">The first **GID\_PAN** command indicates a pan start but does not perform any panning.</span></span> <span data-ttu-id="c0cb7-137">Во втором сообщении команды **GID \_ Pan** приложение начнет панорамирование.</span><span class="sxs-lookup"><span data-stu-id="c0cb7-137">With the second **GID\_PAN** command message, the application will begin panning.</span></span>                                                                            |
| <span data-ttu-id="c0cb7-138">**\_поворот GID**</span><span class="sxs-lookup"><span data-stu-id="c0cb7-138">**GID\_ROTATE**</span></span>       | <span data-ttu-id="c0cb7-139">5</span><span class="sxs-lookup"><span data-stu-id="c0cb7-139">5</span></span>              | <span data-ttu-id="c0cb7-140">Указывает поворот перемещения или начало.</span><span class="sxs-lookup"><span data-stu-id="c0cb7-140">Indicates rotate move or rotate start.</span></span> <span data-ttu-id="c0cb7-141">Первое сообщение-команда **\_ смены GID** указывает на перемещение или поворот начала, но не будет вращаться.</span><span class="sxs-lookup"><span data-stu-id="c0cb7-141">The first **GID\_ROTATE** command message indicates a rotate move or rotate start but will not rotate.</span></span> <span data-ttu-id="c0cb7-142">Второе сообщение-команда **\_ смены GID** активирует операцию вращения относительно состояния, содержащегося в первом **\_ повернутом GID**.</span><span class="sxs-lookup"><span data-stu-id="c0cb7-142">The second **GID\_ROTATE** command message will trigger a rotation operation relative to state contained in the first **GID\_ROTATE**.</span></span> |
| <span data-ttu-id="c0cb7-143">**GID \_ твофинжертап**</span><span class="sxs-lookup"><span data-stu-id="c0cb7-143">**GID\_TWOFINGERTAP**</span></span> | <span data-ttu-id="c0cb7-144">6</span><span class="sxs-lookup"><span data-stu-id="c0cb7-144">6</span></span>              | <span data-ttu-id="c0cb7-145">Указывает жест касания двумя пальцами.</span><span class="sxs-lookup"><span data-stu-id="c0cb7-145">Indicates two-finger tap gesture.</span></span>                                                                                                                                                                                                                                                    |
| <span data-ttu-id="c0cb7-146">**GID \_ прессандтап**</span><span class="sxs-lookup"><span data-stu-id="c0cb7-146">**GID\_PRESSANDTAP**</span></span>  | <span data-ttu-id="c0cb7-147">7</span><span class="sxs-lookup"><span data-stu-id="c0cb7-147">7</span></span>              | <span data-ttu-id="c0cb7-148">Указывает жест нажатия и касания.</span><span class="sxs-lookup"><span data-stu-id="c0cb7-148">Indicates the press and tap gesture.</span></span>                                                                                                                                                                                                                                                 |



 

> [!Note]  
> <span data-ttu-id="c0cb7-149">Чтобы включить поддержку устаревшей версии, сообщения с командами **\_ конечного** жеста **\_ Begin** и GID должны быть перенаправлены с помощью [дефвиндовпрок](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="c0cb7-149">In order to enable legacy support, messages with the **GID\_BEGIN** and **GID\_END** gesture commands need to be forwarded using [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span>

 

<span data-ttu-id="c0cb7-150">В следующей таблице указаны аргументы жеста, передаваемые в параметрах *lParam* и *wParam* .</span><span class="sxs-lookup"><span data-stu-id="c0cb7-150">The following table indicates the gesture arguments passed in the *lParam* and *wParam* parameters.</span></span>



| <span data-ttu-id="c0cb7-151">Идентификатор жеста</span><span class="sxs-lookup"><span data-stu-id="c0cb7-151">Gesture ID</span></span>            | <span data-ttu-id="c0cb7-152">жесты</span><span class="sxs-lookup"><span data-stu-id="c0cb7-152">Gesture</span></span>        | <span data-ttu-id="c0cb7-153">*улларгумент*</span><span class="sxs-lookup"><span data-stu-id="c0cb7-153">*ullArgument*</span></span>                                                                                                                                                                                                                                                                                                                                                                                            | <span data-ttu-id="c0cb7-154">*птслокатион* в структуре [**GestureInfo**](/windows/desktop/api/winuser/nf-winuser-getgestureinfo)</span><span class="sxs-lookup"><span data-stu-id="c0cb7-154">*ptsLocation* in [**GestureInfo**](/windows/desktop/api/winuser/nf-winuser-getgestureinfo) structure</span></span>                                                  |
|-----------------------|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0cb7-155">**\_масштаб GID**</span><span class="sxs-lookup"><span data-stu-id="c0cb7-155">**GID\_ZOOM**</span></span>         | <span data-ttu-id="c0cb7-156">Увеличить/уменьшить</span><span class="sxs-lookup"><span data-stu-id="c0cb7-156">Zoom In/Out</span></span>    | <span data-ttu-id="c0cb7-157">Указывает расстояние между двумя точками.</span><span class="sxs-lookup"><span data-stu-id="c0cb7-157">Indicates the distance between the two points.</span></span>                                                                                                                                                                                                                                                                                                                                                           | <span data-ttu-id="c0cb7-158">Указывает центр масштабирования.</span><span class="sxs-lookup"><span data-stu-id="c0cb7-158">Indicates the center of the zoom.</span></span>                                                                                 |
| <span data-ttu-id="c0cb7-159">**\_сдвиг GID**</span><span class="sxs-lookup"><span data-stu-id="c0cb7-159">**GID\_PAN**</span></span>          | <span data-ttu-id="c0cb7-160">Сдвиг</span><span class="sxs-lookup"><span data-stu-id="c0cb7-160">Pan</span></span>            | <span data-ttu-id="c0cb7-161">Указывает расстояние между двумя точками.</span><span class="sxs-lookup"><span data-stu-id="c0cb7-161">Indicates the distance between the two points.</span></span>                                                                                                                                                                                                                                                                                                                                                           | <span data-ttu-id="c0cb7-162">Указывает текущее расположение панорамы.</span><span class="sxs-lookup"><span data-stu-id="c0cb7-162">Indicates the current position of the pan.</span></span>                                                                        |
| <span data-ttu-id="c0cb7-163">**\_поворот GID**</span><span class="sxs-lookup"><span data-stu-id="c0cb7-163">**GID\_ROTATE**</span></span>       | <span data-ttu-id="c0cb7-164">Повернуть (сведение)</span><span class="sxs-lookup"><span data-stu-id="c0cb7-164">Rotate (pivot)</span></span> | <span data-ttu-id="c0cb7-165">Указывает угол поворота, если установлен флаг **GF \_ Begin** .</span><span class="sxs-lookup"><span data-stu-id="c0cb7-165">Indicates the angle of rotation if the **GF\_BEGIN** flag is set.</span></span> <span data-ttu-id="c0cb7-166">В противном случае это изменение угла с момента начала вращения.</span><span class="sxs-lookup"><span data-stu-id="c0cb7-166">Otherwise, this is the angle change since the rotation has started.</span></span> <span data-ttu-id="c0cb7-167">Это подписывается для обозначения направления вращения.</span><span class="sxs-lookup"><span data-stu-id="c0cb7-167">This is signed to indicate the direction of the rotation.</span></span> <span data-ttu-id="c0cb7-168">Чтобы получить и задать значение угла, используйте угол [**\_ поворота GID \_ \_ от \_ ARGUMENT**](/windows/desktop/api/winuser/nf-winuser-gid_rotate_angle_from_argument) и [**GID \_ угла поворота в макросах \_ \_ \_ аргументов**](/windows/desktop/api/winuser/nf-winuser-gid_rotate_angle_to_argument) .</span><span class="sxs-lookup"><span data-stu-id="c0cb7-168">Use the [**GID\_ROTATE\_ANGLE\_FROM\_ARGUMENT**](/windows/desktop/api/winuser/nf-winuser-gid_rotate_angle_from_argument) and [**GID\_ROTATE\_ANGLE\_TO\_ARGUMENT**](/windows/desktop/api/winuser/nf-winuser-gid_rotate_angle_to_argument) macros to get and set the angle value.</span></span> | <span data-ttu-id="c0cb7-169">Указывает центр вращения, который является стационарной точкой, вокруг которой вращается целевой объект.</span><span class="sxs-lookup"><span data-stu-id="c0cb7-169">This indicates the center of the rotation which is the stationary point that the target object is rotated around.</span></span> |
| <span data-ttu-id="c0cb7-170">**GID \_ твофинжертап**</span><span class="sxs-lookup"><span data-stu-id="c0cb7-170">**GID\_TWOFINGERTAP**</span></span> | <span data-ttu-id="c0cb7-171">Касание с двумя пальцами</span><span class="sxs-lookup"><span data-stu-id="c0cb7-171">Two-finger Tap</span></span> | <span data-ttu-id="c0cb7-172">Указывает расстояние между двумя пальцами.</span><span class="sxs-lookup"><span data-stu-id="c0cb7-172">Indicates the distance between the two fingers.</span></span>                                                                                                                                                                                                                                                                                                                                                          | <span data-ttu-id="c0cb7-173">Указывает центр двух пальцев.</span><span class="sxs-lookup"><span data-stu-id="c0cb7-173">Indicates the center of the two fingers.</span></span>                                                                          |
| <span data-ttu-id="c0cb7-174">**GID \_ прессандтап**</span><span class="sxs-lookup"><span data-stu-id="c0cb7-174">**GID\_PRESSANDTAP**</span></span>  | <span data-ttu-id="c0cb7-175">Нажмите и коснитесь</span><span class="sxs-lookup"><span data-stu-id="c0cb7-175">Press and Tap</span></span>  | <span data-ttu-id="c0cb7-176">Указывает разницу между первым пальцем и вторым пальцем.</span><span class="sxs-lookup"><span data-stu-id="c0cb7-176">Indicates the delta between the first finger and the second finger.</span></span> <span data-ttu-id="c0cb7-177">Это значение хранится в младших 32 битах *улларгумент* в структуре **Point** .</span><span class="sxs-lookup"><span data-stu-id="c0cb7-177">This value is stored in the lower 32 bits of the *ullArgument* in a **POINT** structure.</span></span>                                                                                                                                                                                                                                             | <span data-ttu-id="c0cb7-178">Указывает, на какой должности поступает первый палец.</span><span class="sxs-lookup"><span data-stu-id="c0cb7-178">Indicates the position that the first finger comes down on.</span></span>                                                       |



 

> [!Note]  
> <span data-ttu-id="c0cb7-179">Все расстояния и положения задаются в координатах физического экрана.</span><span class="sxs-lookup"><span data-stu-id="c0cb7-179">All distances and positions are provided in physical screen coordinates.</span></span>

 

> [!Note]  
> <span data-ttu-id="c0cb7-180">Параметры *ДВИД* и *улларгумент* следует рассматривать как сопровождающие \_ \* команды GID и не должны изменяться приложениями.</span><span class="sxs-lookup"><span data-stu-id="c0cb7-180">The *dwID* and *ullArgument* parameters should only be considered to be accompanying the GID\_\* commands and should not be altered by applications.</span></span>

 

## <a name="examples"></a><span data-ttu-id="c0cb7-181">Примеры</span><span class="sxs-lookup"><span data-stu-id="c0cb7-181">Examples</span></span>

<span data-ttu-id="c0cb7-182">В следующем коде показано, как получить сведения о жесте, связанные с этим сообщением.</span><span class="sxs-lookup"><span data-stu-id="c0cb7-182">The following code illustrates how to obtain gesture-specific information associated with this message.</span></span>

> [!Note]  
> <span data-ttu-id="c0cb7-183">Следует всегда пересылать необработанные сообщения [дефвиндовпрок](/windows/win32/api/winuser/nf-winuser-defwindowproca) и закрывать входной маркер жеста для сообщений, обрабатываемых с помощью вызова [**клосежестуреинфохандле**](/windows/desktop/api/winuser/nf-winuser-closegestureinfohandle).</span><span class="sxs-lookup"><span data-stu-id="c0cb7-183">You should always forward unhandled messages to [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) and should close the gesture input handle for messages that you do handle with a call to [**CloseGestureInfoHandle**](/windows/desktop/api/winuser/nf-winuser-closegestureinfohandle).</span></span> <span data-ttu-id="c0cb7-184">В этом примере поведение обработчика жестов по умолчанию будет подавлено, так как дескриптор ТАУЧИНПУТ закрывается в каждом из вариантов жестов.</span><span class="sxs-lookup"><span data-stu-id="c0cb7-184">In this example, the default gesture handler behavior will be suppressed because the TOUCHINPUT handle is closed in each of the gesture cases.</span></span> <span data-ttu-id="c0cb7-185">Если вы удалили варианты в приведенном выше коде для необработанных сообщений, обработчик жестов по умолчанию будет обрабатывать сообщения, пересылаемые в [дефвиндовпрок](/windows/win32/api/winuser/nf-winuser-defwindowproca) в случае по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c0cb7-185">If you removed the cases in the above code for unhandled messages, the default gesture handler would process the messages by getting forwarded to [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) in the default case.</span></span>

 


```C++
  LRESULT DecodeGesture(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam){
    // Create a structure to populate and retrieve the extra message info.
    GESTUREINFO gi;  
    
    ZeroMemory(&gi, sizeof(GESTUREINFO));
    
    gi.cbSize = sizeof(GESTUREINFO);

    BOOL bResult  = GetGestureInfo((HGESTUREINFO)lParam, &gi);
    BOOL bHandled = FALSE;

    if (bResult){
        // now interpret the gesture
        switch (gi.dwID){
           case GID_ZOOM:
               // Code for zooming goes here     
               bHandled = TRUE;
               break;
           case GID_PAN:
               // Code for panning goes here
               bHandled = TRUE;
               break;
           case GID_ROTATE:
               // Code for rotation goes here
               bHandled = TRUE;
               break;
           case GID_TWOFINGERTAP:
               // Code for two-finger tap goes here
               bHandled = TRUE;
               break;
           case GID_PRESSANDTAP:
               // Code for roll over goes here
               bHandled = TRUE;
               break;
           default:
               // A gesture was not recognized
               break;
        }
    }else{
        DWORD dwErr = GetLastError();
        if (dwErr > 0){
            //MessageBoxW(hWnd, L"Error!", L"Could not retrieve a GESTUREINFO structure.", MB_OK);
        }
    }
    if (bHandled){
        return 0;
    }else{
        return DefWindowProc(hWnd, message, wParam, lParam);
    }
  }
```



## <a name="requirements"></a><span data-ttu-id="c0cb7-186">Требования</span><span class="sxs-lookup"><span data-stu-id="c0cb7-186">Requirements</span></span>



| <span data-ttu-id="c0cb7-187">Требование</span><span class="sxs-lookup"><span data-stu-id="c0cb7-187">Requirement</span></span> | <span data-ttu-id="c0cb7-188">Значение</span><span class="sxs-lookup"><span data-stu-id="c0cb7-188">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0cb7-189">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c0cb7-189">Minimum supported client</span></span><br/> | <span data-ttu-id="c0cb7-190">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="c0cb7-190">Windows 7 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="c0cb7-191">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c0cb7-191">Minimum supported server</span></span><br/> | <span data-ttu-id="c0cb7-192">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="c0cb7-192">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                  |
| <span data-ttu-id="c0cb7-193">Header</span><span class="sxs-lookup"><span data-stu-id="c0cb7-193">Header</span></span><br/>                   | <dl> <span data-ttu-id="c0cb7-194"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c0cb7-194"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0cb7-195">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c0cb7-195">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0cb7-196">Уведомления</span><span class="sxs-lookup"><span data-stu-id="c0cb7-196">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="c0cb7-197">Инструкции по программированию жестов сенсорного ввода Windows</span><span class="sxs-lookup"><span data-stu-id="c0cb7-197">Windows Touch Gestures Programming Guide</span></span>](guide-multi-touch-gestures.md)
</dt> </dl>

 

