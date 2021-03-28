---
description: В этом разделе содержатся сведения о вопросах безопасности, связанных с программированием с помощью Windows GDI+.
ms.assetid: 411e16e4-ad8f-4567-8964-564f08283ba5
title: 'Вопросы безопасности: GDI+'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6d8c9d50393708e58651566ee90adcb4339cb9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997450"
---
# <a name="security-considerations-gdi"></a><span data-ttu-id="50f8b-103">Вопросы безопасности: GDI+</span><span class="sxs-lookup"><span data-stu-id="50f8b-103">Security Considerations: GDI+</span></span>

<span data-ttu-id="50f8b-104">В этом разделе содержатся сведения о вопросах безопасности, связанных с программированием с помощью Windows GDI+.</span><span class="sxs-lookup"><span data-stu-id="50f8b-104">This topic provides information about security considerations related to programming with Windows GDI+.</span></span> <span data-ttu-id="50f8b-105">В этом разделе не приводятся все, что нужно знать о проблемах безопасности. вместо этого используйте его в качестве отправной точки и ссылки на эту технологическую область.</span><span class="sxs-lookup"><span data-stu-id="50f8b-105">This topic doesn't provide all you need to know about security issues—instead, use it as a starting point and reference for this technology area.</span></span>

-   [<span data-ttu-id="50f8b-106">Проверка успешности выполнения конструкторов</span><span class="sxs-lookup"><span data-stu-id="50f8b-106">Verifying the Success of Constructors</span></span>](#verifying-the-success-of-constructors)
-   [<span data-ttu-id="50f8b-107">Выделение буферов</span><span class="sxs-lookup"><span data-stu-id="50f8b-107">Allocating Buffers</span></span>](#allocating-buffers)
-   [<span data-ttu-id="50f8b-108">Проверка ошибок</span><span class="sxs-lookup"><span data-stu-id="50f8b-108">Error Checking</span></span>](#error-checking)
-   [<span data-ttu-id="50f8b-109">Синхронизация потоков</span><span class="sxs-lookup"><span data-stu-id="50f8b-109">Thread Synchronization</span></span>](#thread-synchronization)
-   [<span data-ttu-id="50f8b-110">См. также</span><span class="sxs-lookup"><span data-stu-id="50f8b-110">Related topics</span></span>](#related-topics)

## <a name="verifying-the-success-of-constructors"></a><span data-ttu-id="50f8b-111">Проверка успешности выполнения конструкторов</span><span class="sxs-lookup"><span data-stu-id="50f8b-111">Verifying the Success of Constructors</span></span>

<span data-ttu-id="50f8b-112">Многие из классов GDI+ предоставляют метод [**Image:: жетластстатус**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getlaststatus) , который можно вызвать, чтобы определить, успешно ли вызваны методы для объекта.</span><span class="sxs-lookup"><span data-stu-id="50f8b-112">Many of the GDI+ classes provide a [**Image::GetLastStatus**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getlaststatus) method that you can call to determine whether methods invoked on an object are successful.</span></span> <span data-ttu-id="50f8b-113">Можно также вызвать **Image:: жетластстатус** , чтобы определить, успешно ли конструктор.</span><span class="sxs-lookup"><span data-stu-id="50f8b-113">You can also call **Image::GetLastStatus** to determine whether a constructor is successful.</span></span>

<span data-ttu-id="50f8b-114">В следующем примере показано, как создать объект [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) и вызвать метод [**Image:: жетластстатус**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getlaststatus) , чтобы определить, был ли конструктор успешным.</span><span class="sxs-lookup"><span data-stu-id="50f8b-114">The following example shows how to construct an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object and call the [**Image::GetLastStatus**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getlaststatus) method to determine whether the constructor was successful.</span></span> <span data-ttu-id="50f8b-115">Значения **ОК** и **инвалидпараметер** являются элементами перечисления [**Status**](/windows/desktop/api/Gdiplustypes/ne-gdiplustypes-status) .</span><span class="sxs-lookup"><span data-stu-id="50f8b-115">The values **Ok** and **InvalidParameter** are elements of the [**Status**](/windows/desktop/api/Gdiplustypes/ne-gdiplustypes-status) enumeration.</span></span>


```C++
Image myImage(L"Climber.jpg");
Status st = myImage.GetLastStatus();

if(Ok == st)
   // The constructor was successful. Use myImage.
else if(InvalidParameter == st)
   // The constructor failed because of an invalid parameter.
else
   // Compare st to other elements of the Status 
   // enumeration or do general error processing.
```



## <a name="allocating-buffers"></a><span data-ttu-id="50f8b-116">Выделение буферов</span><span class="sxs-lookup"><span data-stu-id="50f8b-116">Allocating Buffers</span></span>

<span data-ttu-id="50f8b-117">Несколько методов GDI+ возвращают числовые или символьные данные в буфер, выделенный вызывающим объектом.</span><span class="sxs-lookup"><span data-stu-id="50f8b-117">Several GDI+ methods return numeric or character data in a buffer that is allocated by the caller.</span></span> <span data-ttu-id="50f8b-118">Для каждого из этих методов существует вспомогательный метод, который предоставляет размер требуемого буфера.</span><span class="sxs-lookup"><span data-stu-id="50f8b-118">For each of those methods, there is a companion method that gives the size of the required buffer.</span></span> <span data-ttu-id="50f8b-119">Например, метод [**GraphicsPath:: жетпаспоинтс**](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-getpathpoints(outpoint_inint)) возвращает массив объектов [**Point**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point) .</span><span class="sxs-lookup"><span data-stu-id="50f8b-119">For example, the [**GraphicsPath::GetPathPoints**](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-getpathpoints(outpoint_inint)) method returns an array of [**Point**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point) objects.</span></span> <span data-ttu-id="50f8b-120">Перед вызовом **GraphicsPath:: жетпаспоинтс** необходимо выделить буфер, достаточно большой для хранения этого массива.</span><span class="sxs-lookup"><span data-stu-id="50f8b-120">Before you call **GraphicsPath::GetPathPoints**, you must allocate a buffer large enough to hold that array.</span></span> <span data-ttu-id="50f8b-121">Размер требуемого буфера можно определить, вызвав метод [**GraphicsPath:: жетпоинткаунт**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-graphicspath-getpointcount) объекта [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) .</span><span class="sxs-lookup"><span data-stu-id="50f8b-121">You can determine the size of the required buffer by calling the [**GraphicsPath::GetPointCount**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-graphicspath-getpointcount) method of a [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) object.</span></span>

<span data-ttu-id="50f8b-122">В следующем примере показано, как определить количество точек в объекте [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) , выделить буфер достаточного размера, чтобы вместить столько точек, а затем вызвать [**GraphicsPath:: жетпаспоинтс**](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-getpathpoints(outpoint_inint)) для заполнения буфера.</span><span class="sxs-lookup"><span data-stu-id="50f8b-122">The following example shows how to determine the number of points in a [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) object, allocate a buffer large enough to hold that many points, and then call [**GraphicsPath::GetPathPoints**](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-getpathpoints(outpoint_inint)) to fill the buffer.</span></span> <span data-ttu-id="50f8b-123">Прежде чем код вызывает функцию **GraphicsPath:: жетпаспоинтс**, он проверяет, что выделение буфера прошло успешно, убедившись, что указатель буфера не равен **null**.</span><span class="sxs-lookup"><span data-stu-id="50f8b-123">Before the code calls **GraphicsPath::GetPathPoints**, it verifies that the buffer allocation was successful by making sure that the buffer pointer is not **NULL**.</span></span>


```C++
GraphicsPath path;
path.AddEllipse(10, 10, 200, 100);

INT count = path.GetPointCount();          // get the size
Point* pointArray = new Point[count];      // allocate the buffer

if(pointArray)  // Check for successful allocation.
{
   path.GetPathPoints(pointArray, count);  // get the data
   ...                                     // use pointArray
   delete[] pointArray;                    // release the buffer
   pointArray = NULL;
}
```



<span data-ttu-id="50f8b-124">В предыдущем примере оператор new используется для выделения буфера.</span><span class="sxs-lookup"><span data-stu-id="50f8b-124">The previous example uses the new operator to allocate a buffer.</span></span> <span data-ttu-id="50f8b-125">Новый оператор удобен, так как буфер заполнен известным количеством объектов [**Point**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point) .</span><span class="sxs-lookup"><span data-stu-id="50f8b-125">The new operator was convenient because the buffer was filled with a known number of [**Point**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point) objects.</span></span> <span data-ttu-id="50f8b-126">В некоторых случаях GDI+ записывает больше в буфер, чем массив объектов GDI+.</span><span class="sxs-lookup"><span data-stu-id="50f8b-126">In some cases, GDI+ writes more into buffer than an array of GDI+ objects.</span></span> <span data-ttu-id="50f8b-127">Иногда буфер заполняется массивом объектов GDI+ вместе с дополнительными данными, на которые указывает член этих объектов.</span><span class="sxs-lookup"><span data-stu-id="50f8b-127">Sometimes a buffer is filled with an array of GDI+ objects along with additional data that is pointed to by members of those objects.</span></span> <span data-ttu-id="50f8b-128">Например, метод [**Image:: жеталлпропертитемс**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getallpropertyitems) возвращает массив объектов [**пропертитем**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) , по одному для каждого элемента свойства (элемента метаданных), хранящегося в изображении.</span><span class="sxs-lookup"><span data-stu-id="50f8b-128">For example, the [**Image::GetAllPropertyItems**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getallpropertyitems) method returns an array of [**PropertyItem**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) objects, one for each property item (piece of metadata) stored in the image.</span></span> <span data-ttu-id="50f8b-129">Но **Image:: жеталлпропертитемс** возвращает больше, чем просто массив объектов **пропертитем** . Он добавляет массив с дополнительными данными.</span><span class="sxs-lookup"><span data-stu-id="50f8b-129">But **Image::GetAllPropertyItems** returns more than just the array of **PropertyItem** objects; it appends the array with additional data.</span></span>

<span data-ttu-id="50f8b-130">Перед вызовом [**Image:: жеталлпропертитемс**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getallpropertyitems)необходимо выделить буфер, достаточно большой для хранения массива объектов [**пропертитем**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) вместе с дополнительными данными.</span><span class="sxs-lookup"><span data-stu-id="50f8b-130">Before you call [**Image::GetAllPropertyItems**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getallpropertyitems), you must allocate a buffer large enough to hold the array of [**PropertyItem**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) objects along with the additional data.</span></span> <span data-ttu-id="50f8b-131">Чтобы определить общий размер требуемого буфера, можно вызвать метод [**Image:: жетпропертисизе**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertysize) объекта Image.</span><span class="sxs-lookup"><span data-stu-id="50f8b-131">You can call the [**Image::GetPropertySize**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertysize) method of an Image object to determine the total size of the required buffer.</span></span>

<span data-ttu-id="50f8b-132">В следующем примере показано, как создать объект [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) и затем вызвать метод [**Image:: Жеталлпропертитемс**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getallpropertyitems) этого объекта **Image** , чтобы получить все элементы свойств (метаданные), хранящиеся в изображении.</span><span class="sxs-lookup"><span data-stu-id="50f8b-132">The following example shows how to create an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object and later call the [**Image::GetAllPropertyItems**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getallpropertyitems) method of that **Image** object to retrieve all the property items (metadata) stored in the image.</span></span> <span data-ttu-id="50f8b-133">Код выделяет буфер на основе значения размера, возвращаемого методом [**Image:: жетпропертисизе**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertysize) .</span><span class="sxs-lookup"><span data-stu-id="50f8b-133">The code allocates a buffer based on a size value returned by the [**Image::GetPropertySize**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertysize) method.</span></span> <span data-ttu-id="50f8b-134">**Image:: жетпропертисизе** также возвращает значение Count, которое позволяет получить количество элементов свойств в изображении.</span><span class="sxs-lookup"><span data-stu-id="50f8b-134">**Image::GetPropertySize** also returns a count value that gives the number of property items in the image.</span></span> <span data-ttu-id="50f8b-135">Обратите внимание, что код не вычисляет размер буфера как `count*sizeof(PropertyItem)` .</span><span class="sxs-lookup"><span data-stu-id="50f8b-135">Notice that the code does not calculate the buffer size as `count*sizeof(PropertyItem)`.</span></span> <span data-ttu-id="50f8b-136">Буфер, вычисленный таким образом, слишком мал.</span><span class="sxs-lookup"><span data-stu-id="50f8b-136">A buffer calculated that way would be too small.</span></span>


```C++
UINT count = 0;
UINT size = 0;
Image myImage(L"FakePhoto.jpg");
myImage.GetPropertySize(&size, &count);

// GetAllPropertyItems returns an array of PropertyItem objects
// along with additional data. Allocate a buffer large enough to 
// receive the array and the additional data.
PropertyItem* propBuffer =(PropertyItem*)malloc(size);

if(propBuffer)
{
   myImage.GetAllPropertyItems(size, count, propBuffer);
   ...
   free(propBuffer);
   propBuffer = NULL;
}
```



## <a name="error-checking"></a><span data-ttu-id="50f8b-137">Проверка ошибок</span><span class="sxs-lookup"><span data-stu-id="50f8b-137">Error Checking</span></span>

<span data-ttu-id="50f8b-138">Большинство примеров кода в документации GDI+ не показывают проверку ошибок.</span><span class="sxs-lookup"><span data-stu-id="50f8b-138">Most of the code examples in the GDI+ documentation do not show error checking.</span></span> <span data-ttu-id="50f8b-139">Полная проверка ошибок делает пример кода намного более длинным и может скрывать точку, показанную в примере.</span><span class="sxs-lookup"><span data-stu-id="50f8b-139">Complete error checking makes a code example much longer and can obscure the point being illustrated by the example.</span></span> <span data-ttu-id="50f8b-140">Не следует вставлять примеры из документации непосредственно в рабочий код; Вместо этого следует усовершенствовать примеры, добавив собственную проверку ошибок.</span><span class="sxs-lookup"><span data-stu-id="50f8b-140">You should not paste examples from the documentation directly into production code; rather, you should enhance the examples by adding your own error checking.</span></span>

<span data-ttu-id="50f8b-141">В следующем примере показан один из способов реализации проверки ошибок с помощью GDI+.</span><span class="sxs-lookup"><span data-stu-id="50f8b-141">The following example shows one way of implementing error checking with GDI+.</span></span> <span data-ttu-id="50f8b-142">При каждом создании объекта GDI+ код проверяет, был ли конструктор успешным.</span><span class="sxs-lookup"><span data-stu-id="50f8b-142">Each time a GDI+ object is constructed, the code checks to see whether the constructor was successful.</span></span> <span data-ttu-id="50f8b-143">Эта проверка особенно важна для конструктора [**изображений**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) , который использует чтение файла.</span><span class="sxs-lookup"><span data-stu-id="50f8b-143">That check is especially important for the [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) constructor, which relies on reading a file.</span></span> <span data-ttu-id="50f8b-144">Если все четыре объекта GDI+ ([**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics), [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath), **Image** и [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush)) успешно созданы, код вызывает методы для этих объектов.</span><span class="sxs-lookup"><span data-stu-id="50f8b-144">If all four of the GDI+ objects ([**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics), [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath), **Image**, and [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush)) are constructed successfully, the code calls methods on those objects.</span></span> <span data-ttu-id="50f8b-145">Каждый вызов метода проверяется на успешное выполнение, и в случае сбоя оставшиеся вызовы метода пропускаются.</span><span class="sxs-lookup"><span data-stu-id="50f8b-145">Each method call is checked for success, and in the event of failure, the remaining method calls are skipped.</span></span>


```C++
Status GdipExample(HDC hdc)
{
   Status status = GenericError;
   INT count = 0;
   Point* points = NULL;

   Graphics graphics(hdc);
   status = graphics.GetLastStatus();
   if(Ok != status)
      return status;

   GraphicsPath path;
   status = path.GetLastStatus();
   if(Ok != status)
      return status;

   Image image(L"MyTexture.bmp");
   status = image.GetLastStatus();
   if(Ok != status)
      return status;

   TextureBrush brush(&image);
   status = brush.GetLastStatus();
   if(Ok != status)
      return status;

   status = path.AddEllipse(10, 10, 200, 100);

   if(Ok == status)
   {
      status = path.AddBezier(40, 130, 200, 130, 200, 200, 60, 200);
   }
  
   if(Ok == status)
   {
      count = path.GetPointCount();
      status = path.GetLastStatus();
   }

   if(Ok == status)
   {
      points = new Point[count];

      if(NULL == points)
         status = OutOfMemory;
   }

   if(Ok == status)
   {
      status = path.GetPathPoints(points, count);  
   }
  
   if(Ok == status)
   {
      status = graphics.FillPath(&brush, &path);
   }
   
   if(Ok == status)
   {
      for(int j = 0; j < count; ++j)
      {
         status = graphics.FillEllipse(
         &brush, points[j].X - 5, points[j].Y - 5, 10, 10);
      }
   }

   if(points)
   {
      delete[] points;
      points = NULL;
   }

   return status;
}
```



## <a name="thread-synchronization"></a><span data-ttu-id="50f8b-146">Синхронизация потоков</span><span class="sxs-lookup"><span data-stu-id="50f8b-146">Thread Synchronization</span></span>

<span data-ttu-id="50f8b-147">Доступ к одному объекту GDI+ может иметь только один поток.</span><span class="sxs-lookup"><span data-stu-id="50f8b-147">It is possible for more than one thread to have access to a single GDI+ object.</span></span> <span data-ttu-id="50f8b-148">Однако в GDI+ не предусмотрен механизм автоматической синхронизации.</span><span class="sxs-lookup"><span data-stu-id="50f8b-148">However, GDI+ does not provide any automatic synchronization mechanism.</span></span> <span data-ttu-id="50f8b-149">Поэтому, если два потока в приложении имеют указатель на один и тот же объект GDI+, вы обязаны синхронизировать доступ к этому объекту.</span><span class="sxs-lookup"><span data-stu-id="50f8b-149">So if two threads in your application have a pointer to the same GDI+ object, it is your responsibility to synchronize access to that object.</span></span>

<span data-ttu-id="50f8b-150">Некоторые методы GDI+ возвращают **обжектбуси** , если поток пытается вызвать метод, в то время как другой поток выполняет метод для того же объекта.</span><span class="sxs-lookup"><span data-stu-id="50f8b-150">Some GDI+ methods return **ObjectBusy** if a thread attempts to call a method while another thread is executing a method on the same object.</span></span> <span data-ttu-id="50f8b-151">Не пытайтесь синхронизировать доступ к объекту на основе возвращаемого значения **обжектбуси** .</span><span class="sxs-lookup"><span data-stu-id="50f8b-151">Do not try to synchronize access to an object based on the **ObjectBusy** return value.</span></span> <span data-ttu-id="50f8b-152">Вместо этого каждый раз, когда вы обращаетесь к члену или вызываете метод объекта, поместите вызов в критическую секцию или используйте другой стандартный метод синхронизации.</span><span class="sxs-lookup"><span data-stu-id="50f8b-152">Instead, each time you access a member or call a method of the object, place the call inside a critical section, or use some other standard synchronization technique.</span></span>

## <a name="related-topics"></a><span data-ttu-id="50f8b-153">См. также</span><span class="sxs-lookup"><span data-stu-id="50f8b-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="50f8b-154">Центре разработчиков безопасности MSDN</span><span class="sxs-lookup"><span data-stu-id="50f8b-154">MSDN Security Developer Center</span></span>](https://msdn.microsoft.com/security/)
</dt> <dt>

<span data-ttu-id="50f8b-155">[Ресурсы по безопасности How-To](/previous-versions/msp-n-p/ff650055(v=pandp.10))</span><span class="sxs-lookup"><span data-stu-id="50f8b-155">[Security How-To Resources](/previous-versions/msp-n-p/ff650055(v=pandp.10))</span></span>
</dt> <dt>

[<span data-ttu-id="50f8b-156">Центр безопасности TechNet</span><span class="sxs-lookup"><span data-stu-id="50f8b-156">TechNet Security Center</span></span>](https://technet.microsoft.com/security/)
</dt> </dl>

 

 
