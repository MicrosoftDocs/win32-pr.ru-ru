---
description: Определяет, установлен или поддерживается ли языковой стандарт, заданный по имени, в операционной системе.
ms.assetid: 6df92e4d-d78e-48b5-9515-18f0497de95b
title: Функция Ртлисвалидлокаленаме (Нтртл. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlIsValidLocaleName
api_type:
- DllExport
api_location:
- Kernel32.dll
ms.openlocfilehash: 3433daaf48e81f662945f1d223e9cf7188ddb706
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897221"
---
# <a name="rtlisvalidlocalename-function"></a><span data-ttu-id="ac92f-103">Функция Ртлисвалидлокаленаме</span><span class="sxs-lookup"><span data-stu-id="ac92f-103">RtlIsValidLocaleName function</span></span>

<span data-ttu-id="ac92f-104">Определяет, установлен или поддерживается ли языковой стандарт, заданный по имени, в операционной системе.</span><span class="sxs-lookup"><span data-stu-id="ac92f-104">Determines if a locale specified by name is installed or supported on the operating system.</span></span>

> [!Note]  
> <span data-ttu-id="ac92f-105">Эта функция доступна только для использования в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="ac92f-105">This function is available for use in Windows Vista only.</span></span> <span data-ttu-id="ac92f-106">Он может быть изменен или недоступен в последующих версиях.</span><span class="sxs-lookup"><span data-stu-id="ac92f-106">It might be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="ac92f-107">Приложения должны использовать [**исвалидлокаленаме**](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename).</span><span class="sxs-lookup"><span data-stu-id="ac92f-107">Applications should use [**IsValidLocaleName**](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="ac92f-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ac92f-108">Syntax</span></span>


```C++
BOOL RtlIsValidLocaleName(
  _In_ LPCWSTR LocaleName,
  _In_ ULONG   Flags
);
```



## <a name="parameters"></a><span data-ttu-id="ac92f-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="ac92f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac92f-110">*LocaleName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ac92f-110">*LocaleName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac92f-111">[Имя языкового стандарта](locale-names.md) для проверки.</span><span class="sxs-lookup"><span data-stu-id="ac92f-111">[Locale name](locale-names.md) to validate.</span></span> <span data-ttu-id="ac92f-112">Этот параметр может указывать имя [пользовательского языкового стандарта](custom-locales.md).</span><span class="sxs-lookup"><span data-stu-id="ac92f-112">This parameter can specify the name of a [custom locale](custom-locales.md).</span></span>

</dd> <dt>

<span data-ttu-id="ac92f-113">*Флаги* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ac92f-113">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac92f-114">Флаги, указывающие, считаются ли Нейтральные языковые стандарты допустимыми.</span><span class="sxs-lookup"><span data-stu-id="ac92f-114">Flags indicating if neutral locales are considered valid.</span></span> <span data-ttu-id="ac92f-115">В настоящее время единственным определенным флагом является [языковой стандарт, \_ допускающий \_ нейтральные](locale-allow-neutral.md).</span><span class="sxs-lookup"><span data-stu-id="ac92f-115">Currently the only defined flag is [LOCALE\_ALLOW\_NEUTRAL](locale-allow-neutral.md).</span></span> <span data-ttu-id="ac92f-116">Значение по умолчанию — нет.</span><span class="sxs-lookup"><span data-stu-id="ac92f-116">The default value is that they are not.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac92f-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ac92f-117">Return value</span></span>

<span data-ttu-id="ac92f-118">При успешном выполнении возвращает ненулевое значение или 0 в противном случае.</span><span class="sxs-lookup"><span data-stu-id="ac92f-118">Returns a nonzero value if successful, or 0 otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="ac92f-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ac92f-119">Remarks</span></span>

<span data-ttu-id="ac92f-120">Эта функция похожа на [**исвалидлокаленаме**](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename).</span><span class="sxs-lookup"><span data-stu-id="ac92f-120">This function is similar to [**IsValidLocaleName**](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename).</span></span> <span data-ttu-id="ac92f-121">Единственное отличие заключается в том, что \_ Если \_ параметр locale разрешен нейтральный, **Ртлисвалидлокаленаме** возвращает **значение true** для имени, которое соответствует нейтральной национальной настройке (например, EN), тогда как [**исвалидлокаленаме**](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename) возвращает **значение true** только для определенного языкового стандарта (например, EN-US).</span><span class="sxs-lookup"><span data-stu-id="ac92f-121">The only difference is that if LOCALE\_ALLOW\_NEUTRAL is set, **RtlIsValidLocaleName** returns **TRUE** for a name that corresponds to a neutral locale (such as "en"), while [**IsValidLocaleName**](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename) returns **TRUE** only for a specific locale (such as "en-US").</span></span> <span data-ttu-id="ac92f-122">Нейтральные языковые стандарты используются в рамках стратегии загрузки ресурсов в Windows Vista и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="ac92f-122">Neutral locales are used as part of the resource loading strategy in Windows Vista and later.</span></span> <span data-ttu-id="ac92f-123">Только небольшой класс строго специализированных приложений используют **ртлисвалидлокаленаме** и Set locale \_ разрешают \_ нейтральные, поскольку Нейтральные языковые стандарты имеют очень ограниченный объем использования.</span><span class="sxs-lookup"><span data-stu-id="ac92f-123">Only a small class of highly specialized applications use **RtlIsValidLocaleName** and set LOCALE\_ALLOW\_NEUTRAL, because neutral locales are of very limited use.</span></span> <span data-ttu-id="ac92f-124">Ни одна из функций, описанных при [вызове функций "locale Name"](calling-the--locale-name--functions.md) , не принимает в качестве входных данных Нейтральные языковые стандарты.</span><span class="sxs-lookup"><span data-stu-id="ac92f-124">None of the functions described in [Calling the "Locale Name" Functions](calling-the--locale-name--functions.md) accept neutral locales as inputs.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac92f-125">Требования</span><span class="sxs-lookup"><span data-stu-id="ac92f-125">Requirements</span></span>



| <span data-ttu-id="ac92f-126">Требование</span><span class="sxs-lookup"><span data-stu-id="ac92f-126">Requirement</span></span> | <span data-ttu-id="ac92f-127">Значение</span><span class="sxs-lookup"><span data-stu-id="ac92f-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ac92f-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ac92f-128">Minimum supported client</span></span><br/> | <span data-ttu-id="ac92f-129">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ac92f-129">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="ac92f-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ac92f-130">Minimum supported server</span></span><br/> | <span data-ttu-id="ac92f-131">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ac92f-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ac92f-132">Header</span><span class="sxs-lookup"><span data-stu-id="ac92f-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="ac92f-133"><dt>Нтртл. h</dt></span><span class="sxs-lookup"><span data-stu-id="ac92f-133"><dt>Ntrtl.h</dt></span></span> </dl>      |
| <span data-ttu-id="ac92f-134">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ac92f-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="ac92f-135"><dt>Kernel32.lib</dt></span><span class="sxs-lookup"><span data-stu-id="ac92f-135"><dt>Kernel32.lib</dt></span></span> </dl> |
| <span data-ttu-id="ac92f-136">DLL</span><span class="sxs-lookup"><span data-stu-id="ac92f-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ac92f-137"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ac92f-137"><dt>Kernel32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac92f-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ac92f-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac92f-139">Поддержка национальных языков</span><span class="sxs-lookup"><span data-stu-id="ac92f-139">National Language Support</span></span>](national-language-support.md)
</dt> <dt>

[<span data-ttu-id="ac92f-140">Функции поддержки национальных языков</span><span class="sxs-lookup"><span data-stu-id="ac92f-140">National Language Support Functions</span></span>](national-language-support-functions.md)
</dt> <dt>

[<span data-ttu-id="ac92f-141">**исвалидлокаленаме**</span><span class="sxs-lookup"><span data-stu-id="ac92f-141">**IsValidLocaleName**</span></span>](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename)
</dt> </dl>

 

 




