---
description: Задает время в образце элемента управления.
ms.assetid: 17ffa106-8b6b-4077-895c-03400505c2a0
title: Метод Контролсамплетимес класса Msvm_MetricService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricService.ControlSampleTimes
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 1bb3797523153592610714406306035f59fc844c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264405"
---
# <a name="controlsampletimes-method-of-the-msvm_metricservice-class"></a><span data-ttu-id="a3148-103">Метод Контролсамплетимес \_ класса Метриксервице мсвм</span><span class="sxs-lookup"><span data-stu-id="a3148-103">ControlSampleTimes method of the Msvm\_MetricService class</span></span>

<span data-ttu-id="a3148-104">Задает время в образце элемента управления.</span><span class="sxs-lookup"><span data-stu-id="a3148-104">Sets the control sample times.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3148-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a3148-105">Syntax</span></span>


```mof
uint32 ControlSampleTimes(
  [in] datetime StartSampleTime,
  [in] datetime PreferredSampleInterval,
  [in] boolean  RestartGathering
);
```



## <a name="parameters"></a><span data-ttu-id="a3148-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a3148-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3148-107">*Стартсамплетиме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a3148-107">*StartSampleTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3148-108">Момент времени, когда необходимо запустить выборку для метрик.</span><span class="sxs-lookup"><span data-stu-id="a3148-108">Point in time when sampling for the metrics is to be started.</span></span>

<span data-ttu-id="a3148-109">Значение 99990101000000.000000 + 000 указывает, что выборка должна начаться в следующий раз, когда она будет синхронизирована с полным временем.</span><span class="sxs-lookup"><span data-stu-id="a3148-109">A value of 99990101000000.000000+000 shall indicate that sampling should start at the next time it is synchronized to the full hour.</span></span> <span data-ttu-id="a3148-110">Выборка синхронизируется с полным часами (в секундах), так как интервал выборки от полуночи по модулю в секундах равен 0.</span><span class="sxs-lookup"><span data-stu-id="a3148-110">Sampling is synchronized to the full hour if seconds since midnight modulo sample interval in seconds is equal to 0.</span></span>

</dd> <dt>

<span data-ttu-id="a3148-111">*Преферредсамплеинтервал* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a3148-111">*PreferredSampleInterval* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3148-112">Предпочтительное время интервала выборки.</span><span class="sxs-lookup"><span data-stu-id="a3148-112">Preferred sample interval time.</span></span> <span data-ttu-id="a3148-113">Чтобы получить коррелированные метрики, рекомендуется выбрать интервал выборки таким образом, чтобы интервал выборки по модулю 3600 в секундах был равен 0.</span><span class="sxs-lookup"><span data-stu-id="a3148-113">In order to get correlatable metrics, it is recommended that the sample interval be chosen in a way that 3600 modulo sample interval time in seconds is equal to 0.</span></span>

<span data-ttu-id="a3148-114">Для определения того, учитывается ли запрошенное время интервала выборки, отвечает реализация службы метрик CIM.</span><span class="sxs-lookup"><span data-stu-id="a3148-114">It is the responsibility of the CIM metric service implementation to decide whether the requested sample interval time is honored.</span></span>

<span data-ttu-id="a3148-115">Клиент CIM может проверить, учитывают ли поставщики метрик запрошенное время интервала выборки, извлекая связанные экземпляры Басеметрикдефинитион и проверяя содержимое свойства "CIM \_ басеметрикдефинитион. SampleInterval".</span><span class="sxs-lookup"><span data-stu-id="a3148-115">The CIM client can check whether or not the metric providers are honoring the requested sample interval time by retrieving related BaseMetricDefinition instances and checking the contents of the "CIM\_BaseMetricDefinition.SampleInterval" property.</span></span>

</dd> <dt>

<span data-ttu-id="a3148-116">*Рестартгасеринг* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a3148-116">*RestartGathering* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3148-117">Логическое значение, которое при задании значения TRUE требует, чтобы сбор всех метрик, связанных со службой метрик, был повторно запущен с помощью этого вызова метода.</span><span class="sxs-lookup"><span data-stu-id="a3148-117">Boolean that when set to TRUE requests that gathering of all metrics associated to the metric service is re-started with this method call.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3148-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a3148-118">Return value</span></span>

<span data-ttu-id="a3148-119">Этот метод возвращает одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="a3148-119">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="a3148-120">**Успешно** (0)</span><span class="sxs-lookup"><span data-stu-id="a3148-120">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a3148-121">**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="a3148-121">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="a3148-122">**Сбой** (2)</span><span class="sxs-lookup"><span data-stu-id="a3148-122">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="a3148-123">**Метод зарезервирован** (..)</span><span class="sxs-lookup"><span data-stu-id="a3148-123">**Method Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="a3148-124">**Зависит от поставщика** (32768.65 535)</span><span class="sxs-lookup"><span data-stu-id="a3148-124">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="a3148-125">Требования</span><span class="sxs-lookup"><span data-stu-id="a3148-125">Requirements</span></span>



| <span data-ttu-id="a3148-126">Требование</span><span class="sxs-lookup"><span data-stu-id="a3148-126">Requirement</span></span> | <span data-ttu-id="a3148-127">Значение</span><span class="sxs-lookup"><span data-stu-id="a3148-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3148-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a3148-128">Minimum supported client</span></span><br/> | <span data-ttu-id="a3148-129">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="a3148-129">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="a3148-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a3148-130">Minimum supported server</span></span><br/> | <span data-ttu-id="a3148-131">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="a3148-131">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="a3148-132">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="a3148-132">Namespace</span></span><br/>                | <span data-ttu-id="a3148-133">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="a3148-133">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="a3148-134">MOF</span><span class="sxs-lookup"><span data-stu-id="a3148-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a3148-135"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a3148-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a3148-136">DLL</span><span class="sxs-lookup"><span data-stu-id="a3148-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a3148-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a3148-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a3148-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a3148-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3148-139">**Мсвм \_ метриксервице**</span><span class="sxs-lookup"><span data-stu-id="a3148-139">**Msvm\_MetricService**</span></span>](msvm-metricservice.md)
</dt> </dl>

 

 




