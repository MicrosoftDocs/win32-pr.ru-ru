---
description: Функция Стрингфромресаурце загружает строку из файла ресурсов с заданным идентификатором ресурса.
ms.assetid: 26b40905-db16-46d1-8621-9aa8cb8e7232
title: Функция Стрингфромресаурце (Вксутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StringFromResource
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a9bb13944f281d528ff95a7856ebc8a0a2374c6e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679760"
---
# <a name="stringfromresource-function"></a><span data-ttu-id="20c54-103">Функция Стрингфромресаурце</span><span class="sxs-lookup"><span data-stu-id="20c54-103">StringFromResource function</span></span>

<span data-ttu-id="20c54-104">`StringFromResource`Функция загружает строку из файла ресурсов с заданным идентификатором ресурса.</span><span class="sxs-lookup"><span data-stu-id="20c54-104">The `StringFromResource` function loads a string from a resource file with the given resource identifier.</span></span>

## <a name="syntax"></a><span data-ttu-id="20c54-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="20c54-105">Syntax</span></span>


```C++
TCHAR* WINAPI StringFromResource(
   TCHAR *pBuffer,
   int   iResourceID
);
```



## <a name="parameters"></a><span data-ttu-id="20c54-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="20c54-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20c54-107">*pBuffer*</span><span class="sxs-lookup"><span data-stu-id="20c54-107">*pBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="20c54-108">Указатель на строку, соответствующую *иресаурцеид*.</span><span class="sxs-lookup"><span data-stu-id="20c54-108">Pointer to the string corresponding to *iResourceID*.</span></span>

</dd> <dt>

<span data-ttu-id="20c54-109">*иресаурцеид*</span><span class="sxs-lookup"><span data-stu-id="20c54-109">*iResourceID*</span></span> 
</dt> <dd>

<span data-ttu-id="20c54-110">Идентификатор ресурса извлекаемой строки.</span><span class="sxs-lookup"><span data-stu-id="20c54-110">Resource identifier of the string to retrieve.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20c54-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="20c54-111">Return value</span></span>

<span data-ttu-id="20c54-112">Возвращает ту же строку, что и *pBuffer*.</span><span class="sxs-lookup"><span data-stu-id="20c54-112">Returns the same string as *pBuffer*.</span></span> <span data-ttu-id="20c54-113">Если функция не выполнена успешно, возвращает пустую строку.</span><span class="sxs-lookup"><span data-stu-id="20c54-113">If the function is not successful, returns a null string.</span></span>

## <a name="remarks"></a><span data-ttu-id="20c54-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="20c54-114">Remarks</span></span>

<span data-ttu-id="20c54-115">Буфер *pBuffer* должен иметь длину не менее str \_ \_ байт.</span><span class="sxs-lookup"><span data-stu-id="20c54-115">The *pBuffer* buffer must be at least STR\_MAX\_LENGTH bytes.</span></span>

## <a name="requirements"></a><span data-ttu-id="20c54-116">Требования</span><span class="sxs-lookup"><span data-stu-id="20c54-116">Requirements</span></span>



| <span data-ttu-id="20c54-117">Требование</span><span class="sxs-lookup"><span data-stu-id="20c54-117">Requirement</span></span> | <span data-ttu-id="20c54-118">Значение</span><span class="sxs-lookup"><span data-stu-id="20c54-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20c54-119">Header</span><span class="sxs-lookup"><span data-stu-id="20c54-119">Header</span></span><br/>  | <dl> <span data-ttu-id="20c54-120"><dt>Вксутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="20c54-120"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="20c54-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="20c54-121">Library</span></span><br/> | <dl> <span data-ttu-id="20c54-122"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="20c54-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20c54-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="20c54-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20c54-124">Вспомогательные функции страницы свойств</span><span class="sxs-lookup"><span data-stu-id="20c54-124">Property Page Helper Functions</span></span>](property-page-helper-functions.md)
</dt> </dl>

 

 




