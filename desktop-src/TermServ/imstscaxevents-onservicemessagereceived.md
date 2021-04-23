---
title: Имстскаксевентс Онсервицемессажерецеивед, метод
description: Вызывается, когда клиент получает системное сообщение.
ms.assetid: 9D230AA3-30F8-4BDF-89D6-D33AF42D0E85
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Онсервицемессажерецеивед
- Службы удаленных рабочих столов метода Онсервицемессажерецеивед, интерфейс Имстскаксевентс
- Службы удаленных рабочих столов интерфейса Имстскаксевентс, метод Онсервицемессажерецеивед
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnServiceMessageReceived
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05a26b78fa31667fb550848d4edd7918aa2bde3e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802717"
---
# <a name="imstscaxeventsonservicemessagereceived-method"></a><span data-ttu-id="7ff79-106">Метод Имстскаксевентс:: Онсервицемессажерецеивед</span><span class="sxs-lookup"><span data-stu-id="7ff79-106">IMsTscAxEvents::OnServiceMessageReceived method</span></span>

<span data-ttu-id="7ff79-107">Вызывается, когда клиент получает системное сообщение.</span><span class="sxs-lookup"><span data-stu-id="7ff79-107">Called when the client receives a system message.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ff79-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7ff79-108">Syntax</span></span>


```C++
void OnServiceMessageReceived(
  [in] BSTR serviceMessage
);
```



## <a name="parameters"></a><span data-ttu-id="7ff79-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="7ff79-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ff79-110">*сервицемессаже* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7ff79-110">*serviceMessage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ff79-111">Указывает системное сообщение.</span><span class="sxs-lookup"><span data-stu-id="7ff79-111">Specifies the system message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ff79-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7ff79-112">Return value</span></span>

<span data-ttu-id="7ff79-113">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="7ff79-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7ff79-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7ff79-114">Remarks</span></span>

<span data-ttu-id="7ff79-115">Дополнительные сведения о системных сообщениях см. [в статье Настройка обмена сообщениями для удаленный рабочий стол сервера шлюза](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/dd834700(v=ws.11)).</span><span class="sxs-lookup"><span data-stu-id="7ff79-115">For more information about system messages, see [Configure Messaging for a Remote Desktop Gateway Server](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/dd834700(v=ws.11)).</span></span>

## <a name="requirements"></a><span data-ttu-id="7ff79-116">Требования</span><span class="sxs-lookup"><span data-stu-id="7ff79-116">Requirements</span></span>



| <span data-ttu-id="7ff79-117">Требование</span><span class="sxs-lookup"><span data-stu-id="7ff79-117">Requirement</span></span> | <span data-ttu-id="7ff79-118">Значение</span><span class="sxs-lookup"><span data-stu-id="7ff79-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7ff79-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7ff79-119">Minimum supported client</span></span><br/> | <span data-ttu-id="7ff79-120">Windows 7</span><span class="sxs-lookup"><span data-stu-id="7ff79-120">Windows 7</span></span><br/>                                                                   |
| <span data-ttu-id="7ff79-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7ff79-121">Minimum supported server</span></span><br/> | <span data-ttu-id="7ff79-122">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7ff79-122">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="7ff79-123">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="7ff79-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="7ff79-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7ff79-124"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="7ff79-125">DLL</span><span class="sxs-lookup"><span data-stu-id="7ff79-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7ff79-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7ff79-126"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="7ff79-127">IID</span><span class="sxs-lookup"><span data-stu-id="7ff79-127">IID</span></span><br/>                      | <span data-ttu-id="7ff79-128">Имстскаксевентс определяется как 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="7ff79-128">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="7ff79-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7ff79-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ff79-130">**имстскаксевентс**</span><span class="sxs-lookup"><span data-stu-id="7ff79-130">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

