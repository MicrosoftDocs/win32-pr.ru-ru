---
description: Следующее консольное приложение перечисляет все параметры, поддерживаемые различными кодировщиками, установленными на компьютере.
ms.assetid: c80ad013-0b92-461f-8714-4b6d0cb6de0d
title: Вывод списка параметров и значений для всех кодировщиков
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fdaf522193f1074a28fe9f5ebb8a7afc2bade0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997246"
---
# <a name="listing-parameters-and-values-for-all-encoders"></a>Вывод списка параметров и значений для всех кодировщиков

Следующее консольное приложение перечисляет все параметры, поддерживаемые различными кодировщиками, установленными на компьютере. Функция Main вызывает [**жетимажеенкодерс**](/windows/desktop/api/Gdiplusimagecodec/nf-gdiplusimagecodec-getimageencoders) , чтобы определить, какие Кодировщики доступны. Для каждого доступного кодировщика функция Main вызывает вспомогательную функцию Шовалленкодерпараметерс.

Функция Шовалленкодерпараметерс вызывает метод [**Image:: жетенкодерпараметерлист**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getencoderparameterlist) , чтобы определить, какие параметры поддерживаются данным кодировщиком. Для каждого поддерживаемого параметра Функция перечисляет категорию, тип данных и количество значений. Функция Шовалленкодерпараметерс основана на двух вспомогательных функциях: Енкодерпараметеркатегорифромгуид и Валуетипефромулонг.


```
#include <windows.h>
#include <gdiplus.h>
#include <strsafe.h>
using namespace Gdiplus;

// Helper functions
void ShowAllEncoderParameters(ImageCodecInfo*);
HRESULT EncoderParameterCategoryFromGUID(GUID guid, WCHAR* category, UINT maxChars);
HRESULT ValueTypeFromULONG(ULONG index, WCHAR* strValueType, UINT maxChars);

INT main()
{
   // Initialize GDI+
   GdiplusStartupInput gdiplusStartupInput;
   ULONG_PTR gdiplusToken;
   GdiplusStartup(&gdiplusToken, &gdiplusStartupInput, NULL);

   UINT  num;        // Number of image encoders
   UINT  size;       // Size of the image encoder array in bytes

   ImageCodecInfo* pImageCodecInfo;

   // How many encoders are there?
   // How big (in bytes) is the array of all ImageCodecInfo objects?
   GetImageEncodersSize(&num, &size);

   // Create a buffer large enough to hold the array of ImageCodecInfo
   // objects that will be returned by GetImageEncoders.
   pImageCodecInfo = (ImageCodecInfo*)(malloc(size));

   // GetImageEncoders creates an array of ImageCodecInfo objects
   // and copies that array into a previously allocated buffer. 
   // The third argument, imageCodecInfos, is a pointer to that buffer. 
   GetImageEncoders(num, size, pImageCodecInfo);
    
   // For each ImageCodecInfo object in the array, show all parameters.
   for(UINT j = 0; j < num; ++j)
   { 
      ShowAllEncoderParameters(&(pImageCodecInfo[j]));
   }

   GdiplusShutdown(gdiplusToken);
   return 0;
}


/////////////////////////////////////////////////
// Helper functions

VOID ShowAllEncoderParameters(ImageCodecInfo* pImageCodecInfo)
{
   CONST MAX_CATEGORY_LENGTH = 50;
   CONST MAX_VALUE_TYPE_LENGTH = 50;
   WCHAR strParameterCategory[MAX_CATEGORY_LENGTH] = L"";
   WCHAR strValueType[MAX_VALUE_TYPE_LENGTH] = L"";

   wprintf(L"\n\n%s\n", pImageCodecInfo->MimeType);

   // Create a Bitmap (inherited from Image) object so that we can call
   // GetParameterListSize and GetParameterList.
   Bitmap bitmap(1, 1);

   // How big (in bytes) is the encoder's parameter list?
   UINT listSize = 0; 
   listSize = bitmap.GetEncoderParameterListSize(&pImageCodecInfo->Clsid);
   printf("  The parameter list requires %d bytes.\n", listSize);

   if(listSize == 0)
      return;

   // Allocate a buffer large enough to hold the parameter list.
   EncoderParameters* pEncoderParameters = NULL;
   pEncoderParameters = (EncoderParameters*)malloc(listSize);

   if(pEncoderParameters == NULL)
      return;

   // Get the parameter list for the encoder.
   bitmap.GetEncoderParameterList(
      &pImageCodecInfo->Clsid, listSize, pEncoderParameters);

   // pEncoderParameters points to an EncoderParameters object, which
   // has a Count member and an array of EncoderParameter objects.
   // How many EncoderParameter objects are in the array?
   printf("  There are %d EncoderParameter objects in the array.\n", 
      pEncoderParameters->Count);

   // For each EncoderParameter object in the array, list the
   // parameter category, data type, and number of values.
   for(UINT k = 0; k < pEncoderParameters->Count; ++k)
   {
      EncoderParameterCategoryFromGUID(
         pEncoderParameters->Parameter[k].Guid, strParameterCategory, MAX_CATEGORY_LENGTH);

      ValueTypeFromULONG(
         pEncoderParameters->Parameter[k].Type, strValueType, MAX_VALUE_TYPE_LENGTH);

      printf("    Parameter[%d]\n", k);
      wprintf(L"      The category is %s.\n", strParameterCategory);
      wprintf(L"      The data type is %s.\n", strValueType);

      printf("      The number of values is %d.\n",
      pEncoderParameters->Parameter[k].NumberOfValues); 
   } // for

   free(pEncoderParameters);
} // ShowAllEncoderParameters


HRESULT EncoderParameterCategoryFromGUID(GUID guid, WCHAR* category, UINT maxChars)
{
   HRESULT hr = E_FAIL;

   if(guid == EncoderCompression)
      hr = StringCchCopyW(category, maxChars, L"Compression");
   else if(guid == EncoderColorDepth)
      hr = StringCchCopyW(category, maxChars, L"ColorDepth");
   else if(guid == EncoderScanMethod)
      hr = StringCchCopyW(category, maxChars, L"ScanMethod");
   else if(guid == EncoderVersion)
      hr = StringCchCopyW(category, maxChars, L"Version");
   else if(guid == EncoderRenderMethod)
      hr = StringCchCopyW(category, maxChars, L"RenderMethod");
   else if(guid == EncoderQuality)
      hr = StringCchCopyW(category, maxChars, L"Quality");
   else if(guid == EncoderTransformation)
      hr = StringCchCopyW(category, maxChars, L"Transformation");
   else if(guid == EncoderLuminanceTable)
      hr = StringCchCopyW(category, maxChars, L"LuminanceTable");
   else if(guid == EncoderChrominanceTable)
      hr = StringCchCopyW(category, maxChars, L"ChrominanceTable");
   else if(guid == EncoderSaveFlag)
      hr = StringCchCopyW(category, maxChars, L"SaveFlag");
   else
      hr = StringCchCopyW(category, maxChars, L"Unknown category");

   return hr;
} // EncoderParameterCategoryFromGUID


HRESULT ValueTypeFromULONG(ULONG index, WCHAR* strValueType, UINT maxChars)
{
   HRESULT hr = E_FAIL;

   WCHAR* valueTypes[] = {
      L"Nothing",                  // 0
      L"ValueTypeByte",            // 1
      L"ValueTypeASCII",           // 2
      L"ValueTypeShort",           // 3
      L"ValueTypeLong",            // 4
      L"ValueTypeRational",        // 5
      L"ValueTypeLongRange",       // 6
      L"ValueTypeUndefined",       // 7
      L"ValueTypeRationalRange"};  // 8

   hr = StringCchCopyW(strValueType, maxChars, valueTypes[index]);
   return hr;

} // ValueTypeFromULONG
```



При запуске предыдущего консольного приложения вы получаете выходные данные, аналогичные приведенным ниже.


```
image/bmp
  The parameter list requires 0 bytes.

image/jpeg
  The parameter list requires 172 bytes.
  There are 4 EncoderParameter objects in the array.
    Parameter[0]
      The category is Transformation.
      The data type is Long.
      The number of values is 5.
    Parameter[1]
      The category is Quality.
      The data type is LongRange.
      The number of values is 1.
    Parameter[2]
      The category is LuminanceTable.
      The data type is Short.
      The number of values is 0.
    Parameter[3]
      The category is ChrominanceTable.
      The data type is Short.
      The number of values is 0.

image/gif
  The parameter list requires 0 bytes.

image/tiff
  The parameter list requires 160 bytes.
  There are 3 EncoderParameter objects in the array.
    Parameter[0]
      The category is Compression.
      The data type is Long.
      The number of values is 5.
    Parameter[1]
      The category is ColorDepth.
      The data type is Long.
      The number of values is 5.
    Parameter[2]
      The category is SaveFlag.
      The data type is Long.
      The number of values is 1.

image/png
  The parameter list requires 0 bytes.
```



Вы можете нарисовать следующие выводы, изучив приведенные выше выходные данные программы:

-   Кодировщик JPEG поддерживает категории параметров преобразования, качества, Луминанцетабле и Чроминанцетабле.
-   Кодировщик TIFF поддерживает категории параметров compression, Clientareawidth и Савефлаг.

Можно также увидеть количество допустимых значений для каждой категории параметров. Например, можно увидеть, что категория параметра Clientareawidth (кодек TIFF) имеет пять значений типа **ulong**. В следующем коде перечислены эти пять значений. Предположим, что **пенкодерпараметерс** является указателем на объект [**EncoderParameters**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameters) , представляющий кодировщик TIFF.


```
ULONG* pUlong = (ULONG*)(pEncoderParameters->Parameter[1].Value);
ULONG numVals = pEncoderParameters->Parameter[1].NumberOfValues;
printf("\nThe allowable values for ColorDepth are\n");

for(ULONG k = 0; k < numVals; ++k)
{
   printf("  %u\n", pUlong[k]);
}
            
```



Предыдущий код представит следующий вывод.


```
The allowable values for ColorDepth are
  1
  4
  8
  24
  32
            
```



> [!Note]  
> В некоторых случаях значения в объекте [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) являются числовыми значениями элементов перечисления [**енкодервалуе**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-encodervalue) . Однако числа в приведенном выше списке не связаны с перечислением **енкодервалуе** . Числа означают 1 бит на пиксель, 2 бита на пиксель и т. д.

 

Если вы напишете код, аналогичный приведенному в предыдущем примере, чтобы исследовать допустимые значения для других категорий параметров, вы получите результат, аналогичный приведенному ниже.



| Параметр кодировщика JPEG | Допустимые значения                                                                                                                                                                                                 |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Преобразование         | EncoderValueTransformRotate90 EncoderValueTransformRotate180<br/>  EncoderValueTransformRotate270<br/>  енкодервалуетрансформфлифоризонтал<br/>  енкодервалуетрансформфлипвертикал<br/> |
| Качество                | от 0 до 100                                                                                                                                                                                                    |



 



| Параметр кодировщика TIFF | Допустимые значения                                                                                                                                                                             |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Сжатие            | Енкодервалуекомпрессионлзв EncoderValueCompressionCCITT3<br/>  EncoderValueCompressionCCITT4<br/>  енкодервалуекомпрессионрле<br/>  енкодервалуекомпрессионноне<br/> |
| Clientareawidth             | 1, 4, 8, 24, 32                                                                                                                                                                              |
| савефлаг               | енкодервалуемултифраме                                                                                                                                                                       |



 

> [!Note]  
> Если ширина и высота изображения JPEG кратны 16, можно применить любые преобразования, разрешенные категорией параметра Енкодертрансформатион (например, поворот на 90 градусов) без потери информации.

 

 

 
