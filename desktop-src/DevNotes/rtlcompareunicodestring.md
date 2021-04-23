---
description: Сравнивает две строки в Юникоде.
ms.assetid: D2703180-946C-4762-AFBA-1E882B01B944
title: Функция Ртлкомпареуникодестринг (WDM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlCompareUnicodeString
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 9de12f218c37916c7e30393c0701efcf1889973f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895825"
---
# <a name="rtlcompareunicodestring-function"></a><span data-ttu-id="1bae6-103">Функция Ртлкомпареуникодестринг</span><span class="sxs-lookup"><span data-stu-id="1bae6-103">RtlCompareUnicodeString function</span></span>

<span data-ttu-id="1bae6-104">Сравнивает две строки в Юникоде.</span><span class="sxs-lookup"><span data-stu-id="1bae6-104">Compares two Unicode strings.</span></span>

## <a name="syntax"></a><span data-ttu-id="1bae6-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1bae6-105">Syntax</span></span>


```C++
LONG RtlCompareUnicodeString(
  _In_ PCUNICODE_STRING String1,
  _In_ PCUNICODE_STRING String2,
  _In_ BOOLEAN          CaseInSensitive
);
```



## <a name="parameters"></a><span data-ttu-id="1bae6-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1bae6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1bae6-107">*Строка1* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1bae6-107">*String1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1bae6-108">Указатель на первую строку.</span><span class="sxs-lookup"><span data-stu-id="1bae6-108">Pointer to the first string.</span></span>

</dd> <dt>

<span data-ttu-id="1bae6-109">*Строка2* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1bae6-109">*String2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1bae6-110">Указатель на вторую строку.</span><span class="sxs-lookup"><span data-stu-id="1bae6-110">Pointer to the second string.</span></span>

</dd> <dt>

<span data-ttu-id="1bae6-111">*Без* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1bae6-111">*CaseInSensitive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1bae6-112">Если **значение — true**, при выполнении сравнения регистр следует игнорировать.</span><span class="sxs-lookup"><span data-stu-id="1bae6-112">If **TRUE**, case should be ignored when doing the comparison.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1bae6-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1bae6-113">Return value</span></span>

<span data-ttu-id="1bae6-114">Значение со знаком, которое дает результаты сравнения:</span><span class="sxs-lookup"><span data-stu-id="1bae6-114">A signed value that gives the results of the comparison:</span></span>



| <span data-ttu-id="1bae6-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="1bae6-115">Return code</span></span>                                                                               | <span data-ttu-id="1bae6-116">Описание</span><span class="sxs-lookup"><span data-stu-id="1bae6-116">Description</span></span>                                     |
|-------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="1bae6-117"><dt>**Ноль**</dt></span><span class="sxs-lookup"><span data-stu-id="1bae6-117"><dt>**Zero**</dt></span></span> </dl>       | <span data-ttu-id="1bae6-118">*Строка1* равна *строка2*.</span><span class="sxs-lookup"><span data-stu-id="1bae6-118">*String1* equals *String2*.</span></span><br/>          |
| <dl> <span data-ttu-id="1bae6-119"><dt>**< ноль**</dt></span><span class="sxs-lookup"><span data-stu-id="1bae6-119"><dt>**< Zero**</dt></span></span> </dl>  | <span data-ttu-id="1bae6-120">*Строка1* меньше, чем *строка2*.</span><span class="sxs-lookup"><span data-stu-id="1bae6-120">*String1* is less than *String2*.</span></span><br/>    |
| <dl> <span data-ttu-id="1bae6-121"><dt>**> ноль**</dt></span><span class="sxs-lookup"><span data-stu-id="1bae6-121"><dt>**> Zero** </dt></span></span> </dl> | <span data-ttu-id="1bae6-122">*Строка1* больше, чем *строка2*.</span><span class="sxs-lookup"><span data-stu-id="1bae6-122">*String1* is greater than *String2*.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="1bae6-123">Требования</span><span class="sxs-lookup"><span data-stu-id="1bae6-123">Requirements</span></span>



| <span data-ttu-id="1bae6-124">Требование</span><span class="sxs-lookup"><span data-stu-id="1bae6-124">Requirement</span></span> | <span data-ttu-id="1bae6-125">Значение</span><span class="sxs-lookup"><span data-stu-id="1bae6-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1bae6-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1bae6-126">Minimum supported client</span></span><br/> | <span data-ttu-id="1bae6-127">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="1bae6-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                              |
| <span data-ttu-id="1bae6-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1bae6-128">Minimum supported server</span></span><br/> | <span data-ttu-id="1bae6-129">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="1bae6-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                    |
| <span data-ttu-id="1bae6-130">Целевая платформа</span><span class="sxs-lookup"><span data-stu-id="1bae6-130">Target platform</span></span><br/>          | <dl> <span data-ttu-id="1bae6-131"><dt>[Универсальной](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt></span><span class="sxs-lookup"><span data-stu-id="1bae6-131"><dt>[Universal](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt></span></span> </dl> |
| <span data-ttu-id="1bae6-132">Header</span><span class="sxs-lookup"><span data-stu-id="1bae6-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="1bae6-133"><dt>WDM. h (включает WDM. h, Нтддк. h или Нтифс. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1bae6-133"><dt>Wdm.h (include Wdm.h, Ntddk.h, or Ntifs.h)</dt></span></span> </dl>                   |
| <span data-ttu-id="1bae6-134">Библиотека</span><span class="sxs-lookup"><span data-stu-id="1bae6-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="1bae6-135"><dt>NTDLL. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1bae6-135"><dt>Ntdll.lib</dt></span></span> </dl>                                                    |
| <span data-ttu-id="1bae6-136">DLL</span><span class="sxs-lookup"><span data-stu-id="1bae6-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1bae6-137"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1bae6-137"><dt>Ntdll.dll</dt></span></span> </dl>                                                    |



## <a name="see-also"></a><span data-ttu-id="1bae6-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1bae6-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1bae6-139">**ртлкомпарестринг**</span><span class="sxs-lookup"><span data-stu-id="1bae6-139">**RtlCompareString**</span></span>](/windows-hardware/drivers/ddi/ntddk/nf-ntddk-rtlcomparestring)
</dt> <dt>

[<span data-ttu-id="1bae6-140">**ртлекуалстринг**</span><span class="sxs-lookup"><span data-stu-id="1bae6-140">**RtlEqualString**</span></span>](/windows-hardware/drivers/ddi/ntddk/nf-ntddk-rtlequalstring)
</dt> </dl>

 

 
