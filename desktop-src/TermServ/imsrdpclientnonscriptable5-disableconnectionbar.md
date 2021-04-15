---
title: IMsRdpClientNonScriptable5 Дисаблеконнектионбар, свойство
description: Указывает, должен ли элемент управления ActiveX удаленный рабочий стол отключать панель подключения.
ms.assetid: 82c57b93-f976-43e6-97f9-3602bf97e466
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Дисаблеконнектионбар
- Службы удаленных рабочих столов свойства Дисаблеконнектионбар, интерфейс IMsRdpClientNonScriptable5
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable5, свойство Дисаблеконнектионбар
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable5.DisableConnectionBar
- IMsRdpClientNonScriptable5.put_DisableConnectionBar
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a129d4781db69a564eecbca3a715c3c5ccf1a9cc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535576"
---
# <a name="imsrdpclientnonscriptable5disableconnectionbar-property"></a><span data-ttu-id="8dfa5-106">IMsRdpClientNonScriptable5: свойство Исаблеконнектионбар:D</span><span class="sxs-lookup"><span data-stu-id="8dfa5-106">IMsRdpClientNonScriptable5::DisableConnectionBar property</span></span>

<span data-ttu-id="8dfa5-107">Указывает, должен ли элемент управления ActiveX удаленный рабочий стол отключать панель подключения.</span><span class="sxs-lookup"><span data-stu-id="8dfa5-107">Specifies whether the Remote Desktop ActiveX control should disable the connection bar.</span></span> <span data-ttu-id="8dfa5-108">Если это свойство содержит **вариант \_ true**, панель подключения должна быть отключена.</span><span class="sxs-lookup"><span data-stu-id="8dfa5-108">If this property contains **VARIANT\_TRUE**, the connection bar should be disabled.</span></span> <span data-ttu-id="8dfa5-109">Если это свойство содержит **\_ значение Variant false**, то панель подключения должна быть включена.</span><span class="sxs-lookup"><span data-stu-id="8dfa5-109">If this property contains **VARIANT\_FALSE**, the connection bar should be enabled.</span></span>

<span data-ttu-id="8dfa5-110">Это свойство доступно только на запись.</span><span class="sxs-lookup"><span data-stu-id="8dfa5-110">This property is write-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="8dfa5-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8dfa5-111">Syntax</span></span>


```C++
HRESULT put_DisableConnectionBar(
  [in] VARIANT_BOOL fDisableConnectionBar
);
```



## <a name="property-value"></a><span data-ttu-id="8dfa5-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="8dfa5-112">Property value</span></span>

<span data-ttu-id="8dfa5-113">Указывает новое значение свойства.</span><span class="sxs-lookup"><span data-stu-id="8dfa5-113">Specifies the new property value.</span></span>

## <a name="requirements"></a><span data-ttu-id="8dfa5-114">Требования</span><span class="sxs-lookup"><span data-stu-id="8dfa5-114">Requirements</span></span>



| <span data-ttu-id="8dfa5-115">Требование</span><span class="sxs-lookup"><span data-stu-id="8dfa5-115">Requirement</span></span> | <span data-ttu-id="8dfa5-116">Значение</span><span class="sxs-lookup"><span data-stu-id="8dfa5-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="8dfa5-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8dfa5-117">Minimum supported client</span></span><br/> | <span data-ttu-id="8dfa5-118">Windows 7</span><span class="sxs-lookup"><span data-stu-id="8dfa5-118">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="8dfa5-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8dfa5-119">Minimum supported server</span></span><br/> | <span data-ttu-id="8dfa5-120">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8dfa5-120">Windows Server 2008 R2</span></span><br/>                                                             |
| <span data-ttu-id="8dfa5-121">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="8dfa5-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="8dfa5-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8dfa5-122"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="8dfa5-123">DLL</span><span class="sxs-lookup"><span data-stu-id="8dfa5-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8dfa5-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8dfa5-124"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="8dfa5-125">IID</span><span class="sxs-lookup"><span data-stu-id="8dfa5-125">IID</span></span><br/>                      | <span data-ttu-id="8dfa5-126">IID \_ IMsRdpClientNonScriptable5 определен как 4f6996d5-d7b1-412c-b0ff-063718566907</span><span class="sxs-lookup"><span data-stu-id="8dfa5-126">IID\_IMsRdpClientNonScriptable5 is defined as 4f6996d5-d7b1-412c-b0ff-063718566907</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8dfa5-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8dfa5-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8dfa5-128">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="8dfa5-128">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> </dl>

 

 





