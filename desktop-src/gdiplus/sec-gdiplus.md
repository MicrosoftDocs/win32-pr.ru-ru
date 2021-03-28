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
# <a name="security-considerations-gdi"></a>Вопросы безопасности: GDI+

В этом разделе содержатся сведения о вопросах безопасности, связанных с программированием с помощью Windows GDI+. В этом разделе не приводятся все, что нужно знать о проблемах безопасности. вместо этого используйте его в качестве отправной точки и ссылки на эту технологическую область.

-   [Проверка успешности выполнения конструкторов](#verifying-the-success-of-constructors)
-   [Выделение буферов](#allocating-buffers)
-   [Проверка ошибок](#error-checking)
-   [Синхронизация потоков](#thread-synchronization)
-   [См. также](#related-topics)

## <a name="verifying-the-success-of-constructors"></a>Проверка успешности выполнения конструкторов

Многие из классов GDI+ предоставляют метод [**Image:: жетластстатус**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getlaststatus) , который можно вызвать, чтобы определить, успешно ли вызваны методы для объекта. Можно также вызвать **Image:: жетластстатус** , чтобы определить, успешно ли конструктор.

В следующем примере показано, как создать объект [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) и вызвать метод [**Image:: жетластстатус**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getlaststatus) , чтобы определить, был ли конструктор успешным. Значения **ОК** и **инвалидпараметер** являются элементами перечисления [**Status**](/windows/desktop/api/Gdiplustypes/ne-gdiplustypes-status) .


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



## <a name="allocating-buffers"></a>Выделение буферов

Несколько методов GDI+ возвращают числовые или символьные данные в буфер, выделенный вызывающим объектом. Для каждого из этих методов существует вспомогательный метод, который предоставляет размер требуемого буфера. Например, метод [**GraphicsPath:: жетпаспоинтс**](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-getpathpoints(outpoint_inint)) возвращает массив объектов [**Point**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point) . Перед вызовом **GraphicsPath:: жетпаспоинтс** необходимо выделить буфер, достаточно большой для хранения этого массива. Размер требуемого буфера можно определить, вызвав метод [**GraphicsPath:: жетпоинткаунт**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-graphicspath-getpointcount) объекта [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) .

В следующем примере показано, как определить количество точек в объекте [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) , выделить буфер достаточного размера, чтобы вместить столько точек, а затем вызвать [**GraphicsPath:: жетпаспоинтс**](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-getpathpoints(outpoint_inint)) для заполнения буфера. Прежде чем код вызывает функцию **GraphicsPath:: жетпаспоинтс**, он проверяет, что выделение буфера прошло успешно, убедившись, что указатель буфера не равен **null**.


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



В предыдущем примере оператор new используется для выделения буфера. Новый оператор удобен, так как буфер заполнен известным количеством объектов [**Point**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point) . В некоторых случаях GDI+ записывает больше в буфер, чем массив объектов GDI+. Иногда буфер заполняется массивом объектов GDI+ вместе с дополнительными данными, на которые указывает член этих объектов. Например, метод [**Image:: жеталлпропертитемс**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getallpropertyitems) возвращает массив объектов [**пропертитем**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) , по одному для каждого элемента свойства (элемента метаданных), хранящегося в изображении. Но **Image:: жеталлпропертитемс** возвращает больше, чем просто массив объектов **пропертитем** . Он добавляет массив с дополнительными данными.

Перед вызовом [**Image:: жеталлпропертитемс**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getallpropertyitems)необходимо выделить буфер, достаточно большой для хранения массива объектов [**пропертитем**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) вместе с дополнительными данными. Чтобы определить общий размер требуемого буфера, можно вызвать метод [**Image:: жетпропертисизе**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertysize) объекта Image.

В следующем примере показано, как создать объект [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) и затем вызвать метод [**Image:: Жеталлпропертитемс**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getallpropertyitems) этого объекта **Image** , чтобы получить все элементы свойств (метаданные), хранящиеся в изображении. Код выделяет буфер на основе значения размера, возвращаемого методом [**Image:: жетпропертисизе**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertysize) . **Image:: жетпропертисизе** также возвращает значение Count, которое позволяет получить количество элементов свойств в изображении. Обратите внимание, что код не вычисляет размер буфера как `count*sizeof(PropertyItem)` . Буфер, вычисленный таким образом, слишком мал.


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



## <a name="error-checking"></a>Проверка ошибок

Большинство примеров кода в документации GDI+ не показывают проверку ошибок. Полная проверка ошибок делает пример кода намного более длинным и может скрывать точку, показанную в примере. Не следует вставлять примеры из документации непосредственно в рабочий код; Вместо этого следует усовершенствовать примеры, добавив собственную проверку ошибок.

В следующем примере показан один из способов реализации проверки ошибок с помощью GDI+. При каждом создании объекта GDI+ код проверяет, был ли конструктор успешным. Эта проверка особенно важна для конструктора [**изображений**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) , который использует чтение файла. Если все четыре объекта GDI+ ([**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics), [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath), **Image** и [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush)) успешно созданы, код вызывает методы для этих объектов. Каждый вызов метода проверяется на успешное выполнение, и в случае сбоя оставшиеся вызовы метода пропускаются.


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



## <a name="thread-synchronization"></a>Синхронизация потоков

Доступ к одному объекту GDI+ может иметь только один поток. Однако в GDI+ не предусмотрен механизм автоматической синхронизации. Поэтому, если два потока в приложении имеют указатель на один и тот же объект GDI+, вы обязаны синхронизировать доступ к этому объекту.

Некоторые методы GDI+ возвращают **обжектбуси** , если поток пытается вызвать метод, в то время как другой поток выполняет метод для того же объекта. Не пытайтесь синхронизировать доступ к объекту на основе возвращаемого значения **обжектбуси** . Вместо этого каждый раз, когда вы обращаетесь к члену или вызываете метод объекта, поместите вызов в критическую секцию или используйте другой стандартный метод синхронизации.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Центре разработчиков безопасности MSDN](https://msdn.microsoft.com/security/)
</dt> <dt>

[Ресурсы по безопасности How-To](/previous-versions/msp-n-p/ff650055(v=pandp.10))
</dt> <dt>

[Центр безопасности TechNet](https://technet.microsoft.com/security/)
</dt> </dl>

 

 
