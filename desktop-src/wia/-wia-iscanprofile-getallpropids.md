---
description: Возвращает все доступные идентификаторы свойств в профиле.
ms.assetid: 9ef2abdd-0b33-4be3-a124-7795f42d5e55
title: 'Метод Исканпрофиле:: Жеталлпропидс (Сканпрофиле. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.GetAllPropIDs
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: 34cd00f626bea3b8f1350950f0d2012ce019068e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692528"
---
# <a name="iscanprofilegetallpropids-method"></a><span data-ttu-id="48a23-103">Метод Исканпрофиле:: Жеталлпропидс</span><span class="sxs-lookup"><span data-stu-id="48a23-103">IScanProfile::GetAllPropIDs method</span></span>

<span data-ttu-id="48a23-104">Возвращает все доступные идентификаторы свойств в профиле.</span><span class="sxs-lookup"><span data-stu-id="48a23-104">Gets all available property IDs in a profile.</span></span>

## <a name="syntax"></a><span data-ttu-id="48a23-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="48a23-105">Syntax</span></span>


```C++
HRESULT GetAllPropIDs(
  [in, out] ULONG  *num,
  [out]     PROPID *ppid
);
```



## <a name="parameters"></a><span data-ttu-id="48a23-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="48a23-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48a23-107">*число* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="48a23-107">*num* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="48a23-108">Тип: \**ulong \** _</span><span class="sxs-lookup"><span data-stu-id="48a23-108">Type: \**ULONG\** _</span></span>

<span data-ttu-id="48a23-109">Количество запрошенных или возвращаемых идентификаторов свойств.</span><span class="sxs-lookup"><span data-stu-id="48a23-109">The number of property IDs requested or returned.</span></span>

</dd> <dt>

<span data-ttu-id="48a23-110">_ppid \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="48a23-110">_ppid\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="48a23-111">Тип: \**PropID \** _</span><span class="sxs-lookup"><span data-stu-id="48a23-111">Type: \**PROPID\** _</span></span>

<span data-ttu-id="48a23-112">Указатель на массив идентификаторов свойств.</span><span class="sxs-lookup"><span data-stu-id="48a23-112">A pointer to an array of property IDs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="48a23-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="48a23-113">Return value</span></span>

<span data-ttu-id="48a23-114">Тип: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="48a23-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="48a23-115">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="48a23-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="48a23-116">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="48a23-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="48a23-117">Требования</span><span class="sxs-lookup"><span data-stu-id="48a23-117">Requirements</span></span>



| <span data-ttu-id="48a23-118">Требование</span><span class="sxs-lookup"><span data-stu-id="48a23-118">Requirement</span></span> | <span data-ttu-id="48a23-119">Значение</span><span class="sxs-lookup"><span data-stu-id="48a23-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="48a23-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="48a23-120">Minimum supported client</span></span><br/> | <span data-ttu-id="48a23-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="48a23-121">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="48a23-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="48a23-122">Minimum supported server</span></span><br/> | <span data-ttu-id="48a23-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="48a23-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="48a23-124">Header</span><span class="sxs-lookup"><span data-stu-id="48a23-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="48a23-125"><dt>Сканпрофиле. h</dt></span><span class="sxs-lookup"><span data-stu-id="48a23-125"><dt>Scanprofile.h</dt></span></span> </dl>    |
| <span data-ttu-id="48a23-126">IDL</span><span class="sxs-lookup"><span data-stu-id="48a23-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="48a23-127"><dt>Сканпрофилес. idl</dt></span><span class="sxs-lookup"><span data-stu-id="48a23-127"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48a23-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="48a23-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48a23-129">**исканпрофиле**</span><span class="sxs-lookup"><span data-stu-id="48a23-129">**IScanProfile**</span></span>](-wia-iscanprofile.md)
</dt> <dt>

[<span data-ttu-id="48a23-130">Схема профиля сканирования</span><span class="sxs-lookup"><span data-stu-id="48a23-130">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




