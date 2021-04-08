---
description: Возвращает количество элементов, хранящихся в этом перечислителе.
ms.assetid: d374ec81-0bd5-4b5d-8002-e3b53476421a
title: 'Метод IEnumWiaItem2:: NOCOUNT (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumWiaItem2.GetCount
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 23c067b8e4da93d678f641890a85e2535b3ca50d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080367"
---
# <a name="ienumwiaitem2getcount-method"></a><span data-ttu-id="78903-103">Метод IEnumWiaItem2:: NOCOUNT</span><span class="sxs-lookup"><span data-stu-id="78903-103">IEnumWiaItem2::GetCount method</span></span>

<span data-ttu-id="78903-104">Возвращает количество элементов, хранящихся в этом перечислителе.</span><span class="sxs-lookup"><span data-stu-id="78903-104">Returns the number of elements stored by this enumerator.</span></span>

## <a name="syntax"></a><span data-ttu-id="78903-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="78903-105">Syntax</span></span>


```C++
HRESULT GetCount(
  [out] ULONG *cElt
);
```



## <a name="parameters"></a><span data-ttu-id="78903-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="78903-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78903-107">*cElt* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="78903-107">*cElt* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="78903-108">Тип: \**ulong \** _</span><span class="sxs-lookup"><span data-stu-id="78903-108">Type: \**ULONG\** _</span></span>

<span data-ttu-id="78903-109">Получает указатель на _ \*ulong\*\*, который получает количество элементов в перечислении.</span><span class="sxs-lookup"><span data-stu-id="78903-109">Receives a pointer to a _ *ULONG*\* that receives the number of elements in the enumeration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78903-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="78903-110">Return value</span></span>

<span data-ttu-id="78903-111">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="78903-111">Type: **HRESULT**</span></span>

<span data-ttu-id="78903-112">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="78903-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="78903-113">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="78903-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="78903-114">Требования</span><span class="sxs-lookup"><span data-stu-id="78903-114">Requirements</span></span>



| <span data-ttu-id="78903-115">Требование</span><span class="sxs-lookup"><span data-stu-id="78903-115">Requirement</span></span> | <span data-ttu-id="78903-116">Значение</span><span class="sxs-lookup"><span data-stu-id="78903-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="78903-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="78903-117">Minimum supported client</span></span><br/> | <span data-ttu-id="78903-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="78903-118">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="78903-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="78903-119">Minimum supported server</span></span><br/> | <span data-ttu-id="78903-120">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="78903-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="78903-121">Header</span><span class="sxs-lookup"><span data-stu-id="78903-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="78903-122"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="78903-122"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="78903-123">IDL</span><span class="sxs-lookup"><span data-stu-id="78903-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="78903-124"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="78903-124"><dt>Wia.idl</dt></span></span> </dl> |



 

 




