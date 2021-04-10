---
description: Возвращает учетную запись-посредник транзакции или транзакции, связанную с текущим контекстом, если таковая имеется.
ms.assetid: 2f85f395-3ec5-4c5a-a6db-c902cb8f8486
title: 'Метод Иконтексттрансактионинфо:: Фетчтрансактион'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextTransactionInfo.FetchTransaction
api_type:
- COM
api_location: ''
ms.openlocfilehash: 0e753974f93539f051465f13a1ea92d7e0e3bfa1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141824"
---
# <a name="icontexttransactioninfofetchtransaction-method"></a><span data-ttu-id="2f56e-103">Метод Иконтексттрансактионинфо:: Фетчтрансактион</span><span class="sxs-lookup"><span data-stu-id="2f56e-103">IContextTransactionInfo::FetchTransaction method</span></span>

<span data-ttu-id="2f56e-104">Возвращает учетную запись-посредник транзакции или транзакции, связанную с текущим контекстом, если таковая имеется.</span><span class="sxs-lookup"><span data-stu-id="2f56e-104">Retrieves the transaction or transaction proxy that is associated with the current context, if any.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f56e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2f56e-105">Syntax</span></span>


```C++
HRESULT FetchTransaction(
  [out, retval] IUnknown **pUnk
);
```



## <a name="parameters"></a><span data-ttu-id="2f56e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2f56e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f56e-107">*Punk* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="2f56e-107">*pUnk* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="2f56e-108">Транзакция или прокси транзакции, связанные с текущим контекстом; в противном случае **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="2f56e-108">The transaction or transaction proxy that is associated with the current context; otherwise, **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f56e-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2f56e-109">Return value</span></span>

<span data-ttu-id="2f56e-110">Этот метод может возвращать стандартные возвращаемые значения E \_ INVALIDARG, e \_ OUTOFMEMORY, e \_ непредвиденные и S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="2f56e-110">This method can return the standard return values E\_INVALIDARG, E\_OUTOFMEMORY, E\_UNEXPECTED, and S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f56e-111">Требования</span><span class="sxs-lookup"><span data-stu-id="2f56e-111">Requirements</span></span>



| <span data-ttu-id="2f56e-112">Требование</span><span class="sxs-lookup"><span data-stu-id="2f56e-112">Requirement</span></span> | <span data-ttu-id="2f56e-113">Значение</span><span class="sxs-lookup"><span data-stu-id="2f56e-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="2f56e-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2f56e-114">Minimum supported client</span></span><br/> | <span data-ttu-id="2f56e-115">Только для настольных приложений Windows XP с пакетом обновления 2 \[\]</span><span class="sxs-lookup"><span data-stu-id="2f56e-115">Windows XP with SP2 \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="2f56e-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2f56e-116">Minimum supported server</span></span><br/> | <span data-ttu-id="2f56e-117">Только для настольных приложений Windows Server 2003 с пакетом обновления 1 \[\]</span><span class="sxs-lookup"><span data-stu-id="2f56e-117">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2f56e-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2f56e-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f56e-119">**иконтексттрансактионинфо**</span><span class="sxs-lookup"><span data-stu-id="2f56e-119">**IContextTransactionInfo**</span></span>](icontexttransactioninfo.md)
</dt> </dl>

 

 




