---
description: В этом разделе описывается, как реализовать поиск в фильтре источника Microsoft DirectShow. В качестве отправной точки в нем используется пример фильтра шарика и описывается дополнительный код, необходимый для поддержки поиска в этом фильтре.
ms.assetid: a2b4be09-2fd6-4aac-8ad6-c3d62377c1f2
title: Поддержка поиска в фильтре источника
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42ac4bbb63410adf9cb4e8d69064679143b84d67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913139"
---
# <a name="supporting-seeking-in-a-source-filter"></a><span data-ttu-id="00ed0-104">Поддержка поиска в фильтре источника</span><span class="sxs-lookup"><span data-stu-id="00ed0-104">Supporting Seeking in a Source Filter</span></span>

<span data-ttu-id="00ed0-105">В этом разделе описывается, как реализовать поиск в фильтре источника Microsoft DirectShow.</span><span class="sxs-lookup"><span data-stu-id="00ed0-105">This topic describes how to implement seeking in a Microsoft DirectShow source filter.</span></span> <span data-ttu-id="00ed0-106">В качестве отправной точки в нем используется пример [фильтра шарика](ball-filter-sample.md) и описывается дополнительный код, необходимый для поддержки поиска в этом фильтре.</span><span class="sxs-lookup"><span data-stu-id="00ed0-106">It uses the [Ball Filter](ball-filter-sample.md) sample as the starting point and describes the additional code needed to support seeking in this filter.</span></span>

<span data-ttu-id="00ed0-107">Образец " [Фильтр шарика](ball-filter-sample.md) " — это фильтр источника, который создает анимированный шарик с отскоками.</span><span class="sxs-lookup"><span data-stu-id="00ed0-107">The [Ball Filter](ball-filter-sample.md) sample is a source filter that creates an animated bouncing ball.</span></span> <span data-ttu-id="00ed0-108">В этой статье описывается, как добавить функции поиска в этот фильтр.</span><span class="sxs-lookup"><span data-stu-id="00ed0-108">This article describes how to add seeking functionality to this filter.</span></span> <span data-ttu-id="00ed0-109">После добавления этой функции можно отобразить фильтр в Графедит и управлять шариком, перетаскивая ползунок Графедит.</span><span class="sxs-lookup"><span data-stu-id="00ed0-109">Once you have added this functionality, you can render the filter in GraphEdit and control the ball by dragging the GraphEdit slider.</span></span>

<span data-ttu-id="00ed0-110">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="00ed0-110">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="00ed0-111">Общие сведения о поиске в DirectShow</span><span class="sxs-lookup"><span data-stu-id="00ed0-111">Overview of Seeking in DirectShow</span></span>](#overview-of-seeking-in-directshow)
-   [<span data-ttu-id="00ed0-112">Краткий обзор фильтра шарика</span><span class="sxs-lookup"><span data-stu-id="00ed0-112">Quick Overview of the Ball Filter</span></span>](#quick-overview-of-the-ball-filter)
-   [<span data-ttu-id="00ed0-113">Изменение фильтра шарика для поиска</span><span class="sxs-lookup"><span data-stu-id="00ed0-113">Modifying the Ball Filter for Seeking</span></span>](#modifying-the-ball-filter-for-seeking)
-   [<span data-ttu-id="00ed0-114">Ограничения класса Ксаурцесикинг</span><span class="sxs-lookup"><span data-stu-id="00ed0-114">Limitations of the CSourceSeeking Class</span></span>](#limitations-of-the-csourceseeking-class)

## <a name="overview-of-seeking-in-directshow"></a><span data-ttu-id="00ed0-115">Общие сведения о поиске в DirectShow</span><span class="sxs-lookup"><span data-stu-id="00ed0-115">Overview of Seeking in DirectShow</span></span>

<span data-ttu-id="00ed0-116">Приложение ищет граф фильтра, вызывая метод [**имедиасикинг**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) в диспетчере графов фильтров.</span><span class="sxs-lookup"><span data-stu-id="00ed0-116">An application seeks the filter graph by calling an [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) method on the Filter Graph Manager.</span></span> <span data-ttu-id="00ed0-117">Затем Диспетчер графа фильтров распространяет вызов на каждый визуализатор в графе.</span><span class="sxs-lookup"><span data-stu-id="00ed0-117">The Filter Graph Manager then distributes the call to every renderer in the graph.</span></span> <span data-ttu-id="00ed0-118">Каждый модуль подготовки отчетов отправляет вышестоящее обращение через выходной ПИН-код следующего вышестоящего фильтра.</span><span class="sxs-lookup"><span data-stu-id="00ed0-118">Each renderer sends the call upstream, through the output pin of the next upstream filter.</span></span> <span data-ttu-id="00ed0-119">Вызов перемещается в потоке до тех пор, пока не достигнет фильтра, который может выполнить команду Seek (обычно это фильтр источника или фильтр анализатора).</span><span class="sxs-lookup"><span data-stu-id="00ed0-119">The call travels upstream until it reaches a filter that can execute the seek command, typically a source filter or a parser filter.</span></span> <span data-ttu-id="00ed0-120">Как правило, фильтр, исходящий отметки времени, также обрабатывает Поиск.</span><span class="sxs-lookup"><span data-stu-id="00ed0-120">In general, the filter that originates the time stamps also handles seeking.</span></span>

<span data-ttu-id="00ed0-121">Фильтр реагирует на команду Seek следующим образом:</span><span class="sxs-lookup"><span data-stu-id="00ed0-121">A filter responds to a seek command as follows:</span></span>

1.  <span data-ttu-id="00ed0-122">Фильтр очищает диаграмму.</span><span class="sxs-lookup"><span data-stu-id="00ed0-122">The filter flushes the graph.</span></span> <span data-ttu-id="00ed0-123">При этом удаляются все устаревшие данные из Graph, что повышает скорость реагирования.</span><span class="sxs-lookup"><span data-stu-id="00ed0-123">This clears any stale data from graph, which improves responsiveness.</span></span> <span data-ttu-id="00ed0-124">В противном случае могут быть доставлены образцы, которые были помещены в буфер до команды Seek.</span><span class="sxs-lookup"><span data-stu-id="00ed0-124">Otherwise, samples that were buffered prior to the seek command might get delivered.</span></span>
2.  <span data-ttu-id="00ed0-125">Фильтр вызывает [**Ипин:: невсегмент**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) для информирования нисходящих фильтров о новом времени окончания, времени начала и скорости воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="00ed0-125">The filter calls [**IPin::NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) to inform downstream filters of the new stop time, start time, and playback rate.</span></span>
3.  <span data-ttu-id="00ed0-126">Затем фильтр устанавливает флаг небесперебойности в первом примере после команды Seek.</span><span class="sxs-lookup"><span data-stu-id="00ed0-126">The filter then sets the discontinuity flag on the first sample after the seek command.</span></span>

<span data-ttu-id="00ed0-127">Метки времени начинаются с нуля после любой команды поиска (включая изменения скорости).</span><span class="sxs-lookup"><span data-stu-id="00ed0-127">Time stamps start from zero after any seek command (including rate changes).</span></span>

## <a name="quick-overview-of-the-ball-filter"></a><span data-ttu-id="00ed0-128">Краткий обзор фильтра шарика</span><span class="sxs-lookup"><span data-stu-id="00ed0-128">Quick Overview of the Ball Filter</span></span>

<span data-ttu-id="00ed0-129">Фильтр шарика — это источник push-уведомлений. Это означает, что он использует рабочий поток для предоставления образцов в нисходящем направлении, в отличие от источника запроса, который, в своюмся состоянии, ожидает, пока подчиненный фильтр не запросит образцы.</span><span class="sxs-lookup"><span data-stu-id="00ed0-129">The Ball filter is a push source, which means that it uses a worker thread to deliver samples downstream, as opposed to a pull source, which passively waits for a downstream filter to request samples.</span></span> <span data-ttu-id="00ed0-130">Фильтр шарика строится на основе класса [**ксаурце**](csource.md) , а его выходной ПИН-код строится на основе класса [**ксаурцестреам**](csourcestream.md) .</span><span class="sxs-lookup"><span data-stu-id="00ed0-130">The Ball filter is built from the [**CSource**](csource.md) class, and its output pin is built from the [**CSourceStream**](csourcestream.md) class.</span></span> <span data-ttu-id="00ed0-131">Класс **ксаурцестреам** создает рабочий поток, который управляет потоком данных.</span><span class="sxs-lookup"><span data-stu-id="00ed0-131">The **CSourceStream** class creates the worker thread that drives the flow of data.</span></span> <span data-ttu-id="00ed0-132">Этот поток входит в цикл, который получает выборки из распределителя, заполняет их данными и доставляет их нисходящим.</span><span class="sxs-lookup"><span data-stu-id="00ed0-132">This thread enters a loop that gets samples from the allocator, fills them with data, and delivers them downstream.</span></span>

<span data-ttu-id="00ed0-133">Большая часть действия в [**ксаурцестреам**](csourcestream.md) происходит в методе [**Ксаурцестреам:: филлбуффер**](csourcestream-fillbuffer.md) , который реализуется производным классом.</span><span class="sxs-lookup"><span data-stu-id="00ed0-133">Most of the action in [**CSourceStream**](csourcestream.md) happens in the [**CSourceStream::FillBuffer**](csourcestream-fillbuffer.md) method, which the derived class implements.</span></span> <span data-ttu-id="00ed0-134">Аргументом для этого метода является указатель на образец для доставки.</span><span class="sxs-lookup"><span data-stu-id="00ed0-134">The argument to this method is a pointer to the sample to be delivered.</span></span> <span data-ttu-id="00ed0-135">Реализация **филлбуффер** в фильтре шарика получает адрес буфера выборки и рисует непосредственно в буфере, устанавливая отдельные значения пикселей.</span><span class="sxs-lookup"><span data-stu-id="00ed0-135">The Ball filter's implementation of **FillBuffer** retrieves the address of the sample buffer and draws directly to the buffer by setting individual pixel values.</span></span> <span data-ttu-id="00ed0-136">(Рисование выполняется вспомогательным классом Кбалл, поэтому вы можете игнорировать сведения о глубине битов, палитрах и т. д.)</span><span class="sxs-lookup"><span data-stu-id="00ed0-136">(The drawing is done by a helper class, CBall, so you can ignore the details regarding bit depths, palettes, and so forth.)</span></span>

## <a name="modifying-the-ball-filter-for-seeking"></a><span data-ttu-id="00ed0-137">Изменение фильтра шарика для поиска</span><span class="sxs-lookup"><span data-stu-id="00ed0-137">Modifying the Ball Filter for Seeking</span></span>

<span data-ttu-id="00ed0-138">Чтобы сделать фильтр шарика пригодным для поиска, используйте класс [**ксаурцесикинг**](csourceseeking.md) , предназначенный для реализации поиска в фильтрах с одним выходным закреплением.</span><span class="sxs-lookup"><span data-stu-id="00ed0-138">To make the Ball filter seekable, use the [**CSourceSeeking**](csourceseeking.md) class, which is designed for implementing seeking in filters with one output pin.</span></span> <span data-ttu-id="00ed0-139">Добавьте класс **ксаурцесикинг** в список наследования для класса кбаллстреам:</span><span class="sxs-lookup"><span data-stu-id="00ed0-139">Add the **CSourceSeeking** class to the inheritance list for the CBallStream class:</span></span>


```C++
class CBallStream :  // Defines the output pin.
    public CSourceStream, public CSourceSeeking
```



<span data-ttu-id="00ed0-140">Кроме того, необходимо добавить инициализатор для [**ксаурцесикинг**](csourceseeking.md) в конструктор кбаллстреам:</span><span class="sxs-lookup"><span data-stu-id="00ed0-140">Also, you will need to add an initializer for [**CSourceSeeking**](csourceseeking.md) to the CBallStream constructor:</span></span>


```C++
    CSourceSeeking(NAME("SeekBall"), (IPin*)this, phr, &m_cSharedState),
```



<span data-ttu-id="00ed0-141">Эта инструкция вызывает базовый конструктор для [**ксаурцесикинг**](csourceseeking.md).</span><span class="sxs-lookup"><span data-stu-id="00ed0-141">This statement calls the base constructor for [**CSourceSeeking**](csourceseeking.md).</span></span> <span data-ttu-id="00ed0-142">Параметры — это имя, указатель на ПИН-код владельца, значение **HRESULT** и адрес объекта критической секции.</span><span class="sxs-lookup"><span data-stu-id="00ed0-142">The parameters are a name, a pointer to the owning pin, an **HRESULT** value, and the address of a critical section object.</span></span> <span data-ttu-id="00ed0-143">Имя используется только для отладки, а макрос [**Name**](name.md) компилируется в пустую строку в розничных сборках.</span><span class="sxs-lookup"><span data-stu-id="00ed0-143">The name is used only for debugging, and the [**NAME**](name.md) macro compiles to an empty string in retail builds.</span></span> <span data-ttu-id="00ed0-144">ПИН-код непосредственно наследует **ксаурцесикинг**, поэтому второй параметр является указателем на себя, приведенным к указателю [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin) .</span><span class="sxs-lookup"><span data-stu-id="00ed0-144">The pin directly inherits **CSourceSeeking**, so the second parameter is a pointer to itself, cast to an [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) pointer.</span></span> <span data-ttu-id="00ed0-145">Значение **HRESULT** игнорируется в текущей версии базовых классов. он остается для совместимости с предыдущими версиями.</span><span class="sxs-lookup"><span data-stu-id="00ed0-145">The **HRESULT** value is ignored in the current version of the base classes; it remains for compatibility with previous versions.</span></span> <span data-ttu-id="00ed0-146">Критическая секция защищает общие данные, такие как текущее время запуска, время окончания и скорость воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="00ed0-146">The critical section protects shared data, such as the current start time, stop time, and playback rate.</span></span>

<span data-ttu-id="00ed0-147">Добавьте следующую инструкцию в конструктор [**ксаурцесикинг**](csourceseeking.md) :</span><span class="sxs-lookup"><span data-stu-id="00ed0-147">Add the following statement inside the [**CSourceSeeking**](csourceseeking.md) constructor:</span></span>


```C++
m_rtStop = 60 * UNITS;
```



<span data-ttu-id="00ed0-148">Переменная *\_ ртстоп m* указывает время окончания.</span><span class="sxs-lookup"><span data-stu-id="00ed0-148">The *m\_rtStop* variable specifies the stop time.</span></span> <span data-ttu-id="00ed0-149">По умолчанию используется значение \_ I64 \_ Max/2, которое составляет примерно 14 600 лет.</span><span class="sxs-lookup"><span data-stu-id="00ed0-149">By default, the value is \_I64\_MAX / 2, which is approximately 14,600 years.</span></span> <span data-ttu-id="00ed0-150">Предыдущая инструкция задает для него более консервативную 60 секунд.</span><span class="sxs-lookup"><span data-stu-id="00ed0-150">The previous statement sets it to a more conservative 60 seconds.</span></span>

<span data-ttu-id="00ed0-151">В Кбаллстреам необходимо добавить две дополнительные переменные члена:</span><span class="sxs-lookup"><span data-stu-id="00ed0-151">Two additional member variables must be added to CBallStream:</span></span>


```C++
BOOL            m_bDiscontinuity; // If true, set the discontinuity flag.
REFERENCE_TIME  m_rtBallPosition; // Position of the ball. 
```



<span data-ttu-id="00ed0-152">После каждой команды Seek фильтр должен установить флаг небесперебойности для следующей выборки путем вызова [**имедиасампле:: сетдисконтинуити**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity).</span><span class="sxs-lookup"><span data-stu-id="00ed0-152">After every seek command, the filter must set the discontinuity flag on the next sample by calling [**IMediaSample::SetDiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity).</span></span> <span data-ttu-id="00ed0-153">Переменная *m \_ бдисконтинуити* будет отследить это.</span><span class="sxs-lookup"><span data-stu-id="00ed0-153">The *m\_bDiscontinuity* variable will keep track of this.</span></span> <span data-ttu-id="00ed0-154">Переменная *\_ ртбаллпоситион m* определяет расположение шарика в кадре видео.</span><span class="sxs-lookup"><span data-stu-id="00ed0-154">The *m\_rtBallPosition* variable will specify the position of the ball within the video frame.</span></span> <span data-ttu-id="00ed0-155">Фильтр исходного шарика Вычисляет положение на основе потокового времени, но время потока сбрасывается в ноль после каждой команды Seek.</span><span class="sxs-lookup"><span data-stu-id="00ed0-155">The original Ball filter calculates the position from the stream time, but the stream time resets to zero after each seek command.</span></span> <span data-ttu-id="00ed0-156">В потоке, доступном для поиска, абсолютное положение не зависит от времени потока.</span><span class="sxs-lookup"><span data-stu-id="00ed0-156">In a seekable stream, the absolute position is independent of the stream time.</span></span>

### <a name="queryinterface"></a><span data-ttu-id="00ed0-157">QueryInterface</span><span class="sxs-lookup"><span data-stu-id="00ed0-157">QueryInterface</span></span>

<span data-ttu-id="00ed0-158">Класс [**ксаурцесикинг**](csourceseeking.md) реализует интерфейс [**имедиасикинг**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) .</span><span class="sxs-lookup"><span data-stu-id="00ed0-158">The [**CSourceSeeking**](csourceseeking.md) class implements the [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) interface.</span></span> <span data-ttu-id="00ed0-159">Чтобы предоставить этот интерфейс клиентам, переопределите метод [**нонделегатингкуеринтерфаце**](cunknown-nondelegatingqueryinterface.md) :</span><span class="sxs-lookup"><span data-stu-id="00ed0-159">To expose this interface to clients, override the [**NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) method:</span></span>


```C++
STDMETHODIMP CBallStream::NonDelegatingQueryInterface
    (REFIID riid, void **ppv)
{
    if( riid == IID_IMediaSeeking ) 
    {
        return CSourceSeeking::NonDelegatingQueryInterface( riid, ppv );
    }
    return CSourceStream::NonDelegatingQueryInterface(riid, ppv);
}
```



<span data-ttu-id="00ed0-160">Метод называется «неделегированным» из-за способа, которым базовые классы DirectShow поддерживают агрегирование объектной модели (COM).</span><span class="sxs-lookup"><span data-stu-id="00ed0-160">The method is called "NonDelegating" because of the way the DirectShow base classes support Component Object Model (COM) aggregation.</span></span> <span data-ttu-id="00ed0-161">Дополнительные сведения см. в разделе "реализация IUnknown" в пакете SDK для DirectShow.</span><span class="sxs-lookup"><span data-stu-id="00ed0-161">For more information, see the "How to Implement IUnknown" topic in the DirectShow SDK.</span></span>

### <a name="seeking-methods"></a><span data-ttu-id="00ed0-162">Поиск методов</span><span class="sxs-lookup"><span data-stu-id="00ed0-162">Seeking Methods</span></span>

<span data-ttu-id="00ed0-163">Класс [**ксаурцесикинг**](csourceseeking.md) поддерживает несколько переменных членов, относящихся к поиску.</span><span class="sxs-lookup"><span data-stu-id="00ed0-163">The [**CSourceSeeking**](csourceseeking.md) class maintains several member variables relating to seeking.</span></span>



| <span data-ttu-id="00ed0-164">Переменная</span><span class="sxs-lookup"><span data-stu-id="00ed0-164">Variable</span></span>          | <span data-ttu-id="00ed0-165">Описание</span><span class="sxs-lookup"><span data-stu-id="00ed0-165">Description</span></span>   | <span data-ttu-id="00ed0-166">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="00ed0-166">Default Value</span></span>  |
|-------------------|---------------|----------------|
| <span data-ttu-id="00ed0-167">*m \_ ртстарт*</span><span class="sxs-lookup"><span data-stu-id="00ed0-167">*m\_rtStart*</span></span>      | <span data-ttu-id="00ed0-168">Время начала</span><span class="sxs-lookup"><span data-stu-id="00ed0-168">Start time</span></span>    | <span data-ttu-id="00ed0-169">Ноль</span><span class="sxs-lookup"><span data-stu-id="00ed0-169">Zero</span></span>           |
| <span data-ttu-id="00ed0-170">*m \_ ртстоп*</span><span class="sxs-lookup"><span data-stu-id="00ed0-170">*m\_rtStop*</span></span>       | <span data-ttu-id="00ed0-171">Время остановки</span><span class="sxs-lookup"><span data-stu-id="00ed0-171">Stop time</span></span>     | <span data-ttu-id="00ed0-172">\_I64 \_ Max/2</span><span class="sxs-lookup"><span data-stu-id="00ed0-172">\_I64\_MAX / 2</span></span> |
| <span data-ttu-id="00ed0-173">*m \_ дратесикинг*</span><span class="sxs-lookup"><span data-stu-id="00ed0-173">*m\_dRateSeeking*</span></span> | <span data-ttu-id="00ed0-174">Скорость воспроизведения</span><span class="sxs-lookup"><span data-stu-id="00ed0-174">Playback rate</span></span> | <span data-ttu-id="00ed0-175">1.0</span><span class="sxs-lookup"><span data-stu-id="00ed0-175">1.0</span></span>            |



 

<span data-ttu-id="00ed0-176">Реализация [**Ксаурцесикинг**](csourceseeking.md) [**Имедиасикинг:: сетпоситионс**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) обновляет время начала и окончания, а затем вызывает два чисто виртуальных метода в производном классе, [**Ксаурцесикинг:: Чанжестарт**](csourceseeking-changestart.md) и [**ксаурцесикинг:: ChangeStop**](csourceseeking-changestop.md).</span><span class="sxs-lookup"><span data-stu-id="00ed0-176">The [**CSourceSeeking**](csourceseeking.md) implementation of [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) updates the start and stop times, and then calls two pure virtual methods on the derived class, [**CSourceSeeking::ChangeStart**](csourceseeking-changestart.md) and [**CSourceSeeking::ChangeStop**](csourceseeking-changestop.md).</span></span> <span data-ttu-id="00ed0-177">Реализация [**имедиасикинг:: сетрате**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate) подобна: она обновляет скорость воспроизведения, а затем вызывает чистый виртуальный метод [**Ксаурцесикинг:: чанжерате**](csourceseeking-changerate.md).</span><span class="sxs-lookup"><span data-stu-id="00ed0-177">The implementation of [**IMediaSeeking::SetRate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate) is similar: It updates the playback rate and then calls the pure virtual method [**CSourceSeeking::ChangeRate**](csourceseeking-changerate.md).</span></span> <span data-ttu-id="00ed0-178">В каждом из этих виртуальных методов ПИН-код должен выполнять следующие действия:</span><span class="sxs-lookup"><span data-stu-id="00ed0-178">In each of these virtual methods, the pin must do the following:</span></span>

1.  <span data-ttu-id="00ed0-179">Чтобы начать очистку данных, вызовите [**Ипин:: бегинфлуш**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) .</span><span class="sxs-lookup"><span data-stu-id="00ed0-179">Call [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) to start flushing data.</span></span>
2.  <span data-ttu-id="00ed0-180">Остановите поток потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="00ed0-180">Halt the streaming thread.</span></span>
3.  <span data-ttu-id="00ed0-181">Вызовите [**Ипин:: ендфлуш**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush).</span><span class="sxs-lookup"><span data-stu-id="00ed0-181">Call [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush).</span></span>
4.  <span data-ttu-id="00ed0-182">Перезапустите поток потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="00ed0-182">Restart the streaming thread.</span></span>
5.  <span data-ttu-id="00ed0-183">Вызовите [**Ипин:: невсегмент**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment).</span><span class="sxs-lookup"><span data-stu-id="00ed0-183">Call [**IPin::NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment).</span></span>
6.  <span data-ttu-id="00ed0-184">Установите флаг небесперебойности в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="00ed0-184">Set the discontinuity flag on the next sample.</span></span>

<span data-ttu-id="00ed0-185">Порядок этих шагов является важнейшим, так как поток потоковой передачи может блокироваться, пока он ожидает доставки примера или получения нового примера.</span><span class="sxs-lookup"><span data-stu-id="00ed0-185">The order of these steps is crucial, because the streaming thread can block while it waits to deliver a sample or get a new sample.</span></span> <span data-ttu-id="00ed0-186">Метод [**бегинфлуш**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) гарантирует, что поток потоковой передачи не блокируется и, следовательно, не будет заблокирован на шаге 2.</span><span class="sxs-lookup"><span data-stu-id="00ed0-186">The [**BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) method ensures that the streaming thread is not blocked and therefore will not deadlock in step 2.</span></span> <span data-ttu-id="00ed0-187">Вызов [**ендфлуш**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) информирует нисходящие фильтры о необходимости получения новых образцов, поэтому они не отклоняют их при повторном запуске потока на шаге 4.</span><span class="sxs-lookup"><span data-stu-id="00ed0-187">The [**EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) call informs the downstream filters to expect new samples, so they do not reject them when the thread starts again in step 4.</span></span>

<span data-ttu-id="00ed0-188">Следующий частный метод выполняет шаги 1 – 4:</span><span class="sxs-lookup"><span data-stu-id="00ed0-188">The following private method performs steps 1 through 4:</span></span>


```C++
void CBallStream::UpdateFromSeek()
{
    if (ThreadExists()) 
    {
        DeliverBeginFlush();
        // Shut down the thread and stop pushing data.
        Stop();
        DeliverEndFlush();
        // Restart the thread and start pushing data again.
        Pause();
    }
}
```



<span data-ttu-id="00ed0-189">Когда поток потоковой передачи снова запускается, он вызывает метод [**ксаурцестреам:: онсреадстартплай**](csourcestream-onthreadstartplay.md) .</span><span class="sxs-lookup"><span data-stu-id="00ed0-189">When the streaming thread starts again, it calls the [**CSourceStream::OnThreadStartPlay**](csourcestream-onthreadstartplay.md) method.</span></span> <span data-ttu-id="00ed0-190">Переопределите этот метод для выполнения шагов 5 и 6:</span><span class="sxs-lookup"><span data-stu-id="00ed0-190">Override this method to perform steps 5 and 6:</span></span>


```C++
HRESULT CBallStream::OnThreadStartPlay()
{
    m_bDiscontinuity = TRUE;
    return DeliverNewSegment(m_rtStart, m_rtStop, m_dRateSeeking);
}
```



<span data-ttu-id="00ed0-191">В методе [**чанжестарт**](csourceseeking-changestart.md) задайте в качестве времени потока нулевое значение и расположение шарика на новое время начала.</span><span class="sxs-lookup"><span data-stu-id="00ed0-191">In the [**ChangeStart**](csourceseeking-changestart.md) method, set the stream time to zero and the position of the ball to the new start time.</span></span> <span data-ttu-id="00ed0-192">Затем вызовите Кбаллстреам:: Упдатефромсик:</span><span class="sxs-lookup"><span data-stu-id="00ed0-192">Then call CBallStream::UpdateFromSeek:</span></span>


```C++
HRESULT CBallStream::ChangeStart( )
{
    {
        CAutoLock lock(CSourceSeeking::m_pLock);
        m_rtSampleTime = 0;
        m_rtBallPosition = m_rtStart;
    }
    UpdateFromSeek();
    return S_OK;
}
```



<span data-ttu-id="00ed0-193">В методе [**чанжестоп**](csourceseeking-changestop.md) вызовите кбаллстреам:: упдатефромсик, если новое время окончания меньше текущей позиции.</span><span class="sxs-lookup"><span data-stu-id="00ed0-193">In the [**ChangeStop**](csourceseeking-changestop.md) method, call CBallStream::UpdateFromSeek if the new stop time is less than the current position.</span></span> <span data-ttu-id="00ed0-194">В противном случае время прекращения остается в будущем, поэтому нет необходимости очищать граф.</span><span class="sxs-lookup"><span data-stu-id="00ed0-194">Otherwise, the stop time is still in the future, so there's no need to flush the graph.</span></span>


```C++
HRESULT CBallStream::ChangeStop( )
{
    {
        CAutoLock lock(CSourceSeeking::m_pLock);
        if (m_rtBallPosition < m_rtStop)
        {
            return S_OK;
        }
    }

    // We're already past the new stop time. Flush the graph.
    UpdateFromSeek();
    return S_OK;
}
```



<span data-ttu-id="00ed0-195">Для изменения ставок метод [**ксаурцесикинг:: сетрате**](csourceseeking-setrate.md) устанавливает для *m \_ дратесикинг* новую ставку (отменяя старое значение) перед вызовом [**чанжерате**](csourceseeking-changerate.md).</span><span class="sxs-lookup"><span data-stu-id="00ed0-195">For rate changes, the [**CSourceSeeking::SetRate**](csourceseeking-setrate.md) method sets *m\_dRateSeeking* to the new rate (discarding the old value) before it calls [**ChangeRate**](csourceseeking-changerate.md).</span></span> <span data-ttu-id="00ed0-196">Увы, если вызывающая сторона дала недопустимую скорость (например, меньше нуля), она слишком поздно вызываемой **чанжерате** времени.</span><span class="sxs-lookup"><span data-stu-id="00ed0-196">Unfortunately, if the caller gave an invalid rate—for example, less than zero—it's too late by the time **ChangeRate** is called.</span></span> <span data-ttu-id="00ed0-197">Одним из решений является переопределение **сетрате** и проверка допустимых ставок:</span><span class="sxs-lookup"><span data-stu-id="00ed0-197">One solution is to override **SetRate** and check for valid rates:</span></span>


```C++
HRESULT CBallStream::SetRate(double dRate)
{
    if (dRate <= 1.0)
    {
        return E_INVALIDARG;
    }
    {
        CAutoLock lock(CSourceSeeking::m_pLock);
        m_dRateSeeking = dRate;
    }
    UpdateFromSeek();
    return S_OK;
}
// Now ChangeRate won't ever be called, but it's pure virtual, so it needs
// a dummy implementation.
HRESULT CBallStream::ChangeRate() { return S_OK; }
```



### <a name="drawing-in-the-buffer"></a><span data-ttu-id="00ed0-198">Рисование в буфере</span><span class="sxs-lookup"><span data-stu-id="00ed0-198">Drawing in the Buffer</span></span>

<span data-ttu-id="00ed0-199">Ниже приведена измененная версия [**ксаурцестреам:: филлбуффер**](csourcestream-fillbuffer.md)— подпрограммы, которая рисует шарик на каждом кадре:</span><span class="sxs-lookup"><span data-stu-id="00ed0-199">Here is the modified version of [**CSourceStream::FillBuffer**](csourcestream-fillbuffer.md), the routine that draws the ball on each frame:</span></span>


```C++
HRESULT CBallStream::FillBuffer(IMediaSample *pMediaSample)
{
    BYTE *pData;
    long lDataLen;
    pMediaSample->GetPointer(&pData);
    lDataLen = pMediaSample->GetSize();
    {
        CAutoLock cAutoLockShared(&m_cSharedState);
        if (m_rtBallPosition >= m_rtStop) 
        {
            // End of the stream.
            return S_FALSE;
        }
        // Draw the ball in its current position.
        ZeroMemory( pData, lDataLen );
        m_Ball->MoveBall(m_rtBallPosition);
        m_Ball->PlotBall(pData, m_BallPixel, m_iPixelSize);
        
        // The sample times are modified by the current rate.
        REFERENCE_TIME rtStart, rtStop;
        rtStart = static_cast<REFERENCE_TIME>(
                      m_rtSampleTime / m_dRateSeeking);
        rtStop  = rtStart + static_cast<int>(
                      m_iRepeatTime / m_dRateSeeking);
        pMediaSample->SetTime(&rtStart, &rtStop);

        // Increment for the next loop.
        m_rtSampleTime += m_iRepeatTime;
        m_rtBallPosition += m_iRepeatTime;
    }
    pMediaSample->SetSyncPoint(TRUE);
    if (m_bDiscontinuity) 
    {
        pMediaSample->SetDiscontinuity(TRUE);
        m_bDiscontinuity = FALSE;
    }
    return NOERROR;
}
```



<span data-ttu-id="00ed0-200">Ниже приведены основные различия между этой и исходной версиями.</span><span class="sxs-lookup"><span data-stu-id="00ed0-200">The major differences between this version and the original are the following:</span></span>

-   <span data-ttu-id="00ed0-201">Как упоминалось ранее, переменная *m \_ ртбаллпоситион* используется для задания расположения шарика, а не потокового времени.</span><span class="sxs-lookup"><span data-stu-id="00ed0-201">As mentioned earlier, the *m\_rtBallPosition* variable is used to set the position of the ball, rather than the stream time.</span></span>
-   <span data-ttu-id="00ed0-202">После удержания критической секции метод проверяет, превышает ли текущая позиция время окончания.</span><span class="sxs-lookup"><span data-stu-id="00ed0-202">After holding the critical section, the method checks whether the current position exceeds the stop time.</span></span> <span data-ttu-id="00ed0-203">Если да, то возвращается **\_ значение false**, которое сигнализирует базовому классу прекратить отправку данных и доставить уведомление о завершении потока.</span><span class="sxs-lookup"><span data-stu-id="00ed0-203">If so, it returns **S\_FALSE**, which signals the base class to stop sending data and deliver an end-of-stream notification.</span></span>
-   <span data-ttu-id="00ed0-204">Метки времени делятся на текущую ставку.</span><span class="sxs-lookup"><span data-stu-id="00ed0-204">The time stamps are divided by the current rate.</span></span>
-   <span data-ttu-id="00ed0-205">Если *m \_ Бдисконтинуити* имеет **значение true**, метод устанавливает флаг небесперебойности в образце.</span><span class="sxs-lookup"><span data-stu-id="00ed0-205">If *m\_bDiscontinuity* is **TRUE**, the method sets the discontinuity flag on the sample.</span></span>

<span data-ttu-id="00ed0-206">Существует еще одно небольшое отличие.</span><span class="sxs-lookup"><span data-stu-id="00ed0-206">There is another minor difference.</span></span> <span data-ttu-id="00ed0-207">Поскольку исходная версия использует ровно один буфер, она заполняет весь буфер нулями один раз, когда начинается потоковая передача.</span><span class="sxs-lookup"><span data-stu-id="00ed0-207">Because the original version relies on having exactly one buffer, it fills the entire buffer with zeroes once, when streaming begins.</span></span> <span data-ttu-id="00ed0-208">После этого шарик просто удаляется из предыдущего места.</span><span class="sxs-lookup"><span data-stu-id="00ed0-208">After that, it just erases the ball from its previous position.</span></span> <span data-ttu-id="00ed0-209">Однако эта оптимизация раскрывает незначительную ошибку в фильтре шарика.</span><span class="sxs-lookup"><span data-stu-id="00ed0-209">However, this optimization reveals a slight bug in the Ball filter.</span></span> <span data-ttu-id="00ed0-210">Когда метод [**кбасеаутпутпин::D еЦидеаллокатор**](cbaseoutputpin-decideallocator.md) вызывает [**Имеминпутпин:: нотифяллокатор**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator), он устанавливает для флага только для чтения **значение false**.</span><span class="sxs-lookup"><span data-stu-id="00ed0-210">When the [**CBaseOutputPin::DecideAllocator**](cbaseoutputpin-decideallocator.md) method calls [**IMemInputPin::NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator), it sets the read-only flag to **FALSE**.</span></span> <span data-ttu-id="00ed0-211">В результате подчиненный фильтр может записываться в буфер.</span><span class="sxs-lookup"><span data-stu-id="00ed0-211">As a result, the downstream filter is free to write on the buffer.</span></span> <span data-ttu-id="00ed0-212">Одним из решений является переопределение **деЦидеаллокатор** для установки флага "только для чтения" в **значение true**.</span><span class="sxs-lookup"><span data-stu-id="00ed0-212">One solution is to override **DecideAllocator** so that it sets the read-only flag to **TRUE**.</span></span> <span data-ttu-id="00ed0-213">Однако для простоты новая версия просто полностью удаляет оптимизацию.</span><span class="sxs-lookup"><span data-stu-id="00ed0-213">For simplicity, however, the new version simply removes the optimization altogether.</span></span> <span data-ttu-id="00ed0-214">Вместо этого эта версия заполняет буфер нулями каждый раз.</span><span class="sxs-lookup"><span data-stu-id="00ed0-214">Instead, this version fills the buffer with zeroes each time.</span></span>

### <a name="miscellaneous-changes"></a><span data-ttu-id="00ed0-215">Прочие изменения</span><span class="sxs-lookup"><span data-stu-id="00ed0-215">Miscellaneous Changes</span></span>

<span data-ttu-id="00ed0-216">В новой версии эти две строки удаляются из конструктора Кбалл:</span><span class="sxs-lookup"><span data-stu-id="00ed0-216">In the new version, these two lines are removed from the CBall constructor:</span></span>


```C++
    m_iRandX = rand();
    m_iRandY = rand();
```



<span data-ttu-id="00ed0-217">Фильтр исходного шарика использует эти значения для добавления случайных значений в исходное расположение шарика.</span><span class="sxs-lookup"><span data-stu-id="00ed0-217">The original Ball filter uses these values to add some randomness to the initial ball position.</span></span> <span data-ttu-id="00ed0-218">Для наших целей мы хотим, чтобы шарик был детерминированным.</span><span class="sxs-lookup"><span data-stu-id="00ed0-218">For our purposes, we want the ball to be deterministic.</span></span> <span data-ttu-id="00ed0-219">Кроме того, некоторые переменные были изменены с объектов [**крефтиме**](creftime.md) на [**переменные \_ времени ссылки**](reference-time.md) .</span><span class="sxs-lookup"><span data-stu-id="00ed0-219">Also, some variables have been changed from [**CRefTime**](creftime.md) objects to [**REFERENCE\_TIME**](reference-time.md) variables.</span></span> <span data-ttu-id="00ed0-220">(Класс **крефтиме** является тонкой оболочкой для значения **\_ времени ссылки** .) Наконец, реализация [**икуалитиконтрол:: notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) немного изменилась; Дополнительные сведения можно найти в исходном коде.</span><span class="sxs-lookup"><span data-stu-id="00ed0-220">(The **CRefTime** class is a thin wrapper for a **REFERENCE\_TIME** value.) Lastly, the implementation of [**IQualityControl::Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) has been modified slightly; you can refer to the source code for details.</span></span>

## <a name="limitations-of-the-csourceseeking-class"></a><span data-ttu-id="00ed0-221">Ограничения класса Ксаурцесикинг</span><span class="sxs-lookup"><span data-stu-id="00ed0-221">Limitations of the CSourceSeeking Class</span></span>

<span data-ttu-id="00ed0-222">Класс [**ксаурцесикинг**](csourceseeking.md) не предназначен для фильтров с несколькими выходными контактами из-за проблем с обменом данными между контактами.</span><span class="sxs-lookup"><span data-stu-id="00ed0-222">The [**CSourceSeeking**](csourceseeking.md) class is not meant for filters with multiple output pins, because of issues with cross-pin communication.</span></span> <span data-ttu-id="00ed0-223">Например, представьте фильтр анализатора, который получает поток аудио-видео с чередованием, разбивает поток на аудио и видео компоненты и доставляет видео из одного выходного ПИН-кода и звука из другого.</span><span class="sxs-lookup"><span data-stu-id="00ed0-223">For example, imagine a parser filter that receives an interleaved audio-video stream, splits the stream into its audio and video components, and delivers video from one output pin and audio from another.</span></span> <span data-ttu-id="00ed0-224">Оба контакта вывода будут принимать все команды Seek, но фильтр будет искать только один раз для каждой команды Seek.</span><span class="sxs-lookup"><span data-stu-id="00ed0-224">Both output pins will receive every seek command, but the filter should seek only once per seek command.</span></span> <span data-ttu-id="00ed0-225">Решение заключается в назначении одного из контактов для управления поиском и пропуска команд поиска, полученных другим ПИН-кодом.</span><span class="sxs-lookup"><span data-stu-id="00ed0-225">The solution is to designate one of the pins to control seeking and to ignore seek commands received by the other pin.</span></span>

<span data-ttu-id="00ed0-226">Однако после команды Seek оба ПИН-кода должны сбрасывать данные.</span><span class="sxs-lookup"><span data-stu-id="00ed0-226">After the seek command, however, both pins should flush data.</span></span> <span data-ttu-id="00ed0-227">Чтобы усложнить дальнейшие операции, команда Seek выполняется в потоке приложения, а не в потоке потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="00ed0-227">To complicate matters further, the seek command happens on the application thread, not the streaming thread.</span></span> <span data-ttu-id="00ed0-228">Поэтому необходимо убедиться, что ни один из ПИН-кодов не заблокирован и не ожидает возврата вызова [**имеминпутпин:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) , либо это может привести к взаимоблокировке.</span><span class="sxs-lookup"><span data-stu-id="00ed0-228">Therefore, you must make certain that neither pin is blocked and waiting for a [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) call to return, or it might cause a deadlock.</span></span> <span data-ttu-id="00ed0-229">Дополнительные сведения о потокобезопасный сброс в ПИН-кодах см. в разделе [потоки и критические разделы](threads-and-critical-sections.md).</span><span class="sxs-lookup"><span data-stu-id="00ed0-229">For more information about thread-safe flushing in pins, see [Threads and Critical Sections](threads-and-critical-sections.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="00ed0-230">См. также</span><span class="sxs-lookup"><span data-stu-id="00ed0-230">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="00ed0-231">Запись фильтров источника</span><span class="sxs-lookup"><span data-stu-id="00ed0-231">Writing Source Filters</span></span>](writing-source-filters.md)
</dt> </dl>

 

 



