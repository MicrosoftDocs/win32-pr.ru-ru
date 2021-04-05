---
title: Метод Енроллмесод класса MDM_ClientCertificateInstall_Install03
description: Активирует устройство для запуска регистрации сертификата.
ms.assetid: 21a31574-0b19-44bf-90db-4bb9e2611364
keywords:
- Метод Енроллмесод
- Метод Енроллмесод, класс MDM_ClientCertificateInstall_Install03
- Класс MDM_ClientCertificateInstall_Install03, метод Енроллмесод
topic_type:
- apiref
api_name:
- MDM_ClientCertificateInstall_Install03.EnrollMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7903407d5a97f056835e529eb21408bdcbe800ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803130"
---
# <a name="enrollmethod-method-of-the-mdm_clientcertificateinstall_install03-class"></a><span data-ttu-id="ca06a-106">Метод Енроллмесод \_ класса MDM клиентцертификатеинсталл \_ Install03</span><span class="sxs-lookup"><span data-stu-id="ca06a-106">EnrollMethod method of the MDM\_ClientCertificateInstall\_Install03 class</span></span>

<span data-ttu-id="ca06a-107">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="ca06a-107">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="ca06a-108">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="ca06a-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="ca06a-109">Активирует устройство для запуска регистрации сертификата.</span><span class="sxs-lookup"><span data-stu-id="ca06a-109">Triggers the device to start the certificate enrollment.</span></span> <span data-ttu-id="ca06a-110">Устройство не будет уведомлять сервер MDM после того, как будет выполнена регистрация сертификата.</span><span class="sxs-lookup"><span data-stu-id="ca06a-110">The device will not notify MDM server after certificate enrollment is done.</span></span> <span data-ttu-id="ca06a-111">Сервер MDM может позже запросить устройство, чтобы узнать, добавлен ли новый сертификат.</span><span class="sxs-lookup"><span data-stu-id="ca06a-111">The MDM server could later query the device to find out whether new certificate is added.</span></span> <span data-ttu-id="ca06a-112">См. также [**Регистрация**](/windows/client-management/mdm/clientcertificateinstall-csp).</span><span class="sxs-lookup"><span data-stu-id="ca06a-112">See also, [**Enroll**](/windows/client-management/mdm/clientcertificateinstall-csp).</span></span>

## <a name="syntax"></a><span data-ttu-id="ca06a-113">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ca06a-113">Syntax</span></span>


```mof
uint32 EnrollMethod();
```



## <a name="parameters"></a><span data-ttu-id="ca06a-114">Параметры</span><span class="sxs-lookup"><span data-stu-id="ca06a-114">Parameters</span></span>

<span data-ttu-id="ca06a-115">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="ca06a-115">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ca06a-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ca06a-116">Return value</span></span>

<span data-ttu-id="ca06a-117">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="ca06a-117">Required.</span></span> <span data-ttu-id="ca06a-118">Активирует устройство для запуска регистрации сертификата.</span><span class="sxs-lookup"><span data-stu-id="ca06a-118">Triggers the device to start the certificate enrollment.</span></span> <span data-ttu-id="ca06a-119">Устройство не будет уведомлять сервер MDM после того, как будет выполнена регистрация сертификата.</span><span class="sxs-lookup"><span data-stu-id="ca06a-119">The device will not notify MDM server after certificate enrollment is done.</span></span> <span data-ttu-id="ca06a-120">Сервер MDM может позже запросить устройство, чтобы узнать, добавлен ли новый сертификат.</span><span class="sxs-lookup"><span data-stu-id="ca06a-120">The MDM server could later query the device to find out whether new certificate is added.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca06a-121">Требования</span><span class="sxs-lookup"><span data-stu-id="ca06a-121">Requirements</span></span>



| <span data-ttu-id="ca06a-122">Требование</span><span class="sxs-lookup"><span data-stu-id="ca06a-122">Requirement</span></span> | <span data-ttu-id="ca06a-123">Значение</span><span class="sxs-lookup"><span data-stu-id="ca06a-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca06a-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ca06a-124">Minimum supported client</span></span><br/> | <span data-ttu-id="ca06a-125">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="ca06a-125">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ca06a-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ca06a-126">Minimum supported server</span></span><br/> | <span data-ttu-id="ca06a-127">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="ca06a-127">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="ca06a-128">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="ca06a-128">Namespace</span></span><br/>                | <span data-ttu-id="ca06a-129">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="ca06a-129">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="ca06a-130">MOF</span><span class="sxs-lookup"><span data-stu-id="ca06a-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ca06a-131"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ca06a-131"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="ca06a-132">DLL</span><span class="sxs-lookup"><span data-stu-id="ca06a-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ca06a-133"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ca06a-133"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca06a-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ca06a-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca06a-135">**MDM \_ клиентцертификатеинсталл \_ Install03**</span><span class="sxs-lookup"><span data-stu-id="ca06a-135">**MDM\_ClientCertificateInstall\_Install03**</span></span>](mdm-clientcertificateinstall-install03.md)
</dt> <dt>

[<span data-ttu-id="ca06a-136">Использование сценариев PowerShell с WMI Bridge Provider</span><span class="sxs-lookup"><span data-stu-id="ca06a-136">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

