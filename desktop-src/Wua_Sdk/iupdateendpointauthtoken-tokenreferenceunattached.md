---
description: Возвращает XML-формат неприсоединенной ссылки на токен.
ms.assetid: D5D61ED7-68FB-4FC0-9C2A-90D3B1219351
title: 'Метод Иупдатиндпоинтаустокен:: Токенреференцеунаттачед (Упдатиндпоинтаус. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthToken.TokenReferenceUnattached
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: 7f9a25c444cf1ba8421d3787a9ead242750e5756
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701631"
---
# <a name="iupdateendpointauthtokentokenreferenceunattached-method"></a><span data-ttu-id="a22b8-103">Метод Иупдатиндпоинтаустокен:: Токенреференцеунаттачед</span><span class="sxs-lookup"><span data-stu-id="a22b8-103">IUpdateEndpointAuthToken::TokenReferenceUnattached method</span></span>

<span data-ttu-id="a22b8-104">Возвращает XML-формат неприсоединенной ссылки на токен.</span><span class="sxs-lookup"><span data-stu-id="a22b8-104">Gets the XML format of an unattached reference to the token.</span></span>

## <a name="syntax"></a><span data-ttu-id="a22b8-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a22b8-105">Syntax</span></span>


```C++
HRESULT TokenReferenceUnattached(
  [out] BSTR *pszTokenReference
);
```



## <a name="parameters"></a><span data-ttu-id="a22b8-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a22b8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a22b8-107">*псзтокенреференце* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="a22b8-107">*pszTokenReference* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a22b8-108">Указатель на неприсоединенную ссылку на маркер.</span><span class="sxs-lookup"><span data-stu-id="a22b8-108">Pointer to the unattached token reference.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a22b8-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a22b8-109">Return value</span></span>

<span data-ttu-id="a22b8-110">При успешном выполнении возвращает значение **\_ ОК** .</span><span class="sxs-lookup"><span data-stu-id="a22b8-110">Returns **S\_OK** if successful.</span></span> <span data-ttu-id="a22b8-111">В противном случае возвращает код ошибки COM или Windows.</span><span class="sxs-lookup"><span data-stu-id="a22b8-111">Otherwise, returns a COM or Windows error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a22b8-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a22b8-112">Remarks</span></span>

<span data-ttu-id="a22b8-113">Неприсоединенная ссылка указывает на рефереце (например, сигнитуре, который использует маркер), не находящийся в сообщении, где находится маркер.</span><span class="sxs-lookup"><span data-stu-id="a22b8-113">An unattached reference refers a referece (such as the signiture that is using the token) that is not in the message where the token resides.</span></span>

## <a name="requirements"></a><span data-ttu-id="a22b8-114">Требования</span><span class="sxs-lookup"><span data-stu-id="a22b8-114">Requirements</span></span>



| <span data-ttu-id="a22b8-115">Требование</span><span class="sxs-lookup"><span data-stu-id="a22b8-115">Requirement</span></span> | <span data-ttu-id="a22b8-116">Значение</span><span class="sxs-lookup"><span data-stu-id="a22b8-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a22b8-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a22b8-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a22b8-118">Windows XP, Windows 2000 Professional с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a22b8-118">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="a22b8-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a22b8-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a22b8-120">Windows Server 2003, Windows 2000 Server с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a22b8-120">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="a22b8-121">Header</span><span class="sxs-lookup"><span data-stu-id="a22b8-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="a22b8-122"><dt>Упдатиндпоинтаус. h</dt></span><span class="sxs-lookup"><span data-stu-id="a22b8-122"><dt>UpdateEndpointAuth.h</dt></span></span> </dl>   |
| <span data-ttu-id="a22b8-123">IDL</span><span class="sxs-lookup"><span data-stu-id="a22b8-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a22b8-124"><dt>Упдатиндпоинтаус. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a22b8-124"><dt>UpdateEndpointAuth.idl</dt></span></span> </dl> |
| <span data-ttu-id="a22b8-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a22b8-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="a22b8-126"><dt>Упдатиндпоинтаус. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a22b8-126"><dt>UpdateEndpointAuth.lib</dt></span></span> </dl> |
| <span data-ttu-id="a22b8-127">DLL</span><span class="sxs-lookup"><span data-stu-id="a22b8-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a22b8-128"><dt>UpdateEndpointAuth.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a22b8-128"><dt>UpdateEndpointAuth.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a22b8-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a22b8-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a22b8-130">**иупдатиндпоинтаустокен**</span><span class="sxs-lookup"><span data-stu-id="a22b8-130">**IUpdateEndpointAuthToken**</span></span>](iupdateendpointauthtoken.md)
</dt> </dl>

 

 




