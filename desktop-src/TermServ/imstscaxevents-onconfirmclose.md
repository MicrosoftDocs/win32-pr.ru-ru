---
title: Имстскаксевентс Онконфирмклосе, метод
description: Вызывается, когда клиент вызывает метод Имсрдпклиент RequestClose.
ms.assetid: fb149fbc-9415-4c4c-8d4b-e22214ac38cb
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Онконфирмклосе
- Службы удаленных рабочих столов метода Онконфирмклосе, интерфейс Имстскаксевентс
- Службы удаленных рабочих столов интерфейса Имстскаксевентс, метод Онконфирмклосе
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnConfirmClose
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 623196033e23a964857a6a604c7eca3904f32c60
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137770"
---
# <a name="imstscaxeventsonconfirmclose-method"></a><span data-ttu-id="35d2f-106">Метод Имстскаксевентс:: Онконфирмклосе</span><span class="sxs-lookup"><span data-stu-id="35d2f-106">IMsTscAxEvents::OnConfirmClose method</span></span>

<span data-ttu-id="35d2f-107">Вызывается, когда клиент вызывает метод [**имсрдпклиент:: RequestClose**](imsrdpclient-requestclose.md) .</span><span class="sxs-lookup"><span data-stu-id="35d2f-107">Called when the client calls the [**IMsRdpClient::RequestClose**](imsrdpclient-requestclose.md) method.</span></span> <span data-ttu-id="35d2f-108">В ответ на это событие пользователю должно быть предложено подтвердить закрытие подключения.</span><span class="sxs-lookup"><span data-stu-id="35d2f-108">In response to this event, the user should be prompted to confirm closing the connection.</span></span> <span data-ttu-id="35d2f-109">Дополнительные сведения см. в разделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="35d2f-109">For more information, see the following Remarks section.</span></span>

## <a name="syntax"></a><span data-ttu-id="35d2f-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="35d2f-110">Syntax</span></span>


```C++
void OnConfirmClose(
  [out] VARIANT_BOOL *pfAllowClose
);
```



## <a name="parameters"></a><span data-ttu-id="35d2f-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="35d2f-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35d2f-112">*пфалловклосе* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="35d2f-112">*pfAllowClose* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="35d2f-113">Если **вариант \_ true**(значение по умолчанию) указывает, что пользователь хочет закрыть соединение.</span><span class="sxs-lookup"><span data-stu-id="35d2f-113">If **VARIANT\_TRUE**, the default, indicates that the user wants to close the connection.</span></span> <span data-ttu-id="35d2f-114">Если значение **варианта \_ false**, указывает, что пользователь не хочет закрывать соединение.</span><span class="sxs-lookup"><span data-stu-id="35d2f-114">If **VARIANT\_FALSE**, indicates that the user does not want to close the connection.</span></span> <span data-ttu-id="35d2f-115">Дополнительные сведения см. в разделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="35d2f-115">For more information, see the following Remarks section.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35d2f-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="35d2f-116">Return value</span></span>

<span data-ttu-id="35d2f-117">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="35d2f-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="35d2f-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="35d2f-118">Remarks</span></span>

<span data-ttu-id="35d2f-119">Когда приложение-контейнер вызывает метод [**имсрдпклиент:: RequestClose**](imsrdpclient-requestclose.md) , этот метод возвращает значение, указывающее, должен ли контейнер ожидать возникновения события **онконфирмклосе** перед закрытием управляющего соединения.</span><span class="sxs-lookup"><span data-stu-id="35d2f-119">When a container application calls the [**IMsRdpClient::RequestClose**](imsrdpclient-requestclose.md) method, that method returns a value indicating whether the container should wait for an **OnConfirmClose** event to occur before closing the control connection.</span></span> <span data-ttu-id="35d2f-120">Если **RequestClose** возвращает **контролклосеваитфоревентс**, а пользователь подключен и вошел в сеанс службы удаленных рабочих столов, срабатывает событие **онконфирмклосе** .</span><span class="sxs-lookup"><span data-stu-id="35d2f-120">If **RequestClose** returns **controlCloseWaitForEvents**, and the user is connected and logged on to their Remote Desktop Services session, the **OnConfirmClose** event fires.</span></span> <span data-ttu-id="35d2f-121">В этот момент контейнерное приложение может запрашивать у пользователя запрос на закрытие подключения.</span><span class="sxs-lookup"><span data-stu-id="35d2f-121">At that point the container application can prompt the user, asking whether the user wants to close the connection.</span></span> <span data-ttu-id="35d2f-122">Если пользователь хочет закрыть подключение, приложение должно задать для параметра *пфалловклосе* значение **Variant \_ true** и продолжить закрытие соединения.</span><span class="sxs-lookup"><span data-stu-id="35d2f-122">If the user wants to close the connection, the application should set the *pfAllowClose* parameter to **VARIANT\_TRUE** and proceed with closing the connection.</span></span> <span data-ttu-id="35d2f-123">Если пользователь не хочет закрываться, приложение должно установить *пфалловклосе* в значение **Variant \_ false** и оставить соединение открытым.</span><span class="sxs-lookup"><span data-stu-id="35d2f-123">If the user does not want to close, the application should set *pfAllowClose* to **VARIANT\_FALSE** and leave the connection open.</span></span>

<span data-ttu-id="35d2f-124">Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="35d2f-124">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="35d2f-125">Требования</span><span class="sxs-lookup"><span data-stu-id="35d2f-125">Requirements</span></span>



| <span data-ttu-id="35d2f-126">Требование</span><span class="sxs-lookup"><span data-stu-id="35d2f-126">Requirement</span></span> | <span data-ttu-id="35d2f-127">Значение</span><span class="sxs-lookup"><span data-stu-id="35d2f-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="35d2f-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="35d2f-128">Minimum supported client</span></span><br/> | <span data-ttu-id="35d2f-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="35d2f-129">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="35d2f-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="35d2f-130">Minimum supported server</span></span><br/> | <span data-ttu-id="35d2f-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="35d2f-131">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="35d2f-132">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="35d2f-132">Type library</span></span><br/>             | <dl> <span data-ttu-id="35d2f-133"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="35d2f-133"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="35d2f-134">DLL</span><span class="sxs-lookup"><span data-stu-id="35d2f-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="35d2f-135"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="35d2f-135"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="35d2f-136">IID</span><span class="sxs-lookup"><span data-stu-id="35d2f-136">IID</span></span><br/>                      | <span data-ttu-id="35d2f-137">Имстскаксевентс определяется как 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="35d2f-137">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="35d2f-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="35d2f-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35d2f-139">**имстскаксевентс**</span><span class="sxs-lookup"><span data-stu-id="35d2f-139">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





