---
description: Уменьшает ссылки на поставщик протокола SSL (SSL).
ms.assetid: 67bfa4b5-c02c-4a76-871d-93f3bf4e3602
title: Функция Сслдекрементпровидерреференцекаунт (Сслпровидер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslDecrementProviderReferenceCount
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 4d3fe072c02f22b713115dd5191b0b5e0cedbb37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991619"
---
# <a name="ssldecrementproviderreferencecount-function"></a><span data-ttu-id="e5a61-103">Функция Сслдекрементпровидерреференцекаунт</span><span class="sxs-lookup"><span data-stu-id="e5a61-103">SslDecrementProviderReferenceCount function</span></span>

<span data-ttu-id="e5a61-104">Функция **сслдекрементпровидерреференцекаунт** уменьшает ссылки на поставщик [*протокола SSL*](/windows/desktop/SecGloss/s-gly) (SSL).</span><span class="sxs-lookup"><span data-stu-id="e5a61-104">The **SslDecrementProviderReferenceCount** function decrements the references to the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) provider.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5a61-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e5a61-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslDecrementProviderReferenceCount(
  _In_ NCRYPT_PROV_HANDLE hSslProvider
);
```



## <a name="parameters"></a><span data-ttu-id="e5a61-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e5a61-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5a61-107">*хсслпровидер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e5a61-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5a61-108">Маркер экземпляра поставщика протокола SSL.</span><span class="sxs-lookup"><span data-stu-id="e5a61-108">The handle of the SSL protocol provider instance.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5a61-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e5a61-109">Return value</span></span>

<span data-ttu-id="e5a61-110">Если функция завершается с ошибкой, она возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="e5a61-110">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="e5a61-111">Если функция завершается ошибкой, она возвращает ненулевое значение ошибки.</span><span class="sxs-lookup"><span data-stu-id="e5a61-111">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="e5a61-112">Возможные коды возврата включают, но не ограничиваются следующим.</span><span class="sxs-lookup"><span data-stu-id="e5a61-112">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="e5a61-113">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="e5a61-113">Return code/value</span></span>                                                                                                                                                        | <span data-ttu-id="e5a61-114">Описание</span><span class="sxs-lookup"><span data-stu-id="e5a61-114">Description</span></span>                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="e5a61-115"><dt> **\_ Недопустимое \_ состояние**</dt> <dt>0xC0000008L</dt> Handle</span><span class="sxs-lookup"><span data-stu-id="e5a61-115"><dt>**STATUS\_INVALID\_HANDLE** </dt> <dt>0xC0000008L</dt></span></span> </dl> | <span data-ttu-id="e5a61-116">Недопустимый маркер поставщика SSL.</span><span class="sxs-lookup"><span data-stu-id="e5a61-116">The SSL provider handle is not valid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="e5a61-117">Требования</span><span class="sxs-lookup"><span data-stu-id="e5a61-117">Requirements</span></span>



| <span data-ttu-id="e5a61-118">Требование</span><span class="sxs-lookup"><span data-stu-id="e5a61-118">Requirement</span></span> | <span data-ttu-id="e5a61-119">Значение</span><span class="sxs-lookup"><span data-stu-id="e5a61-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5a61-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e5a61-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e5a61-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e5a61-121">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="e5a61-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e5a61-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e5a61-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e5a61-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="e5a61-124">Header</span><span class="sxs-lookup"><span data-stu-id="e5a61-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="e5a61-125"><dt>Сслпровидер. h</dt></span><span class="sxs-lookup"><span data-stu-id="e5a61-125"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="e5a61-126">DLL</span><span class="sxs-lookup"><span data-stu-id="e5a61-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e5a61-127"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e5a61-127"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

