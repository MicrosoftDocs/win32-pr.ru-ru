---
description: Определяет, является ли символ алфавитным или цифровым символом.
ms.assetid: d4b01ba5-e42a-4040-a763-ecef0c73977f
title: Функция Исчаралфанумерикврапв
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IsCharAlphaNumericWrapW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.openlocfilehash: bf7f1b4db54cc5374214ff45b51579556dc22062
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984721"
---
# <a name="ischaralphanumericwrapw-function"></a><span data-ttu-id="3655e-103">Функция Исчаралфанумерикврапв</span><span class="sxs-lookup"><span data-stu-id="3655e-103">IsCharAlphaNumericWrapW function</span></span>

<span data-ttu-id="3655e-104">\[**Исчаралфанумерикврапв** доступен для использования в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="3655e-104">\[**IsCharAlphaNumericWrapW** is available for use in Windows XP.</span></span> <span data-ttu-id="3655e-105">Он будет недоступен в последующих версиях.</span><span class="sxs-lookup"><span data-stu-id="3655e-105">It will not be available in subsequent versions.</span></span> <span data-ttu-id="3655e-106">На своем месте следует использовать [**исчаралфанумерикв**](/windows/win32/api/winuser/nf-winuser-ischaralphanumerica) .\]</span><span class="sxs-lookup"><span data-stu-id="3655e-106">You should use [**IsCharAlphaNumericW**](/windows/win32/api/winuser/nf-winuser-ischaralphanumerica) in its place.\]</span></span>

<span data-ttu-id="3655e-107">Определяет, является ли символ алфавитным или цифровым символом.</span><span class="sxs-lookup"><span data-stu-id="3655e-107">Determines whether a character is either an alphabetical or a numeric character.</span></span> <span data-ttu-id="3655e-108">Это определение основано на семантике языка, выбранного пользователем во время установки или с помощью панели управления.</span><span class="sxs-lookup"><span data-stu-id="3655e-108">This determination is based on the semantics of the language selected by the user during setup or through Control Panel.</span></span>

> [!Note]  
> <span data-ttu-id="3655e-109">**Исчаралфанумерикврапв** — это оболочка для функции **исчаралфанумерикв** .</span><span class="sxs-lookup"><span data-stu-id="3655e-109">**IsCharAlphaNumericWrapW** is a wrapper for the **IsCharAlphaNumericW** function.</span></span> <span data-ttu-id="3655e-110">Дополнительные сведения об использовании см. на странице [**исчаралфанумерик**](/windows/win32/api/winuser/nf-winuser-ischaralphanumerica) .</span><span class="sxs-lookup"><span data-stu-id="3655e-110">See the [**IsCharAlphaNumeric**](/windows/win32/api/winuser/nf-winuser-ischaralphanumerica) page for further usage notes.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="3655e-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3655e-111">Syntax</span></span>


```C++
BOOL IsCharAlphaNumericWrapW(
  _In_ WCHAR ch
);
```



## <a name="parameters"></a><span data-ttu-id="3655e-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="3655e-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3655e-113">*CH* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3655e-113">*ch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3655e-114">Тип: **WCHAR**</span><span class="sxs-lookup"><span data-stu-id="3655e-114">Type: **WCHAR**</span></span>

<span data-ttu-id="3655e-115">Проверяемый символ Юникода.</span><span class="sxs-lookup"><span data-stu-id="3655e-115">The Unicode character to be tested.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3655e-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3655e-116">Return value</span></span>

<span data-ttu-id="3655e-117">Тип: **bool** .</span><span class="sxs-lookup"><span data-stu-id="3655e-117">Type: **BOOL**</span></span>

<span data-ttu-id="3655e-118">Если символ является буквенно-цифровым, возвращаемое значение не равно нулю.</span><span class="sxs-lookup"><span data-stu-id="3655e-118">If the character is alphanumeric, the return value is nonzero.</span></span>

<span data-ttu-id="3655e-119">Если символ не является буквенно-цифровым, возвращаемое значение равно нулю.</span><span class="sxs-lookup"><span data-stu-id="3655e-119">If the character is not alphanumeric, the return value is zero.</span></span> <span data-ttu-id="3655e-120">Дополнительные сведения об ошибке можно получить, вызвав [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="3655e-120">To get extended error information, call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="3655e-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3655e-121">Remarks</span></span>

<span data-ttu-id="3655e-122">**Исчаралфанумерикврапв** предоставляет возможность использования строк Юникода в операционных системах, предшествующих Windows XP.</span><span class="sxs-lookup"><span data-stu-id="3655e-122">**IsCharAlphaNumericWrapW** provides the ability to use Unicode strings in operating systems earlier than Windows XP.</span></span> <span data-ttu-id="3655e-123">Предпочтительным методом является использование [**исчаралфанумерикв**](/windows/win32/api/winuser/nf-winuser-ischaralphanumerica) в сочетании с уровнем Майкрософт для Юникода (мслу).</span><span class="sxs-lookup"><span data-stu-id="3655e-123">The preferred method is to use [**IsCharAlphaNumericW**](/windows/win32/api/winuser/nf-winuser-ischaralphanumerica) in conjunction with the Microsoft Layer for Unicode (MSLU).</span></span>

<span data-ttu-id="3655e-124">**Исчаралфанумерикврапв** должен вызываться напрямую из Shlwapi.dll с порядковым номером 28.</span><span class="sxs-lookup"><span data-stu-id="3655e-124">**IsCharAlphaNumericWrapW** must be called directly from Shlwapi.dll, using ordinal 28.</span></span>

## <a name="requirements"></a><span data-ttu-id="3655e-125">Требования</span><span class="sxs-lookup"><span data-stu-id="3655e-125">Requirements</span></span>



| <span data-ttu-id="3655e-126">Требование</span><span class="sxs-lookup"><span data-stu-id="3655e-126">Requirement</span></span> | <span data-ttu-id="3655e-127">Значение</span><span class="sxs-lookup"><span data-stu-id="3655e-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3655e-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3655e-128">Minimum supported client</span></span><br/> | <span data-ttu-id="3655e-129">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="3655e-129">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3655e-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3655e-130">Minimum supported server</span></span><br/> | <span data-ttu-id="3655e-131">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3655e-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="3655e-132">DLL</span><span class="sxs-lookup"><span data-stu-id="3655e-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3655e-133"><dt>Shlwapi.dll (версия 5,0 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="3655e-133"><dt>Shlwapi.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3655e-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3655e-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3655e-135">**исчаралфанумерик**</span><span class="sxs-lookup"><span data-stu-id="3655e-135">**IsCharAlphaNumeric**</span></span>](/windows/win32/api/winuser/nf-winuser-ischaralphanumerica)
</dt> </dl>

 

 
