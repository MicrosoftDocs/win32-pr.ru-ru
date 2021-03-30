---
title: Тип конфиденциальности (WinInet. h)
description: Указывает, что параметры конфиденциальности предназначены для файлов cookie первого или сторонних поставщиков.
ms.assetid: 7d0846d4-fd81-4af9-b7e6-05c4c1438770
topic_type:
- apiref
api_name:
- PRIVACY_TYPE_FIRST_PARTY
- PRIVACY_TYPE_THIRD_PARTY
api_location:
- Wininet.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38583d5f0c5cee148353f98f5d2be2d4f1a50216
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892726"
---
# <a name="privacy-type"></a><span data-ttu-id="4f812-103">Тип конфиденциальности</span><span class="sxs-lookup"><span data-stu-id="4f812-103">Privacy Type</span></span>

<span data-ttu-id="4f812-104">Указывает, что параметры конфиденциальности предназначены для файлов cookie первого или сторонних поставщиков.</span><span class="sxs-lookup"><span data-stu-id="4f812-104">Specifies that privacy settings are for either first-party or third-party cookies.</span></span>

<dl> <dt>

<span data-ttu-id="4f812-105"><span id="PRIVACY_TYPE_FIRST_PARTY"></span><span id="privacy_type_first_party"></span>**\_тип конфиденциальности \_ First \_ вечеринка**</span><span class="sxs-lookup"><span data-stu-id="4f812-105"><span id="PRIVACY_TYPE_FIRST_PARTY"></span><span id="privacy_type_first_party"></span>**PRIVACY\_TYPE\_FIRST\_PARTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f812-106">0</span><span class="sxs-lookup"><span data-stu-id="4f812-106">0</span></span>
</dt> <dt>



<span data-ttu-id="4f812-107">Относится к параметрам конфиденциальности для файлов cookie первого производителя.</span><span class="sxs-lookup"><span data-stu-id="4f812-107">Refers to privacy settings for first party cookies.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4f812-108"><span id="PRIVACY_TYPE_THIRD_PARTY"></span><span id="privacy_type_third_party"></span>**\_тип конфиденциальности \_ третья \_ сторона**</span><span class="sxs-lookup"><span data-stu-id="4f812-108"><span id="PRIVACY_TYPE_THIRD_PARTY"></span><span id="privacy_type_third_party"></span>**PRIVACY\_TYPE\_THIRD\_PARTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f812-109">1</span><span class="sxs-lookup"><span data-stu-id="4f812-109">1</span></span>
</dt> <dt>



<span data-ttu-id="4f812-110">Относится к параметрам конфиденциальности для файлов cookie сторонних производителей.</span><span class="sxs-lookup"><span data-stu-id="4f812-110">Refers to privacy settings for third party cookies.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4f812-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4f812-111">Remarks</span></span>

<span data-ttu-id="4f812-112">Файлы cookie классифицируются как первая сторона и третья сторона.</span><span class="sxs-lookup"><span data-stu-id="4f812-112">Cookies are categorized as first-party and third-party.</span></span> <span data-ttu-id="4f812-113">Первичный файл cookie — это тот, который поступает из домена узла.</span><span class="sxs-lookup"><span data-stu-id="4f812-113">A first-party cookie is one that originates from the host domain.</span></span> <span data-ttu-id="4f812-114">Если https://www.blueyonderairlines.com в адресной строке Microsoft Internet Explorer обнаружено значение "", то "www.blueyonderairlines.com" является доменом узла.</span><span class="sxs-lookup"><span data-stu-id="4f812-114">If "https://www.blueyonderairlines.com" is found in the Microsoft Internet Explorer address bar, "www.blueyonderairlines.com" is the host domain.</span></span> <span data-ttu-id="4f812-115">При посещении этой страницы, если файл cookie задан из домена, отличного от "www.blueyonderairlines.com", например "www.fourthcoffee.com", этот файл cookie считается сторонним файлом cookie.</span><span class="sxs-lookup"><span data-stu-id="4f812-115">While visiting this page, if a cookie is set from a domain other than "www.blueyonderairlines.com", such as "www.fourthcoffee.com", this cookie is considered a third-party cookie.</span></span>

> [!Note]  
> <span data-ttu-id="4f812-116">WinINet не поддерживает реализации серверов.</span><span class="sxs-lookup"><span data-stu-id="4f812-116">WinINet does not support server implementations.</span></span> <span data-ttu-id="4f812-117">Кроме того, его не следует использовать из службы.</span><span class="sxs-lookup"><span data-stu-id="4f812-117">In addition, it should not be used from a service.</span></span> <span data-ttu-id="4f812-118">Для серверных реализаций или служб используйте [службы Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="4f812-118">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4f812-119">Требования</span><span class="sxs-lookup"><span data-stu-id="4f812-119">Requirements</span></span>



| <span data-ttu-id="4f812-120">Требование</span><span class="sxs-lookup"><span data-stu-id="4f812-120">Requirement</span></span> | <span data-ttu-id="4f812-121">Значение</span><span class="sxs-lookup"><span data-stu-id="4f812-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="4f812-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4f812-122">Minimum supported client</span></span><br/> | <span data-ttu-id="4f812-123">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="4f812-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="4f812-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4f812-124">Minimum supported server</span></span><br/> | <span data-ttu-id="4f812-125">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="4f812-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="4f812-126">Заголовок</span><span class="sxs-lookup"><span data-stu-id="4f812-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="4f812-127"><dt>WinInet. h</dt></span><span class="sxs-lookup"><span data-stu-id="4f812-127"><dt>Wininet.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f812-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4f812-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f812-129">**привацижетзонепреференцев**</span><span class="sxs-lookup"><span data-stu-id="4f812-129">**PrivacyGetZonePreferenceW**</span></span>](/windows/win32/api/winineti/nf-winineti-privacygetzonepreferencew)
</dt> <dt>

[<span data-ttu-id="4f812-130">**привацисетзонепреференцев**</span><span class="sxs-lookup"><span data-stu-id="4f812-130">**PrivacySetZonePreferenceW**</span></span>](/windows/win32/api/winineti/nf-winineti-privacysetzonepreferencew)
</dt> </dl>

 

