---
description: Макрос NAME создает строку только для отладки.
ms.assetid: 5cb9f803-dd2b-4055-bdcc-e754ef5fa505
title: ИМЯ (Вксдебуг. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NAME
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0b698551789deb0c3775bd4ac722136e1abc9d38
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105688832"
---
# <a name="name"></a><span data-ttu-id="427f8-103">ИМЯ</span><span class="sxs-lookup"><span data-stu-id="427f8-103">NAME</span></span>

<span data-ttu-id="427f8-104">Макрос **Name** создает строку только для отладки.</span><span class="sxs-lookup"><span data-stu-id="427f8-104">The **NAME** macro generates a debug-only string.</span></span>

``` syntax
NAME(strLiteral);
```

## <a name="parameters"></a><span data-ttu-id="427f8-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="427f8-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="427f8-106"><span id="strLiteral"></span><span id="strliteral"></span><span id="STRLITERAL"></span>*стрлитерал*</span><span class="sxs-lookup"><span data-stu-id="427f8-106"><span id="strLiteral"></span><span id="strliteral"></span><span id="STRLITERAL"></span>*strLiteral*</span></span>
</dt> <dd>

<span data-ttu-id="427f8-107">Текстовая строка.</span><span class="sxs-lookup"><span data-stu-id="427f8-107">Text string.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="427f8-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="427f8-108">Remarks</span></span>

<span data-ttu-id="427f8-109">В отладочных сборках этот макрос эквивалентен **текстовому** макросу.</span><span class="sxs-lookup"><span data-stu-id="427f8-109">In debug builds, this macro is equivalent to the **TEXT** macro.</span></span> <span data-ttu-id="427f8-110">В розничных сборках она разрешается в (TCHAR \* ) **null**.</span><span class="sxs-lookup"><span data-stu-id="427f8-110">In retail builds, it resolves to (TCHAR\*) **NULL**.</span></span> <span data-ttu-id="427f8-111">Этот макрос полезен при объявлении имени объекта, производного от класса [**кбасеобжект**](cbaseobject.md) .</span><span class="sxs-lookup"><span data-stu-id="427f8-111">This macro is useful when declaring the name of an object that derives from the [**CBaseObject**](cbaseobject.md) class.</span></span>


```C++
pObject = new CBaseObject(NAME("My Object"));
```



## <a name="requirements"></a><span data-ttu-id="427f8-112">Требования</span><span class="sxs-lookup"><span data-stu-id="427f8-112">Requirements</span></span>



| <span data-ttu-id="427f8-113">Требование</span><span class="sxs-lookup"><span data-stu-id="427f8-113">Requirement</span></span> | <span data-ttu-id="427f8-114">Значение</span><span class="sxs-lookup"><span data-stu-id="427f8-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="427f8-115">Header</span><span class="sxs-lookup"><span data-stu-id="427f8-115">Header</span></span><br/>  | <dl> <span data-ttu-id="427f8-116"><dt>Вксдебуг. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="427f8-116"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="427f8-117">Библиотека</span><span class="sxs-lookup"><span data-stu-id="427f8-117">Library</span></span><br/> | <dl> <span data-ttu-id="427f8-118"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="427f8-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="427f8-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="427f8-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="427f8-120">Выходные функции отладки</span><span class="sxs-lookup"><span data-stu-id="427f8-120">Debug Output Functions</span></span>](debug-output-functions.md)
</dt> </dl>

 

 




