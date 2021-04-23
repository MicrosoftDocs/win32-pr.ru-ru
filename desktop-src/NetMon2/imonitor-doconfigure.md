---
description: Метод Доконфигуре должен быть реализован монитором. МКСВК вызывает этот метод для получения сведений о конфигурации для записи.
ms.assetid: bc2a3246-28dc-4452-a98e-a8a2447bb127
title: 'Имонитор: метод:D Оконфигуре (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitor.DoConfigure
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: e9a0ba2ade1095f291d5cb325a0902e6caeac3f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104144650"
---
# <a name="imonitordoconfigure-method"></a><span data-ttu-id="8cd9c-104">Имонитор: метод:D Оконфигуре</span><span class="sxs-lookup"><span data-stu-id="8cd9c-104">IMonitor::DoConfigure method</span></span>

<span data-ttu-id="8cd9c-105">Метод **доконфигуре** должен быть реализован монитором.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-105">The **DoConfigure** method must be implemented by the monitor.</span></span> <span data-ttu-id="8cd9c-106">МКСВК вызывает этот метод для получения сведений о конфигурации для записи.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-106">The MCSVC calls this method to obtain configuration information for the capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="8cd9c-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8cd9c-107">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE DoConfigure(
  [in]  char *pName,
  [in]  char *pConfiguration,
  [out] char **ppScriptInstance
);
```



## <a name="parameters"></a><span data-ttu-id="8cd9c-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="8cd9c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8cd9c-109">*pName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8cd9c-109">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8cd9c-110">Имя экземпляра монитора.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-110">Name of an instance of the monitor.</span></span>

</dd> <dt>

<span data-ttu-id="8cd9c-111">*пконфигуратион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8cd9c-111">*pConfiguration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8cd9c-112">Строка конфигурации, предоставленная параметром МКСВК.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-112">Configuration string provided by the MCSVC.</span></span> <span data-ttu-id="8cd9c-113">Монитор должен проанализировать эту строку на наличие данных конфигурации.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-113">The monitor must parse this string for configuration data.</span></span>

</dd> <dt>

<span data-ttu-id="8cd9c-114">*ппскриптинстанце* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="8cd9c-114">*ppScriptInstance* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8cd9c-115">Адрес строки HTML, используемой для настройки монитора.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-115">Address of the HTML string used to configure the monitor.</span></span> <span data-ttu-id="8cd9c-116">Если для конфигурации используется скрипт по умолчанию, это значение должно быть равно **null**.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-116">If a default script is used for configuration, this value should be set to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8cd9c-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8cd9c-117">Return value</span></span>

<span data-ttu-id="8cd9c-118">Если метод выполнен успешно, возвращается значение S OK (то же, что и параметр "noreturn" \_ ), а мксвк запустит монитор.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-118">If the method is successful, the return value is S\_OK (which is the same as NOERROR), and the MCSVC will run the monitor.</span></span>

<span data-ttu-id="8cd9c-119">Если метод завершается неудачно, возвращаемое значение является кодом ошибки.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-119">If the method is unsuccessful, the return value is an error code.</span></span> <span data-ttu-id="8cd9c-120">Недопустимое возвращаемое значение \_ конфигурации монитора нмерр \_ \_ , но при возвращении этой ошибки монитор не может начаться до тех пор, пока будущий вызов **доконфигуре** не будет выполнен.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-120">A return value of NMERR\_MONITOR\_CONFIG\_FAILED is acceptable, but when this error is returned, the monitor cannot start until a future **DoConfigure** call succeeds.</span></span> <span data-ttu-id="8cd9c-121">Любая другая ошибка предотвращает включение экземпляра монитора.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-121">Any other error prevents the instance of the monitor from being enabled.</span></span>

## <a name="remarks"></a><span data-ttu-id="8cd9c-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8cd9c-122">Remarks</span></span>

<span data-ttu-id="8cd9c-123">МКСВК вызывает этот метод после подключения к сети и до вызова метода [ИРТК:: Configure](irtc-configure.md) .</span><span class="sxs-lookup"><span data-stu-id="8cd9c-123">The MCSVC calls this method after it has connected to the network and before the [IRTC::Configure](irtc-configure.md) method is called.</span></span>

<span data-ttu-id="8cd9c-124">Монитор может хранить сведения, предоставленные этим вызовом, обновлять HTML-скрипт или строку конфигурации, а также задавать [фильтр записи](capture-filters.md) в большом ДВОИЧНОМ объекте НПП.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-124">The monitor can store information provided by this call, update the HTML script or configuration string, and set the [capture filter](capture-filters.md) in the NPP BLOB.</span></span>

<span data-ttu-id="8cd9c-125">МКСВК может вызывать этот метод несколько раз, но он не может быть вызван во время записи данных монитором.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-125">The MCSVC may call this method several times, but it cannot be not called while the monitor is capturing data.</span></span> <span data-ttu-id="8cd9c-126">Обратите внимание, что каждый раз, когда [НПП](network-packet-providers.md) начинает запись, необходимо настроить подключение к сети.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-126">Note that every time an [NPP](network-packet-providers.md) starts a capture, the connection to the network must be configured.</span></span> <span data-ttu-id="8cd9c-127">Это ограничение включает в себя ситуации, в которых НПП запускается и останавливает одну и ту же запись.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-127">This restriction includes situations in which the NPP starts and stops the same capture.</span></span>

## <a name="requirements"></a><span data-ttu-id="8cd9c-128">Требования</span><span class="sxs-lookup"><span data-stu-id="8cd9c-128">Requirements</span></span>



| <span data-ttu-id="8cd9c-129">Требование</span><span class="sxs-lookup"><span data-stu-id="8cd9c-129">Requirement</span></span> | <span data-ttu-id="8cd9c-130">Значение</span><span class="sxs-lookup"><span data-stu-id="8cd9c-130">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="8cd9c-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8cd9c-131">Minimum supported client</span></span><br/> | <span data-ttu-id="8cd9c-132">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="8cd9c-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="8cd9c-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8cd9c-133">Minimum supported server</span></span><br/> | <span data-ttu-id="8cd9c-134">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="8cd9c-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="8cd9c-135">Заголовок</span><span class="sxs-lookup"><span data-stu-id="8cd9c-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="8cd9c-136"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="8cd9c-136"><dt>Netmon.h</dt></span></span> </dl> |



 

 




