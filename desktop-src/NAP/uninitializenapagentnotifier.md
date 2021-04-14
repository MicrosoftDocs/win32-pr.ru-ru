---
title: Функция Унинитиализенапажентнотифиер (Напутил. h)
description: Отменяет подписывание вызывающего процесса от уведомлений об изменении состояния Напажент и уведомлений об изменении состояния карантина.
ms.assetid: b676ee33-caf6-48f0-acf8-5be1b23c62fe
keywords:
- Унинитиализенапажентнотифиер функция NAP
topic_type:
- apiref
api_name:
- UninitializeNapAgentNotifier
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5d68b43fba64be82908d73803113f871b08c93c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415257"
---
# <a name="uninitializenapagentnotifier-function"></a><span data-ttu-id="0923a-104">Функция Унинитиализенапажентнотифиер</span><span class="sxs-lookup"><span data-stu-id="0923a-104">UninitializeNapAgentNotifier function</span></span>

> [!Note]  
> <span data-ttu-id="0923a-105">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="0923a-105">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="0923a-106">Функция **унинитиализенапажентнотифиер** отменяет подписывание вызывающего процесса от уведомлений об изменении состояния напажент и уведомлений об изменении состояния карантина.</span><span class="sxs-lookup"><span data-stu-id="0923a-106">The **UninitializeNapAgentNotifier** function unsubscribes the calling process from NapAgent state change notifications and quarantine state change notifications.</span></span> <span data-ttu-id="0923a-107">Эти уведомления предоставляются службой Напажент.</span><span class="sxs-lookup"><span data-stu-id="0923a-107">These notifications are provided by the NapAgent service.</span></span>

## <a name="syntax"></a><span data-ttu-id="0923a-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0923a-108">Syntax</span></span>


```C++
NAPAPI VOID WINAPI UninitializeNapAgentNotifier(
  _In_ NapNotifyType type
);
```



## <a name="parameters"></a><span data-ttu-id="0923a-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="0923a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0923a-110">*тип* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0923a-110">*type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0923a-111">Значение [**напнотифитипе**](/windows/win32/api/naptypes/ne-naptypes-napnotifytype) , указывающее тип уведомлений службы, с которых отменяется подписка.</span><span class="sxs-lookup"><span data-stu-id="0923a-111">A [**NapNotifyType**](/windows/win32/api/naptypes/ne-naptypes-napnotifytype) value that specifies the type of service notifications to unsubscribe from.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0923a-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0923a-112">Return value</span></span>

<span data-ttu-id="0923a-113">Эта функция не имеет возвращаемых значений.</span><span class="sxs-lookup"><span data-stu-id="0923a-113">This function has no return values.</span></span>

## <a name="remarks"></a><span data-ttu-id="0923a-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0923a-114">Remarks</span></span>

<span data-ttu-id="0923a-115">Эта функция не является потокобезопасной.</span><span class="sxs-lookup"><span data-stu-id="0923a-115">This function is not thread safe.</span></span>

<span data-ttu-id="0923a-116">Каждый процесс, подписанный на уведомления службы Напажент указанного *типа* , должен вызывать **унинитиализенапажентнотифиер** для отмены подписки на уведомления.</span><span class="sxs-lookup"><span data-stu-id="0923a-116">Each process subscribed to NapAgent service notifications of the specified *type* must call **UninitializeNapAgentNotifier** to unsubscribe from notifications.</span></span> <span data-ttu-id="0923a-117">Если процесс подписан на более одного типа уведомлений, он должен вызывать **унинитиализенапажентнотифиер** один раз для каждого типа уведомления.</span><span class="sxs-lookup"><span data-stu-id="0923a-117">If a process is subscribed to more than one type of notification, it must call **UninitializeNapAgentNotifier** once for each type of notification.</span></span>

<span data-ttu-id="0923a-118">Эта функция завершается со сбоем автоматически, если процесс ранее не вызывал [**инитиализенапажентнотифиер**](initializenapagentnotifier.md) для типа уведомления.</span><span class="sxs-lookup"><span data-stu-id="0923a-118">This function will fail silently if the process had not previously called [**InitializeNapAgentNotifier**](initializenapagentnotifier.md) for the notification type.</span></span>

## <a name="requirements"></a><span data-ttu-id="0923a-119">Требования</span><span class="sxs-lookup"><span data-stu-id="0923a-119">Requirements</span></span>



| <span data-ttu-id="0923a-120">Требование</span><span class="sxs-lookup"><span data-stu-id="0923a-120">Requirement</span></span> | <span data-ttu-id="0923a-121">Значение</span><span class="sxs-lookup"><span data-stu-id="0923a-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="0923a-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0923a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="0923a-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0923a-123">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="0923a-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0923a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="0923a-125">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0923a-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="0923a-126">Header</span><span class="sxs-lookup"><span data-stu-id="0923a-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="0923a-127"><dt>Напутил. h</dt></span><span class="sxs-lookup"><span data-stu-id="0923a-127"><dt>NapUtil.h</dt></span></span> </dl> |
| <span data-ttu-id="0923a-128">DLL</span><span class="sxs-lookup"><span data-stu-id="0923a-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0923a-129"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0923a-129"><dt>Qutil.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0923a-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0923a-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0923a-131">**инитиализенапажентнотифиер**</span><span class="sxs-lookup"><span data-stu-id="0923a-131">**InitializeNapAgentNotifier**</span></span>](initializenapagentnotifier.md)
</dt> </dl>

 

 





