---
description: Использует последовательные вызовы для получения всех строк в указанных диапазонах.
ms.assetid: 4e819975-84a5-4b73-9a19-792d3607da9c
title: Функция Жетстрингсфромблоб (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetStringsFromBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 25fbc149a663ef68d1588218937568401f414ef7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990894"
---
# <a name="getstringsfromblob-function"></a><span data-ttu-id="e68f9-103">Функция Жетстрингсфромблоб</span><span class="sxs-lookup"><span data-stu-id="e68f9-103">GetStringsFromBlob function</span></span>

<span data-ttu-id="e68f9-104">Функция **жетстрингсфромблоб** использует последовательные вызовы для получения всех строк в указанных диапазонах.</span><span class="sxs-lookup"><span data-stu-id="e68f9-104">The **GetStringsFromBlob** function uses sequential calls to retrieve all of the strings within specified ranges.</span></span>

## <a name="syntax"></a><span data-ttu-id="e68f9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e68f9-105">Syntax</span></span>


```C++
DWORD GetStringsFromBlob(
  _In_        HBLOB hBlob,
  _In_  const char  *pRequestedOwnerName,
  _In_  const char  *pRequestedCategoryName,
  _In_  const char  *pRequestedTagName,
  _Out_ const char  **ppReturnedOwnerName,
  _Out_ const char  **ppReturnedCategoryName,
  _Out_ const char  **ppReturnedTagName,
  _Out_ const char  **ppReturnedString,
  _Out_       DWORD *pRestartKey
);
```



## <a name="parameters"></a><span data-ttu-id="e68f9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e68f9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e68f9-107">*хблоб* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e68f9-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e68f9-108">Маркер для большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="e68f9-108">A handle to the BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="e68f9-109">*прекуестедовнернаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e68f9-109">*pRequestedOwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e68f9-110">Указатель на раздел Owner, из которого нужно получить строку.</span><span class="sxs-lookup"><span data-stu-id="e68f9-110">A pointer to the Owner section to get the string from.</span></span>

</dd> <dt>

<span data-ttu-id="e68f9-111">*прекуестедкатегоринаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e68f9-111">*pRequestedCategoryName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e68f9-112">Указатель на раздел Category, из которого нужно получить строку.</span><span class="sxs-lookup"><span data-stu-id="e68f9-112">A pointer to the Category section to get the string from.</span></span>

</dd> <dt>

<span data-ttu-id="e68f9-113">*прекуестедтагнаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e68f9-113">*pRequestedTagName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e68f9-114">Указатель на тег для запрошенной строки.</span><span class="sxs-lookup"><span data-stu-id="e68f9-114">A pointer to the tag for the requested string.</span></span>

</dd> <dt>

<span data-ttu-id="e68f9-115">*ппретурнедовнернаме* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e68f9-115">*ppReturnedOwnerName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e68f9-116">Указатель на переменную, указывающую на место, где будет возвращено имя **владельца** .</span><span class="sxs-lookup"><span data-stu-id="e68f9-116">A pointer to the variable that points to where the **Owner** name will be returned.</span></span>

</dd> <dt>

<span data-ttu-id="e68f9-117">*ппретурнедкатегоринаме* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e68f9-117">*ppReturnedCategoryName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e68f9-118">Указатель на переменную, указывающую на место, где будет возвращено имя **категории** .</span><span class="sxs-lookup"><span data-stu-id="e68f9-118">A pointer to the variable that points to where the **Category** name will be returned.</span></span>

</dd> <dt>

<span data-ttu-id="e68f9-119">*ппретурнедтагнаме* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e68f9-119">*ppReturnedTagName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e68f9-120">Указатель на переменную, указывающую на место, где будет возвращено имя **тега** .</span><span class="sxs-lookup"><span data-stu-id="e68f9-120">A pointer to the variable that points to where the **Tag** name will be returned.</span></span>

</dd> <dt>

<span data-ttu-id="e68f9-121">*ппретурнедстринг* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e68f9-121">*ppReturnedString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e68f9-122">Указатель на переменную, указывающую на место, где будет возвращено строковое имя.</span><span class="sxs-lookup"><span data-stu-id="e68f9-122">A pointer to the variable that points to where the string name will be returned.</span></span>

</dd> <dt>

<span data-ttu-id="e68f9-123">*престарткэй* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e68f9-123">*pRestartKey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e68f9-124">Указатель на переменную, в которой будет указан и возвращен ключ перезапуска.</span><span class="sxs-lookup"><span data-stu-id="e68f9-124">A pointer to the variable where the restart key will be specified and returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e68f9-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e68f9-125">Return value</span></span>

<span data-ttu-id="e68f9-126">Если функция выполнена успешно, возвращается значение НМЕРР \_ Success.</span><span class="sxs-lookup"><span data-stu-id="e68f9-126">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="e68f9-127">Если функция завершается неудачно, возвращается значение НМЕРР, указывающее на проблему.</span><span class="sxs-lookup"><span data-stu-id="e68f9-127">If the function is unsuccessful, the return value is a NMERR value that indicates the problem.</span></span>

<span data-ttu-id="e68f9-128">Если указанная комбинация сведений о **владельце**, **категории** и **теге** не существует, возвращаемое значение — это **нмерр \_ запись большого двоичного объекта \_ \_ \_ \_**.</span><span class="sxs-lookup"><span data-stu-id="e68f9-128">If a specified combination of **Owner**, **Category**, and **Tag** information does not exist, the return value is **NMERR\_BLOB\_ENTRY\_DOES\_NOT\_EXIST**.</span></span>

<span data-ttu-id="e68f9-129">При первоначальном просмотре большого двоичного объекта в пределах указанных границ функция возвращает **\_ запись большого двоичного \_ объекта \_ \_ \_ нмерр**, а параметр *престарткэй* указывает на ноль.</span><span class="sxs-lookup"><span data-stu-id="e68f9-129">When the BLOB is traversed completely within the bounds initially specified, the function returns **NMERR\_BLOB\_ENTRY\_DOES\_NOT\_EXIST**, and the *pRestartKey* parameter points to zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="e68f9-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e68f9-130">Remarks</span></span>

<span data-ttu-id="e68f9-131">При первом вызове функции **жетстрингсфромблоб** параметр *престарткэй* указывает на переменную, содержащую нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="e68f9-131">On the initial call to the **GetStringsFromBlob** function, the *pRestartKey* parameter points to a variable that contains the value zero.</span></span> <span data-ttu-id="e68f9-132">Предустановленные параметры можно использовать только в том *случае, если* ключ перезапуска равен нулю.</span><span class="sxs-lookup"><span data-stu-id="e68f9-132">The *pRequested* parameters can be used only when the restart key is zero.</span></span> <span data-ttu-id="e68f9-133">В последующих вызовах, когда *престарткэй* имеет ненулевые значения, заданные *параметры игнорируются* .</span><span class="sxs-lookup"><span data-stu-id="e68f9-133">In subsequent calls, when *pRestartKey* has nonzero values, the *pRequested* parameters are ignored.</span></span> <span data-ttu-id="e68f9-134">При первом вызове ALL может указывать на **значение NULL**, которое настраивает запрос для возврата каждой записи в большом двоичном объекте, по одному на последующий вызов.</span><span class="sxs-lookup"><span data-stu-id="e68f9-134">On the initial call, all may point to **NULL**, which sets up the query to return every entry in the BLOB, one per subsequent call.</span></span>

<span data-ttu-id="e68f9-135">Указание владельца ограничивает возвращаемые строки только этим владельцем.</span><span class="sxs-lookup"><span data-stu-id="e68f9-135">Specifying an owner limits the strings returned to just that owner.</span></span> <span data-ttu-id="e68f9-136">Аналогичное ограничение имеет значение true для категорий и тегов. Кроме того, при указании категории необходимо указать владельца, а если указать тег, необходимо указать категорию (и, следовательно, владельца).</span><span class="sxs-lookup"><span data-stu-id="e68f9-136">A similar limitation is true for categories and tags, with the additional caveat that if a category is specified, an owner must also be specified and if a tag is specified, a category (and therefore an owner) must be specified.</span></span>

<span data-ttu-id="e68f9-137">Когда начальный вызов **жетстрингсфромблоб** возвращает, *престарткэй* указывает на новое значение, которое должно быть указано при следующем вызове функции для получения следующего значения.</span><span class="sxs-lookup"><span data-stu-id="e68f9-137">When the initial call to **GetStringsFromBlob** returns, *pRestartKey* points to a new value, which should be specified on the next call to the function to get the next value.</span></span>

## <a name="requirements"></a><span data-ttu-id="e68f9-138">Требования</span><span class="sxs-lookup"><span data-stu-id="e68f9-138">Requirements</span></span>



| <span data-ttu-id="e68f9-139">Требование</span><span class="sxs-lookup"><span data-stu-id="e68f9-139">Requirement</span></span> | <span data-ttu-id="e68f9-140">Значение</span><span class="sxs-lookup"><span data-stu-id="e68f9-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e68f9-141">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e68f9-141">Minimum supported client</span></span><br/> | <span data-ttu-id="e68f9-142">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e68f9-142">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="e68f9-143">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e68f9-143">Minimum supported server</span></span><br/> | <span data-ttu-id="e68f9-144">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e68f9-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e68f9-145">Заголовок</span><span class="sxs-lookup"><span data-stu-id="e68f9-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="e68f9-146"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="e68f9-146"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="e68f9-147">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e68f9-147">Library</span></span><br/>                  | <dl> <span data-ttu-id="e68f9-148"><dt>Нпптулс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e68f9-148"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="e68f9-149">DLL</span><span class="sxs-lookup"><span data-stu-id="e68f9-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e68f9-150"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e68f9-150"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e68f9-151">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e68f9-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e68f9-152">сетстрингинблоб</span><span class="sxs-lookup"><span data-stu-id="e68f9-152">SetStringInBlob</span></span>](setstringinblob.md)
</dt> <dt>

[<span data-ttu-id="e68f9-153">жетбулфромблоб</span><span class="sxs-lookup"><span data-stu-id="e68f9-153">GetBoolFromBlob</span></span>](getboolfromblob.md)
</dt> <dt>

[<span data-ttu-id="e68f9-154">жетклассидфромблоб</span><span class="sxs-lookup"><span data-stu-id="e68f9-154">GetClassIDFromBlob</span></span>](getclassidfromblob.md)
</dt> <dt>

[<span data-ttu-id="e68f9-155">жетдвордфромблоб</span><span class="sxs-lookup"><span data-stu-id="e68f9-155">GetDwordFromBlob</span></span>](getdwordfromblob.md)
</dt> <dt>

[<span data-ttu-id="e68f9-156">жетмакаддрессфромблоб</span><span class="sxs-lookup"><span data-stu-id="e68f9-156">GetMacAddressFromBlob</span></span>](getmacaddressfromblob.md)
</dt> <dt>

[<span data-ttu-id="e68f9-157">жетнетворкинфофромблоб</span><span class="sxs-lookup"><span data-stu-id="e68f9-157">GetNetworkInfoFromBlob</span></span>](getnetworkinfofromblob.md)
</dt> <dt>

[<span data-ttu-id="e68f9-158">жетнппаддрессфилтерфромблоб</span><span class="sxs-lookup"><span data-stu-id="e68f9-158">GetNPPAddressFilterFromBlob</span></span>](getnppaddressfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="e68f9-159">жетнпппаттернфилтерфромблоб</span><span class="sxs-lookup"><span data-stu-id="e68f9-159">GetNPPPatternFilterFromBlob</span></span>](getnpppatternfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="e68f9-160">жетнпптригжерфромблоб</span><span class="sxs-lookup"><span data-stu-id="e68f9-160">GetNPPTriggerFromBlob</span></span>](getnpptriggerfromblob.md)
</dt> <dt>

[<span data-ttu-id="e68f9-161">жетстрингфромблоб</span><span class="sxs-lookup"><span data-stu-id="e68f9-161">GetStringFromBlob</span></span>](getstringfromblob.md)
</dt> </dl>

 

 




