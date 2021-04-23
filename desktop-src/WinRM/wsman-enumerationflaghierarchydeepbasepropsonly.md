---
title: Метод WSMan. Енумератионфлагхиерарчидипбасепропсонли (Всмандисп. h)
description: Возвращает значение флага перечисления Енумератионфлагхиерарчидипбасепропсонли для использования в параметре Flags сеанса. Enumerate.
ms.assetid: f4c5966a-0d9f-4d93-9ccd-2e8a5f32b77f
ms.tgt_platform: multiple
keywords:
- служба удаленного управления Windows метода Енумератионфлагхиерарчидипбасепропсонли
- Служба удаленного управления Windows метода Енумератионфлагхиерарчидипбасепропсонли, объект WSMan
- Объект WSMan служба удаленного управления Windows, метод Енумератионфлагхиерарчидипбасепропсонли
topic_type:
- apiref
api_name:
- WSMan.EnumerationFlagHierarchyDeepBasePropsOnly
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86a0ed7d725f60e673d3426be1b11179ec8333d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105710489"
---
# <a name="wsmanenumerationflaghierarchydeepbasepropsonly-method"></a><span data-ttu-id="006a7-106">Метод WSMan. Енумератионфлагхиерарчидипбасепропсонли</span><span class="sxs-lookup"><span data-stu-id="006a7-106">WSMan.EnumerationFlagHierarchyDeepBasePropsOnly method</span></span>

<span data-ttu-id="006a7-107">Метод **WSMan. енумератионфлагхиерарчидипбасепропсонли** возвращает значение флага перечисления **енумератионфлагхиерарчидипбасепропсонли** для использования в параметре *flags* [**сеанса. Enumerate**](session-enumerate.md).</span><span class="sxs-lookup"><span data-stu-id="006a7-107">The **WSMan.EnumerationFlagHierarchyDeepBasePropsOnly** method returns the value of the enumeration flag **EnumerationFlagHierarchyDeepBasePropsOnly** for use in the *flags* parameter of [**Session.Enumerate**](session-enumerate.md).</span></span> <span data-ttu-id="006a7-108">Этот метод предоставляет более эффективный синтаксис для использования константы, поэтому скрипты не должны устанавливать постоянное значение.</span><span class="sxs-lookup"><span data-stu-id="006a7-108">This method provides a more efficient syntax for using the constant so that scripts are not required to set a constant value.</span></span> <span data-ttu-id="006a7-109">Дополнительные сведения о вызове этого метода см. в разделе [константы сеанса](session-constants.md).</span><span class="sxs-lookup"><span data-stu-id="006a7-109">For more information about how to call this method, see [Session Constants](session-constants.md).</span></span>

<span data-ttu-id="006a7-110">**Енумератионфлагхиерарчидипбасепропсонли** является константой в перечислении **\_ всманенумфлагс** и описана в разделе [**константы перечисления**](enumeration-constants.md).</span><span class="sxs-lookup"><span data-stu-id="006a7-110">**EnumerationFlagHierarchyDeepBasePropsOnly** is a constant in the **\_WSManEnumFlags** enumeration and is described in [**Enumeration Constants**](enumeration-constants.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="006a7-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="006a7-111">Syntax</span></span>


```VB
WSMan.EnumerationFlagHierarchyDeepBasePropsOnly( _
  ByRef flags _
)
```



## <a name="parameters"></a><span data-ttu-id="006a7-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="006a7-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="006a7-113">*Флаги* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="006a7-113">*flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="006a7-114">Значение константы.</span><span class="sxs-lookup"><span data-stu-id="006a7-114">The value of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="006a7-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="006a7-115">Return value</span></span>

<span data-ttu-id="006a7-116">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="006a7-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="006a7-117">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="006a7-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="006a7-118">Требования</span><span class="sxs-lookup"><span data-stu-id="006a7-118">Requirements</span></span>



| <span data-ttu-id="006a7-119">Требование</span><span class="sxs-lookup"><span data-stu-id="006a7-119">Requirement</span></span> | <span data-ttu-id="006a7-120">Значение</span><span class="sxs-lookup"><span data-stu-id="006a7-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="006a7-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="006a7-121">Minimum supported client</span></span><br/> | <span data-ttu-id="006a7-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="006a7-122">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="006a7-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="006a7-123">Minimum supported server</span></span><br/> | <span data-ttu-id="006a7-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="006a7-124">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="006a7-125">Header</span><span class="sxs-lookup"><span data-stu-id="006a7-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="006a7-126"><dt>Всмандисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="006a7-126"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="006a7-127">IDL</span><span class="sxs-lookup"><span data-stu-id="006a7-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="006a7-128"><dt>Всмандисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="006a7-128"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="006a7-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="006a7-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="006a7-130"><dt>Всмандисп. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="006a7-130"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="006a7-131">DLL</span><span class="sxs-lookup"><span data-stu-id="006a7-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="006a7-132"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="006a7-132"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="006a7-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="006a7-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="006a7-134">**Ведущий**</span><span class="sxs-lookup"><span data-stu-id="006a7-134">**WSMan**</span></span>](wsman.md)
</dt> <dt>

[<span data-ttu-id="006a7-135">**Session**</span><span class="sxs-lookup"><span data-stu-id="006a7-135">**Session**</span></span>](session.md)
</dt> </dl>

 

 





