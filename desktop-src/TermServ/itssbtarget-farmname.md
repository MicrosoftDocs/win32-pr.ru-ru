---
title: Итссбтаржет Фармнаме, свойство
description: Возвращает или задает имя фермы, к которой присоединен этот целевой объект.
ms.assetid: 83e168ae-f985-40f9-912b-496c0695f82a
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Фармнаме
- Службы удаленных рабочих столов свойства Фармнаме, интерфейс Итссбтаржет
- Службы удаленных рабочих столов интерфейса Итссбтаржет, свойство Фармнаме
- Службы удаленных рабочих столов свойства Фармнаме, интерфейс Итссбтаржетекс
- Службы удаленных рабочих столов интерфейса Итссбтаржетекс, свойство Фармнаме
topic_type:
- apiref
api_name:
- ITsSbTarget.FarmName
- ITsSbTarget.get_FarmName
- ITsSbTarget.put_FarmName
- ITsSbTargetEx.FarmName
- ITsSbTargetEx.get_FarmName
- ITsSbTargetEx.put_FarmName
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b94f86b2cf0ec257be9fe9b801e6fceae364a46e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "103783855"
---
# <a name="itssbtargetfarmname-property"></a><span data-ttu-id="3318a-108">Свойство Итссбтаржет:: Фармнаме</span><span class="sxs-lookup"><span data-stu-id="3318a-108">ITsSbTarget::FarmName property</span></span>

<span data-ttu-id="3318a-109">Возвращает или задает имя фермы, к которой присоединен этот целевой объект.</span><span class="sxs-lookup"><span data-stu-id="3318a-109">Retrieves or specifies the name of the farm to which this target is joined.</span></span>

<span data-ttu-id="3318a-110">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="3318a-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="3318a-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3318a-111">Syntax</span></span>


```C++
HRESULT put_FarmName(
  [in]          BSTR Val
);

HRESULT get_FarmName(
  [out, retval] BSTR *pVal
);
```



## <a name="property-value"></a><span data-ttu-id="3318a-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="3318a-112">Property value</span></span>

<span data-ttu-id="3318a-113">Переменная **BSTR** , содержащая имя фермы.</span><span class="sxs-lookup"><span data-stu-id="3318a-113">A **BSTR** variable that contains the farm name.</span></span>

## <a name="requirements"></a><span data-ttu-id="3318a-114">Требования</span><span class="sxs-lookup"><span data-stu-id="3318a-114">Requirements</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3318a-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3318a-115">Minimum supported client</span></span><br/></td>
<td><span data-ttu-id="3318a-116">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="3318a-116">None supported</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3318a-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3318a-117">Minimum supported server</span></span><br/></td>
<td><span data-ttu-id="3318a-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3318a-118">Windows Server 2012</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3318a-119">IDL</span><span class="sxs-lookup"><span data-stu-id="3318a-119">IDL</span></span><br/></td>
<td><dl> <span data-ttu-id="3318a-120"><dt>Сбтсв. idl</dt> </span><span class="sxs-lookup"><span data-stu-id="3318a-120"><dt>Sbtsv.idl</dt> </span></span></dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3318a-121">IID</span><span class="sxs-lookup"><span data-stu-id="3318a-121">IID</span></span><br/></td>
<td><span data-ttu-id="3318a-122">IID_ITsSbTarget определяется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="3318a-122">IID_ITsSbTarget is defined as:</span></span>
<ul>
<li><span data-ttu-id="3318a-123">16616ECC-272D-411D-B324-126893033856</span><span class="sxs-lookup"><span data-stu-id="3318a-123">16616ECC-272D-411D-B324-126893033856</span></span></li>
<li><span data-ttu-id="3318a-124">e85e10ea-db0b-4752-b456-5fd5840901c0 на Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="3318a-124">e85e10ea-db0b-4752-b456-5fd5840901c0 on Windows Server 2008 R2</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



## <a name="see-also"></a><span data-ttu-id="3318a-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3318a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3318a-126">**итссбтаржетекс**</span><span class="sxs-lookup"><span data-stu-id="3318a-126">**ITsSbTargetEx**</span></span>](itssbtargetex.md)
</dt> <dt>

[<span data-ttu-id="3318a-127">**итссбтаржет**</span><span class="sxs-lookup"><span data-stu-id="3318a-127">**ITsSbTarget**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget)
</dt> </dl>

 

 





