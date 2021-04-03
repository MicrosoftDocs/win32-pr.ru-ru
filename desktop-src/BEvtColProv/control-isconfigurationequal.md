---
description: Сравните аргумент с активной конфигурацией сборщика.
ms.assetid: 8decb674-c905-4eb6-9f78-7bc7b99db908
ms.tgt_platform: multiple
title: Метод Исконфигуратионекуал класса Control
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.IsConfigurationEqual
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: fb471f144a39519f1f724db458b57b624db2846d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103806989"
---
# <a name="isconfigurationequal-method-of-the-control-class"></a><span data-ttu-id="9193b-103">Метод Исконфигуратионекуал класса Control</span><span class="sxs-lookup"><span data-stu-id="9193b-103">IsConfigurationEqual method of the Control class</span></span>

<span data-ttu-id="9193b-104">Сравните аргумент с активной конфигурацией сборщика.</span><span class="sxs-lookup"><span data-stu-id="9193b-104">Compare the argument with the active configuration of the collector.</span></span>

## <a name="syntax"></a><span data-ttu-id="9193b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9193b-105">Syntax</span></span>


```mof
Uint32 IsConfigurationEqual(
  [in] string Config
);
```



## <a name="parameters"></a><span data-ttu-id="9193b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9193b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9193b-107">*Конфигурация* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9193b-107">*Config* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9193b-108">Конфигурация, сравниваемая с активной конфигурацией.</span><span class="sxs-lookup"><span data-stu-id="9193b-108">The configuration to compare to the active configuration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9193b-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9193b-109">Return value</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="9193b-110">0</span><span class="sxs-lookup"><span data-stu-id="9193b-110">0</span></span>

<span data-ttu-id="9193b-111">Сбой</span><span class="sxs-lookup"><span data-stu-id="9193b-111">Failure</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="9193b-112">1</span><span class="sxs-lookup"><span data-stu-id="9193b-112">1</span></span>

<span data-ttu-id="9193b-113">Успешно</span><span class="sxs-lookup"><span data-stu-id="9193b-113">Success</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9193b-114">Требования</span><span class="sxs-lookup"><span data-stu-id="9193b-114">Requirements</span></span>



| <span data-ttu-id="9193b-115">Требование</span><span class="sxs-lookup"><span data-stu-id="9193b-115">Requirement</span></span> | <span data-ttu-id="9193b-116">Значение</span><span class="sxs-lookup"><span data-stu-id="9193b-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9193b-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9193b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="9193b-118">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="9193b-118">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="9193b-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9193b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="9193b-120">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="9193b-120">Windows Server 2016</span></span><br/>                                                                       |
| <span data-ttu-id="9193b-121">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="9193b-121">Namespace</span></span><br/>                | <span data-ttu-id="9193b-122">Корневой \\ узел Microsoft \\ Windows \\ бутевентколлектор</span><span class="sxs-lookup"><span data-stu-id="9193b-122">Root\\Microsoft\\Windows\\BootEventCollector</span></span><br/>                                              |
| <span data-ttu-id="9193b-123">MOF</span><span class="sxs-lookup"><span data-stu-id="9193b-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9193b-124"><dt>Бутевентколлекторвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9193b-124"><dt>BootEventCollectorWMI.mof</dt></span></span> </dl> |
| <span data-ttu-id="9193b-125">DLL</span><span class="sxs-lookup"><span data-stu-id="9193b-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9193b-126"><dt>BEvtCol.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9193b-126"><dt>BEvtCol.exe</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="9193b-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9193b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9193b-128">**Элемента**</span><span class="sxs-lookup"><span data-stu-id="9193b-128">**Control**</span></span>](control.md)
</dt> </dl>

 

 




