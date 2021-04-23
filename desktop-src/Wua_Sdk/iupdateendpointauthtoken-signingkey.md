---
description: Возвращает ключ, используемый для шифрования исходящих сообщений, которые защищает маркер.
ms.assetid: 1ADBDFC8-E4D9-440B-B310-913213086283
title: 'Метод Иупдатиндпоинтаустокен:: SigningKey (Упдатиндпоинтаус. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthToken.SigningKey
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: ae9847eb698bfcf0402a550ecb54705c4b3f3a52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072801"
---
# <a name="iupdateendpointauthtokensigningkey-method"></a><span data-ttu-id="53825-103">Метод Иупдатиндпоинтаустокен:: SigningKey</span><span class="sxs-lookup"><span data-stu-id="53825-103">IUpdateEndpointAuthToken::SigningKey method</span></span>

<span data-ttu-id="53825-104">Возвращает ключ, используемый для шифрования исходящих сообщений, которые защищает маркер.</span><span class="sxs-lookup"><span data-stu-id="53825-104">Gets the key that is used to encrypt the outgoing messages that the token protects.</span></span>

## <a name="syntax"></a><span data-ttu-id="53825-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="53825-105">Syntax</span></span>


```C++
HRESULT SigningKey(
  [in, out, unique] BYTE  *pbKey,
  [in, out]         ULONG *pcbKeySize
);
```



## <a name="parameters"></a><span data-ttu-id="53825-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="53825-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53825-107">*пбкэй* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="53825-107">*pbKey* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="53825-108">Ключ, используемый для шифрования исходящих сообщений.</span><span class="sxs-lookup"><span data-stu-id="53825-108">Key used to encrypt outgoing message.</span></span>

</dd> <dt>

<span data-ttu-id="53825-109">*пкбкэйсизе* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="53825-109">*pcbKeySize* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="53825-110">Размер ключа, на который ссылается *пбкэй* пареметер.</span><span class="sxs-lookup"><span data-stu-id="53825-110">Size of the key referenced by the *pbkey* paremeter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53825-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="53825-111">Return value</span></span>

<span data-ttu-id="53825-112">При успешном выполнении возвращает значение **\_ ОК** .</span><span class="sxs-lookup"><span data-stu-id="53825-112">Returns **S\_OK** if successful.</span></span> <span data-ttu-id="53825-113">В противном случае возвращает код ошибки COM или Windows.</span><span class="sxs-lookup"><span data-stu-id="53825-113">Otherwise, returns a COM or Windows error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="53825-114">Требования</span><span class="sxs-lookup"><span data-stu-id="53825-114">Requirements</span></span>



| <span data-ttu-id="53825-115">Требование</span><span class="sxs-lookup"><span data-stu-id="53825-115">Requirement</span></span> | <span data-ttu-id="53825-116">Значение</span><span class="sxs-lookup"><span data-stu-id="53825-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="53825-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="53825-117">Minimum supported client</span></span><br/> | <span data-ttu-id="53825-118">Windows XP, Windows 2000 Professional с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="53825-118">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="53825-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="53825-119">Minimum supported server</span></span><br/> | <span data-ttu-id="53825-120">Windows Server 2003, Windows 2000 Server с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="53825-120">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="53825-121">Header</span><span class="sxs-lookup"><span data-stu-id="53825-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="53825-122"><dt>Упдатиндпоинтаус. h</dt></span><span class="sxs-lookup"><span data-stu-id="53825-122"><dt>UpdateEndpointAuth.h</dt></span></span> </dl>   |
| <span data-ttu-id="53825-123">IDL</span><span class="sxs-lookup"><span data-stu-id="53825-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="53825-124"><dt>Упдатиндпоинтаус. idl</dt></span><span class="sxs-lookup"><span data-stu-id="53825-124"><dt>UpdateEndpointAuth.idl</dt></span></span> </dl> |
| <span data-ttu-id="53825-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="53825-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="53825-126"><dt>Упдатиндпоинтаус. lib</dt></span><span class="sxs-lookup"><span data-stu-id="53825-126"><dt>UpdateEndpointAuth.lib</dt></span></span> </dl> |
| <span data-ttu-id="53825-127">DLL</span><span class="sxs-lookup"><span data-stu-id="53825-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="53825-128"><dt>UpdateEndpointAuth.dll</dt></span><span class="sxs-lookup"><span data-stu-id="53825-128"><dt>UpdateEndpointAuth.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53825-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="53825-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53825-130">**иупдатиндпоинтаустокен**</span><span class="sxs-lookup"><span data-stu-id="53825-130">**IUpdateEndpointAuthToken**</span></span>](iupdateendpointauthtoken.md)
</dt> </dl>

 

 




