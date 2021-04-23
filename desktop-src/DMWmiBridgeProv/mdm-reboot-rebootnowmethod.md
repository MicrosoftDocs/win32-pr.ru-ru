---
title: Метод Ребутновмесод класса MDM_Reboot
description: Этот метод выполняет перезагрузку устройства.
ms.assetid: b1bacad8-06db-4e56-9f3d-46c9a0036729
keywords:
- Метод Ребутновмесод
- Метод Ребутновмесод, класс MDM_Reboot
- Класс MDM_Reboot, метод Ребутновмесод
topic_type:
- apiref
api_name:
- MDM_Reboot.RebootNowMethod
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29d35d297858588ade6655ea84876c6e75abd719
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135195"
---
# <a name="rebootnowmethod-method-of-the-mdm_reboot-class"></a><span data-ttu-id="40db6-106">Метод Ребутновмесод \_ класса rereboot MDM</span><span class="sxs-lookup"><span data-stu-id="40db6-106">RebootNowMethod method of the MDM\_Reboot class</span></span>

<span data-ttu-id="40db6-107">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="40db6-107">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="40db6-108">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="40db6-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="40db6-109">Этот метод выполняет перезагрузку устройства.</span><span class="sxs-lookup"><span data-stu-id="40db6-109">This method executes a reboot of the device.</span></span> <span data-ttu-id="40db6-110">См. также [ребутнов](/windows/client-management/mdm/reboot-csp).</span><span class="sxs-lookup"><span data-stu-id="40db6-110">See also, [RebootNow](/windows/client-management/mdm/reboot-csp).</span></span>

## <a name="syntax"></a><span data-ttu-id="40db6-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="40db6-111">Syntax</span></span>


```mof
uint32 RebootNowMethod();
```



## <a name="parameters"></a><span data-ttu-id="40db6-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="40db6-112">Parameters</span></span>

<span data-ttu-id="40db6-113">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="40db6-113">This method has no parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="40db6-114">Требования</span><span class="sxs-lookup"><span data-stu-id="40db6-114">Requirements</span></span>



| <span data-ttu-id="40db6-115">Требование</span><span class="sxs-lookup"><span data-stu-id="40db6-115">Requirement</span></span> | <span data-ttu-id="40db6-116">Значение</span><span class="sxs-lookup"><span data-stu-id="40db6-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="40db6-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="40db6-117">Minimum supported client</span></span><br/> | <span data-ttu-id="40db6-118">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="40db6-118">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="40db6-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="40db6-119">Minimum supported server</span></span><br/> | <span data-ttu-id="40db6-120">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="40db6-120">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="40db6-121">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="40db6-121">Namespace</span></span><br/>                | <span data-ttu-id="40db6-122">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="40db6-122">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="40db6-123">MOF</span><span class="sxs-lookup"><span data-stu-id="40db6-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="40db6-124"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="40db6-124"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl>      |
| <span data-ttu-id="40db6-125">DLL</span><span class="sxs-lookup"><span data-stu-id="40db6-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="40db6-126"><dt>MOF \\DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="40db6-126"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40db6-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="40db6-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40db6-128">**Перезагрузка MDM \_**</span><span class="sxs-lookup"><span data-stu-id="40db6-128">**MDM\_Reboot**</span></span>](mdm-reboot.md)
</dt> </dl>

 

