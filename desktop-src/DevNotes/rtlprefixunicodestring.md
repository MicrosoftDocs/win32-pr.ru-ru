---
description: Сравнивает две строки в Юникоде, чтобы определить, является ли одна строка префиксом другой.
ms.assetid: 7D859C0A-2F72-49A4-8B49-130DCA103F37
title: Функция Ртлпрефиксуникодестринг (Нтддк. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlPrefixUnicodeString
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 47382daab1bac5e71098f79a601d89255f1cf0e9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496104"
---
# <a name="rtlprefixunicodestring-function"></a><span data-ttu-id="4520c-103">Функция Ртлпрефиксуникодестринг</span><span class="sxs-lookup"><span data-stu-id="4520c-103">RtlPrefixUnicodeString function</span></span>

<span data-ttu-id="4520c-104">Сравнивает две строки в Юникоде, чтобы определить, является ли одна строка префиксом другой.</span><span class="sxs-lookup"><span data-stu-id="4520c-104">Compares two Unicode strings to determine whether one string is a prefix of the other.</span></span>

## <a name="syntax"></a><span data-ttu-id="4520c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4520c-105">Syntax</span></span>


```C++
BOOLEAN RtlPrefixUnicodeString(
  _In_ PCUNICODE_STRING String1,
  _In_ PCUNICODE_STRING String2,
  _In_ BOOLEAN          CaseInSensitive
);
```



## <a name="parameters"></a><span data-ttu-id="4520c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4520c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4520c-107">*Строка1* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4520c-107">*String1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4520c-108">Указатель на первую строку, которая может быть префиксом буферизованной строки Юникода в строке *строка2*.</span><span class="sxs-lookup"><span data-stu-id="4520c-108">Pointer to the first string, which might be a prefix of the buffered Unicode string at *String2*.</span></span>

</dd> <dt>

<span data-ttu-id="4520c-109">*Строка2* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4520c-109">*String2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4520c-110">Указатель на вторую строку.</span><span class="sxs-lookup"><span data-stu-id="4520c-110">Pointer to the second string.</span></span>

</dd> <dt>

<span data-ttu-id="4520c-111">*Без* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4520c-111">*CaseInSensitive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4520c-112">Если **значение — true**, при выполнении сравнения регистр следует игнорировать.</span><span class="sxs-lookup"><span data-stu-id="4520c-112">If **TRUE**, case should be ignored when doing the comparison.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4520c-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4520c-113">Return value</span></span>

<span data-ttu-id="4520c-114">**Значение true** , если *строка1* является префиксом *строка_замены*.</span><span class="sxs-lookup"><span data-stu-id="4520c-114">**TRUE** if *String1* is a prefix of *String2*.</span></span>

## <a name="requirements"></a><span data-ttu-id="4520c-115">Требования</span><span class="sxs-lookup"><span data-stu-id="4520c-115">Requirements</span></span>



| <span data-ttu-id="4520c-116">Требование</span><span class="sxs-lookup"><span data-stu-id="4520c-116">Requirement</span></span> | <span data-ttu-id="4520c-117">Значение</span><span class="sxs-lookup"><span data-stu-id="4520c-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4520c-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4520c-118">Minimum supported client</span></span><br/> | <span data-ttu-id="4520c-119">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="4520c-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                              |
| <span data-ttu-id="4520c-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4520c-120">Minimum supported server</span></span><br/> | <span data-ttu-id="4520c-121">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="4520c-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                    |
| <span data-ttu-id="4520c-122">Целевая платформа</span><span class="sxs-lookup"><span data-stu-id="4520c-122">Target platform</span></span><br/>          | <dl> <span data-ttu-id="4520c-123"><dt>[Универсальной](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt></span><span class="sxs-lookup"><span data-stu-id="4520c-123"><dt>[Universal](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt></span></span> </dl> |
| <span data-ttu-id="4520c-124">Header</span><span class="sxs-lookup"><span data-stu-id="4520c-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="4520c-125"><dt>Нтддк. h (включение Нтддк. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4520c-125"><dt>Ntddk.h (include Ntddk.h)</dt></span></span> </dl>                                    |
| <span data-ttu-id="4520c-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="4520c-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="4520c-127"><dt>NTDLL. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4520c-127"><dt>Ntdll.lib</dt></span></span> </dl>                                                    |
| <span data-ttu-id="4520c-128">DLL</span><span class="sxs-lookup"><span data-stu-id="4520c-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4520c-129"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4520c-129"><dt>Ntdll.dll</dt></span></span> </dl>                                                    |



## <a name="see-also"></a><span data-ttu-id="4520c-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4520c-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4520c-131">**ртлкомпареуникодестринг**</span><span class="sxs-lookup"><span data-stu-id="4520c-131">**RtlCompareUnicodeString**</span></span>](rtlcompareunicodestring.md)
</dt> </dl>

 

 




