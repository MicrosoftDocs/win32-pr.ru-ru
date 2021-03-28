---
description: Считывает строку из файла Setup. INF и извлекает указанное поле из строки.
ms.assetid: 621e85f8-af30-4f1f-bab1-b7f824daa363
title: Функция Парсефиелд (util. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ParseField
api_type:
- DllExport
api_location:
- Shell32.dll
ms.openlocfilehash: 45c7d5bc692f969ba821b5d3243b312d0883658e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265086"
---
# <a name="parsefield-function"></a><span data-ttu-id="6353a-103">Функция Парсефиелд</span><span class="sxs-lookup"><span data-stu-id="6353a-103">ParseField function</span></span>

<span data-ttu-id="6353a-104">\[В настоящее время функция **парсефиелд** должна быть доступна для использования в следующей версии операционной системы Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="6353a-104">\[The **ParseField** function is currently expected to be available for use in the next version of the Microsoft Windows operating system.</span></span> <span data-ttu-id="6353a-105">Он может быть изменен или недоступен в последующих версиях.\]</span><span class="sxs-lookup"><span data-stu-id="6353a-105">It might be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="6353a-106">Считывает строку из файла Setup. INF и извлекает указанное поле из строки.</span><span class="sxs-lookup"><span data-stu-id="6353a-106">Reads a line from Setup.inf and extracts the specified field from the string.</span></span>

## <a name="syntax"></a><span data-ttu-id="6353a-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6353a-107">Syntax</span></span>


```C++
bool ParseField(
  _In_ LPCTSTR *szData,
  _In_ int     n,
  _In_ LPTSTR  *szBuf,
  _In_ int     iBufLen
);
```



## <a name="parameters"></a><span data-ttu-id="6353a-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="6353a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6353a-109">*сздата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6353a-109">*szData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6353a-110">Тип: \**LPCTSTR \** _</span><span class="sxs-lookup"><span data-stu-id="6353a-110">Type: \**LPCTSTR\** _</span></span>

<span data-ttu-id="6353a-111">Указатель на строку из файла Setup. INF.</span><span class="sxs-lookup"><span data-stu-id="6353a-111">A pointer to the line from Setup.inf.</span></span>

</dd> <dt>

<span data-ttu-id="6353a-112">_n \* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="6353a-112">_n\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6353a-113">Тип: **int**</span><span class="sxs-lookup"><span data-stu-id="6353a-113">Type: **int**</span></span>

<span data-ttu-id="6353a-114">**Целое** число, указывающее поле для извлечения.</span><span class="sxs-lookup"><span data-stu-id="6353a-114">**INT** that indicates which field to extract.</span></span>

<dt>



 <span data-ttu-id="6353a-115"> (0)</span><span class="sxs-lookup"><span data-stu-id="6353a-115">(0)</span></span>


</dt> <dd>

<span data-ttu-id="6353a-116">Указывает поле перед знаком равенства (=).</span><span class="sxs-lookup"><span data-stu-id="6353a-116">Indicates the field before an equals sign (=).</span></span>

</dd> <dt>



 <span data-ttu-id="6353a-117">(1)</span><span class="sxs-lookup"><span data-stu-id="6353a-117">(1)</span></span>


</dt> <dd>

<span data-ttu-id="6353a-118">Указывает первое поле.</span><span class="sxs-lookup"><span data-stu-id="6353a-118">Indicates the first field.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="6353a-119">*сзбуф* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6353a-119">*szBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6353a-120">Тип: \**LPTSTR \** _</span><span class="sxs-lookup"><span data-stu-id="6353a-120">Type: \**LPTSTR\** _</span></span>

<span data-ttu-id="6353a-121">Указатель на буфер, который получает извлеченное поле.</span><span class="sxs-lookup"><span data-stu-id="6353a-121">A pointer to the buffer that receives the extracted field.</span></span>

</dd> <dt>

<span data-ttu-id="6353a-122">_iBufLen \* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="6353a-122">_iBufLen\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6353a-123">Тип: **int**</span><span class="sxs-lookup"><span data-stu-id="6353a-123">Type: **int**</span></span>

<span data-ttu-id="6353a-124">**Целое** число, получающее размер буфера, получающего извлеченное поле.</span><span class="sxs-lookup"><span data-stu-id="6353a-124">**INT** that receives the size of the buffer that receives the extracted field.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6353a-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6353a-125">Return value</span></span>

<span data-ttu-id="6353a-126">Тип: **bool** .</span><span class="sxs-lookup"><span data-stu-id="6353a-126">Type: **bool**</span></span>

<span data-ttu-id="6353a-127">Возвращает **значение true** , если функция выполнена успешно, и **значение false** в случае сбоя.</span><span class="sxs-lookup"><span data-stu-id="6353a-127">Returns **TRUE** if the function is successful and **FALSE** if it fails.</span></span>

## <a name="remarks"></a><span data-ttu-id="6353a-128">Примечания</span><span class="sxs-lookup"><span data-stu-id="6353a-128">Remarks</span></span>

<span data-ttu-id="6353a-129">Поля в строке должны быть разделены запятыми.</span><span class="sxs-lookup"><span data-stu-id="6353a-129">The fields in the string must be separated by commas.</span></span>

<span data-ttu-id="6353a-130">Начальные и конечные пробелы удаляются.</span><span class="sxs-lookup"><span data-stu-id="6353a-130">Leading and trailing spaces are removed.</span></span>

## <a name="requirements"></a><span data-ttu-id="6353a-131">Требования</span><span class="sxs-lookup"><span data-stu-id="6353a-131">Requirements</span></span>



| <span data-ttu-id="6353a-132">Требование</span><span class="sxs-lookup"><span data-stu-id="6353a-132">Requirement</span></span> | <span data-ttu-id="6353a-133">Значение</span><span class="sxs-lookup"><span data-stu-id="6353a-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6353a-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6353a-134">Minimum supported client</span></span><br/> | <span data-ttu-id="6353a-135">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="6353a-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6353a-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6353a-136">Minimum supported server</span></span><br/> | <span data-ttu-id="6353a-137">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="6353a-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="6353a-138">Заголовок</span><span class="sxs-lookup"><span data-stu-id="6353a-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="6353a-139"><dt>Util. h</dt></span><span class="sxs-lookup"><span data-stu-id="6353a-139"><dt>Util.h</dt></span></span> </dl>                             |
| <span data-ttu-id="6353a-140">Библиотека</span><span class="sxs-lookup"><span data-stu-id="6353a-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="6353a-141"><dt>Shell32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6353a-141"><dt>Shell32.lib</dt></span></span> </dl>                        |
| <span data-ttu-id="6353a-142">DLL</span><span class="sxs-lookup"><span data-stu-id="6353a-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6353a-143"><dt>Shell32.dll (версия 5,0 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="6353a-143"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 




