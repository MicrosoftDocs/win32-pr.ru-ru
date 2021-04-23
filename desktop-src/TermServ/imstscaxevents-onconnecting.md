---
title: Метод OnConnect Имстскаксевентс
description: Вызывается, когда клиентский элемент управления начинает подключаться к серверу в ответ на вызов Имстскакс Connect.
ms.assetid: c5e367a8-126a-48bb-bc94-1063f77e8239
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода OnConnect
- Метод OnConnect службы удаленных рабочих столов, интерфейс Имстскаксевентс
- Интерфейс Имстскаксевентс службы удаленных рабочих столов, метод OnConnect
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnConnecting
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2004fde83b79aff7b7c5082562de94f943eacb25
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104414749"
---
# <a name="imstscaxeventsonconnecting-method"></a><span data-ttu-id="019dd-106">Метод Имстскаксевентс:: OnConnect</span><span class="sxs-lookup"><span data-stu-id="019dd-106">IMsTscAxEvents::OnConnecting method</span></span>

<span data-ttu-id="019dd-107">Вызывается, когда клиентский элемент управления начинает подключаться к серверу в ответ на вызов [**имстскакс:: Connect**](imstscax-connect.md).</span><span class="sxs-lookup"><span data-stu-id="019dd-107">Called when the client control begins connecting to a server in response to a call to [**IMsTscAx::Connect**](imstscax-connect.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="019dd-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="019dd-108">Syntax</span></span>


```C++
void OnConnecting();
```



## <a name="parameters"></a><span data-ttu-id="019dd-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="019dd-109">Parameters</span></span>

<span data-ttu-id="019dd-110">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="019dd-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="019dd-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="019dd-111">Return value</span></span>

<span data-ttu-id="019dd-112">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="019dd-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="019dd-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="019dd-113">Remarks</span></span>

<span data-ttu-id="019dd-114">Реализуйте этот метод в приемнике событий, чтобы получить уведомление о начале подключения элемента управления.</span><span class="sxs-lookup"><span data-stu-id="019dd-114">Implement this method in your event sink to receive notification that the control has begun connecting.</span></span>

## <a name="examples"></a><span data-ttu-id="019dd-115">Примеры</span><span class="sxs-lookup"><span data-stu-id="019dd-115">Examples</span></span>

<span data-ttu-id="019dd-116">В следующем примере показано, как обрабатывает это событие с помощью Visual Basic кода скрипта.</span><span class="sxs-lookup"><span data-stu-id="019dd-116">The following example shows how to handle this event with Visual Basic Scripting code.</span></span> <span data-ttu-id="019dd-117">В этом примере предполагается, что управляющий объект называется "Мсрдпклиент".</span><span class="sxs-lookup"><span data-stu-id="019dd-117">The assumption in this example is that your control object is named "MsRdpClient".</span></span>

<span data-ttu-id="019dd-118">Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="019dd-118">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>


```VB
Sub MsRdpClient.OnConnecting()
    Msgbox("Connecting")
End sub
```



## <a name="requirements"></a><span data-ttu-id="019dd-119">Требования</span><span class="sxs-lookup"><span data-stu-id="019dd-119">Requirements</span></span>



| <span data-ttu-id="019dd-120">Требование</span><span class="sxs-lookup"><span data-stu-id="019dd-120">Requirement</span></span> | <span data-ttu-id="019dd-121">Значение</span><span class="sxs-lookup"><span data-stu-id="019dd-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="019dd-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="019dd-122">Minimum supported client</span></span><br/> | <span data-ttu-id="019dd-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="019dd-123">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="019dd-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="019dd-124">Minimum supported server</span></span><br/> | <span data-ttu-id="019dd-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="019dd-125">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="019dd-126">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="019dd-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="019dd-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="019dd-127"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="019dd-128">DLL</span><span class="sxs-lookup"><span data-stu-id="019dd-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="019dd-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="019dd-129"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="019dd-130">IID</span><span class="sxs-lookup"><span data-stu-id="019dd-130">IID</span></span><br/>                      | <span data-ttu-id="019dd-131">Имстскаксевентс определяется как 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="019dd-131">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="019dd-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="019dd-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="019dd-133">**имстскаксевентс**</span><span class="sxs-lookup"><span data-stu-id="019dd-133">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





