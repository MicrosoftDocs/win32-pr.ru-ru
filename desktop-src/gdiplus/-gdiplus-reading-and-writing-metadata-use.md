---
description: Некоторые файлы изображений содержат метаданные, которые можно прочитать, чтобы определить характеристики изображения.
ms.assetid: 2febea35-3fea-4a2d-baaf-7a4f935fc81f
title: Чтение и запись метаданных
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e4ea0a8f389f31870b31a0b15480815bdd7cf1f
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118299"
---
# <a name="reading-and-writing-metadata"></a>Чтение и запись метаданных

Некоторые файлы изображений содержат метаданные, которые можно прочитать, чтобы определить характеристики изображения. Например, цифровая фотография может содержать метаданные, которые можно прочитать для определения марки и модели камеры, используемой для записи образа. С помощью Windows GDI+ можно считывать существующие метаданные, а также записывать новые метаданные в файлы изображений.

Интерфейс GDI+ обеспечивает единообразный способ хранения и извлечения метаданных из файлов изображений в различных форматах. В GDI+ фрагмент метаданных называется *элементом свойства*. Метаданные можно хранить и извлекать путем вызова методов **сетпропертитем** и **жетпропертитем** класса [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) , и вам не нужно беспокоиться о том, как конкретный формат файлов сохраняет эти метаданные.

В настоящее время GDI+ поддерживает метаданные для форматов TIFF, JPEG, EXIF и PNG. Формат Exif, который указывает, как сохранять изображения, захваченные цифровыми камерами, построена на основе форматов TIFF и JPEG. EXIF использует формат TIFF для несжатых данных пикселей и формат JPEG для сжатых данных пикселей.

GDI+ определяет набор тегов свойств, которые определяют элементы свойств. Некоторые теги предназначены для общего назначения; то есть они поддерживаются всеми форматами файлов, упомянутыми в предыдущем абзаце. Другие теги являются особым целям и применяются только к определенным форматам. При попытке сохранить элемент свойства в файле, который не поддерживает этот элемент свойства, компонент GDI+ игнорирует запрос. В частности, метод [**Image:: сетпропертитем**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-setpropertyitem) возвращает пропертинотсуппортед.

Можно определить элементы свойств, которые хранятся в файле изображения, вызвав [**Image:: жетпропертидлист**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertyidlist). При попытке получить элемент свойства, которого нет в файле, GDI+ игнорирует запрос. В частности, метод [**Image:: жетпропертитем**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertyitem) возвращает пропертинотфаунд.

## <a name="reading-metadata-from-a-file"></a>Чтение метаданных из файла

Следующее консольное приложение вызывает метод **жетпропертисизе** объекта [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) , чтобы определить, сколько элементов метаданных находится в файле FakePhoto.jpg.


```
#include <windows.h>
#include <gdiplus.h>
#include <stdio.h>
using namespace Gdiplus;
INT main()
{
   // Initialize <tla rid="tla_gdiplus"/>.
   GdiplusStartupInput gdiplusStartupInput;
   ULONG_PTR gdiplusToken;
   GdiplusStartup(&gdiplusToken, &gdiplusStartupInput, NULL);
   UINT    size = 0;
   UINT    count = 0;
   Bitmap* bitmap = new Bitmap(L"FakePhoto.jpg");
   bitmap->GetPropertySize(&size, &count);
   printf("There are %d pieces of metadata in the file.\n", count);
   printf("The total size of the metadata is %d bytes.\n", size);
 
   delete bitmap;
   GdiplusShutdown(gdiplusToken);
   return 0;
}
```



Приведенный выше код, наряду с определенным файлом, FakePhoto.jpg, создает следующие выходные данные:


```
There are 7 pieces of metadata in the file.
The total size of the metadata is 436 bytes.
```



GDI+ сохраняет отдельный элемент метаданных в объекте [**пропертитем**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) . Чтобы получить все метаданные из файла, можно вызвать метод **жеталлпропертитемс** класса [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) . Метод **жеталлпропертитемс** возвращает массив объектов **пропертитем** . Перед вызовом **жеталлпропертитемс** необходимо выделить буфер, достаточно большой для получения этого массива. Можно вызвать метод **жетпропертисизе** класса **Image** , чтобы получить размер требуемого буфера (в байтах).

Объект [**пропертитем**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) имеет следующие четыре открытых члена:



|            | Описание                                                                                                                                                                                                                                                                                                       |
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **идентификатор**     | Тег, определяющий элемент метаданных. Значения, которые могут быть назначены **идентификаторам** (Пропертитагимажетитле, Пропертитажекуипмаке, пропертитажексифекспосуретиме и Like), определяются в гдиплусимагинг. h.                                                                                           |
| **length** | Длина массива значений в байтах, на который указывает элемент данных **значения** . Обратите внимание, что если элемент данных **типа** имеет значение пропертитагтипеасЦии, то элемент данных длины имеет **длину** строки символов, завершающейся нулем, включая знак завершения null.                        |
| **type**   | Тип данных значений в массиве, на который указывает элемент данных значения. Константы (Пропертитагтипебите, ПропертитагтипеасЦии и Like), которые представляют различные типы данных, описаны в [**константах типа тега свойства Image**](-gdiplus-constant-image-property-tag-type-constants.md). |
| **value**  | Указатель на массив значений.                                                                                                                                                                                                                                                                       |



 

Следующее консольное приложение считывает и отображает семь элементов метаданных в файле FakePhoto.jpg. Функция Main зависит от вспомогательной функции Пропертитипефромворд, которая показана после функции Main.


```
#include <windows.h>
#include <gdiplus.h>
#include <strsafe.h>
using namespace Gdiplus;

INT main()
{
   // Initialize GDI+
   GdiplusStartupInput gdiplusStartupInput;
   ULONG_PTR gdiplusToken;
   GdiplusStartup(&gdiplusToken, &gdiplusStartupInput, NULL);

   UINT  size = 0;
   UINT  count = 0;

   #define MAX_PROPTYPE_SIZE 30
   WCHAR strPropertyType[MAX_PROPTYPE_SIZE] = L"";

   Bitmap* bitmap = new Bitmap(L"FakePhoto.jpg");

   bitmap->GetPropertySize(&size, &count);
   printf("There are %d pieces of metadata in the file.\n\n", count);

   // GetAllPropertyItems returns an array of PropertyItem objects.
   // Allocate a buffer large enough to receive that array.
   PropertyItem* pPropBuffer =(PropertyItem*)malloc(size);

   // Get the array of PropertyItem objects.
   bitmap->GetAllPropertyItems(size, count, pPropBuffer);

   // For each PropertyItem in the array, display the id, type, and length.
   for(UINT j = 0; j < count; ++j)
   {
      // Convert the property type from a WORD to a string.
      PropertyTypeFromWORD(
         pPropBuffer[j].type, strPropertyType, MAX_PROPTYPE_SIZE);

      printf("Property Item %d\n", j);
      printf("  id: 0x%x\n", pPropBuffer[j].id);
      wprintf(L"  type: %s\n", strPropertyType);
      printf("  length: %d bytes\n\n", pPropBuffer[j].length);
   }

   free(pPropBuffer);
   delete bitmap;
   GdiplusShutdown(gdiplusToken);
   return 0;
} // main

// Helper function
HRESULT PropertyTypeFromWORD(WORD index, WCHAR* string, UINT maxChars)
{
   HRESULT hr = E_FAIL;

   WCHAR* propertyTypes[] = {
      L"Nothing",                   // 0
      L"PropertyTagTypeByte",       // 1
      L"PropertyTagTypeASCII",      // 2
      L"PropertyTagTypeShort",      // 3
      L"PropertyTagTypeLong",       // 4
      L"PropertyTagTypeRational",   // 5
      L"Nothing",                   // 6
      L"PropertyTagTypeUndefined",  // 7
      L"Nothing",                   // 8
      L"PropertyTagTypeSLONG",      // 9
      L"PropertyTagTypeSRational"}; // 10

   hr = StringCchCopyW(string, maxChars, propertyTypes[index]);
   return hr;
}
```



Предыдущее консольное приложение выдает следующие выходные данные:


```
Property Item 0
  id: 0x320
  type: PropertyTagTypeASCII
  length: 16 bytes
Property Item 1
  id: 0x10f
  type: PropertyTagTypeASCII
  length: 17 bytes
Property Item 2
  id: 0x110
  type: PropertyTagTypeASCII
  length: 7 bytes
Property Item 3
  id: 0x9003
  type: PropertyTagTypeASCII
  length: 20 bytes
Property Item 4
  id: 0x829a
  type: PropertyTagTypeRational
  length: 8 bytes
Property Item 5
  id: 0x5090
  type: PropertyTagTypeShort
  length: 128 bytes
Property Item 6
  id: 0x5091
  type: PropertyTagTypeShort
  length: 128 bytes
```



Приведенные выше выходные данные показывают шестнадцатеричный ИДЕНТИФИКАЦИОНный номер для каждого элемента свойства. Вы можете найти эти номера в [константах тегов свойств Image](-gdiplus-constant-image-property-tag-constants.md) и выяснить, что они представляют следующие теги свойств.



| Шестнадцатеричное значение                                                                                                       | Тег свойства                                                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0x0320 0x010f<br/>  0x0110<br/>  0x9003<br/>  0x829a<br/>  0x5090<br/>  0x5091<br/> | Пропертитагимажетитле Пропертитажекуипмаке<br/>  пропертитажекуипмодел<br/>  пропертитажексифдторигинал<br/>  пропертитажексифекспосуретиме<br/>  пропертитаглуминанцетабле<br/>  пропертитагчроминанцетабле<br/> |



 

Второй элемент свойства (index 1) в списке имеет **идентификатор** пропертитажекуипмаке и **тип** пропертитагтипеасЦии. В следующем примере, который является продолжением предыдущего консольного приложения, отображается значение этого элемента свойства:


```
printf("The equipment make is %s.\n", pPropBuffer[1].value);
```



Приведенная выше строка кода выдает следующие выходные данные:


```
The equipment make is Northwind Traders.
```



Пятый элемент свойства (index 4) в списке имеет **идентификатор** пропертитажексифекспосуретиме и **тип** пропертитагтиператионал. Этот тип данных (Пропертитагтиператионал) представляет собой пару **Long** s. В следующем примере, который является продолжением предыдущего консольного приложения, выводит эти два значения **Long** в виде дробной части. Эта дробь, 1/125, является временем выдержки, измеряемым в секундах.


```
long* ptrLong = (long*)(pPropBuffer[4].value);
printf("The exposure time is %d/%d.\n", ptrLong[0], ptrLong[1]);
```



Предыдущий код представит следующий вывод.


```
The exposure time is 1/125.
```



## <a name="writing-metadata-to-a-file"></a>Запись метаданных в файл

Чтобы записать элемент метаданных в объект [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) , инициализируйте объект [**пропертитем**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) , а затем передайте адрес этого объекта **Пропертитем** в метод **сетпропертитем** объекта **Image** .

Следующее консольное приложение записывает один элемент (заголовок образа) метаданных в объект [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) , а затем сохраняет изображение в файл на диске FakePhoto2.jpg. Функция Main зависит от вспомогательной функции Жетенкодерклсид, которая показана в разделе [Получение идентификатора класса для кодировщика](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md).


```
#include <windows.h>
#include <gdiplus.h>
#include <stdio.h>
using namespace Gdiplus;
INT main()
{
   // Initialize <tla rid="tla_gdiplus"/>.
   GdiplusStartupInput gdiplusStartupInput;
   ULONG_PTR gdiplusToken;
   GdiplusStartup(&gdiplusToken, &gdiplusStartupInput, NULL);
   Status stat;
   CLSID  clsid;
   char   propertyValue[] = "Fake Photograph";
   Bitmap* bitmap = new Bitmap(L"FakePhoto.jpg");
   PropertyItem* propertyItem = new PropertyItem;
   // Get the CLSID of the JPEG encoder.
   GetEncoderClsid(L"image/jpeg", &clsid);
   propertyItem->id = PropertyTagImageTitle;
   propertyItem->length = 16;  // string length including NULL terminator
   propertyItem->type = PropertyTagTypeASCII; 
   propertyItem->value = propertyValue;
   bitmap->SetPropertyItem(propertyItem);
   stat = bitmap->Save(L"FakePhoto2.jpg", &clsid, NULL);
   if(stat == Ok)
      printf("FakePhoto2.jpg saved successfully.\n");
   
   delete propertyItem;
   delete bitmap;
   GdiplusShutdown(gdiplusToken);
   return 0;
}
```



 

 
