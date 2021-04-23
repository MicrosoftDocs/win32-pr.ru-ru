---
description: Определяет, соответствует ли строка Юникода указанному шаблону.
ms.assetid: 9b220cb8-4402-4094-8209-59a9af004b4a
title: Функция Ртлиснамеинекспрессион
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlIsNameInExpression
api_type:
- DllExport
api_location:
- ntdll.dll
ms.openlocfilehash: ac6142b364a135b62505841963fa799ce6603dbe
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662081"
---
# <a name="rtlisnameinexpression-function"></a><span data-ttu-id="1411c-103">Функция Ртлиснамеинекспрессион</span><span class="sxs-lookup"><span data-stu-id="1411c-103">RtlIsNameInExpression function</span></span>

<span data-ttu-id="1411c-104">Определяет, соответствует ли строка Юникода указанному шаблону.</span><span class="sxs-lookup"><span data-stu-id="1411c-104">Determines whether a Unicode string matches the specified pattern.</span></span>

## <a name="syntax"></a><span data-ttu-id="1411c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1411c-105">Syntax</span></span>


```C++
 BOOLEAN  RtlIsNameInExpression(
  _In_     PUNICODE_STRING Expression,
  _In_     PUNICODE_STRING Name,
  _In_     BOOLEAN         IgnoreCase,
  _In_opt_ PWCH            UpcaseTable
);
```



## <a name="parameters"></a><span data-ttu-id="1411c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1411c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1411c-107">*Выражение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1411c-107">*Expression* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1411c-108">Указатель на строку шаблона.</span><span class="sxs-lookup"><span data-stu-id="1411c-108">A pointer to the pattern string.</span></span> <span data-ttu-id="1411c-109">Эта строка может содержать подстановочные знаки.</span><span class="sxs-lookup"><span data-stu-id="1411c-109">This string can contain wildcard characters.</span></span> <span data-ttu-id="1411c-110">Если параметр *ignoreCase* имеет значение true, строка должна содержать только символы верхнего регистра.</span><span class="sxs-lookup"><span data-stu-id="1411c-110">If the *IgnoreCase* parameter is TRUE, the string must contain only uppercase characters.</span></span>

</dd> <dt>

<span data-ttu-id="1411c-111">*Имя* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1411c-111">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1411c-112">Указатель на строку, сравниваемую с шаблоном.</span><span class="sxs-lookup"><span data-stu-id="1411c-112">A pointer to the string to be compared against the pattern.</span></span> <span data-ttu-id="1411c-113">Эта строка не может содержать подстановочные знаки.</span><span class="sxs-lookup"><span data-stu-id="1411c-113">This string cannot contain wildcard characters.</span></span>

</dd> <dt>

<span data-ttu-id="1411c-114">*IgnoreCase* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1411c-114">*IgnoreCase* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1411c-115">**Значение true** для сопоставления без учета регистра или **false** для сопоставления с учетом регистра.</span><span class="sxs-lookup"><span data-stu-id="1411c-115">**TRUE** for case-insensitive matching, or **FALSE** for case-sensitive matching.</span></span>

</dd> <dt>

<span data-ttu-id="1411c-116">*Упкасетабле* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="1411c-116">*UpcaseTable* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1411c-117">Необязательный указатель на таблицу символов в верхнем регистре, используемую для сопоставления без учета регистра.</span><span class="sxs-lookup"><span data-stu-id="1411c-117">An optional pointer to an uppercase character table to use for case-insensitive matching.</span></span> <span data-ttu-id="1411c-118">Если этот параметр имеет значение NULL, используется таблица символов верхнего регистра системы по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1411c-118">If this parameter is NULL, the default system uppercase character table is used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1411c-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1411c-119">Return value</span></span>

<span data-ttu-id="1411c-120">Возвращает **значение true** , если строка соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="1411c-120">Returns **TRUE** if the string matches the pattern.</span></span> <span data-ttu-id="1411c-121">Если строка не соответствует шаблону, эта функция возвращает **значение false**.</span><span class="sxs-lookup"><span data-stu-id="1411c-121">If the string does not match the pattern, this function returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="1411c-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1411c-122">Remarks</span></span>

<span data-ttu-id="1411c-123">Эта функция не имеет связанного файла заголовка.</span><span class="sxs-lookup"><span data-stu-id="1411c-123">This function has no associated header file.</span></span> <span data-ttu-id="1411c-124">Связанная библиотека импорта, NTDLL. lib, доступна в наборе драйверов Microsoft Windows (WDK).</span><span class="sxs-lookup"><span data-stu-id="1411c-124">The associated import library, Ntdll.lib, is available in the Microsoft Windows Driver Kit (WDK).</span></span> <span data-ttu-id="1411c-125">Эту функцию также можно вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) для динамической привязки к Ntdll.dll.</span><span class="sxs-lookup"><span data-stu-id="1411c-125">You can also call this function using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Ntdll.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="1411c-126">Требования</span><span class="sxs-lookup"><span data-stu-id="1411c-126">Requirements</span></span>



| <span data-ttu-id="1411c-127">Требование</span><span class="sxs-lookup"><span data-stu-id="1411c-127">Requirement</span></span> | <span data-ttu-id="1411c-128">Значение</span><span class="sxs-lookup"><span data-stu-id="1411c-128">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="1411c-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1411c-129">Minimum supported client</span></span><br/> | <span data-ttu-id="1411c-130">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="1411c-130">Windows 7 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="1411c-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1411c-131">Minimum supported server</span></span><br/> | <span data-ttu-id="1411c-132">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="1411c-132">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="1411c-133">DLL</span><span class="sxs-lookup"><span data-stu-id="1411c-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1411c-134"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1411c-134"><dt>Ntdll.dll</dt></span></span> </dl> |



 

 
