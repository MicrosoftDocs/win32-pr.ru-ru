---
description: В этом разделе содержатся сведения о интерфейсах и классах, используемых для пера в реальном времени.
ms.assetid: fc0900b4-f08b-4a93-bbc0-d3db067d7917
title: Классы и интерфейсы RealTimeStylus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34769b2c268bcdfe2becf9e759344d972092fe28
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910751"
---
# <a name="realtimestylus-classes-and-interfaces"></a><span data-ttu-id="f8661-103">Классы и интерфейсы RealTimeStylus</span><span class="sxs-lookup"><span data-stu-id="f8661-103">RealTimeStylus Classes and Interfaces</span></span>

<span data-ttu-id="f8661-104">В этом разделе содержатся сведения о интерфейсах и классах, используемых для пера в реальном времени.</span><span class="sxs-lookup"><span data-stu-id="f8661-104">This section contains information about the interfaces and classes used in the real time stylus.</span></span>

> [!Note]  
> <span data-ttu-id="f8661-105">Классы и интерфейсы пера в реальном времени не соответствуют автоматизации.</span><span class="sxs-lookup"><span data-stu-id="f8661-105">The real time stylus classes and interfaces are not Automation compliant.</span></span>

 

## <a name="in-this-section"></a><span data-ttu-id="f8661-106">в этом разделе</span><span class="sxs-lookup"><span data-stu-id="f8661-106">In This Section</span></span>



| <span data-ttu-id="f8661-107">Класс</span><span class="sxs-lookup"><span data-stu-id="f8661-107">Class</span></span>                                                      | <span data-ttu-id="f8661-108">Описание</span><span class="sxs-lookup"><span data-stu-id="f8661-108">Description</span></span>                                                                                     |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f8661-109">**Класс RealTimeStylus**</span><span class="sxs-lookup"><span data-stu-id="f8661-109">**RealTimeStylus Class**</span></span>](realtimestylus-class.md)       | <span data-ttu-id="f8661-110">Реализует интерфейс [**иреалтиместилус**](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus) .</span><span class="sxs-lookup"><span data-stu-id="f8661-110">Implements the [**IRealTimeStylus**](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus) interface.</span></span><br/>                 |
| <span data-ttu-id="f8661-111">[**Класс DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f8661-111">[**DynamicRenderer Class**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85))</span></span>     | <span data-ttu-id="f8661-112">Реализует интерфейс [**интерфейса идинамикрендерер**](/windows/desktop/api/RTSCom/nn-rtscom-idynamicrenderer) .</span><span class="sxs-lookup"><span data-stu-id="f8661-112">Implements the [**IDynamicRenderer Interface**](/windows/desktop/api/RTSCom/nn-rtscom-idynamicrenderer) interface.</span></span><br/>     |
| [<span data-ttu-id="f8661-113">**Класс GestureRecognizer**</span><span class="sxs-lookup"><span data-stu-id="f8661-113">**GestureRecognizer Class**</span></span>](gesturerecognizer-class.md) | <span data-ttu-id="f8661-114">Реализует интерфейс [**интерфейса ижестуререкогнизер**](/windows/desktop/api/RTSCom/nn-rtscom-igesturerecognizer) .</span><span class="sxs-lookup"><span data-stu-id="f8661-114">Implements the [**IGestureRecognizer Interface**](/windows/desktop/api/RTSCom/nn-rtscom-igesturerecognizer) interface.</span></span><br/> |
| [<span data-ttu-id="f8661-115">**Класс Строкебуилдер**</span><span class="sxs-lookup"><span data-stu-id="f8661-115">**StrokeBuilder Class**</span></span>](strokebuilder-class.md)         | <span data-ttu-id="f8661-116">Реализует интерфейс [**интерфейса истрокебуилдер**](/windows/desktop/api/RTSCom/nn-rtscom-istrokebuilder) .</span><span class="sxs-lookup"><span data-stu-id="f8661-116">Implements the [**IStrokeBuilder Interface**](/windows/desktop/api/RTSCom/nn-rtscom-istrokebuilder) interface.</span></span><br/>         |



 

## <a name="interfaces"></a><span data-ttu-id="f8661-117">Интерфейсы</span><span class="sxs-lookup"><span data-stu-id="f8661-117">Interfaces</span></span>



| <span data-ttu-id="f8661-118">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="f8661-118">Interface</span></span>                                                                          | <span data-ttu-id="f8661-119">Описание</span><span class="sxs-lookup"><span data-stu-id="f8661-119">Description</span></span>                                                                                                                                                                                 |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f8661-120">**Интерфейс Идинамикрендерер**</span><span class="sxs-lookup"><span data-stu-id="f8661-120">**IDynamicRenderer Interface**</span></span>](/windows/desktop/api/RTSCom/nn-rtscom-idynamicrenderer)                             | <span data-ttu-id="f8661-121">Предоставляет методы, позволяющие управлять отображением данных пера в режиме реального времени по мере обработки данных объектом [**класса RealTimeStylus**](realtimestylus-class.md) .</span><span class="sxs-lookup"><span data-stu-id="f8661-121">Exposes methods enabling you to control the display of stylus data in real time as the data is being handled by the [**RealTimeStylus Class**](realtimestylus-class.md) object.</span></span><br/> |
| [<span data-ttu-id="f8661-122">**Интерфейс Ижестуререкогнизер**</span><span class="sxs-lookup"><span data-stu-id="f8661-122">**IGestureRecognizer Interface**</span></span>](/windows/desktop/api/RTSCom/nn-rtscom-igesturerecognizer)                         | <span data-ttu-id="f8661-123">Предоставляет методы, позволяющие реагировать на события, распознающие жесты пера и позволяющие добавлять данные во входную очередь.</span><span class="sxs-lookup"><span data-stu-id="f8661-123">Exposes methods enabling you to react to events by recognizing stylus gestures and enabling you to add data to the input queue.</span></span><br/>                                                  |
| [<span data-ttu-id="f8661-124">**иреалтиместилус**</span><span class="sxs-lookup"><span data-stu-id="f8661-124">**IRealTimeStylus**</span></span>](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus)                                         | <span data-ttu-id="f8661-125">Обрабатывает данные пакета пера с дигитайзера в режиме реального времени.</span><span class="sxs-lookup"><span data-stu-id="f8661-125">Handles the stylus packet data from a digitizer in real time.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="f8661-126">**IRealTimeStylus2**</span><span class="sxs-lookup"><span data-stu-id="f8661-126">**IRealTimeStylus2**</span></span>](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus2)                                       | <span data-ttu-id="f8661-127">Расширяет интерфейс Иреалтиместилус.</span><span class="sxs-lookup"><span data-stu-id="f8661-127">Extends the IRealTimeStylus interface.</span></span><br/>                                                                                                                                           |
| [<span data-ttu-id="f8661-128">**IRealTimeStylus3**</span><span class="sxs-lookup"><span data-stu-id="f8661-128">**IRealTimeStylus3**</span></span>](/windows/desktop/api/rtscom/nn-rtscom-irealtimestylus3)                                       | <span data-ttu-id="f8661-129">Расширяет интерфейс Иреалтиместилус.</span><span class="sxs-lookup"><span data-stu-id="f8661-129">Extends the IRealTimeStylus interface.</span></span><br/>                                                                                                                                           |
| [<span data-ttu-id="f8661-130">**Интерфейс Иреалтиместилуссинчронизатион**</span><span class="sxs-lookup"><span data-stu-id="f8661-130">**IRealTimeStylusSynchronization Interface**</span></span>](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylussynchronization) | <span data-ttu-id="f8661-131">Синхронизирует доступ к объекту [**класса RealTimeStylus**](realtimestylus-class.md) .</span><span class="sxs-lookup"><span data-stu-id="f8661-131">Synchronizes access to the [**RealTimeStylus Class**](realtimestylus-class.md) object.</span></span><br/>                                                                                          |
| [<span data-ttu-id="f8661-132">**Интерфейс Истрокебуилдер**</span><span class="sxs-lookup"><span data-stu-id="f8661-132">**IStrokeBuilder Interface**</span></span>](/windows/desktop/api/RTSCom/nn-rtscom-istrokebuilder)                                 | <span data-ttu-id="f8661-133">Предоставляет методы, позволяющие программно создавать штрихи.</span><span class="sxs-lookup"><span data-stu-id="f8661-133">Exposes methods that enable you to programmatically create strokes.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="f8661-134">**Интерфейс Истилусплугин**</span><span class="sxs-lookup"><span data-stu-id="f8661-134">**IStylusPlugin Interface**</span></span>](/windows/desktop/api/RTSCom/nn-rtscom-istylusplugin)                                   | <span data-ttu-id="f8661-135">Предоставляет методы, позволяющие получать уведомления о событиях и выполнять пользовательскую обработку на основе этих событий.</span><span class="sxs-lookup"><span data-stu-id="f8661-135">Exposes methods enabling you to receive notifications of events and to perform custom processing based on those events.</span></span><br/>                                                          |
| [<span data-ttu-id="f8661-136">**истилусасинкплугин**</span><span class="sxs-lookup"><span data-stu-id="f8661-136">**IStylusAsyncPlugin**</span></span>](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin)                                   | <span data-ttu-id="f8661-137">Представляет асинхронный подключаемый модуль, который можно добавить в коллекцию асинхронных подключаемых модулей [**класса RealTimeStylus**](realtimestylus-class.md) .</span><span class="sxs-lookup"><span data-stu-id="f8661-137">Represents an asynchronous plug-in that can be added to the [**RealTimeStylus Class**](realtimestylus-class.md) asynchronous plug-in collection.</span></span><br/>                                |
| [<span data-ttu-id="f8661-138">**истилуссинкплугин**</span><span class="sxs-lookup"><span data-stu-id="f8661-138">**IStylusSyncPlugin**</span></span>](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin)                                     | <span data-ttu-id="f8661-139">Представляет синхронный подключаемый модуль, который можно добавить в коллекцию синхронных подключаемых модулей [**класса RealTimeStylus**](realtimestylus-class.md) .</span><span class="sxs-lookup"><span data-stu-id="f8661-139">Represents a synchronous plug-in that can be added to the [**RealTimeStylus Class**](realtimestylus-class.md) synchronous plug-in collection.</span></span><br/>                                   |



 

## <a name="return-values"></a><span data-ttu-id="f8661-140">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="f8661-140">Return Values</span></span>

<span data-ttu-id="f8661-141">Методы в библиотеке COM возвращают значения **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="f8661-141">Methods in the COM Library return values of **HRESULT**.</span></span> <span data-ttu-id="f8661-142">Если не указано иное, в следующей таблице описаны значения **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f8661-142">Unless otherwise noted, the meanings of the **HRESULT** values are described in the following table.</span></span>



| <span data-ttu-id="f8661-143">Значение HRESULT</span><span class="sxs-lookup"><span data-stu-id="f8661-143">HRESULT value</span></span>                                   | <span data-ttu-id="f8661-144">Описание</span><span class="sxs-lookup"><span data-stu-id="f8661-144">Description</span></span>                                                                              |
|-------------------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8661-145">\_ОК</span><span class="sxs-lookup"><span data-stu-id="f8661-145">S\_OK</span></span><br/>                                | <span data-ttu-id="f8661-146">Успешно.</span><span class="sxs-lookup"><span data-stu-id="f8661-146">Success.</span></span><br/>                                                                      |
| <span data-ttu-id="f8661-147">\_указатель E</span><span class="sxs-lookup"><span data-stu-id="f8661-147">E\_POINTER</span></span><br/>                           | <span data-ttu-id="f8661-148">По крайней мере один указатель (для входного или выходного параметра) является недопустимым.</span><span class="sxs-lookup"><span data-stu-id="f8661-148">At least one pointer (for either an input or an output parameter) is invalid.</span></span><br/> |
| <span data-ttu-id="f8661-149">E \_ INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="f8661-149">E\_INVALIDARG</span></span><br/>                        | <span data-ttu-id="f8661-150">Член попытался передать недопустимый аргумент.</span><span class="sxs-lookup"><span data-stu-id="f8661-150">Member attempted to pass in an invalid argument.</span></span><br/>                              |
| <span data-ttu-id="f8661-151">\_исключение рукописного ввода \_</span><span class="sxs-lookup"><span data-stu-id="f8661-151">E\_INK\_EXCEPTION</span></span><br/>                    | <span data-ttu-id="f8661-152">Возникло исключение.</span><span class="sxs-lookup"><span data-stu-id="f8661-152">Exception occurred.</span></span><br/>                                                           |
| <span data-ttu-id="f8661-153">E \_ OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="f8661-153">E\_OUTOFMEMORY</span></span><br/>                       | <span data-ttu-id="f8661-154">Системе не удается выделить память для завершения операции.</span><span class="sxs-lookup"><span data-stu-id="f8661-154">System cannot allocate memory to complete the operation.</span></span><br/>                      |
| <span data-ttu-id="f8661-155">\_Ошибка E</span><span class="sxs-lookup"><span data-stu-id="f8661-155">E\_FAIL</span></span><br/>                              | <span data-ttu-id="f8661-156">Произошла неопределенная ошибка.</span><span class="sxs-lookup"><span data-stu-id="f8661-156">Unspecified failure occurred.</span></span><br/>                                                 |
| <span data-ttu-id="f8661-157">E \_ INVALIDOPERATION</span><span class="sxs-lookup"><span data-stu-id="f8661-157">E\_INVALIDOPERATION</span></span><br/>                  | <span data-ttu-id="f8661-158">Член попытался использовать недопустимую операцию.</span><span class="sxs-lookup"><span data-stu-id="f8661-158">Member attempted to use an invalid operation.</span></span><br/>                                 |
| <span data-ttu-id="f8661-159">\_ \_ Недопустимый \_ режим TPC E</span><span class="sxs-lookup"><span data-stu-id="f8661-159">TPC\_E\_INVALID\_MODE</span></span><br/>                | <span data-ttu-id="f8661-160">Член попытался использовать недопустимый режим.</span><span class="sxs-lookup"><span data-stu-id="f8661-160">Member attempted to use an invalid mode.</span></span><br/>                                      |
| <span data-ttu-id="f8661-161">TPC \_ E \_ Недопустимая \_ Конфигурация</span><span class="sxs-lookup"><span data-stu-id="f8661-161">TPC\_E\_INVALID\_CONFIGURATION</span></span><br/>       | <span data-ttu-id="f8661-162">Член попытался использовать недопустимую конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="f8661-162">Member attempted to use an invalid configuration.</span></span><br/>                             |
| <span data-ttu-id="f8661-163">\_ \_ Описание недействительного пакета TPC E \_ \_</span><span class="sxs-lookup"><span data-stu-id="f8661-163">TPC\_E\_INVALID\_PACKET\_DESCRIPTION</span></span><br/> | <span data-ttu-id="f8661-164">Член попытался использовать недопустимое описание пакета.</span><span class="sxs-lookup"><span data-stu-id="f8661-164">Member attempted to use an invalid packet description.</span></span><br/>                        |



 

## <a name="related-topics"></a><span data-ttu-id="f8661-165">См. также</span><span class="sxs-lookup"><span data-stu-id="f8661-165">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f8661-166">Ссылка RealTimeStylus</span><span class="sxs-lookup"><span data-stu-id="f8661-166">RealTimeStylus Reference</span></span>](realtimestylus-reference.md)
</dt> </dl>

 

 
