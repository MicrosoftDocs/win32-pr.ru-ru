---
title: Метод WSMan. Енумератионфлагнонксмлтекст (Всмандисп. h)
description: Возвращает значение константы перечисления Всманфлагнонксмлтекст для использования в параметре flags метода Session. Enumerate.
ms.assetid: 5e062e73-f833-4090-ba5a-48ca374724e7
ms.tgt_platform: multiple
keywords:
- служба удаленного управления Windows метода Енумератионфлагнонксмлтекст
- Служба удаленного управления Windows метода Енумератионфлагнонксмлтекст, объект WSMan
- Объект WSMan служба удаленного управления Windows, метод Енумератионфлагнонксмлтекст
topic_type:
- apiref
api_name:
- WSMan.EnumerationFlagNonXmlText
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26a9547f85a07702dc3735129842e5bc286ee9b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802920"
---
# <a name="wsmanenumerationflagnonxmltext-method"></a><span data-ttu-id="56b4b-106">Метод WSMan. Енумератионфлагнонксмлтекст</span><span class="sxs-lookup"><span data-stu-id="56b4b-106">WSMan.EnumerationFlagNonXmlText method</span></span>

<span data-ttu-id="56b4b-107">Функция **WSMan. енумератионфлагнонксмлтекст** возвращает значение константы перечисления **всманфлагнонксмлтекст** для использования в параметре *flags* метода [**Session. Enumerate**](session-enumerate.md) .</span><span class="sxs-lookup"><span data-stu-id="56b4b-107">The **WSMan.EnumerationFlagNonXmlText** returns the value of the enumeration constant **WSManFlagNonXmlText** for use in the *flags* parameter of the [**Session.Enumerate**](session-enumerate.md) method.</span></span> <span data-ttu-id="56b4b-108">Этот метод предоставляет более эффективный синтаксис для использования константы, поэтому скрипты не должны устанавливать постоянное значение.</span><span class="sxs-lookup"><span data-stu-id="56b4b-108">This method provides a more efficient syntax for using the constant so that scripts are not required to set a constant value.</span></span> <span data-ttu-id="56b4b-109">Дополнительные сведения о вызове этого метода см. в разделе [константы сеанса](session-constants.md).</span><span class="sxs-lookup"><span data-stu-id="56b4b-109">For more information about how to call this method, see [Session Constants](session-constants.md).</span></span>

<span data-ttu-id="56b4b-110">**Всманфлагнонксмлтекст** — это константа в перечислении **\_ \_ всманенумфлагс** .</span><span class="sxs-lookup"><span data-stu-id="56b4b-110">**WSManFlagNonXmlText** is a constant in the **\_\_WSManEnumFlags** enumeration.</span></span> <span data-ttu-id="56b4b-111">Дополнительные сведения см. в разделе [**константы перечисления**](enumeration-constants.md).</span><span class="sxs-lookup"><span data-stu-id="56b4b-111">For more information, see [**Enumeration Constants**](enumeration-constants.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="56b4b-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="56b4b-112">Syntax</span></span>


```VB
WSMan.EnumerationFlagNonXmlText( _
  ByRef flags _
)
```



## <a name="parameters"></a><span data-ttu-id="56b4b-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="56b4b-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56b4b-114">*Флаги* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="56b4b-114">*flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="56b4b-115">Значение константы.</span><span class="sxs-lookup"><span data-stu-id="56b4b-115">The value of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56b4b-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="56b4b-116">Return value</span></span>

<span data-ttu-id="56b4b-117">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="56b4b-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="56b4b-118">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="56b4b-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="56b4b-119">Требования</span><span class="sxs-lookup"><span data-stu-id="56b4b-119">Requirements</span></span>



| <span data-ttu-id="56b4b-120">Требование</span><span class="sxs-lookup"><span data-stu-id="56b4b-120">Requirement</span></span> | <span data-ttu-id="56b4b-121">Значение</span><span class="sxs-lookup"><span data-stu-id="56b4b-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="56b4b-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="56b4b-122">Minimum supported client</span></span><br/> | <span data-ttu-id="56b4b-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="56b4b-123">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="56b4b-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="56b4b-124">Minimum supported server</span></span><br/> | <span data-ttu-id="56b4b-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="56b4b-125">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="56b4b-126">Header</span><span class="sxs-lookup"><span data-stu-id="56b4b-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="56b4b-127"><dt>Всмандисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="56b4b-127"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="56b4b-128">IDL</span><span class="sxs-lookup"><span data-stu-id="56b4b-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="56b4b-129"><dt>Всмандисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="56b4b-129"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="56b4b-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="56b4b-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="56b4b-131"><dt>Всмандисп. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="56b4b-131"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="56b4b-132">DLL</span><span class="sxs-lookup"><span data-stu-id="56b4b-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="56b4b-133"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="56b4b-133"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="56b4b-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="56b4b-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56b4b-135">**Ведущий**</span><span class="sxs-lookup"><span data-stu-id="56b4b-135">**WSMan**</span></span>](wsman.md)
</dt> <dt>

[<span data-ttu-id="56b4b-136">**ивсманекс**</span><span class="sxs-lookup"><span data-stu-id="56b4b-136">**IWSManEx**</span></span>](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanex)
</dt> <dt>

[<span data-ttu-id="56b4b-137">**IWSManSession**</span><span class="sxs-lookup"><span data-stu-id="56b4b-137">**IWSManSession**</span></span>](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmansession)
</dt> </dl>

 

 





