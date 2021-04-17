---
description: Метод SetExternalT120Address вызывается приложением для настройки внешнего адреса T. 120 для обмена данными.
ms.assetid: 094b43b9-eb15-468a-9986-86313490e1c3
title: 'Метод IH323LineEx:: SetExternalT120Address (H323priv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09756aaf77ba36497b3059f7e93829d7d6a57b42
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685284"
---
# <a name="ih323lineexsetexternalt120address-method"></a><span data-ttu-id="e63bc-103">Метод IH323LineEx:: SetExternalT120Address</span><span class="sxs-lookup"><span data-stu-id="e63bc-103">IH323LineEx::SetExternalT120Address method</span></span>

<span data-ttu-id="e63bc-104">\[**SetExternalT120Address** недоступен для использования в Windows Vista, windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="e63bc-104">\[**SetExternalT120Address** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="e63bc-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="e63bc-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="e63bc-106">Метод **SetExternalT120Address** вызывается приложением для настройки внешнего адреса T. 120 для обмена данными.</span><span class="sxs-lookup"><span data-stu-id="e63bc-106">The **SetExternalT120Address** method is called by an application to configure an external T.120 address for data exchange.</span></span> <span data-ttu-id="e63bc-107">Функция T. 120 будет объявлена во время согласования H. 245, а адрес будет использоваться в подтверждении канала Open Logic, чтобы другая конечная точка могла настроить сеансы T. 120 с помощью службы, слушающей этот адрес.</span><span class="sxs-lookup"><span data-stu-id="e63bc-107">T.120 capability will be advertised during the H.245 negotiation, and the address will be used in the open logic channel acknowledgement so that the other endpoint can set up T.120 sessions with the service listening on that address.</span></span> <span data-ttu-id="e63bc-108">Если эта функция не вызывается, поставщик службы H. 323 не будет объявлять возможность T. 120.</span><span class="sxs-lookup"><span data-stu-id="e63bc-108">If this function is not called, the H.323 service provider will not advertise T.120 capability.</span></span>

## <a name="syntax"></a><span data-ttu-id="e63bc-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e63bc-109">Syntax</span></span>


```C++
HRESULT SetExternalT120Address(
  [in] BOOL  fEnable,
  [in] DWORD dwIP,
  [in] WORD  wPort
);
```



## <a name="parameters"></a><span data-ttu-id="e63bc-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="e63bc-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e63bc-111">*фенабле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e63bc-111">*fEnable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e63bc-112">**Значение true** , чтобы включить функцию T. 120; **Значение false** , чтобы отключить возможность T. 120.</span><span class="sxs-lookup"><span data-stu-id="e63bc-112">**TRUE** to enable T.120 capability; **FALSE** to disable T.120 capability.</span></span>

</dd> <dt>

<span data-ttu-id="e63bc-113">*ДВИП* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e63bc-113">*dwIP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e63bc-114">**DWORD** , содержащий IP-адрес в порядке байтов узла внешней службы T. 120.</span><span class="sxs-lookup"><span data-stu-id="e63bc-114">**DWORD** containing the IP address in host byte order of the external T.120 service.</span></span>

</dd> <dt>

<span data-ttu-id="e63bc-115">*впорт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e63bc-115">*wPort* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e63bc-116">**Слово** , содержащее порт внешней службы T. 120.</span><span class="sxs-lookup"><span data-stu-id="e63bc-116">**WORD** containing the port of the external T.120 service.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e63bc-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e63bc-117">Return value</span></span>

<span data-ttu-id="e63bc-118">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="e63bc-118">This method can return one of these values.</span></span>



| <span data-ttu-id="e63bc-119">Код возврата</span><span class="sxs-lookup"><span data-stu-id="e63bc-119">Return code</span></span>                                                                          | <span data-ttu-id="e63bc-120">Описание</span><span class="sxs-lookup"><span data-stu-id="e63bc-120">Description</span></span>                  |
|--------------------------------------------------------------------------------------|------------------------------|
| <dl> <span data-ttu-id="e63bc-121"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="e63bc-121"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="e63bc-122">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="e63bc-122">Method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="e63bc-123">Требования</span><span class="sxs-lookup"><span data-stu-id="e63bc-123">Requirements</span></span>



| <span data-ttu-id="e63bc-124">Требование</span><span class="sxs-lookup"><span data-stu-id="e63bc-124">Requirement</span></span> | <span data-ttu-id="e63bc-125">Значение</span><span class="sxs-lookup"><span data-stu-id="e63bc-125">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e63bc-126">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="e63bc-126">TAPI version</span></span><br/> | <span data-ttu-id="e63bc-127">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="e63bc-127">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="e63bc-128">Header</span><span class="sxs-lookup"><span data-stu-id="e63bc-128">Header</span></span><br/>       | <dl> <span data-ttu-id="e63bc-129"><dt>H323priv. h</dt></span><span class="sxs-lookup"><span data-stu-id="e63bc-129"><dt>H323priv.h</dt></span></span> </dl> |
| <span data-ttu-id="e63bc-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e63bc-130">Library</span></span><br/>      | <dl> <span data-ttu-id="e63bc-131"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e63bc-131"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="e63bc-132">DLL</span><span class="sxs-lookup"><span data-stu-id="e63bc-132">DLL</span></span><br/>          | <dl> <span data-ttu-id="e63bc-133"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e63bc-133"><dt>Tapi3.dll</dt></span></span> </dl>  |



 

 




