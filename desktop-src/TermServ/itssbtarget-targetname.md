---
title: Итссбтаржет, свойство TargetName
description: Указывает или получает имя целевого объекта.
ms.assetid: ba5c3158-b4bc-457f-94ea-adb2e0852129
ms.tgt_platform: multiple
keywords:
- Свойство TargetName службы удаленных рабочих столов
- Свойство TargetName службы удаленных рабочих столов, интерфейс Итссбтаржет
- Службы удаленных рабочих столов интерфейса Итссбтаржет, свойство TargetName
- Свойство TargetName службы удаленных рабочих столов, интерфейс Итссбтаржетекс
- Службы удаленных рабочих столов интерфейса Итссбтаржетекс, свойство TargetName
topic_type:
- apiref
api_name:
- ITsSbTarget.TargetName
- ITsSbTarget.get_TargetName
- ITsSbTarget.put_TargetName
- ITsSbTargetEx.TargetName
- ITsSbTargetEx.get_TargetName
- ITsSbTargetEx.put_TargetName
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7dce949abee4ca00184a2b784ab154dbd75b9de6
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104069179"
---
# <a name="itssbtargettargetname-property"></a><span data-ttu-id="6cd90-108">Свойство Итссбтаржет:: TargetName</span><span class="sxs-lookup"><span data-stu-id="6cd90-108">ITsSbTarget::TargetName property</span></span>

<span data-ttu-id="6cd90-109">Указывает или получает имя целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="6cd90-109">Specifies or retrieves the name of the target.</span></span>

<span data-ttu-id="6cd90-110">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="6cd90-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="6cd90-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6cd90-111">Syntax</span></span>


```C++
HRESULT put_TargetName(
  [in]          BSTR Val
);

HRESULT get_TargetName(
  [out, retval] BSTR *pVal
);
```



## <a name="property-value"></a><span data-ttu-id="6cd90-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="6cd90-112">Property value</span></span>

<span data-ttu-id="6cd90-113">Переменная **BSTR** , указывающая целевое имя.</span><span class="sxs-lookup"><span data-stu-id="6cd90-113">A **BSTR** variable that specifies the target name.</span></span>

## <a name="remarks"></a><span data-ttu-id="6cd90-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6cd90-114">Remarks</span></span>

<span data-ttu-id="6cd90-115">Это свойство было доступно только для чтения до Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="6cd90-115">This property was read-only prior to Windows Server 2012.</span></span>

## <a name="requirements"></a><span data-ttu-id="6cd90-116">Требования</span><span class="sxs-lookup"><span data-stu-id="6cd90-116">Requirements</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6cd90-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6cd90-117">Minimum supported client</span></span><br/></td>
<td><span data-ttu-id="6cd90-118">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="6cd90-118">None supported</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6cd90-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6cd90-119">Minimum supported server</span></span><br/></td>
<td><span data-ttu-id="6cd90-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6cd90-120">Windows Server 2012</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6cd90-121">IDL</span><span class="sxs-lookup"><span data-stu-id="6cd90-121">IDL</span></span><br/></td>
<td><dl> <span data-ttu-id="6cd90-122"><dt>Сбтсв. idl</dt> </span><span class="sxs-lookup"><span data-stu-id="6cd90-122"><dt>Sbtsv.idl</dt> </span></span></dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6cd90-123">IID</span><span class="sxs-lookup"><span data-stu-id="6cd90-123">IID</span></span><br/></td>
<td><span data-ttu-id="6cd90-124">IID_ITsSbTarget определяется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="6cd90-124">IID_ITsSbTarget is defined as:</span></span>
<ul>
<li><span data-ttu-id="6cd90-125">16616ECC-272D-411D-B324-126893033856</span><span class="sxs-lookup"><span data-stu-id="6cd90-125">16616ECC-272D-411D-B324-126893033856</span></span></li>
<li><span data-ttu-id="6cd90-126">e85e10ea-db0b-4752-b456-5fd5840901c0 на Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6cd90-126">e85e10ea-db0b-4752-b456-5fd5840901c0 on Windows Server 2008 R2</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



## <a name="see-also"></a><span data-ttu-id="6cd90-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6cd90-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6cd90-128">**итссбтаржетекс**</span><span class="sxs-lookup"><span data-stu-id="6cd90-128">**ITsSbTargetEx**</span></span>](itssbtargetex.md)
</dt> <dt>

[<span data-ttu-id="6cd90-129">**итссбтаржет**</span><span class="sxs-lookup"><span data-stu-id="6cd90-129">**ITsSbTarget**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget)
</dt> </dl>

 

 





