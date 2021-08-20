---
description: 'Класс Image предоставляет метод Image:: Жетенкодерпараметерлист, позволяющий определить параметры, которые поддерживаются заданным кодировщиком изображения.'
ms.assetid: 2e1a5279-dd9d-46de-822c-d356a344f340
title: Определение параметров, поддерживаемых кодировщиком
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c842b14a2d14af578eede428e79018a2d266ea6133ed61a9bd0736e8dadc97e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118977574"
---
# <a name="determining-the-parameters-supported-by-an-encoder"></a>Определение параметров, поддерживаемых кодировщиком

Класс [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) предоставляет метод [**Image:: жетенкодерпараметерлист**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getencoderparameterlist) , позволяющий определить параметры, которые поддерживаются заданным кодировщиком изображения. Метод **Image:: жетенкодерпараметерлист** возвращает массив объектов [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) . Необходимо выделить буфер для получения этого массива перед вызовом **Image:: жетенкодерпараметерлист**. Чтобы определить размер требуемого буфера, можно вызвать [**Image:: жетенкодерпараметерлистсизе**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getencoderparameterlistsize) .

Следующее консольное приложение получает список параметров для кодировщика JPEG. Функция Main зависит от вспомогательной функции Жетенкодерклсид, которая показана в статье [Получение идентификатора класса для кодировщика](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md).


```
#include <windows.h>
#include <gdiplus.h>
#include <stdio.h>
using namespace Gdiplus;

INT GetEncoderClsid(const WCHAR* format, CLSID* pClsid);  // helper function

INT main()
{
   // Initialize GDI+.
   GdiplusStartupInput gdiplusStartupInput;
   ULONG_PTR gdiplusToken;
   GdiplusStartup(&gdiplusToken, &gdiplusStartupInput, NULL);

   // Create Bitmap (inherited from Image) object so that we can call
   // GetParameterListSize and GetParameterList.
   Bitmap* bitmap = new Bitmap(1, 1);

   // Get the JPEG encoder CLSID.
   CLSID encoderClsid;
   GetEncoderClsid(L"image/jpeg", &encoderClsid);

   // How big (in bytes) is the JPEG encoder's parameter list?
   UINT listSize = 0; 
   listSize = bitmap->GetEncoderParameterListSize(&encoderClsid);
   printf("The parameter list requires %d bytes.\n", listSize);

   // Allocate a buffer large enough to hold the parameter list.
   EncoderParameters* pEncoderParameters = NULL;
   pEncoderParameters = (EncoderParameters*)malloc(listSize);

   // Get the parameter list for the JPEG encoder.
   bitmap->GetEncoderParameterList(
      &encoderClsid, listSize, pEncoderParameters);

   // pEncoderParameters points to an EncoderParameters object, which
   // has a Count member and an array of EncoderParameter objects.
   // How many EncoderParameter objects are in the array?
   printf("There are %d EncoderParameter objects in the array.\n", 
      pEncoderParameters->Count);

   free(pEncoderParameters);
   delete(bitmap);
   GdiplusShutdown(gdiplusToken);
   return 0;
}
```



При запуске предыдущего консольного приложения вы получаете выходные данные, аналогичные приведенным ниже.


```
The parameter list requires 172 bytes.
There are 4 EncoderParameter objects in the array.
```



Каждый из объектов [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) в массиве имеет следующие четыре открытых элемента данных:

Следующий код является продолжением консольного приложения, показанного в предыдущем примере. Код просматривает второй объект [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) в массиве, возвращаемом [**Image:: жетенкодерпараметерлист**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getencoderparameterlist). Код вызывает [StringFromGUID2](/windows/win32/api/combaseapi/nf-combaseapi-stringfromguid2), который является системной функцией, объявленной в обжбасе. h, для преобразования элемента **GUID** объекта **EncoderParameter** в строку.


```
// Look at the second (index 1) EncoderParameter object in the array.
printf("Parameter[1]\n");

WCHAR strGuid[39];
StringFromGUID2(pEncoderParameters->Parameter[1].Guid, strGuid, 39);
wprintf(L"   The GUID is %s.\n", strGuid);

printf("   The value type is %d.\n", 
   pEncoderParameters->Parameter[1].Type);

printf("   The number of values is %d.\n",
   pEncoderParameters->Parameter[1].NumberOfValues);
```



Предыдущий код представит следующий вывод.


```
Parameter[1]
   The GUID is {1D5BE4B5-FA4A-452D-9CDD-5DB35105E7EB}.
   The value type is 6.
   The number of values is 1.
```



Можно найти идентификатор GUID в Гдиплусимагинг. h и выяснить, что категория этого объекта [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) — енкодеркуалити. Эту категорию (Енкодеркуалити) параметра можно использовать для установки уровня сжатия изображения JPEG.

В Гдиплусенумс. h перечисление [**EncoderParameterValueType**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-encoderparametervaluetype) указывает, что тип данных 6 — **валуелонгранже**. Диапазон типа long — это пара значений **ulong** .

Число значений равно единице, поэтому мы понимаем, что элемент **value** объекта [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) является указателем на массив, содержащий один элемент. Один элемент является парой значений **ulong** .

Следующий код является продолжением консольного приложения, которое показано в двух предыдущих примерах. Код определяет тип данных с именем **плонгранже** (указатель на длинный диапазон). Переменная типа **плонгранже** используется для извлечения минимального и максимального значений, которые можно передать в качестве параметра качества кодировщику JPEG.


```
typedef struct
   {
      long min;
      long max;
   }* PLONGRANGE;

   PLONGRANGE pLongRange = 
      (PLONGRANGE)(pEncoderParameters->Parameter[1].Value);

   printf("   The minimum possible quality value is %d.\n",
      pLongRange->min);

   printf("   The maximum possible quality value is %d.\n",
      pLongRange->max);
```



Предыдущий код представит следующий вывод.


```
The minimum possible quality value is 0.
The maximum possible quality value is 100.
```



В предыдущем примере значение, возвращенное в объекте [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) , является парой значений **ulong** , указывающих минимальное и максимальное значения для параметра Quality. В некоторых случаях значения, возвращаемые в объекте **EncoderParameter** , являются членами перечисления [**енкодервалуе**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-encodervalue) . В следующих разделах описывается перечисление **енкодервалуе** и методы для перечисления возможных значений параметров в более подробностях.

-   [Использование перечисления Енкодервалуе](-gdiplus-using-the-encodervalue-enumeration-use.md)
-   [Вывод списка параметров и значений для всех кодировщиков](-gdiplus-listing-parameters-and-values-for-all-encoders-use.md)

 

 
