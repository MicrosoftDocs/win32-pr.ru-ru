---
title: IMsRdpClientNonScriptable5 Дисаблеремотеаппкапсчекк, свойство
description: Указывает, должен ли элемент управления ActiveX удаленный рабочий стол не проверять наличие у сервера возможностей RemoteApp.
ms.assetid: dcc44d4b-ece5-4f5b-a00a-f90d7a2fa11a
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Дисаблеремотеаппкапсчекк
- Службы удаленных рабочих столов свойства Дисаблеремотеаппкапсчекк, интерфейс IMsRdpClientNonScriptable5
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable5, свойство Дисаблеремотеаппкапсчекк
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable5.DisableRemoteAppCapsCheck
- IMsRdpClientNonScriptable5.get_DisableRemoteAppCapsCheck
- IMsRdpClientNonScriptable5.put_DisableRemoteAppCapsCheck
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4f65b0e1b56b3a1152f71aff25d4cf65a4420d1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493179"
---
# <a name="imsrdpclientnonscriptable5disableremoteappcapscheck-property"></a><span data-ttu-id="d47d1-106">IMsRdpClientNonScriptable5: свойство Исаблеремотеаппкапсчекк:D</span><span class="sxs-lookup"><span data-stu-id="d47d1-106">IMsRdpClientNonScriptable5::DisableRemoteAppCapsCheck property</span></span>

<span data-ttu-id="d47d1-107">Указывает, должен ли элемент управления ActiveX удаленный рабочий стол не проверять наличие у сервера возможностей RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="d47d1-107">Specifies whether the Remote Desktop ActiveX control should not check the server for RemoteApp capabilities.</span></span> <span data-ttu-id="d47d1-108">Если это свойство содержит **вариант \_ true**, элемент управления не должен проверять сервер на наличие возможностей RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="d47d1-108">If this property contains **VARIANT\_TRUE**, the control should not check the server for RemoteApp capabilities.</span></span> <span data-ttu-id="d47d1-109">Если это свойство содержит **\_ значение Variant false**, элемент управления может проверить наличие возможностей удаленного приложения RemoteApp на сервере.</span><span class="sxs-lookup"><span data-stu-id="d47d1-109">If this property contains **VARIANT\_FALSE**, the control can check the server for RemoteApp capabilities.</span></span>

<span data-ttu-id="d47d1-110">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="d47d1-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="d47d1-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d47d1-111">Syntax</span></span>


```C++
HRESULT put_DisableRemoteAppCapsCheck(
  [in]          VARIANT_BOOL fDisableRemoteAppCapsCheck
);

HRESULT get_DisableRemoteAppCapsCheck(
  [out, retval] VARIANT_BOOL *pfDisableRemoteAppCapsCheck
);
```



## <a name="property-value"></a><span data-ttu-id="d47d1-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="d47d1-112">Property value</span></span>

<span data-ttu-id="d47d1-113">Указывает новое значение свойства.</span><span class="sxs-lookup"><span data-stu-id="d47d1-113">Specifies the new property value.</span></span>

## <a name="requirements"></a><span data-ttu-id="d47d1-114">Требования</span><span class="sxs-lookup"><span data-stu-id="d47d1-114">Requirements</span></span>



| <span data-ttu-id="d47d1-115">Требование</span><span class="sxs-lookup"><span data-stu-id="d47d1-115">Requirement</span></span> | <span data-ttu-id="d47d1-116">Значение</span><span class="sxs-lookup"><span data-stu-id="d47d1-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d47d1-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d47d1-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d47d1-118">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d47d1-118">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="d47d1-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d47d1-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d47d1-120">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d47d1-120">Windows Server 2008 R2</span></span><br/>                                                             |
| <span data-ttu-id="d47d1-121">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="d47d1-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="d47d1-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d47d1-122"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="d47d1-123">DLL</span><span class="sxs-lookup"><span data-stu-id="d47d1-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d47d1-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d47d1-124"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="d47d1-125">IID</span><span class="sxs-lookup"><span data-stu-id="d47d1-125">IID</span></span><br/>                      | <span data-ttu-id="d47d1-126">IID \_ IMsRdpClientNonScriptable5 определен как 4f6996d5-d7b1-412c-b0ff-063718566907</span><span class="sxs-lookup"><span data-stu-id="d47d1-126">IID\_IMsRdpClientNonScriptable5 is defined as 4f6996d5-d7b1-412c-b0ff-063718566907</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d47d1-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d47d1-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d47d1-128">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="d47d1-128">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> </dl>

 

 





