---
title: IMsRdpClientNonScriptable5 Усемултимон, свойство
description: Указывает, должен ли элемент управления ActiveX удаленный рабочий стол использовать несколько мониторов.
ms.assetid: 7832E025-80F6-4B4B-9829-C2D2EF2D8C37
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Усемултимон
- Службы удаленных рабочих столов свойства Усемултимон, интерфейс IMsRdpClientNonScriptable5
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable5, свойство Усемултимон
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable5.UseMultimon
- IMsRdpClientNonScriptable5.get_UseMultimon
- IMsRdpClientNonScriptable5.put_UseMultimon
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 941a2991ef5591176cd2508bbb6a097fecabebf0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988943"
---
# <a name="imsrdpclientnonscriptable5usemultimon-property"></a><span data-ttu-id="a09e8-106">Свойство IMsRdpClientNonScriptable5:: Усемултимон</span><span class="sxs-lookup"><span data-stu-id="a09e8-106">IMsRdpClientNonScriptable5::UseMultimon property</span></span>

<span data-ttu-id="a09e8-107">Указывает, должен ли элемент управления ActiveX удаленный рабочий стол использовать несколько мониторов.</span><span class="sxs-lookup"><span data-stu-id="a09e8-107">Specifies whether the Remote Desktop ActiveX control should use multiple monitors.</span></span> <span data-ttu-id="a09e8-108">Если это свойство содержит **вариант \_ true**, элемент управления будет использовать несколько мониторов.</span><span class="sxs-lookup"><span data-stu-id="a09e8-108">If this property contains **VARIANT\_TRUE**, the control will use multiple monitors.</span></span> <span data-ttu-id="a09e8-109">Если это свойство содержит **\_ значение Variant false**, элемент управления не будет использовать несколько мониторов.</span><span class="sxs-lookup"><span data-stu-id="a09e8-109">If this property contains **VARIANT\_FALSE**, the control will not use multiple monitors.</span></span>

<span data-ttu-id="a09e8-110">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="a09e8-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="a09e8-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a09e8-111">Syntax</span></span>


```C++
HRESULT put_UseMultimon(
  [in]          VARIANT_BOOL fUseMultimon
);

HRESULT get_UseMultimon(
  [out, retval] VARIANT_BOOL *pfUseMultimon
);
```



## <a name="property-value"></a><span data-ttu-id="a09e8-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="a09e8-112">Property value</span></span>

<span data-ttu-id="a09e8-113">Указывает новое значение свойства.</span><span class="sxs-lookup"><span data-stu-id="a09e8-113">Specifies the new property value.</span></span>

## <a name="requirements"></a><span data-ttu-id="a09e8-114">Требования</span><span class="sxs-lookup"><span data-stu-id="a09e8-114">Requirements</span></span>



| <span data-ttu-id="a09e8-115">Требование</span><span class="sxs-lookup"><span data-stu-id="a09e8-115">Requirement</span></span> | <span data-ttu-id="a09e8-116">Значение</span><span class="sxs-lookup"><span data-stu-id="a09e8-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a09e8-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a09e8-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a09e8-118">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a09e8-118">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="a09e8-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a09e8-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a09e8-120">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a09e8-120">Windows Server 2008 R2</span></span><br/>                                                             |
| <span data-ttu-id="a09e8-121">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="a09e8-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="a09e8-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a09e8-122"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="a09e8-123">DLL</span><span class="sxs-lookup"><span data-stu-id="a09e8-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a09e8-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a09e8-124"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="a09e8-125">IID</span><span class="sxs-lookup"><span data-stu-id="a09e8-125">IID</span></span><br/>                      | <span data-ttu-id="a09e8-126">IID \_ IMsRdpClientNonScriptable5 определен как 4f6996d5-d7b1-412c-b0ff-063718566907</span><span class="sxs-lookup"><span data-stu-id="a09e8-126">IID\_IMsRdpClientNonScriptable5 is defined as 4f6996d5-d7b1-412c-b0ff-063718566907</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a09e8-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a09e8-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a09e8-128">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="a09e8-128">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> </dl>

 

 





