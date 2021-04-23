---
description: Преобразует символы нижнего регистра в буфере в символы верхнего регистра.
ms.assetid: 63293fda-6f55-419a-b5b4-7a3ada31580c
title: Функция Чаруппербуффврапв
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CharUpperBuffWrapW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.openlocfilehash: dacc5e7609ca7f91bf7c66651d7ba9bdd11ab688
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540554"
---
# <a name="charupperbuffwrapw-function"></a><span data-ttu-id="0dbaf-103">Функция Чаруппербуффврапв</span><span class="sxs-lookup"><span data-stu-id="0dbaf-103">CharUpperBuffWrapW function</span></span>

<span data-ttu-id="0dbaf-104">\[**Чаруппербуффврапв** доступен для использования в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="0dbaf-104">\[**CharUpperBuffWrapW** is available for use in Windows XP.</span></span> <span data-ttu-id="0dbaf-105">Она может быть недоступна в последующих версиях.</span><span class="sxs-lookup"><span data-stu-id="0dbaf-105">It may not be available in subsequent versions.</span></span> <span data-ttu-id="0dbaf-106">На своем месте следует использовать [**чаруппербуффв**](/windows/win32/api/winuser/nf-winuser-charupperbuffa) .\]</span><span class="sxs-lookup"><span data-stu-id="0dbaf-106">You should use [**CharUpperBuffW**](/windows/win32/api/winuser/nf-winuser-charupperbuffa) in its place.\]</span></span>

<span data-ttu-id="0dbaf-107">Преобразует символы нижнего регистра в буфере в символы верхнего регистра.</span><span class="sxs-lookup"><span data-stu-id="0dbaf-107">Converts lowercase characters in a buffer to uppercase characters.</span></span> <span data-ttu-id="0dbaf-108">Функция преобразует символы на месте.</span><span class="sxs-lookup"><span data-stu-id="0dbaf-108">The function converts the characters in place.</span></span>

> [!Note]  
> <span data-ttu-id="0dbaf-109">**Чаруппербуффврапв** — это оболочка для функции **чаруппербуффв** .</span><span class="sxs-lookup"><span data-stu-id="0dbaf-109">**CharUpperBuffWrapW** is a wrapper for the **CharUpperBuffW** function.</span></span> <span data-ttu-id="0dbaf-110">Дополнительные сведения об использовании см. на странице [**чаруппербуфф**](/windows/win32/api/winuser/nf-winuser-charupperbuffa) .</span><span class="sxs-lookup"><span data-stu-id="0dbaf-110">See the [**CharUpperBuff**](/windows/win32/api/winuser/nf-winuser-charupperbuffa) page for further usage notes.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="0dbaf-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0dbaf-111">Syntax</span></span>


```C++
DWORD CharUpperBuffWrapW(
  _In_ LPWSTR pch,
  _In_ DWORD  cchLength
);
```



## <a name="parameters"></a><span data-ttu-id="0dbaf-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="0dbaf-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0dbaf-113">*PCH* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0dbaf-113">*pch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0dbaf-114">Тип: **LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="0dbaf-114">Type: **LPWSTR**</span></span>

<span data-ttu-id="0dbaf-115">Указатель на буфер, содержащий один или несколько символов Юникода для обработки.</span><span class="sxs-lookup"><span data-stu-id="0dbaf-115">A pointer to a buffer that contains one or more Unicode characters to process.</span></span>

</dd> <dt>

<span data-ttu-id="0dbaf-116">*кчленгс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0dbaf-116">*cchLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0dbaf-117">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="0dbaf-117">Type: **DWORD**</span></span>

<span data-ttu-id="0dbaf-118">Задает размер (в символах) буфера, на который указывает *PCH*.</span><span class="sxs-lookup"><span data-stu-id="0dbaf-118">Specifies the size, in characters, of the buffer pointed to by *pch*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0dbaf-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0dbaf-119">Return value</span></span>

<span data-ttu-id="0dbaf-120">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="0dbaf-120">Type: **DWORD**</span></span>

<span data-ttu-id="0dbaf-121">Число обработанных символов.</span><span class="sxs-lookup"><span data-stu-id="0dbaf-121">The number of characters processed.</span></span>

## <a name="remarks"></a><span data-ttu-id="0dbaf-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="0dbaf-122">Remarks</span></span>

<span data-ttu-id="0dbaf-123">Предпочтительным методом является использование [**чаруппербуффв**](/windows/win32/api/winuser/nf-winuser-charupperbuffa) в сочетании с уровнем Майкрософт для Юникода (мслу).</span><span class="sxs-lookup"><span data-stu-id="0dbaf-123">The preferred method is to use [**CharUpperBuffW**](/windows/win32/api/winuser/nf-winuser-charupperbuffa) in conjunction with the Microsoft Layer for Unicode (MSLU).</span></span>

<span data-ttu-id="0dbaf-124">**Чаруппербуффврапв** должен вызываться напрямую из Shlwapi.dll с использованием порядкового номера 44.</span><span class="sxs-lookup"><span data-stu-id="0dbaf-124">**CharUpperBuffWrapW** must be called directly from Shlwapi.dll, using ordinal 44.</span></span>

## <a name="requirements"></a><span data-ttu-id="0dbaf-125">Требования</span><span class="sxs-lookup"><span data-stu-id="0dbaf-125">Requirements</span></span>



| <span data-ttu-id="0dbaf-126">Требование</span><span class="sxs-lookup"><span data-stu-id="0dbaf-126">Requirement</span></span> | <span data-ttu-id="0dbaf-127">Значение</span><span class="sxs-lookup"><span data-stu-id="0dbaf-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0dbaf-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0dbaf-128">Minimum supported client</span></span><br/> | <span data-ttu-id="0dbaf-129">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="0dbaf-129">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0dbaf-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0dbaf-130">Minimum supported server</span></span><br/> | <span data-ttu-id="0dbaf-131">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0dbaf-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="0dbaf-132">DLL</span><span class="sxs-lookup"><span data-stu-id="0dbaf-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0dbaf-133"><dt>Shlwapi.dll (версия 5,0 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="0dbaf-133"><dt>Shlwapi.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0dbaf-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0dbaf-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0dbaf-135">**чаруппербуфф**</span><span class="sxs-lookup"><span data-stu-id="0dbaf-135">**CharUpperBuff**</span></span>](/windows/win32/api/winuser/nf-winuser-charupperbuffa)
</dt> </dl>

 

 
