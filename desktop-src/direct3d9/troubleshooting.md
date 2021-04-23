---
description: В этом разделе перечислены распространенные категории проблем, которые могут возникнуть при написании приложений Direct3D, и способы их предотвращения.
ms.assetid: 27b87f0f-7118-4252-b6e8-6ea18a9399e4
title: Устранение неполадок (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6726e761dd8c15e2da18e6c370472a73e82cef0b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105710676"
---
# <a name="troubleshooting-direct3d-9"></a><span data-ttu-id="b4eea-103">Устранение неполадок (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="b4eea-103">Troubleshooting (Direct3D 9)</span></span>

<span data-ttu-id="b4eea-104">В этом разделе перечислены распространенные категории проблем, которые могут возникнуть при написании приложений Direct3D, и способы их предотвращения.</span><span class="sxs-lookup"><span data-stu-id="b4eea-104">This topic lists common categories of problems that you might encounter when writing Direct3D applications, and how to prevent them.</span></span>

## <a name="device-creation"></a><span data-ttu-id="b4eea-105">Создание устройства</span><span class="sxs-lookup"><span data-stu-id="b4eea-105">Device Creation</span></span>

<span data-ttu-id="b4eea-106">Если во время создания устройства происходит сбой приложения, проверьте наличие следующих распространенных ошибок.</span><span class="sxs-lookup"><span data-stu-id="b4eea-106">If your application fails during device creation, check for the following common errors.</span></span>

-   <span data-ttu-id="b4eea-107">Убедитесь, что вы проверите возможности устройства, в частности, глубины прорисовки.</span><span class="sxs-lookup"><span data-stu-id="b4eea-107">Make sure you check the device capabilities, particularly the render depths.</span></span>
-   <span data-ttu-id="b4eea-108">Изучите код ошибки.</span><span class="sxs-lookup"><span data-stu-id="b4eea-108">Examine the error code.</span></span> <span data-ttu-id="b4eea-109">D3DERR \_ аутофвидеомемори всегда возможно.</span><span class="sxs-lookup"><span data-stu-id="b4eea-109">D3DERR\_OUTOFVIDEOMEMORY is always possible.</span></span>
-   <span data-ttu-id="b4eea-110">Используйте отладочные библиотеки динамической компоновки DirectX (DLL) и проверьте выходные сообщения в отладчике.</span><span class="sxs-lookup"><span data-stu-id="b4eea-110">Use the debug DirectX dynamic-link libraries (DLLs) and review output messages under the debugger.</span></span>

## <a name="using-lit-vertices"></a><span data-ttu-id="b4eea-111">Использование освещенных вершин</span><span class="sxs-lookup"><span data-stu-id="b4eea-111">Using Lit Vertices</span></span>

<span data-ttu-id="b4eea-112">Приложения, использующие освещенные вершины, должны отключить подсистему освещения Direct3D, установив \_ для состояния рендеринга D3DRS **значение false**.</span><span class="sxs-lookup"><span data-stu-id="b4eea-112">Applications that use lit vertices should disable the Direct3D lighting engine by setting the D3DRS\_LIGHTING render state to **FALSE**.</span></span> <span data-ttu-id="b4eea-113">По умолчанию, когда освещение включено, система устанавливает цвет для любой вершины, которая не содержит обычного вектора в 0 (черный цвет), даже если входная вершина содержала ненулевое значение цвета.</span><span class="sxs-lookup"><span data-stu-id="b4eea-113">By default, when lighting is enabled, the system sets the color for any vertex that doesn't contain a normal vector to 0 (black), even if the input vertex contained a nonzero color value.</span></span> <span data-ttu-id="b4eea-114">Так как освещенные вершины не, по своей природе, содержат нормальную вершину, любые сведения о цветах, передаваемые в Direct3D, теряются при отрисовке, если включен механизм освещения.</span><span class="sxs-lookup"><span data-stu-id="b4eea-114">Because lit-vertices don't, by their nature, contain a vertex normal, any color information passed to Direct3D is lost during rendering if the lighting engine is enabled.</span></span>

<span data-ttu-id="b4eea-115">Очевидно, что цвет вершины важен для любого приложения, которое выполняет собственное освещение.</span><span class="sxs-lookup"><span data-stu-id="b4eea-115">Obviously, vertex color is important to any application that performs its own lighting.</span></span> <span data-ttu-id="b4eea-116">Чтобы система не установления значения по умолчанию, убедитесь, что для параметра D3DRS \_ освещение установлено **значение false**.</span><span class="sxs-lookup"><span data-stu-id="b4eea-116">To prevent the system from imposing the default values, make sure you set D3DRS\_LIGHTING to **FALSE**.</span></span>

<span data-ttu-id="b4eea-117">Если приложение выполняется, но ничего не отображается, проверьте наличие следующих распространенных ошибок.</span><span class="sxs-lookup"><span data-stu-id="b4eea-117">If your application runs but nothing is visible, check for the following common errors.</span></span>

-   <span data-ttu-id="b4eea-118">Убедитесь, что треугольники не выводятся.</span><span class="sxs-lookup"><span data-stu-id="b4eea-118">Ensure that your triangles are not degenerate.</span></span>
-   <span data-ttu-id="b4eea-119">Убедитесь, что ваши треугольники не исключаются.</span><span class="sxs-lookup"><span data-stu-id="b4eea-119">Ensure that your triangles are not being culled.</span></span>
-   <span data-ttu-id="b4eea-120">Убедитесь, что преобразования внутренне согласованы.</span><span class="sxs-lookup"><span data-stu-id="b4eea-120">Make sure that your transformations are internally consistent.</span></span>
-   <span data-ttu-id="b4eea-121">Проверьте параметры окна просмотра, чтобы убедиться, что они позволяют видеть треугольники.</span><span class="sxs-lookup"><span data-stu-id="b4eea-121">Check the viewport settings to be sure they allow your triangles to be seen.</span></span>

## <a name="debugging"></a><span data-ttu-id="b4eea-122">Отладка</span><span class="sxs-lookup"><span data-stu-id="b4eea-122">Debugging</span></span>

<span data-ttu-id="b4eea-123">Отладка приложения Direct3D может быть непростой задачей.</span><span class="sxs-lookup"><span data-stu-id="b4eea-123">Debugging a Direct3D application can be challenging.</span></span> <span data-ttu-id="b4eea-124">Воспользуйтесь следующими методами, помимо проверки всех возвращаемых значений, особенно важных советов по программированию Direct3D, которые зависят от реализации оборудования.</span><span class="sxs-lookup"><span data-stu-id="b4eea-124">Try the following techniques, in addition to checking all the return values - a particularly important piece of advice in Direct3D programming, which is dependent on very different hardware implementations.</span></span>

-   <span data-ttu-id="b4eea-125">Переключитесь на отладку библиотек DLL.</span><span class="sxs-lookup"><span data-stu-id="b4eea-125">Switch to debug DLLs.</span></span>
-   <span data-ttu-id="b4eea-126">Принудительно использовать программное устройство, отключив аппаратное ускорение, даже если оно доступно.</span><span class="sxs-lookup"><span data-stu-id="b4eea-126">Force a software-only device, turning off hardware acceleration even when it is available.</span></span>
-   <span data-ttu-id="b4eea-127">Принудительный запуск поверхностей в системной памяти.</span><span class="sxs-lookup"><span data-stu-id="b4eea-127">Force surfaces into system memory.</span></span>
-   <span data-ttu-id="b4eea-128">Создайте параметр для запуска в окне, чтобы можно было использовать встроенный отладчик.</span><span class="sxs-lookup"><span data-stu-id="b4eea-128">Create an option to run in a window, so that you can use an integrated debugger.</span></span>

<span data-ttu-id="b4eea-129">Второй и третий параметры в этом списке позволяют избежать блокировки Win16, которая в противном случае может привести к зависанию отладчика.</span><span class="sxs-lookup"><span data-stu-id="b4eea-129">The second and third options in this list can help you avoid the Win16 lock which can otherwise cause your debugger to hang.</span></span>

<span data-ttu-id="b4eea-130">Кроме того, попробуйте добавить следующие записи в Win.ini.</span><span class="sxs-lookup"><span data-stu-id="b4eea-130">Also, try adding the following entries to Win.ini.</span></span>


```
[Direct3D] 
debug=3 
[DirectDraw] 
debug=3 
```



## <a name="borland-floating-point-initialization"></a><span data-ttu-id="b4eea-131">Инициализация Floating-Point Borland</span><span class="sxs-lookup"><span data-stu-id="b4eea-131">Borland Floating-Point Initialization</span></span>

<span data-ttu-id="b4eea-132">Компиляторы от Borland сообщают об исключениях с плавающей запятой способом, несовместимым с Direct3D.</span><span class="sxs-lookup"><span data-stu-id="b4eea-132">Compilers from Borland report floating-point exceptions in a manner that is incompatible with Direct3D.</span></span> <span data-ttu-id="b4eea-133">Чтобы решить эту проблему, включите \_ обработчик исключений matherr, как в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="b4eea-133">To solve this problem, include a \_matherr exception handler like the following:</span></span>


```
// Borland floating point initialization 
#include <math.h>
#include <float.h>

void initfp(void)
{
    // Disable floating point exceptions
    _control87(MCW_EM,MCW_EM);
}

int _matherr(struct _exception  *e)
{
    e;               // Dummy reference to catch the warning
    return 1;        // Error has been handled
}
```



## <a name="parameter-validation"></a><span data-ttu-id="b4eea-134">Проверка параметров</span><span class="sxs-lookup"><span data-stu-id="b4eea-134">Parameter Validation</span></span>

<span data-ttu-id="b4eea-135">По соображениям производительности отладочная версия времени выполнения Direct3D в режиме интерпретации выполняет больше проверки параметров, чем розничная версия, которая иногда не выполняет никакой проверки.</span><span class="sxs-lookup"><span data-stu-id="b4eea-135">For performance reasons, the debug version of the Direct3D Immediate Mode run time performs more parameter validation than the retail version, which sometimes performs no validation at all.</span></span> <span data-ttu-id="b4eea-136">Это позволяет приложениям выполнять надежную отладку с медленным компонентом времени выполнения отладки, прежде чем использовать более быструю розничную версию для настройки производительности и окончательного выпуска.</span><span class="sxs-lookup"><span data-stu-id="b4eea-136">This enables applications to perform robust debugging with the slower debug run-time component before using the faster retail version for performance tuning and final release.</span></span>

<span data-ttu-id="b4eea-137">Хотя несколько методов режима интерпретации Direct3D накладывают ограничения на значения, которые они могут принимать, эти ограничения часто проверяются и применяются в отладочной версии времени выполнения Direct3D Mode.</span><span class="sxs-lookup"><span data-stu-id="b4eea-137">Although several Direct3D Immediate Mode methods impose limits on the values that they can accept, these limits are often only checked and enforced by the debug version of the Direct3D Immediate Mode run time.</span></span> <span data-ttu-id="b4eea-138">Приложения должны соответствовать этим ограничениям, или непредсказуемые и нежелательные результаты могут возникать при выполнении в розничной версии Direct3D.</span><span class="sxs-lookup"><span data-stu-id="b4eea-138">Applications must conform to these limits, or unpredictable and undesirable results can occur when running on the retail version of Direct3D.</span></span> <span data-ttu-id="b4eea-139">Например, метод [**IDirect3DDevice9::D равпримитиве**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) принимает параметр (примитивекаунт), который указывает количество примитивов, которые будут отображены методом.</span><span class="sxs-lookup"><span data-stu-id="b4eea-139">For example, the [**IDirect3DDevice9::DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) method accepts a parameter (PrimitiveCount) that indicates the number of primitives that the method will render.</span></span> <span data-ttu-id="b4eea-140">Метод может принимать значения только от 0 до D3DMAXNUMPRIMITIVES.</span><span class="sxs-lookup"><span data-stu-id="b4eea-140">The method can only accept values between 0 and D3DMAXNUMPRIMITIVES.</span></span> <span data-ttu-id="b4eea-141">В отладочной версии Direct3D при передаче более чем D3DMAXNUMPRIMITIVES примитивов метод завершается неудачно, выводит сообщение об ошибке в журнал ошибок и возвращает приложению значение ошибки.</span><span class="sxs-lookup"><span data-stu-id="b4eea-141">In the debug version of Direct3D, if you pass more than D3DMAXNUMPRIMITIVES primitives, the method fails gracefully, printing an error message to the error log, and returning an error value to your application.</span></span> <span data-ttu-id="b4eea-142">И наоборот, если приложение выполняет ту же ошибку при выполнении в розничной версии среды выполнения, поведение не определено.</span><span class="sxs-lookup"><span data-stu-id="b4eea-142">Conversely, if your application makes the same error when it is running with the retail version of the run time, behavior is undefined.</span></span> <span data-ttu-id="b4eea-143">Из соображений производительности метод не проверяет параметры, что приводит к непредсказуемому и полностью определенному поведению в ситуации, когда они недопустимы.</span><span class="sxs-lookup"><span data-stu-id="b4eea-143">For performance reasons, the method does not validate the parameters, resulting in unpredictable and completely situational behavior when they are not valid.</span></span> <span data-ttu-id="b4eea-144">В некоторых случаях вызов может работать, и в других случаях это может привести к сбою памяти в Direct3D.</span><span class="sxs-lookup"><span data-stu-id="b4eea-144">In some cases the call might work, and in other cases it might cause a memory fault in Direct3D.</span></span> <span data-ttu-id="b4eea-145">Если недопустимый вызов постоянно работает с определенной конфигурацией оборудования и версией DirectX, нет никакой гарантии, что она будет продолжать работать на другом оборудовании или в более поздних версиях DirectX.</span><span class="sxs-lookup"><span data-stu-id="b4eea-145">If an invalid call consistently works with a particular hardware configuration and DirectX version, there is no guarantee that it will continue to function on other hardware or with later releases of DirectX.</span></span>

<span data-ttu-id="b4eea-146">Если приложение сталкивается с неправильными сбоями при работе с файлом времени выполнения Direct3D для розничной торговли, протестируйте отладочную версию и внимательно просмотрите случаи, когда приложение передает недопустимые параметры.</span><span class="sxs-lookup"><span data-stu-id="b4eea-146">If your application encounters unexplained failures when running with the retail Direct3D run-time file, test against the debug version and look closely for cases where your application passes invalid parameters.</span></span> <span data-ttu-id="b4eea-147">Используйте приложение панели управления DirectX, при необходимости переключитесь в среду выполнения отладки и установите флажок "прерывать на D3DError".</span><span class="sxs-lookup"><span data-stu-id="b4eea-147">Use the DirectX control panel applet, switch to the debug runtime if necessary, and check the "Break on D3DError" option.</span></span> <span data-ttu-id="b4eea-148">Этот параметр приведет к тому, что среда выполнения будет использовать метод Windows DebugBreak для принудительного завершения приложения при обнаружении ошибки приложения.</span><span class="sxs-lookup"><span data-stu-id="b4eea-148">This option will force the runtime to use the Windows DebugBreak method in order to force the application to stop when an application bug is detected.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b4eea-149">См. также</span><span class="sxs-lookup"><span data-stu-id="b4eea-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b4eea-150">Советы по программированию</span><span class="sxs-lookup"><span data-stu-id="b4eea-150">Programming Tips</span></span>](programming-tips.md)
</dt> </dl>

 

 
