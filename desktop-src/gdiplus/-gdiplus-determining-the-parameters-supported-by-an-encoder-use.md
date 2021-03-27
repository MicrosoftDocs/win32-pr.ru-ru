---
description: 'Класс Image предоставляет метод Image:: Жетенкодерпараметерлист, позволяющий определить параметры, которые поддерживаются заданным кодировщиком изображения.'
ms.assetid: 2e1a5279-dd9d-46de-822c-d356a344f340
title: Определение параметров, поддерживаемых кодировщиком
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad9bd76abb0b9f01bf55fd738df77cd086bc757c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997507"
---
# <a name="determining-the-parameters-supported-by-an-encoder"></a><span data-ttu-id="571c6-103">Определение параметров, поддерживаемых кодировщиком</span><span class="sxs-lookup"><span data-stu-id="571c6-103">Determining the Parameters Supported by an Encoder</span></span>

<span data-ttu-id="571c6-104">Класс [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) предоставляет метод [**Image:: жетенкодерпараметерлист**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getencoderparameterlist) , позволяющий определить параметры, которые поддерживаются заданным кодировщиком изображения.</span><span class="sxs-lookup"><span data-stu-id="571c6-104">The [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) class provides the [**Image::GetEncoderParameterList**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getencoderparameterlist) method so that you can determine the parameters that are supported by a given image encoder.</span></span> <span data-ttu-id="571c6-105">Метод **Image:: жетенкодерпараметерлист** возвращает массив объектов [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) .</span><span class="sxs-lookup"><span data-stu-id="571c6-105">The **Image::GetEncoderParameterList** method returns an array of [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) objects.</span></span> <span data-ttu-id="571c6-106">Необходимо выделить буфер для получения этого массива перед вызовом **Image:: жетенкодерпараметерлист**.</span><span class="sxs-lookup"><span data-stu-id="571c6-106">You must allocate a buffer to receive that array before you call **Image::GetEncoderParameterList**.</span></span> <span data-ttu-id="571c6-107">Чтобы определить размер требуемого буфера, можно вызвать [**Image:: жетенкодерпараметерлистсизе**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getencoderparameterlistsize) .</span><span class="sxs-lookup"><span data-stu-id="571c6-107">You can call [**Image::GetEncoderParameterListSize**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getencoderparameterlistsize) to determine the size of the required buffer.</span></span>

<span data-ttu-id="571c6-108">Следующее консольное приложение получает список параметров для кодировщика JPEG.</span><span class="sxs-lookup"><span data-stu-id="571c6-108">The following console application obtains the parameter list for the JPEG encoder.</span></span> <span data-ttu-id="571c6-109">Функция Main зависит от вспомогательной функции Жетенкодерклсид, которая показана в статье [Получение идентификатора класса для кодировщика](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md).</span><span class="sxs-lookup"><span data-stu-id="571c6-109">The main function relies on the helper function GetEncoderClsid, which is shown in [Retrieving the Class Identifier for an Encoder](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md).</span></span>


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



<span data-ttu-id="571c6-110">При запуске предыдущего консольного приложения вы получаете выходные данные, аналогичные приведенным ниже.</span><span class="sxs-lookup"><span data-stu-id="571c6-110">When you run the preceding console application, you get an output similar to the following:</span></span>


```
The parameter list requires 172 bytes.
There are 4 EncoderParameter objects in the array.
```



<span data-ttu-id="571c6-111">Каждый из объектов [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) в массиве имеет следующие четыре открытых элемента данных:</span><span class="sxs-lookup"><span data-stu-id="571c6-111">Each of the [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) objects in the array has the following four public data members:</span></span>

<span data-ttu-id="571c6-112">Следующий код является продолжением консольного приложения, показанного в предыдущем примере.</span><span class="sxs-lookup"><span data-stu-id="571c6-112">The following code is a continuation of the console application shown in the preceding example.</span></span> <span data-ttu-id="571c6-113">Код просматривает второй объект [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) в массиве, возвращаемом [**Image:: жетенкодерпараметерлист**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getencoderparameterlist).</span><span class="sxs-lookup"><span data-stu-id="571c6-113">The code looks at the second [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) object in the array returned by [**Image::GetEncoderParameterList**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getencoderparameterlist).</span></span> <span data-ttu-id="571c6-114">Код вызывает [StringFromGUID2](/windows/win32/api/combaseapi/nf-combaseapi-stringfromguid2), который является системной функцией, объявленной в обжбасе. h, для преобразования элемента **GUID** объекта **EncoderParameter** в строку.</span><span class="sxs-lookup"><span data-stu-id="571c6-114">The code calls [StringFromGUID2](/windows/win32/api/combaseapi/nf-combaseapi-stringfromguid2), which is a system function declared in Objbase.h, to convert the **Guid** member of the **EncoderParameter** object to a string.</span></span>


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



<span data-ttu-id="571c6-115">Предыдущий код представит следующий вывод.</span><span class="sxs-lookup"><span data-stu-id="571c6-115">The preceding code produces the following output:</span></span>


```
Parameter[1]
   The GUID is {1D5BE4B5-FA4A-452D-9CDD-5DB35105E7EB}.
   The value type is 6.
   The number of values is 1.
```



<span data-ttu-id="571c6-116">Можно найти идентификатор GUID в Гдиплусимагинг. h и выяснить, что категория этого объекта [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) — енкодеркуалити.</span><span class="sxs-lookup"><span data-stu-id="571c6-116">You can look up the GUID in Gdiplusimaging.h and find out that the category of this [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) object is EncoderQuality.</span></span> <span data-ttu-id="571c6-117">Эту категорию (Енкодеркуалити) параметра можно использовать для установки уровня сжатия изображения JPEG.</span><span class="sxs-lookup"><span data-stu-id="571c6-117">You can use this category (EncoderQuality) of parameter to set the compression level of a JPEG image.</span></span>

<span data-ttu-id="571c6-118">В Гдиплусенумс. h перечисление [**EncoderParameterValueType**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-encoderparametervaluetype) указывает, что тип данных 6 — **валуелонгранже**.</span><span class="sxs-lookup"><span data-stu-id="571c6-118">In Gdiplusenums.h, the [**EncoderParameterValueType**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-encoderparametervaluetype) enumeration indicates that data type 6 is **ValueLongRange**.</span></span> <span data-ttu-id="571c6-119">Диапазон типа long — это пара значений **ulong** .</span><span class="sxs-lookup"><span data-stu-id="571c6-119">A long range is a pair of **ULONG** values.</span></span>

<span data-ttu-id="571c6-120">Число значений равно единице, поэтому мы понимаем, что элемент **value** объекта [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) является указателем на массив, содержащий один элемент.</span><span class="sxs-lookup"><span data-stu-id="571c6-120">The number of values is one, so we know that the **Value** member of the [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) object is a pointer to an array that has one element.</span></span> <span data-ttu-id="571c6-121">Один элемент является парой значений **ulong** .</span><span class="sxs-lookup"><span data-stu-id="571c6-121">That one element is a pair of **ULONG** values.</span></span>

<span data-ttu-id="571c6-122">Следующий код является продолжением консольного приложения, которое показано в двух предыдущих примерах.</span><span class="sxs-lookup"><span data-stu-id="571c6-122">The following code is a continuation of the console application that is shown in the preceding two examples.</span></span> <span data-ttu-id="571c6-123">Код определяет тип данных с именем **плонгранже** (указатель на длинный диапазон).</span><span class="sxs-lookup"><span data-stu-id="571c6-123">The code defines a data type called **PLONGRANGE** (pointer to a long range).</span></span> <span data-ttu-id="571c6-124">Переменная типа **плонгранже** используется для извлечения минимального и максимального значений, которые можно передать в качестве параметра качества кодировщику JPEG.</span><span class="sxs-lookup"><span data-stu-id="571c6-124">A variable of type **PLONGRANGE** is used to extract the minimum and maximum values that can be passed as a quality setting to the JPEG encoder.</span></span>


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



<span data-ttu-id="571c6-125">Предыдущий код представит следующий вывод.</span><span class="sxs-lookup"><span data-stu-id="571c6-125">The preceding code produces the following output:</span></span>


```
The minimum possible quality value is 0.
The maximum possible quality value is 100.
```



<span data-ttu-id="571c6-126">В предыдущем примере значение, возвращенное в объекте [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) , является парой значений **ulong** , указывающих минимальное и максимальное значения для параметра Quality.</span><span class="sxs-lookup"><span data-stu-id="571c6-126">In the preceding example, the value returned in the [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) object is a pair of **ULONG** values that indicate the minimum and maximum possible values for the quality parameter.</span></span> <span data-ttu-id="571c6-127">В некоторых случаях значения, возвращаемые в объекте **EncoderParameter** , являются членами перечисления [**енкодервалуе**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-encodervalue) .</span><span class="sxs-lookup"><span data-stu-id="571c6-127">In some cases, the values returned in an **EncoderParameter** object are members of the [**EncoderValue**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-encodervalue) enumeration.</span></span> <span data-ttu-id="571c6-128">В следующих разделах описывается перечисление **енкодервалуе** и методы для перечисления возможных значений параметров в более подробностях.</span><span class="sxs-lookup"><span data-stu-id="571c6-128">The following topics discuss the **EncoderValue** enumeration and methods for listing possible parameter values in more detail:</span></span>

-   [<span data-ttu-id="571c6-129">Использование перечисления Енкодервалуе</span><span class="sxs-lookup"><span data-stu-id="571c6-129">Using the EncoderValue Enumeration</span></span>](-gdiplus-using-the-encodervalue-enumeration-use.md)
-   [<span data-ttu-id="571c6-130">Вывод списка параметров и значений для всех кодировщиков</span><span class="sxs-lookup"><span data-stu-id="571c6-130">Listing Parameters and Values for All Encoders</span></span>](-gdiplus-listing-parameters-and-values-for-all-encoders-use.md)

 

 
