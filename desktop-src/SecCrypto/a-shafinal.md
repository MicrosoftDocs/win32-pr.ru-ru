---
description: Выполняет вычисление конечного хэша данных, вводимых функцией MD5Update.
ms.assetid: A0457D26-F4E3-4ED4-B374-0AFCB6F661FB
title: Функция A_SHAFinal (SHA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- A_SHAFinal
api_type:
- DllExport
api_location:
- ntdll.dll
ms.openlocfilehash: 2a206005a686d02891a593243bc0ef3a4ad7db23
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665136"
---
# <a name="a_shafinal-function"></a><span data-ttu-id="d5e6c-103">\_Функция шафинал</span><span class="sxs-lookup"><span data-stu-id="d5e6c-103">A\_SHAFinal function</span></span>

<span data-ttu-id="d5e6c-104">Выполняет вычисление конечного хэша данных, вводимых функцией MD5Update.</span><span class="sxs-lookup"><span data-stu-id="d5e6c-104">Computes the final hash of the data entered by the MD5Update function.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5e6c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d5e6c-105">Syntax</span></span>


```C++
VOID RSA32API A_SHAFinal(
  _Inout_ A_SHA_CTX     *Context,
  _Out_   UNSIGNED CHAR Result
);
```



## <a name="parameters"></a><span data-ttu-id="d5e6c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d5e6c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5e6c-107">*Контекст* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="d5e6c-107">*Context* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d5e6c-108">Контекст SHA.</span><span class="sxs-lookup"><span data-stu-id="d5e6c-108">The SHA context.</span></span>

</dd> <dt>

<span data-ttu-id="d5e6c-109">*Результат* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="d5e6c-109">*Result* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d5e6c-110">Результирующая хэш-таблица.</span><span class="sxs-lookup"><span data-stu-id="d5e6c-110">The resulting hash table.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5e6c-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d5e6c-111">Return value</span></span>

<span data-ttu-id="d5e6c-112">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="d5e6c-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d5e6c-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d5e6c-113">Remarks</span></span>

<span data-ttu-id="d5e6c-114">Эта функция очень похожа на Шафинал, но вызывается непосредственно из библиотеки, а не направляется через криптографическую инфраструктуру.</span><span class="sxs-lookup"><span data-stu-id="d5e6c-114">This function is very similar to SHAFinal, but is called directly from the library, rather than being routed through the cryptography infrastructure.</span></span> <span data-ttu-id="d5e6c-115">Дополнительные сведения см. в разделе [поставщики Нткриптографик Windows](/previous-versions/tn-archive/cc723484(v=technet.10)).</span><span class="sxs-lookup"><span data-stu-id="d5e6c-115">For more information, see [Windows NTCryptographic Providers](/previous-versions/tn-archive/cc723484(v=technet.10)).</span></span>

## <a name="requirements"></a><span data-ttu-id="d5e6c-116">Требования</span><span class="sxs-lookup"><span data-stu-id="d5e6c-116">Requirements</span></span>



| <span data-ttu-id="d5e6c-117">Требование</span><span class="sxs-lookup"><span data-stu-id="d5e6c-117">Requirement</span></span> | <span data-ttu-id="d5e6c-118">Значение</span><span class="sxs-lookup"><span data-stu-id="d5e6c-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d5e6c-119">Header</span><span class="sxs-lookup"><span data-stu-id="d5e6c-119">Header</span></span><br/>  | <dl> <span data-ttu-id="d5e6c-120"><dt>SHA. h</dt></span><span class="sxs-lookup"><span data-stu-id="d5e6c-120"><dt>Sha.h</dt></span></span> </dl>     |
| <span data-ttu-id="d5e6c-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d5e6c-121">Library</span></span><br/> | <dl> <span data-ttu-id="d5e6c-122"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d5e6c-122"><dt>Ntdll.dll</dt></span></span> </dl> |
| <span data-ttu-id="d5e6c-123">DLL</span><span class="sxs-lookup"><span data-stu-id="d5e6c-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="d5e6c-124"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d5e6c-124"><dt>Ntdll.dll</dt></span></span> </dl> |



 

 
