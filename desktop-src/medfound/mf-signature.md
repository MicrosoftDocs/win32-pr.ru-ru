---
description: Содержит сигнатуру глобального списка отзыва (GRL).
ms.assetid: 388a901c-6202-41cf-9c3d-f29d8ccca76b
title: Структура MF_SIGNATURE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MF_SIGNATURE
api_type:
- NA
api_location: ''
ms.openlocfilehash: 4827fea8e4259609cbb54f2b58a3d1c88ad6c23e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272381"
---
# <a name="mf_signature-structure"></a><span data-ttu-id="45282-103">\_Структура сигнатуры MF</span><span class="sxs-lookup"><span data-stu-id="45282-103">MF\_SIGNATURE structure</span></span>

<span data-ttu-id="45282-104">Содержит сигнатуру глобального списка отзыва (GRL).</span><span class="sxs-lookup"><span data-stu-id="45282-104">Contains a global revocation list (GRL) signature.</span></span>

## <a name="syntax"></a><span data-ttu-id="45282-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="45282-105">Syntax</span></span>


```C++
typedef struct _MF_SIGNATURE {
  DWORD dwSignVer;
  DWORD cbSign;
  BYTE  rgSign[1];
} MF_SIGNATURE;
```



## <a name="members"></a><span data-ttu-id="45282-106">Члены</span><span class="sxs-lookup"><span data-stu-id="45282-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="45282-107">**двсигнвер**</span><span class="sxs-lookup"><span data-stu-id="45282-107">**dwSignVer**</span></span>
</dt> <dd>

<span data-ttu-id="45282-108">Номер версии сигнатуры.</span><span class="sxs-lookup"><span data-stu-id="45282-108">The signature version number.</span></span>

</dd> <dt>

<span data-ttu-id="45282-109">**кбсигн**</span><span class="sxs-lookup"><span data-stu-id="45282-109">**cbSign**</span></span>
</dt> <dd>

<span data-ttu-id="45282-110">Размер подписи в байтах.</span><span class="sxs-lookup"><span data-stu-id="45282-110">The size of the signature in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="45282-111">**ргсигн**</span><span class="sxs-lookup"><span data-stu-id="45282-111">**rgSign**</span></span>
</dt> <dd>

<span data-ttu-id="45282-112">Массив байтов размера **кбсигн** , который содержит сигнатуру.</span><span class="sxs-lookup"><span data-stu-id="45282-112">A byte array of size **cbSign** that contains the signature.</span></span> <span data-ttu-id="45282-113">Фактический размер массива превышает размер, заданный в объявлении структуры.</span><span class="sxs-lookup"><span data-stu-id="45282-113">The actual array size is larger than the size given in the structure declaration.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="45282-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="45282-114">Remarks</span></span>

<span data-ttu-id="45282-115">Эта структура не объявлена в заголовке пакета SDK.</span><span class="sxs-lookup"><span data-stu-id="45282-115">This structure is not declared in an SDK header.</span></span> <span data-ttu-id="45282-116">Чтобы использовать эту структуру, добавьте приведенное здесь объявление в исходный код.</span><span class="sxs-lookup"><span data-stu-id="45282-116">To use this structure, add the declaration shown here to your source code.</span></span>

## <a name="requirements"></a><span data-ttu-id="45282-117">Требования</span><span class="sxs-lookup"><span data-stu-id="45282-117">Requirements</span></span>



| <span data-ttu-id="45282-118">Требование</span><span class="sxs-lookup"><span data-stu-id="45282-118">Requirement</span></span> | <span data-ttu-id="45282-119">Значение</span><span class="sxs-lookup"><span data-stu-id="45282-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="45282-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="45282-120">Minimum supported client</span></span><br/> | <span data-ttu-id="45282-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="45282-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="45282-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="45282-122">Minimum supported server</span></span><br/> | <span data-ttu-id="45282-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="45282-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="45282-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="45282-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45282-125">Отзыв сертификата ОПМ</span><span class="sxs-lookup"><span data-stu-id="45282-125">OPM Certificate Revocation</span></span>](opm-certificate-revocation.md)
</dt> <dt>

[<span data-ttu-id="45282-126">Структуры ОПМ</span><span class="sxs-lookup"><span data-stu-id="45282-126">OPM Structures</span></span>](opm-structures.md)
</dt> </dl>

 

 




