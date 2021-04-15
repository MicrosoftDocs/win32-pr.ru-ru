---
description: Метод Сетдинамикреконнектлевел задает уровень динамического повторного подключения во время подготовки к просмотру.
ms.assetid: 092f3464-84a2-48b0-9647-66fe27e9706d
title: 'Метод Ирендеренгине:: Сетдинамикреконнектлевел (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.SetDynamicReconnectLevel
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ae02fb6158b58cd5785aa7df539651acfbea5db8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105676026"
---
# <a name="irenderenginesetdynamicreconnectlevel-method"></a><span data-ttu-id="62764-103">Метод Ирендеренгине:: Сетдинамикреконнектлевел</span><span class="sxs-lookup"><span data-stu-id="62764-103">IRenderEngine::SetDynamicReconnectLevel method</span></span>

> [!Note]  
> <span data-ttu-id="62764-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="62764-104">\[Deprecated.</span></span> <span data-ttu-id="62764-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="62764-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="62764-106">`SetDynamicReconnectLevel`Метод задает уровень динамического повторного подключения во время подготовки к просмотру.</span><span class="sxs-lookup"><span data-stu-id="62764-106">The `SetDynamicReconnectLevel` method sets the level of dynamic reconnection during rendering.</span></span>

## <a name="syntax"></a><span data-ttu-id="62764-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="62764-107">Syntax</span></span>


```C++
HRESULT SetDynamicReconnectLevel(
   DWORD Level
);
```



## <a name="parameters"></a><span data-ttu-id="62764-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="62764-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62764-109">*Level*</span><span class="sxs-lookup"><span data-stu-id="62764-109">*Level*</span></span> 
</dt> <dd>

<span data-ttu-id="62764-110">Сочетание [**динамических флагов переподключения**](dynamic-reconnection-flags.md), определяющих уровень динамического повторного подключения.</span><span class="sxs-lookup"><span data-stu-id="62764-110">Combination of [**Dynamic Reconnection Flags**](dynamic-reconnection-flags.md), specifying the level of dynamic reconnection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62764-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="62764-111">Return value</span></span>

<span data-ttu-id="62764-112">Возвращает одно из следующих значений **HRESULT** :</span><span class="sxs-lookup"><span data-stu-id="62764-112">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="62764-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="62764-113">Return code</span></span>                                                                               | <span data-ttu-id="62764-114">Описание</span><span class="sxs-lookup"><span data-stu-id="62764-114">Description</span></span>                 |
|-------------------------------------------------------------------------------------------|-----------------------------|
| <dl> <span data-ttu-id="62764-115"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="62764-115"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="62764-116">Успешно.</span><span class="sxs-lookup"><span data-stu-id="62764-116">Success.</span></span><br/>         |
| <dl> <span data-ttu-id="62764-117"><dt>**E \_ нотимпл**</dt></span><span class="sxs-lookup"><span data-stu-id="62764-117"><dt>**E\_NOTIMPL**</dt></span></span> </dl> | <span data-ttu-id="62764-118">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="62764-118">Not implemented.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="62764-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="62764-119">Remarks</span></span>

<span data-ttu-id="62764-120">По умолчанию базовый механизм визуализации загружает каждый источник перед отрисовкой проекта.</span><span class="sxs-lookup"><span data-stu-id="62764-120">By default, the basic render engine loads every source before rendering a project.</span></span> <span data-ttu-id="62764-121">Это может привести к длительному времени запуска.</span><span class="sxs-lookup"><span data-stu-id="62764-121">This can result in a long start-up time.</span></span> <span data-ttu-id="62764-122">При динамическом повторном подключении источники загружаются только при необходимости.</span><span class="sxs-lookup"><span data-stu-id="62764-122">With dynamic reconnection, sources are loaded only when needed.</span></span> <span data-ttu-id="62764-123">Это может сократить время запуска, но, возможно, мешает плавному воспроизведению.</span><span class="sxs-lookup"><span data-stu-id="62764-123">This can shorten the start-up time, but possibly interfere with smooth playback.</span></span> <span data-ttu-id="62764-124">Как правило, чем больше фрагментов исходного кода используется в проекте, тем больше возможностей может быть выгодно при динамическом повторном подключении.</span><span class="sxs-lookup"><span data-stu-id="62764-124">Generally, the more source clips that a project uses, the more you might benefit from dynamic reconnection.</span></span>

<span data-ttu-id="62764-125">Модуль интеллектуального просмотра не реализует этот метод.</span><span class="sxs-lookup"><span data-stu-id="62764-125">The smart render engine does not implement this method.</span></span>

> [!Note]  
> <span data-ttu-id="62764-126">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="62764-126">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="62764-127">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="62764-127">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="62764-128">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="62764-128">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="62764-129">Требования</span><span class="sxs-lookup"><span data-stu-id="62764-129">Requirements</span></span>



| <span data-ttu-id="62764-130">Требование</span><span class="sxs-lookup"><span data-stu-id="62764-130">Requirement</span></span> | <span data-ttu-id="62764-131">Значение</span><span class="sxs-lookup"><span data-stu-id="62764-131">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="62764-132">Header</span><span class="sxs-lookup"><span data-stu-id="62764-132">Header</span></span><br/>  | <dl> <span data-ttu-id="62764-133"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="62764-133"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="62764-134">Библиотека</span><span class="sxs-lookup"><span data-stu-id="62764-134">Library</span></span><br/> | <dl> <span data-ttu-id="62764-135"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="62764-135"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62764-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="62764-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62764-137">**Интерфейс Ирендеренгине**</span><span class="sxs-lookup"><span data-stu-id="62764-137">**IRenderEngine Interface**</span></span>](irenderengine.md)
</dt> <dt>

[<span data-ttu-id="62764-138">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="62764-138">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




