---
description: Реализация Ивикбитмапкодекпрогресснотификатион (декодер)
ms.assetid: 686b0875-c7ec-45ee-bd3e-94bfd9e5dcda
title: Реализация Ивикбитмапкодекпрогресснотификатион (декодер)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f92f05f02e77886d96d794be3f974c1eb0eed9dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712039"
---
# <a name="implementing-iwicbitmapcodecprogressnotification-decoder"></a><span data-ttu-id="7aef4-103">Реализация Ивикбитмапкодекпрогресснотификатион (декодер)</span><span class="sxs-lookup"><span data-stu-id="7aef4-103">Implementing IWICBitmapCodecProgressNotification (Decoder)</span></span>

## <a name="iwicbitmapcodecprogressnotification"></a><span data-ttu-id="7aef4-104">ивикбитмапкодекпрогресснотификатион</span><span class="sxs-lookup"><span data-stu-id="7aef4-104">IWICBitmapCodecProgressNotification</span></span>

<span data-ttu-id="7aef4-105">Когда кодек выполняет операцию ввода-вывода, например [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) , на большом изображении, выполнение может занять несколько секунд или даже минут.</span><span class="sxs-lookup"><span data-stu-id="7aef4-105">When a codec is performing an I/O operation such as [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) on a large image, it may take several seconds or even minutes to complete.</span></span> <span data-ttu-id="7aef4-106">Если конечные пользователи не могут прерывать работу длительной операции, это может привести к зависанию приложения.</span><span class="sxs-lookup"><span data-stu-id="7aef4-106">When end users are unable to interrupt a long-running operation, they may think the application has hung.</span></span> <span data-ttu-id="7aef4-107">Пользователи часто закрывают приложение или даже перезапускают свои компьютеры при попытке восстановить контроль над компьютером, когда приложение перестает отвечать на запросы.</span><span class="sxs-lookup"><span data-stu-id="7aef4-107">Users will often close an application, or even restart their computers, in an attempt to regain control of their computer when an application becomes unresponsive.</span></span>

<span data-ttu-id="7aef4-108">Этот интерфейс позволяет приложению указать функцию обратного вызова, которую кодек может вызывать через заданные интервалы, чтобы уведомить вызывающего объекта о ходе выполнения текущей операции.</span><span class="sxs-lookup"><span data-stu-id="7aef4-108">This interface enables an application to specify a callback function that the codec can call at specified intervals to notify the caller of the progress of the current operation.</span></span> <span data-ttu-id="7aef4-109">Приложение может использовать эту функцию обратного вызова для отображения сведений о ходе выполнения в пользовательском интерфейсе, чтобы уведомить пользователя о состоянии операции.</span><span class="sxs-lookup"><span data-stu-id="7aef4-109">The application can use this callback function to display an indication of progress in the user interface to notify the user of the status of the operation.</span></span> <span data-ttu-id="7aef4-110">Если пользователь нажимает кнопку **Отмена** в диалоговом окне **ход выполнения** , приложение возвращает **винкодек Err \_ , \_ прерванное** из функции обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="7aef4-110">If a user clicks the **Cancel** button on the **Progress** dialog box, the application returns **WINCODEC\_ERR\_ABORTED** from the callback function.</span></span> <span data-ttu-id="7aef4-111">В этом случае кодек должен отменить указанную операцию и передать этот **HRESULT** обратно вызывающему методу метода, который выполнял операцию.</span><span class="sxs-lookup"><span data-stu-id="7aef4-111">When this happens, the codec must cancel the specified operation and propagate this **HRESULT** back to the caller of the method that was performing the operation.</span></span>

<span data-ttu-id="7aef4-112">Этот интерфейс должен быть реализован в классе декодера уровня контейнера.</span><span class="sxs-lookup"><span data-stu-id="7aef4-112">This interface should be implemented on your container-level decoder class.</span></span>


```C++
interface IWICBitmapCodecProgressNotification : public IUnknown
{
    HRESULT RegisterProgressNotification ( 
        PFNProgressNotification pfnProgressNotification,
        LPVOID pvData,
        DWORD dwProgressFlags );
}
```



-   [<span data-ttu-id="7aef4-113">регистерпрогресснотификатион</span><span class="sxs-lookup"><span data-stu-id="7aef4-113">RegisterProgressNotification</span></span>](#registerprogressnotification)
-   [<span data-ttu-id="7aef4-114">пфнпрогресснотификатион</span><span class="sxs-lookup"><span data-stu-id="7aef4-114">PFNProgressNotification</span></span>](#pfnprogressnotification)

### <a name="registerprogressnotification"></a><span data-ttu-id="7aef4-115">регистерпрогресснотификатион</span><span class="sxs-lookup"><span data-stu-id="7aef4-115">RegisterProgressNotification</span></span>

<span data-ttu-id="7aef4-116">[**Регистерпрогресснотификатион**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecprogressnotification-registerprogressnotification) вызывается приложением для регистрации функции обратного вызова, которую кодек может вызывать через указанные интервалы.</span><span class="sxs-lookup"><span data-stu-id="7aef4-116">[**RegisterProgressNotification**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecprogressnotification-registerprogressnotification) is invoked by an application to register a callback function that the codec can call at specified intervals.</span></span> <span data-ttu-id="7aef4-117">Первый параметр, *пфнпрогресснотификатион*, является указателем на функцию обратного вызова, которую кодек должен вызывать через регулярные интервалы.</span><span class="sxs-lookup"><span data-stu-id="7aef4-117">The first parameter, *pfnProgressNotification*, is a pointer to the callback function that the codec should call at regular intervals.</span></span>

<span data-ttu-id="7aef4-118">Параметр *пвдата* указывает на некоторый объект, который вызывающий объект хочет передать кодеку обратно в функцию обратного вызова при вызове функции обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="7aef4-118">The *pvData* parameter points to some object that the caller wants the codec to pass back to the callback function whenever the callback function is invoked.</span></span> <span data-ttu-id="7aef4-119">Этот объект может быть любым, но не имеет особой значимости для кодека.</span><span class="sxs-lookup"><span data-stu-id="7aef4-119">This object may be anything at all and has no particular significance to the codec.</span></span>

<span data-ttu-id="7aef4-120">Параметр *двпрогрессфлагс* указывает, когда кодек должен вызывать функцию обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="7aef4-120">The *dwProgressFlags* parameter specifies when the codec should call the callback function.</span></span> <span data-ttu-id="7aef4-121">Для этого параметра можно выполнить функцию или с двумя перечислениями.</span><span class="sxs-lookup"><span data-stu-id="7aef4-121">An OR function can be performed with two enumerations for this parameter.</span></span> <span data-ttu-id="7aef4-122">Перечисление [**викпрогрессоператион**](/windows/desktop/api/Wincodec/ne-wincodec-wicprogressoperation) указывает, следует ли вызывать функцию обратного вызова во время декодирования (**викпрогрессоператионкопипикселс**), кодировки (**Викпрожерссоператионвритепикселс**) или обоих (**WICProgressOperationAll**).</span><span class="sxs-lookup"><span data-stu-id="7aef4-122">The [**WICProgressOperation**](/windows/desktop/api/Wincodec/ne-wincodec-wicprogressoperation) enum specifies whether to call the callback function during decoding (**WICProgressOperationCopyPixels**), encoding (**WICProgerssOperationWritePixels**), or both (**WICProgressOperationAll**).</span></span>


```C++
enum WICProgressOperation
{
   WICProgressOperationCopyPixels,
   WICProgerssOperationWritePixels,
   WICProgressOperationAll      
};
```



<span data-ttu-id="7aef4-123">Кодек должен вызывать функцию обратного вызова через регулярные интервалы во всей операции, но вызывающая сторона может указать определенные требования.</span><span class="sxs-lookup"><span data-stu-id="7aef4-123">The codec should call the callback function at regular intervals throughout the operation, but the caller may specify certain requirements.</span></span> <span data-ttu-id="7aef4-124">Перечисление [**викпрогресснотификатион**](/windows/desktop/api/Wincodec/ne-wincodec-wicprogressnotification) указывает, в какой точке операции следует вызвать функцию обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="7aef4-124">The [**WICProgressNotification**](/windows/desktop/api/Wincodec/ne-wincodec-wicprogressnotification) enum indicates at which point in the operation to call the callback function.</span></span> <span data-ttu-id="7aef4-125">Если вызывающий объект указывает **викпрогресснотификатионбегин**, необходимо вызвать его в начале операции (0,0).</span><span class="sxs-lookup"><span data-stu-id="7aef4-125">If the caller specifies **WICProgressNotificationBegin**, you must call it at the beginning of the operation (0.0).</span></span> <span data-ttu-id="7aef4-126">Если вызывающий объект не указывает это, он является необязательным.</span><span class="sxs-lookup"><span data-stu-id="7aef4-126">If the caller does not specify this, it is optional.</span></span> <span data-ttu-id="7aef4-127">Аналогично, если вызывающий объект указывает **викпрожерсснотификатионенд**, необходимо вызвать его после завершения операции (1,0).</span><span class="sxs-lookup"><span data-stu-id="7aef4-127">Likewise, if the caller specifies **WICProgerssNotificationEnd**, you must call it when the operation is completed (1.0).</span></span> <span data-ttu-id="7aef4-128">Если вызывающий объект указывает **викпрогресснотификатионалл**, необходимо вызвать его в начале и в конце, а также через регулярные интервалы во всей операции.</span><span class="sxs-lookup"><span data-stu-id="7aef4-128">If the caller specifies **WICProgressNotificationAll**, you must call it at the beginning and end, as well as at regular intervals throughout the operation.</span></span> <span data-ttu-id="7aef4-129">Вызывающий объект также может указывать **викпрожерсснотификатионфрекуент**, который указывает, что они должны быть вызваны с частыми интервалами, например после каждой пары строк проверки.</span><span class="sxs-lookup"><span data-stu-id="7aef4-129">The caller may also specify **WICProgerssNotificationFrequent**, which indicates that they want to be called back at frequent intervals, perhaps after every couple of scan lines.</span></span> <span data-ttu-id="7aef4-130">(Вызывающий объект обычно использует этот флаг только для очень большого образа.) В противном случае обычно приходится выполнять обратный вызов с интервалом примерно 10% от общего числа обрабатываемых строк сканирования.</span><span class="sxs-lookup"><span data-stu-id="7aef4-130">(A caller will usually use this flag only for a very large image.) Otherwise, you should usually call back at intervals of approximately 10 percent increments of the total number of scan lines to be processed.</span></span>


```C++
enum WICProgressNotification
{
   WICProgressNotificationBegin,
   WICProgerssNotificationEnd,
   WICProgerssNotificationFrequent,
   WICProgressNotificationAll
};
```



<span data-ttu-id="7aef4-131">Только одна функция обратного вызова в каждый момент времени может быть зарегистрирована для конкретного декодера или экземпляра кодировщика.</span><span class="sxs-lookup"><span data-stu-id="7aef4-131">Only one callback function at a time can be registered for a specific decoder or encoder instance.</span></span> <span data-ttu-id="7aef4-132">Если приложение вызывает [**регистерпрогресснотификатион**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecprogressnotification-registerprogressnotification) несколько раз, замените ранее зарегистрированную функцию обратного вызова новой.</span><span class="sxs-lookup"><span data-stu-id="7aef4-132">If an application calls [**RegisterProgressNotification**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecprogressnotification-registerprogressnotification) more than once, replace the previously registered callback function with the new one.</span></span> <span data-ttu-id="7aef4-133">Чтобы отменить регистрацию обратного вызова, вызывающий объект установит значение **null** для параметра *пфнпрогресснотификатион* .</span><span class="sxs-lookup"><span data-stu-id="7aef4-133">To cancel a callback registration, a caller will set the *pfnProgressNotification* parameter to **NULL**.</span></span>

### <a name="pfnprogressnotification"></a><span data-ttu-id="7aef4-134">пфнпрогресснотификатион</span><span class="sxs-lookup"><span data-stu-id="7aef4-134">PFNProgressNotification</span></span>

<span data-ttu-id="7aef4-135">[**Пфнпрогресснотификатион**](/windows/desktop/api/Wincodec/nc-wincodec-pfnprogressnotification) — это функция обратного вызова со следующей сигнатурой.</span><span class="sxs-lookup"><span data-stu-id="7aef4-135">[**PFNProgressNotification**](/windows/desktop/api/Wincodec/nc-wincodec-pfnprogressnotification) is the callback function with the following signature.</span></span>


```C++
typedef HRESULT (*PFNProgressNotification) ( 
   LPVOID pvData,
   ULONG uFrameNum,
   WICProgressOperation operation,
   double dblProgress );
```



<span data-ttu-id="7aef4-136">При вызове функции обратного вызова используйте параметр *пвдата* , чтобы передать тот же *пвдата* , что и приложение, заданное при регистрации функции обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="7aef4-136">When you invoke the callback function, use the *pvData* parameter to pass back the same *pvData* that the application specified when it registered the callback function.</span></span>

<span data-ttu-id="7aef4-137">Параметр *уфраменум* должен указывать индекс обрабатываемого кадра.</span><span class="sxs-lookup"><span data-stu-id="7aef4-137">The *uFrameNum* parameter should indicate the index of the frame that is being processed.</span></span>

<span data-ttu-id="7aef4-138">Задайте для параметра операции значение **викпрогрессоператионкопипикселс** при декодировании и **викпрогрессоператионвритепикселс** при кодировании.</span><span class="sxs-lookup"><span data-stu-id="7aef4-138">Set the operation parameter to **WICProgressOperationCopyPixels** when decoding and **WICProgressOperationWritePixels** when encoding.</span></span>

<span data-ttu-id="7aef4-139">Параметр *дблпрогресс* должен быть числом в диапазоне от 0,0 (начало операции) до 1,0 (завершение операции).</span><span class="sxs-lookup"><span data-stu-id="7aef4-139">The *dblProgress* parameter should be a number between 0.0 (the beginning of the operation) and 1.0 (the completion of the operation).</span></span> <span data-ttu-id="7aef4-140">Значение должно отражать долю строк сканирования, уже обработанных относительно общего количества обрабатываемых строк сканирования.</span><span class="sxs-lookup"><span data-stu-id="7aef4-140">The value should reflect the proportion of scan lines already processed relative to the total number of scan lines to be processed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7aef4-141">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="7aef4-141">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="7aef4-142">**Reference**</span><span class="sxs-lookup"><span data-stu-id="7aef4-142">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="7aef4-143">**прогресснотификатионкаллбакк**</span><span class="sxs-lookup"><span data-stu-id="7aef4-143">**ProgressNotificationCallback**</span></span>](/windows/desktop/api/Wincodec/nc-wincodec-pfnprogressnotification)
</dt> <dt>

[<span data-ttu-id="7aef4-144">**ивикбитмапкодекпрогресснотификатион**</span><span class="sxs-lookup"><span data-stu-id="7aef4-144">**IWICBitmapCodecProgressNotification**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecprogressnotification)
</dt> <dt>

<span data-ttu-id="7aef4-145">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="7aef4-145">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="7aef4-146">Реализация Ивикбитмапдекодер</span><span class="sxs-lookup"><span data-stu-id="7aef4-146">Implementing IWICBitmapDecoder</span></span>](-wic-imp-iwicbitmapdecoder.md)
</dt> <dt>

[<span data-ttu-id="7aef4-147">Реализация IWICBitmapSource</span><span class="sxs-lookup"><span data-stu-id="7aef4-147">Implementing IWICBitmapSource</span></span>](-wic-imp-iwicbitmapsource.md)
</dt> <dt>

[<span data-ttu-id="7aef4-148">Написание WIC-Enabled КОДЕка</span><span class="sxs-lookup"><span data-stu-id="7aef4-148">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="7aef4-149">Общие сведения о компоненте создания образов Windows</span><span class="sxs-lookup"><span data-stu-id="7aef4-149">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



