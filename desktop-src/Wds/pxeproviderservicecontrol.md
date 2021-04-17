---
title: Функция обратного вызова Пксепровидерсервицеконтрол
description: Вызывается, когда служба WDS получает код управления службой.
ms.assetid: 180ddcda-d111-4c81-9177-db99cbf1449f
keywords:
- Функция обратного вызова Пксепровидерсервицеконтрол службы развертывания Windows
topic_type:
- apiref
api_name:
- PxeProviderServiceControl
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8c8a2c71b7b386254622758efa5f3dc5269a131d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105701046"
---
# <a name="pxeproviderservicecontrol-callback-function"></a><span data-ttu-id="0fbb0-104">Функция обратного вызова Пксепровидерсервицеконтрол</span><span class="sxs-lookup"><span data-stu-id="0fbb0-104">PxeProviderServiceControl callback function</span></span>

<span data-ttu-id="0fbb0-105">Вызывается, когда служба WDS получает код управления службой.</span><span class="sxs-lookup"><span data-stu-id="0fbb0-105">Called when a service control code is received by the WDS service.</span></span> <span data-ttu-id="0fbb0-106">Эта функция обратного вызова регистрируется путем вызова функции [**пксерегистеркаллбакк**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) с параметром *каллбакктипе* , установленным в **\_ \_ \_ элемент управления обратного вызова PXE**.</span><span class="sxs-lookup"><span data-stu-id="0fbb0-106">This callback function is registered by calling the [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) function with the *CallbackType* parameter set to **PXE\_CALLBACK\_SERVICE\_CONTROL**.</span></span>

## <a name="syntax"></a><span data-ttu-id="0fbb0-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0fbb0-107">Syntax</span></span>


```C++
DWORD PXEAPI PxeProviderServiceControl(
  _In_ PVOID pContext,
       DWORD dwControl
);
```



## <a name="parameters"></a><span data-ttu-id="0fbb0-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="0fbb0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0fbb0-109">*пконтекст* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0fbb0-109">*pContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0fbb0-110">Значение контекста, передаваемое функции [**пксерегистеркаллбакк**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) .</span><span class="sxs-lookup"><span data-stu-id="0fbb0-110">Context value passed to the [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) function.</span></span>

</dd> <dt>

<span data-ttu-id="0fbb0-111">*двконтрол*</span><span class="sxs-lookup"><span data-stu-id="0fbb0-111">*dwControl*</span></span> 
</dt> <dd>

<span data-ttu-id="0fbb0-112">Контрольный код.</span><span class="sxs-lookup"><span data-stu-id="0fbb0-112">Control code.</span></span> <span data-ttu-id="0fbb0-113">Список возможных значений см. в описании параметра *двконтрол* функции [*хандлерекс*](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex) .</span><span class="sxs-lookup"><span data-stu-id="0fbb0-113">For the list of possible values, see the *dwControl* parameter of the [*HandlerEx*](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0fbb0-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0fbb0-114">Return value</span></span>

<span data-ttu-id="0fbb0-115">Если завершение работы поставщика завершается успешно, обратный вызов должен возвращать **ошибку \_ успешно**.</span><span class="sxs-lookup"><span data-stu-id="0fbb0-115">If the provider shutdown succeeds, the callback should return **ERROR\_SUCCESS**.</span></span> <span data-ttu-id="0fbb0-116">В случае сбоя должен возвращаться соответствующий код ошибки.</span><span class="sxs-lookup"><span data-stu-id="0fbb0-116">In case of failure, an appropriate error code should be returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="0fbb0-117">Требования</span><span class="sxs-lookup"><span data-stu-id="0fbb0-117">Requirements</span></span>



| <span data-ttu-id="0fbb0-118">Требование</span><span class="sxs-lookup"><span data-stu-id="0fbb0-118">Requirement</span></span> | <span data-ttu-id="0fbb0-119">Значение</span><span class="sxs-lookup"><span data-stu-id="0fbb0-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0fbb0-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0fbb0-120">Minimum supported client</span></span><br/> | <span data-ttu-id="0fbb0-121">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="0fbb0-121">None supported</span></span><br/>                                                          |
| <span data-ttu-id="0fbb0-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0fbb0-122">Minimum supported server</span></span><br/> | <span data-ttu-id="0fbb0-123">Windows Server 2008, Windows Server 2003 с пакетом обновления 2 (SP2), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="0fbb0-123">Windows Server 2008, Windows Server 2003 with SP2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0fbb0-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0fbb0-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0fbb0-125">Функции сервера служб развертывания Windows</span><span class="sxs-lookup"><span data-stu-id="0fbb0-125">Windows Deployment Services Server Functions</span></span>](windows-deployment-services-server-functions.md)
</dt> <dt>

[<span data-ttu-id="0fbb0-126">**пксерегистеркаллбакк**</span><span class="sxs-lookup"><span data-stu-id="0fbb0-126">**PxeRegisterCallback**</span></span>](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback)
</dt> </dl>

 

