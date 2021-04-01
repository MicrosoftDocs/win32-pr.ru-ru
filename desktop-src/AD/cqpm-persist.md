---
title: Сообщение CQPM_PERSIST (Кмнкуери. h)
description: Отправляется в функцию обратного вызова Ккпажепрок страницы расширения формы запроса, чтобы разрешить странице считывать или записывать данные запросов из энергонезависимой памяти.
ms.assetid: f01586dd-4ed3-45af-9e25-a596a693313d
ms.tgt_platform: multiple
keywords:
- Сообщение CQPM_PERSIST Active Directory
topic_type:
- apiref
api_name:
- CQPM_PERSIST
api_location:
- Cmnquery.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70aaaae3b4fcc6788a16d59477d5f8158b43b892
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071567"
---
# <a name="cqpm_persist-message"></a><span data-ttu-id="0c4d6-104">ККПМ \_ сообщение о сохранении</span><span class="sxs-lookup"><span data-stu-id="0c4d6-104">CQPM\_PERSIST message</span></span>

<span data-ttu-id="0c4d6-105">Сообщение **о \_ сохранении ККПМ** отправляется в функцию обратного вызова [**ккпажепрок**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) на странице расширения формы запроса, чтобы разрешить странице считывать или записывать данные запросов из энергонезависимой памяти.</span><span class="sxs-lookup"><span data-stu-id="0c4d6-105">The **CQPM\_PERSIST** message is sent to the [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) callback function of a query form extension page to allow the page to read or write query data from persistent memory.</span></span>

## <a name="parameters"></a><span data-ttu-id="0c4d6-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0c4d6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c4d6-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0c4d6-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0c4d6-108">Содержит ненулевое значение для чтения данных запроса или нуля для записи данных запроса.</span><span class="sxs-lookup"><span data-stu-id="0c4d6-108">Contains nonzero to read the query data or zero to write the query data.</span></span>

</dd> <dt>

<span data-ttu-id="0c4d6-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0c4d6-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0c4d6-110">Указатель на интерфейс [**иперсисткуери**](/windows/win32/api/cmnquery/nn-cmnquery-ipersistquery) , в который должны считываться или записываться данные запроса.</span><span class="sxs-lookup"><span data-stu-id="0c4d6-110">Pointer to an [**IPersistQuery**](/windows/win32/api/cmnquery/nn-cmnquery-ipersistquery) interface that the query data should be read from or written to.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0c4d6-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0c4d6-111">Return value</span></span>

<span data-ttu-id="0c4d6-112">Возвращает **значение \_ ОК** , если успешно, или стандартный код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0c4d6-112">Returns **S\_OK** if successful or a standard **HRESULT** error code otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c4d6-113">Требования</span><span class="sxs-lookup"><span data-stu-id="0c4d6-113">Requirements</span></span>



| <span data-ttu-id="0c4d6-114">Требование</span><span class="sxs-lookup"><span data-stu-id="0c4d6-114">Requirement</span></span> | <span data-ttu-id="0c4d6-115">Значение</span><span class="sxs-lookup"><span data-stu-id="0c4d6-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0c4d6-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0c4d6-116">Minimum supported client</span></span><br/> | <span data-ttu-id="0c4d6-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0c4d6-117">Windows Vista</span></span><br/>                                                              |
| <span data-ttu-id="0c4d6-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0c4d6-118">Minimum supported server</span></span><br/> | <span data-ttu-id="0c4d6-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0c4d6-119">Windows Server 2008</span></span><br/>                                                        |
| <span data-ttu-id="0c4d6-120">Header</span><span class="sxs-lookup"><span data-stu-id="0c4d6-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="0c4d6-121"><dt>Кмнкуери. h</dt></span><span class="sxs-lookup"><span data-stu-id="0c4d6-121"><dt>Cmnquery.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c4d6-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0c4d6-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c4d6-123">**ккпажепрок**</span><span class="sxs-lookup"><span data-stu-id="0c4d6-123">**CQPageProc**</span></span>](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc)
</dt> <dt>

[<span data-ttu-id="0c4d6-124">**иперсисткуери**</span><span class="sxs-lookup"><span data-stu-id="0c4d6-124">**IPersistQuery**</span></span>](/windows/win32/api/cmnquery/nn-cmnquery-ipersistquery)
</dt> </dl>

 

