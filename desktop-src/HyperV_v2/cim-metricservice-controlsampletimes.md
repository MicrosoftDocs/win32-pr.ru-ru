---
description: Позволяет запустить сбор метрик точки во времени и указать предпочтительное время интервала выборки для периодического сбора данных.
ms.assetid: 3dd6dc16-a618-49ff-bbaf-cfa25c249cf1
title: Метод Контролсамплетимес класса CIM_MetricService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MetricService.ControlSampleTimes
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 2e32d184199ff7ddc63be5d1fcfcd4ea376dad89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683556"
---
# <a name="controlsampletimes-method-of-the-cim_metricservice-class"></a><span data-ttu-id="8d9ed-103">Метод Контролсамплетимес \_ класса CIM метриксервице</span><span class="sxs-lookup"><span data-stu-id="8d9ed-103">ControlSampleTimes method of the CIM\_MetricService class</span></span>

<span data-ttu-id="8d9ed-104">Позволяет запустить сбор метрик точки во времени и указать предпочтительное время интервала выборки для периодического сбора данных.</span><span class="sxs-lookup"><span data-stu-id="8d9ed-104">Allows specification of the point in time metric gathering is to be started and to specify the preferred sample interval time for periodic data gathering.</span></span>

<span data-ttu-id="8d9ed-105">При запуске выборки для дополнительных метрик можно использовать параметры, заданные этим методом.</span><span class="sxs-lookup"><span data-stu-id="8d9ed-105">Whenever sampling for additional metrics is started, the settings specified by this method may be used.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d9ed-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8d9ed-106">Syntax</span></span>


```mof
uint32 ControlSampleTimes(
  [in] datetime StartSampleTime,
  [in] datetime PreferredSampleInterval,
  [in] boolean  RestartGathering
);
```



## <a name="parameters"></a><span data-ttu-id="8d9ed-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="8d9ed-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d9ed-108">*Стартсамплетиме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8d9ed-108">*StartSampleTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d9ed-109">Момент времени, когда необходимо запустить выборку для метрик.</span><span class="sxs-lookup"><span data-stu-id="8d9ed-109">Point in time when sampling for the metrics is to be started.</span></span>

<span data-ttu-id="8d9ed-110">Значение 99990101000000.000000 + 000 указывает, что выборка должна начаться в следующий раз, когда она будет синхронизирована с полным временем.</span><span class="sxs-lookup"><span data-stu-id="8d9ed-110">A value of 99990101000000.000000+000 shall indicate that sampling should start at the next time it is synchronized to the full hour.</span></span> <span data-ttu-id="8d9ed-111">Выборка синхронизируется с полным часами (в секундах), так как интервал выборки от полуночи по модулю в секундах равен 0.</span><span class="sxs-lookup"><span data-stu-id="8d9ed-111">Sampling is synchronized to the full hour if seconds since midnight modulo sample interval in seconds is equal to 0.</span></span>

</dd> <dt>

<span data-ttu-id="8d9ed-112">*Преферредсамплеинтервал* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8d9ed-112">*PreferredSampleInterval* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d9ed-113">Предпочтительное время интервала выборки.</span><span class="sxs-lookup"><span data-stu-id="8d9ed-113">Preferred sample interval time.</span></span> <span data-ttu-id="8d9ed-114">Чтобы получить коррелированные метрики, рекомендуется выбрать интервал выборки таким образом, чтобы интервал выборки по модулю 3600 в секундах был равен 0.</span><span class="sxs-lookup"><span data-stu-id="8d9ed-114">In order to get correlatable metrics, it is recommended that the sample interval be chosen in a way that 3600 modulo sample interval time in seconds is equal to 0.</span></span>

<span data-ttu-id="8d9ed-115">Для определения того, учитывается ли запрошенное время интервала выборки, отвечает реализация службы метрик CIM.</span><span class="sxs-lookup"><span data-stu-id="8d9ed-115">It is the responsibility of the CIM metric service implementation to decide whether the requested sample interval time is honored.</span></span>

<span data-ttu-id="8d9ed-116">Клиент CIM может проверить, учитывают ли поставщики метрик запрошенное время интервала выборки, извлекая связанные экземпляры Басеметрикдефинитион и проверяя содержимое [**CIM \_ басеметрикдефинитион**](cim-basemetricdefinition.md).**Свойство SampleInterval** .</span><span class="sxs-lookup"><span data-stu-id="8d9ed-116">The CIM client can check whether or not the metric providers are honoring the requested sample interval time by retrieving related BaseMetricDefinition instances and checking the contents of the [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md).**SampleInterval** property.</span></span>

</dd> <dt>

<span data-ttu-id="8d9ed-117">*Рестартгасеринг* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8d9ed-117">*RestartGathering* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d9ed-118">**Значение true** , чтобы запрос на сбор всех метрик, связанных со службой метрик, был повторно запущен с помощью этого вызова метода.</span><span class="sxs-lookup"><span data-stu-id="8d9ed-118">**TRUE** to request that gathering of all metrics associated to the metric service is re-started with this method call.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d9ed-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8d9ed-119">Return value</span></span>

<span data-ttu-id="8d9ed-120">Возвращает значение 0 в случае успешного выполнения; в противном случае возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="8d9ed-120">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="8d9ed-121">**Успешно** (0)</span><span class="sxs-lookup"><span data-stu-id="8d9ed-121">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="8d9ed-122">**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="8d9ed-122">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="8d9ed-123">**Сбой** (2)</span><span class="sxs-lookup"><span data-stu-id="8d9ed-123">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="8d9ed-124">**Метод зарезервирован** (..)</span><span class="sxs-lookup"><span data-stu-id="8d9ed-124">**Method Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="8d9ed-125">**Зависит от поставщика** (32768.65 535)</span><span class="sxs-lookup"><span data-stu-id="8d9ed-125">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="8d9ed-126">Требования</span><span class="sxs-lookup"><span data-stu-id="8d9ed-126">Requirements</span></span>



| <span data-ttu-id="8d9ed-127">Требование</span><span class="sxs-lookup"><span data-stu-id="8d9ed-127">Requirement</span></span> | <span data-ttu-id="8d9ed-128">Значение</span><span class="sxs-lookup"><span data-stu-id="8d9ed-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8d9ed-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8d9ed-129">Minimum supported client</span></span><br/> | <span data-ttu-id="8d9ed-130">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="8d9ed-130">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="8d9ed-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8d9ed-131">Minimum supported server</span></span><br/> | <span data-ttu-id="8d9ed-132">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="8d9ed-132">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="8d9ed-133">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="8d9ed-133">Namespace</span></span><br/>                | <span data-ttu-id="8d9ed-134">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="8d9ed-134">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="8d9ed-135">MOF</span><span class="sxs-lookup"><span data-stu-id="8d9ed-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8d9ed-136"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8d9ed-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="8d9ed-137">DLL</span><span class="sxs-lookup"><span data-stu-id="8d9ed-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8d9ed-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8d9ed-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="8d9ed-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8d9ed-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d9ed-140">**\_МЕТРИКСЕРВИЦЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="8d9ed-140">**CIM\_MetricService**</span></span>](cim-metricservice.md)
</dt> </dl>

 

 




