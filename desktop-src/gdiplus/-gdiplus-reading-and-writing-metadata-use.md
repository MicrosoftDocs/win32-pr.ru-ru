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
# <a name="reading-and-writing-metadata"></a><span data-ttu-id="b3162-103">Чтение и запись метаданных</span><span class="sxs-lookup"><span data-stu-id="b3162-103">Reading and Writing Metadata</span></span>

<span data-ttu-id="b3162-104">Некоторые файлы изображений содержат метаданные, которые можно прочитать, чтобы определить характеристики изображения.</span><span class="sxs-lookup"><span data-stu-id="b3162-104">Some image files contain metadata that you can read to determine features of the image.</span></span> <span data-ttu-id="b3162-105">Например, цифровая фотография может содержать метаданные, которые можно прочитать для определения марки и модели камеры, используемой для записи образа.</span><span class="sxs-lookup"><span data-stu-id="b3162-105">For example, a digital photograph might contain metadata that you can read to determine the make and model of the camera used to capture the image.</span></span> <span data-ttu-id="b3162-106">С помощью Windows GDI+ можно считывать существующие метаданные, а также записывать новые метаданные в файлы изображений.</span><span class="sxs-lookup"><span data-stu-id="b3162-106">With Windows GDI+, you can read existing metadata, and you can also write new metadata to image files.</span></span>

<span data-ttu-id="b3162-107">Интерфейс GDI+ обеспечивает единообразный способ хранения и извлечения метаданных из файлов изображений в различных форматах.</span><span class="sxs-lookup"><span data-stu-id="b3162-107">GDI+ provides a uniform way of storing and retrieving metadata from image files in various formats.</span></span> <span data-ttu-id="b3162-108">В GDI+ фрагмент метаданных называется *элементом свойства*.</span><span class="sxs-lookup"><span data-stu-id="b3162-108">In GDI+, a piece of metadata is called a *property item*.</span></span> <span data-ttu-id="b3162-109">Метаданные можно хранить и извлекать путем вызова методов **сетпропертитем** и **жетпропертитем** класса [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) , и вам не нужно беспокоиться о том, как конкретный формат файлов сохраняет эти метаданные.</span><span class="sxs-lookup"><span data-stu-id="b3162-109">You can store and retrieve metadata by calling the **SetPropertyItem** and **GetPropertyItem** methods of the [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) class, and you don't have to be concerned about the details of how a particular file format stores that metadata.</span></span>

<span data-ttu-id="b3162-110">В настоящее время GDI+ поддерживает метаданные для форматов TIFF, JPEG, EXIF и PNG.</span><span class="sxs-lookup"><span data-stu-id="b3162-110">GDI+ currently supports metadata for the TIFF, JPEG, Exif, and PNG file formats.</span></span> <span data-ttu-id="b3162-111">Формат Exif, который указывает, как сохранять изображения, захваченные цифровыми камерами, построена на основе форматов TIFF и JPEG.</span><span class="sxs-lookup"><span data-stu-id="b3162-111">The Exif format, which specifies how to store images captured by digital still cameras, is built on top of the TIFF and JPEG formats.</span></span> <span data-ttu-id="b3162-112">EXIF использует формат TIFF для несжатых данных пикселей и формат JPEG для сжатых данных пикселей.</span><span class="sxs-lookup"><span data-stu-id="b3162-112">Exif uses the TIFF format for uncompressed pixel data and the JPEG format for compressed pixel data.</span></span>

<span data-ttu-id="b3162-113">GDI+ определяет набор тегов свойств, которые определяют элементы свойств.</span><span class="sxs-lookup"><span data-stu-id="b3162-113">GDI+ defines a set of property tags that identify property items.</span></span> <span data-ttu-id="b3162-114">Некоторые теги предназначены для общего назначения; то есть они поддерживаются всеми форматами файлов, упомянутыми в предыдущем абзаце.</span><span class="sxs-lookup"><span data-stu-id="b3162-114">Certain tags are general-purpose; that is, they are supported by all of the file formats mentioned in the preceding paragraph.</span></span> <span data-ttu-id="b3162-115">Другие теги являются особым целям и применяются только к определенным форматам.</span><span class="sxs-lookup"><span data-stu-id="b3162-115">Other tags are special-purpose and apply only to certain formats.</span></span> <span data-ttu-id="b3162-116">При попытке сохранить элемент свойства в файле, который не поддерживает этот элемент свойства, компонент GDI+ игнорирует запрос.</span><span class="sxs-lookup"><span data-stu-id="b3162-116">If you try to save a property item to a file that does not support that property item, GDI+ ignores the request.</span></span> <span data-ttu-id="b3162-117">В частности, метод [**Image:: сетпропертитем**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-setpropertyitem) возвращает пропертинотсуппортед.</span><span class="sxs-lookup"><span data-stu-id="b3162-117">More specifically, the [**Image::SetPropertyItem**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-setpropertyitem) method returns PropertyNotSupported.</span></span>

<span data-ttu-id="b3162-118">Можно определить элементы свойств, которые хранятся в файле изображения, вызвав [**Image:: жетпропертидлист**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertyidlist).</span><span class="sxs-lookup"><span data-stu-id="b3162-118">You can determine the property items that are stored in an image file by calling [**Image::GetPropertyIdList**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertyidlist).</span></span> <span data-ttu-id="b3162-119">При попытке получить элемент свойства, которого нет в файле, GDI+ игнорирует запрос.</span><span class="sxs-lookup"><span data-stu-id="b3162-119">If you try to retrieve a property item that is not in the file, GDI+ ignores the request.</span></span> <span data-ttu-id="b3162-120">В частности, метод [**Image:: жетпропертитем**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertyitem) возвращает пропертинотфаунд.</span><span class="sxs-lookup"><span data-stu-id="b3162-120">More specifically, the [**Image::GetPropertyItem**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertyitem) method returns PropertyNotFound.</span></span>

## <a name="reading-metadata-from-a-file"></a><span data-ttu-id="b3162-121">Чтение метаданных из файла</span><span class="sxs-lookup"><span data-stu-id="b3162-121">Reading Metadata from a File</span></span>

<span data-ttu-id="b3162-122">Следующее консольное приложение вызывает метод **жетпропертисизе** объекта [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) , чтобы определить, сколько элементов метаданных находится в файле FakePhoto.jpg.</span><span class="sxs-lookup"><span data-stu-id="b3162-122">The following console application calls the **GetPropertySize** method of an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object to determine how many pieces of metadata are in the file FakePhoto.jpg.</span></span>


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



<span data-ttu-id="b3162-123">Приведенный выше код, наряду с определенным файлом, FakePhoto.jpg, создает следующие выходные данные:</span><span class="sxs-lookup"><span data-stu-id="b3162-123">The preceding code, along with a particular file, FakePhoto.jpg, produced the following output:</span></span>


```
There are 7 pieces of metadata in the file.
The total size of the metadata is 436 bytes.
```



<span data-ttu-id="b3162-124">GDI+ сохраняет отдельный элемент метаданных в объекте [**пропертитем**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) .</span><span class="sxs-lookup"><span data-stu-id="b3162-124">GDI+ stores an individual piece of metadata in a [**PropertyItem**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) object.</span></span> <span data-ttu-id="b3162-125">Чтобы получить все метаданные из файла, можно вызвать метод **жеталлпропертитемс** класса [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) .</span><span class="sxs-lookup"><span data-stu-id="b3162-125">You can call the **GetAllPropertyItems** method of the [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) class to retrieve all the metadata from a file.</span></span> <span data-ttu-id="b3162-126">Метод **жеталлпропертитемс** возвращает массив объектов **пропертитем** .</span><span class="sxs-lookup"><span data-stu-id="b3162-126">The **GetAllPropertyItems** method returns an array of **PropertyItem** objects.</span></span> <span data-ttu-id="b3162-127">Перед вызовом **жеталлпропертитемс** необходимо выделить буфер, достаточно большой для получения этого массива.</span><span class="sxs-lookup"><span data-stu-id="b3162-127">Before you call **GetAllPropertyItems**, you must allocate a buffer large enough to receive that array.</span></span> <span data-ttu-id="b3162-128">Можно вызвать метод **жетпропертисизе** класса **Image** , чтобы получить размер требуемого буфера (в байтах).</span><span class="sxs-lookup"><span data-stu-id="b3162-128">You can call the **GetPropertySize** method of the **Image** class to get the size (in bytes) of the required buffer.</span></span>

<span data-ttu-id="b3162-129">Объект [**пропертитем**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) имеет следующие четыре открытых члена:</span><span class="sxs-lookup"><span data-stu-id="b3162-129">A [**PropertyItem**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) object has the following four public members:</span></span>



|            | <span data-ttu-id="b3162-130">Описание</span><span class="sxs-lookup"><span data-stu-id="b3162-130">Description</span></span>                                                                                                                                                                                                                                                                                                       |
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3162-131">**идентификатор**</span><span class="sxs-lookup"><span data-stu-id="b3162-131">**id**</span></span>     | <span data-ttu-id="b3162-132">Тег, определяющий элемент метаданных.</span><span class="sxs-lookup"><span data-stu-id="b3162-132">A tag that identifies the metadata item.</span></span> <span data-ttu-id="b3162-133">Значения, которые могут быть назначены **идентификаторам** (Пропертитагимажетитле, Пропертитажекуипмаке, пропертитажексифекспосуретиме и Like), определяются в гдиплусимагинг. h.</span><span class="sxs-lookup"><span data-stu-id="b3162-133">The values that can be assigned to **id** (PropertyTagImageTitle, PropertyTagEquipMake, PropertyTagExifExposureTime, and the like) are defined in Gdiplusimaging.h.</span></span>                                                                                           |
| <span data-ttu-id="b3162-134">**length**</span><span class="sxs-lookup"><span data-stu-id="b3162-134">**length**</span></span> | <span data-ttu-id="b3162-135">Длина массива значений в байтах, на который указывает элемент данных **значения** .</span><span class="sxs-lookup"><span data-stu-id="b3162-135">The length, in bytes, of the array of values pointed to by the **value** data member.</span></span> <span data-ttu-id="b3162-136">Обратите внимание, что если элемент данных **типа** имеет значение пропертитагтипеасЦии, то элемент данных длины имеет **длину** строки символов, завершающейся нулем, включая знак завершения null.</span><span class="sxs-lookup"><span data-stu-id="b3162-136">Note that if the **type** data member is set to PropertyTagTypeASCII, then the length data member is the **length** of a null-terminated character string, including the NULL terminator.</span></span>                        |
| <span data-ttu-id="b3162-137">**type**</span><span class="sxs-lookup"><span data-stu-id="b3162-137">**type**</span></span>   | <span data-ttu-id="b3162-138">Тип данных значений в массиве, на который указывает элемент данных значения.</span><span class="sxs-lookup"><span data-stu-id="b3162-138">The data type of the values in the array pointed to by the value data member.</span></span> <span data-ttu-id="b3162-139">Константы (Пропертитагтипебите, ПропертитагтипеасЦии и Like), которые представляют различные типы данных, описаны в [**константах типа тега свойства Image**](-gdiplus-constant-image-property-tag-type-constants.md).</span><span class="sxs-lookup"><span data-stu-id="b3162-139">Constants (PropertyTagTypeByte, PropertyTagTypeASCII, and the like) that represent various data types are described in [**Image Property Tag Type Constants**](-gdiplus-constant-image-property-tag-type-constants.md).</span></span> |
| <span data-ttu-id="b3162-140">**value**</span><span class="sxs-lookup"><span data-stu-id="b3162-140">**value**</span></span>  | <span data-ttu-id="b3162-141">Указатель на массив значений.</span><span class="sxs-lookup"><span data-stu-id="b3162-141">A pointer to an array of values.</span></span>                                                                                                                                                                                                                                                                       |



 

<span data-ttu-id="b3162-142">Следующее консольное приложение считывает и отображает семь элементов метаданных в файле FakePhoto.jpg.</span><span class="sxs-lookup"><span data-stu-id="b3162-142">The following console application reads and displays the seven pieces of metadata in the file FakePhoto.jpg.</span></span> <span data-ttu-id="b3162-143">Функция Main зависит от вспомогательной функции Пропертитипефромворд, которая показана после функции Main.</span><span class="sxs-lookup"><span data-stu-id="b3162-143">The main function relies on the helper function PropertyTypeFromWORD, which is shown following the main function.</span></span>


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



<span data-ttu-id="b3162-144">Предыдущее консольное приложение выдает следующие выходные данные:</span><span class="sxs-lookup"><span data-stu-id="b3162-144">The preceding console application produces the following output:</span></span>


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



<span data-ttu-id="b3162-145">Приведенные выше выходные данные показывают шестнадцатеричный ИДЕНТИФИКАЦИОНный номер для каждого элемента свойства.</span><span class="sxs-lookup"><span data-stu-id="b3162-145">The preceding output shows a hexadecimal ID number for each property item.</span></span> <span data-ttu-id="b3162-146">Вы можете найти эти номера в [константах тегов свойств Image](-gdiplus-constant-image-property-tag-constants.md) и выяснить, что они представляют следующие теги свойств.</span><span class="sxs-lookup"><span data-stu-id="b3162-146">You can look up those ID numbers in [Image Property Tag Constants](-gdiplus-constant-image-property-tag-constants.md) and find out that they represent the following property tags.</span></span>



| <span data-ttu-id="b3162-147">Шестнадцатеричное значение</span><span class="sxs-lookup"><span data-stu-id="b3162-147">Hexadecimal value</span></span>                                                                                                       | <span data-ttu-id="b3162-148">Тег свойства</span><span class="sxs-lookup"><span data-stu-id="b3162-148">Property tag</span></span>                                                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3162-149">0x0320 0x010f</span><span class="sxs-lookup"><span data-stu-id="b3162-149">0x0320 0x010f</span></span><br/>  <span data-ttu-id="b3162-150">0x0110</span><span class="sxs-lookup"><span data-stu-id="b3162-150">0x0110</span></span><br/>  <span data-ttu-id="b3162-151">0x9003</span><span class="sxs-lookup"><span data-stu-id="b3162-151">0x9003</span></span><br/>  <span data-ttu-id="b3162-152">0x829a</span><span class="sxs-lookup"><span data-stu-id="b3162-152">0x829a</span></span><br/>  <span data-ttu-id="b3162-153">0x5090</span><span class="sxs-lookup"><span data-stu-id="b3162-153">0x5090</span></span><br/>  <span data-ttu-id="b3162-154">0x5091</span><span class="sxs-lookup"><span data-stu-id="b3162-154">0x5091</span></span><br/> | <span data-ttu-id="b3162-155">Пропертитагимажетитле Пропертитажекуипмаке</span><span class="sxs-lookup"><span data-stu-id="b3162-155">PropertyTagImageTitle PropertyTagEquipMake</span></span><br/>  <span data-ttu-id="b3162-156">пропертитажекуипмодел</span><span class="sxs-lookup"><span data-stu-id="b3162-156">PropertyTagEquipModel</span></span><br/>  <span data-ttu-id="b3162-157">пропертитажексифдторигинал</span><span class="sxs-lookup"><span data-stu-id="b3162-157">PropertyTagExifDTOriginal</span></span><br/>  <span data-ttu-id="b3162-158">пропертитажексифекспосуретиме</span><span class="sxs-lookup"><span data-stu-id="b3162-158">PropertyTagExifExposureTime</span></span><br/>  <span data-ttu-id="b3162-159">пропертитаглуминанцетабле</span><span class="sxs-lookup"><span data-stu-id="b3162-159">PropertyTagLuminanceTable</span></span><br/>  <span data-ttu-id="b3162-160">пропертитагчроминанцетабле</span><span class="sxs-lookup"><span data-stu-id="b3162-160">PropertyTagChrominanceTable</span></span><br/> |



 

<span data-ttu-id="b3162-161">Второй элемент свойства (index 1) в списке имеет **идентификатор** пропертитажекуипмаке и **тип** пропертитагтипеасЦии.</span><span class="sxs-lookup"><span data-stu-id="b3162-161">The second (index 1) property item in the list has **id** PropertyTagEquipMake and **type** PropertyTagTypeASCII.</span></span> <span data-ttu-id="b3162-162">В следующем примере, который является продолжением предыдущего консольного приложения, отображается значение этого элемента свойства:</span><span class="sxs-lookup"><span data-stu-id="b3162-162">The following example, which is a continuation of the previous console application, displays the value of that property item:</span></span>


```
printf("The equipment make is %s.\n", pPropBuffer[1].value);
```



<span data-ttu-id="b3162-163">Приведенная выше строка кода выдает следующие выходные данные:</span><span class="sxs-lookup"><span data-stu-id="b3162-163">The preceding line of code produces the following output:</span></span>


```
The equipment make is Northwind Traders.
```



<span data-ttu-id="b3162-164">Пятый элемент свойства (index 4) в списке имеет **идентификатор** пропертитажексифекспосуретиме и **тип** пропертитагтиператионал.</span><span class="sxs-lookup"><span data-stu-id="b3162-164">The fifth (index 4) property item in the list has **id** PropertyTagExifExposureTime and **type** PropertyTagTypeRational.</span></span> <span data-ttu-id="b3162-165">Этот тип данных (Пропертитагтиператионал) представляет собой пару **Long** s.</span><span class="sxs-lookup"><span data-stu-id="b3162-165">That data type (PropertyTagTypeRational) is a pair of **LONG** s.</span></span> <span data-ttu-id="b3162-166">В следующем примере, который является продолжением предыдущего консольного приложения, выводит эти два значения **Long** в виде дробной части.</span><span class="sxs-lookup"><span data-stu-id="b3162-166">The following example, which is a continuation of the previous console application, displays those two **LONG** values as a fraction.</span></span> <span data-ttu-id="b3162-167">Эта дробь, 1/125, является временем выдержки, измеряемым в секундах.</span><span class="sxs-lookup"><span data-stu-id="b3162-167">That fraction, 1/125, is the exposure time measured in seconds.</span></span>


```
long* ptrLong = (long*)(pPropBuffer[4].value);
printf("The exposure time is %d/%d.\n", ptrLong[0], ptrLong[1]);
```



<span data-ttu-id="b3162-168">Предыдущий код представит следующий вывод.</span><span class="sxs-lookup"><span data-stu-id="b3162-168">The preceding code produces the following output:</span></span>


```
The exposure time is 1/125.
```



## <a name="writing-metadata-to-a-file"></a><span data-ttu-id="b3162-169">Запись метаданных в файл</span><span class="sxs-lookup"><span data-stu-id="b3162-169">Writing Metadata to a File</span></span>

<span data-ttu-id="b3162-170">Чтобы записать элемент метаданных в объект [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) , инициализируйте объект [**пропертитем**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) , а затем передайте адрес этого объекта **Пропертитем** в метод **сетпропертитем** объекта **Image** .</span><span class="sxs-lookup"><span data-stu-id="b3162-170">To write an item of metadata to an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object, initialize a [**PropertyItem**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) object and then pass the address of that **PropertyItem** object to the **SetPropertyItem** method of the **Image** object.</span></span>

<span data-ttu-id="b3162-171">Следующее консольное приложение записывает один элемент (заголовок образа) метаданных в объект [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) , а затем сохраняет изображение в файл на диске FakePhoto2.jpg.</span><span class="sxs-lookup"><span data-stu-id="b3162-171">The following console application writes one item (the image title) of metadata to an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object and then saves the image in the disk file FakePhoto2.jpg.</span></span> <span data-ttu-id="b3162-172">Функция Main зависит от вспомогательной функции Жетенкодерклсид, которая показана в разделе [Получение идентификатора класса для кодировщика](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md).</span><span class="sxs-lookup"><span data-stu-id="b3162-172">The main function relies on the helper function GetEncoderClsid, which is shown in the topic [Retrieving the Class Identifier for an Encoder](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md).</span></span>


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



 

 
