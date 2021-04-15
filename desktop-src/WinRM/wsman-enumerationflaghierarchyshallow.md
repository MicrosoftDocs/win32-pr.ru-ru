---
title: Метод WSMan. Енумератионфлагхиерарчишаллов (Всмандисп. h)
description: Возвращает значение флага перечисления Енумератионфлагхиерарчишаллов для использования в параметре Flags сеанса. Enumerate.
ms.assetid: 18b564e6-dda1-44b9-b445-26c6183b6af9
ms.tgt_platform: multiple
keywords:
- служба удаленного управления Windows метода Енумератионфлагхиерарчишаллов
- Служба удаленного управления Windows метода Енумератионфлагхиерарчишаллов, объект WSMan
- Объект WSMan служба удаленного управления Windows, метод Енумератионфлагхиерарчишаллов
topic_type:
- apiref
api_name:
- WSMan.EnumerationFlagHierarchyShallow
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46b74552fd88ac370ad4a3f8b885a7f61e65a053
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534526"
---
# <a name="wsmanenumerationflaghierarchyshallow-method"></a><span data-ttu-id="3ded0-106">Метод WSMan. Енумератионфлагхиерарчишаллов</span><span class="sxs-lookup"><span data-stu-id="3ded0-106">WSMan.EnumerationFlagHierarchyShallow method</span></span>

<span data-ttu-id="3ded0-107">Метод **енумератионфлагхиерарчишаллов** возвращает значение флага перечисления **енумератионфлагхиерарчишаллов** для использования в параметре *flags* [**сеанса. Enumerate**](session-enumerate.md).</span><span class="sxs-lookup"><span data-stu-id="3ded0-107">The **EnumerationFlagHierarchyShallow** method returns the value of the enumeration flag **EnumerationFlagHierarchyShallow** for use in the *flags* parameter of [**Session.Enumerate**](session-enumerate.md).</span></span> <span data-ttu-id="3ded0-108">Этот метод предоставляет более эффективный синтаксис для использования константы, поэтому скрипты не должны устанавливать постоянное значение.</span><span class="sxs-lookup"><span data-stu-id="3ded0-108">This method provides a more efficient syntax for using the constant so that scripts are not required to set a constant value.</span></span> <span data-ttu-id="3ded0-109">Дополнительные сведения о вызове этого метода см. в разделе [константы сеанса](session-constants.md).</span><span class="sxs-lookup"><span data-stu-id="3ded0-109">For more information about how to call this method, see [Session Constants](session-constants.md).</span></span>

<span data-ttu-id="3ded0-110">**Енумератионфлагхиерарчишаллов** является константой в перечислении **\_ всманенумфлагс** и описана в разделе [**константы перечисления**](enumeration-constants.md).</span><span class="sxs-lookup"><span data-stu-id="3ded0-110">**EnumerationFlagHierarchyShallow** is a constant in the **\_WSManEnumFlags** enumeration and is described in [**Enumeration Constants**](enumeration-constants.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="3ded0-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3ded0-111">Syntax</span></span>


```VB
WSMan.EnumerationFlagHierarchyShallow( _
  ByRef flags _
)
```



## <a name="parameters"></a><span data-ttu-id="3ded0-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="3ded0-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ded0-113">*Флаги* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="3ded0-113">*flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3ded0-114">Значение константы.</span><span class="sxs-lookup"><span data-stu-id="3ded0-114">The value of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ded0-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3ded0-115">Return value</span></span>

<span data-ttu-id="3ded0-116">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="3ded0-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3ded0-117">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3ded0-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ded0-118">Требования</span><span class="sxs-lookup"><span data-stu-id="3ded0-118">Requirements</span></span>



| <span data-ttu-id="3ded0-119">Требование</span><span class="sxs-lookup"><span data-stu-id="3ded0-119">Requirement</span></span> | <span data-ttu-id="3ded0-120">Значение</span><span class="sxs-lookup"><span data-stu-id="3ded0-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ded0-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3ded0-121">Minimum supported client</span></span><br/> | <span data-ttu-id="3ded0-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3ded0-122">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="3ded0-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3ded0-123">Minimum supported server</span></span><br/> | <span data-ttu-id="3ded0-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3ded0-124">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="3ded0-125">Header</span><span class="sxs-lookup"><span data-stu-id="3ded0-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="3ded0-126"><dt>Всмандисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="3ded0-126"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="3ded0-127">IDL</span><span class="sxs-lookup"><span data-stu-id="3ded0-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3ded0-128"><dt>Всмандисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3ded0-128"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="3ded0-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="3ded0-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="3ded0-130"><dt>Всмандисп. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="3ded0-130"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="3ded0-131">DLL</span><span class="sxs-lookup"><span data-stu-id="3ded0-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3ded0-132"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3ded0-132"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="3ded0-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3ded0-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ded0-134">**Ведущий**</span><span class="sxs-lookup"><span data-stu-id="3ded0-134">**WSMan**</span></span>](wsman.md)
</dt> <dt>

[<span data-ttu-id="3ded0-135">**Session**</span><span class="sxs-lookup"><span data-stu-id="3ded0-135">**Session**</span></span>](session.md)
</dt> </dl>

 

 





