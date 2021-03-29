---
title: Итссбтаржет Таржетлоад, свойство
description: Извлекает относительную нагрузку на целевой объект.
ms.assetid: 56618dcf-1319-4310-80ba-7ed71b8b02e8
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Таржетлоад
- Службы удаленных рабочих столов свойства Таржетлоад, интерфейс Итссбтаржет
- Службы удаленных рабочих столов интерфейса Итссбтаржет, свойство Таржетлоад
- Службы удаленных рабочих столов свойства Таржетлоад, интерфейс Итссбтаржетекс
- Службы удаленных рабочих столов интерфейса Итссбтаржетекс, свойство Таржетлоад
topic_type:
- apiref
api_name:
- ITsSbTarget.TargetLoad
- ITsSbTarget.get_TargetLoad
- ITsSbTargetEx.TargetLoad
- ITsSbTargetEx.get_TargetLoad
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ddfc9be9805406ab76b166e2a34bc47a7f5e9ab5
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "103784119"
---
# <a name="itssbtargettargetload-property"></a><span data-ttu-id="e70c3-108">Свойство Итссбтаржет:: Таржетлоад</span><span class="sxs-lookup"><span data-stu-id="e70c3-108">ITsSbTarget::TargetLoad property</span></span>

<span data-ttu-id="e70c3-109">Извлекает относительную нагрузку на целевой объект.</span><span class="sxs-lookup"><span data-stu-id="e70c3-109">Retrieves the relative load on a target.</span></span> <span data-ttu-id="e70c3-110">Это значение основано на количестве существующих и ожидающих сеансов.</span><span class="sxs-lookup"><span data-stu-id="e70c3-110">This value is based on the number of existing and pending sessions.</span></span> <span data-ttu-id="e70c3-111">По умолчанию ожидающий сеанс имеет то же значение, что и существующий сеанс.</span><span class="sxs-lookup"><span data-stu-id="e70c3-111">By default a pending session has the same value as an existing session.</span></span>

<span data-ttu-id="e70c3-112">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="e70c3-112">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e70c3-113">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e70c3-113">Syntax</span></span>


```C++
HRESULT get_TargetLoad(
  [out, retval] DWORD *pTargetLoad
);
```



## <a name="property-value"></a><span data-ttu-id="e70c3-114">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="e70c3-114">Property value</span></span>

<span data-ttu-id="e70c3-115">Число, представляющее относительную нагрузку на целевой объект.</span><span class="sxs-lookup"><span data-stu-id="e70c3-115">A number representing the relative load on a target.</span></span>

## <a name="remarks"></a><span data-ttu-id="e70c3-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e70c3-116">Remarks</span></span>

<span data-ttu-id="e70c3-117">Вес ожидающего сеанса относительно активного сеанса можно изменить, задав значение параметра *\_ коннектионестаблишментпеналти балансировки нагрузки* для брокера подключений.</span><span class="sxs-lookup"><span data-stu-id="e70c3-117">The weight of a pending session relative to an active session can be changed by setting the value of the *LB\_ConnectionEstablishmentPenalty* parameter for the Connection Broker.</span></span> <span data-ttu-id="e70c3-118">Этот параметр находится в разделе реестра **HKLM \\ System \\ CurrentControlSet \\ Services \\ Tssdis \\ Parameters** .</span><span class="sxs-lookup"><span data-stu-id="e70c3-118">This parameter is located under the **HKLM\\System\\CurrentControlSet\\Services\\Tssdis\\Parameters** registry key.</span></span> <span data-ttu-id="e70c3-119">Значение по умолчанию 1 указывает, что ожидающие сеансы имеют тот же вес, что и активные сеансы.</span><span class="sxs-lookup"><span data-stu-id="e70c3-119">The default value of 1 specifies that pending sessions have the same weight as active sessions.</span></span>

<span data-ttu-id="e70c3-120">Это свойство доступно в Windows Server 2012 R2 с [KB3091411](https://support.microsoft.com/kb/3091411) , установленным в интерфейсе [**итссбтаржетекс**](itssbtargetex.md) .</span><span class="sxs-lookup"><span data-stu-id="e70c3-120">This property is available on Windows Server 2012 R2 with [KB3091411](https://support.microsoft.com/kb/3091411) installed in the [**ITsSbTargetEx**](itssbtargetex.md) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="e70c3-121">Требования</span><span class="sxs-lookup"><span data-stu-id="e70c3-121">Requirements</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e70c3-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e70c3-122">Minimum supported client</span></span><br/></td>
<td><span data-ttu-id="e70c3-123">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="e70c3-123">None supported</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e70c3-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e70c3-124">Minimum supported server</span></span><br/></td>
<td><span data-ttu-id="e70c3-125">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="e70c3-125">Windows Server 2016</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e70c3-126">IDL</span><span class="sxs-lookup"><span data-stu-id="e70c3-126">IDL</span></span><br/></td>
<td><dl> <span data-ttu-id="e70c3-127"><dt>Сбтсв. idl</dt> </span><span class="sxs-lookup"><span data-stu-id="e70c3-127"><dt>Sbtsv.idl</dt> </span></span></dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e70c3-128">IID</span><span class="sxs-lookup"><span data-stu-id="e70c3-128">IID</span></span><br/></td>
<td><span data-ttu-id="e70c3-129">IID_ITsSbTarget определяется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="e70c3-129">IID_ITsSbTarget is defined as:</span></span>
<ul>
<li><span data-ttu-id="e70c3-130">16616ECC-272D-411D-B324-126893033856</span><span class="sxs-lookup"><span data-stu-id="e70c3-130">16616ECC-272D-411D-B324-126893033856</span></span></li>
<li><span data-ttu-id="e70c3-131">e85e10ea-db0b-4752-b456-5fd5840901c0 на Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e70c3-131">e85e10ea-db0b-4752-b456-5fd5840901c0 on Windows Server 2008 R2</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



## <a name="see-also"></a><span data-ttu-id="e70c3-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e70c3-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e70c3-133">**итссбтаржетекс**</span><span class="sxs-lookup"><span data-stu-id="e70c3-133">**ITsSbTargetEx**</span></span>](itssbtargetex.md)
</dt> <dt>

[<span data-ttu-id="e70c3-134">**итссбтаржет**</span><span class="sxs-lookup"><span data-stu-id="e70c3-134">**ITsSbTarget**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget)
</dt> </dl>

 

 





