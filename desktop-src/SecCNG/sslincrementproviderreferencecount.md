---
description: Увеличивает значение счетчика ссылок на экземпляр поставщика SSL протокола (SSL).
ms.assetid: 67e7b8b4-b073-4936-b1e0-3fc7c1c011a2
title: Функция Сслинкрементпровидерреференцекаунт (Сслпровидер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslIncrementProviderReferenceCount
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 862697035d978db082c303c6e1df6f2a444d8be3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664649"
---
# <a name="sslincrementproviderreferencecount-function"></a><span data-ttu-id="84377-103">Функция Сслинкрементпровидерреференцекаунт</span><span class="sxs-lookup"><span data-stu-id="84377-103">SslIncrementProviderReferenceCount function</span></span>

<span data-ttu-id="84377-104">Функция **сслинкрементпровидерреференцекаунт** увеличивает значение счетчика ссылок на экземпляр поставщика [*SSL протокола*](/windows/desktop/SecGloss/s-gly) (SSL).</span><span class="sxs-lookup"><span data-stu-id="84377-104">The **SslIncrementProviderReferenceCount** function increments the reference count to a [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) provider instance.</span></span>

## <a name="syntax"></a><span data-ttu-id="84377-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="84377-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslIncrementProviderReferenceCount(
  _In_ NCRYPT_PROV_HANDLE hSslProvider
);
```



## <a name="parameters"></a><span data-ttu-id="84377-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="84377-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84377-107">*хсслпровидер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="84377-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84377-108">Обработчик для экземпляра поставщика протокола SSL.</span><span class="sxs-lookup"><span data-stu-id="84377-108">The handle to the SSL protocol provider instance.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84377-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="84377-109">Return value</span></span>

<span data-ttu-id="84377-110">Если функция завершается с ошибкой, она возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="84377-110">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="84377-111">Если функция завершается ошибкой, она возвращает ненулевое значение ошибки.</span><span class="sxs-lookup"><span data-stu-id="84377-111">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="84377-112">Возможные коды возврата включают, но не ограничиваются следующим.</span><span class="sxs-lookup"><span data-stu-id="84377-112">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="84377-113">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="84377-113">Return code/value</span></span>                                                                                                                                                    | <span data-ttu-id="84377-114">Описание</span><span class="sxs-lookup"><span data-stu-id="84377-114">Description</span></span>                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="84377-115">Не <dt>**превышать \_ Недопустимый 0x80090026L \_ Handle**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="84377-115"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl> | <span data-ttu-id="84377-116">Недопустимый маркер *хсслпровидер* .</span><span class="sxs-lookup"><span data-stu-id="84377-116">The *hSslProvider* handle is not valid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="84377-117">Требования</span><span class="sxs-lookup"><span data-stu-id="84377-117">Requirements</span></span>



| <span data-ttu-id="84377-118">Требование</span><span class="sxs-lookup"><span data-stu-id="84377-118">Requirement</span></span> | <span data-ttu-id="84377-119">Значение</span><span class="sxs-lookup"><span data-stu-id="84377-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="84377-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="84377-120">Minimum supported client</span></span><br/> | <span data-ttu-id="84377-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="84377-121">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="84377-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="84377-122">Minimum supported server</span></span><br/> | <span data-ttu-id="84377-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="84377-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="84377-124">Header</span><span class="sxs-lookup"><span data-stu-id="84377-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="84377-125"><dt>Сслпровидер. h</dt></span><span class="sxs-lookup"><span data-stu-id="84377-125"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="84377-126">DLL</span><span class="sxs-lookup"><span data-stu-id="84377-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="84377-127"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="84377-127"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

