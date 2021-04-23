---
description: Гуиднамес — это глобальный массив в библиотеке базовых классов DirectShow, который содержит строки, представляющие идентификаторы GUID, определенные в UUID. h. Этот массив полезен для создания выходных данных отладки.
ms.assetid: 6d72ad1e-588a-4a82-a1c1-e1e7b49df572
title: Гуиднамес (Вксдебуг. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GuidNames
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 359294d0cf3ab4e2074db5935cbbd604dcc1b250
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675513"
---
# <a name="guidnames"></a><span data-ttu-id="6330c-104">гуиднамес</span><span class="sxs-lookup"><span data-stu-id="6330c-104">GuidNames</span></span>

<span data-ttu-id="6330c-105">`GuidNames` является глобальным массивом в библиотеке базовых классов DirectShow, который содержит строки, представляющие идентификаторы GUID, определенные в UUID. h.</span><span class="sxs-lookup"><span data-stu-id="6330c-105">`GuidNames` is a global array in the DirectShow base class library that contains strings representing the GUIDs defined in Uuids.h.</span></span> <span data-ttu-id="6330c-106">Этот массив полезен для создания выходных данных отладки.</span><span class="sxs-lookup"><span data-stu-id="6330c-106">This array is useful for generating debug output.</span></span>

``` syntax
char* GuidNames[guid]
```

## <a name="parameters"></a><span data-ttu-id="6330c-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="6330c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6330c-108"><span id="guid"></span><span id="GUID"></span>*устройства*</span><span class="sxs-lookup"><span data-stu-id="6330c-108"><span id="guid"></span><span id="GUID"></span>*guid*</span></span>
</dt> <dd>

<span data-ttu-id="6330c-109">Указывает любое значение GUID, определенное в файле заголовков UUID. h.</span><span class="sxs-lookup"><span data-stu-id="6330c-109">Specifies any GUID value defined in the header file Uuids.h.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6330c-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6330c-110">Remarks</span></span>

<span data-ttu-id="6330c-111">Используйте этот глобальный массив для вывода констант GUID в виде строк.</span><span class="sxs-lookup"><span data-stu-id="6330c-111">Use this global array to output GUID constants as strings.</span></span> <span data-ttu-id="6330c-112">Например, следующий код выводит строку "MEDIATYPE \_ Video" в консоль:</span><span class="sxs-lookup"><span data-stu-id="6330c-112">For example, the following code prints the string "MEDIATYPE\_Video" to the console:</span></span>


```C++
puts(GuidNames[MEDIATYPE_Video]);
```



<span data-ttu-id="6330c-113">Если идентификатор GUID не совпадает, возвращается строка "неизвестное имя GUID".</span><span class="sxs-lookup"><span data-stu-id="6330c-113">If the GUID is not matched, the string "Unknown GUID Name" is returned.</span></span> <span data-ttu-id="6330c-114">Не все идентификаторы GUID DirectShow определены в UUID. h.</span><span class="sxs-lookup"><span data-stu-id="6330c-114">Not all DirectShow GUIDs are defined in uuids.h.</span></span>

## <a name="requirements"></a><span data-ttu-id="6330c-115">Требования</span><span class="sxs-lookup"><span data-stu-id="6330c-115">Requirements</span></span>



| <span data-ttu-id="6330c-116">Требование</span><span class="sxs-lookup"><span data-stu-id="6330c-116">Requirement</span></span> | <span data-ttu-id="6330c-117">Значение</span><span class="sxs-lookup"><span data-stu-id="6330c-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6330c-118">Header</span><span class="sxs-lookup"><span data-stu-id="6330c-118">Header</span></span><br/>  | <dl> <span data-ttu-id="6330c-119"><dt>Вксдебуг. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6330c-119"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="6330c-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="6330c-120">Library</span></span><br/> | <dl> <span data-ttu-id="6330c-121"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="6330c-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6330c-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6330c-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6330c-123">Выходные функции отладки</span><span class="sxs-lookup"><span data-stu-id="6330c-123">Debug Output Functions</span></span>](debug-output-functions.md)
</dt> </dl>

 

 




