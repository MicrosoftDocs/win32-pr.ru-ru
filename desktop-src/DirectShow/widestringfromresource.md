---
description: Функция Видестрингфромресаурце загружает строку расширенных символов из файла ресурсов с заданным идентификатором ресурса.
ms.assetid: c5fac767-20c4-4342-9d4d-e1b916854b95
title: Функция Видестрингфромресаурце (Вксутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WideStringFromResource
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9c7cbdccc76fc57e660109851ae5b8f141704d04
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668736"
---
# <a name="widestringfromresource-function"></a><span data-ttu-id="4627d-103">Функция Видестрингфромресаурце</span><span class="sxs-lookup"><span data-stu-id="4627d-103">WideStringFromResource function</span></span>

<span data-ttu-id="4627d-104">`WideStringFromResource`Функция загружает строку расширенных символов из файла ресурсов с заданным идентификатором ресурса.</span><span class="sxs-lookup"><span data-stu-id="4627d-104">The `WideStringFromResource` function loads a wide-character string from a resource file with the given resource identifier.</span></span>

## <a name="syntax"></a><span data-ttu-id="4627d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4627d-105">Syntax</span></span>


```C++
WCHAR* WINAPI WideStringFromResource(
   pBuffer *pBuffer,
   int     iResourceID
);
```



## <a name="parameters"></a><span data-ttu-id="4627d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4627d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4627d-107">*pBuffer*</span><span class="sxs-lookup"><span data-stu-id="4627d-107">*pBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="4627d-108">Указатель на строку, соответствующую *иресаурцеид*.</span><span class="sxs-lookup"><span data-stu-id="4627d-108">Pointer to the string corresponding to *iResourceID*.</span></span>

</dd> <dt>

<span data-ttu-id="4627d-109">*иресаурцеид*</span><span class="sxs-lookup"><span data-stu-id="4627d-109">*iResourceID*</span></span> 
</dt> <dd>

<span data-ttu-id="4627d-110">Идентификатор ресурса извлекаемой строки.</span><span class="sxs-lookup"><span data-stu-id="4627d-110">Resource identifier of the string to retrieve.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4627d-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4627d-111">Return value</span></span>

<span data-ttu-id="4627d-112">Возвращает ту же строку, что и *pBuffer*.</span><span class="sxs-lookup"><span data-stu-id="4627d-112">Returns the same string as *pBuffer*.</span></span> <span data-ttu-id="4627d-113">Если функция не выполнена успешно, возвращает пустую строку.</span><span class="sxs-lookup"><span data-stu-id="4627d-113">If the function is not successful, returns a null string.</span></span>

## <a name="remarks"></a><span data-ttu-id="4627d-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4627d-114">Remarks</span></span>

<span data-ttu-id="4627d-115">Страницы свойств обычно вызываются через интерфейсы COM, которые используют строки расширенных символов независимо от того, как создается двоичный файл.</span><span class="sxs-lookup"><span data-stu-id="4627d-115">Property pages are typically called through their COM interfaces, which use wide-character strings regardless of how the binary is built.</span></span> <span data-ttu-id="4627d-116">Эта функция позволяет преобразовать строку ресурса в строку расширенных символов.</span><span class="sxs-lookup"><span data-stu-id="4627d-116">This function allows you to convert a resource string to a wide-character string.</span></span> <span data-ttu-id="4627d-117">Функция преобразует ресурс в строку расширенных символов (если она еще не одна) после ее загрузки.</span><span class="sxs-lookup"><span data-stu-id="4627d-117">The function converts the resource to a wide-character string (if it is not already one) after loading it.</span></span>

## <a name="requirements"></a><span data-ttu-id="4627d-118">Требования</span><span class="sxs-lookup"><span data-stu-id="4627d-118">Requirements</span></span>



| <span data-ttu-id="4627d-119">Требование</span><span class="sxs-lookup"><span data-stu-id="4627d-119">Requirement</span></span> | <span data-ttu-id="4627d-120">Значение</span><span class="sxs-lookup"><span data-stu-id="4627d-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4627d-121">Header</span><span class="sxs-lookup"><span data-stu-id="4627d-121">Header</span></span><br/>  | <dl> <span data-ttu-id="4627d-122"><dt>Вксутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4627d-122"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="4627d-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="4627d-123">Library</span></span><br/> | <dl> <span data-ttu-id="4627d-124"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="4627d-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4627d-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4627d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4627d-126">Вспомогательные функции страницы свойств</span><span class="sxs-lookup"><span data-stu-id="4627d-126">Property Page Helper Functions</span></span>](property-page-helper-functions.md)
</dt> </dl>

 

 




