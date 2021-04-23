---
description: Считывает активную конфигурацию сборщика.
ms.assetid: ea26142d-5dcd-466d-b9df-5349f58a190f
ms.tgt_platform: multiple
title: Метод настройки класса Control
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.GetConfiguration
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: 5adfedb833043ffc56da09c7bdab95c1c4698587
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990347"
---
# <a name="getconfiguration-method-of-the-control-class"></a><span data-ttu-id="71c53-103">Метод настройки класса Control</span><span class="sxs-lookup"><span data-stu-id="71c53-103">GetConfiguration method of the Control class</span></span>

<span data-ttu-id="71c53-104">Считывает активную конфигурацию сборщика.</span><span class="sxs-lookup"><span data-stu-id="71c53-104">Read the active configuration of the collector.</span></span>

## <a name="syntax"></a><span data-ttu-id="71c53-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="71c53-105">Syntax</span></span>


```mof
Uint32 GetConfiguration(
  [out] Uint32 TimestampLow,
  [out] Uint32 TimestampHigh
);
```



## <a name="parameters"></a><span data-ttu-id="71c53-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="71c53-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71c53-107">*Тиместамплов* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="71c53-107">*TimestampLow* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="71c53-108">При возврате из этого метода этот параметр содержит младшие биты метки времени, указывающие, когда была задана конфигурация.</span><span class="sxs-lookup"><span data-stu-id="71c53-108">When this method returns, this parameter contains the low-order bits of a timestamp that indicates when the configuration was set.</span></span>

</dd> <dt>

<span data-ttu-id="71c53-109">*Тиместамфигх* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="71c53-109">*TimestampHigh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="71c53-110">При возврате из этого метода этот параметр содержит старшие биты метки времени, указывающие, когда была задана конфигурация.</span><span class="sxs-lookup"><span data-stu-id="71c53-110">When this method returns, this parameter contains the high-order bits of a timestamp that indicates when the configuration was set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71c53-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="71c53-111">Return value</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="71c53-112">0</span><span class="sxs-lookup"><span data-stu-id="71c53-112">0</span></span>

<span data-ttu-id="71c53-113">Сбой</span><span class="sxs-lookup"><span data-stu-id="71c53-113">Failure</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="71c53-114">1</span><span class="sxs-lookup"><span data-stu-id="71c53-114">1</span></span>

<span data-ttu-id="71c53-115">Успешно</span><span class="sxs-lookup"><span data-stu-id="71c53-115">Success</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="71c53-116">Требования</span><span class="sxs-lookup"><span data-stu-id="71c53-116">Requirements</span></span>



| <span data-ttu-id="71c53-117">Требование</span><span class="sxs-lookup"><span data-stu-id="71c53-117">Requirement</span></span> | <span data-ttu-id="71c53-118">Значение</span><span class="sxs-lookup"><span data-stu-id="71c53-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71c53-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="71c53-119">Minimum supported client</span></span><br/> | <span data-ttu-id="71c53-120">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="71c53-120">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="71c53-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="71c53-121">Minimum supported server</span></span><br/> | <span data-ttu-id="71c53-122">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="71c53-122">Windows Server 2016</span></span><br/>                                                                       |
| <span data-ttu-id="71c53-123">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="71c53-123">Namespace</span></span><br/>                | <span data-ttu-id="71c53-124">Корневой \\ узел Microsoft \\ Windows \\ бутевентколлектор</span><span class="sxs-lookup"><span data-stu-id="71c53-124">Root\\Microsoft\\Windows\\BootEventCollector</span></span><br/>                                              |
| <span data-ttu-id="71c53-125">MOF</span><span class="sxs-lookup"><span data-stu-id="71c53-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="71c53-126"><dt>Бутевентколлекторвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="71c53-126"><dt>BootEventCollectorWMI.mof</dt></span></span> </dl> |
| <span data-ttu-id="71c53-127">DLL</span><span class="sxs-lookup"><span data-stu-id="71c53-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="71c53-128"><dt>BEvtCol.exe</dt></span><span class="sxs-lookup"><span data-stu-id="71c53-128"><dt>BEvtCol.exe</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="71c53-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="71c53-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71c53-130">**Элемента**</span><span class="sxs-lookup"><span data-stu-id="71c53-130">**Control**</span></span>](control.md)
</dt> </dl>

 

 




