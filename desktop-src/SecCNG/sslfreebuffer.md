---
description: Используется для освобождения памяти, выделенной одной из функций поставщика SSL протокола (SSL).
ms.assetid: 75a85013-c745-43cb-85b5-e13a2778ec1d
title: Функция Сслфрибуффер (Сслпровидер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslFreeBuffer
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: bced83b52ddf37266f64ae0c2b8919902f30fff4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081570"
---
# <a name="sslfreebuffer-function"></a><span data-ttu-id="a470b-103">Функция Сслфрибуффер</span><span class="sxs-lookup"><span data-stu-id="a470b-103">SslFreeBuffer function</span></span>

<span data-ttu-id="a470b-104">Функция **сслфрибуффер** используется для освобождения памяти, выделенной одной из функций поставщика [*SSL протокола*](/windows/desktop/SecGloss/s-gly) (SSL).</span><span class="sxs-lookup"><span data-stu-id="a470b-104">The **SslFreeBuffer** function is used to free memory that was allocated by one of the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) provider functions.</span></span>

## <a name="syntax"></a><span data-ttu-id="a470b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a470b-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslFreeBuffer(
  _In_ PVOID pvInput
);
```



## <a name="parameters"></a><span data-ttu-id="a470b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a470b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a470b-107">*пвинпут* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a470b-107">*pvInput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a470b-108">Указатель на буфер памяти, который необходимо освободить.</span><span class="sxs-lookup"><span data-stu-id="a470b-108">A pointer to the memory buffer to be freed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a470b-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a470b-109">Return value</span></span>

<span data-ttu-id="a470b-110">Если функция завершается с ошибкой, она возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="a470b-110">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="a470b-111">Если функция завершается ошибкой, она возвращает ненулевое значение ошибки.</span><span class="sxs-lookup"><span data-stu-id="a470b-111">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="a470b-112">Возможные коды возврата включают, но не ограничиваются следующим.</span><span class="sxs-lookup"><span data-stu-id="a470b-112">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="a470b-113">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="a470b-113">Return code/value</span></span>                                                                                                                                                       | <span data-ttu-id="a470b-114">Описание</span><span class="sxs-lookup"><span data-stu-id="a470b-114">Description</span></span>                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a470b-115">Не <dt>**превышать \_ Недопустимый \_ параметр**</dt> <dt>0x80090027L</dt></span><span class="sxs-lookup"><span data-stu-id="a470b-115"><dt>**NTE\_INVALID\_PARAMETER**</dt> <dt>0x80090027L</dt></span></span> </dl> | <span data-ttu-id="a470b-116">Параметр *пдвпровидеркаунт* или *Пппровидерлист* имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="a470b-116">The *pdwProviderCount* or *ppProviderList* parameter is **NULL**.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="a470b-117">Требования</span><span class="sxs-lookup"><span data-stu-id="a470b-117">Requirements</span></span>



| <span data-ttu-id="a470b-118">Требование</span><span class="sxs-lookup"><span data-stu-id="a470b-118">Requirement</span></span> | <span data-ttu-id="a470b-119">Значение</span><span class="sxs-lookup"><span data-stu-id="a470b-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a470b-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a470b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a470b-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a470b-121">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="a470b-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a470b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a470b-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a470b-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="a470b-124">Header</span><span class="sxs-lookup"><span data-stu-id="a470b-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="a470b-125"><dt>Сслпровидер. h</dt></span><span class="sxs-lookup"><span data-stu-id="a470b-125"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="a470b-126">DLL</span><span class="sxs-lookup"><span data-stu-id="a470b-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a470b-127"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a470b-127"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

