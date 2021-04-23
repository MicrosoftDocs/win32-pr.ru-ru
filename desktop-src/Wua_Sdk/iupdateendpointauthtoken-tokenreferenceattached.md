---
description: Возвращает XML-формат присоединенной ссылки на токен.
ms.assetid: F4329A2E-61FD-40E0-9E24-87C9A4585E55
title: 'Метод Иупдатиндпоинтаустокен:: Токенреференцеаттачед (Упдатиндпоинтаус. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthToken.TokenReferenceAttached
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: 9582c54c42e2416d5d7a98e85eba3151fd6769a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682760"
---
# <a name="iupdateendpointauthtokentokenreferenceattached-method"></a><span data-ttu-id="5d045-103">Метод Иупдатиндпоинтаустокен:: Токенреференцеаттачед</span><span class="sxs-lookup"><span data-stu-id="5d045-103">IUpdateEndpointAuthToken::TokenReferenceAttached method</span></span>

<span data-ttu-id="5d045-104">Возвращает XML-формат присоединенной ссылки на токен.</span><span class="sxs-lookup"><span data-stu-id="5d045-104">Gets the XML format of an attached reference to the token.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d045-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5d045-105">Syntax</span></span>


```C++
HRESULT TokenReferenceAttached(
  [out] BSTR *pszTokenReference
);
```



## <a name="parameters"></a><span data-ttu-id="5d045-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5d045-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d045-107">*псзтокенреференце* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="5d045-107">*pszTokenReference* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5d045-108">Указатель на ссылку на присоединенный маркер.</span><span class="sxs-lookup"><span data-stu-id="5d045-108">Pointer to the attached token reference.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d045-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5d045-109">Return value</span></span>

<span data-ttu-id="5d045-110">При успешном выполнении возвращает значение **\_ ОК** .</span><span class="sxs-lookup"><span data-stu-id="5d045-110">Returns **S\_OK** if successful.</span></span> <span data-ttu-id="5d045-111">В противном случае возвращает код ошибки COM или Windows.</span><span class="sxs-lookup"><span data-stu-id="5d045-111">Otherwise, returns a COM or Windows error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="5d045-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5d045-112">Remarks</span></span>

<span data-ttu-id="5d045-113">Присоединенная ссылка указывает на рефереце (например, сигнитуре, который использует токен), который находится в том же сообщении, где находится маркер.</span><span class="sxs-lookup"><span data-stu-id="5d045-113">An attached reference refers a referece (such as the signiture that is using the token) that is in the same message where the token resides.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d045-114">Требования</span><span class="sxs-lookup"><span data-stu-id="5d045-114">Requirements</span></span>



| <span data-ttu-id="5d045-115">Требование</span><span class="sxs-lookup"><span data-stu-id="5d045-115">Requirement</span></span> | <span data-ttu-id="5d045-116">Значение</span><span class="sxs-lookup"><span data-stu-id="5d045-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d045-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5d045-117">Minimum supported client</span></span><br/> | <span data-ttu-id="5d045-118">Windows XP, Windows 2000 Professional с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="5d045-118">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="5d045-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5d045-119">Minimum supported server</span></span><br/> | <span data-ttu-id="5d045-120">Windows Server 2003, Windows 2000 Server с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="5d045-120">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="5d045-121">Header</span><span class="sxs-lookup"><span data-stu-id="5d045-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="5d045-122"><dt>Упдатиндпоинтаус. h</dt></span><span class="sxs-lookup"><span data-stu-id="5d045-122"><dt>UpdateEndpointAuth.h</dt></span></span> </dl>   |
| <span data-ttu-id="5d045-123">IDL</span><span class="sxs-lookup"><span data-stu-id="5d045-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5d045-124"><dt>Упдатиндпоинтаус. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5d045-124"><dt>UpdateEndpointAuth.idl</dt></span></span> </dl> |
| <span data-ttu-id="5d045-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="5d045-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="5d045-126"><dt>Упдатиндпоинтаус. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5d045-126"><dt>UpdateEndpointAuth.lib</dt></span></span> </dl> |
| <span data-ttu-id="5d045-127">DLL</span><span class="sxs-lookup"><span data-stu-id="5d045-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5d045-128"><dt>UpdateEndpointAuth.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5d045-128"><dt>UpdateEndpointAuth.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d045-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5d045-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d045-130">**иупдатиндпоинтаустокен**</span><span class="sxs-lookup"><span data-stu-id="5d045-130">**IUpdateEndpointAuthToken**</span></span>](iupdateendpointauthtoken.md)
</dt> </dl>

 

 




