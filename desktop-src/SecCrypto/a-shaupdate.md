---
description: Добавляет данные в указанный хэш-объект.
ms.assetid: 8E32BBC4-C2DD-4174-9FF1-9001E4A7D87B
title: Функция A_SHAUpdate (SHA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- A_SHAUpdate
api_type:
- DllExport
api_location:
- ntdll.dll
ms.openlocfilehash: a0f8ac49d8221538a168ade536e55766e209d3d4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685105"
---
# <a name="a_shaupdate-function"></a><span data-ttu-id="f46d8-103">\_Функция шаупдате</span><span class="sxs-lookup"><span data-stu-id="f46d8-103">A\_SHAUpdate function</span></span>

<span data-ttu-id="f46d8-104">Добавляет данные в указанный хэш-объект.</span><span class="sxs-lookup"><span data-stu-id="f46d8-104">Adds data to a specified hash object.</span></span>

## <a name="syntax"></a><span data-ttu-id="f46d8-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f46d8-105">Syntax</span></span>


```C++
void RSA32API A_SHAUpdate(
  _Inout_ A_SHA_CTX     *Context,
  _Out_   UNSIGNED CHAR *Buffer,
          UNSIGNED INT  BufferSize
);
```



## <a name="parameters"></a><span data-ttu-id="f46d8-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f46d8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f46d8-107">*Контекст* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="f46d8-107">*Context* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f46d8-108">Контекст SHA.</span><span class="sxs-lookup"><span data-stu-id="f46d8-108">The SHA context.</span></span>

</dd> <dt>

<span data-ttu-id="f46d8-109">*Буфер* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="f46d8-109">*Buffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f46d8-110">Хэш-таблица.</span><span class="sxs-lookup"><span data-stu-id="f46d8-110">The hash table.</span></span>

</dd> <dt>

<span data-ttu-id="f46d8-111">*BufferSize*</span><span class="sxs-lookup"><span data-stu-id="f46d8-111">*BufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="f46d8-112">Размер буфера.</span><span class="sxs-lookup"><span data-stu-id="f46d8-112">The size of the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f46d8-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f46d8-113">Return value</span></span>

<span data-ttu-id="f46d8-114">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="f46d8-114">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f46d8-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f46d8-115">Remarks</span></span>

<span data-ttu-id="f46d8-116">Эту функцию можно вызывать несколько раз, чтобы вычислить хэш для длинных потоков данных или ненепрерывных потоков данных.</span><span class="sxs-lookup"><span data-stu-id="f46d8-116">This function can be called multiple times to compute the hash on long data streams or discontinuous data streams.</span></span> <span data-ttu-id="f46d8-117">Перед получением хэш-значения необходимо вызвать функцию [**\_ шафинал**](a-shafinal.md) .</span><span class="sxs-lookup"><span data-stu-id="f46d8-117">The [**A\_SHAFinal**](a-shafinal.md) function must be called before retrieving the hash value.</span></span>

<span data-ttu-id="f46d8-118">Эта функция очень похожа на Шаупдате, но вызывается непосредственно из библиотеки, а не направляется через криптографическую инфраструктуру.</span><span class="sxs-lookup"><span data-stu-id="f46d8-118">This function is very similar to SHAUpdate, but is called directly from the library, rather than being routed through the cryptography infrastructure.</span></span> <span data-ttu-id="f46d8-119">Дополнительные сведения см. в разделе [поставщики Нткриптографик Windows](/previous-versions/tn-archive/cc723484(v=technet.10)).</span><span class="sxs-lookup"><span data-stu-id="f46d8-119">For more information, see [Windows NTCryptographic Providers](/previous-versions/tn-archive/cc723484(v=technet.10)).</span></span>

## <a name="requirements"></a><span data-ttu-id="f46d8-120">Требования</span><span class="sxs-lookup"><span data-stu-id="f46d8-120">Requirements</span></span>



| <span data-ttu-id="f46d8-121">Требование</span><span class="sxs-lookup"><span data-stu-id="f46d8-121">Requirement</span></span> | <span data-ttu-id="f46d8-122">Значение</span><span class="sxs-lookup"><span data-stu-id="f46d8-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f46d8-123">Header</span><span class="sxs-lookup"><span data-stu-id="f46d8-123">Header</span></span><br/>  | <dl> <span data-ttu-id="f46d8-124"><dt>SHA. h</dt></span><span class="sxs-lookup"><span data-stu-id="f46d8-124"><dt>Sha.h</dt></span></span> </dl>     |
| <span data-ttu-id="f46d8-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f46d8-125">Library</span></span><br/> | <dl> <span data-ttu-id="f46d8-126"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f46d8-126"><dt>Ntdll.dll</dt></span></span> </dl> |
| <span data-ttu-id="f46d8-127">DLL</span><span class="sxs-lookup"><span data-stu-id="f46d8-127">DLL</span></span><br/>     | <dl> <span data-ttu-id="f46d8-128"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f46d8-128"><dt>Ntdll.dll</dt></span></span> </dl> |



 

 
