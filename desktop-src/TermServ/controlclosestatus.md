---
title: Перечисление Контролклосестатус
description: Указывает, может ли приложение, содержащее элемент управления, немедленно закрыть элемент управления.
ms.assetid: ac2e1c68-81b1-4b51-aa7e-0ff703e619a2
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов перечисления Контролклосестатус
topic_type:
- apiref
api_name:
- ControlCloseStatus
api_location:
- MsTscAx.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6b94e0ce5cd040a2ade970f566897d2eac339dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988288"
---
# <a name="controlclosestatus-enumeration"></a><span data-ttu-id="30b64-104">Перечисление Контролклосестатус</span><span class="sxs-lookup"><span data-stu-id="30b64-104">ControlCloseStatus enumeration</span></span>

<span data-ttu-id="30b64-105">Указывает, может ли приложение, содержащее элемент управления, немедленно закрыть элемент управления.</span><span class="sxs-lookup"><span data-stu-id="30b64-105">Indicates whether the application containing the control can close the control immediately.</span></span>

## <a name="syntax"></a><span data-ttu-id="30b64-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="30b64-106">Syntax</span></span>


```C++
enum ControlCloseStatus {
  controlCloseCanProceed     = 0x0000, 
  controlCloseWaitForEvents  = 0x0001 

};
```



## <a name="constants"></a><span data-ttu-id="30b64-107">Константы</span><span class="sxs-lookup"><span data-stu-id="30b64-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="30b64-108"><span id="controlCloseCanProceed"></span><span id="controlclosecanproceed"></span><span id="CONTROLCLOSECANPROCEED"></span>**контролклосеканпроцеед**</span><span class="sxs-lookup"><span data-stu-id="30b64-108"><span id="controlCloseCanProceed"></span><span id="controlclosecanproceed"></span><span id="CONTROLCLOSECANPROCEED"></span>**controlCloseCanProceed**</span></span>
</dt> <dd>

<span data-ttu-id="30b64-109">Контейнер может немедленно закрываться.</span><span class="sxs-lookup"><span data-stu-id="30b64-109">Container can go ahead with close immediately.</span></span> <span data-ttu-id="30b64-110">Это может произойти, если элемент управления не подключен.</span><span class="sxs-lookup"><span data-stu-id="30b64-110">This can happen if the control is not connected.</span></span>

</dd> <dt>

<span data-ttu-id="30b64-111"><span id="controlCloseWaitForEvents"></span><span id="controlclosewaitforevents"></span><span id="CONTROLCLOSEWAITFOREVENTS"></span>**контролклосеваитфоревентс**</span><span class="sxs-lookup"><span data-stu-id="30b64-111"><span id="controlCloseWaitForEvents"></span><span id="controlclosewaitforevents"></span><span id="CONTROLCLOSEWAITFOREVENTS"></span>**controlCloseWaitForEvents**</span></span>
</dt> <dd>

<span data-ttu-id="30b64-112">Контейнер должен ожидать событий [**имстскаксевентс:: Ondisconnectо**](imstscaxevents-ondisconnected.md) или [**Имстскаксевентс:: онконфирмклосе**](imstscaxevents-onconfirmclose.md).</span><span class="sxs-lookup"><span data-stu-id="30b64-112">Container should wait for events [**IMsTscAxEvents::OnDisconnected**](imstscaxevents-ondisconnected.md) or [**IMsTscAxEvents::OnConfirmClose**](imstscaxevents-onconfirmclose.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="30b64-113">Требования</span><span class="sxs-lookup"><span data-stu-id="30b64-113">Requirements</span></span>



| <span data-ttu-id="30b64-114">Требование</span><span class="sxs-lookup"><span data-stu-id="30b64-114">Requirement</span></span> | <span data-ttu-id="30b64-115">Значение</span><span class="sxs-lookup"><span data-stu-id="30b64-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="30b64-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="30b64-116">Minimum supported client</span></span><br/> | <span data-ttu-id="30b64-117">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="30b64-117">Windows 8.1</span></span><br/>                                                                 |
| <span data-ttu-id="30b64-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="30b64-118">Minimum supported server</span></span><br/> | <span data-ttu-id="30b64-119">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="30b64-119">Windows Server 2012 R2</span></span><br/>                                                      |
| <span data-ttu-id="30b64-120">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="30b64-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="30b64-121"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="30b64-121"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30b64-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="30b64-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30b64-123">**Имсрдпклиент:: RequestClose**</span><span class="sxs-lookup"><span data-stu-id="30b64-123">**IMsRdpClient::RequestClose**</span></span>](imsrdpclient-requestclose.md)
</dt> <dt>

[<span data-ttu-id="30b64-124">**Имстскаксевентс:: Онконфирмклосе**</span><span class="sxs-lookup"><span data-stu-id="30b64-124">**IMsTscAxEvents::OnConfirmClose**</span></span>](imstscaxevents-onconfirmclose.md)
</dt> <dt>

[<span data-ttu-id="30b64-125">**Имстскаксевентс:: ondisconnectо**</span><span class="sxs-lookup"><span data-stu-id="30b64-125">**IMsTscAxEvents::OnDisconnected**</span></span>](imstscaxevents-ondisconnected.md)
</dt> </dl>

 

 





