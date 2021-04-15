---
title: Метод WSMan. Енумератионфлагретурнепр (Всмандисп. h)
description: Возвращает значение флага перечисления Енумератионфлагретурнепр для использования в параметре Flags сеанса. Enumerate.
ms.assetid: 5e168aa9-5be1-46b3-bb9b-59895e68a75d
ms.tgt_platform: multiple
keywords:
- служба удаленного управления Windows метода Енумератионфлагретурнепр
- Служба удаленного управления Windows метода Енумератионфлагретурнепр, объект WSMan
- Объект WSMan служба удаленного управления Windows, метод Енумератионфлагретурнепр
topic_type:
- apiref
api_name:
- WSMan.EnumerationFlagReturnEPR
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 129aca059bcca1b1a6f6729d4df97fbf8617fa52
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489105"
---
# <a name="wsmanenumerationflagreturnepr-method"></a><span data-ttu-id="0b833-106">Метод WSMan. Енумератионфлагретурнепр</span><span class="sxs-lookup"><span data-stu-id="0b833-106">WSMan.EnumerationFlagReturnEPR method</span></span>

<span data-ttu-id="0b833-107">Метод **енумератионфлагретурнепр** возвращает значение флага перечисления **енумератионфлагретурнепр** для использования в параметре *flags* [**сеанса. Enumerate**](session-enumerate.md).</span><span class="sxs-lookup"><span data-stu-id="0b833-107">The **EnumerationFlagReturnEPR** method returns the value of the enumeration flag **EnumerationFlagReturnEPR** for use in the *flags* parameter of [**Session.Enumerate**](session-enumerate.md).</span></span> <span data-ttu-id="0b833-108">Этот метод предоставляет более эффективный синтаксис для использования константы, поэтому скрипты не должны устанавливать постоянное значение.</span><span class="sxs-lookup"><span data-stu-id="0b833-108">This method provides a more efficient syntax for using the constant so that scripts are not required to set a constant value.</span></span> <span data-ttu-id="0b833-109">Дополнительные сведения о вызове этого метода см. в разделе [константы сеанса](session-constants.md).</span><span class="sxs-lookup"><span data-stu-id="0b833-109">For more information about how to call this method, see [Session Constants](session-constants.md).</span></span>

<span data-ttu-id="0b833-110">**Енумератионфлагретурнепр** является константой в перечислении **\_ всманенумфлагс** и описана в разделе [**константы перечисления**](enumeration-constants.md).</span><span class="sxs-lookup"><span data-stu-id="0b833-110">**EnumerationFlagReturnEPR** is a constant in the **\_WSManEnumFlags** enumeration and is described in [**Enumeration Constants**](enumeration-constants.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="0b833-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0b833-111">Syntax</span></span>


```VB
WSMan.EnumerationFlagReturnEPR( _
  ByRef flags _
)
```



## <a name="parameters"></a><span data-ttu-id="0b833-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="0b833-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b833-113">*Флаги* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="0b833-113">*flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0b833-114">Значение константы.</span><span class="sxs-lookup"><span data-stu-id="0b833-114">The value of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b833-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0b833-115">Return value</span></span>

<span data-ttu-id="0b833-116">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="0b833-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0b833-117">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0b833-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b833-118">Требования</span><span class="sxs-lookup"><span data-stu-id="0b833-118">Requirements</span></span>



| <span data-ttu-id="0b833-119">Требование</span><span class="sxs-lookup"><span data-stu-id="0b833-119">Requirement</span></span> | <span data-ttu-id="0b833-120">Значение</span><span class="sxs-lookup"><span data-stu-id="0b833-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b833-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0b833-121">Minimum supported client</span></span><br/> | <span data-ttu-id="0b833-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0b833-122">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="0b833-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0b833-123">Minimum supported server</span></span><br/> | <span data-ttu-id="0b833-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0b833-124">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="0b833-125">Header</span><span class="sxs-lookup"><span data-stu-id="0b833-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="0b833-126"><dt>Всмандисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="0b833-126"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="0b833-127">IDL</span><span class="sxs-lookup"><span data-stu-id="0b833-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0b833-128"><dt>Всмандисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0b833-128"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="0b833-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="0b833-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="0b833-130"><dt>Всмандисп. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="0b833-130"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="0b833-131">DLL</span><span class="sxs-lookup"><span data-stu-id="0b833-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0b833-132"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0b833-132"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0b833-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0b833-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b833-134">**Ведущий**</span><span class="sxs-lookup"><span data-stu-id="0b833-134">**WSMan**</span></span>](wsman.md)
</dt> <dt>

[<span data-ttu-id="0b833-135">**Session**</span><span class="sxs-lookup"><span data-stu-id="0b833-135">**Session**</span></span>](session.md)
</dt> </dl>

 

 





