---
title: IMsRdpClientNonScriptable5 Алловпромптингфоркредентиалс, свойство
description: Указывает, может ли элемент управления удаленный рабочий стол ActiveX запрашивать учетные данные у пользователя.
ms.assetid: 9a780886-39ee-4d3b-9a54-fa209708d9f8
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Алловпромптингфоркредентиалс
- Службы удаленных рабочих столов свойства Алловпромптингфоркредентиалс, интерфейс IMsRdpClientNonScriptable5
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable5, свойство Алловпромптингфоркредентиалс
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable5.AllowPromptingForCredentials
- IMsRdpClientNonScriptable5.get_AllowPromptingForCredentials
- IMsRdpClientNonScriptable5.put_AllowPromptingForCredentials
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c326a83a46b41d3578c958e24fd901beb7c7b321
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105682146"
---
# <a name="imsrdpclientnonscriptable5allowpromptingforcredentials-property"></a><span data-ttu-id="c9a0f-106">Свойство IMsRdpClientNonScriptable5:: Алловпромптингфоркредентиалс</span><span class="sxs-lookup"><span data-stu-id="c9a0f-106">IMsRdpClientNonScriptable5::AllowPromptingForCredentials property</span></span>

<span data-ttu-id="c9a0f-107">Указывает, может ли элемент управления удаленный рабочий стол ActiveX запрашивать учетные данные у пользователя.</span><span class="sxs-lookup"><span data-stu-id="c9a0f-107">Specifies whether the Remote Desktop ActiveX control can prompt the user for credentials.</span></span> <span data-ttu-id="c9a0f-108">Если это свойство содержит **вариант \_ true**, пользователю может быть предложено ввести учетные данные.</span><span class="sxs-lookup"><span data-stu-id="c9a0f-108">If this property contains **VARIANT\_TRUE**, the user can be prompted for credentials.</span></span> <span data-ttu-id="c9a0f-109">Если это свойство содержит **вариант \_ false**, пользователю не может быть предложено ввести учетные данные.</span><span class="sxs-lookup"><span data-stu-id="c9a0f-109">If this property contains **VARIANT\_FALSE**, the user cannot be prompted for credentials.</span></span>

<span data-ttu-id="c9a0f-110">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="c9a0f-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9a0f-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c9a0f-111">Syntax</span></span>


```C++
HRESULT put_AllowPromptingForCredentials(
  [in]          VARIANT_BOOL fAllow
);

HRESULT get_AllowPromptingForCredentials(
  [out, retval] VARIANT_BOOL *pfAllow
);
```



## <a name="property-value"></a><span data-ttu-id="c9a0f-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="c9a0f-112">Property value</span></span>

<span data-ttu-id="c9a0f-113">Указывает новое значение свойства.</span><span class="sxs-lookup"><span data-stu-id="c9a0f-113">Specifies the new property value.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9a0f-114">Требования</span><span class="sxs-lookup"><span data-stu-id="c9a0f-114">Requirements</span></span>



| <span data-ttu-id="c9a0f-115">Требование</span><span class="sxs-lookup"><span data-stu-id="c9a0f-115">Requirement</span></span> | <span data-ttu-id="c9a0f-116">Значение</span><span class="sxs-lookup"><span data-stu-id="c9a0f-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9a0f-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c9a0f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c9a0f-118">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c9a0f-118">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="c9a0f-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c9a0f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="c9a0f-120">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c9a0f-120">Windows Server 2008 R2</span></span><br/>                                                             |
| <span data-ttu-id="c9a0f-121">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="c9a0f-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="c9a0f-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c9a0f-122"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="c9a0f-123">DLL</span><span class="sxs-lookup"><span data-stu-id="c9a0f-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c9a0f-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c9a0f-124"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="c9a0f-125">IID</span><span class="sxs-lookup"><span data-stu-id="c9a0f-125">IID</span></span><br/>                      | <span data-ttu-id="c9a0f-126">IID \_ IMsRdpClientNonScriptable5 определен как 4f6996d5-d7b1-412c-b0ff-063718566907</span><span class="sxs-lookup"><span data-stu-id="c9a0f-126">IID\_IMsRdpClientNonScriptable5 is defined as 4f6996d5-d7b1-412c-b0ff-063718566907</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c9a0f-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c9a0f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9a0f-128">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="c9a0f-128">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> </dl>

 

 





