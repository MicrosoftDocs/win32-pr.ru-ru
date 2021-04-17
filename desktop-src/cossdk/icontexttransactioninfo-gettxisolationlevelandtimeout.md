---
description: Возвращает уровень изоляции и значение времени ожидания транзакции, размещенной в корневом контексте транзакции.
ms.assetid: bb3ff03e-e69e-4a50-af36-4938eb4323df
title: 'Метод Иконтексттрансактионинфо:: Жеттксисолатионлевеландтимеаут'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextTransactionInfo.GetTxIsolationLevelAndTimeout
api_type:
- COM
api_location: ''
ms.openlocfilehash: b8545a697e672af7206a69ffa19618d5b70e055c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692040"
---
# <a name="icontexttransactioninfogettxisolationlevelandtimeout-method"></a><span data-ttu-id="bf36c-103">Метод Иконтексттрансактионинфо:: Жеттксисолатионлевеландтимеаут</span><span class="sxs-lookup"><span data-stu-id="bf36c-103">IContextTransactionInfo::GetTxIsolationLevelAndTimeout method</span></span>

<span data-ttu-id="bf36c-104">Возвращает уровень изоляции и значение времени ожидания транзакции, размещенной в корневом контексте транзакции.</span><span class="sxs-lookup"><span data-stu-id="bf36c-104">Retrieves the isolation level and timeout value of a transaction that is hosted in the root transaction context.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf36c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bf36c-105">Syntax</span></span>


```C++
HRESULT GetTxIsolationLevelAndTimeout(
  [out] ISOLEVEL *pIsoLevel,
  [out] DWORD    *dwTime
);
```



## <a name="parameters"></a><span data-ttu-id="bf36c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="bf36c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf36c-107">*писолевел* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="bf36c-107">*pIsoLevel* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bf36c-108">Значение [ISOLATIONLEVEL](/previous-versions/windows/desktop/ms679234(v=vs.85)) для транзакции.</span><span class="sxs-lookup"><span data-stu-id="bf36c-108">The [ISOLATIONLEVEL](/previous-versions/windows/desktop/ms679234(v=vs.85)) value for the transaction.</span></span>

</dd> <dt>

<span data-ttu-id="bf36c-109">*двтиме* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="bf36c-109">*dwTime* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bf36c-110">Время ожидания транзакции в секундах.</span><span class="sxs-lookup"><span data-stu-id="bf36c-110">The timeout of the transaction, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf36c-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bf36c-111">Return value</span></span>

<span data-ttu-id="bf36c-112">Этот метод может возвращать стандартные возвращаемые значения E \_ INVALIDARG, e \_ OUTOFMEMORY, e \_ непредвиденные и S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="bf36c-112">This method can return the standard return values E\_INVALIDARG, E\_OUTOFMEMORY, E\_UNEXPECTED, and S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf36c-113">Требования</span><span class="sxs-lookup"><span data-stu-id="bf36c-113">Requirements</span></span>



| <span data-ttu-id="bf36c-114">Требование</span><span class="sxs-lookup"><span data-stu-id="bf36c-114">Requirement</span></span> | <span data-ttu-id="bf36c-115">Значение</span><span class="sxs-lookup"><span data-stu-id="bf36c-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="bf36c-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bf36c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="bf36c-117">Только для настольных приложений Windows XP с пакетом обновления 2 \[\]</span><span class="sxs-lookup"><span data-stu-id="bf36c-117">Windows XP with SP2 \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="bf36c-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bf36c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="bf36c-119">Только для настольных приложений Windows Server 2003 с пакетом обновления 1 \[\]</span><span class="sxs-lookup"><span data-stu-id="bf36c-119">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bf36c-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bf36c-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf36c-121">**иконтексттрансактионинфо**</span><span class="sxs-lookup"><span data-stu-id="bf36c-121">**IContextTransactionInfo**</span></span>](icontexttransactioninfo.md)
</dt> </dl>

 

