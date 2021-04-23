---
description: Извлекает ПРОПВАРИАНТ и входную строку, представляющую фрагмент данных. Вызов этого метода аналогичен вызову GetData.
ms.assetid: 78846D1D-923F-4FEA-8BF2-B16BB1B21BB3
title: 'Метод Ириччунк:: Ремотежетдата'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRichChunk.RemoteGetData
api_type:
- COM
api_location: ''
ms.openlocfilehash: 002c85b189a3994b70795c05228ae5331c610284
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104144035"
---
# <a name="irichchunkremotegetdata-method"></a><span data-ttu-id="905e8-104">Метод Ириччунк:: Ремотежетдата</span><span class="sxs-lookup"><span data-stu-id="905e8-104">IRichChunk::RemoteGetData method</span></span>

<span data-ttu-id="905e8-105">Извлекает [пропвариант](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) и входную строку, представляющую фрагмент данных.</span><span class="sxs-lookup"><span data-stu-id="905e8-105">Retrieves the [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) and input string that represents a chunk of data.</span></span> <span data-ttu-id="905e8-106">Вызов этого метода аналогичен вызову [**GetData**](/windows/desktop/api/StructuredQueryCondition/nf-structuredquerycondition-irichchunk-getdata).</span><span class="sxs-lookup"><span data-stu-id="905e8-106">Calling this method is the same as calling [**GetData**](/windows/desktop/api/StructuredQueryCondition/nf-structuredquerycondition-irichchunk-getdata).</span></span>

## <a name="syntax"></a><span data-ttu-id="905e8-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="905e8-107">Syntax</span></span>


```C++
HRESULT RemoteGetData(
  [out] ULONG       *pFirstPos,
  [out] ULONG       *pLength,
  [out] LPWSTR      *ppsz,
  [out] PROPVARIANT *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="905e8-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="905e8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="905e8-109">*пфирстпос* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="905e8-109">*pFirstPos* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="905e8-110">Получает начальную точку диапазона (с отсчетом от нуля).</span><span class="sxs-lookup"><span data-stu-id="905e8-110">Receives the zero-based starting position of the range.</span></span> <span data-ttu-id="905e8-111">Этот параметр может принимать значение **NULL**.</span><span class="sxs-lookup"><span data-stu-id="905e8-111">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="905e8-112">*пленгс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="905e8-112">*pLength* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="905e8-113">Получает длину диапазона.</span><span class="sxs-lookup"><span data-stu-id="905e8-113">Receives the length of the range.</span></span> <span data-ttu-id="905e8-114">Этот параметр может принимать значение **NULL**.</span><span class="sxs-lookup"><span data-stu-id="905e8-114">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="905e8-115">*ппсз* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="905e8-115">*ppsz* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="905e8-116">Получает связанное строковое значение Юникода или **значение NULL** , если оно недоступно.</span><span class="sxs-lookup"><span data-stu-id="905e8-116">Receives the associated Unicode string value, or **NULL** if not available.</span></span>

</dd> <dt>

<span data-ttu-id="905e8-117">*pValue* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="905e8-117">*pValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="905e8-118">Получает связанное значение [пропвариант](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) или **VT \_ Empty** , если оно недоступно.</span><span class="sxs-lookup"><span data-stu-id="905e8-118">Receives the associated [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) value, or **VT\_EMPTY** if not available.</span></span> <span data-ttu-id="905e8-119">Этот параметр может принимать значение **NULL**.</span><span class="sxs-lookup"><span data-stu-id="905e8-119">This parameter can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="905e8-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="905e8-120">Return value</span></span>

<span data-ttu-id="905e8-121">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="905e8-121">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="905e8-122">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="905e8-122">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="see-also"></a><span data-ttu-id="905e8-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="905e8-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="905e8-124">**ириччунк**</span><span class="sxs-lookup"><span data-stu-id="905e8-124">**IRichChunk**</span></span>](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-irichchunk)
</dt> </dl>

 

 
