---
title: IMsRdpClientNonScriptable5 Ремотемониторкаунт, свойство
description: Указывает число удаленных мониторов.
ms.assetid: AFBF233D-44B2-4E6E-8C0C-A234F25B6111
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Ремотемониторкаунт
- Службы удаленных рабочих столов свойства Ремотемониторкаунт, интерфейс IMsRdpClientNonScriptable5
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable5, свойство Ремотемониторкаунт
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable5.RemoteMonitorCount
- IMsRdpClientNonScriptable5.get_RemoteMonitorCount
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63833382d5dcbd764c0139e74ef072c34b2c10ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672753"
---
# <a name="imsrdpclientnonscriptable5remotemonitorcount-property"></a><span data-ttu-id="0b9c8-106">Свойство IMsRdpClientNonScriptable5:: Ремотемониторкаунт</span><span class="sxs-lookup"><span data-stu-id="0b9c8-106">IMsRdpClientNonScriptable5::RemoteMonitorCount property</span></span>

<span data-ttu-id="0b9c8-107">Указывает число удаленных мониторов.</span><span class="sxs-lookup"><span data-stu-id="0b9c8-107">Specifies the number of remote monitors.</span></span>

<span data-ttu-id="0b9c8-108">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="0b9c8-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b9c8-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0b9c8-109">Syntax</span></span>


```C++
HRESULT get_RemoteMonitorCount(
  [out, retval] ULONG *pcRemoteMonitors
);
```



## <a name="property-value"></a><span data-ttu-id="0b9c8-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="0b9c8-110">Property value</span></span>

<span data-ttu-id="0b9c8-111">Получает значение свойства.</span><span class="sxs-lookup"><span data-stu-id="0b9c8-111">Receives the property value.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b9c8-112">Требования</span><span class="sxs-lookup"><span data-stu-id="0b9c8-112">Requirements</span></span>



| <span data-ttu-id="0b9c8-113">Требование</span><span class="sxs-lookup"><span data-stu-id="0b9c8-113">Requirement</span></span> | <span data-ttu-id="0b9c8-114">Значение</span><span class="sxs-lookup"><span data-stu-id="0b9c8-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b9c8-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0b9c8-115">Minimum supported client</span></span><br/> | <span data-ttu-id="0b9c8-116">Windows 7</span><span class="sxs-lookup"><span data-stu-id="0b9c8-116">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="0b9c8-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0b9c8-117">Minimum supported server</span></span><br/> | <span data-ttu-id="0b9c8-118">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="0b9c8-118">Windows Server 2008 R2</span></span><br/>                                                             |
| <span data-ttu-id="0b9c8-119">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="0b9c8-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="0b9c8-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0b9c8-120"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="0b9c8-121">DLL</span><span class="sxs-lookup"><span data-stu-id="0b9c8-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0b9c8-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0b9c8-122"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="0b9c8-123">IID</span><span class="sxs-lookup"><span data-stu-id="0b9c8-123">IID</span></span><br/>                      | <span data-ttu-id="0b9c8-124">IID \_ IMsRdpClientNonScriptable5 определен как 4f6996d5-d7b1-412c-b0ff-063718566907</span><span class="sxs-lookup"><span data-stu-id="0b9c8-124">IID\_IMsRdpClientNonScriptable5 is defined as 4f6996d5-d7b1-412c-b0ff-063718566907</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0b9c8-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0b9c8-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b9c8-126">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="0b9c8-126">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> </dl>

 

 





