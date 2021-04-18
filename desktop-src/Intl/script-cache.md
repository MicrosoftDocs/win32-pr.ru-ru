---
description: Определяет кэш метрик шрифтов Uniscribe.
ms.assetid: 56a98529-6ae9-4b71-bd7d-cf056a1e3683
title: SCRIPT_CACHE (usp10. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ece29fe0ed610b4576263c36c50311ef57317579
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105651114"
---
# <a name="script_cache"></a><span data-ttu-id="5b76c-103">\_кэш скриптов</span><span class="sxs-lookup"><span data-stu-id="5b76c-103">SCRIPT\_CACHE</span></span>

<span data-ttu-id="5b76c-104">Определяет кэш метрик шрифтов Uniscribe.</span><span class="sxs-lookup"><span data-stu-id="5b76c-104">Defines a Uniscribe font metric cache.</span></span>


```C++
typedef void* SCRIPT_CACHE;
```



## <a name="remarks"></a><span data-ttu-id="5b76c-105">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5b76c-105">Remarks</span></span>

<span data-ttu-id="5b76c-106">Это непрозрачная структура.</span><span class="sxs-lookup"><span data-stu-id="5b76c-106">This is an opaque structure.</span></span> <span data-ttu-id="5b76c-107">Приложение должно выделить и хранить одну \_ переменную кэша скрипта для каждого используемого стиля символов.</span><span class="sxs-lookup"><span data-stu-id="5b76c-107">The application must allocate and retain one SCRIPT\_CACHE variable for each character style used.</span></span> <span data-ttu-id="5b76c-108">Переменная должна быть инициализирована **значением NULL**.</span><span class="sxs-lookup"><span data-stu-id="5b76c-108">The variable must be initialized to **NULL**.</span></span>

<span data-ttu-id="5b76c-109">Многие функции скрипта используют сочетание дескриптора контекста аппаратного устройства и \_ переменной кэша скрипта.</span><span class="sxs-lookup"><span data-stu-id="5b76c-109">Many script functions take a combination of a hardware device context handle and a SCRIPT\_CACHE variable.</span></span> <span data-ttu-id="5b76c-110">Uniscribe сначала пытается получить доступ к данным шрифта с помощью \_ переменной кэша скрипта.</span><span class="sxs-lookup"><span data-stu-id="5b76c-110">Uniscribe first attempts to access font data by using the SCRIPT\_CACHE variable.</span></span> <span data-ttu-id="5b76c-111">Он проверяет контекст устройства оборудования только в том случае, если необходимые данные еще не кэшированы.</span><span class="sxs-lookup"><span data-stu-id="5b76c-111">It only inspects the hardware device context if the required data is not already cached.</span></span>

<span data-ttu-id="5b76c-112">Маркер контекста аппаратного устройства может быть передан Uniscribe как **null**.</span><span class="sxs-lookup"><span data-stu-id="5b76c-112">The hardware device context handle can be passed to Uniscribe as **NULL**.</span></span> <span data-ttu-id="5b76c-113">Если данные, необходимые для Uniscribe, уже кэшированы, контекст устройства недоступен, и операция продолжится нормально.</span><span class="sxs-lookup"><span data-stu-id="5b76c-113">If data required by Uniscribe is already cached, the device context is not accessed, and the operation continues normally.</span></span>

<span data-ttu-id="5b76c-114">Если контекст устройства передается как **значение NULL** , а Uniscribe — по любой причине, Uniscribe возвращает код ошибки E \_ Pending.</span><span class="sxs-lookup"><span data-stu-id="5b76c-114">If the device context is passed as **NULL** and Uniscribe needs to access it for any reason, Uniscribe returns the error code E\_PENDING.</span></span> <span data-ttu-id="5b76c-115">Этот код быстро возвращается, позволяя приложению избежать требующих много времени вызовов [**SelectObject**](/windows/win32/api/wingdi/nf-wingdi-selectobject) .</span><span class="sxs-lookup"><span data-stu-id="5b76c-115">This code is returned quickly, allowing the application to avoid time-consuming [**SelectObject**](/windows/win32/api/wingdi/nf-wingdi-selectobject) calls.</span></span>

## <a name="examples"></a><span data-ttu-id="5b76c-116">Примеры</span><span class="sxs-lookup"><span data-stu-id="5b76c-116">Examples</span></span>

<span data-ttu-id="5b76c-117">Следующий пример применяется ко всем функциям, которые принимают \_ переменную кэша скрипта и дополнительный дескриптор контекста аппаратного устройства.</span><span class="sxs-lookup"><span data-stu-id="5b76c-117">The following example applies to all functions that take a SCRIPT\_CACHE variable and an optional handle to a hardware device context.</span></span>


```C++
hr = ScriptShape(NULL, &sc,
                 pwcChars, cChars, cMaxGlyphs, psa, pwOutGlyphs, pwLogClust, psva, pcGlyphs);
if (hr == E_PENDING)
{
    // ... select font into hdc ...
    hr = ScriptShape(hdc, &sc,
                 pwcChars, cChars, cMaxGlyphs, psa, pwOutGlyphs, pwLogClust, psva, pcGlyphs);
}
```



## <a name="requirements"></a><span data-ttu-id="5b76c-118">Требования</span><span class="sxs-lookup"><span data-stu-id="5b76c-118">Requirements</span></span>



| <span data-ttu-id="5b76c-119">Требование</span><span class="sxs-lookup"><span data-stu-id="5b76c-119">Requirement</span></span> | <span data-ttu-id="5b76c-120">Значение</span><span class="sxs-lookup"><span data-stu-id="5b76c-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5b76c-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5b76c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="5b76c-122">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="5b76c-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="5b76c-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5b76c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="5b76c-124">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="5b76c-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="5b76c-125">Заголовок</span><span class="sxs-lookup"><span data-stu-id="5b76c-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="5b76c-126"><dt>Usp10. h</dt></span><span class="sxs-lookup"><span data-stu-id="5b76c-126"><dt>Usp10.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b76c-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5b76c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b76c-128">Uniscribe</span><span class="sxs-lookup"><span data-stu-id="5b76c-128">Uniscribe</span></span>](uniscribe.md)
</dt> <dt>

[<span data-ttu-id="5b76c-129">Структуры Uniscribe</span><span class="sxs-lookup"><span data-stu-id="5b76c-129">Uniscribe Structures</span></span>](uniscribe-structures.md)
</dt> <dt>

[<span data-ttu-id="5b76c-130">Кэширование</span><span class="sxs-lookup"><span data-stu-id="5b76c-130">Caching</span></span>](caching.md)
</dt> </dl>

 

 
